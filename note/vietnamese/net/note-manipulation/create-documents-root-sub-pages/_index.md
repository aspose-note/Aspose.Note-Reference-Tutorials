---
title: Tạo tài liệu với trang gốc và trang phụ bằng Aspose.Note
linktitle: Tạo tài liệu với trang gốc và trang phụ bằng Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách sử dụng Aspose.Note cho .NET để tạo tài liệu OneNote động với cấu trúc phân cấp.
weight: 11
url: /vi/net/note-manipulation/create-documents-root-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo tài liệu với trang gốc và trang phụ bằng Aspose.Note

## Giới thiệu

Chào mừng bạn đến với hướng dẫn của chúng tôi về cách tạo tài liệu với trang gốc và trang phụ bằng Aspose.Note cho .NET! Aspose.Note là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote theo chương trình, cho phép tạo, thao tác và chuyển đổi tài liệu OneNote.

Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước quy trình tạo tài liệu OneNote với trang gốc và trang phụ. Chúng tôi sẽ cung cấp các giải thích chi tiết và đoạn mã bằng cách sử dụng Aspose.Note cho .NET, giúp bạn dễ dàng theo dõi và triển khai trong các dự án của riêng mình.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

1. Visual Studio: Bạn sẽ cần cài đặt Visual Studio trên hệ thống của mình để viết và biên dịch mã .NET.
2.  Aspose.Note for .NET: Tải xuống và cài đặt Aspose.Note for .NET từ[trang tải xuống](https://releases.aspose.com/note/net/).
3. Kiến thức C# cơ bản: Cần phải làm quen với ngôn ngữ lập trình C# để hiểu và triển khai các ví dụ mã.

Bây giờ bạn đã thiết lập xong mọi thứ, hãy đi sâu vào phần hướng dẫn!

## Nhập không gian tên

Đầu tiên, hãy nhập các không gian tên cần thiết vào dự án của chúng ta:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## Bước 1: Khởi tạo đối tượng tài liệu

```csharp
//Tạo một đối tượng của lớp Tài liệu
Document doc = new Document();
```

## Bước 2: Tạo trang gốc và trang phụ

```csharp
// Khởi tạo các đối tượng lớp Trang và đặt cấp độ của chúng
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### Đối với Trang 1:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### Đối với Trang 2:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### Đối với Trang 3:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## Bước 4: Thêm trang vào tài liệu

```csharp
// Thêm trang vào Tài liệu OneNote
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## Bước 5: Lưu tài liệu

```csharp
// Lưu tài liệu OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách tạo tài liệu với trang gốc và trang phụ bằng Aspose.Note cho .NET. Giờ đây, bạn có thể sử dụng kiến thức này để tạo động các tài liệu OneNote phức tạp trong ứng dụng của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.Note có thể xử lý các tài liệu OneNote lớn không?

Trả lời 1: Có, Aspose.Note được thiết kế để xử lý hiệu quả các tài liệu OneNote lớn mà không ảnh hưởng đến hiệu suất.

### Câu 2: Aspose.Note có tương thích với .NET Core không?

Câu trả lời 2: Có, Aspose.Note hỗ trợ .NET Core cùng với .NET Framework truyền thống.

### Câu hỏi 3: Tôi có thể chuyển đổi tài liệu OneNote sang các định dạng khác bằng Aspose.Note không?

Câu trả lời 3: Hoàn toàn có thể, Aspose.Note cung cấp khả năng chuyển đổi sang nhiều định dạng khác nhau bao gồm PDF, DOCX, HTML, v.v.

### Câu hỏi 4: Aspose.Note có cung cấp tích hợp đám mây không?

Câu trả lời 4: Aspose.Note chủ yếu tập trung vào phát triển tại chỗ, nhưng bạn có thể sử dụng nó trong môi trường đám mây với thiết lập phù hợp.

### Câu hỏi 5: Aspose.Note có hỗ trợ kỹ thuật không?

Câu trả lời 5: Có, Aspose cung cấp hỗ trợ kỹ thuật chuyên dụng thông qua diễn đàn của họ, nơi bạn có thể đặt câu hỏi và nhận trợ giúp.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
