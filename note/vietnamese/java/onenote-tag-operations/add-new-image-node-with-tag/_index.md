---
title: Thêm nút hình ảnh mới có thẻ trong OneNote - Aspose.Note
linktitle: Thêm nút hình ảnh mới có thẻ trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Tìm hiểu cách thêm nút hình ảnh mới bằng thẻ trong OneNote bằng Aspose.Note for Java. Nâng cao kỹ năng lập trình Java của bạn một cách dễ dàng.
weight: 10
url: /vi/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm nút hình ảnh mới có thẻ trong OneNote - Aspose.Note

## Giới thiệu
Trong lĩnh vực lập trình Java, Aspose.Note nổi bật như một công cụ mạnh mẽ để xử lý các tài liệu OneNote một cách dễ dàng. Nếu bạn đang tìm cách nâng cao kỹ năng của mình và tìm hiểu cách thêm nút hình ảnh mới bằng thẻ trong OneNote bằng Aspose.Note, thì bạn đã đến đúng nơi. Hướng dẫn từng bước này sẽ hướng dẫn bạn thực hiện quy trình, đảm bảo bạn nắm bắt kỹ lưỡng từng khái niệm.
## Điều kiện tiên quyết
Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có mọi thứ mình cần:
1.  Aspose.Note for Java: Đảm bảo bạn đã cài đặt thư viện Aspose.Note. Nếu không, bạn có thể tải xuống[đây](https://releases.aspose.com/note/java/).
2. Môi trường phát triển Java: Đảm bảo bạn đã thiết lập môi trường phát triển Java đang hoạt động trên máy của mình.
Bây giờ chúng ta đã có các điều kiện tiên quyết, hãy chuyển sang các bước tiếp theo.
## Gói nhập khẩu
Trong dự án Java của bạn, hãy bắt đầu bằng cách nhập các gói cần thiết:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Bước 1: Tạo đối tượng tài liệu
```java
// Đường dẫn đến thư mục tài liệu.
String dataDir = "Your Document Directory";
// tạo một đối tượng của lớp Tài liệu
Document doc = new Document();
```
## Bước 2: Khởi tạo đối tượng lớp trang
```java
// khởi tạo đối tượng lớp Trang
Page page = new Page();
```
## Bước 3: Khởi tạo đối tượng lớp Outline
```java
// khởi tạo đối tượng lớp Outline
Outline outline = new Outline();
```
## Bước 4: Khởi tạo đối tượng lớp OutlineElement
```java
// khởi tạo đối tượng lớp OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Bước 5: Tải và chèn hình ảnh
```java
// tải một hình ảnh
Image image = new Image(null, dataDir + "Input.jpg");
// chèn hình ảnh vào nút tài liệu
outlineElem.appendChildLast(image);
```
## Bước 6: Thêm thẻ ghi chú vào hình ảnh
```java
// thêm thẻ ghi chú ngôi sao màu vàng vào hình ảnh
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Bước 7: Thêm nút phần tử phác thảo
```java
// thêm nút phần tử phác thảo
outline.appendChildLast(outlineElem);
```
## Bước 8: Thêm nút phác thảo
```java
// thêm nút phác thảo
page.appendChildLast(outline);
```
## Bước 9: Thêm nút trang
```java
// thêm nút trang
doc.appendChildLast(page);
```
## Bước 10: Lưu tài liệu OneNote
```java
// lưu tài liệu OneNote dưới dạng PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Chúc mừng! Bạn đã thêm thành công nút hình ảnh mới có thẻ trong OneNote bằng Aspose.Note for Java.
## Phần kết luận
 Làm chủ Aspose.Note cho Java mở ra những khả năng thú vị trong thao tác tài liệu OneNote. Bằng cách làm theo hướng dẫn này, bạn đã đạt được kỹ năng thực tế có thể áp dụng cho nhiều dự án khác nhau. Tiếp tục khám phá tài liệu Aspose.Note[đây](https://reference.aspose.com/note/java/)để biết thêm các tính năng và khả năng nâng cao.
## Câu hỏi thường gặp
### Tôi có thể tìm tài liệu Aspose.Note ở đâu?
 Bạn có thể tìm thấy tài liệu[đây](https://reference.aspose.com/note/java/).
### Làm cách nào để tải xuống Aspose.Note cho Java?
 Bạn có thể tải xuống từ trang phát hành[đây](https://releases.aspose.com/note/java/).
### Có bản dùng thử miễn phí không?
 Có, bạn có thể truy cập bản dùng thử miễn phí[đây](https://releases.aspose.com/).
### Tôi có thể nhận hỗ trợ cho Aspose.Note ở đâu?
 Truy cập diễn đàn cộng đồng[đây](https://forum.aspose.com/c/note/28) để hỗ trợ.
### Tôi có cần giấy phép tạm thời không?
 Nếu được yêu cầu, bạn có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
