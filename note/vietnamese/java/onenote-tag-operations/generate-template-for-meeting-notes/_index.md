---
date: 2026-03-03
description: Học cách tạo dàn mục trong OneNote và tạo mẫu ghi chú cuộc họp với Aspose.Note
  cho Java. Tùy chỉnh kiểu phông chữ và thêm hộp kiểm một cách dễ dàng.
linktitle: Create Outline in OneNote – Meeting Notes Template
second_title: Aspose.Note Java API
title: Tạo Dàn Bài trong OneNote – Mẫu Ghi chú Cuộc họp
url: /vi/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo Dàn Bài trong OneNote – Mẫu Ghi Chú Cuộc Họp

## Giới thiệu
Trong thế giới ngày nay với nhịp độ nhanh, việc **tạo dàn bài trong OneNote** một cách hiệu quả là rất quan trọng để có tài liệu cuộc họp rõ ràng. Aspose.Note for Java cung cấp một cách mạnh mẽ để **tạo mẫu ghi chú cuộc họp** mà bạn có thể tùy chỉnh, thêm hộp kiểm và định dạng phông chữ chính xác theo nhu cầu. Trong hướng dẫn từng bước này, chúng tôi sẽ hướng dẫn cách xây dựng một mẫu agenda cuộc họp có thể tái sử dụng, giải thích **cách thêm hộp kiểm**, **thêm danh sách kiểm tra vào OneNote**, và **tùy chỉnh kiểu phông chữ onenote** để có giao diện chuyên nghiệp.

## Câu trả lời nhanh
- **“tạo dàn bài trong OneNote” có nghĩa là gì?** Có nghĩa là xây dựng một cấu trúc phân cấp (tiêu đề, phần, dấu đầu dòng) trong một tệp OneNote bằng mã.
- **Thư viện nào hỗ trợ việc này?** Aspose.Note for Java.  
- **Tôi có thể thêm hộp kiểm vào dàn bài không?** Có – sử dụng `NoteCheckBox.createBlueCheckBox()`.  
- **Tôi có cần giấy phép không?** Có phiên bản dùng thử miễn phí; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Java 8 trở lên.

## “tạo dàn bài trong OneNote” là gì?
Tạo dàn bài trong OneNote có nghĩa là định nghĩa một trang với tiêu đề, nhiều phần dàn bài, và tùy chọn đánh số danh sách hoặc hộp kiểm. Cấu trúc này giống như cách bạn tự tay gõ tiêu đề và dấu đầu dòng trong giao diện OneNote, nhưng được tạo tự động bằng mã.

## Tại sao nên dùng Aspose.Note cho mẫu agenda cuộc họp?
- **Nhất quán:** Mỗi cuộc họp đều bắt đầu với cùng một bố cục sạch sẽ.  
- **Tự động hoá:** Giảm việc gõ tay và đảm bảo mọi phần cần thiết (agenda, hành động, ghi chú) đều có mặt.  
- **Tùy chỉnh:** Thay đổi phông chữ, màu sắc và thêm hộp kiểm tương tác để theo dõi nhiệm vụ.  
- **Tích hợp:** Hoạt động với bất kỳ IDE Java nào và có thể kết hợp với các thư viện Aspose khác cho PDF, bảng tính, v.v.

