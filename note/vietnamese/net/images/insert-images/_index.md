---
date: 2026-05-05
description: Tìm hiểu cách chèn hình ảnh vào tài liệu Aspose.Note bằng .NET. Hướng
  dẫn từng bước này chỉ cho bạn cách căn chỉnh hình ảnh, thêm hình ảnh vào trang và
  nâng cao nội dung hình ảnh.
keywords:
- how to insert image
- how to align image
- append image to page
linktitle: Chèn hình ảnh vào tài liệu Aspose.Note
second_title: Aspose.Note .NET API
title: Cách chèn hình ảnh vào tài liệu Aspose.Note bằng .NET
url: /vi/net/images/insert-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách chèn hình ảnh vào tài liệu Aspose.Note bằng .NET

## Giới thiệu

Nếu bạn muốn làm cho các tệp Aspose.Note của mình trở nên sinh động hơn, **cách chèn hình ảnh** là kỹ năng đầu tiên bạn cần nắm vững. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn chi tiết các bước cần thiết để thêm hình ảnh, kiểm soát kích thước, định vị chúng một cách chính xác, và thậm chí căn chỉnh chúng theo ý muốn. Khi kết thúc, bạn sẽ tự tin chèn hình ảnh, căn chỉnh chúng và đính kèm hình ảnh vào trang — tất cả bằng mã C# sạch sẽ và dễ đọc.

## Câu trả lời nhanh
- **Thư viện nào cần thiết?** Aspose.Note for .NET  
- **Tôi có thể đặt kích thước hình ảnh bằng chương trình không?** Có – sử dụng các thuộc tính Width và Height.  
- **Làm thế nào để định vị một hình ảnh?** Điều chỉnh HorizontalOffset, VerticalOffset hoặc sử dụng các tùy chọn căn chỉnh.  
- **Có giới hạn nào về định dạng hình ảnh không?** JPG, PNG, BMP, GIF và các định dạng khác được hỗ trợ.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Một giấy phép Aspose.Note hợp lệ là bắt buộc cho việc sử dụng thương mại.

## Chèn hình ảnh trong Aspose.Note là gì?

Chèn một hình ảnh có nghĩa là tạo một đối tượng Aspose.Note.Image, cấu hình các thuộc tính hiển thị của nó, và gắn nó vào một trang trong tệp .one tương thích với OneNote. Điều này cho phép bạn làm phong phú các ghi chú bằng ảnh chụp màn hình, sơ đồ, hoặc bất kỳ công cụ hỗ trợ hình ảnh nào.

## Tại sao nên chèn hình ảnh bằng Aspose.Note?

- **Giao tiếp tốt hơn:** Hình ảnh làm rõ các ý tưởng phức tạp nhanh hơn so với chỉ văn bản.  
- **Bố cục nhất quán:** Kiểm soát bằng chương trình đảm bảo mọi tài liệu tuân theo cùng tiêu chuẩn thiết kế.  
- **Thân thiện với tự động hoá:** Lý tưởng để tạo báo cáo, hướng dẫn, hoặc sổ ghi chú được xử lý hàng loạt.

## Yêu cầu trước

