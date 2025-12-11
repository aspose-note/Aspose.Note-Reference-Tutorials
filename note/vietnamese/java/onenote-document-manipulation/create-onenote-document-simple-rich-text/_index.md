---
date: 2025-12-08
description: Tìm hiểu cách đặt kiểu đoạn văn và thêm phần tử đề mục khi tạo tài liệu
  OneNote bằng Java sử dụng Aspose.Note. Xuất OneNote sang PDF và tạo tệp OneNote
  một cách dễ dàng.
language: vi
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: Đặt kiểu đoạn văn khi tạo tài liệu OneNote bằng Java
url: /java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt Kiểu Đoạn Văn khi Tạo Tài liệu OneNote bằng Java

## Giới thiệu

Trong môi trường phát triển nhanh ngày nay, khả năng **đặt kiểu đoạn văn** một cách lập trình là rất cần thiết để tạo ra các tệp OneNote chuyên nghiệp. Hướng dẫn này sẽ chỉ cho bạn, từng bước một, cách tạo một tài liệu OneNote với văn bản giàu định dạng đơn giản, áp dụng định dạng đoạn văn tùy chỉnh, và cuối cùng **xuất OneNote ra PDF** bằng Aspose.Note cho Java. Dù bạn đang xây dựng một công cụ báo cáo, một giải pháp ghi chú tự động, hay một dịch vụ chuyển đổi tài liệu, các kỹ thuật ở đây sẽ giúp bạn **tạo tệp OneNote** trông đúng như mong muốn.

## Trả lời nhanh
- **“đặt kiểu đoạn văn” có nghĩa là gì?** Nó áp dụng phông chữ, kích thước, màu sắc và các định dạng khác cho một đoạn văn bản.  
- **Tôi có thể xuất kết quả ra PDF không?** Có – hướng dẫn kết thúc bằng việc lưu tệp OneNote dưới dạng PDF.  
- **Có cần giấy phép cho Aspose.Note không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép cần thiết cho môi trường sản xuất.  
- **Những IDE nào được hỗ trợ?** Bất kỳ IDE Java nào – Eclipse, IntelliJ IDEA, NetBeans, v.v.  
- **Thời gian thực hiện khoảng bao lâu?** Khoảng 10‑15 phút cho một tài liệu cơ bản.

## “đặt kiểu đoạn văn” trong Aspose.Note là gì?
Đặt kiểu đoạn văn đề cập đến việc cấu hình một đối tượng `ParagraphStyle` (tên phông, kích thước, màu sắc, v.v.) và gắn nó vào một nút `RichText`. Điều này cho phép bạn kiểm soát hoàn toàn cách văn bản hiển thị trong một trang OneNote.

## Tại sao cần đặt kiểu đoạn văn khi tạo tệp OneNote?
- **Nhận diện thương hiệu đồng nhất:** Tự động áp dụng phông chữ và màu sắc công ty.  
- **Độ dễ đọc:** Phông chữ lớn hơn hoặc màu sắc đặc biệt cải thiện khả năng truy cập.  
- **Độ trung thực khi xuất:** Văn bản đã định dạng sẽ được giữ nguyên khi bạn **chuyển đổi OneNote PDF** sau này.  

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

