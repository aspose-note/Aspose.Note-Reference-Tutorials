---
title: Mở và đóng dự án bằng thẻ trong Aspose.Note
linktitle: Mở và đóng dự án bằng thẻ trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách thao tác với các tệp Microsoft OneNote theo chương trình bằng Aspose.Note for .NET. Mở và đóng dự án bằng thẻ một cách hiệu quả.
type: docs
weight: 15
url: /vi/net/tag-management/open-close-projects-tags/
---
## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ tìm hiểu cách sử dụng Aspose.Note cho .NET để mở và đóng các dự án bằng thẻ. Aspose.Note là một API mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote theo chương trình, cho phép thực hiện các tác vụ như thao tác văn bản, hình ảnh và thẻ trong tài liệu.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn đã thiết lập các điều kiện tiên quyết sau:

## Nhập không gian tên

```csharp
using System.IO;
using System.Linq;
```

Bây giờ hãy chia mỗi ví dụ thành nhiều bước:

## Bước 1: Tải tài liệu

Đầu tiên, chúng ta cần tải tài liệu vào Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Bước 2: Đóng các mục dự án C

Bây giờ, hãy đóng tất cả các mục hộp kiểm liên quan đến 'Dự án C'.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Bước 3: Lưu ghi chú dự án đã đóng C

Lưu tài liệu đã sửa đổi với các mục 'Dự án C' đã đóng.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Bước 4: Mở các mục Project C

Tiếp theo, chúng ta hãy mở tất cả các mục hộp kiểm liên quan đến “Dự án C”.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Bước 5: Lưu ghi chú dự án C đang mở

Lưu tài liệu đã sửa đổi với các mục 'Dự án C' đã mở.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Bây giờ bạn đã học cách mở và đóng dự án bằng thẻ trong Aspose.Note bằng .NET.

## Phần kết luận

Aspose.Note for .NET cung cấp một cách thuận tiện để thao tác các tài liệu OneNote theo chương trình. Bằng cách làm theo hướng dẫn này, bạn có thể quản lý dự án của mình một cách hiệu quả bằng cách mở và đóng các mục bằng thẻ.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.Note có tương thích với tất cả các phiên bản OneNote không?

Trả lời 1: Aspose.Note hỗ trợ Microsoft OneNote 2010 và các phiên bản mới hơn.

### Câu hỏi 2: Tôi có thể sử dụng Aspose.Note cho các dự án thương mại không?

 Câu trả lời 2: Có, bạn có thể sử dụng Aspose.Note cho cả dự án cá nhân và thương mại. Thăm nom[đây](https://purchase.aspose.com/buy) để mua giấy phép.

### Câu 3: Aspose.Note có cung cấp bản dùng thử miễn phí không?

 A3: Có, bạn có thể dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 4: Tôi có thể tìm tài liệu về Aspose.Note ở đâu?

 A4: Bạn có thể tìm tài liệu[đây](https://reference.aspose.com/note/net/).

### Câu hỏi 5: Tôi có thể nhận hỗ trợ cho Aspose.Note ở đâu?

 Câu trả lời 5: Để được hỗ trợ, bạn có thể truy cập Aspose.Note[diễn đàn](https://forum.aspose.com/c/note/28).