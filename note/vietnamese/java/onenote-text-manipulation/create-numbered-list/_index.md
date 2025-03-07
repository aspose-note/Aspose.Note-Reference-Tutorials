---
title: Tạo danh sách đánh số trong OneNote - Aspose.Note
linktitle: Tạo danh sách đánh số trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Tìm hiểu cách dễ dàng tạo danh sách đánh số trong OneNote bằng Aspose.Note for Java. Tải xuống bản dùng thử miễn phí và đi sâu vào thế giới phát triển Java!
weight: 14
url: /vi/java/onenote-text-manipulation/create-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo danh sách đánh số trong OneNote - Aspose.Note

## Giới thiệu
Aspose.Note for Java trao quyền cho các nhà phát triển Java làm việc liền mạch với các tệp Microsoft OneNote. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình tạo danh sách đánh số trong OneNote bằng thư viện Aspose.Note for Java mạnh mẽ.
## Điều kiện tiên quyết
Trước khi đi sâu vào hướng dẫn, hãy đảm bảo có sẵn các điều kiện tiên quyết sau:
- Đã cài đặt Bộ công cụ phát triển Java (JDK) trên máy của bạn.
-  Aspose.Note cho thư viện Java được tải xuống từ[đây](https://releases.aspose.com/note/java/).
## Nhập gói
Trước tiên, hãy nhập các gói cần thiết trong dự án Java của bạn để tận dụng tối đa các chức năng của Aspose.Note. Bao gồm mã sau đây trong dự án của bạn:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## Bước 1: Khởi tạo các đối tượng Tài liệu, Trang và Phác thảo
```java
// Thư mục tài liệu của bạn
String dataDir = "Your Document Directory";
// Tạo các đối tượng Tài liệu, Trang và Phác thảo
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Đặt kiểu văn bản mặc định
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Bước 2: Đặt kiểu văn bản mặc định
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Bước 3: Tạo các phần tử phác thảo
Bây giờ, hãy tạo các phần tử cho danh sách đánh số của bạn.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Lặp lại cho các phần tử khác (outlineElem2 và OutlineElem3)
```
## Bước 4: Thêm các phần tử phác thảo vào phác thảo
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Bước 5: Thêm dàn ý vào trang
```java
page.appendChildLast(outline);
```
## Bước 6: Lưu tài liệu
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Hãy làm theo các bước này một cách tỉ mỉ và bạn sẽ dễ dàng tạo danh sách được đánh số trong OneNote bằng cách sử dụng Aspose.Note for Java.
## Phần kết luận
Trong hướng dẫn này, chúng ta đã khám phá quy trình liền mạch để tạo danh sách đánh số trong OneNote bằng Aspose.Note cho Java. Các tính năng mạnh mẽ của thư viện khiến nó trở thành một công cụ vô giá dành cho các nhà phát triển Java làm việc với các tệp Microsoft OneNote.
## Các câu hỏi thường gặp
### Hỏi: Tôi có thể tùy chỉnh định dạng đánh số trong danh sách OneNote của mình không?
Đ: Chắc chắn rồi! Bạn có thể tùy chỉnh định dạng đánh số bằng lớp NumberList do Aspose.Note for Java cung cấp.
### Câu hỏi: Có phiên bản dùng thử cho Aspose.Note cho Java không?
 Trả lời: Có, bạn có thể tải xuống bản dùng thử miễn phí[đây](https://releases.aspose.com/).
### Câu hỏi: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.Note cho Java?
 Đáp: Hãy ghé thăm[Aspose.Note cho diễn đàn Java](https://forum.aspose.com/c/note/28) để hỗ trợ cộng đồng.
### Câu hỏi: Tôi có thể tìm tài liệu chi tiết về Aspose.Note cho Java ở đâu?
 Đáp: Hãy tham khảo[tài liệu](https://reference.aspose.com/note/java/) để biết thông tin toàn diện.
### Câu hỏi: Làm cách nào để mua giấy phép Aspose.Note cho Java?
 A: Bạn có thể mua giấy phép[đây](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
