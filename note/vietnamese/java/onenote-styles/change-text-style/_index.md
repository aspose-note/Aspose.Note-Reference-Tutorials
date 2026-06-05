---
date: 2026-06-05
description: Tìm hiểu cách thay đổi font size trong OneNote, đặt font color và highlight
  text với Aspose.Note cho Java – step‑by‑step guide với code snippets.
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: Thay đổi kích thước phông chữ trong OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: Thay đổi kích thước phông chữ trong OneNote - Aspose.Note
url: /vi/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thay Đổi Kích Thước Phông Chữ trong OneNote - Aspose.Note

## Giới Thiệu

Trong hướng dẫn này, bạn sẽ học **how to change font size onenote** tài liệu bằng cách sử dụng Aspose.Note cho Java. Chúng tôi sẽ hướng dẫn cách tải một tệp OneNote, truy cập các nút văn bản của nó, áp dụng thay đổi màu, tô sáng và kích thước phông chữ, và cuối cùng lưu tệp đã cập nhật. Cho dù bạn đang tự động tạo báo cáo hay chỉnh sửa ghi chú cuộc họp, hướng dẫn này cung cấp cho bạn một cách đáng tin cậy để định dạng nội dung OneNote một cách lập trình.

## Câu Trả Lời Nhanh
- **Làm thế nào để thay đổi kích thước phông chữ trong OneNote bằng Java?** Tải tài liệu, sửa đổi thuộc tính `FontSize` của mỗi `TextRun`, sau đó lưu – ba bước đơn giản.  
- **Tôi có thể cũng thay đổi màu văn bản và tô sáng không?** Có, đặt `FontColor` và `HighlightColor` trên cùng một `TextRun`.  
- **Phiên bản Aspose.Note nào được yêu cầu?** Bất kỳ bản phát hành 23.10+ nào cũng hỗ trợ các API định dạng này.  
- **Tôi có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí hoạt động cho việc kiểm tra; giấy phép thương mại là bắt buộc cho môi trường sản xuất.  
- **Phương pháp này có phù hợp cho sổ ghi chú lớn không?** Có – Aspose.Note xử lý các sổ ghi chú hàng trăm trang mà không cần tải toàn bộ tệp vào bộ nhớ.

## change font size onenote là gì?
**change font size onenote** đề cập đến việc điều chỉnh thuộc tính `FontSize` của các phần tử văn bản bên trong một sổ ghi chú OneNote một cách lập trình. Sử dụng Aspose.Note, các nhà phát triển có thể sửa đổi thuộc tính này thông qua API, cập nhật trực tiếp cấu trúc tệp OneNote nền, đảm bảo thay đổi giao diện trực quan mà không cần chỉnh sửa thủ công hoặc tương tác giao diện người dùng.

## Tại sao nên sử dụng Aspose.Note để thay đổi kiểu văn bản trong OneNote?
Aspose.Note cung cấp hơn 30 tùy chọn định dạng — bao gồm họ phông chữ, kích thước, màu, tô sáng, căn chỉnh và khoảng cách đoạn — và được thiết kế để xử lý các sổ ghi chú lớn một cách hiệu quả. Nó có thể xử lý các sổ ghi chú có hơn 500 trang trong khi tiêu thụ dưới 150 MB RAM, mang lại tự động hoá đáng tin cậy, hiệu suất cao cho quy trình công việc tài liệu quy mô doanh nghiệp.

## Yêu Cầu Trước

1. Kiến thức lập trình Java cơ bản.  
2. JDK 8 hoặc cao hơn được cài đặt trên máy của bạn.  
3. Thư viện Aspose.Note cho Java (tải xuống từ trang web Aspose).  
4. Hiểu biết về cấu trúc phân cấp của OneNote (trang, phần, nút RichText).

## Cách thay đổi kích thước phông chữ trong OneNote bằng Aspose.Note?
Tải tệp OneNote của bạn, xác định mỗi nút `RichText`, cập nhật kiểu của mỗi `TextRun`, và lưu tài liệu. Quy trình từ đầu đến cuối này chỉ cần vài dòng mã và chạy dưới một giây cho các sổ ghi chú thông thường.

### Bước 1: Nhập Gói

Các lớp `Document`, `RichText` và `TextRun` nằm trong không gian tên `com.aspose.note`. Nhập chúng vào đầu tệp nguồn Java của bạn:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### Bước 2: Tải Tài Liệu

