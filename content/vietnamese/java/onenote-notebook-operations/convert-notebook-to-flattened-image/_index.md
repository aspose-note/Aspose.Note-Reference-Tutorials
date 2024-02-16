---
title: Chuyển đổi sổ ghi chép thành hình ảnh phẳng trong OneNote - Aspose.Note
linktitle: Chuyển đổi sổ ghi chép thành hình ảnh phẳng trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Tìm hiểu cách chuyển đổi sổ ghi chép thành hình ảnh phẳng trong OneNote bằng Aspose.Note for Java. Bảo toàn tất cả các thành phần trong một tệp hình ảnh một cách dễ dàng.
type: docs
weight: 13
url: /vi/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---
## Giới thiệu

Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình chuyển đổi sổ ghi chép thành hình ảnh phẳng trong OneNote bằng Aspose.Note cho Java. Điều này cho phép bạn lưu sổ ghi chép của mình dưới dạng tệp hình ảnh, đảm bảo rằng tất cả các thành phần được giữ nguyên ở một định dạng hình ảnh duy nhất.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn có những điều sau:

1. Bộ công cụ phát triển Java (JDK) được cài đặt trên hệ thống của bạn.
2.  Thư viện Aspose.Note for Java được tải xuống và thiết lập trong dự án Java của bạn. Bạn có thể tải thư viện từ[đây](https://releases.aspose.com/note/java/).
3. Kiến thức cơ bản về lập trình Java.

## Gói nhập khẩu

Để bắt đầu, bạn cần nhập các gói cần thiết từ Aspose.Note cho Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Bước 1: Thiết lập thư mục tài liệu

Đầu tiên, xác định thư mục chứa tệp sổ ghi chép của bạn:

```java
String dataDir = "Your Document Directory";
```

 Thay thế`"Your Document Directory"` với đường dẫn đến tệp sổ ghi chép của bạn.

## Bước 2: Tải sổ tay

 Tiếp theo, tải tệp sổ ghi chép bằng cách sử dụng`Notebook` lớp học:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Đảm bảo thay thế`"test.onetoc2"` với tên của tập tin sổ ghi chép của bạn.

## Bước 3: Đặt tùy chọn lưu ảnh

Bây giờ, hãy thiết lập các tùy chọn để lưu sổ ghi chép dưới dạng hình ảnh. Chúng tôi sẽ chỉ định định dạng lưu là PNG và đặt độ phân giải thành 400 dpi:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Bạn có thể điều chỉnh độ phân giải theo yêu cầu của bạn.

## Bước 4: Làm phẳng Notebook

Để đảm bảo rằng tất cả các phần tử được làm phẳng thành một hình ảnh duy nhất, hãy đặt`flatten` tùy chọn để`true`:

```java
saveOptions.setFlatten(true);
```

Điều này đảm bảo rằng hình ảnh thu được sẽ duy trì bố cục của sổ ghi chép của bạn.

## Bước 5: Lưu hình ảnh

Cuối cùng, lưu sổ ghi chép dưới dạng hình ảnh phẳng:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Thay thế`"ExportImageasFlattenedNotebook_out.png"` với tên tệp đầu ra mong muốn của bạn.

## Phần kết luận

Tóm lại, bằng cách sử dụng Aspose.Note cho Java, bạn có thể dễ dàng chuyển đổi sổ ghi chép của mình thành hình ảnh phẳng trong OneNote. Quá trình này đảm bảo rằng tất cả các thành phần được giữ nguyên ở một định dạng hình ảnh duy nhất, tạo điều kiện dễ dàng chia sẻ và xem.

## Câu hỏi thường gặp

### Q1: Tôi có thể điều chỉnh độ phân giải của hình ảnh đầu ra không?

 Trả lời 1: Có, bạn có thể điều chỉnh độ phân giải theo yêu cầu của mình bằng cách sửa đổi`setResolution` tham số phương thức.

### Câu hỏi 2: Aspose.Note có hỗ trợ xuất các định dạng hình ảnh khác không?

Câu trả lời 2: Có, Aspose.Note hỗ trợ nhiều định dạng hình ảnh khác nhau như PNG, JPEG, BMP, v.v. để xuất sổ tay.

### Câu 3: Tôi có thể tùy chỉnh thêm hình ảnh đầu ra không?

Câu trả lời 3: Có, Aspose.Note cung cấp các tùy chọn mở rộng để tùy chỉnh hình ảnh đầu ra, bao gồm cài đặt kích thước trang, hướng và chất lượng.

### Câu hỏi 4: Có phiên bản dùng thử cho Aspose.Note cho Java không?

 Đ4: Có, bạn có thể tải phiên bản dùng thử miễn phí từ[đây](https://releases.aspose.com/).

### Câu hỏi 5: Tôi có thể tìm hỗ trợ cho Aspose.Note dành cho Java ở đâu?

 Câu trả lời 5: Bạn có thể tìm thấy sự hỗ trợ và tài nguyên trên diễn đàn Aspose.Note[đây](https://forum.aspose.com/c/note/28).