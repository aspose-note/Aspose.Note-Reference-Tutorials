---
date: 2026-04-03
description: Tìm hiểu cách thêm siêu liên kết vào tài liệu Aspose.Note bằng Aspose.Note
  cho .NET, tùy chỉnh giao diện siêu liên kết và chèn nhiều siêu liên kết để tạo các
  tệp OneNote phong phú hơn.
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: Cách Thêm Siêu Liên Kết vào Tài Liệu Aspose.Note
second_title: Aspose.Note .NET API
title: Cách Thêm Siêu Liên Kết vào Tài Liệu Aspose.Note
url: /vi/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Thêm Siêu Liên Kết trong Tài Liệu Aspose.Note

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách thêm siêu liên kết** vào văn bản trong tài liệu Aspose.Note bằng API .NET. Thêm một siêu liên kết biến các ghi chú tĩnh thành nội dung tương tác, có thể nhấp chuột—hoàn hảo để liên kết tới tài nguyên web, các phần nội bộ, hoặc tệp bên ngoài. Chúng tôi sẽ hướng dẫn từng bước, cho bạn biết cách **tùy chỉnh giao diện siêu liên kết**, và giải thích cách **chèn nhiều siêu liên kết** khi bạn cần các trang OneNote phong phú hơn.

## Câu trả lời nhanh
- **Lớp chính để tạo tệp OneNote là gì?** `Document` from Aspose.Note.
- **Thuộc tính nào làm cho văn bản hoạt động như một siêu liên kết?** `IsHyperlink = true` on `TextStyle`.
- **Tôi có thể liên kết tới các trang web bên ngoài không?** Yes, set `HyperlinkAddress` to a URL like `https://www.google.com`.
- **Tôi có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?** A valid Aspose.Note license is required for non‑evaluation builds.
- **Các phiên bản .NET nào được hỗ trợ?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.

## “Cách thêm siêu liên kết” trong Aspose.Note là gì
Thêm một siêu liên kết có nghĩa là gắn một URL vào một đoạn văn bản sao cho khi người dùng nhấp vào nó trong OneNote, tài nguyên được liên kết sẽ mở trong trình duyệt hoặc ứng dụng khác. Aspose.Note cung cấp cờ `TextStyle.IsHyperlink` và thuộc tính `HyperlinkAddress` để thực hiện điều này một cách lập trình.

## Tại sao nên thêm siêu liên kết vào tài liệu OneNote?
- **Cải thiện điều hướng:** Nhảy trực tiếp tới các trang web hoặc phần liên quan.
- **Tài liệu phong phú hơn:** Cung cấp tham chiếu, hướng dẫn, hoặc tệp nguồn mà không cần rời khỏi ghi chú.
- **Giao diện chuyên nghiệp:** Màu sắc và kiểu dáng có thể tùy chỉnh giúp siêu liên kết hòa hợp với thiết kế tài liệu của bạn.

## Yêu cầu trước

1. Kiến thức cơ bản về C# và Visual Studio.
2. Thư viện Aspose.Note for .NET đã được cài đặt – tải về từ [here](https://releases.aspose.com/note/net/).
3. Hiểu cấu trúc tài liệu Aspose.Note (các trang, outline, rich text).

## Nhập các không gian tên

Đầu tiên, nhập các không gian tên cho phép bạn truy cập các lớp cốt lõi của Aspose.Note và các kiểu .NET cơ bản.

```csharp
using System;
using System.Drawing;
```

## Hướng dẫn từng bước

### Bước 1: Tạo Đối tượng Document mới

Khởi tạo một `Document` sẽ chứa tất cả các trang và nội dung của bạn.

```csharp
Document doc = new Document();
```

### Bước 2: Định nghĩa các kiểu văn bản (bao gồm kiểu siêu liên kết)

Tạo hai đối tượng `TextStyle` – một cho văn bản thường và một cho siêu liên kết.  
Ở đây chúng ta cũng **tùy chỉnh giao diện siêu liên kết** bằng cách đặt màu phông chữ.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **Mẹo chuyên nghiệp:** Để chèn **nhiều siêu liên kết**, định nghĩa các đối tượng `TextStyle` bổ sung với các giá trị `HyperlinkAddress` khác nhau và tái sử dụng chúng trong các đoạn `RichText` sau này.

### Bước 3: Tạo các đối tượng RichText

Xây dựng đoạn văn bản kết hợp văn bản bình thường và siêu liên kết. Phương thức `Append` cho phép bạn nối các đoạn có kiểu dáng khác nhau.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### Bước 4: Tạo Outline và Outline Element

Outline hoạt động như các container cho các phần tử trực quan trên một trang. Đặt kích thước và vị trí theo nhu cầu.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### Bước 5: Thêm các phần tử vào Trang

Mỗi tệp OneNote bao gồm các trang. Chúng ta tạo một `Title` và một `Page`, sau đó gắn outline vào.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### Bước 6: Lưu tài liệu

Chọn thư mục, tạo tên tệp đầy đủ, và gọi `Save`. Tệp đầu ra sẽ là một tệp OneNote `.one` hợp lệ chứa siêu liên kết của bạn.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| Siêu liên kết không mở | Đảm bảo `HyperlinkAddress` bao gồm giao thức (`http://` hoặc `https://`). |
| Màu văn bản không được áp dụng | Đặt `FontColor` trên `TextStyle` được sử dụng cho siêu liên kết. |
| Cần nhiều liên kết trên một trang | Tạo nhiều đối tượng `TextStyle`, mỗi cái có `HyperlinkAddress` riêng, và nối chúng vào cùng hoặc các đối tượng `RichText` khác nhau. |
| Tài liệu không tải được trong OneNote | Xác minh bạn đang sử dụng phiên bản OneNote được hỗ trợ (2010+). |

## Câu hỏi thường gặp

**Q: Tôi có thể thêm nhiều siêu liên kết trong cùng một tài liệu bằng Aspose.Note không?**  
A: Có, chỉ cần tạo các thể hiện `TextStyle` bổ sung với các giá trị `HyperlinkAddress` khác nhau và nối chúng vào các đối tượng `RichText` của bạn.

**Q: Làm thế nào tôi có thể tùy chỉnh giao diện của siêu liên kết?**  
A: Sử dụng các thuộc tính như `FontColor`, `FontName`, và `FontSize` trên `TextStyle` có `IsHyperlink = true`. Điều này cho phép bạn phù hợp với thương hiệu tài liệu.

**Q: Aspose.Note có hỗ trợ siêu liên kết tới các trang web bên ngoài không?**  
A: Chắc chắn. Đặt `HyperlinkAddress` thành bất kỳ URL hợp lệ nào (bao gồm `http://` hoặc `https://`) để liên kết ra ngoài tệp OneNote.

**Q: Có thể tạo một tệp OneNote duy nhất chứa nhiều siêu liên kết không?**  
A: Có. Bằng cách liên tục nối các đoạn `RichText` có kiểu dáng khác nhau với các địa chỉ siêu liên kết khác nhau, bạn có thể **tạo một bộ sưu tập siêu liên kết trong một tệp**.

**Q: Aspose.Note có tương thích với các phiên bản OneNote mới nhất không?**  
A: Thư viện hoạt động với OneNote 2010 và các phiên bản sau, bao gồm cả phiên bản Windows 10 UWP.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.Note for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}