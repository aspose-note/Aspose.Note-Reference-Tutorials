---
title: Áp dụng dấu đầu dòng trên văn bản trong Aspose.Note
linktitle: Áp dụng dấu đầu dòng trên văn bản trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách áp dụng dấu đầu dòng trên văn bản trong Aspose.Note for .NET để cải thiện tài liệu OneNote của bạn. Hãy làm theo hướng dẫn từng bước này để định dạng hiệu quả.
type: docs
weight: 10
url: /vi/net/text-manipulation/apply-bullets-on-text/
---
## Giới thiệu
Chào mừng bạn đến với hướng dẫn từng bước này về cách áp dụng dấu đầu dòng vào văn bản bằng Aspose.Note for .NET. Aspose.Note là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc liền mạch với các tệp Microsoft OneNote trong ứng dụng .NET của họ. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình áp dụng dấu đầu dòng vào văn bản, nâng cao sức hấp dẫn trực quan cho tài liệu OneNote của bạn.
## Điều kiện tiên quyết
Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:
- Kiến thức cơ bản về lập trình C# và .NET.
-  Aspose.Note cho thư viện .NET được cài đặt. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/note/net/).
## Nhập không gian tên
Trong mã C# của bạn, hãy đảm bảo bao gồm các không gian tên cần thiết:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Bước 1: Thiết lập tài liệu của bạn
```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "Your Document Directory";
//Tạo một đối tượng của lớp Tài liệu
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Bước 2: Khởi tạo trang và dàn ý
```csharp
// Khởi tạo đối tượng lớp Trang
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Khởi tạo đối tượng lớp Outline
Outline outline = new Outline(doc);
```
## Bước 3: Đặt kiểu văn bản mặc định
```csharp
// Khởi tạo đối tượng lớp TextStyle và đặt thuộc tính định dạng
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Bước 4: Tạo các phần tử phác thảo bằng dấu đầu dòng
```csharp
// Khởi tạo các đối tượng lớp OutlineElement và áp dụng dấu đầu dòng
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Lặp lại cho các phần tử phác thảo khác
```
## Bước 5: Thêm các phần tử phác thảo vào phác thảo
```csharp
// Thêm các phần tử phác thảo
outline.AppendChildLast(outlineElem1);
// Lặp lại cho các phần tử phác thảo khác
```
## Bước 6: Thêm dàn ý vào trang
```csharp
// Thêm nút phác thảo
page.AppendChildLast(outline);
```
## Bước 7: Thêm trang vào tài liệu
```csharp
//Thêm nút Trang
doc.AppendChildLast(page);
```
## Bước 8: Lưu tài liệu OneNote
```csharp
// Lưu tài liệu OneNote
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Phần kết luận
Chúc mừng! Bạn đã học thành công cách áp dụng dấu đầu dòng vào văn bản bằng Aspose.Note for .NET. Tính năng này có thể nâng cao đáng kể việc định dạng tài liệu OneNote của bạn, khiến chúng trở nên hấp dẫn hơn về mặt hình ảnh.
## Câu hỏi thường gặp
### Tôi có thể áp dụng các kiểu dấu đầu dòng khác nhau cho từng mục trong danh sách không?
 Có, bạn có thể tùy chỉnh kiểu dấu đầu dòng bằng cách sửa đổi`NumberList` thuộc tính cho mỗi`OutlineElement`.
### Aspose.Note có tương thích với phiên bản Microsoft OneNote mới nhất không?
Aspose.Note hỗ trợ nhiều phiên bản khác nhau của Microsoft OneNote, đảm bảo khả năng tương thích với cả phiên bản cũ hơn và mới hơn.
### Tôi có thể sử dụng Aspose.Note cho mục đích thương mại không?
 Có, bạn có thể sử dụng Aspose.Note for .NET trong các dự án thương mại. Để có được giấy phép, hãy truy cập[đây](https://purchase.aspose.com/buy).
### Có phiên bản dùng thử cho Aspose.Note cho .NET không?
 Có, bạn có thể tải xuống bản dùng thử miễn phí[đây](https://releases.aspose.com/).
### Tôi có thể tìm thêm sự hỗ trợ và nguồn lực ở đâu?
 Bạn có thể truy cập diễn đàn cộng đồng Aspose.Note[đây](https://forum.aspose.com/c/note/28) để được hỗ trợ và thảo luận.