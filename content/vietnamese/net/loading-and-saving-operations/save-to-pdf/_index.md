---
title: Lưu vào PDF trong Aspose.Note
linktitle: Lưu vào PDF trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách lưu tài liệu Microsoft OneNote sang định dạng PDF bằng Aspose.Note for .NET. Hướng dẫn từng bước với các ví dụ về mã cho bố cục trang Letter và A4.
type: docs
weight: 26
url: /vi/net/loading-and-saving-operations/save-to-pdf/
---
## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ khám phá cách lưu tài liệu sang định dạng PDF bằng Aspose.Note cho .NET. Aspose.Note là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote theo chương trình. Chúng tôi sẽ đề cập đến các điều kiện tiên quyết, nhập vùng tên và cung cấp hướng dẫn từng bước để lưu tài liệu sang PDF ở nhiều bố cục trang khác nhau.

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu, hãy đảm bảo bạn có những điều sau:

- Visual Studio được cài đặt trên hệ thống của bạn.
-  Aspose.Note cho thư viện .NET được tải xuống và cài đặt. Bạn có thể tải nó xuống từ[đây](https://releases.aspose.com/note/net/).
- Kiến thức cơ bản về ngôn ngữ lập trình C#.

## Nhập không gian tên

Trước tiên, hãy nhập các không gian tên cần thiết vào mã C# của chúng ta:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Bây giờ chúng ta đã có các điều kiện tiên quyết và các không gian tên đã được nhập, hãy tiếp tục lưu tài liệu sang PDF ở các bố cục trang khác nhau.

## Bước 1: Lưu vào PDF bằng Cài đặt trang thư


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Đường dẫn đến thư mục tài liệu.
    string dataDir = "Your Document Directory";

    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    //Lưu tài liệu.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Giải trình:

- Chúng tôi tải tài liệu OneNote vào Aspose.Note.
- Xác định đường dẫn đích cho tệp PDF đã lưu.
-  Lưu tài liệu sang PDF bằng cách sử dụng`PdfSaveOptions` với`PageSettings` đặt thành`Letter`.

## Bước 2: Lưu sang PDF bằng cách sử dụng Cài đặt trang A4 không giới hạn chiều cao

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Đường dẫn đến thư mục tài liệu.
    string dataDir = "Your Document Directory";

    // Tải tài liệu vào Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    //Lưu tài liệu.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Giải trình:

- Tương tự như bước trước, chúng ta tải tài liệu OneNote vào Aspose.Note.
- Xác định đường dẫn đích cho tệp PDF đã lưu.
-  Lưu tài liệu sang PDF bằng cách sử dụng`PdfSaveOptions` với`PageSettings` đặt thành`A4NoHeightLimit`.

## Phần kết luận

Trong hướng dẫn này, chúng ta đã tìm hiểu cách lưu tài liệu sang định dạng PDF bằng Aspose.Note cho .NET. Chúng tôi đã đề cập đến hai bố cục trang khác nhau: Letter và A4 không giới hạn chiều cao. Với Aspose.Note, các nhà phát triển có thể dễ dàng thao tác với các tệp OneNote theo chương trình, mang lại sự linh hoạt và hiệu quả trong các tác vụ quản lý tài liệu.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.Note có thể xử lý các tệp OneNote phức tạp không?

Trả lời 1: Có, Aspose.Note hỗ trợ nhiều tính năng và chức năng khác nhau để xử lý các tệp OneNote phức tạp một cách hiệu quả.

### Câu hỏi 2: Aspose.Note có phù hợp với các dự án thương mại không?

 Câu trả lời 2: Hoàn toàn có thể, Aspose.Note có thể được sử dụng dễ dàng trong các dự án thương mại. Bạn có thể mua giấy phép[đây](https://purchase.aspose.com/buy).

### Câu 3: Aspose.Note có cung cấp bản dùng thử miễn phí không?

 Câu trả lời 3: Có, bạn có thể khám phá Aspose.Note với bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 4: Tôi có thể tìm tài liệu về Aspose.Note ở đâu?

 A4: Bạn có thể tìm tài liệu chi tiết[đây](https://reference.aspose.com/note/net/).

### Câu 5: Cần hỗ trợ thêm?

 Câu trả lời 5: Vui lòng đặt bất kỳ câu hỏi nào hoặc tìm kiếm sự hỗ trợ trên diễn đàn Aspose.Note[đây](https://forum.aspose.com/c/note/28).