---
date: 2025-12-28
description: Tìm hiểu cách xuất OneNote sang PDF với kiểm soát đầy đủ bằng Aspose.Note
  cho Java. Bao gồm các tùy chọn xuất sổ tay OneNote sang PDF và hướng dẫn chuyển
  đổi sổ tay sang PDF bằng Java.
linktitle: How to Export OneNote to PDF with Options – Convert Notebook to PDF using
  Aspose.Note
second_title: Aspose.Note Java API
title: Cách xuất OneNote sang PDF với các tùy chọn – Chuyển đổi sổ ghi chú sang PDF
  bằng Aspose.Note
url: /vi/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách xuất OneNote sang PDF với các tùy chọn – Aspose.Note Java API

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học **cách xuất OneNote sang PDF** với các tùy chọn có thể tùy chỉnh bằng Aspose.Note cho Java. Chuyển đổi một sổ tay OneNote sang PDF là một nhu cầu thường gặp—cho dù bạn cần chia sẻ ghi chú cuộc họp, lưu trữ tài liệu, hay tạo báo cáo có thể in được. Với Aspose.Note, quy trình trở nên đơn giản, hoàn toàn có thể lập trình và cho phép bạn kiểm soát chi tiết kết quả PDF.

## Câu trả lời nhanh
- **API làm gì?** Nó tải một sổ tay OneNote và lưu nó dưới dạng PDF với các cài đặt tùy chọn.  
- **Ngôn ngữ nào được sử dụng?** Java – hoàn hảo cho các ứng dụng phía máy chủ hoặc máy tính để bàn.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí hoạt động cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Tôi có thể kiểm soát bố cục trang không?** Có, bạn có thể đặt thuật toán chia trang, tiêu đề, chân trang và hơn thế nữa.  
- **Mã mẫu có thể chạy được không?** Chắc chắn – chỉ cần thay thế đường dẫn placeholder bằng vị trí sổ tay của bạn.

## “Cách xuất OneNote sang PDF” là gì?

Xuất OneNote sang PDF có nghĩa là chuyển đổi sổ tay OneNote gốc (`*.onetoc2` và các tệp phần liên quan) thành một tài liệu PDF cố định, có thể di động. Quá trình chuyển đổi này giữ định dạng, hình ảnh và các đối tượng nhúng đồng thời cho phép nội dung được xem trên bất kỳ thiết bị nào mà không cần OneNote.

## Tại sao nên sử dụng Aspose.Note cho Java?

- **Không phụ thuộc vào Microsoft Office** – hoạt động trên bất kỳ nền tảng nào chạy Java.  
- **Các tùy chọn PDF phong phú** – kiểm soát việc chia trang, tiêu đề/chân trang và xử lý đối tượng.  
- **Độ trung thực cao** – đầu ra PDF gần giống với giao diện gốc của OneNote.  
- **Mở rộng được** – phù hợp cho việc xử lý hàng loạt hàng nghìn sổ tay.

## Yêu cầu trước

