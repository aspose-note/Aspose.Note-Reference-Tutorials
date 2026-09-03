---
date: 2026-01-28
description: Học cách tạo dàn nội dung trong OneNote, thêm thẻ vào OneNote và tạo
  PDF từ OneNote bằng Aspose.Note cho Java.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: Tạo Đề mục trong OneNote và Thêm Thẻ – Aspose.Note
url: /vi/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo Dàn Bài trong OneNote và Thêm Thẻ – Aspose.Note

## Giới thiệu
Bạn có muốn **tạo dàn bài trong OneNote** và tăng cường hợp tác bằng các thẻ sử dụng Java không? Aspose.Note for Java giúp bạn dễ dàng thêm thẻ, cấu trúc ghi chú và thậm chí **tạo PDF từ OneNote**. Trong hướng dẫn này, chúng tôi sẽ đi qua từng bước, giải thích *tại sao* mỗi phần quan trọng và chỉ cho bạn cách tạo ra một tệp PDF hoàn chỉnh ở cuối.

## Câu trả lời nhanh
- **“tạo dàn bài trong OneNote” có nghĩa là gì?** Nó xây dựng một cấu trúc phân cấp (dàn bài) để tổ chức nội dung như tiêu đề và các phần phụ.  
- **Thư viện nào thêm thẻ vào OneNote?** Aspose.Note for Java cung cấp lớp `NoteTag` cho các dấu hiệu trực quan.  
- **Tôi có thể xuất kết quả ra PDF không?** Có – sử dụng `SaveFormat.Pdf` để **tạo PDF từ OneNote**.  
- **Có cần giấy phép cho môi trường sản xuất không?** Một giấy phép tạm thời có sẵn cho việc thử nghiệm; giấy phép đầy đủ cần thiết cho sử dụng thương mại.  
- **Các yêu cầu chính là gì?** Đã cài đặt JDK, thư viện Aspose.Note for Java và kiến thức cơ bản về Java.

## “tạo dàn bài trong OneNote” là gì?
Tạo dàn bài trong OneNote có nghĩa là thêm các đối tượng `Outline` và `OutlineElement` xác định cấu trúc dạng cây cho ghi chú của bạn. Cấu trúc này cho phép bạn thu gọn, mở rộng và sắp xếp thông tin giống như các tiêu đề trong tài liệu.

## Tại sao cần thêm thẻ vào OneNote?
Các thẻ như sao, dấu kiểm hoặc biểu tượng tùy chỉnh cung cấp dấu hiệu trực quan cho người đọc, cải thiện khả năng tìm kiếm và giúp các nhóm ưu tiên các mục. Với Aspose.Note, bạn có thể gắn một `NoteTag` vào bất kỳ đoạn văn bản nào một cách lập trình.

## Yêu cầu trước
Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:
- Java Development Kit (JDK) đã được cài đặt.
- Thư viện Aspose.Note for Java đã tải về. Bạn có thể tải [tại đây](https://releases.aspose.com/note/java/).
- Kiến thức cơ bản về lập trình Java.

## Nhập khẩu các gói
Đảm bảo bạn nhập các gói cần thiết để khởi động dự án:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
Hãy phân tích đoạn mã trên thành các bước chi tiết.

## Bước 1: Thiết lập Document và Page
Bắt đầu bằng cách tạo một đối tượng `Document` mới và khởi tạo một đối tượng `Page`:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```
Ở đây, chúng ta đặt đường dẫn tới thư mục tài liệu, tạo một `Document` mới và khởi tạo một `Page`.

## Bước 2: Tạo Outline
Tiếp theo, tạo một đối tượng `Outline` để cấu trúc nội dung:
```java
Outline outline = new Outline();
```
Outline cung cấp cấu trúc phân cấp cho tài liệu, giúp dễ dàng **tạo dàn bài trong OneNote** và giữ thông tin được tổ chức.

## Bước 3: Khởi tạo OutlineElement và ParagraphStyle
Bây giờ, khởi tạo một `OutlineElement` và thiết lập `ParagraphStyle` cho định dạng văn bản:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
`OutlineElement` đại diện cho một phần tử trong dàn bài, và `ParagraphStyle` xác định các thuộc tính định dạng văn bản.

## Bước 4: Thêm RichText với NoteTag
Tạo một đối tượng `RichText`, nối văn bản OneNote của bạn và thêm một `NoteTag`:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
`RichText` cho phép bạn chèn văn bản có định dạng, và `NoteTag` **thêm thẻ vào OneNote** như một dấu hiệu trực quan.

## Bước 5: Xây dựng cấu trúc Outline
Thêm nút văn bản, nút OutlineElement và nút Outline để xây dựng cấu trúc tài liệu:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
Bước này đảm bảo nội dung của bạn được sắp xếp trong tài liệu, hoàn thiện quy trình **tạo dàn bài trong OneNote**.

## Bước 6: Lưu Document
Lưu tài liệu ở định dạng PDF, điều này **tạo PDF từ OneNote**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
Bây giờ, tài liệu OneNote của bạn với các thẻ đã được lưu dưới dạng PDF.

Bằng cách thực hiện các bước trên, bạn có thể dễ dàng nâng cao tài liệu OneNote bằng Aspose.Note for Java.

## Kết luận
Trong hướng dẫn này, chúng ta đã khám phá cách **tạo dàn bài trong OneNote**, thêm thẻ vào OneNote và sau đó **tạo PDF từ OneNote** bằng Aspose.Note for Java. Sử dụng Java cho phép bạn kiểm soát toàn bộ cấu trúc ghi chú, thẻ trực quan và các tùy chọn xuất, giúp ghi chú của bạn trở nên có tổ chức và dễ chia sẻ hơn.

## Câu hỏi thường gặp
### 1. Tôi có thể dùng Aspose.Note for Java với các ngôn ngữ lập trình khác không?
Aspose.Note chủ yếu hỗ trợ Java, nhưng cũng có các phiên bản cho .NET.

### 2. Aspose.Note for Java có phù hợp cho người mới bắt đầu không?
Có, Aspose.Note for Java cung cấp tài liệu và hỗ trợ chi tiết, giúp người mới và các nhà phát triển có kinh nghiệm đều có thể sử dụng dễ dàng.

### 3. Làm sao để tôi có được giấy phép tạm thời cho Aspose.Note for Java?
Bạn có thể lấy giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

### 4. Tôi có thể tìm hỗ trợ bổ sung ở đâu?
Đối với bất kỳ câu hỏi hay hỗ trợ nào, hãy truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28).

### 5. Có bản dùng thử miễn phí không?
Có, bạn có thể khám phá bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

**Câu hỏi & Trả lời bổ sung**

**Hỏi: Tôi có thể tùy chỉnh biểu tượng thẻ không?**  
Đáp: Có – Aspose.Note cung cấp nhiều biểu tượng được định sẵn qua `TagIcon` và cũng cho phép sử dụng hình ảnh tùy chỉnh.

**Hỏi: Làm sao để thay đổi cài đặt xuất PDF?**  
Đáp: Sử dụng `PdfSaveOptions` để điều chỉnh chất lượng hình ảnh, nén và bảo mật trước khi gọi `doc.save`.

**Hỏi: Có thể thêm nhiều thẻ vào cùng một đoạn văn bản không?**  
Đáp: Hoàn toàn có thể. Gọi `text.getTags().add()` nhiều lần với các thể hiện `NoteTag` khác nhau.

---

**Cập nhật lần cuối:** 2026-01-28  
**Kiểm tra với:** Aspose.Note for Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}