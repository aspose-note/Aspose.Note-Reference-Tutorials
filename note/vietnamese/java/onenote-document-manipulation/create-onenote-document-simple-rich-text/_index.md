---
date: 2026-08-18
description: Tìm hiểu cách xuất OneNote sang PDF, thiết lập định dạng đoạn văn trong
  Java và lưu OneNote dưới dạng PDF bằng Aspose.Note for Java.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: Đặt Kiểu Đoạn Văn khi Tạo Tài liệu OneNote trong Java
og_description: Xuất OneNote sang PDF và thiết lập kiểu đoạn văn trong Java bằng Aspose.Note.
  Thực hiện theo hướng dẫn từng bước để tạo ra các tệp PDF hoàn hảo một cách dễ dàng.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: Xuất OneNote sang PDF với kiểu đoạn văn trong Java (58 ký tự)
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  headline: How to export OneNote to PDF with paragraph style in Java
  type: TechArticle
- description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  name: How to export OneNote to PDF with paragraph style in Java
  steps:
  - name: set document directory
    text: Define where the generated files will be saved. Replace `"Your Document
      Directory"` with an absolute or relative path on your machine.
  - name: initialize document object
    text: Create the root `Document` that represents the OneNote file. **Definition
      anchor:** `Document` is Aspose.Note’s top‑level object that holds one or more
      pages in memory.
  - name: initialize page object
    text: A OneNote file consists of one or more pages; we start with a single page.
      **Definition anchor:** `Page` represents a single OneNote page, containing outlines,
      images, and other elements.
  - name: initialize outline object
    text: Outlines act as containers for outline elements (think of them as sections).
      **Definition anchor:** `Outline` groups related `OutlineElement` objects and
      defines their visual hierarchy.
  - name: initialize outline element object
    text: Here we **add outline element** that will hold our rich text. **Definition
      anchor:** `OutlineElement` is a leaf node inside an `Outline` that can contain
      text, images, or other media.
  - name: set text style (set paragraph style)
    text: '`ParagraphStyle` defines the font family, size, color, and other typographic
      attributes for a paragraph. The `ParagraphStyle` instance defines the font,
      size, and color—this is where we **set paragraph style** for the upcoming text
      node.'
  - name: initialize rich text object
    text: '`RichText` is the node that stores styled text within an `OutlineElement`.
      We create a `RichText` node, insert a simple string, and attach the previously
      defined style.'
  - name: add rich text node to outline element
    text: Now the styled text lives inside the outline element.
  - name: add outline element node to outline
    text: The outline now contains the element that holds our paragraph.
  - name: add outline node to page
    text: We place the outline onto the page.
  type: HowTo
