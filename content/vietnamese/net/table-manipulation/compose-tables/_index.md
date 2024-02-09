---
title: Soạn bảng với Aspose.Note
linktitle: Soạn bảng với Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách soạn các bảng có cấu trúc với nội dung văn bản đa dạng thức bằng Aspose.Note for .NET. Tăng cường tổ chức tài liệu và khả năng đọc dễ dàng.
type: docs
weight: 11
url: /vi/net/table-manipulation/compose-tables/
---
## Giới thiệu

Bảng là thành phần cơ bản của tài liệu, cho phép trình bày thông tin có cấu trúc. Aspose.Note for .NET cung cấp các công cụ mạnh mẽ để soạn bảng một cách dễ dàng. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình tạo bảng có nội dung văn bản đa dạng thức bằng Aspose.Note.

## Điều kiện tiên quyết

Trước khi đi sâu vào thành phần bảng với Aspose.Note dành cho .NET, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

1. Thiết lập môi trường: Đảm bảo bạn đã thiết lập môi trường phát triển phù hợp với .NET Framework hoặc .NET Core.
2.  Cài đặt: Tải xuống và cài đặt Aspose.Note cho .NET từ[trang mạng](https://releases.aspose.com/note/net/).
3. Kiến thức cơ bản: Làm quen với các khái niệm cơ bản về lập trình C# và thao tác tài liệu.

## Nhập không gian tên

Trước khi bắt đầu soạn bảng, hãy đảm bảo bạn nhập các không gian tên cần thiết:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Hãy chia nhỏ ví dụ được cung cấp thành các bước có thể quản lý được:

## Bước 1: Thiết lập thư mục tài liệu

Trước khi soạn bảng, hãy xác định thư mục nơi tài liệu sẽ được lưu.

```csharp
string dataDir = "Your Document Directory";
```

## Bước 2: Tạo văn bản tiêu đề

Xác định văn bản tiêu đề với các kiểu cụ thể như cỡ chữ và độ đậm.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Bước 3: Tạo trang và dàn ý

Khởi tạo một trang và một dàn ý để cấu trúc nội dung.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Bước 4: Thêm văn bản tóm tắt

Bao gồm một văn bản tóm tắt trước bảng.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Bước 5: Tạo bảng

Khởi tạo một bảng để sắp xếp dữ liệu theo hàng và cột.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Bước 6: Thêm hàng tiêu đề

Điền vào bảng một hàng tiêu đề chứa tiêu đề cột.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Bước 7: Thêm hàng trống

Chèn các hàng trống để chuẩn bị chèn dữ liệu.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Bước 8: Thêm thông tin liên hệ

Điền vào cột 'Danh bạ' bằng nội dung mẫu.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Bước 9: Lưu tài liệu

Lưu tài liệu bảng đã soạn.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Bước 10: Xác nhận

Xác nhận thành phần tài liệu thành công.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Phần kết luận

Trong hướng dẫn này, chúng ta đã khám phá cách soạn bảng có nội dung văn bản đa dạng thức bằng Aspose.Note cho .NET. Bằng cách làm theo các hướng dẫn từng bước này, bạn có thể tạo các bảng có cấu trúc trong tài liệu của mình một cách hiệu quả, nâng cao khả năng đọc và tổ chức.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tùy chỉnh kiểu dáng của các thành phần bảng không?
   
Trả lời 1: Có, bạn có thể tùy chỉnh nhiều khía cạnh khác nhau như kích thước phông chữ, màu sắc và căn chỉnh để phù hợp với yêu cầu của bạn.

### Câu hỏi 2: Aspose.Note có tương thích với các thư viện .NET khác không?
   
Câu trả lời 2: Aspose.Note tích hợp liền mạch với các thư viện .NET khác, mang đến sự linh hoạt sâu rộng trong thao tác tài liệu.

### Câu hỏi 3: Aspose.Note có hỗ trợ xuất bảng sang các định dạng khác nhau không?
   
Câu trả lời 3: Hoàn toàn có thể, Aspose.Note cho phép bạn xuất bảng sang nhiều định dạng khác nhau bao gồm PDF, DOCX và HTML.

### Câu hỏi 4: Tôi có thể tự động điền dữ liệu từ các nguồn bên ngoài vào bảng không?
   
Câu trả lời 4: Có, bạn có thể tự động điền bảng bằng cách tìm nạp dữ liệu từ cơ sở dữ liệu, API hoặc thông tin đầu vào của người dùng.

### Câu hỏi 5: Người dùng Aspose.Note có được hỗ trợ kỹ thuật không?
   
Câu trả lời 5: Có, Aspose cung cấp hỗ trợ kỹ thuật toàn diện thông qua các diễn đàn và các kênh hỗ trợ riêng của họ.