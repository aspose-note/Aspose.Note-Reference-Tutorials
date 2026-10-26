---
date: 2026-10-26
description: Tìm hiểu cách thêm checkboxes onenote khi tạo meeting notes template
  với Aspose.Note for Java, và tùy chỉnh font style onenote một cách dễ dàng.
keywords:
- add checkboxes onenote
- generate meeting notes template
- customize font style onenote
- create outline onenote
lastmod: 2026-10-26
linktitle: Tạo Meeting Notes Template với Aspose.Note for Java – Tạo Outline trong
  OneNote
og_description: Tìm hiểu cách thêm checkboxes onenote khi tạo meeting notes template
  với Aspose.Note for Java, và tùy chỉnh font style onenote một cách dễ dàng.
og_image_alt: 'Developer guide: add checkboxes onenote and generate meeting notes
  template using Aspose.Note for Java'
og_title: Thêm checkboxes onenote và tạo notes template trong Java
schemas:
- author: Aspose
  dateModified: '2026-10-26'
  description: Learn how to add checkboxes onenote while generating a meeting notes
    template with Aspose.Note for Java, and customize font style onenote easily.
  headline: Add checkboxes onenote and create notes template in Java
  type: TechArticle
- questions:
  - answer: You can create a bulleted list and manually mark items, but using `NoteCheckBox`
      provides interactive checkboxes that sync with OneNote’s UI.
    question: How do I add a checklist to OneNote without using checkboxes?
  - answer: Absolutely. Just change the date formatting or pass a custom title string
      to reuse the same structure for each week.
    question: Can I use this template to create a meeting agenda template for weekly
      repeats?
  - answer: Define `ParagraphStyle` objects with your corporate font name, size, and
      color, then apply them to each `RichText` element as shown in Step 1.
    question: What is the best way to customize font style onenote for branding?
  - answer: Yes. After saving the OneNote file, you can load it with Aspose.Note and
      export to PDF using `Document.save("output.pdf", SaveFormat.Pdf)`.
    question: Does Aspose.Note support exporting the outline to PDF?
  - answer: You can set the checkbox state by adding a `NoteCheckBox` tag with the
      `Checked` property set to `true`.
    question: Is there a way to programmatically mark a checkbox as completed?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote
- Aspose.Note
- Java
- meeting notes template
- checkboxes
title: Thêm checkboxes onenote và tạo notes template trong Java
url: /vi/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm hộp kiểm onenote và tạo mẫu ghi chú trong Java

## Giới thiệu
Trong môi trường cộng tác hiện đại, **add checkboxes onenote** nhanh chóng và tạo ra một mẫu ghi chú cuộc họp được hoàn thiện mà không cần định dạng thủ công. Aspose.Note for Java cung cấp cho bạn toàn quyền kiểm soát tiêu đề trang, cấu trúc đề mục phân cấp, kiểu chữ và các hộp kiểm tương tác, cho phép bạn tạo một agenda có thể tái sử dụng trong vài giây. Hướng dẫn này sẽ đưa bạn qua từng bước — từ việc nhập các lớp cần thiết đến lưu tệp OneNote cuối cùng — để bạn có thể tập trung vào nội dung cuộc họp, không phải công việc UI tẻ nhạt.

## Câu trả lời nhanh
- **“add checkboxes onenote” có nghĩa là gì?** Nó có nghĩa là chèn các hộp kiểm tương tác vào một đề mục OneNote một cách lập trình, giống như giao diện người dùng làm.  
- **Thư viện nào hỗ trợ việc này?** Aspose.Note for Java cung cấp API đầy đủ.  
- **Tôi có thể thêm hộp kiểm vào đề mục không?** Có – sử dụng `NoteCheckBox.createBlueCheckBox()` hoặc các biến thể màu khác.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí hoạt động cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Java 8 trở lên.

## add checkboxes onenote là gì?
Thêm hộp kiểm onenote chèn một thẻ `NoteCheckBox` vào phần tử `RichText`, biến một dòng văn bản thông thường thành một hộp tick tương tác mà người dùng có thể đánh dấu hoặc bỏ đánh dấu trực tiếp trong giao diện OneNote, duy trì trạng thái hộp kiểm trên các thiết bị và đảm bảo tính nhất quán.

## Tại sao nên sử dụng Aspose.Note để tạo mẫu ghi chú cuộc họp?
Aspose.Note xử lý **hơn 50 định dạng đầu vào và đầu ra** và có thể xử lý các trang với **lên tới 500 dòng** mà không cần tải toàn bộ tài liệu vào bộ nhớ, mang lại việc tạo agenda lớn nhanh chóng và tiết kiệm bộ nhớ. Nó cũng cung cấp một API linh hoạt cho việc tạo kiểu, hỗ trợ ký tự Unicode, và tích hợp liền mạch với các thư viện Aspose khác, làm cho nó trở thành lựa chọn lý tưởng cho quy trình tài liệu cuộc họp quy mô doanh nghiệp.