- questions:
  - answer: Yes, the API supports tables, images, hyperlinks, and advanced layout
      features in addition to plain text.
    question: Can Aspose.Note handle complex formatting such as tables or images?
  - answer: Direct conversion isn’t provided, but you can extract PDF content and
      rebuild a OneNote document using the API.
    question: Is it possible to convert a OneNote PDF back to a OneNote file?
  - answer: Absolutely. Aspose.Note for Java is platform‑independent; just ensure
      a compatible JDK is installed.
    question: Does the library work on Linux/macOS environments?
  - answer: Create additional `Page` and `Outline` objects, then append them to the
      `Document` just like the single‑page example.
    question: How do I add multiple pages or outlines?
  - answer: The official Aspose.Note documentation and the [support forum](https://forum.aspose.com/c/note/28)
      contain many code samples and real‑world scenarios.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- export onenote
- aspose.note
- java document processing
title: Cách xuất OneNote sang PDF với kiểu đoạn văn trong Java
url: /vi/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt kiểu đoạn văn khi tạo tài liệu OneNote bằng Java

## Giới thiệu

Xuất OneNote sang PDF một cách lập trình là yêu cầu phổ biến cho các công cụ báo cáo, dịch vụ ghi chú tự động và quy trình chuyển đổi tài liệu. Trong hướng dẫn này, bạn sẽ học cách **xuất OneNote sang PDF**, áp dụng định dạng đoạn văn tùy chỉnh và lưu tệp OneNote — tất cả đều sử dụng Aspose.Note cho Java. Khi hoàn thành, bạn sẽ có một đoạn mã Java sẵn sàng sử dụng để tạo ra PDF chuyên nghiệp với giao diện chính xác như bạn đã định nghĩa.

## Câu trả lời nhanh
- **“set paragraph style” có nghĩa là gì?** Nó áp dụng phông chữ, kích thước, màu sắc và các thuộc tính định dạng khác cho một đoạn văn bản.  
- **Tôi có thể xuất kết quả sang PDF không?** Có – hướng dẫn kết thúc bằng việc lưu tệp OneNote dưới dạng PDF.  
- **Tôi có cần giấy phép cho Aspose.Note không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép thương mại là bắt buộc cho môi trường sản xuất.  
- **Những IDE nào được hỗ trợ?** Bất kỳ IDE Java nào – Eclipse, IntelliJ IDEA, NetBeans, v.v.  
- **Thời gian thực hiện ước tính là bao lâu?** Khoảng 10‑15 phút cho một tài liệu cơ bản.

## Cách xuất OneNote sang PDF trong Java?

`Document` đại diện cho một tệp OneNote chứa các trang, outline và các yếu tố khác. Tải tài liệu OneNote của bạn bằng `new Document()` (hoặc tạo mới) và gọi `document.save("output.pdf", SaveFormat.Pdf)`. Aspose.Note ghi PDF trong một lần duy nhất, giữ nguyên kiểu, hình ảnh và outline mà không cần cài đặt Microsoft OneNote. Cách tiếp cận trực tiếp này hoạt động trên Windows, Linux và macOS với bất kỳ JDK 1.8+ nào.

## “set paragraph style” là gì trong Aspose.Note?

`ParagraphStyle` là lớp lưu trữ tên phông, kích thước, màu sắc, căn chỉnh và các thiết lập kiểu chữ khác cho một đoạn văn. Bằng cách gắn một thể hiện `ParagraphStyle` vào nút `RichText` bạn kiểm soát chính xác cách đoạn văn xuất hiện trong trang OneNote cuối cùng và PDF đã xuất.

## Tại sao xuất OneNote sang PDF?

Xuất OneNote sang PDF đảm bảo thương hiệu nhất quán bằng cách giữ nguyên phông và màu sắc công ty, cải thiện khả năng đọc bằng cách duy trì bố cục chính xác cho việc in ấn hoặc lưu trữ, và cung cấp truy cập đa nền tảng để người nhận có thể xem tài liệu trên bất kỳ thiết bị nào mà không cần OneNote. Ngoài ra còn mang lại lợi thế về hiệu suất, cho phép xử lý nhanh các tài liệu lớn.

## Yêu cầu trước

1. **Java Development Kit (JDK) 1.8+** – bất kỳ JDK hiện đại nào cũng hoạt động.  
2. **Aspose.Note for Java** – tải JAR mới nhất từ [trang tải xuống Aspose.Note](https://releases.aspose.com/note/java/).  
3. **Một IDE** (Eclipse, IntelliJ IDEA hoặc NetBeans) để biên dịch và chạy mẫu.  

> **Mẹo chuyên nghiệp:** Thêm JAR Aspose.Note vào classpath của dự án qua Maven (`<dependency>`) hoặc bằng cách tham chiếu thủ công JAR trong IDE của bạn.

## Nhập các gói

Đầu tiên, nhập các namespace cần thiết. Khối này không thay đổi.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> Lớp `ParagraphStyle` là chìa khóa để **set paragraph style** sau này trong hướng dẫn.

## Hướng dẫn từng bước

Dưới đây là một quy trình ngắn gọn cho từng thao tác. Các khối mã được giữ nguyên như trong mẫu gốc; chúng tôi chỉ thêm phần giải thích.

### Bước 1: đặt thư mục tài liệu
Xác định nơi các tệp được tạo sẽ được lưu.

```java
String dataDir = "Your Document Directory";
```

Thay thế `"Your Document Directory"` bằng đường dẫn tuyệt đối hoặc tương đối trên máy của bạn.

### Bước 2: khởi tạo đối tượng tài liệu
Tạo đối tượng `Document` gốc đại diện cho tệp OneNote.

```java
Document doc = new Document();
```

**Mô tả:** `Document` là đối tượng cấp cao nhất của Aspose.Note, chứa một hoặc nhiều trang trong bộ nhớ.

### Bước 3: khởi tạo đối tượng trang
Một tệp OneNote bao gồm một hoặc nhiều trang; chúng ta bắt đầu với một trang duy nhất.

```java
Page page = new Page();
```

**Mô tả:** `Page` đại diện cho một trang OneNote đơn, chứa outline, hình ảnh và các yếu tố khác.

### Bước 4: khởi tạo đối tượng outline
Outline hoạt động như container cho các yếu tố outline (tưởng như các phần).

```java
Outline outline = new Outline();
```

**Mô tả:** `Outline` nhóm các đối tượng `OutlineElement` có liên quan và xác định thứ tự hiển thị của chúng.

### Bước 5: khởi tạo đối tượng outline element
Ở đây chúng ta **add outline element** sẽ chứa văn bản phong phú của chúng ta.

```java
OutlineElement outlineElem = new OutlineElement();
```

**Mô tả:** `OutlineElement` là nút lá trong một `Outline` có thể chứa văn bản, hình ảnh hoặc các phương tiện khác.

### Bước 6: đặt kiểu văn bản (set paragraph style)

`ParagraphStyle` xác định họ phông, kích thước, màu sắc và các thuộc tính kiểu chữ khác cho một đoạn văn.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Thể hiện `ParagraphStyle` định nghĩa phông, kích thước và màu – đây là nơi chúng ta **set paragraph style** cho nút văn bản sắp tới.

### Bước 7: khởi tạo đối tượng rich text

`RichText` là nút lưu trữ văn bản có định dạng bên trong một `OutlineElement`.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Chúng ta tạo một nút `RichText`, chèn một chuỗi đơn giản và gắn kiểu đã định nghĩa trước đó.

### Bước 8: thêm nút rich text vào outline element

```java
outlineElem.appendChildLast(text);
```

Bây giờ văn bản đã được định dạng nằm bên trong outline element.

### Bước 9: thêm nút outline element vào outline

```java
outline.appendChildLast(outlineElem);
```

Outline hiện chứa phần tử giữ đoạn văn của chúng ta.

### Bước 10: thêm nút outline vào trang

```java
page.appendChildLast(outline);
```

Chúng ta đặt outline lên trang.

### Bước 11: thêm nút trang vào tài liệu

```java
doc.appendChildLast(page);
```

Tài liệu hiện có một trang duy nhất với văn bản đã định dạng.

### Bước 12: lưu tài liệu (xuất OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Phương thức `save` ghi tệp OneNote và **exports OneNote to PDF** trong một bước. Bạn cũng có thể lưu dưới dạng `.one` bằng cách sử dụng `SaveFormat.One` nếu cần định dạng gốc.

## Các vấn đề thường gặp & giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|------------|----------------|
| **File not found** | `dataDir` trỏ tới thư mục không tồn tại. | Đảm bảo thư mục tồn tại hoặc tạo nó bằng chương trình (`new File(dataDir).mkdirs();`). |
| **Blank PDF** | Không có nội dung nào được thêm trước khi lưu. | Kiểm tra xem nút `RichText` đã được nối và kiểu đã được đặt chưa. |
| **Unsupported font** | Tên phông không được cài đặt trên hệ thống. | Sử dụng phông chung như `"Arial"` hoặc nhúng phông vào dự án. |

## Câu hỏi thường gặp

**Q: Aspose.Note có thể xử lý định dạng phức tạp như bảng hoặc hình ảnh không?**  
A: Có, API hỗ trợ bảng, hình ảnh, siêu liên kết và các tính năng bố cục nâng cao bên cạnh văn bản thuần.

**Q: Có thể chuyển đổi PDF của OneNote lại thành tệp OneNote không?**  
A: Chuyển đổi trực tiếp không được cung cấp, nhưng bạn có thể trích xuất nội dung PDF và xây dựng lại tài liệu OneNote bằng API.

**Q: Thư viện có hoạt động trên môi trường Linux/macOS không?**  
A: Hoàn toàn có. Aspose.Note cho Java không phụ thuộc vào nền tảng; chỉ cần đảm bảo cài đặt JDK tương thích.

**Q: Làm sao để thêm nhiều trang hoặc outline?**  
A: Tạo thêm các đối tượng `Page` và `Outline`, sau đó nối chúng vào `Document` giống như ví dụ một trang.

**Q: Tôi có thể tìm thêm ví dụ ở đâu?**  
A: Tài liệu chính thức của Aspose.Note và [diễn đàn hỗ trợ](https://forum.aspose.com/c/note/28) chứa nhiều mẫu mã và kịch bản thực tế.

## Kết luận

Bạn đã thấy cách **set paragraph style**, **add outline element**, và **export OneNote to PDF** bằng Aspose.Note cho Java. Áp dụng văn bản có định dạng từ sớm giúp PDF cuối cùng trông chuyên nghiệp, và thao tác `save` một lần xử lý chuyển đổi một cách hiệu quả. Bạn có thể mở rộng nền tảng này với hình ảnh, bảng hoặc siêu dữ liệu tùy chỉnh để đáp ứng nhu cầu cụ thể của ứng dụng.

---

**Cập nhật lần cuối:** 2026-08-18  
**Kiểm tra với:** Aspose.Note for Java 26.5 (bản phát hành mới nhất)  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Cách lưu OneNote dưới dạng PDF với Aspose.Note cho Java](/note/java/onenote-document-loading/load-save-format/)
- [Học cách chuyển OneNote sang PDF với Aspose.Note sử dụng PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Đặt Kiểu Đoạn Văn Mặc Định trong OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}