---
date: 2025-12-04
description: Tìm hiểu cách trích xuất hình ảnh từ tệp OneNote và chuyển đổi OneNote
  sang văn bản trong Java bằng Aspose.Note. Hướng dẫn từng bước kèm ví dụ mã.
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Trích xuất hình ảnh từ OneNote bằng Document Visitor - Java
url: /vi/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Trích xuất hình ảnh từ OneNote bằng Document Visitor - Java

## Giới thiệu

Aspose.Note for Java giúp bạn **trích xuất hình ảnh từ OneNote** trong các sổ tay cũng như đọc tệp `.one` gốc trong Java. Trong hướng dẫn này, chúng tôi sẽ đưa bạn qua một ví dụ thực tế đầy đủ, cho thấy cách tải tệp OneNote, duyệt cấu trúc của nó bằng một `DocumentVisitor` tùy chỉnh, và lấy ra cả hình ảnh lẫn văn bản thuần. Khi kết thúc, bạn cũng sẽ biết cách **chuyển đổi OneNote sang văn bản** nếu chỉ cần nội dung văn bản.

## Câu trả lời nhanh
- **Thư viện tôi cần gì?** Aspose.Note for Java (liên kết tải xuống bên dưới).  
- **Tôi có thể chỉ trích xuất hình ảnh không?** Có – triển khai phương thức `VisitImageStart` trong một `DocumentVisitor`.  
- **Làm sao đọc tệp .one trong Java?** Dùng `new Document(path, new LoadOptions())`.  
- **Có cần giấy phép cho môi trường sản xuất không?** Cần giấy phép thương mại cho việc sử dụng không phải bản thử nghiệm.  
- **Phiên bản Java nào được hỗ trợ?** JDK 8 hoặc cao hơn.

## Yêu cầu trước

Trước khi bắt đầu, hãy đảm bảo bạn có:

1. Java Development Kit (JDK) 8 hoặc mới hơn đã được cài đặt.  
2. Thư viện Aspose.Note for Java đã tải về. Bạn có thể tải nó **[tại đây](https://releases.aspose.com/note/java/)**.  
3. Một tài liệu OneNote (`.one` file) mà bạn muốn trích xuất hình ảnh hoặc chuyển đổi sang văn bản.

## Nhập khẩu các gói

Đầu tiên, nhập các lớp cần thiết từ API Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Bước 1: Thiết lập Document Visitor tùy chỉnh

Tạo một lớp kế thừa `DocumentVisitor`. Lớp này sẽ được gọi cho mỗi nút trong tài liệu OneNote, cho phép bạn **trích xuất hình ảnh từ OneNote** và tùy chọn thu thập văn bản.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Bước 2: Triển khai các phương thức Visitor

Thêm các override cho các loại nút mà bạn quan tâm. Dưới đây chúng ta xử lý rich‑text, hình ảnh, tiêu đề, trang, outline và các phần tử outline. Phương thức `VisitImageStart` là nơi thực hiện việc trích xuất hình ảnh.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Tại sao cần triển khai các phương thức này?

- **Trích xuất hình ảnh từ OneNote:** `VisitImageStart` cung cấp cho bạn quyền truy cập trực tiếp vào các byte hình ảnh thô.  
- **Chuyển đổi OneNote sang văn bản:** `VisitRichTextStart` thu thập nội dung văn bản, cho phép thực hiện một thao tác **chuyển đổi OneNote sang văn bản** đơn giản.  
- **Đọc tệp .one trong Java:** Mẫu Visitor trừu tượng hoá cấu trúc tệp `.one` nền tảng, vì vậy bạn không cần tự phân tích định dạng nhị phân.

## Bước 3: Chạy Visitor từ phương thức Main của bạn

Tải tệp `.one`, khởi tạo visitor của bạn, và bắt đầu duyệt.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Các trường hợp sử dụng phổ biến

- **Báo cáo tự động:** Lấy hình ảnh và văn bản từ sổ tay họp OneNote để tạo bản tóm tắt PDF hoặc HTML.  
- **Di chuyển nội dung:** Chuyển đổi các kho lưu trữ OneNote cũ sang tệp văn bản thuần để lập chỉ mục hoặc nhập vào công cụ tìm kiếm.  
- **Trích xuất tài sản kỹ thuật số:** Thu thập các ảnh chụp màn hình, sơ đồ hoặc ảnh nhúng để tái sử dụng trong các ứng dụng khác.

## Khắc phục sự cố & Mẹo

- **Sổ tay lớn:** Nếu gặp vấn đề về bộ nhớ, hãy xử lý các trang riêng lẻ bằng cách kiểm tra `VisitPageStart` và chỉ tải tài nguyên cấp trang khi cần.  
- **Định dạng hình ảnh:** Đối tượng `Image` trả về các byte thô; bạn có thể cần xác định định dạng (PNG, JPEG) trước khi lưu.  
- **Lỗi giấy phép:** Đảm bảo bạn đã thiết lập giấy phép Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) trước khi tải tài liệu trong môi trường sản xuất.

## Câu hỏi thường gặp

**Q: Tôi có thể trích xuất các loại nội dung cụ thể nào từ tài liệu OneNote?**  
A: Có – chỉ cần ghi đè các phương thức visitor bạn cần (ví dụ, `VisitImageStart` cho hình ảnh, `VisitRichTextStart` cho văn bản).

**Q: Aspose.Note for Java có tương thích với các phiên bản tài liệu OneNote khác nhau không?**  
A: Hoàn toàn. Thư viện hỗ trợ tất cả các phiên bản tệp OneNote chính, vì vậy bạn có thể an tâm **đọc tệp .one trong Java** bất kể phiên bản gốc của OneNote.

**Q: Tôi có thể tích hợp quy trình trích xuất này vào ứng dụng Java của mình không?**  
A: Có. Mẫu Visitor hoạt động mượt mà trong bất kỳ dự án Java nào; chỉ cần thêm JAR thư viện và gọi ví dụ đã trình bày ở trên.

**Q: Aspose.Note for Java có hỗ trợ xử lý các tài OneNote phức tạp không?**  
A: Có. Các outline lồng nhau, phương tiện nhúng và dữ liệu tùy chỉnh đều được mở ra qua API visitor.

**Q: Có giới hạn nào về kích thước tài liệu OneNote có thể xử lý không?**  
A: Không có giới hạn cứng, nhưng các sổ tay cực lớn có thể yêu cầu nhiều bộ nhớ heap hơn; hãy cân nhắc xử lý từng trang một.

**Q: Làm sao chuyển đổi văn bản đã trích xuất thành tệp văn bản thuần?**  
A: Sau khi `myConverter.GetText()` trả về một `String`, ghi nó vào tệp bằng I/O chuẩn của Java (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Cập nhật lần cuối:** 2025-12-04  
**Kiểm tra với:** Aspose.Note for Java 24.10  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}