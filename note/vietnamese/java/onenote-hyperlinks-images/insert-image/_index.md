---
date: 2025-12-21
description: Tìm hiểu cách thêm hình ảnh vào tài liệu OneNote bằng Java với Aspose.Note
  for Java. Thực hiện theo hướng dẫn từng bước của chúng tôi để chèn hình ảnh và tùy
  chọn lưu OneNote dưới dạng PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Cách thêm hình ảnh vào OneNote bằng Java
url: /vi/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chèn hình ảnh vào tài liệu OneNote bằng Java

## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ khám phá cách chèn một hình ảnh vào tài liệu OneNote bằng Java với sự trợ giúp của Aspose.Note for Java. Aspose.Note for Java là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote một cách lập trình, hỗ trợ các thao tác như tạo, đọc và thao tác các tài liệu OneNote.

## Câu trả lời nhanh
- **Cách dễ nhất để thêm hình ảnh vào OneNote bằng Java là gì?**  
  Sử dụng lớp `Image` của Aspose.Note for Java và thêm nó vào một trang.
- **Tôi có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?**  
  Có, cần giấy phép thương mại cho các triển khai trong môi trường sản xuất.
- **Tôi có thể đặt kích thước tùy chỉnh cho hình ảnh không?**  
  Chắc chắn – gọi `setWidth()` và `setHeight()` trên đối tượng `Image`.
- **Có thể lưu tệp OneNote dưới dạng PDF sau khi thêm hình ảnh không?**  
  Có, gọi `save(..., SaveFormat.Pdf)` để **lưu OneNote dưới dạng PDF**.
- **Phiên bản Java nào được hỗ trợ?**  
  Aspose.Note for Java hoạt động với JDK 8 và các phiên bản sau.

## Cách thêm hình ảnh vào OneNote bằng Java?

Trước khi bắt đầu viết mã, hãy cùng thảo luận ngắn gọn tại sao bạn có thể muốn nhúng hình ảnh vào OneNote một cách lập trình. Dù bạn đang tạo biên bản họp, tạo báo cáo tự động, hay xây dựng quy trình tài liệu, việc chèn hình ảnh sẽ cung cấp ngữ cảnh trực quan cho ghi chú mà văn bản thuần không thể mang lại. Với Aspose.Note for Java, bạn có thể thực hiện toàn bộ quá trình này bằng code, mà không cần mở giao diện OneNote.

## Yêu cầu trước

Trước khi bắt đầu, hãy đảm bảo rằng bạn đã thiết lập các yêu cầu sau:

### 1. Java Development Kit (JDK)
Đảm bảo bạn đã cài đặt Java Development Kit (JDK) trên hệ thống của mình. Bạn có thể tải và cài đặt JDK từ trang web của Oracle.

### 2. Aspose.Note for Java Library
Tải xuống và thiết lập thư viện Aspose.Note for Java bằng cách tham khảo [documentation](https://reference.aspose.com/note/java/).

## Nhập gói

Bắt đầu bằng việc nhập các gói cần thiết vào dự án Java của bạn. Các gói này bao gồm thư viện Aspose.Note và các phụ thuộc khác cần thiết.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Hãy phân tích quy trình chèn hình ảnh vào tài liệu OneNote thành nhiều bước:

## Bước 1: Tải tài liệu OneNote

Đầu tiên, tải tài liệu OneNote mà bạn muốn chèn hình ảnh vào.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Bước 2: Lấy trang

Lấy trang trong tài liệu nơi bạn muốn chèn hình ảnh.

```java
Page page = oneFile.getFirstChild();
```

## Bước 3: Tải hình ảnh

Tải hình ảnh mà bạn muốn chèn vào tài liệu OneNote.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Bước 4: Tùy chỉnh thuộc tính hình ảnh (Tùy chọn)

Tùy chọn, bạn có thể tùy chỉnh kích thước, vị trí và căn chỉnh của hình ảnh theo yêu cầu của mình. Đây là nơi bạn **đặt kích thước hình ảnh theo phong cách Java**.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Bước 5: Thêm hình ảnh vào trang

Thêm hình ảnh vào trang trong tài liệu OneNote.

```java
page.appendChildLast(image);
```

## Bước 6: Lưu tài liệu

Lưu tài liệu đã chỉnh sửa, bao gồm cả hình ảnh đã chèn. Bạn cũng có thể **lưu OneNote dưới dạng PDF** ở bước này.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Kết luận

Trong hướng dẫn này, chúng ta đã học cách chèn một hình ảnh vào tài liệu OneNote bằng Java với sự trợ giúp của thư viện Aspose.Note for Java. Bằng cách làm theo hướng dẫn từng bước, bạn có thể dễ dàng tích hợp hình ảnh vào tài liệu OneNote một cách lập trình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể chèn nhiều hình ảnh vào một tài liệu OneNote duy nhất bằng phương pháp này không?
A1: Có, bạn có thể chèn nhiều hình ảnh vào một tài liệu OneNote duy nhất bằng cách lặp lại quy trình đã mô tả trong hướng dẫn này cho mỗi hình ảnh.

### Câu hỏi 2: Aspose.Note for Java có tương thích với mọi phiên bản OneNote không?
A2: Aspose.Note for Java hỗ trợ làm việc với các tệp OneNote được tạo trong Microsoft OneNote 2010 và các phiên bản sau này.

### Câu hỏi 3: Tôi có thể chèn hình ảnh ở các định dạng khác nhau, như PNG hoặc GIF, vào tài liệu OneNote không?
A3: Có, Aspose.Note for Java hỗ trợ chèn hình ảnh ở nhiều định dạng, bao gồm PNG, JPEG, GIF và các định dạng khác.

### Câu hỏi 4: Có phiên bản dùng thử của Aspose.Note for Java để thử nghiệm không?
A4: Có, bạn có thể tải xuống phiên bản dùng thử miễn phí của Aspose.Note for Java từ trang web để đánh giá.

### Câu hỏi 5: Làm thế nào để tôi nhận được hỗ trợ kỹ thuật cho Aspose.Note for Java?
A5: Bạn có thể nhận hỗ trợ kỹ thuật cho Aspose.Note for Java bằng cách truy cập [forum](https://forum.aspose.com/c/note/28) dành cho các sản phẩm Aspose.Note.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}