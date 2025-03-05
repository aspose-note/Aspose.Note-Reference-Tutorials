---
title: Thêm nút bảng có thẻ trong Aspose.Note
linktitle: Thêm nút bảng có thẻ trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách thêm bảng có thẻ trong Aspose.Note cho .NET. Nâng cao kỹ năng thao tác tài liệu của bạn theo chương trình.
type: docs
weight: 11
url: /vi/net/tag-management/add-table-node-tag/
---
## Giới thiệu

Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình thêm nút bảng bằng thẻ bằng Aspose.Note cho .NET. Thực hiện theo các bước dưới đây để đạt được điều này.

## Nhập không gian tên

Trước khi bắt đầu, hãy đảm bảo nhập các không gian tên cần thiết để hoạt động với Aspose.Lưu ý:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Điều kiện tiên quyết

Đảm bảo bạn đã thiết lập các điều kiện tiên quyết sau trước khi tiếp tục:

1.  Cài đặt: Tải xuống và cài đặt thư viện Aspose.Note for .NET từ[đây](https://releases.aspose.com/note/net/).
2.  Giấy phép: Có được giấy phép hoặc sử dụng một[giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để sử dụng thư viện.
3. Môi trường phát triển: Thiết lập môi trường phát triển tương thích, chẳng hạn như Visual Studio.

## Bước 1: Khởi tạo đối tượng tài liệu và trang

 Bắt đầu bằng cách tạo một thể hiện của`Document` lớp và khởi tạo một`Page` sự vật:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Bước 2: Tạo đối tượng bảng, hàng và ô

 Khởi tạo`Table`, `TableRow` , Và`TableCell` các đối tượng:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Bước 3: Chèn nội dung vào ô

 Thêm nội dung vào ô bằng cách sử dụng`AppendChildLast` phương pháp:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Bước 4: Khởi tạo nút bảng

 Khởi tạo`Table` đối tượng có thuộc tính được chỉ định:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Bước 5: Thêm hàng vào bảng

Thêm nút hàng vào bảng:

```csharp
table.AppendChildLast(row);
```

## Bước 6: Thêm thẻ vào nút bảng

Bao gồm một thẻ cho nút bảng:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Bước 7: Thêm nút bảng vào phần tử phác thảo

 Tạo ra một`Outline` Và`OutlineElement` để thêm nút bảng:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Bước 8: Lưu tài liệu

Lưu tài liệu OneNote:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Sau khi làm theo các bước này, bạn đã thêm thành công nút bảng có thẻ bằng Aspose.Note for .NET.

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã trình bày quy trình thêm nút bảng bằng thẻ trong Aspose.Note cho .NET. Bằng cách làm theo các bước này, bạn có thể thao tác hiệu quả với tài liệu OneNote theo chương trình, nâng cao khả năng quản lý tài liệu của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.Note có tương thích với tất cả các phiên bản .NET không?

Câu trả lời 1: Aspose.Note for .NET hỗ trợ .NET Framework phiên bản 2.0 trở lên, bao gồm .NET Core và .NET Standard.

### Câu hỏi 2: Tôi có thể dùng thử Aspose.Note trước khi mua giấy phép không?

 Câu trả lời 2: Có, bạn có thể nhận bản dùng thử miễn phí Aspose.Note từ[đây](https://releases.aspose.com/).

### Câu hỏi 3: Làm cách nào để có được giấy phép tạm thời cho Aspose.Note?

 A3: Bạn có thể nhận được giấy phép tạm thời từ[liên kết này](https://purchase.aspose.com/temporary-license/), có giá trị trong 30 ngày.

### Câu hỏi 4: Aspose.Note có hỗ trợ mã hóa tài liệu không?

Trả lời4: Có, Aspose.Note cung cấp hỗ trợ mã hóa tài liệu OneNote để đảm bảo bảo mật dữ liệu.

### Câu hỏi 5: Người dùng Aspose.Note có được hỗ trợ kỹ thuật không?

 Câu trả lời 5: Có, hỗ trợ kỹ thuật được cung cấp qua diễn đàn Aspose[đây](https://forum.aspose.com/c/note/28), nơi bạn có thể tìm kiếm sự trợ giúp từ các chuyên gia.