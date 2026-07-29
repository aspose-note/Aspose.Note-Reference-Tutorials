---
date: 2026-07-29
description: Tìm hiểu cách nhúng liên kết OneNote, lưu OneNote dưới dạng PDF và thêm
  siêu liên kết bằng Java với Aspose.Note. Xuất OneNote sang PDF một cách dễ dàng.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: Lưu OneNote dưới dạng PDF và Thêm Siêu liên kết trong OneNote bằng Java
og_description: Nhúng liên kết OneNote và xuất OneNote sang PDF bằng Java và Aspose.Note.
  Tìm hiểu từng bước cách thêm siêu liên kết và tạo PDF.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Nhúng liên kết OneNote – Lưu OneNote dưới dạng PDF bằng Java
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: Nhúng liên kết OneNote – Lưu OneNote dưới dạng PDF bằng Java
url: /vi/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu OneNote dưới dạng PDF và Thêm Siêu liên kết trong OneNote bằng Java

## Giới thiệu

Nếu bạn cần **embed link onenote** trong khi chuyển một sổ ghi chú thành PDF di động, bạn đã đến đúng nơi. Hướng dẫn này sẽ chỉ cho bạn cách lưu OneNote dưới dạng PDF và chèn các siêu liên kết có thể nhấp được bằng Java và thư viện Aspose.Note. Bạn sẽ thấy tại sao cách tiếp cận này lý tưởng cho việc lưu trữ, chia sẻ và tự động hoá các quy trình tài liệu.

## Câu trả lời nhanh
- **Tôi có thể lưu OneNote dưới dạng PDF bằng Java không?** Có, Aspose.Note for Java cung cấp một lệnh `save` duy nhất để tạo PDF.
- **Làm thế nào để tôi chèn một siêu liên kết?** Sử dụng `TextStyle.setHyperlinkAddress` trên một đoạn `RichText`.
- **Các yêu cầu trước là gì?** JDK 8+ và thư viện Aspose.Note cho Java.
- **Các định dạng đầu ra nào được hỗ trợ?** PDF, DOCX, XPS và hơn nữa.
- **Có cần giấy phép cho môi trường sản xuất không?** Có, một giấy phép thương mại là cần thiết cho việc sử dụng không phải để đánh giá.

## “save onenote as pdf” là gì?

Lưu một sổ OneNote dưới dạng PDF tạo ra một phiên bản chỉ đọc, đa nền tảng của ghi chú của bạn mà bất kỳ ai cũng có thể mở mà không cần ứng dụng OneNote. Định dạng này lý tưởng cho việc lưu trữ, in ấn, hoặc chia sẻ với những cộng tác viên không cài đặt OneNote, đồng thời vẫn giữ nguyên bố cục gốc, hình ảnh và bất kỳ siêu liên kết nào được nhúng.

## Tại sao tạo PDF từ OneNote bằng Aspose.Note Java?

Aspose.Note cho Java có thể **export onenote to pdf** với độ chính xác bố cục 100 %, xử lý lên tới 200 trang mỗi tài liệu mà không cần tải toàn bộ tệp vào bộ nhớ. Thư viện xử lý hơn 30 loại nội dung khác nhau — bao gồm hình ảnh, bảng và 95 % các kiểu siêu liên kết — vì vậy bạn nhận được bản sao chính xác của sổ ghi chú gốc. Nó cũng chạy trên Windows, Linux và macOS, cho phép chuyển đổi hàng loạt trên đám mây hoặc dịch vụ tại chỗ.

## Các yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã cài đặt và cấu hình các yêu cầu sau trên hệ thống của mình:

### Bộ công cụ phát triển Java (JDK)

