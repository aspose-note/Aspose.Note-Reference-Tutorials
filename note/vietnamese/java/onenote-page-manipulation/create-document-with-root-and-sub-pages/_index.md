---
date: 2026-04-30
description: Tìm hiểu cách **lưu OneNote dưới dạng PDF** và thêm các trang con trong
  OneNote bằng Aspose.Note cho Java. Hãy làm theo hướng dẫn từng bước này để tổ chức
  ghi chú của bạn một cách hiệu quả.
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: Cách lưu OneNote dưới dạng PDF và thêm các trang con
second_title: Aspose.Note Java API
title: Cách lưu OneNote dưới dạng PDF và thêm các trang phụ
url: /vi/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách lưu OneNote dưới dạng PDF và Thêm các Trang con

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách lưu onenote dưới dạng pdf** trong khi tạo một tài liệu chứa cả các trang gốc và trang con bằng Aspose.Note for Java. Việc tổ chức các sổ tay OneNote của bạn với một cấu trúc phân cấp rõ ràng giúp việc điều hướng trở nên dễ dàng, và xuất ra PDF đảm bảo bạn có thể chia sẻ ghi chú của mình ở định dạng có thể đọc được trên mọi nền tảng. Chúng tôi cũng sẽ chỉ cho bạn cách **thêm các trang con onenote** theo kiểu, để bạn có thể xây dựng các cấu trúc đa cấp một cách dễ dàng.

## Câu trả lời nhanh
- **Câu hỏi “save onenote as pdf” có nghĩa là gì?** Nó đề cập đến việc xuất một sổ tay OneNote ra file PDF bằng cách sử dụng Aspose.Note for Java.  
- **API nào được yêu cầu?** Aspose.Note for Java cung cấp các lớp và phương thức cần thiết.  
- **Tôi có thể tạo các trang phân cấp không?** Có – đặt mức độ trang để tạo các trang gốc và trang con.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Có phiên bản dùng thử miễn phí, nhưng giấy phép thương mại cần thiết cho việc sử dụng trong môi trường sản xuất.  
- **Các định dạng nào tôi có thể xuất ra?** Ngoài PDF, bạn có thể xuất ra BMP, PNG, JPEG, DOCX và nhiều định dạng khác.

## Cách lưu OneNote dưới dạng PDF

Lưu OneNote dưới dạng PDF chuyển đổi mỗi trang sổ tay thành một tài liệu có bố cục cố định, giữ nguyên định dạng, hình ảnh và cấu trúc phân cấp của trang. Điều này lý tưởng cho việc chia sẻ, lưu trữ hoặc in ấn ghi chú trong khi vẫn giữ nguyên cấu trúc gốc.

## Tại sao thêm các trang con onenote?

Thêm các trang con cho phép bạn nhóm nội dung liên quan dưới một trang cha, mô phỏng cấu trúc giống thư mục. Nó cải thiện việc tổ chức ghi chú, tăng tốc tìm kiếm và nâng cao trải nghiệm đọc khi sổ tay được xuất ra PDF.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn đã có các yêu cầu sau:

