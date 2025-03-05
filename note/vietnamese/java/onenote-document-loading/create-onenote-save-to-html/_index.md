---
title: Tạo tài liệu OneNote và lưu vào HTML - Java
linktitle: Tạo tài liệu OneNote và lưu vào HTML - Java
second_title: API Java Aspose.Note
description: Tìm hiểu cách tạo và lưu tài liệu OneNote dưới dạng HTML bằng Aspose.Note for Java. Tích hợp vào các ứng dụng Java để xử lý tệp OneNote theo chương trình.

type: docs
weight: 18
url: /vi/java/onenote-document-loading/create-onenote-save-to-html/
---
## Giới thiệu

Aspose.Note for Java là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote theo chương trình. Trong hướng dẫn này, chúng ta sẽ khám phá cách tạo tài liệu OneNote và lưu nó sang định dạng HTML bằng Aspose.Note cho Java.

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu, hãy đảm bảo rằng bạn có những điều sau:

1. Bộ công cụ phát triển Java (JDK) được cài đặt trên hệ thống của bạn.
2.  Aspose.Note cho thư viện Java. Bạn có thể tải nó xuống từ[đây](https://releases.aspose.com/note/java/).
3. Kiến thức cơ bản về lập trình Java.

## Gói nhập khẩu

Đầu tiên, nhập các gói cần thiết vào dự án Java của bạn:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Bước 1: Tạo đối tượng tài liệu OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Mã này khởi tạo một`Document` đối tượng bằng cách tải tệp OneNote mẫu.

## Bước 2: Lưu dưới dạng HTML vào Luồng bộ nhớ

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Ở đây, chúng tôi thiết lập các tùy chọn lưu HTML và lưu tài liệu vào luồng bộ nhớ.

## Bước 3: Lưu dưới dạng HTML với tài nguyên trong các tệp riêng biệt

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Bước này lưu tài liệu dưới dạng HTML với các tài nguyên như CSS, phông chữ và hình ảnh trong các tệp riêng biệt.

## Bước 4: Lưu dưới dạng HTML vào Luồng bộ nhớ bằng lệnh gọi lại để tiết kiệm tài nguyên

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Ở đây, chúng tôi lưu tài liệu dưới dạng HTML vào luồng bộ nhớ bằng cách sử dụng lệnh gọi lại để xử lý việc tiết kiệm tài nguyên.

## Phần kết luận

Chúc mừng! Bạn đã học cách tạo tài liệu OneNote và lưu nó sang định dạng HTML bằng Aspose.Note cho Java. Bây giờ bạn có thể tích hợp chức năng này vào các ứng dụng Java của mình để hoạt động với các tệp OneNote theo chương trình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể chuyển đổi nhiều tài liệu OneNote sang HTML cùng một lúc không?

Câu trả lời 1: Có, bạn có thể lặp qua nhiều tài liệu và áp dụng quy trình lưu lặp đi lặp lại.

### Câu hỏi 2: Aspose.Note for Java có hỗ trợ các định dạng đầu ra khác ngoài HTML không?

Câu trả lời 2: Có, Aspose.Note for Java hỗ trợ nhiều định dạng đầu ra khác nhau bao gồm định dạng PDF, DOCX và hình ảnh.

### Câu hỏi 3: Có phiên bản dùng thử cho Aspose.Note cho Java không?

Đ3: Có, bạn có thể tải xuống phiên bản dùng thử miễn phí từ[đây](https://releases.aspose.com/).

### Câu hỏi 4: Tôi có thể nhận hỗ trợ cho Aspose.Note cho Java ở đâu?

 A4: Bạn có thể nhận được hỗ trợ từ[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28).

### Câu hỏi 5: Làm cách nào tôi có thể mua giấy phép Aspose.Note cho Java?

 Câu trả lời 5: Bạn có thể mua giấy phép từ[trang web giả định](https://purchase.aspose.com/buy).