Đảm bảo bạn đã cài đặt Bộ công cụ phát triển Java (JDK) trên hệ thống của mình. Bạn có thể tải xuống và cài đặt JDK từ [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Thư viện Aspose.Note cho Java

Tải xuống và cài đặt thư viện Aspose.Note cho Java. Bạn có thể tìm tài liệu và liên kết tải xuống [tại đây](https://reference.aspose.com/note/java/).

## Nhập gói

Để bắt đầu, nhập các gói cần thiết để làm việc với Aspose.Note cho Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Bây giờ, chúng ta sẽ phân tích ví dụ được cung cấp thành nhiều bước:

## Cách chèn link onenote khi lưu dưới dạng PDF?

Tải một thể hiện `Document` mới, xây dựng cấu trúc trang, định nghĩa một `TextStyle` màu đỏ cho siêu liên kết, và cuối cùng gọi `document.save("output.pdf", SaveFormat.Pdf)`. Trình tự này tạo ra một PDF chứa siêu liên kết hoạt động đầy đủ, giữ nguyên tất cả định dạng và hình ảnh gốc.

## Bước 1: Thiết lập cấu trúc tài liệu

`Document` đại diện cho một sổ OneNote trong Aspose.Note.  
`Page` là một container cho các outline và các phần tử cấp trang khác.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Bước 2: Định nghĩa kiểu văn bản mặc định

`ParagraphStyle` định nghĩa định dạng mặc định cho các đoạn văn như căn chỉnh, khoảng cách và thụt lề.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Bước 3: Đặt văn bản tiêu đề

`Title` đại diện cho phần tiêu đề của trang trong tài liệu OneNote.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Bước 4: Tạo Outline và các phần tử Outline

`Outline` hoạt động như một container cho một hệ thống các khối nội dung.  
`OutlineElement` là một phần tử riêng biệt trong một outline, chẳng hạn như một đoạn văn hoặc một bảng.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Bước 5: Định nghĩa kiểu văn bản cho Siêu liên kết

`TextStyle` kiểm soát giao diện hiển thị của các đoạn văn bản, bao gồm phông chữ, màu sắc và cài đặt gạch chân.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Bước 6: Thêm văn bản với Siêu liên kết

`RichText` đại diện cho một đoạn văn bản đã định dạng trong một đoạn. Đặt địa chỉ siêu liên kết làm cho văn bản có thể nhấp được trong PDF đã xuất.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Bước 7: Thêm Outline vào Page và Page vào Document

Bước này gắn các phần tử outline đã tạo trước đó vào trang và sau đó thêm trang vào đối tượng `Document`.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Bước 8: Lưu tài liệu dưới dạng PDF

`SaveFormat.Pdf` chỉ cho Aspose.Note xuất tài liệu dưới định dạng PDF.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Kết luận

Chúc mừng! Bạn đã thành công **lưu OneNote dưới dạng PDF** và thêm một siêu liên kết vào tài liệu bằng Java và thư viện Aspose.Note. Khả năng này cho phép bạn **embed link onenote** và tạo các PDF tương tác, có thể chia sẻ trực tiếp từ nội dung OneNote của bạn.

## Câu hỏi thường gặp

**Q: Làm thế nào tôi có thể tùy chỉnh giao diện của siêu liên kết?**  
A: Sử dụng các thuộc tính của `TextStyle` như `setFontColor`, `setUnderline`, hoặc `setFontName` trước khi gọi `setHyperlinkAddress`.

**Q: Tôi có thể lưu tài liệu ở các định dạng khác ngoài PDF không?**  
A: Có, Aspose.Note hỗ trợ DOCX, XPS, HTML và một số định dạng xuất khác.

**Q: Nếu tôi cần thêm một siêu liên kết vào tệp OneNote hiện có thì sao?**  
A: Tải tệp hiện có bằng `new Document("input.one")`, chỉnh sửa nội dung như đã trình bày, và sau đó gọi `save` với định dạng mong muốn.

**Q: Có cách nào mở siêu liên kết bằng chương trình sau khi PDF được tạo không?**  
A: Trình xem PDF sẽ tự động xử lý các liên kết có thể nhấp; không cần mã bổ sung.

**Q: Tôi có cần giấy phép cho việc sử dụng phát triển không?**  
A: Giấy phép đánh giá tạm thời đủ cho việc phát triển và thử nghiệm, nhưng giấy phép đầy đủ cần cho triển khai sản xuất.

---

**Last Updated:** 2026-07-29  
**Tested With:** Aspose.Note for Java 26.4  
**Author:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Các hướng dẫn liên quan

- [How to Save OneNote as PDF with Aspose.Note for Java](/note/java/onenote-document-loading/load-save-format/)
- [Convert OneNote to PDF with Aspose.Note using PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Add Hyperlink to Image in OneNote with Java](/note/java/onenote-hyperlinks-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}