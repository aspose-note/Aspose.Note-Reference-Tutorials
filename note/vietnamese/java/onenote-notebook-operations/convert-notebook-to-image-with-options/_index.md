---
date: 2025-12-28
description: Tìm hiểu cách **chuyển đổi OneNote sang hình ảnh** và thiết lập độ phân
  giải hình ảnh trong Java bằng Aspose.Note. Hướng dẫn từng bước này cũng chỉ cách
  xuất các tệp PNG từ OneNote.
linktitle: Convert OneNote to Image with Options - Aspose.Note
second_title: Aspose.Note Java API
title: Chuyển đổi OneNote sang hình ảnh với các tùy chọn - Aspose.Note
url: /vi/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi OneNote sang Hình ảnh với Các tùy chọn - Aspose.Note

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học cách **convert OneNote to image** với nhiều tùy chọn khác nhau bằng cách sử dụng Aspose.Note cho Java. Cho dù bạn cần PNG độ phân giải cao cho báo cáo hay một ảnh thu nhỏ JPEG nhanh chóng, các bước dưới đây sẽ chỉ cho bạn cách thực hiện và tích hợp quy trình này vào các ứng dụng Java của mình.

## Câu trả lời nhanh
- **What does “convert OneNote to image” mean?** Nó chuyển đổi toàn bộ sổ tay OneNote thành các tệp hình ảnh raster (PNG, JPEG, v.v.).
- **Which format is recommended for lossless quality?** PNG, vì nó giữ nguyên mọi chi tiết mà không có hiện tượng nén mất dữ liệu.
- **How can I set the image resolution in Java?** Sử dụng `ImageSaveOptions.setResolution(int dpi)` thông qua `NotebookImageSaveOptions`.
- **Can I export a OneNote notebook as a PNG in one step?** Có, Aspose.Note cung cấp một lệnh `save` duy nhất với các tùy chọn phù hợp.
- **Do I need a license for production use?** Cần có giấy phép thương mại cho môi trường sản xuất; bản dùng thử miễn phí có sẵn để đánh giá.

## “convert OneNote to image” là gì?
Chuyển đổi một sổ tay OneNote sang hình ảnh có nghĩa là render mỗi trang của sổ tay thành một tệp bitmap. Điều này hữu ích để tạo các bản xem trước tĩnh, lưu trữ nội dung, hoặc nhúng các trang sổ tay vào báo cáo khi định dạng OneNote gốc không được hỗ trợ.

## Tại sao nên sử dụng Aspose.Note cho Java?
- **Full control** trên định dạng đầu ra, độ phân giải và độ sâu màu.  
- **No Microsoft Office dependency** – hoạt động trên bất kỳ môi trường Java phía máy chủ nào.  
- **Supports complex notebooks** có các tệp nhúng, nét vẽ và văn bản phong phú.

## Yêu cầu trước

1. **Java Development Kit (JDK)** – phiên bản 8 trở lên.  
2. **Aspose.Note for Java JAR files** – tải xuống thư viện mới nhất từ [here](https://releases.aspose.com/note/java/) và thêm vào classpath của dự án.  

## Nhập các gói

Đầu tiên, nhập các lớp mà chúng ta sẽ cần để tải sổ tay và cấu hình đầu ra hình ảnh.

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Bước 1: Tải sổ tay

Tải sổ tay OneNote mà bạn muốn chuyển đổi. Thay thế đường dẫn bằng vị trí của tệp `.onetoc2` của bạn.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## Bước 2: Đặt tùy chọn lưu (Cách **set image resolution java**)

Tạo một thể hiện `NotebookImageSaveOptions`, chọn định dạng đầu ra và chỉ định độ phân giải mong muốn. Trong ví dụ này chúng tôi sử dụng PNG ở 400 dpi.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

> **Pro tip:** Để xử lý nhanh hơn trên các sổ tay lớn, giảm độ phân giải (ví dụ, 150 dpi). Tăng độ phân giải cho đồ họa sẵn sàng in.

## Bước 3: Lưu sổ tay dưới dạng hình ảnh (Cách **export OneNote PNG**)

Xác định tên tệp đầu ra và gọi `save`. Các tùy chọn giống nhau sẽ được áp dụng cho mỗi trang trong sổ tay.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

Mã trên sẽ tạo ra một tệp PNG (hoặc một loạt các tệp PNG, mỗi trang một tệp) với độ phân giải bạn đã đặt.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **OutOfMemoryError** trên sổ tay lớn | Tăng kích thước heap JVM (`-Xmx2g`) hoặc giảm độ phân giải. |
| **Blank pages in output** | Đảm bảo sổ tay không được bảo vệ bằng mật khẩu; sử dụng `Notebook.load(path, password)` nếu cần. |
| **Unsupported image format** | Chỉ sử dụng `SaveFormat.Png`, `SaveFormat.Jpeg`, hoặc `SaveFormat.Bmp` – các định dạng khác không được hỗ trợ cho xuất sổ tay. |

## Câu hỏi thường gặp

**Q: Aspose.Note có thể xử lý các tệp OneNote phức tạp không?**  
A: Có, nó xử lý hiệu quả các sổ tay có tệp nhúng, chú thích nét vẽ và định dạng phong phú.

**Q: Aspose.Note cho Java có dễ tích hợp vào các dự án hiện có không?**  
A: Hoàn toàn. API đơn giản, và bạn chỉ cần thêm JAR vào classpath.

**Q: Tôi có thể tùy chỉnh đầu ra hình ảnh khi chuyển đổi một Notebook không?**  
A: Có. Bạn có thể đặt độ phân giải, định dạng và thậm chí độ sâu màu qua `ImageSaveOptions`.

**Q: Aspose.Note có cung cấp hỗ trợ cho nhà phát triển không?**  
A: Có. Aspose cung cấp tài liệu phong phú, diễn đàn và kênh hỗ trợ phản hồi nhanh.

**Q: Có bản dùng thử miễn phí cho Aspose.Note cho Java không?**  
A: Có, bạn có thể tải phiên bản dùng thử từ [here](https://releases.aspose.com/).

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}