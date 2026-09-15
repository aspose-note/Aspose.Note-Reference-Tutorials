---
date: 2026-03-05
description: Tìm hiểu cách lưu OneNote dưới dạng PDF trong khi tạo danh sách đánh
  số bằng Aspose.Note cho Java. Bao gồm các bước thiết lập kiểu văn bản mặc định và
  tùy chỉnh đánh số.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: Lưu OneNote dưới dạng PDF – Tạo danh sách đánh số với Aspose.Note
url: /vi/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu OneNote dưới dạng PDF – Tạo Danh sách Đánh số với Aspose.Note

## Giới thiệu
Aspose.Note for Java cung cấp cho các nhà phát triển Java khả năng **lưu OneNote dưới dạng PDF** và làm phong phú tài liệu với định dạng nâng cao, chẳng hạn như danh sách đánh số. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình hoàn chỉnh — từ việc thiết lập kiểu văn bản mặc định đến tùy chỉnh định dạng đánh số — để bạn có thể xuất OneNote sang PDF với giao diện chuyên nghiệp.

## Câu trả lời nhanh
- **Hướng dẫn này đề cập đến gì?** Tạo danh sách đánh số trong OneNote và lưu tệp dưới dạng PDF bằng Aspose.Note for Java.  
- **Từ khóa chính được nhắm tới là gì?** *save onenote as pdf*  
- **Có cần giấy phép không?** Có bản dùng thử miễn phí; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Yêu cầu phiên bản Java nào?** JDK 8 trở lên.  
- **Thời gian triển khai khoảng bao lâu?** Khoảng 10–15 phút cho một danh sách cơ bản.

## “Lưu OneNote dưới dạng PDF” là gì?
Lưu OneNote dưới dạng PDF chuyển trang OneNote dạng văn bản phong phú thành tài liệu cố định, có thể mang theo và chia sẻ trên mọi nền tảng mà không cần cài đặt OneNote. Điều này rất hữu ích cho việc lưu trữ, báo cáo hoặc phân phối nội dung cho người dùng không có OneNote.

## Tại sao cần tạo danh sách đánh số trước khi xuất?
Danh sách đánh số giúp cấu trúc và tăng khả năng đọc, khiến PDF xuất ra trông giống như một báo cáo được biên soạn kỹ lưỡng. Với Aspose.Note, bạn có thể **tùy chỉnh định dạng đánh số**, đặt phông chữ và kiểm soát khoảng cách — tất cả vẫn giữ nguyên bố cục gốc của OneNote.

## Yêu cầu trước
Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

- Java Development Kit (JDK) được cài đặt trên máy tính.  
- Thư viện Aspose.Note for Java tải về từ [here](https://releases.aspose.com/note/java/).  

## Nhập khẩu các gói
Đầu tiên, nhập các lớp cần thiết để làm việc với các đối tượng OneNote và chuyển đổi sang PDF.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## Cách lưu OneNote dưới dạng PDF với danh sách đánh số?
Dưới đây là hướng dẫn từng bước cho thấy **cách tạo các phần tử danh sách**, **đặt kiểu văn bản mặc định**, và cuối cùng **xuất OneNote sang PDF**.

### Bước 1: Khởi tạo các đối tượng Document, Page và Outline
Chúng ta bắt đầu bằng việc tạo các cấu trúc cốt lõi của OneNote. Điều này cũng minh họa cách sử dụng **add outline element java**.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Mẹo:** Giữ đường dẫn `dataDir` ở dạng tuyệt đối hoặc dùng `System.getProperty("user.dir")` để tránh các vấn đề về đường dẫn.

### Bước 2: Đặt Kiểu Văn bản Mặc định
Kiểu thống nhất giúp danh sách trông đồng nhất trên mọi mục.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Bước 3: Tạo Các Phần tử Outline (Danh sách Đánh số)
Ở đây chúng ta **tùy chỉnh định dạng đánh số** bằng `NumberList`. Mẫu `"{0})"` sẽ tạo ra “1)”, “2)”, v.v.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Tại sao lại quan trọng:** Khi gắn một `NumberList` vào mỗi `OutlineElement`, bạn có toàn quyền kiểm soát kiểu đánh số, phông chữ và kích thước.

### Bước 4: Thêm Các Phần tử Outline vào Outline
Bây giờ chúng ta gộp các mục danh sách riêng lẻ thành một outline duy nhất.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Bước 5: Gắn Outline vào Page
Outline sẽ trở thành một phần của cấu trúc trang OneNote.

```java
page.appendChildLast(outline);
```

### Bước 6: Lưu Tài liệu dưới dạng PDF
Cuối cùng, chúng ta **lưu OneNote dưới dạng PDF**. Tệp đầu ra sẽ chứa danh sách đánh số đúng như đã định nghĩa.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

Chạy đoạn mã trên sẽ tạo ra một PDF có tên `CreateNumberedList_out.pdf` trong thư mục bạn chỉ định, giữ nguyên định dạng danh sách đánh số.

## Các vấn đề thường gặp & Giải pháp
| Vấn đề | Giải pháp |
|-------|----------|
| **PDF trống** | Đảm bảo gọi `doc.appendChildLast(page);` trước khi `doc.save()`. |
| **Không hiển thị số thứ tự** | Kiểm tra lại mẫu `NumberList` và `NumberFormat` đã được thiết lập đúng chưa. |
| **Lỗi không tìm thấy tệp** | Sử dụng đường dẫn tuyệt đối cho `dataDir` hoặc tạo thư mục trước khi lưu. |
| **Phông chữ không khớp** | Cài đặt phông chữ (ví dụ: Arial) trên máy chạy mã. |

## Câu hỏi thường gặp
### H: Tôi có thể tùy chỉnh định dạng đánh số trong danh sách OneNote của mình không?
Đ: Chắc chắn! Bạn có thể tùy chỉnh định dạng đánh số bằng lớp `NumberList` được cung cấp bởi Aspose.Note for Java.

### H: Có phiên bản dùng thử cho Aspose.Note for Java không?
Đ: Có, bạn có thể tải bản dùng thử miễn phí [here](https://releases.aspose.com/).

### H: Làm sao tôi có thể nhận hỗ trợ cho Aspose.Note for Java?
Đ: Truy cập diễn đàn [Aspose.Note for Java forum](https://forum.aspose.com/c/note/28) để nhận hỗ trợ cộng đồng.

### H: Tôi có thể tìm tài liệu chi tiết cho Aspose.Note for Java ở đâu?
Đ: Tham khảo [documentation](https://reference.aspose.com/note/java/) để có thông tin đầy đủ.

### H: Làm thế nào để mua giấy phép cho Aspose.Note for Java?
Đ: Bạn có thể mua giấy phép [here](https://purchase.aspose.com/buy).

## Kết luận
Trong hướng dẫn này, chúng tôi đã trình bày cách **lưu OneNote dưới dạng PDF** đồng thời tạo một danh sách đánh số sạch sẽ bằng Aspose.Note for Java. Bằng cách thiết lập kiểu văn bản mặc định, tùy chỉnh định dạng đánh số và làm theo các bước hướng dẫn, bạn có thể nhanh chóng và đáng tin cậy tạo ra các PDF chuyên nghiệp từ các trang OneNote.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2026-03-05  
**Kiểm tra với:** Aspose.Note for Java 24.11  
**Tác giả:** Aspose  

---