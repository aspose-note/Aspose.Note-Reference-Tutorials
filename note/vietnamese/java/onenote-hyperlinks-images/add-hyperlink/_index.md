---
date: 2025-12-20
description: Tìm hiểu cách lưu OneNote dưới dạng PDF và thêm siêu liên kết trong OneNote
  bằng Java với thư viện Aspose.Note. Tạo PDF từ OneNote một cách dễ dàng.
linktitle: Save OneNote as PDF and Add Hyperlink in OneNote with Java
second_title: Aspose.Note Java API
title: Lưu OneNote dưới dạng PDF và Thêm siêu liên kết trong OneNote bằng Java
url: /vi/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu OneNote dưới dạng PDF và Thêm Siêu liên kết trong OneNote bằng Java

## Giới thiệu

Thêm siêu liên kết vào tài liệu OneNote của bạn đồng thời lưu chúng dưới dạng PDF có thể cải thiện đáng kể tính tương tác của ghi chú và giúp việc chia sẻ dễ dàng hơn. Trong hướng dẫn này, bạn sẽ học **cách lưu OneNote dưới dạng PDF** và nhúng một liên kết có thể nhấp được bằng Java và thư viện Aspose.Note. Hãy cùng đi qua các bước nhé!

## Câu trả lời nhanh
- **Tôi có thể lưu OneNote dưới dạng PDF bằng Java không?** Có, Aspose.Note for Java cung cấp một lệnh `save` duy nhất để tạo PDF.
- **Làm thế nào để nhúng một siêu liên kết?** Sử dụng `TextStyle.setHyperlinkAddress` trên một đoạn `RichText`.
- **Các yêu cầu trước là gì?** JDK 8+ và thư viện Aspose.Note cho Java.
- **Các định dạng đầu ra được hỗ trợ là gì?** PDF, DOCX, XPS và nhiều hơn nữa.
- **Có cần giấy phép cho môi trường sản xuất không?** Có, cần giấy phép thương mại cho việc sử dụng không phải để đánh giá.

## “Lưu OneNote dưới dạng PDF” là gì?

Lưu một sổ tay OneNote dưới dạng PDF tạo ra một phiên bản di động, chỉ đọc của ghi chú của bạn, có thể mở trên bất kỳ thiết bị nào mà không cần ứng dụng OneNote. Điều này đặc biệt hữu ích cho việc lưu trữ, in ấn hoặc chia sẻ với những người dùng không có OneNote.

## Tại sao tạo PDF từ OneNote bằng Aspose.Note Java?

- **Độ trung thực đầy đủ:** Giữ nguyên định dạng, hình ảnh và siêu liên kết.
- **Kiểm soát lập trình:** Tự động hoá chuyển đổi hàng loạt trong các dịch vụ backend.
- **Đa nền tảng:** Hoạt động trên Windows, Linux và macOS.
- **API phong phú:** Dễ dàng thêm hoặc chỉnh sửa nội dung trước khi lưu.

## Yêu cầu trước

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt và thiết lập các yêu cầu sau trên hệ thống của mình:

### Java Development Kit (JDK)

