---
title: Chuyển đổi Notebook sang PDF bằng các tùy chọn trong Aspose Note .NET
linktitle: Chuyển đổi Notebook sang PDF bằng các tùy chọn trong Aspose Note .NET
second_title: Aspose.Note .NET API
description: Tìm hiểu cách chuyển đổi sổ ghi chép Microsoft OneNote sang định dạng PDF bằng thư viện Aspose.Note for .NET với các tùy chọn có thể tùy chỉnh.
weight: 16
url: /vi/net/notebook-operations/convert-to-pdf-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi Notebook sang PDF bằng các tùy chọn trong Aspose Note .NET

## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ tìm hiểu quy trình chuyển đổi sổ ghi chép sang định dạng PDF bằng thư viện Aspose.Note cho .NET. Aspose.Note for .NET cung cấp một bộ tính năng mạnh mẽ để hoạt động với các tệp Microsoft OneNote theo chương trình.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

### 1. Aspose.Note cho Thư viện .NET
 Đảm bảo bạn đã tải xuống và cài đặt thư viện Aspose.Note for .NET. Bạn có thể tải nó xuống từ[trang mạng](https://releases.aspose.com/note/net/).

### 2. Môi trường phát triển
Bạn nên thiết lập một môi trường phát triển, chẳng hạn như Visual Studio, với cài đặt .NET framework cần thiết.

## Nhập không gian tên

Trước khi chúng tôi bắt đầu sử dụng Aspose.Note cho .NET trong dự án của mình, hãy nhập các không gian tên được yêu cầu:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Bây giờ, hãy chia nhỏ quá trình chuyển đổi sổ ghi chép sang PDF với các tùy chọn thành nhiều bước:

## Bước 1: Tải Notebook

Trước tiên, chúng ta cần tải sổ ghi chép OneNote mà chúng ta muốn chuyển đổi thành tệp PDF.

```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "Your Document Directory";

// Tải sổ tay OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Bước 2: Chỉ định tùy chọn lưu PDF

Tiếp theo, chúng tôi sẽ chỉ định các tùy chọn để lưu sổ ghi chép dưới dạng tệp PDF. Chúng tôi có thể tùy chỉnh các cài đặt khác nhau như thuật toán chia trang, lề và kích thước trang.

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## Bước 3: Lưu Notebook dưới dạng PDF

Bây giờ, chúng tôi sẽ lưu sổ ghi chép dưới dạng tệp PDF bằng các tùy chọn đã chỉ định.

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// Lưu sổ tay
notebook.Save(dataDir, notebookSaveOptions);
```

## Bước 4: Xác minh chuyển đổi

Cuối cùng, hãy xác minh rằng quá trình chuyển đổi đã thành công và in vị trí lưu tệp PDF.

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## Phần kết luận

Trong hướng dẫn này, chúng ta đã tìm hiểu cách chuyển đổi sổ ghi chép OneNote sang định dạng PDF bằng thư viện Aspose.Note for .NET. Bằng cách làm theo các bước được nêu ở trên, bạn có thể dễ dàng tích hợp chức năng này vào các ứng dụng .NET của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.Note for .NET có tương thích với tất cả các phiên bản Microsoft OneNote không?

Trả lời 1: Có, Aspose.Note for .NET hỗ trợ nhiều phiên bản khác nhau của Microsoft OneNote, bao gồm các định dạng .one và .onetoc2.

### Câu hỏi 2: Tôi có thể tùy chỉnh giao diện của đầu ra PDF không?

Câu trả lời 2: Có, bạn có thể chỉ định nhiều tùy chọn khác nhau như kích thước trang, lề và thuật toán chia trang để tùy chỉnh hình thức của đầu ra PDF.

### Câu hỏi 3: Aspose.Note for .NET có hỗ trợ các định dạng tệp khác không?

Câu trả lời 3: Có, Aspose.Note for .NET hỗ trợ chuyển đổi sang nhiều định dạng khác như hình ảnh, HTML và tài liệu Microsoft Word.

### Câu hỏi 4: Có bản dùng thử miễn phí dành cho Aspose.Note dành cho .NET không?

Câu trả lời 4: Có, bạn có thể tải xuống bản dùng thử miễn phí Aspose.Note dành cho .NET từ trang web để đánh giá các tính năng của nó trước khi mua hàng.

### Câu hỏi 5: Làm cách nào tôi có thể nhận được hỗ trợ kỹ thuật cho Aspose.Note dành cho .NET?

 Câu trả lời 5: Bạn có thể nhận hỗ trợ kỹ thuật cho Aspose.Note dành cho .NET bằng cách truy cập[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) hoặc liên hệ trực tiếp với nhóm hỗ trợ Aspose.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
