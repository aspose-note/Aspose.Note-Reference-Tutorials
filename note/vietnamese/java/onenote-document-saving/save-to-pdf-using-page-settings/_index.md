---
title: Lưu vào PDF bằng Cài đặt trang trong OneNote - Aspose.Note
linktitle: Lưu vào PDF bằng Cài đặt trang trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Tìm hiểu cách lưu tài liệu OneNote thành PDF trong Java bằng thư viện Aspose.Note. Hướng dẫn từng bước với các ví dụ về mã cho các cài đặt trang khác nhau.
weight: 19
url: /vi/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu vào PDF bằng Cài đặt trang trong OneNote - Aspose.Note

## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ tìm hiểu cách lưu tài liệu OneNote sang định dạng PDF bằng cách sử dụng các cài đặt trang khác nhau với Aspose.Note cho Java. Chúng tôi sẽ đề cập đến hai phương pháp: lưu bằng cài đặt trang Letter và lưu bằng cài đặt trang A4 không giới hạn chiều cao.

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

1. Bộ công cụ phát triển Java (JDK) được cài đặt trên hệ thống của bạn.
2. Thư viện Aspose.Note for Java được tải xuống và đưa vào dự án Java của bạn.
3. Hiểu biết cơ bản về ngôn ngữ lập trình Java.

## Gói nhập khẩu

Đảm bảo rằng bạn đã nhập các gói cần thiết để sử dụng Aspose.Note for Java trong dự án của mình. Đây là báo cáo nhập khẩu:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Lưu vào PDF bằng cách sử dụng cài đặt trang thư

### Bước 1: Tải tài liệu

Đầu tiên, tải tài liệu OneNote vào Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Bước 2: Xác định đường dẫn đích

Chỉ định đường dẫn đích cho tệp PDF:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Bước 3: Lưu tài liệu

Lưu tài liệu với cài đặt trang Letter:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Lưu vào PDF bằng cách sử dụng cài đặt trang A4 không giới hạn chiều cao

### Bước 1: Tải tài liệu

Tương tự, tải tài liệu OneNote vào Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Bước 2: Xác định đường dẫn đích

Chỉ định đường dẫn đích cho tệp PDF:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Bước 3: Lưu tài liệu

Lưu tài liệu với thiết lập trang A4 không giới hạn chiều cao:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Sau khi làm theo các bước này, bạn sẽ lưu thành công tài liệu OneNote của mình sang PDF bằng các cài đặt trang khác nhau.

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã khám phá cách lưu tài liệu OneNote sang định dạng PDF bằng thư viện Aspose.Note for Java. Bằng cách làm theo hướng dẫn từng bước, bạn có thể dễ dàng tích hợp chức năng này vào các ứng dụng Java của mình.

## Câu hỏi thường gặp

### Q1: Tôi có thể tùy chỉnh thêm cài đặt trang không?

Câu trả lời 1: Có, bạn có thể tùy chỉnh cài đặt trang theo yêu cầu của mình bằng Aspose.Note for Java.

### Câu hỏi 2: Aspose.Note có hỗ trợ các định dạng đầu ra khác ngoài PDF không?

Câu trả lời 2: Có, Aspose.Note hỗ trợ nhiều định dạng đầu ra khác nhau bao gồm hình ảnh và HTML.

### Câu hỏi 3: Aspose.Note có tương thích với các phiên bản khác nhau của tệp OneNote không?

Câu trả lời 3: Có, Aspose.Note hỗ trợ các tệp OneNote từ các phiên bản khác nhau bao gồm .one và .onetoc2.

### Câu hỏi 4: Tôi có thể chuyển đổi nhiều tệp OneNote thành PDF trong một lần chạy không?

Câu trả lời 4: Có, bạn có thể xử lý hàng loạt nhiều tệp OneNote bằng Aspose.Note for Java.

### Câu hỏi 5: Có phiên bản dùng thử nào dành cho mục đích thử nghiệm không?

Câu trả lời 5: Có, bạn có thể dùng thử miễn phí Aspose.Note dành cho Java từ trang web.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
