---
date: 2026-02-18
description: Học cách đặt kiểu đoạn văn và thêm phần tử outline khi tạo tài liệu OneNote
  bằng Java sử dụng Aspose.Note. Xuất OneNote sang PDF, lưu OneNote dưới dạng PDF
  và tạo tệp OneNote một cách dễ dàng.
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: Xuất OneNote sang PDF – Đặt kiểu đoạn văn khi tạo tài liệu OneNote bằng Java
url: /vi/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt Kiểu Đoạn Văn khi Tạo Tài liệu OneNote trong Java

## Giới thiệu

Trong bối cảnh phát triển nhanh chóng ngày nay, khả năng **export OneNote to PDF** một cách lập trình là điều cần thiết để tạo ra các tài liệu hoàn thiện, sẵn sàng chia sẻ. Hướng dẫn này sẽ chỉ cho bạn cách tạo một tệp OneNote, áp dụng kiểu đoạn văn tùy chỉnh, và cuối cùng **export OneNote to PDF** bằng Aspose.Note cho Java. Dù bạn đang xây dựng một công cụ báo cáo, một giải pháp ghi chú tự động, hay một dịch vụ chuyển đổi tài liệu, các kỹ thuật ở đây sẽ giúp bạn **save OneNote as PDF** với kiểm soát định dạng chính xác.

## Trả lời nhanh
- **“set paragraph style” có nghĩa là gì?** Nó áp dụng phông chữ, kích thước, màu sắc và các định dạng khác cho một đoạn văn bản.  
- **Tôi có thể xuất kết quả ra PDF không?** Có – hướng dẫn kết thúc bằng việc lưu tệp OneNote dưới dạng PDF.  
- **Có cần giấy phép cho Aspose.Note không?** Bản dùng thử miễn phí đủ cho việc đánh giá; cần giấy phép cho môi trường sản xuất.  
- **Những IDE nào được hỗ trợ?** Bất kỳ IDE Java nào – Eclipse, IntelliJ IDEA, NetBeans, v.v.  
- **Thời gian thực hiện ước tính là bao lâu?** Khoảng 10‑15 phút cho một tài liệu cơ bản.

## “set paragraph style” trong Aspose.Note là gì?
Việc đặt kiểu đoạn văn đề cập đến việc cấu hình một đối tượng `ParagraphStyle` (tên phông, kích thước, màu sắc, v.v.) và gắn nó vào một nút `RichText`. Điều này cho phép bạn kiểm soát hoàn toàn cách hiển thị văn bản trong một trang OneNote.

## Cách đặt Paragraph Style trong OneNote?
Áp dụng một kiểu chỉ cần tạo một thể hiện `ParagraphStyle`, tùy chỉnh các thuộc tính của nó, và gán cho phần tử `RichText`. API cho phép thực hiện việc này chỉ trong một dòng lệnh khi đối tượng kiểu đã sẵn sàng.

## Tại sao phải Export OneNote to PDF?
- **Nhận diện thương hiệu nhất quán:** Giữ nguyên phông chữ và màu sắc công ty khi chia sẻ ghi chú ra bên ngoài.  
- **Độ đọc tốt:** PDF giữ nguyên bố cục, rất phù hợp cho việc in ấn hoặc lưu trữ.  
- **Truy cập đa nền tảng:** Người nhận có thể xem PDF trên bất kỳ thiết bị nào mà không cần cài đặt OneNote.  

## Các yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

