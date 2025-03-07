---
title: Lưu vào hình ảnh thang độ xám trong Aspose.Note
linktitle: Lưu vào hình ảnh thang độ xám trong Aspose.Note
second_title: Aspose.Note .NET API
description: Tìm hiểu cách lưu tài liệu OneNote dưới dạng hình ảnh thang độ xám bằng Aspose.Note for .NET. Hãy làm theo hướng dẫn toàn diện này để xử lý tài liệu hiệu quả.
weight: 24
url: /vi/net/loading-and-saving-operations/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu vào hình ảnh thang độ xám trong Aspose.Note

## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ khám phá cách sử dụng Aspose.Note cho .NET để lưu tài liệu dưới dạng hình ảnh thang độ xám. Aspose.Note là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote theo chương trình, cung cấp nhiều chức năng.

## Điều kiện tiên quyết

Trước khi chúng tôi tiến hành, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

- Hiểu biết cơ bản về ngôn ngữ lập trình C#.
- Visual Studio được cài đặt trên hệ thống của bạn.
-  Aspose.Note cho thư viện .NET được cài đặt. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/note/net/).
- Làm quen với việc truy cập và thao tác với các tệp bằng .NET.

## Nhập không gian tên

Hãy bắt đầu bằng cách nhập các không gian tên cần thiết:

```csharp
using System;

using Aspose.Note.Saving;

```

## Bước 1: Tải tài liệu

Đầu tiên, tải tài liệu vào Aspose.Note. 

```csharp
string dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Bước 2: Lưu dưới dạng hình ảnh thang độ xám

Tiếp theo, chỉ định đường dẫn lưu hình ảnh thang độ xám và lưu tài liệu tương ứng.

```csharp
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
oneFile.Save(dataDir, new ImageSaveOptions(SaveFormat.Png)
					  {
						  ColorMode = ColorMode.GrayScale
					  });
```

## Bước 3: Xác minh và hiển thị kết quả

Cuối cùng, xác minh và hiển thị thông báo chuyển đổi thành công cùng với đường dẫn tệp.

```csharp
Console.WriteLine("\nOneNote document converted successfully to grayscale image.\nFile saved at " + dataDir);
```

## Phần kết luận

Trong hướng dẫn này, chúng ta đã học cách sử dụng Aspose.Note for .NET để chuyển đổi tài liệu thành hình ảnh thang độ xám. Bằng cách làm theo các bước đơn giản này, nhà phát triển có thể kết hợp hiệu quả chức năng này vào ứng dụng của mình, nâng cao khả năng xử lý tài liệu của họ.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.Note có thể xử lý các tệp OneNote phức tạp không?

Câu trả lời 1: Có, Aspose.Note có thể xử lý các tệp OneNote phức tạp một cách hiệu quả, cung cấp các chức năng mạnh mẽ để thao tác tài liệu.

### Câu hỏi 2: Aspose.Note có tương thích với các định dạng tệp khác nhau không?

Câu trả lời 2: Hoàn toàn có thể, Aspose.Note hỗ trợ nhiều định dạng tệp khác nhau, đảm bảo tính linh hoạt trong quá trình xử lý tài liệu.

### Câu 3: Aspose.Note có cung cấp hỗ trợ cho nhà phát triển không?

Câu trả lời 3: Có, các nhà phát triển có thể truy cập hỗ trợ toàn diện thông qua diễn đàn và tài liệu Aspose.

### Câu hỏi 4: Tôi có thể dùng thử Aspose.Note trước khi mua không?

Câu trả lời 4: Có, bạn có thể khám phá Aspose.Note thông qua bản dùng thử miễn phí có sẵn trên trang web của họ.

### Câu hỏi 5: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.Note?

Câu trả lời 5: Bạn có thể lấy giấy phép tạm thời cho Aspose.Note bằng cách truy cập liên kết được cung cấp và làm theo hướng dẫn.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
