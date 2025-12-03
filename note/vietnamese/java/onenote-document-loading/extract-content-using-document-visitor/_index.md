---
date: 2025-12-03
description: Tìm hiểu cách chuyển OneNote sang văn bản bằng Aspose.Note cho Java.
  Hướng dẫn từng bước bao gồm trích xuất văn bản, trích xuất hình ảnh và cách đọc
  các tệp OneNote.
language: vi
linktitle: Convert OneNote to Text with Document Visitor – Java
second_title: Aspose.Note Java API
title: Chuyển OneNote sang Văn bản với Document Visitor – Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển OneNote sang Văn bản bằng Document Visitor – Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học **cách chuyển OneNote sang văn bản** bằng cách sử dụng Document Visitor của Aspose.Note cho Java. Cho dù bạn cần đọc các tệp OneNote một cách lập trình, trích xuất nội dung văn bản thuần, hoặc lấy ra các hình ảnh nhúng, Document Visitor cung cấp cho bạn khả năng kiểm soát chi tiết từng nút trong tài liệu .one.

## Câu trả lời nhanh
- **Ý nghĩa của “chuyển OneNote sang văn bản” là gì?** Nó có nghĩa là trích xuất biểu diễn văn bản thuần (và tùy chọn là hình ảnh) từ tệp .one.  
- **Thư viện nào hỗ trợ việc này?** Aspose.Note cho Java cung cấp API `DocumentVisitor`.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép trả phí cần thiết cho môi trường sản xuất.  
- **Tôi có thể trích xuất hình ảnh không?** Có – triển khai phương thức `VisitImageStart` để lấy ra các hình ảnh.  
- **Các yêu cầu trước là gì?** Java JDK 8+, JAR Aspose.Note cho Java, và một tệp .one để xử lý.

## “Chuyển OneNote sang văn bản” là gì?
Chuyển OneNote sang văn bản có nghĩa là đọc một tệp OneNote (.one) một cách lập trình và lấy nội dung văn bản, tiêu đề và các thành phần khác mà không cần giao diện OneNote gốc. Điều này hữu ích cho việc lập chỉ mục tìm kiếm, báo cáo, hoặc di chuyển nội dung sang các nền tảng khác.

## Tại sao sử dụng Document Visitor để **đọc tệp OneNote**?
Document Visitor tuân theo mẫu thiết kế Visitor, cho phép bạn duyệt qua từng phần tử (trang, outline, hình ảnh, đoạn văn bản phong phú, v.v.) trong tài liệu OneNote. So với việc tải toàn bộ tài liệu vào bộ nhớ và phân tích thủ công, cách tiếp cận Visitor có các ưu điểm:

* **Tiết kiệm bộ nhớ** – xử lý các nút từng cái một.  
* **Mở rộng** – bạn có thể thêm logic tùy chỉnh cho bất kỳ loại nút nào (ví dụ, trích xuất hình ảnh).  
* **Chính xác** – giữ nguyên cấu trúc gốc, đảm bảo bạn không bỏ lỡ nội dung ẩn.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

1. **Java Development Kit (JDK) 8 trở lên** đã được cài đặt.  
2. Thư viện **Aspose.Note cho Java** được tải xuống từ trang chính thức – [download here](https://releases.aspose.com/note/java/).  
3. Một **tài liệu OneNote** (`.one` file) mà bạn muốn chuyển sang văn bản.  

## Bước 1: Nhập các gói

Đầu tiên, nhập các lớp bạn sẽ cần để làm việc với Aspose.Note cho Java.

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

## Bước 2: Thiết lập lớp Document Visitor

Tạo một lớp kế thừa `DocumentVisitor`. Visitor tùy chỉnh này sẽ thu thập văn bản, đếm số nút, và (nếu muốn) lưu trữ hình ảnh.

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

## Bước 3: Triển khai các phương thức Visitor  

Ở đây chúng ta triển khai các callback cho các loại nút mà chúng ta quan tâm. Các phương thức tăng bộ đếm nút và, đối với `RichText`, nối văn bản thực tế vào `StringBuilder` của chúng ta. Bạn cũng có thể thêm logic để **trích xuất hình ảnh từ OneNote** bằng cách xử lý `VisitStart`.

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
    // Pro tip: you can save the image stream here if you need to extract images.
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

## Bước 4: Phương thức main – Chạy Visitor

Phương thức `main` tải một tệp OneNote, tạo một thể hiện của visitor tùy chỉnh của chúng ta, và bắt đầu duyệt. Sau khi duyệt, chúng ta in ra văn bản đã trích xuất và tổng số nút.

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
    System.out.println(myConverter.GetText());
    System.out.println(myConverter.NodeCount());
}
```

## Các trường hợp sử dụng phổ biến – **trích xuất hình ảnh từ OneNote**

* **Lập chỉ mục tìm kiếm** – Chuyển sổ tay OneNote sang văn bản thuần cho các công cụ tìm kiếm toàn văn.  
* **Di chuyển nội dung** – Đưa ghi chú vào CMS hoặc cổng tài liệu.  
* **Phân tích dữ liệu** – Lấy văn bản và hình ảnh để xử lý ngôn ngữ tự nhiên hoặc phân tích hình ảnh.  

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **NullPointerException khi đọc tệp .one** | Đảm bảo đường dẫn tệp (`dataDir`) kết thúc bằng dấu phân cách đường dẫn (`/` hoặc `\\`) và tệp tồn tại. |
| **Hình ảnh không được trích xuất** | Triển khai logic bên trong `VisitImageStart` để ghi `image.getImageData()` vào tệp hoặc luồng. |
| **Sổ tay lớn gây tiêu thụ bộ nhớ cao** | Xử lý tài liệu theo từng trang hoặc sử dụng API streaming nếu có. |

## Câu hỏi thường gặp

**H: Tôi có thể trích xuất các loại nội dung cụ thể từ tài liệu OneNote không?**  
Đáp: Có, bằng cách triển khai chỉ các phương thức visitor bạn cần (ví dụ, `VisitRichTextStart` cho văn bản, `VisitImageStart` cho hình ảnh).

**H: Aspose.Note cho Java có tương thích với các phiên bản tệp OneNote khác nhau không?**  
Đáp: Hoàn toàn. Thư viện hỗ trợ các tệp .one được tạo bởi các phiên bản gần đây của Microsoft OneNote.

**H: Tôi có thể tích hợp quá trình trích xuất này vào ứng dụng Java của mình không?**  
Đáp: Có. Mã được trình bày là một ví dụ tự chứa mà bạn có thể nhúng trực tiếp vào bất kỳ dự án Java nào.

**H: Aspose.Note cho Java có xử lý các cấu trúc OneNote phức tạp không?**  
Đáp: Có. Mẫu Visitor cho phép bạn duyệt các outline lồng nhau, nhóm và đối tượng nhúng mà không mất cấu trúc phân cấp.

**H: Có giới hạn nào về kích thước tài liệu OneNote có thể xử lý không?**  
Đáp: Mặc dù không có giới hạn cứng, sổ tay cực lớn có thể yêu cầu nhiều bộ nhớ heap hơn; hãy cân nhắc xử lý chúng theo từng phần.

**H: Làm thế nào để trích xuất hình ảnh từ OneNote?**  
Đáp: Triển khai phương thức `VisitImageStart` để truy cập `image.getImageData()` và ghi các byte vào tệp.

---

**Cập nhật lần cuối:** 2025-12-03  
**Kiểm thử với:** Aspose.Note cho Java 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}