Đảm bảo bạn đã cài đặt Java Development Kit (JDK) trên hệ thống. Bạn có thể tải và cài đặt JDK từ [trang web Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Aspose.Note for Java Library

Tải xuống và cài đặt thư viện Aspose.Note cho Java. Bạn có thể tìm tài liệu và liên kết tải xuống [tại đây](https://reference.aspose.com/note/java/).

## Nhập các Gói

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

Bây giờ, chúng ta sẽ phân tích ví dụ đã cung cấp thành nhiều bước:

## Bước 1: Thiết lập cấu trúc tài liệu

Đầu tiên, tạo một tài liệu mới và một trang nơi nội dung sẽ được đặt.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Bước 2: Định nghĩa kiểu văn bản mặc định

Định nghĩa một kiểu đoạn văn mặc định sẽ được áp dụng cho hầu hết các phần tử văn bản.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Bước 3: Đặt tiêu đề

Tạo tiêu đề cho trang và áp dụng kiểu mặc định.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Bước 4: Tạo Outline và các phần tử Outline

Outline hoạt động như các container cho các đoạn văn và các phần tử khác.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Bước 5: Định nghĩa kiểu văn bản cho Siêu liên kết

Ở đây chúng ta định nghĩa một kiểu màu đỏ sẽ được sử dụng cho phần có thể nhấp.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Bước 6: Thêm Văn bản với Siêu liên kết

Bây giờ chúng ta tạo một đối tượng `RichText` kết hợp văn bản thường và một siêu liên kết.  
Phương thức `setHyperlinkAddress` cho Aspose.Note biết rằng đoạn này nên có thể nhấp.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Bước 7: Thêm Outline vào Trang và Trang vào Tài liệu

Gắn phần tử outline vào outline, outline vào trang, và cuối cùng trang vào tài liệu.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Bước 8: Lưu Tài liệu dưới dạng PDF

Bước cuối cùng là lưu tài liệu OneNote dưới dạng tệp PDF. Đây là nơi từ khóa chính **save onenote as pdf** được áp dụng.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Kết luận

Chúc mừng! Bạn đã thành công **lưu OneNote dưới dạng PDF** và thêm một siêu liên kết vào tài liệu bằng Java và thư viện Aspose.Note. Khả năng này cho phép bạn tạo các tệp PDF tương tác, có thể chia sẻ trực tiếp từ nội dung OneNote của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.Note có tương thích với mọi phiên bản Java không?

A1: Có, Aspose.Note cho Java hỗ trợ tất cả các phiên bản Java chính, bao gồm JDK 8 trở lên.

### Câu hỏi 2: Tôi có thể thêm nhiều siêu liên kết trong một tài liệu duy nhất bằng Aspose.Note không?

A2: Chắc chắn! Bạn có thể thêm bao nhiêu siêu liên kết tùy thích trong tài liệu OneNote của mình bằng Aspose.Note cho Java.

### Câu hỏi 3: Aspose.Note có hỗ trợ các ngôn ngữ lập trình khác không?

A3: Có, Aspose.Note cung cấp các thư viện cho nhiều ngôn ngữ lập trình, bao gồm .NET, Python và Android.

### Câu hỏi 4: Aspose.Note có dễ tích hợp vào các dự án Java hiện có không?

A4: Có, việc tích hợp Aspose.Note vào các dự án Java của bạn rất đơn giản và được tài liệu hoá đầy đủ, giúp bạn dễ dàng bắt đầu.

### Câu hỏi 5: Tôi có thể tìm thêm trợ giúp và tài nguyên cho việc sử dụng Aspose.Note ở đâu?

A5: Bạn có thể tìm tài liệu chi tiết, hướng dẫn và hỗ trợ cộng đồng trên [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28).

## Các câu hỏi thường gặp

**Q: Làm thế nào để tùy chỉnh giao diện của siêu liên kết?**  
A: Sử dụng các thuộc tính của `TextStyle` như `setFontColor`, `setUnderline`, hoặc `setFontName` trước khi gọi `setHyperlinkAddress`.

**Q: Tôi có thể lưu tài liệu ở các định dạng khác ngoài PDF không?**  
A: Có, Aspose.Note hỗ trợ DOCX, XPS, HTML và một số định dạng xuất khác.

**Q: Nếu tôi cần thêm một siêu liên kết vào tệp OneNote hiện có thì sao?**  
A: Tải tệp hiện có bằng `new Document("input.one")`, chỉnh sửa nội dung như đã minh họa, và sau đó gọi `save` với định dạng mong muốn.

**Q: Có cách nào mở siêu liên kết một cách lập trình sau khi PDF được tạo không?**  
A: Trình xem PDF sẽ tự động xử lý các liên kết có thể nhấp; không cần mã bổ sung.

**Q: Tôi có cần giấy phép cho việc sử dụng trong phát triển không?**  
A: Giấy phép đánh giá tạm thời đủ cho việc phát triển và thử nghiệm, nhưng cần giấy phép đầy đủ cho triển khai trong môi trường sản xuất.

---

**Cập nhật lần cuối:** 2025-12-20  
**Được kiểm tra với:** Aspose.Note for Java 23.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}