1. **Java Development Kit (JDK) 1.8+** – bất kỳ JDK hiện đại nào đều hoạt động.  
2. **Aspose.Note for Java** – tải JAR mới nhất từ [trang tải Aspose.Note](https://releases.aspose.com/note/java/).  
3. **Một IDE** (Eclipse, IntelliJ IDEA hoặc NetBeans) để biên dịch và chạy mẫu.  

> **Mẹo chuyên nghiệp:** Thêm JAR Aspose.Note vào classpath của dự án qua Maven hoặc bằng cách tham chiếu thủ công JAR trong IDE.

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

> Lớp `ParagraphStyle` là chìa khóa để **đặt kiểu đoạn văn** sau này trong hướng dẫn.

## Hướng dẫn từng bước

Dưới đây là quy trình ngắn gọn cho mỗi thao tác. Các khối mã giữ nguyên như mẫu gốc; chúng tôi chỉ thêm phần giải thích.

### Bước 1: Đặt Thư mục Tài liệu
Xác định nơi các tệp được tạo sẽ được lưu.

```java
String dataDir = "Your Document Directory";
```

Thay `"Your Document Directory"` bằng đường dẫn tuyệt đối hoặc tương đối trên máy của bạn.

### Bước 2: Khởi tạo Đối tượng Document
Tạo đối tượng `Document` gốc đại diện cho tệp OneNote.

```java
Document doc = new Document();
```

### Bước 3: Khởi tạo Đối tượng Page
Một tệp OneNote gồm một hoặc nhiều trang; chúng ta bắt đầu với một trang duy nhất.

```java
Page page = new Page();
```

### Bước 4: Khởi tạo Đối tượng Outline
Outline hoạt động như các container cho các phần outline (tưởng như các mục).

```java
Outline outline = new Outline();
```

### Bước 5: Khởi tạo Đối tượng OutlineElement
Ở đây chúng ta **thêm outline element** sẽ chứa văn bản giàu định dạng của chúng ta.

```java
OutlineElement outlineElem = new OutlineElement();
```

### Bước 6: Đặt Kiểu Văn bản (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Đối tượng `ParagraphStyle` xác định phông chữ, kích thước và màu sắc — đây là nơi chúng ta **đặt kiểu đoạn văn** cho nút văn bản sắp tới.

### Bước 7: Khởi tạo Đối tượng RichText

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Chúng ta tạo một nút `RichText`, chèn một chuỗi đơn giản và gắn kiểu đã định nghĩa trước đó.

### Bước 8: Thêm Nút RichText vào OutlineElement

```java
outlineElem.appendChildLast(text);
```

Bây giờ văn bản đã được định dạng nằm trong outline element.

### Bước 9: Thêm Nút OutlineElement vào Outline

```java
outline.appendChildLast(outlineElem);
```

Outline hiện chứa phần tử giữ đoạn văn của chúng ta.

### Bước 10: Thêm Nút Outline vào Page

```java
page.appendChildLast(outline);
```

Chúng ta đặt outline lên trang.

### Bước 11: Thêm Nút Page vào Document

```java
doc.appendChildLast(page);
```

Tài liệu giờ đã có một trang duy nhất với văn bản đã định dạng.

### Bước 12: Lưu Tài liệu (Xuất OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Phương thức `save` ghi tệp OneNote và **xuất OneNote PDF** trong một bước. Bạn cũng có thể lưu dưới dạng `.one` bằng cách dùng `SaveFormat.One` nếu cần định dạng gốc.

## Các vấn đề thường gặp & Giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| **File không tồn tại** | `dataDir` trỏ tới thư mục không tồn tại. | Đảm bảo thư mục tồn tại hoặc tạo nó bằng mã (`new File(dataDir).mkdirs();`). |
| **PDF trống** | Không có nội dung nào được thêm trước khi lưu. | Kiểm tra xem nút `RichText` đã được gắn và kiểu đã được đặt chưa. |
| **Phông chữ không hỗ trợ** | Tên phông không được cài đặt trên hệ thống. | Sử dụng phông chung như `"Arial"` hoặc nhúng phông vào dự án. |

## Câu hỏi thường gặp

**Hỏi: Aspose.Note có thể xử lý định dạng phức tạp như bảng hay hình ảnh không?**  
Đáp: Có, API hỗ trợ bảng, hình ảnh, siêu liên kết và các tính năng bố cục nâng cao khác.

**Hỏi: Có thể **chuyển đổi OneNote PDF** ngược lại thành tệp OneNote không?**  
Đáp: Chuyển đổi trực tiếp không được cung cấp, nhưng bạn có thể trích xuất nội dung PDF và xây dựng lại tài liệu OneNote bằng API.

**Hỏi: Thư viện có hoạt động trên môi trường Linux/macOS không?**  
Đáp: Hoàn toàn có. Aspose.Note cho Java không phụ thuộc vào nền tảng; chỉ cần cài đặt JDK.

**Hỏi: Làm sao để thêm nhiều trang hoặc outline?**  
Đáp: Tạo thêm các đối tượng `Page` và `Outline`, sau đó gắn chúng vào `Document` tương tự như ví dụ một trang.

**Hỏi: Tôi có thể tìm thêm ví dụ ở đâu?**  
Đáp: Tài liệu chính thức của Aspose.Note và [diễn đàn hỗ trợ](https://forum.aspose.com/c/note/28) có rất nhiều mẫu mã.

## Kết luận

Bạn đã thấy cách **đặt kiểu đoạn văn**, **thêm outline element**, và **tạo tệp OneNote** có thể **xuất ra PDF** bằng Aspose.Note cho Java. Việc áp dụng kiểu văn bản ngay từ đầu đảm bảo tài liệu cuối cùng trông chuyên nghiệp và bất kỳ thao tác **chuyển đổi OneNote PDF** nào sau này sẽ giữ nguyên định dạng. Hãy mở rộng nền tảng này bằng cách thêm hình ảnh, bảng hoặc siêu dữ liệu tùy chỉnh để đáp ứng nhu cầu dự án của bạn.

---

**Cập nhật lần cuối:** 2025-12-08  
**Đã kiểm tra với:** Aspose.Note for Java 24.11 (phiên bản mới nhất)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}