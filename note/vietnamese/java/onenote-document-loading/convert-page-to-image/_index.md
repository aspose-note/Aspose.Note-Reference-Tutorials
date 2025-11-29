---
date: 2025-11-29
description: Tìm hiểu cách xuất các trang OneNote thành hình ảnh bằng Java và khám
  phá cách chuyển đổi hình ảnh trang OneNote với Aspose.Note. Hãy làm theo hướng dẫn
  từng bước của chúng tôi để tích hợp nhanh chóng.
language: vi
linktitle: How to Export OneNote Page to Image Using Java
second_title: Aspose.Note Java API
title: Cách xuất trang OneNote sang hình ảnh bằng Java
url: /java/onenote-document-loading/convert-page-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách xuất trang OneNote thành hình ảnh bằng Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học **cách xuất trang OneNote** ra các tệp hình ảnh bằng Java với Aspose.Note. Việc chuyển đổi một trang OneNote thành hình ảnh rất hữu ích khi bạn cần nhúng nội dung sổ ghi chú vào báo cáo, chia sẻ ảnh chụp nhanh với người dùng không dùng OneNote, hoặc tạo ảnh thu nhỏ cho hệ thống quản lý tài liệu. Chúng tôi sẽ hướng dẫn từng bước, giải thích lý do mỗi dòng mã quan trọng, và chỉ cho bạn cách tùy chỉnh kết quả.

## Câu trả lời nhanh
- **Thư viện cần thiết là gì?** Aspose.Note for Java  
- **Tôi có thể chọn định dạng ảnh không?** Có – JPEG, PNG, BMP, v.v. thông qua `ImageSaveOptions`  
- **Có cần giấy phép cho môi trường sản xuất không?** Cần giấy phép Aspose.Note hợp lệ cho việc sử dụng thương mại.  
- **Trang nào tôi có thể xuất?** Bất kỳ trang nào bằng cách đặt `PageIndex` (đánh số từ 0).  
- **Quá trình chuyển đổi mất bao lâu?** Thông thường dưới một giây cho một trang tiêu chuẩn.

## Xuất trang OneNote thành hình ảnh là gì?
Xuất trang OneNote có nghĩa là render nội dung phong phú của trang—văn bản, bản vẽ, bảng—vào một tệp hình ảnh tĩnh (ví dụ: JPEG). Quá trình này tạo ra một biểu diễn trực quan di động có thể hiển thị ở bất kỳ đâu, ngay cả khi không cài đặt client OneNote.

## Tại sao nên sử dụng Aspose.Note để chuyển đổi trang OneNote?
- **Độ trung thực cao** – giữ nguyên bố cục, phông chữ và nét bút.  
- **Không phụ thuộc vào Microsoft Office** – hoạt động trên bất kỳ nền tảng nào hỗ trợ Java.  
- **Kiểm soát chi tiết** – chọn định dạng ảnh, chất lượng và chỉ mục trang cụ thể.  
- **Mở rộng** – phù hợp cho việc xử lý hàng loạt nhiều trang.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã chuẩn bị các yêu cầu sau:

1. **Java Development Kit (JDK)** – Cài đặt JDK 11 hoặc mới hơn. Bạn có thể tải về từ [trang chính thức của Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) nếu chưa có.  
2. **Aspose.Note for Java** – Lấy thư viện mới nhất từ [trang tải xuống Aspose.Note](https://releases.aspose.com/note/java/). Thêm file JAR vào classpath của dự án.

## Nhập các gói

Đầu tiên, hãy nhập các gói cần thiết để chúng ta có thể làm việc với tài liệu và tùy chọn lưu ảnh.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Bước 1: Tải tài liệu OneNote

Chúng ta bắt đầu bằng việc tải file `.one` vào đối tượng `Document` của `Aspose.Note`.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Mẹo chuyên nghiệp:** Sử dụng đường dẫn tuyệt đối hoặc luồng tài nguyên nếu tệp của bạn nằm trong một JAR.

## Bước 2: Khởi tạo tùy chọn lưu ảnh

Tạo một thể hiện `ImageSaveOptions` để xác định định dạng đầu ra (JPEG trong ví dụ này). Bạn có thể chuyển sang PNG, BMP hoặc GIF bằng cách thay đổi `SaveFormat`.

```java
// Initialize ImageSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
```

## Bước 3: Chỉ định chỉ mục trang

Các trang được đánh số từ 0, vì vậy `1` sẽ chọn **trang thứ hai**. Điều chỉnh giá trị này để xuất bất kỳ trang nào bạn cần.

```java
// Specify second page for conversion
options.setPageIndex(1);
```

## Bước 4: Lưu tài liệu dưới dạng hình ảnh

Bây giờ chúng ta gọi `save` trên đối tượng `Document`, truyền tên tệp đích và các tùy chọn đã cấu hình.

```java
// Save the document
oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);
```

## Bước 5: In xác nhận

Một thông báo console đơn giản sẽ xác nhận rằng ảnh đã được tạo thành công.

```java
// Print confirmation message
System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
```

## Cách chuyển đổi trang OneNote thành hình ảnh (kịch bản thay thế)

Nếu bạn cần **chuyển đổi hàng loạt các tệp ảnh trang OneNote**, chỉ cần đặt đoạn mã trên vào một vòng lặp lặp qua `Document.getPages()`. Thay đổi `options.setPageIndex(i)` cho mỗi lần lặp, và tùy chọn điều chỉnh `options.setQuality(90)` để kiểm soát mức nén JPEG.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| **Ảnh trống** | Chỉ mục trang ngoài phạm vi hoặc tài liệu không được tải đúng. | Kiểm tra `options.setPageIndex` nằm trong `0 .. document.getPages().size() - 1`. |
| **Định dạng không hỗ trợ** | Sử dụng phiên bản Aspose.Note cũ không có một số định dạng. | Cập nhật lên phiên bản mới nhất của Aspose.Note for Java. |
| **OutOfMemoryError** | Chuyển đổi các trang rất lớn trên JVM bộ nhớ thấp. | Tăng kích thước heap (`-Xmx2g`) hoặc xử lý từng trang một. |

## Câu hỏi thường gặp

**Q1: Tôi có thể chuyển đổi nhiều trang thành ảnh bằng phương pháp này không?**  
A: Có. Đặt logic lưu trong một vòng lặp và thay đổi `options.setPageIndex(i)` cho mỗi trang bạn muốn xuất.

**Q2: Aspose.Note có tương thích với các phiên bản tệp OneNote khác nhau không?**  
A: Hoàn toàn. Aspose.Note hỗ trợ các tệp .one từ OneNote 2007, 2010, 2013 và các phiên bản sau.

**Q3: Tôi có thể tùy chỉnh định dạng và chất lượng ảnh trong quá trình chuyển đổi không?**  
A: Có. Chọn `SaveFormat.Png`, `SaveFormat.Bmp`, v.v., và đặt `options.setQuality(int)` cho chất lượng JPEG (0‑100).

**Q4: Aspose.Note có hỗ trợ các ngôn ngữ lập trình khác không?**  
A: Có. Thư viện cũng có sẵn cho .NET, Python, C++, và nhiều ngôn ngữ khác.

**Q5: Tôi có thể tìm thêm hỗ trợ hoặc trợ giúp ở đâu?**  
A: Truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) hoặc tham khảo tài liệu chính thức [tại đây](https://reference.aspose.com/note/java/).

---

**Cập nhật lần cuối:** 2025-11-29  
**Đã kiểm tra với:** Aspose.Note for Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}