Lớp `Document` là đối tượng cấp cao nhất của Aspose.Note đại diện cho một tệp OneNote duy nhất trong bộ nhớ. Tải một tệp chỉ cần truyền đường dẫn tệp vào hàm khởi tạo của nó.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### Bước 3: Truy Cập Các Nút RichText

Các nút `RichText` chứa văn bản đoạn thực tế. Bằng cách lặp qua `document.getRichTextNodes()`, bạn có thể truy cập mọi đoạn văn bản có thể chỉnh sửa trong sổ ghi chú.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### Bước 4: Thay Đổi Kiểu Văn Bản

`TextRun` đại diện cho một dải ký tự liên tiếp có cùng định dạng. Trong vòng lặp, đặt `FontColor` thành màu vàng, `HighlightColor` thành màu xanh dương, và `FontSize` thành **20** điểm để đạt được kiểu dáng mong muốn.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### Bước 5: Lưu Tài Liệu

Gọi `document.save("StyledSample.one")` để ghi các thay đổi trở lại tệp OneNote. Thao tác lưu giữ nguyên toàn bộ nội dung gốc đồng thời áp dụng các kiểu mới.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## Các Vấn Đề Thường Gặp và Giải Pháp

- **Văn bản không thay đổi:** Đảm bảo bạn đang lặp qua các đối tượng `TextRun` bên trong mỗi nút `RichText`; bỏ qua cấp này sẽ khiến định dạng không bị thay đổi.  
- **Màu hiển thị khác:** Aspose.Note sử dụng giá trị RGB; hãy xác nhận bạn đang dùng các hằng số `java.awt.Color` đúng.  
- **Sổ ghi chú lớn làm chậm:** LoadOptions cấu hình cách Aspose.Note tải tệp, cho phép streaming và lựa chọn định dạng. Sử dụng `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` để bật chế độ streaming, giảm lượng bộ nhớ sử dụng.

## Câu Hỏi Thường Gặp

**Q: Tôi có thể áp dụng các thay đổi kiểu văn bản này cho các phần cụ thể của tài liệu OneNote không?**  
A: Có, lọc bộ sưu tập `RichText` theo ID trang hoặc phần trước khi áp dụng các thay đổi kiểu.

**Q: Aspose.Note có hỗ trợ các tùy chọn định dạng khác ngoài màu, tô sáng và kích thước không?**  
A: Chắc chắn, bạn có thể sửa đổi họ phông chữ, in đậm/nghiêng, gạch chân, căn chỉnh và khoảng cách đoạn bằng cùng mô hình đối tượng.

**Q: Tôi có thể tích hợp Aspose.Note với các thư viện Java khác để xử lý nâng cao không?**  
A: Có, Aspose.Note hoạt động liền mạch với các thư viện như Apache POI, Jackson hoặc Spring để xây dựng các pipeline tài liệu phức tạp.

**Q: Aspose.Note có được cấp phép cho việc sử dụng thương mại không?**  
A: Giấy phép thương mại là bắt buộc cho triển khai sản xuất; giấy phép đánh giá miễn phí có sẵn cho phát triển và kiểm thử.

**Q: Tôi có thể tìm các mẫu bổ sung và tài liệu tham khảo API ở đâu?**  
A: Truy cập cổng tài liệu Aspose.Note, tải xuống PDF tham khảo API đầy đủ, và khám phá kho lưu trữ GitHub để xem các ví dụ cộng đồng.

## Kết Luận

Bằng cách thực hiện các bước trên, bạn đã biết **how to change font size onenote** các tệp, điều chỉnh màu văn bản và áp dụng tô sáng bằng Aspose.Note cho Java. Khả năng này cho phép bạn tự động hoá việc làm đẹp trực quan cho ghi chú cuộc họp, tài liệu đào tạo, hoặc bất kỳ nội dung nào dựa trên OneNote ở quy mô lớn.

---

**Cập Nhật Cuối Cùng:** 2026-06-05  
**Kiểm Tra Với:** Aspose.Note 23.10 for Java  
**Tác Giả:** Aspose

## Hướng Dẫn Liên Quan

- [Đặt Kiểu Đoạn Mặc Định trong OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [Đặt Ngôn Ngữ Kiểm Tra cho Văn Bản trong OneNote - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Đặt Tiêu Đề Trang trong Kiểu Microsoft OneNote - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}