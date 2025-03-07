---
title: Chuyển đổi chủ đề tối với Aspose.Note cho .NET
linktitle: Áp dụng chủ đề tối cho văn bản trong Aspose.Note
second_title: Aspose.Note .NET API
description: Chuyển đổi tài liệu OneNote của bạn bằng Aspose.Note for .NET! Áp dụng chủ đề tối kiểu dáng đẹp một cách dễ dàng. Tải xuống ngay bây giờ và nâng cao trải nghiệm ghi chú của bạn.
weight: 11
url: /vi/net/text-manipulation/apply-dark-theme-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi chủ đề tối với Aspose.Note cho .NET

## Giới thiệu
Chào mừng bạn đến với hướng dẫn từng bước của chúng tôi về cách áp dụng chủ đề tối cho văn bản trong Aspose.Note for .NET. Aspose.Note là một API .NET mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote theo chương trình. Trong hướng dẫn này, chúng ta sẽ khám phá cách mang đến cho tài liệu OneNote của bạn một giao diện đẹp mắt và hiện đại bằng cách áp dụng chủ đề tối cho văn bản.
## Điều kiện tiên quyết
Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:
-  Aspose.Note for .NET: Đảm bảo bạn đã cài đặt Aspose.Note for .NET. Nếu không, bạn có thể tải xuống từ[Tài liệu Aspose.Note](https://reference.aspose.com/note/net/).
- Môi trường phát triển: Thiết lập môi trường phát triển .NET ưa thích của bạn, chẳng hạn như Visual Studio.
- Thư mục Tài liệu: Chuẩn bị thư mục chứa tài liệu OneNote của bạn.
## Nhập không gian tên
Trong dự án .NET của bạn, hãy nhập các vùng tên cần thiết để hoạt động với Aspose.Lưu ý:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## Bước 1: Tải tài liệu OneNote
Tải tài liệu OneNote của bạn vào Aspose.Note bằng mã sau:
```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "Your Document Directory";
// Tải tài liệu vào Aspose.Note.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## Bước 2: Đặt màu nền
Đặt màu nền của mỗi trang thành màu đen:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## Bước 3: Điều chỉnh màu văn bản
Chỉnh màu chữ của văn bản thành màu trắng để nhìn rõ hơn:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## Bước 4: Lưu tài liệu
Lưu tài liệu OneNote đã sửa đổi dưới dạng PDF:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## Phần kết luận
Chúc mừng! Bạn đã áp dụng thành công chủ đề tối cho văn bản trong tài liệu Aspose.Note của mình. Cải tiến đơn giản nhưng hiệu quả này có thể mang lại cho các tệp OneNote của bạn một diện mạo tinh tế hơn.
## Các câu hỏi thường gặp
### Tôi có thể áp dụng chủ đề tối cho các phần cụ thể trong tài liệu OneNote của mình không?
Có, bạn có thể tùy chỉnh mã để nhắm mục tiêu các trang hoặc phần cụ thể trong tài liệu của mình.
### Aspose.Note có hỗ trợ các định dạng xuất khác ngoài PDF không?
Tuyệt đối! Aspose.Note hỗ trợ nhiều định dạng xuất khác nhau, bao gồm hình ảnh và Microsoft Word.
### Có giới hạn nào về kích thước tài liệu mà Aspose.Note có thể xử lý không?
Aspose.Note có thể xử lý các tài liệu có kích thước khác nhau và hiệu suất của nó được tối ưu hóa để mang lại hiệu quả.
### Tôi có thể quay lại chủ đề ban đầu sau khi áp dụng chủ đề tối không?
Có, bạn có thể sửa đổi mã để chuyển giữa các chủ đề dựa trên sở thích của mình.
### Tôi có thể nhận hỗ trợ cho các truy vấn liên quan đến Aspose.Note ở đâu?
 Để được trợ giúp, hãy truy cập[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) hoặc khám phá[tài liệu](https://reference.aspose.com/note/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
