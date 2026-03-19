---
date: 2026-03-19
description: Tìm hiểu cách thêm hình ảnh vào OneNote bằng Aspose.Note cho Java. Hướng
  dẫn chi tiết này chỉ ra cách tạo tài liệu OneNote, chèn hình ảnh vào OneNote và
  lưu OneNote dưới dạng PDF.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Cách thêm hình ảnh vào OneNote bằng Java – Tạo tài liệu và chèn hình
url: /vi/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách thêm hình ảnh vào OneNote bằng Java – Tạo tài liệu và chèn hình ảnh

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học **cách thêm hình ảnh vào OneNote** bằng cách sử dụng Aspose.Note Java API. Chúng tôi sẽ hướng dẫn bạn tạo một tài liệu OneNote từ đầu, chèn một hình ảnh và lưu kết quả dưới dạng PDF. Dù bạn đang xây dựng công cụ báo cáo, tự động ghi chú, hay chỉ cần nhúng đồ họa một cách lập trình, hướng dẫn này cung cấp cho bạn một lộ trình rõ ràng, thực tế.

## Câu trả lời nhanh
- **Thư viện tôi cần là gì?** Aspose.Note for Java.  
- **Tôi có thể chèn bất kỳ định dạng hình ảnh nào không?** JPEG, PNG, BMP, GIF và nhiều định dạng khác được hỗ trợ.  
- **Các định dạng đầu ra nào có sẵn?** Bạn có thể lưu dưới dạng OneNote, PDF, XPS, HTML, v.v.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Có, cần giấy phép thương mại cho việc sử dụng không phải thử nghiệm.  
- **Mã có đa nền tảng không?** Chắc chắn – Java chạy trên Windows, Linux và macOS.

## Cách thêm hình ảnh vào OneNote bằng Java

Thêm một hình ảnh vào OneNote có nghĩa là nhúng một tệp hình ảnh vào trang OneNote một cách lập trình để nó hiển thị cùng với văn bản, đề mục hoặc các yếu tố khác. Aspose.Note API trừu tượng hoá định dạng tệp OneNote, cho phép bạn tập trung vào nội dung thay vì cấu trúc XML bên dưới.

### Tại sao nhúng hình ảnh vào OneNote?

- **Tự động hoá:** Tự động tạo biên bản họp với ảnh chụp màn hình.  
- **Nhất quán:** Đảm bảo mọi trang tuân theo cùng một bố cục và thương hiệu.  
- **Tích hợp:** Kết hợp dữ liệu từ các hệ thống khác (ví dụ: biểu đồ) trực tiếp vào sổ tay OneNote.  
- **Đa nền tảng:** Java cho phép bạn chạy cùng một mã trên bất kỳ máy chủ hoặc môi trường máy tính để bàn nào.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có những thứ sau:

1. **Java Development Kit (JDK)** – bất kỳ phiên bản mới nào (8 trở lên).  
2. **Thư viện Aspose.Note cho Java** – tải xuống từ [website](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình chỉnh sửa nào tương thích với Java mà bạn thích.  

## Nhập các gói

Bắt đầu bằng cách nhập các lớp cần thiết vào tệp nguồn Java của bạn:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Hướng dẫn từng bước

### Bước 1: Thiết lập tài liệu

Tạo một tài liệu OneNote mới và một container trang nơi nội dung sẽ được đặt.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Bước 2: Khởi tạo Outline

*Outline* hoạt động như một container cho các yếu tố như văn bản và hình ảnh. Chúng ta đặt các offset của nó về 0 để nội dung bắt đầu từ góc trên‑trái.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Bước 3: Tải và căn chỉnh hình ảnh

Tải hình ảnh bạn muốn nhúng và căn chỉnh nó sang phía bên phải của trang. Đây là nơi chúng ta thực sự **thêm hình ảnh vào OneNote**. Hàm khởi tạo `Image` minh họa cách **tải tệp hình ảnh java** bằng mã.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Bước 4: Gắn hình ảnh vào một Outline Element

Đặt hình ảnh bên trong một `OutlineElement`. Bước này liên kết đối tượng hình ảnh với cấu trúc outline của tài liệu và thực tế **chèn hình ảnh vào OneNote**.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Bước 5: Lắp ráp cấu trúc tài liệu

Thêm phần tử outline vào outline, sau đó gắn outline vào trang, và cuối cùng thêm trang vào tài liệu.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Bước 6: Lưu tài liệu OneNote

Lưu tài liệu vào đĩa. Trong ví dụ này chúng tôi xuất ra PDF, điều này minh họa cách **lưu OneNote dưới dạng PDF** hoặc **chuyển đổi OneNote sang PDF**. Bạn cũng có thể lưu dưới dạng tệp OneNote gốc (`.one`) bằng cách thay đổi `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Các vấn đề thường gặp và giải pháp

| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **Image not appearing** | Đường dẫn tệp sai hoặc định dạng không được hỗ trợ. | Xác minh `dataDir` trỏ tới thư mục đúng và sử dụng định dạng hình ảnh được hỗ trợ (JPEG, PNG, v.v.). |
| **Document saved as empty PDF** | Các offset của outline được đặt không đúng. | Đảm bảo gọi `setVerticalOffset(0)` và `setHorizontalOffset(0)`, hoặc điều chỉnh offset để đặt nội dung trong giới hạn trang. |
| **IOException on save** | Thư mục đích không tồn tại hoặc thiếu quyền ghi. | Tạo thư mục trước hoặc chạy chương trình với quyền phù hợp. |

## Câu hỏi thường gặp

**Q1: Tôi có thể tìm tài liệu cho Aspose.Note cho Java ở đâu?**  
A1: Bạn có thể truy cập tài liệu [tại đây](https://reference.aspose.com/note/java/).

**Q2: Làm sao tôi tải Aspose.Note cho Java?**  
A2: Bạn có thể tải Aspose.Note cho Java từ [trang tải xuống](https://releases.aspose.com/note/java/).

**Q3: Có bản dùng thử miễn phí cho Aspose.Note cho Java không?**  
A3: Có, bạn có thể nhận bản dùng thử miễn phí từ [website](https://releases.aspose.com/).

**Q4: Tôi có thể nhận hỗ trợ cho Aspose.Note cho Java ở đâu?**  
A4: Để được hỗ trợ, hãy truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28).

**Q5: Tôi có thể nhận giấy phép tạm thời cho Aspose.Note cho Java không?**  
A5: Có, bạn có thể yêu cầu giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

**Q6: Tôi có thể sử dụng mã này để **lưu OneNote dưới dạng PDF** trên máy chủ Linux không?**  
A6: Chắc chắn. Thư viện Aspose.Note không phụ thuộc vào nền tảng, vì vậy cùng một mã hoạt động trên Windows, Linux và macOS.

**Q7: API có hỗ trợ **nhúng hình ảnh vào OneNote** với PNG trong suốt không?**  
A7: Có, các tệp PNG có kênh alpha được hỗ trợ đầy đủ và giữ độ trong suốt khi chèn.

---

**Cập nhật lần cuối:** 2026-03-19  
**Kiểm tra với:** Aspose.Note for Java 24.12 (latest)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}