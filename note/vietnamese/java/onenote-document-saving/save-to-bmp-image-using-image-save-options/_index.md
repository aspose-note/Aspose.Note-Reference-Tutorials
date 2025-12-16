---
date: 2025-12-16
description: Tìm hiểu cách lưu tài liệu OneNote thành hình ảnh BMP bằng các tùy chọn
  lưu ảnh của Aspose.Note cho Java. Cũng xem cách lưu OneNote thành PDF hoặc PNG.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: Cách lưu OneNote thành ảnh BMP bằng tùy chọn lưu ảnh
url: /vi/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# cách lưu onenote thành ảnh BMP bằng tùy chọn lưu ảnh

## Giới thiệu

Aspose.Note for Java là một thư viện mạnh mẽ cho phép các nhà phát triển Java làm việc với các tệp Microsoft OneNote một cách lập trình. **Trong hướng dẫn này bạn sẽ học cách lưu tài liệu onenote thành ảnh BMP** bằng tính năng Image Save Options của Aspose.Note for Java. Chúng tôi sẽ hướng dẫn từng bước, giải thích lý do bạn có thể chọn BMP thay vì các định dạng khác, và chỉ cho bạn cách tích hợp khả năng này vào ứng dụng của mình.

## Câu trả lời nhanh
- **Lớp Image Save Options làm gì?** Nó cho phép bạn chỉ định định dạng ảnh đầu ra (BMP, PNG, JPEG, v.v.) khi chuyển đổi một trang OneNote.  
- **Tôi có cần giấy phép để chạy mẫu không?** Bản dùng thử miễn phí đủ cho việc đánh giá, nhưng cần giấy phép thương mại cho môi trường sản xuất.  
- **Tôi có thể chuyển đổi một trang OneNote sang PDF hoặc PNG thay vì BMP không?** Có – chỉ cần thay đổi enum `SaveFormat` (ví dụ, `SaveFormat.Pdf` hoặc `SaveFormat.Png`).  
- **Phiên bản Java nào được hỗ trợ?** Java 8 trở lên được hỗ trợ đầy đủ.  
- **Có xử lý đặc biệt nào cho tài liệu lớn không?** Bạn có thể stream đầu ra để tránh tiêu thụ bộ nhớ cao.

## Image Save Options là gì trong Aspose.Note?
Lớp `ImageSaveOptions` cung cấp khả năng kiểm soát chi tiết cách các trang OneNote được render thành ảnh raster. Bạn có thể đặt định dạng ảnh, độ phân giải, độ sâu màu và nhiều hơn nữa. Sự linh hoạt này giúp bạn dễ dàng tạo các tệp BMP cho hệ thống cũ hoặc các tệp PNG/JPEG cho việc sử dụng trên web.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có:

1. Kiến thức cơ bản về ngôn ngữ lập trình Java.  
2. JDK (Java Development Kit) đã được cài đặt trên máy của bạn.  
3. Một IDE như Eclipse hoặc IntelliJ IDEA.  
4. Thư viện Aspose.Note for Java – tải về từ [here](https://releases.aspose.com/note/java/).

## Nhập gói

Đầu tiên, nhập các lớp Aspose.Note cần thiết và các tiện ích I/O chuẩn của Java:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Bước 1: Tải tài liệu OneNote

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Ở đây chúng ta chỉ đến thư mục chứa tệp OneNote nguồn (`Aspose.one`) và tải nó vào một đối tượng `Document`. Đối tượng này cho phép bạn truy cập đầy đủ vào các trang, phần và các yếu tố khác trong sổ ghi chú.

## Bước 2: Lưu tài liệu dưới dạng ảnh BMP

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

Chúng ta ghép tên tệp đầu ra, sau đó gọi `save` với một thể hiện `ImageSaveOptions` được cấu hình cho **BMP** (`SaveFormat.Bmp`).  
Nếu bạn muốn **lưu trang onenote** dưới dạng PNG, chỉ cần thay thế `SaveFormat.Bmp` bằng `SaveFormat.Png`. Tương tự, `SaveFormat.Pdf` cho phép bạn thực hiện chuyển đổi **onenote sang pdf**.

## Tại sao chọn BMP?
- **Chất lượng không mất mát** – BMP lưu dữ liệu pixel thô, bảo toàn ngoại hình chính xác của trang gốc.  
- **Tính tương thích** – Các ứng dụng Windows cũ thường yêu cầu tệp BMP.  
- **Đơn giản** – Không có hiện tượng nén, làm cho nó lý tưởng cho các xử lý ảnh tiếp theo.

## Vấn đề thường gặp & Mẹo

- **Lỗi đường dẫn tệp** – Đảm bảo `dataDir` kết thúc bằng ký tự phân tách tệp thích hợp (`/` hoặc `\`).  
- **Sổ ghi chú lớn** – Đối với các tệp OneNote rất lớn, hãy cân nhắc lưu từng trang riêng biệt để giảm mức tiêu thụ bộ nhớ.  
- **Ngoại lệ giấy phép** – Chạy mã mà không có giấy phép hợp lệ sẽ thêm watermark vào ảnh được tạo.

## Kết luận

Trong hướng dẫn này chúng tôi đã trình bày **cách lưu onenote** tài liệu thành ảnh BMP bằng `ImageSaveOptions` của Aspose.Note for Java. Bằng cách thay đổi enum `SaveFormat` bạn cũng có thể tạo PNG, JPEG, PDF hoặc các định dạng hỗ trợ khác, cung cấp cho bạn một cách linh hoạt để xuất nội dung OneNote cho bất kỳ kịch bản downstream nào.

## Câu hỏi thường gặp

**Q1: Tôi có thể lưu tài liệu OneNote sang các định dạng ảnh khác ngoài BMP không?**  
A: Có, bạn có thể sử dụng `ImageSaveOptions` với `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` hoặc `SaveFormat.Tiff` để xuất sang các định dạng đó.

**Q2: Aspose.Note for Java có hỗ trợ chuyển đổi giữa các định dạng tài liệu khác nhau không?**  
A: Chắc chắn. Ngoài các định dạng ảnh, bạn có thể chuyển đổi tệp OneNote sang PDF, DOCX, HTML và nhiều hơn nữa bằng cách sử dụng `SaveFormat` phù hợp.

**Q3: Aspose.Note for Java có tương thích với các phiên bản OneNote mới nhất không?**  
A: Có, thư viện được cập nhật thường xuyên để đồng bộ với các phiên bản OneNote mới nhất.

**Q4: Tôi có thể thao tác nội dung của tài liệu OneNote một cách lập trình không?**  
A: Có, bạn có thể thêm, chỉnh sửa hoặc xóa các trang, phần và nội dung phong phú (văn bản, hình ảnh, bảng) thông qua API.

**Q5: Aspose.Note for Java có cung cấp hỗ trợ kỹ thuật không?**  
A: Có, Aspose cung cấp hỗ trợ kỹ thuật và một diễn đàn chuyên dụng. Truy cập [Aspose.Note forum](https://forum.aspose.com/c/note/28) để được trợ giúp.

---

**Last Updated:** 2025-12-16  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
