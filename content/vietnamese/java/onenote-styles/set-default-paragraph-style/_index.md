---
title: Đặt kiểu đoạn văn mặc định trong OneNote - Aspose.Note
linktitle: Đặt kiểu đoạn văn mặc định trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Tìm hiểu cách đặt kiểu đoạn văn mặc định trong OneNote bằng Aspose.Note for Java. Hãy làm theo hướng dẫn từng bước của chúng tôi để định dạng văn bản hiệu quả trong các ứng dụng Java của bạn.
type: docs
weight: 11
url: /vi/java/onenote-styles/set-default-paragraph-style/
---
## Giới thiệu

Aspose.Note for Java cung cấp các khả năng mạnh mẽ để thao tác định dạng văn bản, bao gồm đặt kiểu đoạn văn mặc định. Hướng dẫn này sẽ hướng dẫn bạn quy trình thiết lập kiểu đoạn văn mặc định trong OneNote bằng Aspose.Note.

## Điều kiện tiên quyết

Trước khi bắt đầu, hãy đảm bảo bạn có những điều sau:

1. Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt JDK trên hệ thống của mình.
2.  Aspose.Note for Java Library: Tải xuống và cài đặt Aspose.Note for Java từ[trang tải xuống](https://releases.aspose.com/note/java/).
3. Môi trường phát triển tích hợp (IDE): Bạn nên cài đặt IDE, chẳng hạn như Eclipse hoặc IntelliJ IDEA, để thuận tiện cho việc mã hóa.

## Gói nhập khẩu

Đầu tiên, nhập các gói cần thiết để bắt đầu mã hóa:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

Bây giờ, hãy chia mã ví dụ thành nhiều bước:

## Bước 1: Khởi tạo tài liệu, trang và dàn ý

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## Bước 2: Tạo phần tử phác thảo

```java
OutlineElement outlineElem = new OutlineElement();
```

## Bước 3: Xác định kiểu đoạn văn mặc định

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## Bước 4: Tạo văn bản có định dạng với kiểu mặc định

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## Bước 5: Nối văn bản có định dạng vào phần tử phác thảo

```java
outlineElem.appendChildLast(text);
```

## Bước 6: Nối phần tử phác thảo vào phác thảo

```java
outline.appendChildLast(outlineElem);
```

## Bước 7: Nối dàn ý vào trang

```java
page.appendChildLast(outline);
```

## Bước 8: Nối trang vào tài liệu

```java
document.appendChildLast(page);
```

## Bước 9: Lưu tài liệu

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

Mã này sẽ đặt kiểu đoạn văn mặc định trong OneNote bằng Aspose.Note cho Java.

## Phần kết luận

Việc đặt kiểu đoạn văn mặc định trong OneNote theo chương trình có thể đạt được một cách hiệu quả với Aspose.Note for Java. Bằng cách làm theo các bước được nêu trong hướng dẫn này, bạn có thể tích hợp liền mạch chức năng này vào các ứng dụng Java của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tùy chỉnh thêm kiểu đoạn văn mặc định không?

Trả lời 1: Có, bạn có thể điều chỉnh các thông số khác nhau như tên phông chữ, kích thước, màu sắc và căn chỉnh cho phù hợp với yêu cầu của mình.

### Câu hỏi 2: Aspose.Note có hỗ trợ các thao tác định dạng văn bản khác không?

Câu trả lời 2: Hoàn toàn có thể, Aspose.Note cung cấp hỗ trợ rộng rãi cho việc thao tác định dạng văn bản, bao gồm kiểu phông chữ, dấu đầu dòng và thụt lề.

### Câu hỏi 3: Aspose.Note có tương thích với tất cả các phiên bản OneNote không?

Trả lời 3: Aspose.Note được thiết kế để hoạt động với các tệp Microsoft OneNote trên các phiên bản khác nhau, đảm bảo khả năng tương thích rộng rãi.

### Câu hỏi 4: Tôi có thể tích hợp Aspose.Note vào dự án Java hiện tại của mình không?

Câu trả lời 4: Có, bạn có thể dễ dàng tích hợp Aspose.Note vào các dự án Java của mình bằng cách thêm các phần phụ thuộc cần thiết và nhập các gói được yêu cầu.

### Câu hỏi 5: Có phiên bản dùng thử cho Aspose.Note không?

 Câu trả lời 5: Có, bạn có thể truy cập bản dùng thử miễn phí của Aspose.Note từ[trang mạng](https://releases.aspose.com/).