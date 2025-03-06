---
title: Lưu vào hình ảnh thang độ xám trong OneNote - Aspose.Note
linktitle: Lưu vào hình ảnh thang độ xám trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Tìm hiểu cách lưu tài liệu dưới dạng hình ảnh thang độ xám trong OneNote bằng Aspose.Note for Java. Dễ dàng thao tác với tài liệu Microsoft OneNote theo chương trình.
weight: 17
url: /vi/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu vào hình ảnh thang độ xám trong OneNote - Aspose.Note

## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ khám phá cách lưu tài liệu dưới dạng hình ảnh thang độ xám trong OneNote bằng Aspose.Note cho Java. Hình ảnh thang độ xám là hình ảnh đơn sắc trong đó thông tin màu sắc chỉ được thể hiện bằng các sắc thái của màu xám. Aspose.Note là một API Java mạnh mẽ cho phép thao tác các tài liệu Microsoft OneNote theo chương trình.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn có những điều sau:

1. Bộ công cụ phát triển Java (JDK) được cài đặt trên hệ thống của bạn.
2.  Aspose.Note cho thư viện Java. Bạn có thể tải nó xuống từ[đây](https://releases.aspose.com/note/java/).
3. Hiểu biết cơ bản về lập trình Java.

## Gói nhập khẩu

Để bắt đầu, hãy nhập các gói cần thiết:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Bước 1: Tải tài liệu

 Đầu tiên, tải tài liệu vào Aspose.Note. Thay thế`"Your Document Directory"` với đường dẫn đến thư mục tài liệu của bạn và`"Aspose.one"` với tên tài liệu OneNote của bạn.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Bước 2: Đặt đường dẫn và tùy chọn đầu ra

Xác định đường dẫn đầu ra cho hình ảnh thang độ xám và chỉ định các tùy chọn lưu. Chúng tôi sẽ đặt chế độ màu thành thang độ xám.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Bước 3: Lưu tài liệu

Cuối cùng, lưu tài liệu dưới dạng hình ảnh thang độ xám bằng các tùy chọn đã chỉ định.

```java
oneFile.save(dataDir, options);
```

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách lưu tài liệu dưới dạng hình ảnh thang độ xám trong OneNote bằng Aspose.Note cho Java. Điều này có thể cực kỳ hữu ích cho các ứng dụng khác nhau yêu cầu hình ảnh thang độ xám.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể lưu hình ảnh thang độ xám ở định dạng khác không?

 A1: Có, bạn có thể. Đơn giản chỉ cần thay đổi`SaveFormat` tham số trong`ImageSaveOptions` constructor theo định dạng mong muốn của bạn.

### Câu hỏi 2: Aspose.Note có tương thích với tất cả các phiên bản của tài liệu OneNote không?

A2: Aspose.Note hỗ trợ Microsoft OneNote 2010 trở lên.

### Câu hỏi 3: Aspose.Note có cần giấy phép sử dụng không?

Câu trả lời 3: Có, bạn cần có giấy phép hợp lệ để sử dụng Aspose.Note trong môi trường sản xuất. Tuy nhiên, bạn có thể lấy giấy phép tạm thời cho mục đích thử nghiệm.

### Câu hỏi 4: Tôi có thể thao tác các khía cạnh khác của tài liệu trước khi lưu dưới dạng hình ảnh không?

A4: Chắc chắn rồi! Aspose.Note cung cấp nhiều tính năng để chỉnh sửa tài liệu OneNote theo chương trình.

### Câu hỏi 5: Tôi có thể tìm hỗ trợ ở đâu nếu gặp sự cố?

Câu trả lời 5: Bạn có thể tìm thấy sự hỗ trợ trên diễn đàn Aspose.Note[đây](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
