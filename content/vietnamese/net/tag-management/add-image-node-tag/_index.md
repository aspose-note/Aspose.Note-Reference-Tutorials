---
title: Thêm nút hình ảnh có thẻ trong Aspose.Note
linktitle: Thêm nút hình ảnh có thẻ trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách nâng cao tài liệu OneNote của bạn bằng cách thêm hình ảnh có thẻ tùy chỉnh bằng Aspose.Note for .NET.
type: docs
weight: 10
url: /vi/net/tag-management/add-image-node-tag/
---
## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ khám phá cách thêm nút hình ảnh có thẻ bằng Aspose.Note cho .NET. Tính năng này cho phép bạn nâng cao tài liệu OneNote của mình bằng cách thêm hình ảnh bằng thẻ tùy chỉnh.

## Điều kiện tiên quyết

Trước khi bắt đầu, hãy đảm bảo bạn có những điều sau:

1. Visual Studio: Cài đặt Visual Studio IDE trên hệ thống của bạn.
2.  Aspose.Note for .NET: Tải xuống và cài đặt thư viện Aspose.Note for .NET từ[Liên kết tải xuống](https://releases.aspose.com/note/net/).
3. Kiến thức cơ bản: Làm quen với ngôn ngữ lập trình C# và .NET framework.

## Nhập không gian tên

Trước tiên, hãy đảm bảo bao gồm các không gian tên cần thiết trong mã C# của bạn:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Bước 1: Khởi tạo đối tượng tài liệu và trang

 Bắt đầu bằng cách tạo một thể hiện của`Document` lớp học và một`Page` sự vật:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Bước 2: Khởi tạo các đối tượng Outline và OutlineElement

 Tiếp theo, khởi tạo`Outline` Và`OutlineElement` các đối tượng:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## Bước 3: Tải và chèn hình ảnh

Tải hình ảnh mong muốn và chèn nó vào nút tài liệu:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## Bước 4: Thêm thẻ vào hình ảnh

Thêm thẻ tùy chỉnh vào hình ảnh:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## Bước 5: Nối phần tử phác thảo và nút trang

Nối phần tử phác thảo và các nút phác thảo vào trang:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## Bước 6: Lưu tài liệu

Lưu tài liệu OneNote đã sửa đổi:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## Phần kết luận

Bằng cách làm theo các bước này, bạn có thể thêm liền mạch nút hình ảnh bằng thẻ tùy chỉnh bằng cách sử dụng Aspose.Note for .NET, làm phong phú thêm tài liệu OneNote của bạn bằng hình ảnh được cá nhân hóa.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể thêm nhiều hình ảnh với các thẻ khác nhau vào một tài liệu bằng Aspose.Note không?

Câu trả lời 1: Có, bạn có thể thêm nhiều hình ảnh với các thẻ khác nhau bằng cách thực hiện theo các bước tương tự cho từng hình ảnh.

### Câu hỏi 2: Aspose.Note có tương thích với tất cả các phiên bản OneNote không?

Câu trả lời 2: Aspose.Note hỗ trợ nhiều phiên bản OneNote khác nhau, đảm bảo khả năng tương thích trên các môi trường khác nhau.

### Câu hỏi 3: Tôi có thể tùy chỉnh giao diện của thẻ được thêm vào hình ảnh không?

Câu trả lời 3: Có, Aspose.Note cung cấp tính linh hoạt trong việc tùy chỉnh giao diện thẻ cho phù hợp với sở thích của bạn.

### Câu hỏi 4: Aspose.Note có hỗ trợ thêm hình ảnh từ URL không?

Câu trả lời 4: Aspose.Note chủ yếu hỗ trợ thêm hình ảnh từ các thư mục cục bộ, nhưng trước tiên bạn có thể kết hợp các hình ảnh bên ngoài bằng cách tải chúng xuống cục bộ.

### Câu hỏi 5: Có bất kỳ hạn chế nào về kích thước hoặc định dạng của hình ảnh có thể được thêm vào không?

Câu trả lời 5: Aspose.Note hỗ trợ nhiều định dạng hình ảnh và không đặt ra giới hạn nghiêm ngặt nào về kích thước hình ảnh, cho phép bạn kết hợp các hình ảnh đa dạng vào tài liệu của mình.