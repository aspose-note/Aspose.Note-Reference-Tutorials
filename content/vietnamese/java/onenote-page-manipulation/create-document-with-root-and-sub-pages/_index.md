---
title: Tạo tài liệu với trang gốc và trang phụ trong OneNote
linktitle: Tạo tài liệu với trang gốc và trang phụ trong OneNote
second_title: API Java Aspose.Note
description: Tạo tài liệu có trang gốc và trang phụ trong OneNote bằng Aspose.Note for Java. Hãy làm theo hướng dẫn từng bước để sắp xếp các ghi chú của bạn một cách hiệu quả.
type: docs
weight: 11
url: /vi/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## Giới thiệu

Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình tạo tài liệu với các trang gốc và trang phụ trong OneNote bằng Aspose.Note for Java. Bằng cách làm theo các bước này, bạn sẽ có thể sắp xếp hiệu quả các tài liệu OneNote của mình theo cấu trúc phân cấp.

## Điều kiện tiên quyết

Trước khi bắt đầu, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

1. Bộ công cụ phát triển Java (JDK): Đảm bảo rằng bạn đã cài đặt JDK trên hệ thống của mình.
2. Aspose.Note for Java: Tải xuống và cài đặt Aspose.Note for Java từ[trang mạng](https://purchase.aspose.com/buy).
3. Môi trường phát triển tích hợp (IDE): Chọn một Java IDE như IntelliJ IDEA, Eclipse hoặc NetBeans.

## Gói nhập khẩu

Bắt đầu bằng cách nhập các gói cần thiết trong dự án Java của bạn:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Bước 1: Thiết lập thư mục tài liệu

Xác định thư mục nơi bạn muốn lưu tài liệu OneNote của mình:

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tạo đối tượng tài liệu

 Khởi tạo một`Document` sự vật:

```java
Document doc = new Document();
```

## Bước 3: Tạo trang

Khởi tạo các đối tượng trang và đặt cấp độ của chúng:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Bước 4: Thêm nút vào trang

### Thêm nút vào trang đầu tiên

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Thêm nút vào trang thứ hai

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Thêm nút vào trang thứ ba

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Bước 5: Thêm trang vào tài liệu

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Bước 6: Lưu tài liệu

Lưu tài liệu OneNote:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Xử lý ngoại lệ
}
```

Chúc mừng! Bạn đã tạo thành công tài liệu có trang gốc và trang phụ trong OneNote bằng Aspose.Note for Java.

## Phần kết luận

Việc sắp xếp các tài liệu OneNote của bạn theo cấu trúc phân cấp là điều cần thiết để quản lý và điều hướng tốt hơn. Với Aspose.Note cho Java, bạn có thể tạo tài liệu với trang gốc và trang phụ một cách hiệu quả, cung cấp bố cục rõ ràng và có tổ chức cho ghi chú của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tạo nhiều cấp độ trang phụ bằng Aspose.Note cho Java không?

Câu trả lời 1: Có, bạn có thể tạo nhiều cấp độ trang phụ bằng cách đặt cấp độ phù hợp cho từng trang.

### Câu hỏi 2: Aspose.Note for Java có tương thích với các IDE Java khác nhau không?

Câu trả lời 2: Có, Aspose.Note for Java tương thích với các IDE Java phổ biến như IntelliJ IDEA, Eclipse và NetBeans.

### Câu hỏi 3: Tôi có thể tùy chỉnh định dạng văn bản trong tài liệu OneNote của mình không?

Câu trả lời 3: Có, bạn có thể tùy chỉnh phông chữ, màu sắc, kích thước và các tùy chọn định dạng khác bằng Aspose.Note dành cho các tính năng văn bản đa dạng thức của Java.

### Câu hỏi 4: Aspose.Note for Java có hỗ trợ lưu tài liệu ở các định dạng khác nhau không?

Câu trả lời 4: Có, Aspose.Note for Java hỗ trợ lưu tài liệu ở nhiều định dạng khác nhau bao gồm BMP, PDF, PNG, v.v.

### Câu hỏi 5: Có phiên bản dùng thử cho Aspose.Note cho Java không?

Câu trả lời 5: Có, bạn có thể tải xuống phiên bản dùng thử miễn phí của Aspose.Note dành cho Java từ trang web.