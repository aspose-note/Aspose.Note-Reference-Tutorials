---
title: Tạo tài liệu OneNote và lưu vào HTML trong Aspose.Note
linktitle: Tạo tài liệu OneNote và lưu vào HTML trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách tạo và lưu tài liệu Microsoft OneNote sang định dạng HTML trong các ứng dụng .NET bằng API Aspose.Note. Hãy làm theo hướng dẫn toàn diện của chúng tôi với các ví dụ từng bước.
weight: 14
url: /vi/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo tài liệu OneNote và lưu vào HTML trong Aspose.Note

## Giới thiệu

Aspose.Note for .NET là một API mạnh mẽ cho phép các nhà phát triển làm việc với các tài liệu Microsoft OneNote theo chương trình trong các ứng dụng .NET của họ. Với Aspose.Note, bạn có thể tạo, thao tác và chuyển đổi các tệp OneNote một cách dễ dàng. Trong hướng dẫn này, chúng ta sẽ khám phá cách tạo tài liệu OneNote và lưu nó sang định dạng HTML bằng nhiều tùy chọn khác nhau được cung cấp bởi Aspose.Note cho .NET API.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

- Kiến thức cơ bản về ngôn ngữ lập trình C#.
- Visual Studio được cài đặt trên hệ thống của bạn.
-  Aspose.Note dành cho .NET API được cài đặt trong dự án của bạn. Bạn có thể tải nó xuống từ[đây](https://releases.aspose.com/note/net/).
- Làm quen với cấu trúc của tài liệu Microsoft OneNote.

## Nhập không gian tên

Trước khi đi sâu vào phần mã hóa, hãy nhập các không gian tên cần thiết:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Bây giờ, hãy chia từng ví dụ thành nhiều bước và xem cách tạo tài liệu OneNote và lưu nó sang định dạng HTML bằng Aspose.Note cho .NET.

## Bước 1: Tạo tài liệu OneNote với các tùy chọn mặc định

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Khởi tạo tài liệu OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Kiểu mặc định cho tất cả văn bản trong tài liệu.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Lưu vào định dạng HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

Trong bước này, chúng tôi khởi tạo tài liệu OneNote mới, thêm trang có tiêu đề và lưu nó sang định dạng HTML bằng các tùy chọn mặc định.

## Bước 2: Tạo và lưu phạm vi trang cụ thể vào HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Khởi tạo tài liệu OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Kiểu mặc định cho tất cả văn bản trong tài liệu.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Lưu vào định dạng HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Ở đây, chúng tôi trình bày cách tạo tài liệu và lưu một phạm vi trang cụ thể sang định dạng HTML.

## Bước 3: Lưu dưới dạng HTML vào Luồng bộ nhớ bằng tài nguyên nhúng

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Tải tài liệu OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Chỉ định các tùy chọn lưu HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Lưu tài liệu vào luồng bộ nhớ
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Bước này minh họa cách lưu tài liệu OneNote sang định dạng HTML với các tài nguyên được nhúng (CSS, phông chữ và hình ảnh) vào luồng bộ nhớ.

## Bước 4: Lưu dưới dạng HTML vào tệp với tài nguyên trong các tệp riêng biệt

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Tải tài liệu OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Chỉ định các tùy chọn lưu HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Lưu tài liệu vào tệp HTML với tài nguyên được lưu trữ trong các tệp riêng biệt
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

Trong bước này, chúng tôi lưu tài liệu OneNote sang định dạng HTML với tất cả tài nguyên (CSS, phông chữ và hình ảnh) được lưu trữ trong các tệp riêng biệt.

## Bước 5: Lưu dưới dạng HTML vào Luồng bộ nhớ bằng lệnh gọi lại để tiết kiệm tài nguyên

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Chỉ định cấu hình lưu cuộc gọi lại
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Chỉ định các tùy chọn lưu HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Tải tài liệu OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Lưu tài liệu sang định dạng HTML với các tài nguyên được quản lý bởi lệnh gọi lại do người dùng xác định
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Thêm dữ liệu theo cách thủ công vào luồng CSS
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Ở đây, chúng tôi trình bày cách lưu tài liệu OneNote sang định dạng HTML với các tài nguyên được quản lý bởi lệnh gọi lại do người dùng xác định.

## Phần kết luận

Trong bài viết này, chúng tôi đã khám phá cách làm việc với tài liệu OneNote và lưu chúng sang định dạng HTML bằng Aspose.Note cho .NET. Bằng cách làm theo hướng dẫn từng bước, bạn có thể dễ dàng

 tích hợp chức năng này vào các ứng dụng .NET của bạn, cho phép bạn thao tác với các tệp OneNote một cách hiệu quả.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tùy chỉnh giao diện của tệp HTML đã lưu không?

Câu trả lời 1: Có, bạn có thể tùy chỉnh giao diện bằng cách sửa đổi biểu định kiểu CSS được tạo trong quá trình chuyển đổi.

### Câu hỏi 2: Aspose.Note có hỗ trợ chuyển đổi sang các định dạng khác ngoài HTML không?

Câu trả lời 2: Có, Aspose.Note hỗ trợ chuyển đổi sang nhiều định dạng khác nhau như PDF, hình ảnh và tài liệu Microsoft Word.

### Câu 3: Aspose.Note có tương thích với các ứng dụng .NET Core không?

Câu trả lời 3: Có, Aspose.Note tương thích với cả ứng dụng .NET Framework và .NET Core.

### Câu hỏi 4: Tôi có thể trích xuất văn bản và hình ảnh từ tài liệu OneNote bằng Aspose.Note không?

Câu trả lời 4: Có, bạn có thể trích xuất văn bản và hình ảnh cũng như thực hiện nhiều thao tác khác bằng API Aspose.Note.

### Câu hỏi 5: Có phiên bản dùng thử để thử nghiệm các tính năng của Aspose.Note không?

 Câu trả lời 5: Có, bạn có thể tải xuống phiên bản dùng thử miễn phí từ[đây](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