1. **Java Development Kit (JDK) 1.8+** – bất kỳ JDK hiện đại nào cũng hoạt động.  
2. **Aspose.Note for Java** – tải JAR mới nhất từ [trang tải Aspose.Note](https://releases.aspose.com/note/java/).  
3. **Một IDE** (Eclipse, IntelliJ IDEA, hoặc NetBeans) để biên dịch và chạy mẫu.  

> **Mẹo chuyên nghiệp:** Thêm JAR Aspose.Note vào classpath của dự án qua Maven hoặc bằng cách tham chiếu thủ công JAR trong IDE của bạn.

## Nhập các gói

Đầu tiên, nhập các lớp cần thiết. Khối này không thay đổi.

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

Dưới đây là quy trình ngắn gọn cho mỗi thao tác. Các khối mã giữ nguyên như mẫu gốc; chúng tôi chỉ thêm phần giải thích.

### Bước 1: Đặt thư mục tài liệu
Xác định nơi sẽ lưu các tệp được tạo.

```java
String dataDir = "Your Document Directory";
```

Thay `"Your Document Directory"` bằng đường dẫn tuyệt đối hoặc tương đối trên máy của bạn.

### Bước 2: Khởi tạo đối tượng Document
Tạo đối tượng gốc `Document` đại diện cho tệp OneNote.

```java
Document doc = new Document();
```

### Bước 3: Khởi tạo đối tượng Page
Một tệp OneNote bao gồm một hoặc nhiều trang; ở đây chúng ta bắt đầu với một trang duy nhất.

```java
Page page = new Page();
```

### Bước 4: Khởi tạo đối tượng Outline
Outline hoạt động như các container cho các phần outline (tưởng như các mục).

```java
Outline outline = new Outline();
```

### Bước 5: Khởi tạo đối tượng OutlineElement
Ở đây chúng ta **add outline element** mà sẽ chứa văn bản giàu định dạng của chúng ta.

```java
OutlineElement outlineElem = new OutlineElement();
```

### Bước 6: Đặt kiểu văn bản (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Đối tượng `ParagraphStyle` xác định phông chữ, kích thước và màu sắc — đây là nơi chúng ta **set paragraph style** cho nút văn bản sắp tới.

### Bước 7: Khởi tạo đối tượng RichText

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Chúng ta tạo một nút `RichText`, chèn một chuỗi đơn giản, và gắn kiểu đã định nghĩa trước đó.

### Bước 8: Thêm nút RichText vào OutlineElement

```java
outlineElem.appendChildLast(text);
```

Bây giờ văn bản đã được định dạng nằm trong phần tử outline.

### Bước 9: Thêm nút OutlineElement vào Outline

```java
outline.appendChildLast(outlineElem);
```

Outline hiện chứa phần tử giữ đoạn văn của chúng ta.

### Bước 10: Thêm nút Outline vào Page

```java
page.appendChildLast(outline);
```

Chúng ta đặt outline lên trang.

### Bước 11: Thêm nút Page vào Document

```java
doc.appendChildLast(page);
```

Tài liệu hiện có một trang duy nhất với văn bản đã được định dạng.

### Bước 12: Lưu tài liệu (Export OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Phương thức `save` ghi tệp OneNote và **export OneNote PDF** trong một bước. Bạn cũng có thể lưu dưới dạng `.one` bằng cách sử dụng `SaveFormat.One` nếu cần định dạng gốc.

## Các vấn đề thường gặp & Giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| **File không tồn tại** | `dataDir` trỏ tới thư mục không có. | Đảm bảo thư mục tồn tại hoặc tạo nó bằng chương trình (`new File(dataDir).mkdirs();`). |
| **PDF trắng** | Không có nội dung nào được thêm trước khi lưu. | Kiểm tra xem nút `RichText` đã được thêm và kiểu đã được đặt chưa. |
| **Phông chữ không được hỗ trợ** | Tên phông không được cài đặt trên hệ thống. | Sử dụng phông chung như `"Arial"` hoặc nhúng phông vào dự án. |

## Câu hỏi thường gặp

**Hỏi: Aspose.Note có thể xử lý định dạng phức tạp như bảng hoặc hình ảnh không?**  
Đáp: Có, API hỗ trợ bảng, hình ảnh, siêu liên kết và các tính năng bố cục nâng cao khác.

**Hỏi: Có thể **convert OneNote PDF** lại thành tệp OneNote không?**  
Đáp: Chuyển đổi trực tiếp không được cung cấp, nhưng bạn có thể trích xuất nội dung PDF và xây dựng lại tài liệu OneNote bằng API.

**Hỏi: Thư viện có hoạt động trên môi trường Linux/macOS không?**  
Đáp: Hoàn toàn có. Aspose.Note cho Java không phụ thuộc vào nền tảng; chỉ cần cài đặt JDK.

**Hỏi: Làm sao để thêm nhiều trang hoặc outline?**  
Đáp: Tạo thêm các đối tượng `Page` và `Outline`, sau đó thêm chúng vào `Document` giống như ví dụ một trang.

**Hỏi: Tôi có thể tìm thêm ví dụ ở đâu?**  
Đáp: Tài liệu chính thức của Aspose.Note và [diễn đàn hỗ trợ](https://forum.aspose.com/c/note/28) có nhiều mẫu mã.

## Kết luận

Bạn đã thấy cách **set paragraph style**, **add outline element**, và **generate a OneNote file** có thể **export to PDF** bằng Aspose.Note cho Java. Việc áp dụng văn bản có định dạng ngay từ đầu giúp tài liệu cuối cùng trông chuyên nghiệp và bất kỳ thao tác **convert OneNote PDF** nào sau này cũng giữ nguyên định dạng. Hãy mở rộng nền tảng này với hình ảnh, bảng hoặc siêu dữ liệu tùy chỉnh để đáp ứng nhu cầu dự án của bạn.

---

**Cập nhật lần cuối:** 2026-02-18  
**Đã kiểm tra với:** Aspose.Note for Java 24.11 (bản phát hành mới nhất)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}