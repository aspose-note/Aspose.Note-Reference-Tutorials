---
title: Khám phá các bản sửa đổi trang trong tài liệu Aspose.Note
linktitle: Khám phá các bản sửa đổi trang trong tài liệu Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách khám phá các bản sửa đổi trang trong tài liệu Aspose.Note bằng .NET framework với hướng dẫn từng bước.
weight: 14
url: /vi/net/note-manipulation/page-revisions-exploration/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Khám phá các bản sửa đổi trang trong tài liệu Aspose.Note

## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ đi sâu vào khám phá các bản sửa đổi trang trong tài liệu Aspose.Note bằng cách sử dụng .NET framework. Aspose.Note là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote theo chương trình, cung cấp nhiều tính năng khác nhau để thao tác và trích xuất dữ liệu từ các tệp này.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn đã thiết lập các điều kiện tiên quyết sau:

### 1. Tải xuống và cài đặt Aspose.Note cho .NET

 Tham quan[trang tải xuống](https://releases.aspose.com/note/net/) và tải xuống thư viện Aspose.Note cho .NET. Làm theo hướng dẫn cài đặt được cung cấp để thiết lập thư viện trong môi trường phát triển của bạn.

### 2. Tải các không gian tên cần thiết

Đảm bảo nhập các không gian tên cần thiết trong dự án .NET của bạn để truy cập liền mạch các chức năng Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

Bây giờ, hãy chia nhỏ quá trình khám phá các bản sửa đổi trang thành các hướng dẫn từng bước:

## Bước 1: Tải tài liệu

Đầu tiên chúng ta cần tải tài liệu Aspose.Note, đảm bảo cho phép tải lịch sử tài liệu.

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## Bước 2: Truy xuất các bản sửa đổi trang

Sau khi tài liệu được tải, chúng tôi có thể truy xuất các bản sửa đổi cho một trang cụ thể. Trong ví dụ này, chúng tôi sẽ nhận được các bản sửa đổi cho trang đầu tiên.

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## Bước 3: Lặp lại các bản sửa đổi

Trong vòng lặp, lặp qua từng bản sửa đổi của trang và truy cập các thuộc tính của nó như thời gian sửa đổi lần cuối, thời gian tạo, tiêu đề, cấp độ và tác giả.

## Phần kết luận

Khám phá các bản sửa đổi trang trong tài liệu Aspose.Note bằng .NET là một quá trình đơn giản. Bằng cách làm theo các bước được nêu trong hướng dẫn này, bạn có thể truy xuất và phân tích lịch sử sửa đổi của các tệp OneNote một cách hiệu quả theo chương trình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.Note for .NET để tạo tài liệu OneNote mới không?

Câu trả lời 1: Có, Aspose.Note for .NET cho phép bạn tạo, chỉnh sửa và thao tác với tài liệu OneNote theo chương trình.

### Câu hỏi 2: Aspose.Note có hỗ trợ tải lịch sử cho tất cả các loại tệp OneNote không?

Câu trả lời 2: Aspose.Note hỗ trợ lịch sử tải cho cả định dạng tệp .one và .onepkg.

### Câu hỏi 3: Có bản dùng thử miễn phí dành cho Aspose.Note dành cho .NET không?

Câu trả lời 3: Có, bạn có thể tải xuống bản dùng thử miễn phí Aspose.Note cho .NET từ[đây](https://releases.aspose.com/).

### Câu hỏi 4: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.Note cho .NET?

 A4: Bạn có thể yêu cầu giấy phép tạm thời từ[liên kết này](https://purchase.aspose.com/temporary-license/).

### Câu hỏi 5: Tôi có thể tìm hỗ trợ cho Aspose.Note cho .NET ở đâu?

 Câu trả lời 5: Bạn có thể tìm thấy sự hỗ trợ và tài nguyên trên[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
