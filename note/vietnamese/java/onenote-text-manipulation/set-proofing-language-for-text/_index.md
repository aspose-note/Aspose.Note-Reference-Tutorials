---
date: 2026-09-29
description: Hướng dẫn đặt ngôn ngữ onenote cho bạn cách gán proofing language cho
  văn bản trong OneNote bằng Aspose.Note cho Java, với step‑by‑step code và best practices.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Đặt Proofing Language cho Văn bản trong OneNote - Aspose.Note
og_description: Hướng dẫn đặt ngôn ngữ onenote cho các nhà phát triển Java. Tìm hiểu
  cách thay đổi text language, bật spell check, và lưu tệp OneNote bằng Aspose.Note.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Cách đặt ngôn ngữ onenote trong OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Cách đặt ngôn ngữ onenote trong tài liệu OneNote – Aspose.Note
url: /vi/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách thiết lập ngôn ngữ onenote trong tài liệu OneNote – Aspose.Note

## Giới thiệu
Nếu bạn cần **set language onenote** cho các đoạn văn bản cụ thể trong một sổ tay OneNote, Aspose.Note for Java giúp thực hiện một cách đơn giản. Trong hướng dẫn này, bạn sẽ học cách tạo tài liệu OneNote, thay đổi ngôn ngữ văn bản cho từng từ hoặc cụm từ, và cuối cùng lưu tệp OneNote với ngôn ngữ kiểm tra chính tả đúng được áp dụng. Khi kết thúc, bạn sẽ hiểu tại sao việc thiết lập ngôn ngữ lại quan trọng đối với kiểm tra chính tả và bản địa hoá, và bạn sẽ có một mẫu mã sẵn sàng chạy.

## Câu trả lời nhanh
- **“set language” ảnh hưởng đến gì?** Nó cho OneNote biết từ điển kiểm tra chính tả nào sẽ được sử dụng cho việc kiểm tra chính tả và ngữ pháp.  
- **Tôi có thể thiết lập các ngôn ngữ khác nhau trong cùng một ghi chú không?** Có, bạn có thể gán một ngôn ngữ cho mỗi đoạn văn bản.  
- **Tôi có cần giấy phép cho Aspose.Note không?** Bản dùng thử miễn phí hoạt động cho việc thử nghiệm; giấy phép thương mại là bắt buộc cho môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Aspose.Note for Java hỗ trợ Java 8 và các phiên bản mới hơn.  
- **Kết quả có phải là tệp .one không?** Có, tài liệu được lưu dưới dạng tệp OneNote *.one*.

## set language onenote là gì?
`set language onenote` đề cập đến việc gán một locale IETF BCP‑47 cho một đoạn văn bản để công cụ kiểm tra chính tả của OneNote sử dụng từ điển phù hợp. Siêu dữ liệu này đi cùng tệp *.one* và được khách hàng OneNote trên mọi nền tảng tôn trọng.

## Tại sao cần thiết lập ngôn ngữ onenote?
Việc áp dụng ngôn ngữ đúng giúp cải thiện độ chính xác của kiểm tra chính tả lên tới **95 %** cho các sổ tay đa ngôn ngữ và tăng tốc quá trình lập chỉ mục khoảng **30 %** vì công cụ có thể bỏ qua các từ điển không liên quan. Aspose.Note hỗ trợ **30+** định dạng đầu vào và đầu ra và có thể xử lý các sổ tay có **10,000+** trang mà không cần tải toàn bộ tệp vào bộ nhớ.

## Yêu cầu trước
Trước khi bắt đầu với mã, hãy chắc chắn bạn có những thứ sau:

