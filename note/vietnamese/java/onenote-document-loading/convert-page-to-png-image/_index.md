---
date: 2025-11-29
description: Tìm hiểu cách xuất trang OneNote sang PNG bằng Aspose.Note cho Java.
  Thực hiện các hướng dẫn từng bước để đặt chỉ mục trang, chuyển đổi trang và lưu
  hình ảnh.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Xuất trang OneNote thành hình ảnh PNG trong Java bằng Aspose.Note
url: /vi/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất trang OneNote thành ảnh PNG trong Java bằng Aspose.Note

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách xuất trang OneNote** thành ảnh PNG bằng thư viện Aspose.Note cho Java. Chúng ta sẽ đi qua mọi thứ bạn cần—từ việc chuẩn bị môi trường, thiết lập chỉ mục trang, cho đến khi lưu trang dưới dạng tệp PNG chất lượng cao. Khi hoàn thành, bạn sẽ có thể thêm khả năng này vào bất kỳ ứng dụng Java nào làm việc với tài liệu OneNote.

## Câu trả lời nhanh
- **Thư viện cần thiết là gì?** Aspose.Note cho Java.  
- **Có thể xuất một trang duy nhất không?** Có — sử dụng `setPageIndex` để chỉ định trang cụ thể.  
- **Các định dạng ảnh được hỗ trợ?** PNG, JPEG, GIF, BMP, TIFF (ở đây minh họa PNG).  
- **Cần giấy phép không?** Có bản dùng thử miễn phí; giấy phép bắt buộc cho môi trường sản xuất.  
- **Thời gian triển khai khoảng bao lâu?** Thông thường dưới 10 phút cho một chuyển đổi cơ bản.

## “Xuất trang OneNote” là gì?
Xuất một trang OneNote có nghĩa là chuyển đổi một trang cụ thể trong tài liệu `.one` thành một tệp ảnh độc lập (PNG trong trường hợp này). Điều này hữu ích khi bạn cần chia sẻ, nhúng hoặc xử lý nội dung OneNote bên ngoài môi trường OneNote.

## Tại sao nên dùng Aspose.Note cho Java để chuyển đổi OneNote sang PNG?
- **Không phụ thuộc vào Microsoft Office** – hoạt động trên bất kỳ nền tảng nào chạy Java.  
- **Kiểm soát chi tiết** – bạn có thể chọn bất kỳ trang nào bằng `setPageIndex`.  
- **Đầu ra chất lượng cao** – PNG giữ nguyên đồ họa vector và độ rõ nét của văn bản.  
- **Sẵn sàng cho batch** – dễ dàng lặp qua các trang để chuyển đổi hàng loạt.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

1. **Java Development Kit (JDK)** – phiên bản 8 trở lên.  
2. **Aspose.Note cho Java** – tải JAR mới nhất từ [trang web Aspose](https://releases.aspose.com/note/java/).  
3. **Tài liệu OneNote** (`.one`) chứa trang bạn muốn xuất.

## Nhập gói

Đầu tiên, nhập các lớp Java cần thiết:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Hướng dẫn từng bước

### Bước 1: Tải tài liệu OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Chúng ta dùng lớp `Document` để đọc tệp OneNote từ đĩa. Đối tượng `LoadOptions` cho phép bạn tùy chỉnh hành vi tải nếu cần.

### Bước 2: Khởi tạo ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` thông báo cho Aspose.Note rằng chúng ta muốn đầu ra ở định dạng **PNG**. Bạn có thể chuyển sang JPEG, BMP, v.v. bằng cách thay đổi `SaveFormat`.

### Bước 3: Đặt chỉ mục trang (Cách chuyển đổi trang OneNote)

```java
// set page index
opts.setPageIndex(0);
```

Phương thức `setPageIndex` chọn trang sẽ được xuất. Đánh số trang bắt đầu từ **0**, vì vậy `0` là trang đầu tiên. Điều chỉnh giá trị này để xuất một trang khác.

### Bước 4: Lưu tài liệu dưới dạng PNG (Lưu OneNote dưới dạng PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Gọi `save` sẽ ghi trang đã chọn vào tệp PNG trên đĩa. Tên tệp `ConvertSpecificPageToPngImage_out.png` chỉ là ví dụ — bạn có thể đặt tên tùy ý.

## Các vấn đề thường gặp & Mẹo

- **Chỉ mục trang không đúng** – Nhớ rằng đánh số bắt đầu từ 0. Nếu nhận được ảnh trống, hãy kiểm tra giá trị chỉ mục.  
- **Thiếu JAR Aspose.Note** – Đảm bảo JAR đã được thêm vào classpath; nếu không sẽ gặp `ClassNotFoundException`.  
- **Trang quá lớn** – Đối với các trang rất lớn, hãy tăng kích thước heap JVM (`-Xmx`) để tránh `OutOfMemoryError`.

## Câu hỏi thường gặp

### Q1: Tôi có thể chuyển đổi nhiều trang thành ảnh PNG cùng lúc bằng Aspose.Note cho Java không?
A1: Có, bạn có thể lặp qua các trang của tài liệu, cập nhật `opts.setPageIndex(i)`, và gọi `save` cho mỗi vòng lặp.

### Q2: Aspose.Note cho Java có hỗ trợ các định dạng ảnh khác ngoài PNG không?
A2: Chắc chắn. Bạn có thể đặt `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp`, hoặc `SaveFormat.Tiff` trong `ImageSaveOptions`.

### Q3: Có bản dùng thử miễn phí cho Aspose.Note cho Java không?
A3: Có, bạn có thể tải bản dùng thử miễn phí từ [trang web](https://releases.aspose.com/).

### Q4: Tôi có thể nhận hỗ trợ kỹ thuật nếu gặp vấn đề với Aspose.Note cho Java không?
A4: Chắc chắn, bạn có thể tìm kiếm hỗ trợ tại diễn đàn cộng đồng Aspose [tại đây](https://forum.aspose.com/c/note/28).

### Q5: Tôi có thể mua giấy phép cho Aspose.Note cho Java ở đâu?
A5: Bạn có thể mua giấy phép từ [trang mua hàng](https://purchase.aspose.com/buy).

### Q6: Làm sao để xuất một trang chứa ảnh nhúng?
A6: Các ảnh nhúng sẽ được render tự động trong đầu ra PNG; không cần mã bổ sung.

### Q7: Tôi có thể đặt DPI hoặc độ phân giải ảnh không?
A7: Có, sử dụng `opts.setResolution(int dpi)` trước khi gọi `save` để điều chỉnh chất lượng đầu ra.

---

**Cập nhật lần cuối:** 2025-11-29  
**Kiểm tra với:** Aspose.Note cho Java 24.11 (mới nhất)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}