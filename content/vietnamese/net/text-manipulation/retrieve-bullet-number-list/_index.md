---
title: Truy xuất danh sách dấu đầu dòng hoặc số trong văn bản Aspose.Note
linktitle: Truy xuất danh sách dấu đầu dòng hoặc số trong văn bản Aspose.Note
second_title: Aspose.Note .NET API
description: Khai phá tiềm năng của Aspose.Note dành cho .NET với hướng dẫn từng bước của chúng tôi về cách truy xuất danh sách dấu đầu dòng hoặc số. Nâng cao kỹ năng thao tác tài liệu OneNote của bạn!
type: docs
weight: 23
url: /vi/net/text-manipulation/retrieve-bullet-number-list/
---
## Giới thiệu
Chào mừng bạn đến với thế giới của Aspose.Note for .NET, một thư viện mạnh mẽ và linh hoạt giúp các nhà phát triển có thể xử lý thao tác tài liệu OneNote một cách dễ dàng. Trong hướng dẫn này, chúng ta sẽ đi sâu vào quá trình truy xuất danh sách dấu đầu dòng hoặc số bằng Aspose.Note cho .NET. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm hay người đam mê mã hóa, hướng dẫn này sẽ trang bị cho bạn kiến thức để điều hướng qua những điểm phức tạp khi làm việc với danh sách trong Aspose.Note.
## Điều kiện tiên quyết
Trước khi chúng ta bắt tay vào hành trình viết mã này, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:
-  Aspose.Note for .NET: Đảm bảo rằng bạn đã cài đặt thư viện Aspose.Note. Nếu không, bạn có thể tải xuống từ[Aspose.Note dành cho tài liệu .NET](https://reference.aspose.com/note/net/).
- Môi trường phát triển: Có môi trường phát triển hoạt động, tốt nhất là Microsoft Visual Studio, được thiết lập trên máy của bạn.
- Kiến thức cơ bản về C#: Làm quen với C# vì hướng dẫn này được viết bằng ngôn ngữ này.
## Nhập không gian tên
Để tương tác với Aspose.Note cho .NET, bạn cần nhập các không gian tên cần thiết vào dự án của mình. Bao gồm các không gian tên sau vào đầu mã của bạn:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Bây giờ, hãy chia nhỏ quá trình truy xuất danh sách dấu đầu dòng hoặc số theo từng bước:
## Bước 1: Đặt thư mục tài liệu của bạn
```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "Your Document Directory";
```
 Thay thế`"Your Document Directory"` với đường dẫn thực tế nơi đặt tài liệu Aspose.Note của bạn.
## Bước 2: Tải tài liệu
```csharp
// Tải tài liệu vào Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Đảm bảo rằng bạn thay thế`"ApplyNumberingOnText.one"` với tên tài liệu OneNote cụ thể của bạn.
## Bước 3: Truy xuất bộ sưu tập các nút
```csharp
// Truy xuất tập hợp các nút của phần tử phác thảo.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Bước này truy xuất một tập hợp các nút phác thảo từ tài liệu đã tải.
## Bước 4: Lặp lại qua từng nút
```csharp
// Lặp lại qua từng nút.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Tiếp tục thực hiện các bước tiếp theo...
    }
}
```
Vòng lặp này đảm bảo rằng chúng ta chỉ xử lý các nút có chứa danh sách số.
## Bước 5: Truy xuất thông tin phông chữ
```csharp
// Truy xuất tên phông chữ
Console.WriteLine("Font Name: " + list.Font);
// Truy xuất độ dài phông chữ
Console.WriteLine("Font Length: " + list.Font.Length);
// Truy xuất kích thước phông chữ
Console.WriteLine("Font Size: " + list.FontSize);
// Lấy lại màu chữ
Console.WriteLine("Font Color: " + list.FontColor);
// Truy xuất định dạng
Console.WriteLine("Font format: " + list.Format);
// Kiểm tra in đậm
Console.WriteLine("Is bold: " + list.IsBold);
// Kiểm tra chữ nghiêng
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Những dòng mã này trích xuất nhiều thông tin liên quan đến phông chữ từ danh sách số.
## Phần kết luận
 Chúc mừng! Bạn đã học thành công cách truy xuất danh sách dấu đầu dòng hoặc số bằng Aspose.Note cho .NET. Khi bạn tiếp tục khám phá, hãy tham khảo[tài liệu](https://reference.aspose.com/note/net/) để biết thêm thông tin chi tiết và chức năng chuyên sâu.
## Câu hỏi thường gặp
### Tôi có thể sử dụng Aspose.Note cho .NET với các ngôn ngữ lập trình khác không?
Aspose.Note chủ yếu hỗ trợ .NET, nhưng có các phiên bản khác của thư viện được điều chỉnh cho các nền tảng và ngôn ngữ khác nhau.
### Aspose.Note có tương thích với các định dạng OneNote mới nhất không?
Có, Aspose.Note hỗ trợ nhiều định dạng OneNote, đảm bảo khả năng tương thích với các phiên bản mới nhất.
### Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.Note?
 Thăm nom[liên kết này](https://purchase.aspose.com/temporary-license/) để có được giấy phép tạm thời cho mục đích đánh giá.
### Những tùy chọn hỗ trợ nào có sẵn cho người dùng Aspose.Note?
 Bạn có thể tìm hiểu và tìm kiếm sự trợ giúp trong[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) cho bất kỳ truy vấn hoặc vấn đề nào bạn có thể gặp phải.
### Có phiên bản dùng thử miễn phí của Aspose.Note cho .NET không?
 Có, bạn có thể truy cập phiên bản dùng thử miễn phí của Aspose.Note cho .NET[đây](https://releases.aspose.com/).