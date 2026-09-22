---
date: 2026-08-18
description: Tìm hiểu cách lưu OneNote dưới dạng PDF trong Java bằng Aspose.Note,
  tạo tài liệu OneNote, định dạng văn bản phong phú và xuất ra PDF. Hướng dẫn nhanh
  từng bước.
keywords:
- save onenote as pdf
- export onenote to pdf
- format rich text java
lastmod: 2026-08-18
linktitle: Tạo tài liệu OneNote và lưu dưới dạng PDF trong Java
og_description: Tìm hiểu cách lưu OneNote dưới dạng PDF trong Java với Aspose.Note.
  Bài hướng dẫn này trình bày cách tạo tệp OneNote, áp dụng định dạng văn bản phong
  phú và xuất ra PDF.
og_image_alt: Screenshot of Java code converting OneNote to PDF using Aspose.Note
og_title: Lưu OneNote dưới dạng PDF trong Java – Hướng dẫn nhanh Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to save onenote as pdf in Java using Aspose.Note, create
    OneNote documents, format rich text, and export to PDF. Quick step‑by‑step guide.
  headline: How to save onenote as pdf in Java with Aspose.Note
  type: TechArticle
- description: Learn how to save onenote as pdf in Java using Aspose.Note, create
    OneNote documents, format rich text, and export to PDF. Quick step‑by‑step guide.
  name: How to save onenote as pdf in Java with Aspose.Note
  steps:
  - name: set up document and page
    text: '`Document` is Aspose.Note''s top‑level object that represents a OneNote
      file in memory. A `Page` object holds the visual elements of a OneNote page,
      such as text, images, and containers.'
  - name: create title with formatting
    text: '`ParagraphStyle` defines alignment, indentation, and spacing for a paragraph.
      `TextStyle` defines font, size, color and other character attributes for rich‑text
      runs.'
  - name: create rich text with formatting
    text: Here we build rich‑text content using several `TextStyle` objects to demonstrate
      **rich text formatting**.
  - name: add elements to page and document
    text: Combine the title and rich text into the page hierarchy so the document
      reflects the desired structure.
  - name: save document – export onenote to pdf
    text: Finally, export the OneNote document as a PDF file in one call, preserving
      all styling and layout.
  type: HowTo
- questions:
  - answer: Yes, you can adjust additional properties such as underline, strike‑through,
      and text alignment via the `TextStyle` and `ParagraphStyle` classes.
    question: Can I customize the font styles further?
  - answer: Absolutely. As long as the IDE supports standard Java development, you
      can add the Aspose.Note JAR to the project’s classpath.
    question: Is Aspose.Note for Java compatible with all Java IDEs?
  - answer: Yes, the same code works in servlet‑based or Spring Boot applications,
      enabling dynamic OneNote‑to‑PDF generation on the server side.
    question: Can I integrate this functionality into web applications?
  - answer: A commercial license is required for production use. A temporary license
      is available for evaluation and testing.
    question: Are there licensing requirements for using Aspose.Note for Java?
  - answer: It supports PDF, HTML, PNG, JPEG, and several other export formats, giving
      you flexibility to convert OneNote pages into the format you need.
    question: Does Aspose.Note for Java support other document formats besides OneNote?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote
- Aspose.Note
- Java document automation
title: Cách lưu OneNote dưới dạng PDF trong Java với Aspose.Note
url: /vi/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách lưu OneNote thành PDF trong Java với Aspose.Note

## Giới thiệu

Nếu bạn cần **lưu OneNote thành PDF** trong khi giữ nguyên mọi tiêu đề, kiểu đoạn văn và hình ảnh nhúng, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng ta sẽ đi qua việc tạo một tài liệu OneNote, áp dụng các kiểu văn bản giàu tùy chỉnh, và xuất trực tiếp ra PDF bằng Aspose.Note cho Java. Khi hoàn thành, bạn sẽ có một đoạn mã có thể tái sử dụng để đưa vào bất kỳ dự án Java nào, tự động hoá việc chuyển đổi OneNote sang PDF một cách chuyên nghiệp.

## Trả lời nhanh
- **Tutorial này dạy gì?** Cách tạo tài liệu OneNote với văn bản có kiểu và lưu nó dưới dạng PDF.  
- **Thư viện nào cần?** Aspose.Note cho Java (tải về từ trang chính thức).  
- **Có cần giấy phép không?** Giấy phép tạm thời hoạt động cho việc thử nghiệm; giấy phép đầy đủ cần cho môi trường sản xuất.  
- **IDE nào có thể dùng?** Bất kỳ IDE Java nào—IntelliJ IDEA, Eclipse, hoặc NetBeans.  
- **Có thể thay đổi định dạng đầu ra không?** Có, Aspose.Note hỗ trợ PDF, HTML, PNG và nhiều định dạng khác.

## Lưu OneNote thành PDF là gì?
Lưu OneNote thành PDF chuyển đổi trang OneNote có cấu trúc—bao gồm văn bản, hình ảnh, bảng và định dạng—thành một tài liệu PDF phẳng có thể mở trên bất kỳ thiết bị nào mà không cần OneNote. Quá trình chuyển đổi giữ nguyên bố cục, phông chữ và các đối tượng nhúng, cung cấp cho bạn một bản đại diện chỉ đọc, di động, phù hợp để chia sẻ, lưu trữ hoặc in ấn.

