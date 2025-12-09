---
date: 2025-12-09
description: Tìm hiểu cách lưu OneNote dưới dạng PDF với văn bản giàu định dạng trong
  Java bằng Aspose.Note for Java. Hãy theo dõi hướng dẫn từng bước của chúng tôi để
  tự động hoá tài liệu một cách liền mạch.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Lưu OneNote dưới dạng PDF với Văn bản Định dạng Đầy đủ trong Java
url: /vi/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu OneNote dưới dạng PDF với Văn bản Định dạng Đầy đủ trong Java

## Giới thiệu

Nếu bạn cần **lưu OneNote dưới dạng PDF** trong khi giữ nguyên định dạng văn bản phong phú, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn cách tạo tài liệu OneNote, áp dụng các kiểu tùy chỉnh, và xuất trực tiếp ra PDF bằng Aspose.Note cho Java. Khi hoàn thành, bạn sẽ có một đoạn mã có thể tái sử dụng, có thể chèn vào bất kỳ dự án Java nào để tự động chuyển đổi OneNote sang PDF một cách chuyên nghiệp.

## Câu trả lời nhanh
- **Hướng dẫn này dạy gì?** Cách tạo tài liệu OneNote với văn bản có kiểu dáng và lưu nó dưới dạng PDF.  
- **Thư viện nào được yêu cầu?** Aspose.Note for Java (downloadable from the official site).  
- **Tôi có cần giấy phép không?** Một giấy phép tạm thời hoạt động cho việc thử nghiệm; giấy phép đầy đủ cần thiết cho môi trường sản xuất.  
- **IDE nào tôi có thể sử dụng?** Bất kỳ IDE Java nào—IntelliJ IDEA, Eclipse, hoặc NetBeans.  
- **Tôi có thể thay đổi định dạng đầu ra không?** Có, Aspose.Note hỗ trợ PDF, HTML, PNG và nhiều hơn nữa.

## “Lưu OneNote dưới dạng PDF” là gì?
Lưu OneNote dưới dạng PDF có nghĩa là chuyển đổi cấu trúc trang OneNote—bao gồm văn bản, hình ảnh và định dạng—thành một tệp PDF tĩnh có thể xem trên bất kỳ nền tảng nào mà không cần OneNote.

## Tại sao định dạng văn bản phong phú trong Java?
Áp dụng định dạng văn bản phong phú (phông chữ, màu sắc, kiểu dáng) trực tiếp trong Java cho phép bạn tạo tài liệu trông chuyên nghiệp và phù hợp với hướng dẫn thương hiệu mà không cần chỉnh sửa thủ công.

## Yêu cầu trước

1. **Bộ công cụ phát triển Java (JDK)** – bất kỳ phiên bản mới nào (8 trở lên).  
2. **Aspose.Note for Java JAR** – tải xuống từ [liên kết tải xuống](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình chỉnh sửa nào bạn thích.  

## Nhập các Gói

Đầu tiên bạn cần nhập các gói cần thiết vào dự án Java của mình. Thêm các câu lệnh import sau vào đầu tệp Java của bạn:

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

## Bước 1: Thiết lập Tài liệu và Trang

Hãy bắt đầu bằng việc khởi tạo các đối tượng `Document` và `Page`:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Bước 2: Tạo Tiêu đề với Định dạng

Bây giờ, chúng ta sẽ tạo một tiêu đề với văn bản đã được định dạng:

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

## Bước 3: Tạo Văn bản Định dạng Đầy đủ

Tiếp theo, chúng ta sẽ tạo văn bản phong phú với các kiểu định dạng khác nhau:

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

## Bước 4: Thêm các Thành phần vào Trang và Tài liệu

Bây giờ, chúng ta sẽ thêm tiêu đề và văn bản phong phú vào trang và các thành phần phác thảo:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Bước 5: Lưu Tài liệu

Cuối cùng, lưu tài liệu OneNote đã tạo dưới dạng PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Các vấn đề thường gặp và Giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Không tìm thấy tệp** | Xác minh `dataDir` trỏ tới một thư mục tồn tại và bạn có quyền ghi. |
| **Thiếu phông chữ** | Đảm bảo các phông chữ bạn tham chiếu (ví dụ, *Calibri*) đã được cài đặt trên máy chủ. |
| **Giấy phép chưa được áp dụng** | Tải giấy phép Aspose của bạn trước khi tạo `Document` để tránh dấu nước đánh giá. |

## Câu hỏi thường gặp

**Q: Tôi có thể tùy chỉnh thêm các kiểu phông chữ không?**  
A: Có, bạn có thể điều chỉnh các thuộc tính bổ sung như gạch chân, gạch ngang và căn chỉnh văn bản thông qua các lớp `TextStyle` và `ParagraphStyle`.

**Q: Aspose.Note cho Java có tương thích với mọi IDE Java không?**  
A: Chắc chắn. Miễn là IDE hỗ trợ phát triển Java tiêu chuẩn, bạn có thể thêm JAR Aspose.Note vào classpath của dự án.

**Q: Tôi có thể tích hợp chức năng này vào các ứng dụng web không?**  
A: Có, cùng một đoạn mã hoạt động trong các ứng dụng dựa trên servlet hoặc Spring Boot, cho phép tạo OneNote‑to‑PDF động phía máy chủ.

**Q: Có yêu cầu giấy phép nào cho việc sử dụng Aspose.Note cho Java không?**  
A: Một giấy phép thương mại là bắt buộc cho việc sử dụng trong môi trường sản xuất. Giấy phép tạm thời có sẵn cho việc đánh và thử nghiệm.

**Q: Aspose.Note cho Java có hỗ trợ các định dạng tài liệu khác ngoài OneNote không?**  
A: Nó hỗ trợ PDF, HTML, PNG, JPEG và một số định dạng xuất khác, giúp bạn linh hoạt chuyển đổi trang OneNote sang định dạng cần thiết.

## Kết luận

Trong hướng dẫn này, chúng tôi đã trình bày cách **lưu OneNote dưới dạng PDF** đồng thời áp dụng định dạng văn bản phong phú bằng Aspose.Note cho Java. Bằng cách làm theo các bước chi tiết, bạn có thể tự động tạo các tài liệu OneNote chuyên nghiệp và chuyển đổi chúng sang PDF trong bất kỳ giải pháp dựa trên Java nào.

---

**Last Updated:** 2025-12-09  
**Tested With:** Aspose.Note for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}