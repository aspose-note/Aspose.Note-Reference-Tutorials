---
title: Lưu bằng hệ thống con phông chữ được chỉ định trong OneNote
linktitle: Lưu bằng hệ thống con phông chữ được chỉ định trong OneNote
second_title: API Java Aspose.Note
description: Tìm hiểu cách lưu tài liệu OneNote bằng hệ thống con phông chữ được chỉ định trong Java với Aspose.Note. Đảm bảo thể hiện phông chữ nhất quán trên các nền tảng một cách dễ dàng.
weight: 22
url: /vi/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu bằng hệ thống con phông chữ được chỉ định trong OneNote

## Giới thiệu

Aspose.Note for Java cung cấp các khả năng mạnh mẽ để làm việc với tài liệu OneNote. Một yêu cầu chung khi làm việc với những tài liệu như vậy là đảm bảo rằng phông chữ được duy trì đúng cách, đặc biệt nếu tài liệu được xuất hoặc lưu ở các định dạng khác nhau như PDF. Hướng dẫn này sẽ hướng dẫn bạn quy trình lưu tài liệu OneNote trong khi chỉ định hệ thống con phông chữ, đảm bảo thể hiện văn bản nhất quán và chính xác trên nhiều nền tảng khác nhau.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn đã thiết lập các điều kiện tiên quyết sau:

### 1. Bộ công cụ phát triển Java (JDK)

 Đảm bảo bạn đã cài đặt Bộ công cụ phát triển Java (JDK) trên hệ thống của mình. Bạn có thể tải nó xuống từ[đây](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) nếu bạn chưa làm vậy.

### 2. Aspose.Note cho Thư viện Java

 Tải xuống và thiết lập thư viện Aspose.Note cho Java. Bạn có thể tải nó xuống từ[trang mạng](https://releases.aspose.com/note/java/).

## Gói nhập khẩu

Đảm bảo nhập các gói cần thiết trong dự án Java của bạn:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Bây giờ, hãy chia từng ví dụ thành nhiều bước để hiểu rõ hơn về quy trình.

## Bước 1: Lưu bằng hệ thống con phông chữ tài liệu với tên phông chữ mặc định

Bước này trình bày cách lưu tài liệu ở định dạng PDF bằng tên phông chữ mặc định được chỉ định.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Chỉ định phông chữ mặc định.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Lưu tài liệu dưới dạng PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Ở bước này:
- Tài liệu OneNote được tải bằng Aspose.Note.
- Phông chữ mặc định được chỉ định là "Time New Roman".
- Tài liệu được lưu ở định dạng PDF với phông chữ được chỉ định.

## Bước 2: Lưu bằng hệ thống con phông chữ tài liệu với phông chữ mặc định từ tệp

Bước này trình bày cách lưu tài liệu ở định dạng PDF bằng phông chữ mặc định được tải từ một tệp.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Chỉ định đường dẫn đến tệp phông chữ.
    String fontFile = "geo_1.ttf";

    // Chỉ định phông chữ mặc định từ tệp.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Lưu tài liệu dưới dạng PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Ở bước này:
- Tệp phông chữ "geo_1.ttf" đã được tải.
- Phông chữ mặc định được chỉ định từ tệp phông chữ đã tải.
- Tài liệu được lưu ở định dạng PDF với phông chữ được chỉ định.

## Bước 3: Lưu bằng hệ thống con phông chữ tài liệu với phông chữ mặc định từ luồng

Bước này trình bày cách lưu tài liệu ở định dạng PDF bằng phông chữ mặc định được tải từ luồng.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Chỉ định đường dẫn đến tệp phông chữ.
    String fontFile = "geo_1.ttf";

    // Tải tệp phông chữ dưới dạng luồng.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Chỉ định phông chữ mặc định từ luồng.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Lưu tài liệu dưới dạng PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Ở bước này:
- Tệp phông chữ "geo_1.ttf" được tải dưới dạng luồng.
- Phông chữ mặc định được chỉ định từ luồng đã tải.
- Tài liệu được lưu ở định dạng PDF với phông chữ được chỉ định.

## Phần kết luận

Trong hướng dẫn này, chúng ta đã tìm hiểu cách lưu tài liệu OneNote bằng hệ thống con phông chữ được chỉ định trong Java bằng Aspose.Note. Bằng cách làm theo các bước này, bạn có thể đảm bảo cách trình bày phông chữ nhất quán trên nhiều nền tảng khác nhau khi xuất hoặc lưu tài liệu của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể chỉ định các phông chữ khác nhau cho các phần khác nhau của tài liệu không?

Câu trả lời 1: Có, bạn có thể chỉ định các phông chữ khác nhau cho các phần khác nhau của tài liệu bằng Aspose.Note for Java.

### Câu hỏi 2: Aspose.Note có tương thích với tất cả các phiên bản OneNote không?

Câu trả lời 2: Aspose.Note hỗ trợ nhiều phiên bản OneNote khác nhau, đảm bảo khả năng tương thích trên các môi trường khác nhau.

### Câu hỏi 3: Làm cách nào để xử lý việc thiếu phông chữ khi lưu tài liệu?

Câu trả lời 3: Aspose.Note cung cấp các tùy chọn để chỉ định phông chữ mặc định nhằm xử lý phông chữ bị thiếu một cách hiệu quả trong quá trình lưu tài liệu.

### Q4: Tôi có thể tùy chỉnh các thuộc tính phông chữ như kích thước và kiểu dáng không?

Câu trả lời 4: Có, bạn có thể tùy chỉnh các thuộc tính phông chữ như kích thước, kiểu và màu sắc bằng cách sử dụng Aspose.Note for Java.

### Câu hỏi 5: Có phiên bản dùng thử cho Aspose.Note cho Java không?

Câu trả lời 5: Có, bạn có thể dùng thử miễn phí Aspose.Note dành cho Java từ trang web.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