## Yêu cầu trước
- Hiểu biết cơ bản về lập trình Java.  
- Thư viện Aspose.Note for Java đã được cài đặt. Bạn có thể **download Aspose.Note for Java** từ trang phát hành chính thức của Aspose.Note for Java: [Aspose.Note for Java release page](https://releases.aspose.com/note/java/).  
- Một IDE như Eclipse hoặc IntelliJ IDEA.  

## Nhập các gói
Các lớp `Document`, `Outline`, `ParagraphStyle`, `RichText`, và `NoteCheckBox` là các khối xây dựng cốt lõi.  

`Document` đại diện cho toàn bộ tệp OneNote trong bộ nhớ, cho phép thêm hoặc sửa đổi các trang và nội dung.  
`Outline` mô hình cấu trúc danh sách phân cấp hiển thị trong OneNote, cho phép các điểm đầu dòng và đánh số lồng nhau.  
`ParagraphStyle` định nghĩa các thuộc tính phông chữ và đoạn văn có thể tái sử dụng, có thể áp dụng cho nhiều phần tử `RichText`.  
`RichText` chứa nội dung văn bản thực tế của một đoạn và có thể chứa các thẻ như `NoteCheckBox`.  
`NoteCheckBox` tạo một thẻ hộp kiểm tương tác có thể gắn vào đoạn `RichText`.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Bước 1: tạo cấu trúc tài liệu
Đầu tiên, khởi tạo một `Document`, đặt tiêu đề trang, và định nghĩa hai đối tượng `ParagraphStyle` có thể tái sử dụng — một cho tiêu đề và một cho nội dung chính.  

Các đối tượng `ParagraphStyle` cho phép bạn áp dụng cùng một họ phông, kích thước và màu cho nhiều đoạn mà không cần lặp lại mã.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*Những gì chúng tôi đã làm:*  
- Định nghĩa `headerStyle` cho tiêu đề và `bodyStyle` cho văn bản thường.  
- Tạo một `Document` và thêm một `Title` bao gồm ngày hiện tại, cung cấp cho trang một tiêu đề rõ ràng.

## Bước 2: phác thảo các điểm quan trọng
Tiếp theo, thêm một đối tượng `Outline` vào trang và điền nó với các phần như “Agenda”, “Discussion Items”, và “Action Items”.  

Đối tượng `Outline` đại diện cho danh sách phân cấp bạn thấy trong OneNote. Sử dụng `createListNumberingStyle` chúng tôi tạo một danh sách đánh số có thể khởi động lại cho mỗi phần mới.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*Lý do điều này quan trọng:*  
- Cấu trúc đề mục phản ánh cách bạn gõ thủ công trong OneNote, đảm bảo tính nhất quán trên tất cả các trang được tạo.  
- Kiểu đánh số giữ cho mỗi phần agenda gọn gàng và dễ theo dõi.

## Bước 3: làm nổi bật các mục hành động (cách thêm hộp kiểm)
Các mục hành động cần một dấu hiệu trực quan. Bằng cách gắn thẻ `NoteCheckBox` vào mỗi phần tử `RichText`, bạn kích hoạt **add checkboxes onenote** trực tiếp trong đề mục.  

`NoteCheckBox.createBlueCheckBox()` tạo một hộp tick màu xanh; các màu khác cũng có sẵn để tùy chỉnh thương hiệu.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*Mẹo chuyên nghiệp:* Sử dụng `NoteCheckBox.createBlueCheckBox()` cho hộp tick màu xanh; các màu khác có sẵn nếu bạn cần phong cách trực quan khác.

## Bước 4: tùy chỉnh kiểu phông chữ onenote
Để ghi chú cuộc họp phù hợp với thương hiệu, áp dụng các đối tượng `ParagraphStyle` đã định nghĩa trước cho mỗi phần tử `RichText`.  

Việc thiết lập các thuộc tính `FontName`, `FontSize`, và `FontColor` đảm bảo trang được tạo phù hợp với hướng dẫn phong cách công ty của bạn.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Bước 5: lưu tài liệu
Cuối cùng, ghi tệp OneNote ra đĩa. Tệp có thể được mở trực tiếp trong ứng dụng OneNote desktop, và bạn cũng có thể chuyển đổi sang PDF sau nếu cần.

*Câu trả lời trực tiếp:* Gọi `document.save("MeetingTemplate.one")` — API sẽ ghi một tệp OneNote hoàn toàn tương thích, mở ngay lập tức trong client OneNote.

## Các vấn đề thường gặp và giải pháp
| Vấn đề | Giải pháp |
|-------|----------|
| **Checkboxes not appearing** | Đảm bảo bạn đã gọi `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` sau khi thiết lập kiểu đoạn. |
| **Fonts look different in OneNote** | Xác minh rằng tên phông (ví dụ, “Calibri”) đã được cài đặt trên máy nơi OneNote mở tệp. |
| **Outline not indented** | Điều chỉnh `setVerticalOffset` và `setHorizontalOffset` trên đối tượng `Outline`. |
| **Numbering restarts unexpectedly** | Sử dụng `restartFlag` đúng cách; đặt thành `true` chỉ cho danh sách đầu tiên trong một phần mới. |

## Câu hỏi thường gặp
### Làm thế nào để thêm hộp kiểm onenote?
Tải một phần tử `RichText`, sau đó gọi `richText.getTags().add(NoteCheckBox.createBlueCheckBox())`. Thẻ này biến dòng thành một hộp kiểm tương tác mà người dùng có thể đánh dấu trong OneNote.

### Tôi có thể tùy chỉnh kiểu phông chữ trong ghi chú cuộc họp không?
Có. Tạo các đối tượng `ParagraphStyle` với `FontName`, `FontSize`, và `FontColor` mong muốn, sau đó gán chúng cho mỗi phần tử `RichText` như đã minh họa ở Bước 1.

### Aspose.Note có tương thích với các thư viện Java khác không?
Aspose.Note hoạt động cùng với các sản phẩm Aspose khác (PDF, Cells, Slides) và các thư viện Java tiêu chuẩn, cho phép bạn chuỗi các thao tác như chuyển đổi tệp OneNote đã tạo sang PDF.

### Làm thế nào để thêm các phần bổ sung vào ghi chú cuộc họp?
Áp dụng cùng một mẫu: tạo một nút `Outline` mới, áp dụng `ParagraphStyle`, và tùy chọn thêm hộp kiểm. API có thể lặp lại hoàn toàn cho bất kỳ số lượng phần nào.

### Có những lưu ý về giấy phép nào cho Aspose.Note không?
Tham khảo [Aspose.Note documentation](https://reference.aspose.com/note/java/) để biết chi tiết về giấy phép. Bản dùng thử miễn phí đủ cho phát triển; giấy phép thương mại cần thiết cho triển khai sản xuất.

### Có phiên bản dùng thử cho Aspose.Note không?
Có, bạn có thể truy cập **trang tải bản dùng thử miễn phí của Aspose.Note**: [Aspose.Note trial download page](https://releases.aspose.com/).

## FAQ
**Q: Làm thế nào để thêm danh sách kiểm tra vào OneNote mà không sử dụng hộp kiểm?**  
A: Bạn có thể tạo một danh sách có dấu đầu dòng và đánh dấu thủ công các mục, nhưng sử dụng `NoteCheckBox` cung cấp các hộp kiểm tương tác đồng bộ với giao diện UI của OneNote.

**Q: Tôi có thể sử dụng mẫu này để tạo agenda họp hàng tuần không?**  
A: Chắc chắn. Chỉ cần thay đổi định dạng ngày hoặc truyền một chuỗi tiêu đề tùy chỉnh để tái sử dụng cùng cấu trúc cho mỗi tuần.

**Q: Cách tốt nhất để tùy chỉnh kiểu phông chữ onenote cho thương hiệu là gì?**  
A: Định nghĩa các đối tượng `ParagraphStyle` với tên phông, kích thước và màu sắc của công ty, sau đó áp dụng chúng cho mỗi phần tử `RichText` như đã trình bày ở Bước 1.

**Q: Aspose.Note có hỗ trợ xuất đề mục ra PDF không?**  
A: Có. Sau khi lưu tệp OneNote, bạn có thể tải nó bằng Aspose.Note và xuất ra PDF bằng `Document.save("output.pdf", SaveFormat.Pdf)`.

**Q: Có cách nào để lập trình đánh dấu một hộp kiểm là đã hoàn thành không?**  
A: Bạn có thể đặt trạng thái hộp kiểm bằng cách thêm thẻ `NoteCheckBox` với thuộc tính `Checked` được đặt thành `true`.

---

**Last Updated:** 2026-10-26  
**Tested With:** Aspose.Note for Java 24.11 (latest at time of writing)  
**Author:** Aspose

## Các hướng dẫn liên quan

- [Add Tags to OneNote – Create Tagged OneNote Document with Aspose.Note](/note/java/onenote-tag-operations/)
- [How to Customize OneNote Styles with Aspose.Note for Java](/note/java/onenote-styles/)
- [Create OneNote Document Java – Aspose Note Java Tutorial](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}