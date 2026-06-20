---
date: 2026-06-20
description: Tìm hiểu cách tạo tài liệu văn bản phong phú và tạo tệp OneNote một cách
  lập trình với Aspose.Note cho .NET. Hướng dẫn chi tiết từng bước kèm đoạn mã mẫu.
keywords:
- create rich text document
- create onenote file
- set paragraph style
- apply font color
- create document outline
linktitle: Tạo tài liệu văn bản phong phú với Aspose.Note cho .NET
schemas:
- author: Aspose
  dateModified: '2026-06-20'
  description: Learn how to create rich text documents and generate OneNote files
    programmatically with Aspose.Note for .NET. Step‑by‑step guide with code snippets.
  headline: Create Rich Text Document with Aspose.Note for .NET
  type: TechArticle
- description: Learn how to create rich text documents and generate OneNote files
    programmatically with Aspose.Note for .NET. Step‑by‑step guide with code snippets.
  name: Create Rich Text Document with Aspose.Note for .NET
  steps:
  - name: '**Development Environment** – Visual Studio 2022 or any compatible .NET
      IDE.'
    text: '**Development Environment** – Visual Studio 2022 or any compatible .NET
      IDE.'
  - name: '**Aspose.Note for .NET** – Download from the [download link](https://releases.aspose.com/note/net/).'
    text: '**Aspose.Note for .NET** – Download from the [download link](https://releases.aspose.com/note/net/).'
  - name: '**Basic C# Knowledge** – You should be comfortable with classes, objects,
      and inline code.'
    text: '**Basic C# Knowledge** – You should be comfortable with classes, objects,
      and inline code.'
  type: HowTo