## Yêu cầu trước
- Kiến thức cơ bản về lập trình Java.  
- Thư viện Aspose.Note for Java đã được cài đặt. Bạn có thể tải về [tại đây](https://releases.aspose.com/note/java/).  
- Một IDE như Eclipse hoặc IntelliJ IDEA.  

## Nhập khẩu các gói
Đầu tiên, nhập các lớp cần thiết. Đoạn mã này giữ nguyên như trong hướng dẫn gốc.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Bước 1: Tạo cấu trúc tài liệu
Chúng ta bắt đầu bằng việc xây dựng tài liệu, thiết lập tiêu đề và chuẩn bị các kiểu đoạn văn sẽ giúp **tùy chỉnh kiểu phông chữ onenote** sau này.

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
- Định nghĩa hai đối tượng `ParagraphStyle` (`headerStyle` cho tiêu đề, `bodyStyle` cho văn bản thường).  
- Tạo một `Document` và thêm một `Title` bao gồm ngày hiện tại, giúp trang có tiêu đề rõ ràng.

## Bước 2: Dàn bài các điểm quan trọng
Tiếp theo, chúng ta **tạo dàn bài trong OneNote** bằng cách thêm một đối tượng `Outline` và điền các phần như “Important”. Đây là nơi các mục agenda được đặt.

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

*Tại sao điều này quan trọng:*  
- Đối tượng `Outline` đại diện cho danh sách phân cấp mà bạn thấy trong OneNote.  
- Sử dụng `createListNumberingStyle` chúng ta tạo danh sách có đánh số có thể khởi động lại cho mỗi phần mới.

## Bước 3: Nổi bật các mục hành động (Cách thêm hộp kiểm)
Các mục hành động cần một dấu hiệu trực quan. Bằng cách gắn thẻ hộp kiểm vào mỗi phần tử `RichText`, chúng ta cho phép **cách thêm hộp kiểm** trực tiếp trong dàn bài.

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

*Mẹo chuyên nghiệp:* Sử dụng `NoteCheckBox.createBlueCheckBox()` cho hộp kiểm màu xanh; các màu khác cũng có sẵn nếu bạn cần phong cách trực quan khác.

## Bước 4: Lưu tài liệu
Cuối cùng, ghi tệp OneNote ra đĩa. Tệp này có thể mở trực tiếp trong ứng dụng OneNote trên máy tính.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Các vấn đề thường gặp và giải pháp
| Vấn đề | Giải pháp |
|-------|----------|
| **Hộp kiểm không hiển thị** | Đảm bảo bạn đã gọi `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` sau khi thiết lập kiểu đoạn văn. |
| **Phông chữ hiển thị khác trong OneNote** | Kiểm tra rằng tên phông chữ (ví dụ, “Calibri”) đã được cài đặt trên máy nơi OneNote mở tệp. |
| **Dàn bài không thụt lề** | Điều chỉnh `setVerticalOffset` và `setHorizontalOffset` trên đối tượng `Outline`. |
| **Đánh số khởi động lại không mong muốn** | Sử dụng `restartFlag` đúng cách; đặt `true` chỉ cho danh sách đầu tiên trong một phần mới. |

## Câu hỏi thường gặp
### Tôi có thể tùy chỉnh kiểu phông chữ trong ghi chú cuộc họp không?
Có, Aspose.Note cho phép bạn định nghĩa các kiểu phông chữ tùy chỉnh cho tiêu đề và nội dung.

### Aspose.Note có tương thích với các thư viện Java khác không?
Aspose.Note có thể được tích hợp liền mạch với các thư viện Java khác để mở rộng chức năng.

### Làm sao tôi thêm các phần bổ sung vào ghi chú cuộc họp?
Bạn có thể dễ dàng mở rộng cấu trúc dàn bài bằng cách làm theo cùng một mẫu đã trình bày trong hướng dẫn.

### Có những lưu ý về giấy phép cho Aspose.Note không?
Tham khảo [tài liệu Aspose.Note](https://reference.aspose.com/note/java/) để biết chi tiết về giấy phép.

### Có phiên bản dùng thử cho Aspose.Note không?
Có, bạn có thể truy cập [phiên bản dùng thử miễn phí tại đây](https://releases.aspose.com/).

## FAQ
**H: Làm sao tôi thêm danh sách kiểm tra vào OneNote mà không dùng hộp kiểm?**  
Đ: Bạn có thể tạo danh sách có dấu đầu dòng và đánh dấu thủ công, nhưng sử dụng `NoteCheckBox` cung cấp hộp kiểm tương tác đồng bộ với giao diện OneNote.

**H: Tôi có thể dùng mẫu này để tạo agenda cuộc họp hàng tuần không?**  
Đ: Chắc chắn. Chỉ cần thay đổi định dạng ngày hoặc truyền một chuỗi tiêu đề tùy chỉnh để tái sử dụng cùng cấu trúc mỗi tuần.

**H: Cách tốt nhất để **tùy chỉnh kiểu phông chữ onenote** cho thương hiệu là gì?**  
Đ: Định nghĩa các đối tượng `ParagraphStyle` với tên phông chữ công ty, kích thước và màu sắc, sau đó áp dụng chúng cho mỗi phần tử `RichText` như trong Bước 1.

**H: Aspose.Note có hỗ trợ xuất dàn bài ra PDF không?**  
Đ: Có. Sau khi lưu tệp OneNote, bạn có thể tải nó bằng Aspose.Note và xuất ra PDF bằng `Document.save("output.pdf", SaveFormat.Pdf)`.

**H: Có cách nào lập trình để đánh dấu hộp kiểm là đã hoàn thành không?**  
Đ: Bạn có thể đặt trạng thái hộp kiểm bằng cách thêm thẻ `NoteCheckBox` với thuộc tính `Checked` được đặt thành `true`.

---

**Cập nhật lần cuối:** 2026-03-03  
**Kiểm tra với:** Aspose.Note for Java 24.11 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}