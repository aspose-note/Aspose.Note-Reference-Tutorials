---
title: Lưu bằng cách sử dụng phông chữ được chỉ định trong Aspose.Note
linktitle: Lưu bằng cách sử dụng phông chữ được chỉ định trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách lưu tài liệu với phông chữ được chỉ định trong Aspose.Note dành cho .NET. Dễ dàng tùy chỉnh cài đặt phông chữ để định dạng tài liệu nhất quán.
type: docs
weight: 28
url: /vi/net/loading-and-saving-operations/save-using-specified-fonts/
---
## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ tìm hiểu cách lưu tài liệu bằng các phông chữ được chỉ định trong Aspose.Note cho .NET. Chúng ta sẽ khám phá các phương pháp khác nhau để đạt được điều này, từng bước một.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn có những điều sau:

1.  Aspose.Note for .NET: Đảm bảo bạn đã cài đặt Aspose.Note for .NET. Bạn có thể tải nó xuống từ[đây](https://releases.aspose.com/note/net/).

2. Môi trường phát triển: Bạn cần thiết lập môi trường phát triển để phát triển .NET.

## Nhập không gian tên

Đầu tiên, hãy nhập các không gian tên cần thiết:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Bước 1: Lưu với tên phông chữ mặc định

Trong bước này, chúng tôi sẽ lưu tài liệu bằng tên phông chữ mặc định được chỉ định.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Đường dẫn đến thư mục tài liệu.
    string dataDir = "Your Document Directory";

    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Lưu tài liệu dưới dạng PDF với phông chữ mặc định được chỉ định.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Bước 2: Lưu với phông chữ mặc định từ tệp

Tiếp theo, hãy lưu tài liệu bằng phông chữ mặc định được tải từ một tệp.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Đường dẫn đến thư mục tài liệu.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Lưu tài liệu dưới dạng PDF với phông chữ mặc định được tải từ tệp.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Bước 3: Lưu với phông chữ mặc định từ luồng

Cuối cùng, hãy lưu tài liệu bằng phông chữ mặc định được tải từ luồng.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Đường dẫn đến thư mục tài liệu.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Lưu tài liệu dưới dạng PDF với phông chữ mặc định được tải từ luồng.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã khám phá cách lưu tài liệu bằng các phông chữ được chỉ định trong Aspose.Note cho .NET. Bằng cách làm theo các bước này, bạn có thể tùy chỉnh cài đặt phông chữ theo yêu cầu của mình, đảm bảo tài liệu của bạn được định dạng như mong muốn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng bất kỳ phông chữ nào để lưu tài liệu trong Aspose.Note không?

A1: Có, bạn có thể chỉ định bất kỳ phông chữ nào để lưu tài liệu. Chỉ cần đảm bảo tệp phông chữ có thể truy cập được và tải chính xác.

### Câu hỏi 2: Aspose.Note có tương thích với các định dạng tài liệu khác nhau không?

Câu trả lời 2: Aspose.Note chủ yếu hoạt động với tài liệu OneNote nhưng cung cấp các tùy chọn để lưu ở nhiều định dạng khác nhau, bao gồm cả PDF.

### Câu hỏi 3: Làm cách nào để xử lý việc thiếu phông chữ khi lưu tài liệu?

Câu trả lời 3: Aspose.Note cung cấp các tùy chọn để sử dụng phông chữ mặc định trong trường hợp thiếu phông chữ được chỉ định, đảm bảo định dạng tài liệu nhất quán.

### Câu hỏi 4: Aspose.Note có hỗ trợ nhúng phông chữ vào tài liệu đầu ra không?

Câu trả lời 4: Có, Aspose.Note cho phép nhúng phông chữ để đảm bảo tính di động của tài liệu và hiển thị nhất quán trên các nền tảng khác nhau.

### Câu hỏi 5: Tôi có thể nhận thêm hỗ trợ với Aspose.Note ở đâu?

 Câu trả lời 5: Để được hỗ trợ thêm hoặc hỗ trợ kỹ thuật, bạn có thể truy cập[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28).