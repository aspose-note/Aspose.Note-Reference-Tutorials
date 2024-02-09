---
title: Thêm nút văn bản có thẻ trong Aspose.Note
linktitle: Thêm nút văn bản có thẻ trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách thêm nút văn bản có thẻ vào tài liệu OneNote bằng Aspose.Note for .NET.
type: docs
weight: 12
url: /vi/net/tag-management/add-text-node-tag/
---
## Giới thiệu

Aspose.Note for .NET là một thư viện mạnh mẽ cho phép các nhà phát triển tạo, thao tác và chuyển đổi các tệp Microsoft OneNote theo chương trình bằng cách sử dụng .NET framework. Trong hướng dẫn này, chúng ta sẽ khám phá cách thêm nút văn bản có thẻ vào tài liệu OneNote bằng Aspose.Note cho .NET.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

1. Visual Studio: Đảm bảo rằng bạn đã cài đặt Visual Studio trên hệ thống của mình.
2.  Aspose.Note for .NET: Tải xuống và cài đặt Aspose.Note for .NET từ[trang mạng](https://releases.aspose.com/note/net/).
3. Kiến thức cơ bản về C#: Làm quen với các nguyên tắc cơ bản của ngôn ngữ lập trình C#.

## Nhập không gian tên

Trước tiên, bạn cần nhập các không gian tên cần thiết để truy cập các lớp và phương thức cần thiết để làm việc với Aspose.Note cho .NET.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Bước 1: Tạo đối tượng tài liệu

Khởi tạo đối tượng Tài liệu để bắt đầu làm việc với tài liệu OneNote.

```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## Bước 2: Khởi tạo các đối tượng trang và phác thảo

Tạo các đối tượng Trang và Dàn bài để cấu trúc nội dung của tài liệu OneNote.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## Bước 3: Thêm nút văn bản bằng thẻ

Tạo một đối tượng RichText với văn bản và kiểu mong muốn, sau đó thêm nó vào OutlineElement.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## Bước 4: Nối phần tử phác thảo và nút trang

Nối phần tử Outline vào Outline, sau đó nối Outline vào Trang. Cuối cùng, nối Trang vào Tài liệu.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Bước 5: Lưu tài liệu

Lưu tài liệu OneNote đã sửa đổi vào một vị trí được chỉ định.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách thêm nút văn bản có thẻ vào tài liệu OneNote bằng Aspose.Note cho .NET. Với kiến thức này, giờ đây bạn có thể tùy chỉnh và nâng cao các tệp OneNote của mình theo chương trình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể thêm nhiều nút văn bản với các thẻ khác nhau trong cùng một tài liệu không?

Câu trả lời 1: Có, bạn có thể thêm nhiều nút văn bản với các thẻ khác nhau bằng cách thực hiện theo cùng một quy trình cho mỗi nút.

### Câu hỏi 2: Aspose.Note for .NET có tương thích với tất cả các phiên bản OneNote không?

Câu trả lời 2: Aspose.Note for .NET hỗ trợ nhiều phiên bản OneNote khác nhau, bao gồm 2010, 2013, 2016 trở lên.

### Câu 3: Tôi có thể tùy chỉnh màu sắc và kiểu dáng của thẻ không?

A3: Có, bạn có thể tùy chỉnh màu sắc và kiểu dáng thẻ theo yêu cầu của bạn.

### Câu hỏi 4: Aspose.Note dành cho .NET có hỗ trợ mã hóa tài liệu không?

Câu trả lời 4: Có, Aspose.Note for .NET hỗ trợ mã hóa tài liệu để đảm bảo bảo mật dữ liệu.

### Câu hỏi 5: Tôi có thể tìm thêm tài nguyên và hỗ trợ cho Aspose.Note cho .NET ở đâu?

 A5: Bạn có thể khám phá[Aspose.Note dành cho tài liệu .NET](https://reference.aspose.com/note/net/) và tìm kiếm sự giúp đỡ từ[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28).