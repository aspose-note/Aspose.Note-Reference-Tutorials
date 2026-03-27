---
date: 2026-01-23
description: Tìm hiểu cách thêm bảng vào OneNote một cách lập trình bằng Aspose.Note
  cho Java. Hướng dẫn từng bước để tạo tài liệu hiệu quả.
linktitle: How to add table to OneNote with Aspose.Note for Java
second_title: Aspose.Note Java API
title: Cách thêm bảng vào OneNote bằng Aspose.Note cho Java
url: /vi/java/onenote-table-manipulation/compose-table/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách thêm bảng vào OneNote bằng Aspose.Note cho Java

## Giới thiệu
Trong hướng dẫn này, bạn sẽ học cách **thêm bảng vào OneNote** bằng Aspose.Note cho Java, cho phép bạn tạo tài liệu phong phú, có cấu trúc một cách lập trình, nâng cao khả năng cộng tác và báo cáo. Aspose.Note cung cấp một API mạnh mẽ để xây dựng các trang, đề mục và bảng trong OneNote mà không cần chỉnh sửa thủ công.

## Câu trả lời nhanh
- **Hướng dẫn này đề cập đến gì?** Thêm một bảng vào OneNote bằng Aspose.Note cho Java.  
- **Cần bao lâu?** Khoảng 10‑15 phút cho một triển khai cơ bản.  
- **Có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc đánh giá; cần giấy phép thương mại cho môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Java 8 trở lên.  
- **Có thể tùy chỉnh kiểu bảng không?** Có – bạn có thể thay đổi phông chữ, màu sắc và viền ô qua API.

## Yêu cầu trước
Trước khi bắt đầu, hãy đảm bảo bạn đã có các yêu cầu sau:
- Kiến thức cơ bản về lập trình Java.  
- Thư viện Aspose.Note cho Java đã được cài đặt. Bạn có thể tải xuống từ [đây](https://releases.aspose.com/note/java/).  
- Một môi trường phát triển tích hợp (IDE) đã được thiết lập cho phát triển Java.

## Nhập gói
Đảm bảo nhập các gói cần thiết để khởi động dự án của bạn. Thêm các câu lệnh import sau vào lớp Java của bạn:

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```

## Bước 1: Đặt thư mục tài liệu
```java
String dataDir = "Your Document Directory";
```
Thay thế `"Your Document Directory"` bằng đường dẫn thực tế nơi bạn muốn lưu tài liệu OneNote.

## Bước 2: Soạn tiêu đề
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
Tạo một tiêu đề bắt mắt cho tài liệu. Điều chỉnh kích thước phông chữ, độ đậm và căn chỉnh theo nhu cầu.

## Bước 3: Tạo trang và đề mục
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
Thiết lập một trang và đề mục mới, sau đó thêm tiêu đề đã tạo vào đề mục.

## Bước 4: Thêm văn bản tóm tắt
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
Bao gồm một đoạn văn tóm tắt ngắn để cung cấp ngữ cảnh cho bảng.

## Bước 5: Thêm bảng vào OneNote
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// Remaining steps are involved in setting up the table structure, header row, and adding empty rows.
// Refer to the provided code for detailed implementation.
```
Soạn cấu trúc bảng và điền dữ liệu liên quan. Mã mẫu bao gồm việc thêm các cột, hàng tiêu đề, các hàng trống và nội dung mẫu cho cột “Contacts”.

## Bước 6: Lưu tài liệu
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
Lưu tài liệu đã soạn với tên tệp và đường dẫn thư mục chỉ định.

## Kết luận
Chúc mừng! Bạn đã **thêm thành công một bảng vào OneNote** bằng Aspose.Note cho Java. Hướng dẫn này đã trình bày quy trình từng bước, giúp bạn nâng cao khả năng tạo tài liệu một cách lập trình.

## Câu hỏi thường gặp
### Hỏi: Tôi có thể tìm tài liệu Aspose.Note cho Java ở đâu?
Bạn có thể tham khảo tài liệu [tại đây](https://reference.aspose.com/note/java/).

### Hỏi: Làm sao để tải Aspose.Note cho Java?
Bạn có thể tải xuống từ [liên kết này](https://releases.aspose.com/note/java/).

### Hỏi: Có bản dùng thử miễn phí không?
Có, bạn có thể truy cập bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Hỏi: Tôi có thể nhận hỗ trợ cho Aspose.Note cho Java ở đâu?
Truy cập diễn đàn hỗ trợ [tại đây](https://forum.aspose.com/c/note/28).

### Hỏi: Tôi có thể lấy giấy phép tạm thời không?
Có, bạn có thể nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

---

**Cập nhật lần cuối:** 2026-01-23  
**Kiểm tra với:** Aspose.Note cho Java (phiên bản mới nhất)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}