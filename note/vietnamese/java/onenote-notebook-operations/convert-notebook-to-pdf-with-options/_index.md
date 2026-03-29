---
date: 2026-03-29
description: Chuyển đổi sổ tay OneNote sang PDF với các tùy chọn, lưu sổ tay dưới
  dạng PDF và thêm tiêu đề, chân trang PDF bằng Aspose.Note cho Java.
linktitle: Convert Notebook to PDF with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Chuyển đổi OneNote sang PDF với các tùy chọn - Aspose.Note
url: /vi/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi OneNote sang PDF với Các Tùy chọn bằng Aspose.Note

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học cách **convert onenote to pdf** với quyền kiểm soát đầy đủ đối với kết quả. Aspose.Note cho Java giúp việc xuất sổ tay OneNote sang PDF trở nên dễ dàng, cho phép bạn **save notebook as pdf** đồng thời tùy chỉnh tiêu đề, chân trang và hành vi chia trang. Dù bạn cần tạo báo cáo, lưu trữ ghi chú cuộc họp, hay chia sẻ nội dung với người dùng không có OneNote, hướng dẫn này sẽ dẫn bạn qua từng bước.

## Câu trả lời nhanh
- **Thư viện nào xử lý việc chuyển đổi?** Aspose.Note cho Java.
- **Tôi có thể thêm tiêu đề hoặc chân trang vào PDF không?** Có – sử dụng tùy chọn lưu PDF để chèn tiêu đề/chân trang tùy chỉnh.
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Cần giấy phép thương mại cho việc sử dụng không phải thử nghiệm.
- **Các phiên bản Java nào được hỗ trợ?** Java 8 và các phiên bản sau.
- **Quá trình chuyển đổi mất bao lâu?** Thông thường vài giây cho sổ tay kích thước trung bình.

## Chuyển đổi OneNote sang PDF có nghĩa là gì?

Chuyển đổi OneNote sang PDF có nghĩa là lấy một sổ tay OneNote (tệp *.onetoc2*) và hiển thị mỗi trang dưới dạng một trang PDF. PDF kết quả giữ nguyên văn bản, hình ảnh và bố cục, cho phép xem trên bất kỳ thiết bị nào mà không cần OneNote.

## Tại sao nên sử dụng Aspose.Note để xuất sổ tay onenote sang pdf?

- **Không cần cài đặt Office** – API hoạt động độc lập.
- **Kiểm soát chi tiết** – bạn có thể thiết lập thuật toán chia trang, nhúng phông chữ và thêm tiêu đề/chân trang.
- **Độ trung thực cao** – giao diện hình ảnh của sổ tay gốc được giữ nguyên.
- **Đa nền tảng** – hoạt động trên Windows, Linux và macOS với bất kỳ môi trường Java nào.

## Yêu cầu trước

Trước khi bắt đầu, hãy đảm bảo bạn đã chuẩn bị các yêu cầu sau:

1. Java Development Kit (JDK) – JDK 8 hoặc mới hơn đã được cài đặt.
2. Aspose.Note cho Java – tải xuống và cài đặt từ [download link](https://releases.aspose.com/note/java/).
3. IDE (Môi trường Phát triển Tích hợp) – IntelliJ IDEA, Eclipse hoặc NetBeans là các lựa chọn phổ biến.

## Nhập các Gói

Đầu tiên, bạn cần nhập các gói cần thiết vào dự án Java của mình. Các gói này cung cấp các lớp và phương thức cần thiết để làm việc với tài liệu OneNote.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Bước 1: Tải Sổ tay OneNote

Để **convert onenote to pdf**, bạn cần tải sổ tay OneNote trước. Đảm bảo rằng đường dẫn tới tệp sổ tay được chỉ định chính xác.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Bước 2: Chỉ định Các Tùy chọn Lưu PDF

Aspose.Note cung cấp nhiều tùy chọn để tùy chỉnh đầu ra PDF. Bạn có thể chỉ định các tùy chọn như thuật toán chia trang, cài đặt tiêu đề/chân trang, và hơn thế nữa.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Bước 3: Lưu Sổ tay dưới dạng PDF

Sau khi bạn đã tải sổ tay và chỉ định các tùy chọn lưu, đã đến lúc **save the notebook as pdf**.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|----------|
| PDF thiếu hình ảnh | Hình ảnh được lưu dưới dạng đối tượng nhúng nhưng không được tải | Đảm bảo tệp sổ tay và tất cả các tài nguyên liên kết nằm trong cùng một thư mục trước khi tải. |
| Tiêu đề/chân trang không hiển thị | Các tùy chọn tiêu đề/chân trang chưa được đặt trong `PdfSaveOptions` | Sử dụng `documentSaveOptions.setHeaderFooter()` để định nghĩa nội dung trước khi lưu. |
| Lỗi bộ nhớ khi xử lý sổ tay lớn | Toàn bộ sổ tay được tải vào bộ nhớ | Xử lý sổ tay theo từng phần hoặc tăng kích thước heap JVM (`-Xmx2g`). |

## Câu hỏi thường gặp

### Q1: Tôi có thể tùy chỉnh giao diện đầu ra PDF không?

A1: Có, Aspose.Note cung cấp nhiều tùy chọn để tùy chỉnh đầu ra PDF, bao gồm cài đặt tiêu đề/chân trang, thuật toán chia trang, và hơn thế nữa.

### Q2: Aspose.Note có tương thích với mọi phiên bản OneNote không?

A2: Aspose.Note hỗ trợ Microsoft OneNote 2010 và các phiên bản sau.

### Q3: Aspose.Note có cung cấp bản dùng thử miễn phí không?

A3: Có, bạn có thể tải bản dùng thử miễn phí của Aspose.Note từ [here](https://releases.aspose.com/).

### Q4: Tôi có thể tìm tài liệu cho Aspose.Note ở đâu?

A4: Bạn có thể tìm tài liệu đầy đủ cho Aspose.Note [here](https://reference.aspose.com/note/java/).

### Q5: Làm thế nào để tôi nhận được hỗ trợ cho Aspose.Note?

A5: Đối với bất kỳ hỗ trợ kỹ thuật hoặc câu hỏi nào, bạn có thể truy cập diễn đàn hỗ trợ Aspose.Note [here](https://forum.aspose.com/c/note/28).

## Các Câu hỏi Thường gặp Bổ sung

**Q: Làm thế nào để thêm tiêu đề hoặc chân trang PDF tùy chỉnh?**  
A: Tạo một đối tượng `PdfHeaderFooterOptions`, cấu hình văn bản hoặc hình ảnh, và gán nó cho `documentSaveOptions.setHeaderFooterOptions()` trước khi gọi `save`.

**Q: Tôi có thể xuất chỉ các phần đã chọn của sổ tay không?**  
A: Có – tải sổ tay, lấy các đối tượng `Section` mong muốn, và gọi `section.save()` với cùng các tùy chọn PDF.

**Q: Có thể mã hóa PDF đã tạo không?**  
A: Chắc chắn. Sử dụng `documentSaveOptions.setEncryptionPassword("yourPassword")` để bảo vệ PDF.

**Q: Những lưu ý về hiệu năng nào cần cân nhắc?**  
A: Đối với sổ tay rất lớn, hãy cân nhắc truyền dữ liệu đầu ra tới một `FileOutputStream` và tăng kích thước heap JVM nếu gặp `OutOfMemoryError`.

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}