1. **Bộ công cụ phát triển Java (JDK)** – phiên bản 8 trở lên.  
2. **Aspose.Note cho Java** – tải xuống từ [download link](https://releases.aspose.com/note/java/).  
3. **Một IDE** – IntelliJ IDEA, Eclipse hoặc NetBeans (tùy chọn của bạn).  
4. **Một sổ tay OneNote** mà bạn muốn chuyển đổi (ví dụ, `Notizbuch öffnen.onetoc2`).

## Nhập các gói

Đầu tiên, nhập các lớp cung cấp chức năng xử lý sổ tay và lưu PDF.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Bước 1: Tải sổ tay OneNote

Tải tệp sổ tay từ đĩa. Thay thế `Your Document Directory` bằng thư mục thực tế chứa tệp `.onetoc2` của bạn.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Bước 2: Chỉ định tùy chọn lưu PDF

Ở đây bạn định nghĩa cách PDF sẽ được tạo ra. Ví dụ đặt thuật toán chia trang giữ các đối tượng rắn (solid objects) cùng nhau, hữu ích khi bạn có sơ đồ hoặc bảng cần ở cùng một trang.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Bước 3: Lưu sổ tay dưới dạng PDF

Cuối cùng, ghi sổ tay ra tệp PDF. Đường dẫn đầu ra có thể là bất kỳ vị trí nào bạn muốn.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **File không tìm thấy** | Sai `dataDir` hoặc tên tệp. | Kiểm tra lại đường dẫn và đảm bảo tệp sổ tay tồn tại. |
| **Thiếu phông chữ** | Kết xuất PDF cần các phông chữ giống như trong OneNote. | Cài đặt các phông chữ cần thiết trên máy chủ hoặc nhúng chúng qua các tùy chọn Aspose bổ sung. |
| **Sổ tay lớn gây OutOfMemoryError** | Toàn bộ sổ tay được tải vào bộ nhớ. | Xử lý từng phần riêng biệt hoặc tăng kích thước heap JVM (`-Xmx`). |

## Kết luận

Chúng tôi đã hướng dẫn **cách xuất OneNote sang PDF** bằng Aspose.Note cho Java, bao gồm tải sổ tay, cấu hình các tùy chọn PDF và lưu kết quả. Khi thực hiện theo các bước này, bạn có thể tích hợp việc chuyển đổi sổ tay sang PDF vào bất kỳ ứng dụng Java nào, dù là công cụ desktop, dịch vụ web hay backend xử lý hàng loạt.

## Câu hỏi thường gặp

### Q1: Tôi có thể tùy chỉnh giao diện đầu ra PDF không?

A1: Có, Aspose.Note cung cấp nhiều tùy chọn để tùy chỉnh đầu ra PDF, bao gồm cài đặt tiêu đề/chân trang, thuật toán chia trang và hơn thế nữa.

### Q2: Aspose.Note có tương thích với mọi phiên bản OneNote không?

A2: Aspose.Note hỗ trợ Microsoft OneNote 2010 và các phiên bản sau này.

### Q3: Aspose.Note có cung cấp bản dùng thử miễn phí không?

A3: Có, bạn có thể tải bản dùng thử miễn phí của Aspose.Note từ [here](https://releases.aspose.com/).

### Q4: Tôi có thể tìm tài liệu cho Aspose.Note ở đâu?

A4: Bạn có thể tìm tài liệu đầy đủ cho Aspose.Note [here](https://reference.aspose.com/note/java/).

### Q5: Làm thế nào để tôi nhận được hỗ trợ cho Aspose.Note?

A5: Đối với bất kỳ hỗ trợ kỹ thuật hoặc câu hỏi nào, bạn có thể truy cập diễn đàn hỗ trợ Aspose.Note [here](https://forum.aspose.com/c/note/28).

## Các câu hỏi thường gặp bổ sung

**Q: Làm sao để xuất sổ tay OneNote sang PDF mà không mất hình ảnh?**  
A: Đảm bảo `KeepSolidObjectsAlgorithm` được đặt (như trong ví dụ) và các tệp hình ảnh của sổ tay nguồn có thể truy cập được trong cùng thư mục.

**Q: Tôi có thể chuyển đổi hàng loạt nhiều sổ tay trong một lần chạy không?**  
A: Có. Lặp qua danh sách các đường dẫn sổ tay, khởi tạo một `Notebook` cho mỗi cái, áp dụng cùng một `NotebookPdfSaveOptions`, và gọi `save()`.

**Q: Có cách nào để đặt siêu dữ liệu PDF (tác giả, tiêu đề) trong quá trình chuyển đổi không?**  
A: Sử dụng `PdfSaveOptions.setMetadata()` để xác định tác giả, tiêu đề, chủ đề và từ khóa trước khi lưu.

**Q: API có hỗ trợ PDF được bảo vệ bằng mật khẩu không?**  
A: Bạn có thể đặt mật khẩu cho `PdfSaveOptions` qua `setEncryptionPassword()` sau khi cấu hình các tùy chọn khác.

**Q: Phiên bản Aspose.Note nào đã được sử dụng cho hướng dẫn này?**  
A: Mã đã được kiểm tra với Aspose.Note cho Java 23.12.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.Note cho Java 23.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}