## Tại sao định dạng rich text java?
Định dạng văn bản giàu trong Java cho phép bạn lập trình kiểu cho tiêu đề, đoạn văn và các phần tử nội tuyến như chữ đậm hoặc màu sắc, để các trang OneNote được tạo ra phù hợp với thương hiệu hoặc tiêu chuẩn báo cáo mà không cần chỉnh sửa thủ công. Bằng cách áp dụng các kiểu trong mã, bạn đảm bảo tính nhất quán, giảm lỗi và có thể tạo tài liệu động dựa trên dữ liệu hoặc đầu vào của người dùng.

## Yêu cầu trước

1. **Java Development Kit (JDK)** – bất kỳ phiên bản mới nào (8 trở lên).  
2. **Aspose.Note cho Java JAR** – tải về từ [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình soạn thảo nào bạn thích.  

## Nhập các gói

Trước khi bắt đầu, nhập các lớp cần thiết vào file Java của bạn:

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

## Cách lưu OneNote thành PDF trong Java – hướng dẫn từng bước

Tải tài liệu OneNote, thêm nội dung có kiểu, và gọi phương thức xuất PDF – đó là quy trình hoàn chỉnh trong ba bước ngắn gọn.

### Bước 1: thiết lập tài liệu và trang

`Document` là đối tượng cấp cao của Aspose.Note đại diện cho một tệp OneNote trong bộ nhớ.  
Một đối tượng `Page` chứa các yếu tố trực quan của một trang OneNote, như văn bản, hình ảnh và các container.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Bước 2: tạo tiêu đề với định dạng

`ParagraphStyle` định nghĩa căn chỉnh, thụt lề và khoảng cách cho một đoạn văn.  
`TextStyle` định nghĩa phông chữ, kích thước, màu và các thuộc tính ký tự khác cho các run văn bản giàu.

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

### Bước 3: tạo văn bản giàu với định dạng

Ở đây chúng ta xây dựng nội dung văn bản giàu bằng một vài đối tượng `TextStyle` để minh họa **định dạng văn bản giàu**.

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

### Bước 4: thêm các phần tử vào trang và tài liệu

Kết hợp tiêu đề và văn bản giàu vào cấu trúc trang để tài liệu phản ánh đúng cấu trúc mong muốn.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Bước 5: lưu tài liệu – xuất OneNote sang PDF

Cuối cùng, xuất tài liệu OneNote dưới dạng tệp PDF trong một lời gọi, giữ nguyên mọi kiểu và bố cục.

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Không tìm thấy tệp** | Xác minh `dataDir` trỏ tới thư mục tồn tại và bạn có quyền ghi. |
| **Thiếu phông chữ** | Đảm bảo các phông chữ bạn tham chiếu (ví dụ, *Calibri*) đã được cài đặt trên máy. |
| **Giấy phép chưa được áp dụng** | Tải giấy phép Aspose trước khi tạo `Document` để tránh dấu nước đánh giá. |

## Câu hỏi thường gặp

**Q: Tôi có thể tùy chỉnh thêm các kiểu phông chữ không?**  
A: Có, bạn có thể điều chỉnh các thuộc tính bổ sung như gạch chân, gạch ngang và căn chỉnh văn bản thông qua các lớp `TextStyle` và `ParagraphStyle`.

**Q: Aspose.Note cho Java có tương thích với mọi IDE Java không?**  
A: Hoàn toàn. Miễn là IDE hỗ trợ phát triển Java tiêu chuẩn, bạn có thể thêm JAR Aspose.Note vào classpath của dự án.

**Q: Tôi có thể tích hợp chức năng này vào các ứng dụng web không?**  
A: Có, cùng một đoạn mã hoạt động trong các ứng dụng servlet hoặc Spring Boot, cho phép tạo tài liệu OneNote‑to‑PDF động phía server.

**Q: Có yêu cầu giấy phép nào khi sử dụng Aspose.Note cho Java không?**  
A: Giấy phép thương mại là bắt buộc cho môi trường sản xuất. Giấy phép tạm thời có sẵn cho mục đích đánh giá và thử nghiệm.

**Q: Aspose.Note cho Java có hỗ trợ các định dạng tài liệu khác ngoài OneNote không?**  
A: Nó hỗ trợ PDF, HTML, PNG, JPEG và một số định dạng xuất khác, giúp bạn linh hoạt chuyển đổi các trang OneNote sang định dạng cần thiết.

## Kết luận

Trong hướng dẫn này, chúng ta đã trình bày cách **tạo tài liệu OneNote**, áp dụng **định dạng văn bản giàu**, và **lưu OneNote thành PDF** bằng Aspose.Note cho Java. Bằng cách làm theo các bước chi tiết, bạn có thể tự động hoá việc tạo ra các tài liệu OneNote chuyên nghiệp và chuyển chúng sang PDF trong bất kỳ giải pháp Java nào.

---

**Last Updated:** 2026-08-18  
**Tested With:** Aspose.Note for Java 26.5 (latest at time of writing)  
**Author:** Aspose

## Các hướng dẫn liên quan

- [Học cách chuyển đổi OneNote sang PDF với Aspose.Note sử dụng PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Lưu OneNote PDF vào Stream - Aspose.Note](/note/java/onenote-document-saving/save-onenote-document-to-stream/)
- [Lưu PDF các trang cụ thể trong OneNote - Aspose.Note](/note/java/onenote-document-saving/specify-save-options/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}