1. Aspose.Note for .NET: Tải xuống và cài đặt Aspose.Note for .NET từ [đây](https://releases.aspose.com/note/net/).  
2. Tệp hình ảnh: Chuẩn bị các tệp hình ảnh (JPG, PNG, v.v.) mà bạn dự định nhúng sẵn trên ổ đĩa.

## Nhập không gian tên

Chúng ta bắt đầu bằng cách nhập các không gian tên cho phép chúng ta truy cập vào I/O tệp và API Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Bước 1: Tải tài liệu và lấy trang

Đầu tiên, mở tài liệu .one hiện có và lấy trang mà hình ảnh sẽ được chèn.

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## Cách căn chỉnh hình ảnh

Trước khi thêm hình ảnh, quyết định cách nó sẽ căn chỉnh với nội dung khác. Aspose.Note cung cấp các tùy chọn căn chỉnh ngang (Trái, Giữa, Phải). Bạn cũng có thể tinh chỉnh vị trí bằng các giá trị offset.

## Bước 2: Tải hình ảnh và đặt thuộc tính

Tạo đối tượng Image, chỉ tới tệp của bạn, và xác định kích thước, offset, và căn chỉnh.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Set image width
    Height = 100,               // Set image height
    HorizontalOffset = 100,     // Set horizontal offset
    VerticalOffset = 400,       // Set vertical offset
    Alignment = HorizontalAlignment.Right  // Set image alignment
};
```

## Đính kèm hình ảnh vào trang

Bây giờ hình ảnh đã được cấu hình đầy đủ, gắn nó vào cây phần tử của trang.

```csharp
page.AppendChildLast(image);
```

## Những lỗi thường gặp & Mẹo

- **Offset không đúng:** Hãy nhớ rằng offset được đo từ góc trên‑trái của trang. Offset dọc lớn có thể đẩy hình ảnh ra khỏi màn hình.  
- **Định dạng không hỗ trợ:** Nếu bạn thử một định dạng không được nhận dạng, Aspose.Note sẽ ném ra ngoại lệ — hãy chuyển tệp sang JPG hoặc PNG trước.  
- **Cảnh báo giấy phép:** Chạy mà không có giấy phép sẽ thêm watermark vào tài liệu được tạo; luôn áp dụng giấy phép của bạn trong môi trường sản xuất.

## Kết luận

Bạn đã học được **cách chèn hình ảnh** vào tài liệu Aspose.Note, **cách căn chỉnh hình ảnh**, và **cách đính kèm hình ảnh vào trang** bằng một vài dòng C# đơn giản. Những kỹ thuật này cho phép bạn tự động tạo ra các sổ ghi chú phong phú và chuyên nghiệp hơn.

## Câu hỏi thường gặp

### Câu 1: Tôi có thể chèn hình ảnh ở bất kỳ định dạng nào vào tài liệu Aspose.Note không?

A1: Có, Aspose.Note hỗ trợ nhiều định dạng hình ảnh bao gồm JPG, PNG, BMP, GIF, v.v.

### Câu 2: Có thể thay đổi kích thước hình ảnh đã chèn bằng chương trình không?

A2: Chắc chắn! Bạn có thể điều chỉnh chiều rộng và chiều cao của hình ảnh theo sở thích của mình khi chèn.

### Câu 3: Aspose.Note có cung cấp tùy chọn để chỉnh sửa căn chỉnh hình ảnh không?

A3: Có, bạn có thể căn chỉnh hình ảnh sang trái, phải hoặc giữa trong các trang tài liệu của mình.

### Câu 4: Tôi có thể chèn nhiều hình ảnh vào một trang duy nhất của tài liệu không?

A4: Chắc chắn! Bạn có thể chèn bao nhiêu hình ảnh tùy ý trên một trang duy nhất bằng Aspose.Note.

### Câu 5: Có giới hạn nào về kích thước tệp hình ảnh có thể chèn không?

A5: Aspose.Note không đặt ra giới hạn nghiêm ngặt về kích thước tệp hình ảnh, nhưng nên tối ưu hóa hình ảnh để hiệu suất tốt hơn.

## Các câu hỏi thường gặp

**Hỏi: Làm sao để tải hình ảnh từ một luồng thay vì đường dẫn tệp?**  
A: Sử dụng hàm khởi tạo Image(Stream, Document) và truyền một MemoryStream chứa các byte của hình ảnh.

**Hỏi: Tôi có thể thay đổi hình ảnh sau khi đã thêm vào trang không?**  
A: Có, bạn có thể sửa đổi các thuộc tính Width, Height, HorizontalOffset, VerticalOffset, và Alignment của đối tượng Image hiện có và sau đó gọi page.Update().

**Hỏi: Có thể thêm chú thích dưới hình ảnh không?**  
A: Chèn một phần tử RichText sau hình ảnh và đặt văn bản của nó làm chú thích.

**Hỏi: Aspose.Note có hỗ trợ GIF động không?**  
A: GIF động được xử lý như hình ảnh tĩnh; chỉ khung đầu tiên được hiển thị.

**Hỏi: Tôi nên làm gì nếu hình ảnh bị mờ?**  
A: Đảm bảo hình ảnh nguồn có độ phân giải đủ và tránh phóng to vượt quá kích thước gốc.

---

**Last Updated:** 2026-05-05  
**Tested With:** Aspose.Note 23.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}