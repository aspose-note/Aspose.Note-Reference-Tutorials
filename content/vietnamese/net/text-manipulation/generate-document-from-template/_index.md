---
title: Tạo tài liệu từ mẫu trong Aspose.Note
linktitle: Tạo tài liệu từ mẫu trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tạo tài liệu động dễ dàng với Aspose.Note cho .NET. Hãy làm theo hướng dẫn từng bước của chúng tôi để tạo tài liệu được cá nhân hóa và dựa trên dữ liệu.
type: docs
weight: 18
url: /vi/net/text-manipulation/generate-document-from-template/
---
## Giới thiệu
Trong bối cảnh tạo tài liệu ngày càng phát triển, Aspose.Note for .NET nổi bật như một công cụ mạnh mẽ để tạo tài liệu động một cách dễ dàng. Cho dù bạn đang xử lý báo cáo, hóa đơn hay tài liệu được cá nhân hóa, hướng dẫn này sẽ hướng dẫn bạn quy trình tạo tài liệu từ mẫu bằng Aspose.Note for .NET.
## Điều kiện tiên quyết
Trước khi đi sâu vào hướng dẫn từng bước, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:
1.  Aspose.Note for .NET Library: Tải xuống và cài đặt thư viện từ[Aspose.Note dành cho tài liệu .NET](https://reference.aspose.com/note/net/).
2. Mẫu tài liệu: Chuẩn bị tài liệu mẫu ở định dạng OneNote (có phần mở rộng .one). Điều này sẽ đóng vai trò là nền tảng cho tài liệu được tạo động của bạn.
## Nhập không gian tên
Đảm bảo bao gồm các không gian tên cần thiết trong dự án của bạn:
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
Bây giờ, hãy chia nhỏ từng bước trong hướng dẫn.
## Bước 1: Xác định thư mục tài liệu của bạn
```csharp
string dataDir = "Your Document Directory";
```
Thay thế "Thư mục tài liệu của bạn" bằng đường dẫn bạn muốn lưu tài liệu đã tạo.
## Bước 2: Tạo từ điển với các giá trị thay thế
```csharp
var templateData = new Dictionary<string, string>
{
    { "Company", "Atlas Shrugged Ltd" },
    { "CandidateName", "John Galt" },
    { "JobTitle", "Chief Entrepreneur Officer" },
    { "Department", "Sales" },
    { "Salary", "123456 USD" },
    { "Vacation", "30" },
    { "StartDate", "29 Feb 2024" },
    { "YourName", "Ayn Rand" }
};
```
Xác định một từ điển trong đó các khóa là phần giữ chỗ trong mẫu của bạn và các giá trị là dữ liệu bạn muốn thay thế chúng.

## Bước 3: Tải tài liệu mẫu
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
Tải tài liệu mẫu OneNote của bạn vào Aspose.Note.

## Bước 4: Thay thế các từ mẫu bằng dữ liệu động
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
Lặp lại qua từng đoạn trong mẫu, thay thế phần giữ chỗ bằng dữ liệu động.

## Bước 5: Lưu tài liệu đã tạo
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
Lưu tài liệu được tạo động vào thư mục được chỉ định của bạn.

## Phần kết luận
Chúc mừng! Bạn đã tạo thành công tài liệu động bằng Aspose.Note cho .NET. Quá trình này mở ra nhiều khả năng để tạo các tài liệu được cá nhân hóa và dựa trên dữ liệu một cách liền mạch.

## Các câu hỏi thường gặp
### Tôi có thể sử dụng Aspose.Note cho .NET với các định dạng tài liệu khác không?
Có, Aspose.Note for .NET chủ yếu xử lý các tài liệu OneNote, nhưng Aspose cung cấp nhiều thư viện khác nhau cho các định dạng khác nhau.
### Có bản dùng thử miễn phí dành cho Aspose.Note cho .NET không?
 Có, bạn có thể khám phá các khả năng của Aspose.Note dành cho .NET bằng bản dùng thử miễn phí. Thăm nom[đây](https://releases.aspose.com/) để biết thêm thông tin.
### Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.Note cho .NET?
 Tham quan[Aspose.Note dành cho diễn đàn .NET](https://forum.aspose.com/c/note/28) để nhận được sự hỗ trợ từ cộng đồng và các chuyên gia.
### Giấy phép tạm thời có sẵn cho Aspose.Note cho .NET không?
 Có, bạn có thể có được giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/) nhằm mục đích kiểm tra và đánh giá.
### Tôi có thể tìm tài liệu toàn diện về Aspose.Note cho .NET ở đâu?
 Tham khảo đến[tài liệu](https://reference.aspose.com/note/net/) để biết thông tin chuyên sâu về cách sử dụng Aspose.Note cho .NET.