1. **Java Development Kit (JDK)** – Đảm bảo rằng bạn đã cài đặt JDK trên hệ thống của mình.  
2. **Aspose.Note for Java** – Tải xuống và cài đặt Aspose.Note for Java từ [website](https://purchase.aspose.com/buy).  
3. **Integrated Development Environment (IDE)** – Chọn một IDE Java như IntelliJ IDEA, Eclipse hoặc NetBeans.

## Nhập các gói

Bắt đầu bằng việc nhập các gói cần thiết vào dự án Java của bạn:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Bước 1: Thiết lập thư mục tài liệu

Xác định thư mục nơi bạn muốn lưu tài liệu OneNote của mình:

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tạo đối tượng Document

Tạo một đối tượng `Document`:

```java
Document doc = new Document();
```

## Bước 3: Tạo các trang

Khởi tạo các đối tượng trang và đặt mức độ của chúng. Việc đặt mức độ xác định một trang là trang gốc hay trang con:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Bước 4: Thêm các nút vào các trang

### Thêm các nút vào Trang đầu tiên

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Thêm các nút vào Trang thứ hai

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Thêm các nút vào Trang thứ ba

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Bước 5: Thêm các trang vào tài liệu

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Bước 6: Lưu tài liệu

Lưu tài liệu OneNote dưới dạng PDF (hoặc BMP trong ví dụ này). Thay đổi `SaveFormat` cho phép bạn xuất ra PDF, đáp ứng yêu cầu “save onenote as pdf”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Mẹo chuyên nghiệp:** Để xuất trực tiếp sang PDF, thay thế `SaveFormat.Bmp` bằng `SaveFormat.Pdf`.

Chúc mừng! Bạn đã tạo thành công một tài liệu OneNote với các trang gốc và trang con và đã học được **cách lưu onenote dưới dạng pdf** bằng cách sử dụng Aspose.Note for Java.

## Tại sao điều này quan trọng

- **Tổ chức phân cấp:** Các trang gốc và trang con cho phép bạn mô phỏng cấu trúc thư mục bên trong OneNote.  
- **Xuất PDF liền mạch:** Khi đã được tổ chức, việc xuất ra PDF giữ nguyên cấu trúc phân cấp, làm cho tài liệu cuối cùng dễ đọc và chia sẻ.  
- **Tự động hóa:** Mã có thể được tích hợp vào các ứng dụng Java lớn hơn, cho phép tạo hàng loạt sổ tay có cấu trúc.

## Những lỗi thường gặp & Cách tránh

| Issue | Cause | Solution |
|-------|-------|----------|
| Các trang xuất hiện ở cùng mức độ | Giá trị `setLevel` không đúng | Sử dụng `setLevel((byte) 1)` cho các trang gốc và `setLevel((byte) 2)` (hoặc cao hơn) cho các trang con. |
| Kết quả PDF trông trống | Thiếu `SaveFormat.Pdf` hoặc đường dẫn tệp không đúng | Kiểm tra thư mục tồn tại và sử dụng `SaveFormat.Pdf`. |
| Phông chữ không được áp dụng | Tên phông chữ sai hoặc thiếu phông chữ trên hệ thống | Đảm bảo phông chữ (ví dụ, “David Transparent”) được cài đặt trên máy chạy mã. |

## Câu hỏi thường gặp

**Q: Tôi có thể tạo nhiều cấp độ của các trang con bằng Aspose.Note cho Java không?**  
A: Có, bạn có thể tạo các cấu trúc phân cấp sâu hơn bằng cách đặt số mức độ cao hơn (ví dụ, `setLevel((byte) 3)` cho một trang con cấp ba).

**Q: Aspose.Note cho Java có tương thích với các IDE Java khác nhau không?**  
A: Chắc chắn. Nó hoạt động với IntelliJ IDEA, Eclipse, NetBeans và bất kỳ IDE nào hỗ trợ phát triển Java.

**Q: Tôi có thể tùy chỉnh định dạng văn bản trong tài liệu OneNote của mình không?**  
A: Có. Sử dụng `ParagraphStyle` để đặt tên phông chữ, kích thước, màu sắc và các thuộc tính khác cho mỗi phần tử `RichText`.

**Q: Aspose.Note cho Java có hỗ trợ lưu tài liệu ở các định dạng khác ngoài BMP không?**  
A: Có. Các định dạng được hỗ trợ bao gồm PDF, PNG, JPEG, DOCX và nhiều hơn nữa. Thay đổi enum `SaveFormat` cho phù hợp.

**Q: Có phiên bản dùng thử cho Aspose.Note cho Java không?**  
A: Có, bạn có thể tải phiên bản dùng thử miễn phí từ trang web Aspose.

## Kết luận

Việc tổ chức các sổ tay OneNote của bạn với một cấu trúc phân cấp rõ ràng và xuất chúng dưới dạng PDF giúp ghi chú của bạn dễ tiếp cận và chia sẻ hơn. Bằng cách làm theo các bước trên, bạn hiện đã biết **cách lưu onenote dưới dạng pdf** và **thêm các trang con onenote** theo phong cách lập trình bằng Aspose.Note cho Java.

---

**Cập nhật lần cuối:** 2026-04-30  
**Kiểm tra với:** Aspose.Note for Java 24.11 (latest)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}