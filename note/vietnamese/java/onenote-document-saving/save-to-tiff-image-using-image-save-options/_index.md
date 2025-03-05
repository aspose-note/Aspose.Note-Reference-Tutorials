---
title: Lưu vào hình ảnh TIFF bằng tùy chọn lưu hình ảnh trong OneNote
linktitle: Lưu vào hình ảnh TIFF bằng tùy chọn lưu hình ảnh trong OneNote
second_title: API Java Aspose.Note
description: Chuyển đổi tài liệu OneNote sang TIFF và kiểm soát kích thước cũng như chất lượng tệp! Chọn nén Jpeg, PackBits hoặc Fax trong Java. Nhận ví dụ về mã và tìm hiểu cách thực hiện! #OneNote #Java #Aspose
type: docs
weight: 21
url: /vi/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---
## Giới thiệu

Trong hướng dẫn này, bạn sẽ tìm hiểu cách lưu tài liệu sang định dạng hình ảnh TIFF bằng các phương pháp nén khác nhau trong Aspose.Note cho Java. Chúng tôi sẽ đề cập đến các điều kiện tiên quyết, nhập gói và cung cấp hướng dẫn từng bước cho từng phương pháp nén.

## Điều kiện tiên quyết

Trước khi bắt đầu, hãy đảm bảo bạn có những điều sau:

- Bộ công cụ phát triển Java (JDK) được cài đặt trên hệ thống của bạn.
- Aspose.Note cho thư viện Java được tải xuống và định cấu hình.
- Hiểu biết cơ bản về ngôn ngữ lập trình Java.

## Gói nhập khẩu

Trước tiên, bạn cần nhập các gói cần thiết vào tệp Java của mình:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Bước 1: Lưu vào TIFF bằng nén JPEG

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // Đường dẫn đến thư mục tài liệu.
    String dataDir = "Your Document Directory";

    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  Tải tài liệu bằng cách sử dụng`Document` lớp học.
-  Tạo một thể hiện của`ImageSaveOptions` và chỉ định loại nén TIFF là JPEG.
- Đặt chất lượng mong muốn (tùy chọn).
- Lưu tài liệu sang định dạng TIFF bằng các tùy chọn đã chỉ định.

## Bước 2: Lưu vào TIFF bằng cách sử dụng nén PackBits

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // Đường dẫn đến thư mục tài liệu.
    String dataDir = "Your Document Directory";

    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  Tải tài liệu bằng cách sử dụng`Document` lớp học.
-  Tạo một thể hiện của`ImageSaveOptions` và chỉ định loại nén TIFF là PackBits.
- Lưu tài liệu sang định dạng TIFF bằng các tùy chọn đã chỉ định.

## Bước 3: Lưu vào TIFF bằng cách sử dụng nén fax CCITT nhóm 3

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // Đường dẫn đến thư mục tài liệu.
    String dataDir = "Your Document Directory";

    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  Tải tài liệu bằng cách sử dụng`Document` lớp học.
-  Tạo một thể hiện của`ImageSaveOptions` và chỉ định loại nén TIFF là CCITT Nhóm 3 Fax.
- Đặt chế độ màu thành đen trắng.
- Lưu tài liệu sang định dạng TIFF bằng các tùy chọn đã chỉ định.

## Phần kết luận

Trong hướng dẫn này, bạn đã học cách lưu tài liệu sang định dạng hình ảnh TIFF bằng các phương pháp nén khác nhau trong Aspose.Note cho Java. Bằng cách làm theo hướng dẫn từng bước, bạn có thể sử dụng hiệu quả các khả năng của Aspose.Note để đáp ứng yêu cầu của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.Note for Java để chuyển đổi các định dạng tài liệu khác sang TIFF không?

Trả lời 1: Có, Aspose.Note for Java hỗ trợ chuyển đổi từ nhiều định dạng tài liệu khác nhau sang TIFF, bao gồm cả tài liệu OneNote.

### Câu hỏi 2: Tầm quan trọng của việc chỉ định kiểu nén khi lưu vào TIFF là gì?

Câu trả lời 2: Việc chỉ định kiểu nén cho phép bạn kiểm soát chất lượng hình ảnh và kích thước tệp. Các phương pháp nén khác nhau đưa ra sự cân bằng giữa chất lượng và tỷ lệ nén.

### Câu hỏi 3: Aspose.Note dành cho Java có phù hợp để xử lý hàng loạt tài liệu không?

Câu trả lời 3: Có, Aspose.Note for Java cung cấp các API để xử lý hàng loạt, cho phép bạn tự động hóa các tác vụ chuyển đổi tài liệu một cách hiệu quả.

### Q4: Tôi có thể tùy chỉnh thêm cài đặt nén không?

Trả lời 4: Có, bạn có thể điều chỉnh các thông số như chất lượng, độ phân giải và phương pháp nén để điều chỉnh đầu ra theo yêu cầu của mình.

### Câu hỏi 5: Aspose.Note dành cho Java có cung cấp hỗ trợ kỹ thuật không?

Câu trả lời 5: Có, Aspose cung cấp hỗ trợ kỹ thuật toàn diện thông qua các diễn đàn và hệ thống dựa trên phiếu.