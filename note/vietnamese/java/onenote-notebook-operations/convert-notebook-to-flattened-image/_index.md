---
date: 2025-12-25
description: Tìm hiểu cách chuyển đổi OneNote sang PNG bằng Aspose.Note cho Java.
  Hướng dẫn này chỉ ra cách đặt độ phân giải hình ảnh, làm phẳng một sổ ghi chú và
  lưu OneNote dưới dạng hình ảnh một cách hiệu quả.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Cách chuyển OneNote sang PNG – Chuyển đổi sổ ghi chú thành hình ảnh với Aspose.Note
url: /vi/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển Notebook thành Hình ảnh Phẳng trong OneNote - Aspose.Note

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá cách **chuyển OneNote sang PNG** bằng cách biến toàn bộ notebook thành một hình ảnh phẳng duy nhất sử dụng Aspose.Note cho Java. Cách tiếp cận này rất phù hợp khi bạn cần chia sẻ notebook dưới dạng hình tĩnh, nhúng vào báo cáo, hoặc lưu trữ mà không mất bất kỳ chi tiết hình ảnh nào.

## Câu trả lời nhanh
- **“Flatten notebook” có nghĩa là gì?** Nó hợp nhất tất cả các thành phần trang vào một hình ảnh raster duy nhất.  
- **Định dạng nào được sử dụng?** PNG là mặc định, cung cấp chất lượng không mất mát.  
- **Tôi có thể thay đổi DPI không?** Có, sử dụng `setResolution` trên `ImageSaveOptions`.  
- **Có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Có được hỗ trợ trên mọi hệ điều hành không?** API Java chạy ở bất kỳ nơi nào có Java.

## Chuyển OneNote sang PNG là gì?

Chuyển OneNote sang PNG tạo ra một biểu diễn bitmap của mọi trang trong notebook, giữ nguyên văn bản, bản vẽ và các đối tượng nhúng trong một tệp hình ảnh duy nhất. Điều này đặc biệt hữu ích cho tài liệu, bài thuyết trình hoặc lưu trữ tuân thủ.

## Tại sao nên chuyển OneNote sang PNG với Aspose.Note?

- **Độ trung thực cao** – Tất cả các yếu tố hình ảnh được giữ nguyên.  
- **Đầu ra một tệp duy nhất** – Không cần quản lý nhiều tệp trang.  
- **Độ phân giải tùy chỉnh** – Điều chỉnh DPI để đáp ứng yêu cầu chất lượng.  
- **Không cần cài đặt Office** – Hoạt động hoàn toàn độc lập với Microsoft OneNote.

## Yêu cầu trước

Trước khi bắt đầu, hãy đảm bảo bạn có những thứ sau:

1. Java Development Kit (JDK) đã được cài đặt trên hệ thống.  
2. Thư viện Aspose.Note cho Java đã tải về và được thiết lập trong dự án Java của bạn. Bạn có thể tải thư viện từ [here](https://releases.aspose.com/note/java/).  
3. Kiến thức cơ bản về lập trình Java.

## Nhập gói

Để bắt đầu, bạn cần nhập các gói cần thiết từ Aspose.Note cho Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Bước 1: Thiết lập thư mục tài liệu

Đầu tiên, xác định thư mục chứa tệp notebook của bạn:

```java
String dataDir = "Your Document Directory";
```

Thay `"Your Document Directory"` bằng đường dẫn tới tệp notebook của bạn.

## Bước 2: Tải Notebook

Tiếp theo, tải tệp notebook bằng lớp `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Đảm bảo thay `"test.onetoc2"` bằng tên tệp notebook của bạn.

## Bước 3: Thiết lập tùy chọn lưu ảnh

Bây giờ, cấu hình các tùy chọn để lưu notebook dưới dạng ảnh. Chúng ta sẽ chỉ định định dạng lưu là PNG và đặt độ phân giải là 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Bạn có thể điều chỉnh độ phân giải theo yêu cầu. Đây là nơi bạn **đặt độ phân giải ảnh** để kiểm soát chất lượng đầu ra.

## Bước 4: Làm phẳng Notebook

Để đảm bảo tất cả các yếu tố được làm phẳng thành một hình ảnh duy nhất, đặt tùy chọn `flatten` thành `true`:

```java
saveOptions.setFlatten(true);
```

Việc đặt `flatten` thành `true` đảm bảo PNG kết quả giữ nguyên bố cục chính xác của notebook.

## Bước 5: Lưu ảnh

Cuối cùng, lưu notebook dưới dạng hình ảnh đã được làm phẳng:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Thay `"ExportImageasFlattenedNotebook_out.png"` bằng tên tệp đầu ra mong muốn của bạn. Bước này **lưu OneNote dưới dạng ảnh** mà bạn có thể chia sẻ hoặc nhúng ở bất kỳ đâu.

## Các trường hợp sử dụng phổ biến

- **Tài liệu:** Nhúng hình ảnh notebook vào sổ tay kỹ thuật hoặc hướng dẫn người dùng.  
- **Bài thuyết trình:** Sử dụng slide PNG độ phân giải cao trong PowerPoint mà không lo về tương thích phông chữ hay đối tượng.  
- **Lưu trữ:** Lưu một bản sao chỉ đọc của notebook cho các cuộc kiểm toán tuân thủ.

## Mẹo khắc phục sự cố

- **Không tìm thấy tệp:** Kiểm tra lại đường dẫn `dataDir` và chắc chắn tệp `.onetoc2` tồn tại.  
- **Ảnh chất lượng thấp:** Tăng DPI bằng cách thay đổi `documentSaveOptions.setResolution(600);`.  
- **Thiếu một số yếu tố:** Đảm bảo `saveOptions.setFlatten(true);` được bật; nếu không, một số lớp có thể vẫn còn tách rời.

## Câu hỏi thường gặp

**Q1: Tôi có thể điều chỉnh độ phân giải của ảnh đầu ra không?**  
A1: Có, bạn có thể điều chỉnh độ phân giải theo yêu cầu bằng cách thay đổi tham số của phương thức `setResolution`.

**Q2: Aspose.Note có hỗ trợ các định dạng ảnh khác để xuất không?**  
A2: Có, Aspose.Note hỗ trợ nhiều định dạng ảnh như PNG, JPEG, BMP, v.v., để xuất notebook.

**Q3: Tôi có thể tùy chỉnh thêm ảnh đầu ra không?**  
A3: Có, Aspose.Note cung cấp nhiều tùy chọn mở rộng để tùy chỉnh ảnh đầu ra, bao gồm kích thước trang, hướng và cài đặt chất lượng.

**Q4: Có phiên bản dùng thử cho Aspose.Note cho Java không?**  
A4: Có, bạn có thể lấy phiên bản dùng thử miễn phí từ [here](https://releases.aspose.com/).

**Q5: Tôi có thể tìm hỗ trợ cho Aspose.Note cho Java ở đâu?**  
A5: Bạn có thể tìm hỗ trợ và tài nguyên trên diễn đàn Aspose.Note [here](https://forum.aspose.com/c/note/28).

---

**Cập nhật lần cuối:** 2025-12-25  
**Đã kiểm tra với:** Aspose.Note cho Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}