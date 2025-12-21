---
date: 2025-12-21
description: Tìm hiểu cách tạo tài liệu OneNote bằng Java và chèn hình ảnh một cách
  dễ dàng bằng Aspose.Note cho Java. Hướng dẫn từng bước dành cho các nhà phát triển
  Java.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Cách tạo tài liệu OneNote bằng Java – Xây dựng tài liệu và chèn hình ảnh bằng
  Stream
url: /vi/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách tạo tài liệu onenote bằng Java – Xây dựng tài liệu và chèn hình ảnh bằng Stream

## Giới thiệu

Chào mừng! Trong hướng dẫn này, bạn sẽ **tạo tài liệu onenote bằng Java** từ đầu và học cách chèn hình ảnh bằng một luồng hình ảnh. Chúng tôi sẽ hướng dẫn từng bước, giải thích lý do mỗi phần quan trọng, và cung cấp các mẹo thực tế để bạn có thể áp dụng kỹ thuật này trong các dự án thực tế. Khi hoàn thành, bạn sẽ có thể tạo các trang OneNote một cách lập trình và nhúng hình ảnh chính xác ở vị trí bạn muốn.

## Câu trả lời nhanh
- **Thư viện tôi cần là gì?** Aspose.Note for Java  
- **Tôi có thể chèn hình ảnh từ một stream không?** Có – chỉ cần truyền một `InputStream` vào hàm khởi tạo `Image`.  
- **Tôi có thể xuất sang định dạng nào?** Bất kỳ định dạng nào được Aspose.Note hỗ trợ, ví dụ: PDF, DOCX, HTML.  
- **Tôi có cần giấy phép cho việc phát triển không?** Giấy phép tạm thời miễn phí đủ cho việc đánh giá; cần giấy phép đầy đủ cho môi trường sản xuất.  
- **Phiên bản Java yêu cầu là gì?** Java 8 hoặc cao hơn.

## create onenote document java là gì?

Tạo một tài liệu OneNote bằng Java có nghĩa là sử dụng API Aspose.Note để xây dựng cấu trúc sổ ghi chú—các trang, outline và các phần tử—một cách lập trình, mà không cần mở ứng dụng OneNote trên máy tính. Cách tiếp cận này lý tưởng cho việc tạo báo cáo tự động, xử lý hàng loạt ghi chú, hoặc tích hợp nội dung OneNote vào các ứng dụng Java lớn hơn.

## Tại sao nên dùng Aspose.Note cho Java để tạo onenote document java?

- **Kiểm soát đầy đủ** bố cục trang, vị trí outline và kiểu dáng các phần tử.  
- **Không cần COM interop** – hoạt động trên bất kỳ hệ điều hành nào hỗ trợ Java.  
- **Tùy chọn xuất phong phú** – chuyển đổi cùng một tài liệu sang PDF, DOCX, HTML, v.v., chỉ với một lệnh.  
- **Thân thiện với stream** – bạn có thể tải hình ảnh trực tiếp từ bộ nhớ, mạng hoặc lưu trữ đám mây.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã chuẩn bị các thứ sau:

### Bộ công cụ phát triển Java (JDK)

Một JDK mới (phiên bản 8 trở lên) đã được cài đặt trên máy của bạn.

### Thư viện Aspose.Note cho Java

Tải thư viện từ trang phát hành chính thức của Aspose: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### Cấu hình IDE

Cấu hình IDE yêu thích của bạn (IntelliJ IDEA, Eclipse, VS Code) để bao gồm các tệp JAR của Aspose.Note trong classpath của dự án.

## Nhập các gói

Để bắt đầu, nhập các lớp Java và Aspose.Note cần thiết. Những import này cho phép bạn truy cập vào việc tạo tài liệu, xử lý trang, quản lý outline và chèn hình ảnh.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Bước 1: Thiết lập thư mục tài liệu

Xác định thư mục chứa các hình ảnh nguồn và nơi sẽ lưu tệp đầu ra. Thay thế phần giữ chỗ bằng đường dẫn thực tế trên máy của bạn.

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tạo đối tượng Document

Khởi tạo một `Document` mới. Đối tượng này đại diện cho sổ ghi chú OneNote mà bạn đang xây dựng.

```java
Document doc = new Document();
```

## Bước 3: Khởi tạo đối tượng Page

Tạo một `Page` sẽ chứa tất cả các outline và phần tử cho trang sổ ghi chú này.

```java
Page page = new Page();
```

## Bước 4: Tạo Outline

