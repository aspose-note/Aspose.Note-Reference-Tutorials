---
title: Áp dụng đánh số trên văn bản trong Aspose.Note
linktitle: Áp dụng đánh số trên văn bản trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách áp dụng đánh số văn bản trong Aspose.Note cho .NET với hướng dẫn toàn diện này. Nâng cao định dạng tài liệu của bạn một cách dễ dàng.
weight: 12
url: /vi/net/text-manipulation/apply-numbering-on-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Áp dụng đánh số trên văn bản trong Aspose.Note

## Giới thiệu
Aspose.Note for .NET cung cấp các công cụ mạnh mẽ để thao tác tài liệu trong các ứng dụng C#. Trong hướng dẫn này, chúng ta sẽ khám phá quy trình áp dụng đánh số trên văn bản bằng Aspose.Note. Hãy làm theo các hướng dẫn từng bước này để cải thiện định dạng tài liệu của bạn một cách dễ dàng.
## Điều kiện tiên quyết
Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:
- Hiểu biết cơ bản về ngôn ngữ lập trình C#.
-  Aspose.Note cho .NET đã được cài đặt. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/note/net/).
- Một môi trường phát triển tích hợp (IDE) như Visual Studio.
## Nhập không gian tên
Để bắt đầu, hãy đảm bảo nhập các vùng tên cần thiết trong dự án C# của bạn:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Bước 1: Thiết lập tài liệu của bạn
Bắt đầu bằng cách tạo một tài liệu mới và khởi tạo các đối tượng cần thiết:
```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "Your Document Directory";
//Tạo một đối tượng của lớp Tài liệu
Document doc = new Document();
// Khởi tạo đối tượng lớp Trang
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Khởi tạo đối tượng lớp Outline
Outline outline = new Outline(doc);
```
## Bước 2: Xác định kiểu mặc định
Thiết lập kiểu dáng mặc định cho văn bản của bạn bằng lớp ParagraphStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Bước 3: Áp dụng đánh số
Khởi tạo các đối tượng lớp OutlineElement và áp dụng đánh số cho từng phần tử:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Bước 4: Thêm các phần tử phác thảo
Nối các phần tử phác thảo vào phác thảo:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Bước 5: Lưu tài liệu
Lưu tài liệu OneNote với cách đánh số được áp dụng:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Phần kết luận
Chúc mừng! Bạn đã học thành công cách áp dụng đánh số trên văn bản trong Aspose.Note for .NET. Thử nghiệm với các tùy chọn định dạng khác nhau để dễ dàng tạo ra các tài liệu hấp dẫn về mặt hình ảnh.
## Câu hỏi thường gặp
### 1. Tôi có thể tùy chỉnh định dạng đánh số không?
Có, lớp NumberList cho phép bạn tùy chỉnh định dạng đánh số theo sở thích của mình.
### 2. Có sẵn các tùy chọn định dạng khác không?
Aspose.Note cung cấp nhiều tùy chọn định dạng, bao gồm kiểu phông chữ, màu sắc, v.v.
### 3. Aspose.Note có tương thích với Visual Studio không?
Tuyệt đối! Aspose.Note tích hợp liền mạch với Visual Studio để mang lại trải nghiệm phát triển mượt mà.
### 4. Tôi có thể dùng thử Aspose.Note trước khi mua không?
 Chắc chắn! Bạn có thể khám phá bản dùng thử miễn phí[đây](https://releases.aspose.com/).
### 5. Tôi có thể nhận hỗ trợ cho Aspose.Note ở đâu?
 Đối với bất kỳ sự trợ giúp hoặc thắc mắc nào, hãy truy cập[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
