---
title: Thêm nút văn bản có thẻ trong OneNote - Aspose.Note
linktitle: Thêm nút văn bản có thẻ trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Khám phá cách thêm nút văn bản có thẻ trong OneNote bằng Aspose.Note for Java. Dễ dàng, hiệu quả và thân thiện với nhà phát triển. Tải thư viện ngay bây giờ!
weight: 13
url: /vi/java/onenote-tag-operations/add-text-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm nút văn bản có thẻ trong OneNote - Aspose.Note

## Giới thiệu
Trong hướng dẫn này, chúng ta sẽ khám phá cách thêm nút văn bản có thẻ trong OneNote bằng Aspose.Note cho Java. Aspose.Note là một thư viện Java mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft OneNote theo chương trình. Thêm các nút văn bản bằng thẻ là một yêu cầu phổ biến trong xử lý tài liệu và Aspose.Note đơn giản hóa tác vụ này.
## Điều kiện tiên quyết
Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:
- Kiến thức cơ bản về lập trình Java.
-  Aspose.Note cho thư viện Java đã được cài đặt. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/note/java/).
- Môi trường phát triển tích hợp (IDE) được thiết lập để phát triển Java.
## Gói nhập khẩu
Bắt đầu bằng cách nhập các gói cần thiết cho dự án Java của bạn. Trong mã của bạn, hãy bao gồm các mục nhập sau:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## Bước 1: Tạo đối tượng tài liệu
Khởi tạo một đối tượng lớp Tài liệu để thể hiện tài liệu OneNote:
```java
// Đường dẫn đến thư mục tài liệu.
String dataDir = "Your Document Directory";
//Tạo một đối tượng của lớp Tài liệu
Document doc = new Document();
```
## Bước 2: Khởi tạo đối tượng lớp trang
Khởi tạo một đối tượng lớp Trang để thể hiện trang trong tài liệu:
```java
// Khởi tạo đối tượng lớp Trang
Page page = new Page();
```
## Bước 3: Khởi tạo đối tượng lớp Outline
Khởi tạo một đối tượng lớp Outline để cấu trúc nội dung trong trang:
```java
// Khởi tạo đối tượng lớp Outline
Outline outline = new Outline();
```
## Bước 4: Khởi tạo đối tượng lớp OutlineElement
Khởi tạo một đối tượng lớp OutlineElement để thể hiện một phần tử trong đường viền:
```java
// Khởi tạo đối tượng lớp OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Bước 5: Tùy chỉnh kiểu văn bản
Thiết lập kiểu cho nút văn bản, chẳng hạn như màu phông chữ, tên và kích thước:
```java
// Tùy chỉnh kiểu văn bản
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## Bước 6: Tạo đối tượng RichText
Tạo một đối tượng RichText và nối thêm văn bản mong muốn vào nó:
```java
// Tạo đối tượng RichText
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## Bước 7: Thêm thẻ ghi chú
Thêm thẻ ghi chú, chẳng hạn như ngôi sao màu vàng, vào văn bản:
```java
// Thêm thẻ ghi chú
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## Bước 8: Thêm nút văn bản
Thêm nút văn bản vào phần tử phác thảo:
```java
// Thêm nút văn bản
outlineElem.appendChildLast(text);
```
## Bước 9: Thêm phần tử phác thảo vào phác thảo
Thêm phần tử phác thảo vào phác thảo:
```java
// Thêm nút phần tử phác thảo
outline.appendChildLast(outlineElem);
```
## Bước 10: Thêm dàn ý vào trang
Thêm dàn ý vào trang:
```java
// Thêm nút phác thảo
page.appendChildLast(outline);
```
## Bước 11: Thêm trang vào tài liệu
Thêm trang vào tài liệu:
```java
// Thêm nút trang
doc.appendChildLast(page);
```
## Bước 12: Lưu tài liệu OneNote
Lưu tài liệu OneNote vào thư mục được chỉ định:
```java
// Lưu tài liệu OneNote
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
Chúc mừng! Bạn đã thêm thành công nút văn bản có thẻ trong OneNote bằng Aspose.Note for Java.
## Phần kết luận
Trong hướng dẫn này, chúng tôi đã trình bày quy trình từng bước thêm nút văn bản có thẻ trong OneNote bằng thư viện Aspose.Note for Java. Thư viện mạnh mẽ này đơn giản hóa các tác vụ xử lý tài liệu, giúp nhà phát triển dễ dàng thao tác với các tệp OneNote theo chương trình.
## Các câu hỏi thường gặp
### Câu hỏi: Tôi có thể sử dụng Aspose.Note cho Java với các thư viện Java khác không?
Trả lời: Có, Aspose.Note for Java có thể được tích hợp liền mạch với các thư viện Java khác để nâng cao khả năng xử lý tài liệu.
### Câu hỏi: Có bản dùng thử miễn phí dành cho Aspose.Note dành cho Java không?
 Đ: Có, bạn có thể truy cập bản dùng thử miễn phí[đây](https://releases.aspose.com/).
### Câu hỏi: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.Note cho Java?
Trả lời: Bạn có thể tìm kiếm sự hỗ trợ từ cộng đồng Aspose.Note[diễn đàn](https://forum.aspose.com/c/note/28).
### Câu hỏi: Aspose.Note dành cho Java có sẵn giấy phép tạm thời không?
 Đáp: Có, bạn có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).
### Câu hỏi: Tôi có thể tìm tài liệu về Aspose.Note cho Java ở đâu?
 A: Tài liệu có sẵn[đây](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
