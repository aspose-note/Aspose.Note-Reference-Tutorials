---
description: Tìm hiểu cách lưu PDF OneNote và thêm các trang con trong OneNote bằng
  Aspose.Note cho Java. Hãy làm theo hướng dẫn từng bước này để tổ chức ghi chú của
  bạn một cách hiệu quả.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Cách lưu PDF từ OneNote và thêm các trang con
url: /vi/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Lưu OneNote PDF và Thêm Trang Con

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách lưu OneNote PDF** đồng thời tạo một tài liệu chứa cả trang gốc và trang con bằng Aspose.Note for Java. Việc tổ chức sổ ghi chú OneNote với cấu trúc phân cấp rõ ràng giúp việc điều hướng trở nên dễ dàng, và khả năng xuất ra PDF đảm bảo bạn có thể chia sẻ ghi chú dưới định dạng mà mọi người đều đọc được. Chúng tôi cũng sẽ chỉ cho bạn **cách thêm sub pages onenote** theo phong cách, để bạn có thể xây dựng cấu trúc đa cấp một cách dễ dàng.

## Trả lời nhanh
- **Từ khóa chính có nghĩa là gì?** Nó đề cập đến việc xuất một sổ OneNote ra PDF bằng Aspose.Note.  
- **API nào được sử dụng?** Aspose.Note for Java.  
- **Tôi có thể tạo các trang phân cấp không?** Có – đặt mức độ trang để xây dựng trang gốc và trang con.  
- **Có cần giấy phép không?** Có bản dùng thử miễn phí; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Các định dạng đầu ra được hỗ trợ là gì?** BMP, PDF, PNG và nhiều hơn nữa.

## “cách lưu OneNote PDF” là gì?
Lưu OneNote dưới dạng PDF chuyển các trang của sổ ghi chú thành một tài liệu bố cục cố định, giữ nguyên định dạng, hình ảnh và cấu trúc phân cấp. Điều này lý tưởng để chia sẻ, lưu trữ hoặc in ấn ghi chú.

## Tại sao cần thêm sub pages onenote?
Thêm trang con cho phép bạn nhóm nội dung liên quan dưới một trang cha, giống như cấu trúc thư mục. Nó cải thiện việc tổ chức ghi chú, tăng tốc tìm kiếm và nâng cao trải nghiệm đọc khi sổ ghi chú được xuất ra PDF.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có các yêu cầu sau:

1. Java Development Kit (JDK): Đảm bảo JDK đã được cài đặt trên hệ thống của bạn.  
2. Aspose.Note for Java: Tải và cài đặt Aspose.Note for Java từ [website](https://purchase.aspose.com/buy).  
3. Integrated Development Environment (IDE): Chọn một IDE Java như IntelliJ IDEA, Eclipse hoặc NetBeans.

## Nhập gói

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

Xác định thư mục nơi bạn muốn lưu tài liệu OneNote:

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tạo đối tượng Document

Khởi tạo một đối tượng `Document`:

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

## Bước 4: Thêm Nodes vào các trang

### Thêm Nodes vào Trang Đầu Tiên

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

### Thêm Nodes vào Trang Thứ Hai

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

### Thêm Nodes vào Trang Thứ Ba

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

## Bước 5: Thêm các trang vào Document

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Bước 6: Lưu tài liệu

Lưu tài liệu OneNote dưới dạng PDF (hoặc BMP trong ví dụ này). Thay đổi `SaveFormat` cho phép bạn xuất ra PDF, đáp ứng yêu cầu “cách lưu OneNote PDF”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Mẹo chuyên nghiệp:** Để xuất trực tiếp ra PDF, thay `SaveFormat.Bmp` bằng `SaveFormat.Pdf`.

Chúc mừng! Bạn đã tạo thành công một tài liệu OneNote với các trang gốc và trang con và học được **cách lưu OneNote PDF** bằng Aspose.Note for Java.

## Tại sao điều này quan trọng

- **Tổ chức phân cấp:** Trang gốc và trang con cho phép bạn mô phỏng cấu trúc thư mục bên trong OneNote.  
- **Xuất PDF liền mạch:** Khi đã được tổ chức, việc xuất ra PDF giữ nguyên phân cấp, giúp tài liệu cuối cùng dễ đọc và chia sẻ.  
- **Tự động hoá:** Mã có thể được tích hợp vào các ứng dụng Java lớn hơn, cho phép tạo hàng loạt sổ ghi chú có cấu trúc.

## Những lỗi thường gặp & Cách tránh

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|-----------|
| Các trang xuất hiện ở cùng mức độ | Giá trị `setLevel` không đúng | Sử dụng `setLevel((byte) 1)` cho trang gốc và `setLevel((byte) 2)` (hoặc cao hơn) cho trang con. |
| Đầu ra PDF trống | Thiếu `SaveFormat.Pdf` hoặc đường dẫn tệp không đúng | Kiểm tra thư mục tồn tại và sử dụng `SaveFormat.Pdf`. |
| Phông chữ không áp dụng | Tên phông chữ sai hoặc phông chưa được cài trên hệ thống | Đảm bảo phông (ví dụ: “David Transparent”) đã được cài trên máy chạy mã. |

## Câu hỏi thường gặp

**H: Tôi có thể tạo nhiều cấp độ trang con bằng Aspose.Note for Java không?**  
Đ: Có, bạn có thể tạo cấu trúc sâu hơn bằng cách đặt số mức độ cao hơn (ví dụ: `setLevel((byte) 3)` cho trang con cấp ba).

**H: Aspose.Note for Java có tương thích với các IDE Java khác nhau không?**  
Đ: Hoàn toàn. Nó hoạt động với IntelliJ IDEA, Eclipse, NetBeans và bất kỳ IDE nào hỗ trợ phát triển Java.

**H: Tôi có thể tùy chỉnh định dạng văn bản trong tài liệu OneNote không?**  
Đ: Có. Sử dụng `ParagraphStyle` để đặt tên phông, kích thước, màu và các thuộc tính khác cho mỗi phần tử `RichText`.

**H: Aspose.Note for Java có hỗ trợ lưu tài liệu ở các định dạng khác BMP không?**  
Đ: Có. Các định dạng được hỗ trợ bao gồm PDF, PNG, JPEG, DOCX và nhiều hơn nữa. Thay đổi enum `SaveFormat` cho phù hợp.

**H: Có phiên bản dùng thử cho Aspose.Note for Java không?**  
Đ: Có, bạn có thể tải bản dùng thử miễn phí từ trang web Aspose.

## Kết luận

Việc tổ chức sổ ghi chú OneNote với cấu trúc phân cấp rõ ràng và xuất chúng dưới dạng PDF giúp ghi chú của bạn trở nên dễ tiếp cận và chia sẻ hơn. Bằng cách làm theo các bước trên, bạn đã biết **cách lưu OneNote PDF** và **thêm sub pages onenote** một cách lập trình bằng Aspose.Note for Java.

---

**Cập nhật lần cuối:** 2026-01-07  
**Được kiểm tra với:** Aspose.Note for Java 24.11 (mới nhất)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}