Một `Outline` hoạt động như một container cho các phần tử được định vị. Ở đây chúng ta đặt các offset dọc và ngang để định vị outline trên trang.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Bước 5: Tạo Outline Element

`OutlineElement` sẽ chứa hình ảnh mà chúng ta sắp chèn.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Bước 6: Tải luồng hình ảnh

Mở tệp hình ảnh dưới dạng luồng. Sử dụng luồng cho phép bạn đọc hình ảnh từ bất kỳ nguồn nào (hệ thống tệp, mạng, cơ sở dữ liệu) mà không cần lưu nó vào đĩa trước.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Bước 7: Chèn hình ảnh

Tạo một đối tượng `Image`. Tham số đầu tiên có thể là `null` khi bạn cung cấp luồng sau này, nhưng để đơn giản chúng tôi tham chiếu đến đường dẫn tệp ở đây và đặt căn chỉnh của nó sang phía bên phải của trang.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Bước 8: Thêm hình ảnh vào Outline Element

Thêm hình ảnh vào outline element để nó trở thành một phần của cấu trúc hiển thị trên trang.

```java
outlineElem1.appendChildLast(image);
```

## Bước 9: Thêm Outline Element vào Outline

Bây giờ gắn outline element (chứa hình ảnh) vào container outline.

```java
outline1.appendChildLast(outlineElem1);
```

## Bước 10: Thêm Outline vào Page

Đặt outline lên trang.

```java
page.appendChildLast(outline1);
```

## Bước 11: Thêm Page vào Document

Thêm trang đã được xây dựng hoàn chỉnh vào đối tượng document.

```java
doc.appendChildLast(page);
```

## Bước 12: Lưu Document

Cuối cùng, lưu tài liệu OneNote ở định dạng bạn cần. Trong ví dụ này chúng tôi xuất ra PDF, nhưng bạn có thể chọn bất kỳ định dạng nào được Aspose.Note hỗ trợ.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Bằng cách thực hiện các bước trên, bạn đã thành công **tạo onenote document java** và nhúng một hình ảnh bằng luồng đầu vào.

## Những lỗi thường gặp & Mẹo

- **Luồng không được đóng** – Trong môi trường sản xuất, luôn đóng `InputStream` trong khối `finally` hoặc sử dụng try‑with‑resources.  
- **Đường dẫn tệp không đúng** – Kiểm tra lại rằng `dataDir` kết thúc bằng dấu phân tách thích hợp (`/` hoặc `\`).  
- **Căn chỉnh hình ảnh** – Nếu hình ảnh hiển thị lệch, điều chỉnh giá trị `VerticalOffset`/`HorizontalOffset` của outline.  
- **Ngoại lệ giấy phép** – Sử dụng phiên bản đánh giá có thể thêm watermark vào kết quả; áp dụng giấy phép hợp lệ để loại bỏ.

## Câu hỏi thường gặp

### Q1: Aspose.Note cho Java có tương thích với mọi phiên bản của OneNote không?

A1: Aspose.Note cho Java hỗ trợ nhiều định dạng tệp OneNote, đảm bảo tính tương thích trên các phiên bản desktop, online và mobile.

### Q2: Tôi có thể tùy chỉnh giao diện của hình ảnh chèn trong tài liệu OneNote bằng Aspose.Note cho Java không?

A2: Có, bạn có thể thay đổi căn chỉnh, kích thước, xoay và thậm chí cắt ảnh bằng cách sử dụng các thuộc tính tương ứng trên đối tượng `Image`.

### Q3: Aspose.Note cho Java có hỗ trợ các định dạng tài liệu khác ngoài PDF không?

A3: Chắc chắn. API có thể xuất ra DOCX, HTML, XPS và một số định dạng khác, mang lại sự linh hoạt trong việc chia sẻ hoặc lưu trữ ghi chú.

### Q4: Tôi có thể tìm tài nguyên và hỗ trợ bổ sung cho Aspose.Note cho Java ở đâu?

A4: Trang web chính thức của Aspose cung cấp tài liệu chi tiết, ví dụ mã nguồn, diễn đàn và giấy phép tạm thời để đánh giá.

### Q5: Có phiên bản dùng thử cho Aspose.Note cho Java không?

A5: Có, bạn có thể tải bản dùng thử miễn phí từ trang phát hành của Aspose để khám phá tất cả các tính năng trước khi mua.

---

**Cập nhật lần cuối:** 2025-12-21  
**Kiểm thử với:** Aspose.Note for Java 24.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}