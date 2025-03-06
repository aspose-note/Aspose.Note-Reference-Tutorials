---
title: Xây dựng tài liệu và chèn hình ảnh bằng luồng trong OneNote - Java
linktitle: Xây dựng tài liệu và chèn hình ảnh bằng luồng trong OneNote - Java
second_title: API Java Aspose.Note
description: Tìm hiểu cách tích hợp hình ảnh dễ dàng vào tài liệu OneNote bằng Aspose.Note for Java. Hướng dẫn từng bước dành cho nhà phát triển Java.
weight: 13
url: /vi/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xây dựng tài liệu và chèn hình ảnh bằng luồng trong OneNote - Java

## Giới thiệu

Chào mừng bạn đến với hướng dẫn toàn diện của chúng tôi về cách sử dụng Aspose.Note cho Java để xây dựng tài liệu và chèn hình ảnh bằng luồng hình ảnh trong OneNote! Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước thực hiện quy trình, đảm bảo bạn hiểu rõ ràng về từng giai đoạn. Cuối cùng, bạn sẽ có thể dễ dàng tích hợp hình ảnh vào tài liệu OneNote của mình bằng Java.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

### Bộ công cụ phát triển Java (JDK)

Đảm bảo bạn đã cài đặt Bộ công cụ phát triển Java (JDK) trên hệ thống của mình. Bạn có thể tải nó từ trang web của Oracle.

### Aspose.Note cho Thư viện Java

 Tải xuống và cài đặt thư viện Aspose.Note cho Java từ thư viện được cung cấp[liên kết](https://releases.aspose.com/note/java/).

### Cài đặt IDE

Thiết lập Môi trường phát triển tích hợp (IDE) của bạn với các cấu hình cần thiết để làm việc với các dự án Java.

## Gói nhập khẩu

Để bắt đầu, hãy nhập các gói cần thiết vào dự án Java của bạn. Các gói này sẽ cung cấp chức năng cần thiết để hoạt động với các tài liệu và hình ảnh OneNote.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Bước 1: Thiết lập thư mục tài liệu

 Xác định thư mục chứa tài liệu và hình ảnh của bạn. Thay thế`"Your Document Directory"` với đường dẫn đến thư mục của bạn.

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tạo đối tượng tài liệu

 Khởi tạo một thể hiện của`Document` class để bắt đầu làm việc với tài liệu OneNote của bạn.

```java
Document doc = new Document();
```

## Bước 3: Khởi tạo đối tượng trang

 Tạo một`Page` đối tượng để đại diện cho trang trong tài liệu.

```java
Page page = new Page();
```

## Bước 4: Tạo phác thảo

 Khởi tạo một`Outline` đối tượng để cấu trúc nội dung trong trang.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Bước 5: Tạo phần tử phác thảo

 Tạo ra một`OutlineElement` để giữ hình ảnh và xác định vị trí của nó.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Bước 6: Tải luồng hình ảnh

 Tải luồng hình ảnh bằng cách sử dụng`FileInputStream` cho hình ảnh mong muốn.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Bước 7: Chèn hình ảnh

 Chèn hình ảnh vào tài liệu bằng cách tạo một`Image` đối tượng và thiết lập sự liên kết của nó.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Bước 8: Nối hình ảnh vào phần tử phác thảo

Nối hình ảnh vào phần tử phác thảo.

```java
outlineElem1.appendChildLast(image);
```

## Bước 9: Nối phần tử phác thảo vào phác thảo

Thêm phần tử phác thảo vào phác thảo.

```java
outline1.appendChildLast(outlineElem1);
```

## Bước 10: Nối dàn ý vào trang

Thêm dàn ý vào trang.

```java
page.appendChildLast(outline1);
```

## Bước 11: Nối trang vào tài liệu

Cuối cùng, nối trang vào tài liệu.

```java
doc.appendChildLast(page);
```

## Bước 12: Lưu tài liệu

Lưu tài liệu đã sửa đổi, chỉ định định dạng mong muốn (ví dụ: PDF).

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Bằng cách làm theo các bước này, bạn có thể dễ dàng tạo tài liệu và chèn hình ảnh bằng luồng hình ảnh trong OneNote bằng Aspose.Note for Java.

## Phần kết luận

Tóm lại, việc nắm vững cách tích hợp hình ảnh vào tài liệu OneNote bằng Java có thể nâng cao đáng kể quá trình tạo tài liệu của bạn. Với Aspose.Note for Java, bạn có sẵn một công cụ mạnh mẽ để hoàn thành nhiệm vụ này một cách liền mạch.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.Note for Java có tương thích với tất cả các phiên bản OneNote không?

Câu trả lời 1: Aspose.Note for Java hỗ trợ nhiều phiên bản OneNote khác nhau, đảm bảo khả năng tương thích trên các môi trường khác nhau.

### Câu hỏi 2: Tôi có thể tùy chỉnh giao diện của hình ảnh được chèn trong tài liệu OneNote bằng Aspose.Note for Java không?

Câu trả lời 2: Có, bạn có thể tùy chỉnh các khía cạnh khác nhau của hình ảnh được chèn, chẳng hạn như căn chỉnh, kích thước và hướng để phù hợp với yêu cầu cụ thể của bạn.

### Câu hỏi 3: Aspose.Note for Java có hỗ trợ các định dạng tài liệu khác ngoài PDF không?

Câu trả lời 3: Có, Aspose.Note for Java hỗ trợ nhiều định dạng tài liệu, bao gồm DOCX, HTML, v.v., giúp bạn linh hoạt trong các tác vụ quản lý tài liệu của mình.

### Câu hỏi 4: Tôi có thể tìm thêm tài nguyên và hỗ trợ cho Aspose.Note dành cho Java ở đâu?

Câu trả lời 4: Bạn có thể truy cập tài liệu, liên kết tải xuống, diễn đàn hỗ trợ và giấy phép tạm thời cho Aspose.Note cho Java thông qua các liên kết được cung cấp.

### Câu hỏi 5: Có phiên bản dùng thử cho Aspose.Note cho Java không?

Câu trả lời 5: Có, bạn có thể tải bản dùng thử miễn phí Aspose.Note dành cho Java để khám phá các tính năng và khả năng của nó trước khi đưa ra quyết định mua hàng.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
