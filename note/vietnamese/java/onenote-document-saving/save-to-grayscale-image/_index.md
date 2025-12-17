---
date: 2025-12-17
description: Tìm hiểu cách xuất OneNote bằng cách lưu tài liệu dưới dạng hình ảnh
  PNG xám bằng Aspose.Note cho Java. Bao gồm các bước tải tài liệu OneNote và tạo
  hình ảnh xám.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Cách xuất OneNote dưới dạng ảnh xám – Aspose.Note
url: /vi/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu ảnh Grayscale trong OneNote - Aspose.Note

## Giới thiệu

Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn **cách xuất onenote** bằng cách lưu tài liệu dưới dạng ảnh grayscale sử dụng Aspose.Note cho Java. Ảnh grayscale là hình ảnh đơn sắc chỉ chứa các mức độ xám, có thể hữu ích cho việc in ấn, lưu trữ, hoặc giảm kích thước tệp. Chúng tôi sẽ hướng dẫn tải tài liệu OneNote, cấu hình các tùy chọn lưu để **tạo ảnh grayscale**, và cuối cùng **lưu tài liệu dưới dạng PNG**.

## Câu trả lời nhanh
- **“cách xuất onenote” có nghĩa là gì?** Nó đề cập đến việc chuyển đổi một tệp OneNote sang định dạng khác, chẳng hạn như ảnh, một cách lập trình.  
- **Định dạng nào là tốt nhất cho đầu ra grayscale?** PNG hoạt động tốt vì nó giữ chất lượng loss‑less và hỗ trợ chế độ màu grayscale.  
- **Tôi có cần giấy phép không?** Một giấy phép Aspose.Note hợp lệ là bắt buộc cho môi trường sản xuất; giấy phép dùng thử tạm thời có sẵn để thử nghiệm.  
- **Yêu cầu phiên bản Java nào?** Java 8 trở lên được khuyến nghị.  
- **Tôi có thể thay đổi kích thước ảnh không?** Có, bạn có thể điều chỉnh các thuộc tính của `ImageSaveOptions` như `Resolution` hoặc `PageSize` trước khi lưu.

## “cách xuất onenote” là gì?
Xuất OneNote có nghĩa là chuyển đổi một tệp OneNote `.one` sang dạng biểu diễn khác—như PDF, HTML, hoặc ảnh—bằng cách lập trình. Trong hướng dẫn này, chúng tôi tập trung vào việc xuất ra ảnh **grayscale PNG**, một yêu cầu phổ biến cho tài liệu hoặc quy trình in ấn.

## Tại sao nên xuất OneNote dưới dạng ảnh grayscale?
- **Giảm kích thước tệp** – PNG grayscale thường nhỏ hơn so với ảnh màu đầy đủ.  
- **Độ đọc tốt hơn** – Đối với báo cáo in, grayscale thường cung cấp độ tương phản rõ ràng hơn.  
- **Tương thích** – PNG được hỗ trợ rộng rãi trên các trình duyệt, trình soạn thảo và thiết bị di động.  

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn đã có:

1. Java Development Kit (JDK) được cài đặt trên hệ thống.  
2. Thư viện Aspose.Note cho Java. Bạn có thể tải xuống từ [đây](https://releases.aspose.com/note/java/).  
3. Kiến thức cơ bản về lập trình Java.  

## Nhập gói

Để bắt đầu, nhập các gói cần thiết:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Bước 1: Tải tài liệu OneNote

Đầu tiên, **tải tài liệu onenote** vào Aspose.Note. Thay thế `"Your Document Directory"` bằng đường dẫn tới thư mục cục bộ của bạn và `"Aspose.one"` bằng tên tệp OneNote của bạn.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Bước 2: Đặt đường dẫn đầu ra và tùy chọn

Xác định đường dẫn đầu ra cho ảnh grayscale và chỉ định các tùy chọn lưu. Chúng ta sẽ đặt `ColorMode` thành `GrayScale` và sử dụng định dạng **lưu tài liệu dưới dạng png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Bước 3: Lưu tài liệu

Cuối cùng, lưu tài liệu dưới dạng ảnh PNG grayscale bằng các tùy chọn đã cấu hình.

```java
oneFile.save(dataDir, options);
```

## Các vấn đề thường gặp và giải pháp
- **FileNotFoundException** – Kiểm tra lại `dataDir` để chắc chắn rằng nó trỏ tới thư mục đúng và tệp `.one` tồn tại.  
- **LicenseException** – Đảm bảo bạn đã áp dụng giấy phép Aspose.Note hợp lệ trước khi gọi `save`.  
- **Đầu ra độ phân giải thấp** – Điều chỉnh `options.setResolution(300)` để tăng DPI nếu cần.

## Câu hỏi thường gặp

**Q1: Tôi có thể lưu ảnh grayscale ở định dạng khác không?**  
A1: Có, chỉ cần thay đổi tham số `SaveFormat` trong hàm khởi tạo `ImageSaveOptions` thành `Jpeg`, `Bmp`, v.v.

**Q2: Aspose.Note có tương thích với?**  
A2: Aspose.Note hỗ trợ Microsoft OneNote 2010 và các phiên bản sau này.

**Q3: Aspose.Note có yêu cầu giấy phép để sử dụng không?**  
A3: Giấy phép hợp lệ là bắt buộc cho môi trường sản xuất, nhưng bạn có thể nhận giấy phép dùng thử tạm thời để đánh giá.

**Q4: Tôi có thể thao tác các khía cạnh khác của tài liệu trước khi lưu dưới dạng ảnh không?**  
A4: Chắc chắn! Aspose.Note cung cấp API toàn diện để chỉnh sửa các phần, trang và nội dung trước khi xuất.

**Q5: Tôi có thể tìm hỗ trợ ở đâu nếu gặp vấn đề?**  
A5: Bạn có thể tìm hỗ trợ trên diễn đàn Aspose.Note [tại đây](https://forum.aspose.com/c/note/28).

## Kết luận

Bạn đã học **cách xuất onenote** bằng cách tải tệp OneNote, cấu hình các tùy chọn lưu để **tạo ảnh grayscale**, và **lưu tài liệu dưới dạng PNG**. Kỹ thuật này hữu ích cho việc tạo ra các hình ảnh nhẹ, sẵn sàng in từ sổ tay OneNote. Hãy thoải mái thử nghiệm các thiết lập `ColorMode` khác hoặc các định dạng ảnh để phù hợp với nhu cầu dự án của bạn.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2025-12-17  
**Kiểm tra với:** Aspose.Note 24.12 cho Java  
**Tác giả:** Aspose  

---