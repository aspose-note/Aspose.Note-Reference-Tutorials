---
title: Tải tài liệu OneNote trong Aspose.Note
linktitle: Tải tài liệu OneNote trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách tải, mã hóa và giải mã tài liệu OneNote theo lập trình trong .NET bằng Aspose.Note.
type: docs
weight: 16
url: /vi/net/loading-and-saving-operations/load-onenote-document/
---
## Giới thiệu

Aspose.Note for .NET là một API mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote theo chương trình trong các ứng dụng .NET của họ. Cho dù bạn cần tải, thao tác hay chuyển đổi tài liệu OneNote, Aspose.Note for .NET đều cung cấp chức năng toàn diện để hợp lý hóa quy trình làm việc của bạn.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

1. Visual Studio: Cài đặt Visual Studio, môi trường phát triển tích hợp (IDE) toàn diện để phát triển .NET.
2.  Aspose.Note for .NET: Tải xuống và cài đặt Aspose.Note for .NET từ[trang tải xuống](https://releases.aspose.com/note/net/).
3. Kiến thức C# cơ bản: Cần phải làm quen với các nguyên tắc cơ bản của ngôn ngữ lập trình C# để hiểu và triển khai các ví dụ được cung cấp trong hướng dẫn này.

## Nhập không gian tên

Trước khi bạn bắt đầu làm việc với Aspose.Note cho .NET, hãy đảm bảo nhập các vùng tên được yêu cầu vào dự án C# của bạn:

```csharp
using System;
using System.IO;
```

Hãy chia mỗi ví dụ thành nhiều bước:

## Tải tài liệu OneNote trong Aspose.Note

### Bước 1: Tải sổ ghi chép đơn giản:
   -  Bắt đầu bằng cách tạo một phiên bản mới của`Notebook` class, chuyển đường dẫn đến tài liệu OneNote.
   - Lặp lại qua các nút con của sổ ghi chép bằng vòng lặp foreach.
   - Hiển thị tên hiển thị của từng nút con.
   - Thực hiện các hành động cụ thể dựa trên việc nút con là tài liệu hay sổ ghi chép khác.

```csharp
public static void SimpleLoadNotebook()
{
    // Đường dẫn đến thư mục tài liệu.
    string dataDir = "Your Document Directory";
    string fileName = "Open Notebook.onetoc2";
    try
    {
        var notebook = new Notebook(Path.Combine(dataDir, fileName));
        foreach (var notebookChildNode in notebook)
        {
            Console.WriteLine(notebookChildNode.DisplayName);
            if (notebookChildNode is Document)
            {
                // Làm điều gì đó với tài liệu con
            }
            else if (notebookChildNode is Notebook)
            {
                // Làm điều gì đó với sổ tay con
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}
```

### Bước 2: Kiểm tra xem tài liệu đã được mã hóa chưa và tải:
   - Kiểm tra xem tài liệu OneNote có được mã hóa hay không bằng cách gọi`Document.IsEncrypted` phương thức, truyền tên tệp.
   - Nếu chưa được mã hóa, hãy tiến hành xử lý tài liệu.
   - Nếu được mã hóa, hãy nhắc người dùng cung cấp mật khẩu để giải mã.

```csharp
public static void Document_CheckIfEncryptedAndLoad()
{
    // Đường dẫn đến thư mục tài liệu.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (!Document.IsEncrypted(fileName, out document))
    {
        Console.WriteLine("The document is loaded and ready to be processed.");
    }
    else
    {
        Console.WriteLine("The document is encrypted. Provide a password.");
    }
}
```

### Bước 3: Kiểm tra xem tài liệu có được mã hóa bằng mật khẩu và tải hay không:
   - Tương tự như bước trước, kiểm tra xem tài liệu có được mã hóa bằng mật khẩu cụ thể hay không.
   - Nếu được mã hóa và cung cấp mật khẩu chính xác, hãy tiến hành xử lý tài liệu.
   - Nếu được mã hóa nhưng mật khẩu không chính xác được cung cấp, hãy nhắc người dùng về mật khẩu không hợp lệ.

```csharp
public static void Document_CheckIfEncryptedByPasswordAndLoad()
{
    // Đường dẫn đến thư mục tài liệu.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (Document.IsEncrypted(fileName, "VerySecretPassword", out document))
    {
        if (document != null)
        {
            Console.WriteLine("The document is decrypted. It is loaded and ready to be processed.");
        }
        else
        {
            Console.WriteLine("The document is encrypted. Invalid password was provided.");
        }
    }
    else
    {
        Console.WriteLine("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
}
```

### Bước 4: Xử lý định dạng OneNote 2007 không được hỗ trợ:
   - Cố gắng tải tài liệu OneNote ở định dạng 2007.
   -  Nếu định dạng không được hỗ trợ, hãy bắt`UnsupportedFileFormatException` và xử lý phù hợp, thông báo cho người dùng về định dạng không được hỗ trợ.

```csharp
public static void Document_OneNote2007_Is_NotSupported()
{
    // Đường dẫn đến thư mục tài liệu.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "OneNote2007.one");

    try
    {
        new Document(fileName);
    }
    catch (UnsupportedFileFormatException e)
    {
        if (e.FileFormat == FileFormat.OneNote2007)
        {
            Console.WriteLine("It looks like the provided file is in OneNote 2007 format that is not supported.");
        }
        else
            throw;
    }
}
```

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã khám phá cách tải tài liệu OneNote trong Aspose.Note cho .NET bằng nhiều phương pháp khác nhau. Bằng cách làm theo các hướng dẫn từng bước này, bạn có thể tích hợp liền mạch các khả năng xử lý tài liệu OneNote vào các ứng dụng .NET của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.Note for .NET có tương thích với tất cả các phiên bản Microsoft OneNote không?

Trả lời 1: Aspose.Note for .NET hỗ trợ nhiều phiên bản OneNote khác nhau. Tuy nhiên, có thể có những hạn chế với các định dạng cũ hơn như OneNote 2007.

### Câu hỏi 2: Tôi có thể mã hóa và giải mã tài liệu OneNote theo chương trình bằng Aspose.Note cho .NET không?

Câu trả lời 2: Có, bạn có thể kiểm tra xem tài liệu có được mã hóa hay không và giải mã nó bằng Aspose.Note for .NET.

### Câu hỏi 3: Tôi có thể tìm thêm tài nguyên và hỗ trợ cho Aspose.Note cho .NET ở đâu?

 A3: Bạn có thể ghé thăm[Aspose.Note dành cho tài liệu .NET](https://reference.aspose.com/note/net/) để có hướng dẫn và ví dụ toàn diện. Ngoài ra, bạn có thể tìm kiếm sự trợ giúp từ[Aspose.Note dành cho diễn đàn .NET](https://forum.aspose.com/c/note/28).

### Câu hỏi 4: Có bản dùng thử miễn phí dành cho Aspose.Note dành cho .NET không?

 Đ4: Có, bạn có thể tải xuống bản dùng thử miễn phí từ[trang web giả định](https://releases.aspose.com/).

### Câu hỏi 5: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.Note cho .NET?

 Câu trả lời 5: Bạn có thể yêu cầu giấy phép tạm thời từ[Trang mua hàng](https://purchase.aspose.com/temporary-license/).