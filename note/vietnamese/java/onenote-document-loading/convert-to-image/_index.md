---
title: Chuyển đổi tài liệu OneNote thành hình ảnh - Java
linktitle: Chuyển đổi tài liệu OneNote thành hình ảnh - Java
second_title: API Java Aspose.Note
description: Tìm hiểu cách chuyển đổi OneNote thành hình ảnh bằng Aspose.Note for Java. Thực hiện theo các bước đơn giản, tải tài liệu, khởi tạo các tùy chọn và lưu dưới dạng PNG.
type: docs
weight: 14
url: /vi/java/onenote-document-loading/convert-to-image/
---
## Giới thiệu

Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình sử dụng Aspose.Note for Java để chuyển đổi tài liệu OneNote thành hình ảnh. Chúng tôi sẽ chia nhỏ từng bước thành các hướng dẫn dễ thực hiện.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn có những điều sau:

1. Bộ công cụ phát triển Java (JDK) được cài đặt trên hệ thống của bạn.
2.  Aspose.Note cho thư viện Java. Bạn có thể tải nó xuống từ[đây](https://releases.aspose.com/note/java/).

## Gói nhập khẩu

Đầu tiên, nhập các gói cần thiết vào mã Java của bạn:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Bây giờ hãy chia mã ví dụ được cung cấp thành nhiều bước:

## Bước 1: Thiết lập thư mục tài liệu

Xác định thư mục chứa tài liệu OneNote của bạn:

```java
String dataDir = "Your Document Directory";
```

 Thay thế`"Your Document Directory"` với đường dẫn đến tài liệu OneNote của bạn.

## Bước 2: Tải tài liệu

Tải tài liệu OneNote vào Aspose.Note:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Đảm bảo`"Sample1.one"` khớp với tên tệp tài liệu OneNote của bạn.

## Bước 3: Khởi tạo ImageSaveOptions

 Khởi tạo`ImageSaveOptions` đối tượng để chỉ định định dạng lưu:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Ở đây, chúng tôi đang lưu tài liệu dưới dạng hình ảnh PNG. Bạn có thể chọn các định dạng khác như JPEG hoặc BMP nếu cần.

## Bước 4: Lưu tài liệu dưới dạng hình ảnh

Lưu tài liệu đã tải dưới dạng hình ảnh:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Dòng này lưu tài liệu dưới dạng hình ảnh PNG với các tùy chọn được chỉ định.

## Bước 5: In xác nhận

In thông báo để xác nhận tệp đã được lưu:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Dòng này thông báo cho bạn về việc chuyển đổi thành công và vị trí của tệp hình ảnh đã lưu.

## Phần kết luận

Bằng cách làm theo các bước được nêu ở trên, bạn có thể dễ dàng chuyển đổi tài liệu OneNote thành hình ảnh bằng Aspose.Note for Java. Đó là cách đơn giản và hiệu quả để xử lý chuyển đổi tài liệu trong ứng dụng Java của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể chuyển đổi nhiều tài liệu OneNote cùng một lúc không?

Câu trả lời 1: Có, bạn có thể lặp qua danh sách tài liệu và thực hiện thao tác chuyển đổi cho từng tài liệu.

### Câu hỏi 2: Aspose.Note có hỗ trợ các định dạng đầu ra khác ngoài hình ảnh không?

Câu trả lời 2: Có, Aspose.Note hỗ trợ nhiều định dạng đầu ra khác nhau như định dạng PDF, HTML và Microsoft Word.

### Câu hỏi 3: Aspose.Note có tương thích với tất cả các phiên bản của tệp OneNote không?

A3: Aspose.Note cung cấp khả năng tương thích với các tệp OneNote được tạo trong các phiên bản khác nhau của Microsoft OneNote.

### Q4: Tôi có thể tùy chỉnh độ phân giải của hình ảnh đầu ra không?

Câu trả lời 4: Có, bạn có thể điều chỉnh độ phân giải và các thông số khác bằng cách sử dụng các tùy chọn có sẵn trong Aspose.Note.

### Câu hỏi 5: Aspose.Note có yêu cầu kết nối Internet để chuyển đổi tài liệu không?

Câu trả lời 5: Không, Aspose.Note hoạt động cục bộ mà không cần kết nối internet.