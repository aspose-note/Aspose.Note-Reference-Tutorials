---
title: Tạo tài liệu OneNote với văn bản có định dạng trong Java
linktitle: Tạo tài liệu OneNote với văn bản có định dạng trong Java
second_title: API Java Aspose.Note
description: Tìm hiểu cách tạo tài liệu OneNote có định dạng phong phú theo chương trình trong Java bằng cách sử dụng Aspose.Note for Java. Hãy làm theo hướng dẫn từng bước của chúng tôi để tự động hóa tài liệu một cách liền mạch.
weight: 11
url: /vi/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo tài liệu OneNote với văn bản có định dạng trong Java

## Giới thiệu

Tạo tài liệu OneNote có định dạng phong phú theo chương trình có thể là một công cụ mạnh mẽ dành cho các nhà phát triển muốn tự động hóa các tác vụ tạo tài liệu trong ứng dụng Java. Aspose.Note for Java cung cấp một bộ tính năng và chức năng toàn diện để đạt được điều này một cách liền mạch. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình tạo tài liệu OneNote với văn bản đa dạng thức được định dạng bằng Aspose.Note cho Java.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn đã thiết lập các điều kiện tiên quyết sau:

1. Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt JDK trên hệ thống của mình.
2.  Aspose.Note for Java JAR: Tải xuống và đưa tệp Aspose.Note for Java JAR vào dự án của bạn. Bạn có thể lấy nó từ[Liên kết tải xuống](https://releases.aspose.com/note/java/).
3. Môi trường phát triển tích hợp (IDE): Sử dụng IDE ưa thích của bạn như IntelliJ IDEA hoặc Eclipse.

## Gói nhập khẩu

Trước tiên, bạn cần nhập các gói cần thiết vào dự án Java của mình. Thêm các câu lệnh nhập sau vào đầu tệp Java của bạn:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Bước 1: Thiết lập tài liệu và trang

Hãy bắt đầu bằng việc khởi tạo các đối tượng Document và Page:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Bước 2: Tạo tiêu đề có định dạng

Bây giờ, hãy tạo một tiêu đề có văn bản được định dạng:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## Bước 3: Tạo văn bản có định dạng

Tiếp theo, hãy tạo văn bản có định dạng với nhiều kiểu định dạng khác nhau:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## Bước 4: Thêm các phần tử vào trang và tài liệu

Bây giờ, hãy thêm tiêu đề và văn bản đa dạng thức vào trang và các thành phần phác thảo:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Bước 5: Lưu tài liệu

Cuối cùng, lưu tài liệu OneNote đã tạo:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Phần kết luận

Trong hướng dẫn này, chúng ta đã tìm hiểu cách tạo tài liệu OneNote có văn bản đa dạng thức được định dạng trong Java bằng cách sử dụng Aspose.Note for Java. Bằng cách làm theo các hướng dẫn từng bước này, bạn có thể dễ dàng tạo tài liệu OneNote tùy chỉnh theo chương trình, nâng cao khả năng tự động hóa tài liệu của mình.

## Câu hỏi thường gặp

### Q1: Tôi có thể tùy chỉnh thêm kiểu phông chữ không?

Trả lời 1: Có, bạn có thể điều chỉnh các thuộc tính khác nhau như màu phông chữ, kích thước, kiểu dáng, v.v. để phù hợp với yêu cầu của bạn.

### Câu hỏi 2: Aspose.Note for Java có tương thích với tất cả các IDE Java không?

Câu trả lời 2: Có, bạn có thể sử dụng Aspose.Note for Java với bất kỳ IDE Java nào hỗ trợ phát triển Java.

### Câu hỏi 3: Tôi có thể tích hợp chức năng này vào các ứng dụng web không?

Câu trả lời 3: Hoàn toàn có thể, Aspose.Note dành cho Java có thể được tích hợp liền mạch vào các ứng dụng web để tạo tài liệu động.

### Câu hỏi 4: Có bất kỳ yêu cầu cấp phép nào khi sử dụng Aspose.Note cho Java không?

Câu trả lời 4: Có, bạn cần có giấy phép để sử dụng Aspose.Note cho Java trong các dự án thương mại. Tuy nhiên, bạn cũng có thể sử dụng giấy phép tạm thời cho mục đích thử nghiệm.

### Câu hỏi 5: Aspose.Note for Java có hỗ trợ các định dạng tài liệu khác ngoài OneNote không?

Câu trả lời 5: Có, Aspose.Note for Java hỗ trợ nhiều định dạng tài liệu khác nhau, bao gồm định dạng PDF, HTML và hình ảnh.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