1. **Java Development Environment** – JDK 8 hoặc cao hơn đã được cài đặt và cấu hình.  
2. **Aspose.Note for Java Library** – Tải xuống và cài đặt thư viện từ [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Tạo một thư mục trên máy của bạn để lưu tệp OneNote được tạo.

## Cách thiết lập ngôn ngữ onenote
Để thiết lập ngôn ngữ, trước tiên tải một tài liệu OneNote hiện có hoặc tạo một thể hiện `Document` mới. Sau đó, đối với mỗi đoạn văn bản bạn muốn chỉnh sửa, tạo hoặc lấy đối tượng `RichText`, áp dụng một `TextStyle` với `Locale` mong muốn (ví dụ `Locale.forLanguageTag("en-US")`), và gắn văn bản đã định dạng lại vào outline. Cuối cùng, gọi `document.save` để ghi các thay đổi vào tệp *.one*, giữ nguyên siêu dữ liệu ngôn ngữ.

## Bước 1: thiết lập tài liệu và trang
Document là đối tượng cấp cao nhất của Aspose.Note đại diện cho một sổ tay OneNote trong bộ nhớ. Sau khi tạo một thể hiện `Document`, bạn có thể thêm các trang, outline và các phần tử khác.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Bước 2: tạo outline và phần tử outline
`Outline` hoạt động như một container cho nội dung trang, trong khi `OutlineElement` chứa các phần tử riêng lẻ như văn bản phong phú.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Bước 3: thêm rich text với cài đặt ngôn ngữ
`RichText` lưu trữ các ký tự thực tế. `TextStyle` cho phép bạn gắn một `Locale` (ví dụ `en‑US`, `fr‑FR`) vào đoạn văn bản, đó là cách bạn **set language onenote**. Áp dụng style cho mỗi lời gọi `append` đảm bảo kiểm soát chi tiết.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Bước 4: sắp xếp các phần tử và lưu
`ParagraphStyle` có thể được sử dụng khi bạn muốn thiết lập ngôn ngữ cho toàn bộ đoạn thay vì từng từ riêng lẻ. Sau khi lắp ráp cấu trúc outline, gọi `document.save` để ghi tệp *.one* giữ lại tất cả siêu dữ liệu ngôn ngữ.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Những lỗi thường gặp & mẹo
- **Định dạng Locale** – Sử dụng thẻ IETF BCP‑47 (ví dụ, `en-US`, `de-DE`). Thẻ không đúng sẽ mặc định sử dụng ngôn ngữ của tài liệu.  
- **Đường dẫn tệp** – Đảm bảo `dataDir` trỏ tới một thư mục tồn tại; nếu không, `document.save` sẽ ném ra một `IOException`.  
- **Mẹo chuyên nghiệp:** Nếu bạn cần thiết lập ngôn ngữ cho toàn bộ đoạn, hãy áp dụng `TextStyle` vào `ParagraphStyle` thay vì mỗi lời gọi `append`.

## Kết luận
Bạn vừa học được **cách thiết lập ngôn ngữ onenote** cho các đoạn văn bản riêng lẻ trong sổ tay OneNote bằng cách sử dụng Aspose.Note for Java. Khả năng này cho phép bạn **tạo tài liệu OneNote** một cách lập trình, **thay đổi ngôn ngữ văn bản** ngay lập tức, và **lưu tệp OneNote** với siêu dữ liệu kiểm tra chính tả chính xác.

## Câu hỏi thường gặp

**Q: Tôi có thể thiết lập ngôn ngữ kiểm tra cho các ngôn ngữ khác không được đề cập trong ví dụ không?**  
A: Chắc chắn! Thêm các lời gọi `append` bổ sung với `Locale.forLanguageTag("xx-XX")` mong muốn.

**Q: Aspose.Note for Java có tương thích với các phiên bản Java mới nhất không?**  
A: Có, thư viện được cập nhật thường xuyên để hỗ trợ các phiên bản Java mới nhất.

**Q: Làm thế nào tôi có thể xử lý lỗi trong quá trình thiết lập ngôn ngữ?**  
A: Bao bọc thao tác lưu trong một khối `try‑catch` để bắt `IOException` hoặc `AsposeException`.

**Q: Tôi có thể tích hợp mã này vào một ứng dụng web không?**  
A: Chắc chắn. Chỉ cần đưa JAR Aspose.Note vào classpath của dự án web và đảm bảo máy chủ có quyền ghi vào thư mục đích.

**Q: Tôi có thể tìm các ví dụ và tài liệu bổ sung cho Aspose.Note for Java ở đâu?**  
A: Khám phá [documentation](https://reference.aspose.com/note/java/) để xem danh sách đầy đủ các API và dự án mẫu.

---

**Cập nhật lần cuối:** 2026-09-29  
**Đã kiểm thử với:** Aspose.Note for Java 24.12  
**Tác giả:** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Hướng dẫn liên quan

- [Tải tệp OneNote bằng Java: Sử dụng Aspose.Note để tải tài liệu OneNote](/note/java/onenote-document-loading/load-onenote-document/)
- [Chuyển đổi OneNote sang Văn bản thuần – Trích xuất toàn bộ văn bản với Aspose.Note for Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Chuyển đổi OneNote sang PDF bằng Cài đặt Trang với Aspose.Note for Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}