- questions:
  - answer: Yes. By creating multiple `TextRun` objects with distinct `TextStyle`
      settings, you can mix bold, color, and size in a single paragraph.
    question: Can I apply different formatting styles within the same text string?
  - answer: Absolutely. The library processes multi‑hundred‑page OneNote files using
      a streaming model that keeps memory usage low.
    question: Is Aspose.Note suitable for handling large‑scale document processing
      tasks?
  - answer: Yes. Aspose.Note works seamlessly with ASP.NET Core, WPF, and any .NET
      Standard‑compatible library.
    question: Can I integrate Aspose.Note with other .NET libraries or frameworks?
  - answer: While the core API runs locally, you can host it in Azure Functions or
      AWS Lambda to build cloud‑enabled services.
    question: Does Aspose.Note provide support for cloud‑based document processing?
  - answer: You can explore the [Aspose.Note forum](https://forum.aspose.com/c/note/28)
      for community help and access documentation on the [website](https://reference.aspose.com/note/net/).
    question: Where can I find more resources and support for Aspose.Note?
  type: FAQPage
second_title: Aspose.Note .NET API
title: Tạo tài liệu văn bản phong phú với Aspose.Note cho .NET
url: /vi/net/loading-and-saving-operations/create-doc-with-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo tài liệu Rich Text với Aspose.Note cho .NET

## Giới thiệu  

Trong hướng dẫn này, bạn sẽ học **cách tạo một tài liệu rich text** bằng cách sử dụng Aspose.Note cho .NET và sau đó lưu nó dưới dạng tệp OneNote. Cho dù bạn cần tạo ghi chú cuộc họp, bản tóm tắt dự án, hoặc bất kỳ nội dung có định dạng nào một cách lập trình, Aspose.Note cung cấp cho bạn toàn quyền kiểm soát việc định dạng văn bản, kiểu đoạn văn và cấu trúc tài liệu. Chúng tôi sẽ hướng dẫn từng bước — từ việc nhập các namespace đến lưu tệp *.one* cuối cùng — để bạn có thể bắt đầu tự động tạo OneNote ngay hôm nay.

## Câu trả lời nhanh  

- **Aspose.Note làm gì?** Nó cho phép các nhà phát triển .NET tạo, đọc và chỉnh sửa tệp OneNote mà không cần ứng dụng OneNote.  
- **Có bao nhiêu tùy chọn định dạng được hỗ trợ?** Hơn 30 kiểu văn bản, bao gồm họ phông chữ, kích thước, màu sắc, in đậm, in nghiêng và gạch chân.  
- **Tôi có thể đặt kiểu đoạn văn bằng mã không?** Có – sử dụng lớp `ParagraphStyle` để xác định căn chỉnh, thụt lề và khoảng cách.  
- **Định dạng tệp được tạo là gì?** Một tệp *.one* tiêu chuẩn có thể mở trong Microsoft OneNote, OneNote Online và các ứng dụng di động.  
- **Tôi có cần giấy phép cho việc phát triển không?** Giấy phép tạm thời miễn phí hoạt động cho việc đánh giá; giấy phép đầy đủ cần thiết cho môi trường sản xuất.

## Tài liệu rich text là gì?  

Một **tài liệu rich text** là tệp lưu trữ văn bản cùng với thông tin định dạng như phông chữ, màu sắc và kiểu đoạn văn. Trong Aspose.Note, điều này được biểu diễn bằng lớp `RichText`, có thể được gắn vào tiêu đề, outline hoặc bất kỳ phần tử nào của trang.

## Tại sao tạo tệp OneNote với rich text?  

Việc tạo tệp OneNote với rich text cho phép bạn tạo ra các ghi chú được định dạng chuyên nghiệp và giữ nguyên kiểu dáng khi mở trong bất kỳ client OneNote nào. Điều này rất phù hợp cho việc báo cáo tự động, biên bản họp hoặc tài liệu giáo dục, nơi mà cấu trúc trực quan và nhấn mạnh cải thiện khả năng đọc. Khả năng của Aspose.Note trong việc tạo ra các tài liệu lớn, đa trang mà không cần tải toàn bộ vào bộ nhớ khiến nó thích hợp cho các giải pháp quy mô doanh nghiệp.

## Yêu cầu trước  

1. **Môi trường phát triển** – Visual Studio 2022 hoặc bất kỳ IDE .NET nào tương thích.  
2. **Aspose.Note cho .NET** – Tải xuống từ [liên kết tải xuống](https://releases.aspose.com/note/net/).  
3. **Kiến thức C# cơ bản** – Bạn nên quen thuộc với các lớp, đối tượng và mã nội tuyến.

## Cách nhập các namespace cần thiết?  

Tải các namespace cần thiết để trình biên dịch nhận diện các kiểu Aspose.Note. Việc nhập `System` và `System.Drawing` cung cấp chức năng .NET cơ bản, trong khi namespace Aspose.Note (được tham chiếu tự động sau khi thêm thư viện) cho phép truy cập các lớp tạo tài liệu như `Document`, `Page` và `RichText`. Bước này đảm bảo rằng mọi mã sau này biên dịch mà không gặp lỗi thiếu tham chiếu.  

```csharp
using Aspose.Note;
using Aspose.Note.Rendering;
using System.Drawing;
```

Bây giờ bạn đã có quyền truy cập vào `Document`, `Page`, `Title`, `RichText` và các lớp định dạng.  

```csharp
using System;
using System.Drawing;
```

## Cách tạo đối tượng Document?  

Khởi tạo lớp `Document` – đối tượng này đại diện cho toàn bộ tệp OneNote trong bộ nhớ. Lớp `Document` là container cấp cao nhất chứa các trang, outline và tài nguyên, cho phép bạn xây dựng cấu trúc sổ ghi chú hoàn chỉnh bằng mã.  

```csharp
Document oneNoteDoc = new Document();
```

```csharp
Document doc = new Document();
```

## Cách khởi tạo đối tượng Page?  

Thêm một `Page` vào tài liệu; mỗi trang tương ứng với một tab trong OneNote. Lớp `Page` mô hình hoá một trang OneNote duy nhất, bao gồm kích thước, nền và cấu trúc nội dung, cung cấp một canvas cho tiêu đề, outline và các yếu tố khác.  

```csharp
Page page = new Page(oneNoteDoc);
```

```csharp
Page page = new Page();
```

## Cách tạo đối tượng Title?  

`Title` chứa tiêu đề của trang và hiển thị ở đầu tab OneNote. `Title` là một container nhẹ cho một dòng rich text dùng làm tiêu đề của trang, giúp dễ dàng đặt tên rõ ràng, mô tả cho trang.  

```csharp
Title pageTitle = new Title();
```

```csharp
Title title = new Title();
```

## Cách đặt thuộc tính định dạng văn bản?  

Xác định một `ParagraphStyle` mặc định sẽ được áp dụng cho tất cả văn bản tiếp theo trừ khi được ghi đè. `ParagraphStyle` cho phép bạn đặt họ phông chữ, kích thước, màu sắc, căn chỉnh và khoảng cách ở một nơi, đảm bảo giao diện nhất quán trong toàn tài liệu đồng thời vẫn cho phép ghi đè riêng lẻ khi cần.  

```csharp
TextStyle defaultStyle = new TextStyle
{
    FontName = "Calibri",
    FontSize = 12,
    FontColor = Color.Black
};
```

```csharp
ParagraphStyle defaultTextStyle = new ParagraphStyle
{
    FontColor = Color.Black,
    FontName = "Arial",
    FontSize = 10
};
```

## Cách tạo RichText với định dạng cho tiêu đề?  

Tạo một đối tượng `RichText`, gán kiểu mặc định và sau đó áp dụng bất kỳ định dạng đặc biệt nào cho tiêu đề. `RichText` lưu trữ một tập hợp các đối tượng `TextRun`, mỗi đối tượng có thể có kiểu riêng, cho phép kiểm soát chi tiết về phông chữ, màu sắc và các thuộc tính khác trong một đoạn văn duy nhất.  

```csharp
RichText titleRichText = new RichText();
titleRichText.Add(new TextRun("Quarterly Report", new TextStyle
{
    FontSize = 24,
    FontColor = Color.DarkBlue,
    Bold = true
}));
```

```csharp
RichText titleText = new RichText() { ParagraphStyle = defaultTextStyle }.Append("Title!");
```

## Cách khởi tạo các đối tượng Outline và OutlineElement?  

`Outline` nhóm nội dung liên quan trên một trang, trong khi `OutlineElement` đại diện cho một mục bullet hoặc đánh số. Các lớp này cho phép bạn xây dựng cấu trúc phân cấp tương tự như khung điều hướng bên trái trong OneNote, mang lại cho người đọc cái nhìn rõ ràng, có tổ chức về các phần của ghi chú.  

```csharp
Outline outline = new Outline(oneNoteDoc);
OutlineElement outlineElement = new OutlineElement();
```

```csharp
Outline outline = new Outline()
{
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
```

## Cách định nghĩa các kiểu văn bản bổ sung?  

Tạo các thể hiện `ParagraphStyle` riêng biệt cho tiêu đề, tiêu đề phụ và các đoạn văn thông thường. Sử dụng các kiểu riêng biệt cho phép bạn **đặt kiểu đoạn văn** và **áp dụng màu phông chữ** một cách nhất quán trong toàn tài liệu, giúp dễ dàng duy trì cấu trúc trực quan và cải thiện khả năng đọc.  

```csharp
TextStyle headingStyle = new TextStyle
{
    FontSize = 18,
    FontColor = Color.DarkGreen,
    Bold = true
};

TextStyle paragraphStyle = new TextStyle
{
    FontSize = 12,
    FontColor = Color.Black
};
```

```csharp
TextStyle textStyleForHelloWord = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

// Define more text styles as needed
```

## Cách thêm văn bản đã định dạng vào đối tượng RichText?  

Thêm nhiều đối tượng `TextRun`, mỗi cái có kiểu riêng, để xây dựng một đoạn văn được định dạng phong phú. Bước này cho thấy cách **áp dụng màu phông chữ** và **đặt kiểu đoạn văn** cho các phần khác nhau của cùng một dòng, cho phép câu có kiểu hỗn hợp như tiêu đề in đậm tiếp theo là nhấn mạnh màu sắc.  

```csharp
RichText contentRichText = new RichText();
contentRichText.Add(new TextRun("Introduction: ", headingStyle));
contentRichText.Add(new TextRun("This report outlines the Q3 performance metrics.", paragraphStyle));
```

```csharp
RichText text = new RichText() { ParagraphStyle = defaultTextStyle }
    .Append("Hello", textStyleForHelloWord)
    .Append(" OneNote", textStyleForOneNoteWord)
    .Append(" text", textStyleForTextWord)
    .Append("!", TextStyle.Default);
```

## Cách thêm Title và RichText vào Outline?  

Gắn tiêu đề và nội dung vào `OutlineElement`, sau đó thêm nó vào `Outline`. `OutlineElement` có thể chứa cả tiêu đề và phần nội dung rich text, tạo thành một phần ghi chú hoàn chỉnh xuất hiện như một mục có thể thu gọn trong khung điều hướng của OneNote.  

```csharp
outlineElement.Title = pageTitle;
outlineElement.RichText = contentRichText;
outline.Add(outlineElement);
```

```csharp
title.TitleText = titleText;
outlineElem.AppendChildLast(text);
```

## Cách thêm Outline vào Page và Page vào Document?  

Chèn outline vào trang và sau đó thêm trang vào cấu trúc tài liệu. Điều này tạo ra cấu trúc cuối cùng mà OneNote sẽ hiển thị dưới dạng một trang có outline được định dạng, đảm bảo mọi yếu tố xuất hiện theo đúng thứ tự khi tệp được mở.  

```csharp
page.Add(outline);
oneNoteDoc.Add(page);
```

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Cách lưu Document dưới dạng tệp OneNote?  

Xác định đường dẫn đầu ra và gọi `Save`. Tệp sẽ có phần mở rộng *.one*, sẵn sàng mở trong OneNote. Việc lưu tạo ra một **tệp onenote** giữ nguyên tất cả kiểu dáng rich‑text và cấu trúc outline, giúp tài liệu có thể xem ngay trong bất kỳ client OneNote nào.  

```csharp
oneNoteDoc.Save("QuarterlyReport.one");
```

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithFormattedRichText_out.one";
doc.Save(dataDir);
```

## Các vấn đề thường gặp và giải pháp  

- **Thiếu phông chữ** – Đảm bảo phông chữ bạn chỉ định (ví dụ: Calibri) đã được cài đặt trên máy chủ; nếu không, Aspose.Note sẽ chuyển sang phông chữ mặc định.  
- **Tài liệu lớn** – Sử dụng `Document.SaveOptions` để bật streaming, giúp ngăn ngừa tiêu thụ bộ nhớ cao cho các tệp trên 200 trang.  
- **Căn chỉnh đoạn không được áp dụng** – Kiểm tra rằng bạn đã đặt `ParagraphStyle.Alignment` trên `TextStyle` trước khi thêm `TextRun`.

## Câu hỏi thường gặp  

**Q: Tôi có thể áp dụng các kiểu định dạng khác nhau trong cùng một chuỗi văn bản không?**  
A: Có. Bằng cách tạo nhiều đối tượng `TextRun` với các cài đặt `TextStyle` khác nhau, bạn có thể kết hợp in đậm, màu sắc và kích thước trong một đoạn văn duy nhất.  

**Q: Aspose.Note có phù hợp để xử lý các tác vụ xử lý tài liệu quy mô lớn không?**  
A: Hoàn toàn. Thư viện xử lý các tệp OneNote hàng trăm trang bằng mô hình streaming giúp giảm mức sử dụng bộ nhớ.  

**Q: Tôi có thể tích hợp Aspose.Note với các thư viện hoặc framework .NET khác không?**  
A: Có. Aspose.Note hoạt động liền mạch với ASP.NET Core, WPF và bất kỳ thư viện nào tương thích với .NET Standard.  

**Q: Aspose.Note có hỗ trợ xử lý tài liệu dựa trên đám mây không?**  
A: Mặc dù API cốt lõi chạy cục bộ, bạn có thể triển khai nó trong Azure Functions hoặc AWS Lambda để xây dựng các dịch vụ hỗ trợ đám mây.  

**Q: Tôi có thể tìm thêm tài nguyên và hỗ trợ cho Aspose.Note ở đâu?**  
A: Bạn có thể khám phá [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) để nhận trợ giúp cộng đồng và truy cập tài liệu trên [trang web](https://reference.aspose.com/note/net/).  

**Cập nhật lần cuối:** 2026-06-20  
**Kiểm thử với:** Aspose.Note 24.11 cho .NET  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Create Document with Page Title in Aspose.Note](/note/net/loading-and-saving-operations/create-doc-with-page-title/)
- [Save Document to OneNote Format in Aspose.Note](/note/net/loading-and-saving-operations/save-doc-to-onenote-format/)
- [Text Manipulation in OneNote with Aspose.Note for .NET](/note/net/text-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}