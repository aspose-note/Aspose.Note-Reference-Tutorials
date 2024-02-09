---
title: Hoạt động xuất khẩu tiếp theo trong Aspose.Note
linktitle: Hoạt động xuất khẩu tiếp theo trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách thực hiện các thao tác xuất tiếp theo trong Aspose.Note for .NET để lưu tài liệu OneNote ở các định dạng khác nhau một cách hiệu quả.
type: docs
weight: 10
url: /vi/net/loading-and-saving-operations/consequent-export-operations/
---
## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ đi sâu vào việc thực hiện các hoạt động xuất sau đó bằng Aspose.Note cho .NET. Aspose.Note là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote theo chương trình. Xuất tài liệu sang các định dạng khác nhau là một yêu cầu phổ biến và Aspose.Note đơn giản hóa tác vụ này một cách hiệu quả. Hãy cùng khám phá cách lưu tài liệu ở nhiều định dạng khác nhau từng bước.

## Điều kiện tiên quyết

Trước khi tiếp tục với hướng dẫn này, hãy đảm bảo bạn có những điều sau:

1. Hiểu biết cơ bản về ngôn ngữ lập trình C#.
2. Visual Studio được cài đặt trên hệ thống của bạn.
3. Aspose.Note cho thư viện .NET được tích hợp vào dự án của bạn.

## Nhập không gian tên

Để bắt đầu, hãy đảm bảo nhập các vùng tên cần thiết trong mã C# của bạn:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Drawing;
using System.Globalization;
```

## Bước 1: Khởi tạo tài liệu

 Đầu tiên, khởi tạo một cái mới`Document` đối tượng bị tắt tính năng phát hiện thay đổi bố cục tự động:

```csharp
Document doc = new Document() { AutomaticLayoutChangesDetectionEnabled = false };
```

## Bước 2: Khởi tạo một trang mới

 Tạo một cái mới`Page` đối tượng và chỉ định các thuộc tính của nó:

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Bước 3: Đặt tiêu đề trang

Xác định tiêu đề cho trang cùng với thông tin ngày và giờ:

```csharp
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Bước 4: Nối nút trang

Thêm nút trang vào tài liệu:

```csharp
doc.AppendChildLast(page);
```

## Bước 5: Lưu tài liệu ở các định dạng khác nhau

Bây giờ, hãy lưu tài liệu OneNote ở nhiều định dạng khác nhau:

```csharp
string dataDir = "Your Document Directory";
doc.Save(dataDir + "ConsequentExportOperations_out.html");            
doc.Save(dataDir + "ConsequentExportOperations_out.pdf");            
doc.Save(dataDir + "ConsequentExportOperations_out.jpg");            
textStyle.FontSize = 11;           
doc.DetectLayoutChanges();            
doc.Save(dataDir + "ConsequentExportOperations_out.bmp");
```

## Phần kết luận

Tóm lại, chúng ta đã học cách thực hiện các thao tác xuất sau đó bằng Aspose.Note cho .NET. Bằng cách làm theo các bước được nêu trong hướng dẫn này, bạn có thể lưu tài liệu OneNote một cách liền mạch ở nhiều định dạng khác nhau, từ đó nâng cao tính linh hoạt cho ứng dụng của bạn.

## Câu hỏi thường gặp

### Q1: Tôi có thể tùy chỉnh thêm tiêu đề trang không?

Trả lời 1: Có, bạn có thể sửa đổi văn bản tiêu đề, ngày và giờ theo yêu cầu của mình trước khi lưu tài liệu.

### Câu hỏi 2: Làm cách nào để xử lý việc phát hiện thay đổi bố cục?

 Câu trả lời 2: Như đã trình bày, bạn có thể phát hiện các thay đổi bố cục theo cách thủ công bằng cách sử dụng`DetectLayoutChanges()` phương pháp được cung cấp bởi Aspose.Note.

### Câu hỏi 3: Aspose.Note có hỗ trợ các định dạng xuất khác ngoài các định dạng được đề cập không?

Câu trả lời 3: Có, Aspose.Note hỗ trợ nhiều định dạng xuất, bao gồm DOCX, PNG, TIFF, v.v.

### Câu hỏi 4: Aspose.Note có tương thích với .NET Core không?

Câu trả lời 4: Có, Aspose.Note tương thích với cả môi trường .NET Framework và .NET Core.

### Câu hỏi 5: Tôi có thể tìm thêm tài nguyên và hỗ trợ cho Aspose.Note ở đâu?

Câu trả lời 5: Bạn có thể truy cập tài liệu và diễn đàn Aspose.Note để xem hướng dẫn, hướng dẫn toàn diện và hỗ trợ cộng đồng.