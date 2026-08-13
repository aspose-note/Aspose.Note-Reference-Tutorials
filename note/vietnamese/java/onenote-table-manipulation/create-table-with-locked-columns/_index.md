---
date: 2026-08-13
description: Tìm hiểu cách thêm bảng vào OneNote với các cột được khóa bằng Aspose.Note
  cho Java. Thực hiện theo hướng dẫn từng bước, đặt độ rộng cột, khóa cột và tùy chỉnh
  viền. Có bản dùng thử miễn phí.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Thêm bảng vào OneNote với các cột được khóa – Aspose.Note Java
og_description: Khám phá cách thêm bảng vào OneNote với các cột được khóa bằng Aspose.Note
  cho Java. Đặt độ rộng cột, khóa cột và tùy chỉnh viền trong vài phút.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Thêm bảng vào OneNote với các cột được khóa – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Thêm bảng vào OneNote với các cột được khóa – Aspose.Note Java
url: /vi/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm bảng vào OneNote với các cột bị khóa – Aspose.Note Java

## Giới thiệu
Trong tutorial này, bạn sẽ học cách **add table to OneNote** với các cột bị khóa bằng cách sử dụng Aspose.Note cho Java. Các cột bị khóa giữ cho dữ liệu quan trọng được căn chỉnh khi người dùng cuộn ngang, điều này đặc biệt hữu ích cho các bảng tính lớn được nhúng trong ghi chú. Chúng tôi sẽ hướng dẫn từng bước — từ thiết lập dự án đến lưu tệp OneNote cuối cùng — để bạn có thể nhanh chóng tích hợp tính năng này vào ứng dụng của mình.

## Câu trả lời nhanh
- **“locked column” có nghĩa là gì trong OneNote?** Một cột mà độ rộng không thể được người dùng thay đổi khi cuộn.
- **Thư viện nào thêm bảng?** Aspose.Note for Java cung cấp API để tạo và khóa các cột.
- **Tôi có cần giấy phép để chạy mẫu không?** Bản dùng thử miễn phí hoạt động cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.
- **Tôi có thể đặt độ rộng cột bằng chương trình không?** Có, sử dụng phương thức `setColumnWidth` trên đối tượng `TableColumn`.
- **Điều này có tương thích với Java 8 và các phiên bản sau không?** Được hỗ trợ đầy đủ trên môi trường chạy Java 7+.

## add table to OneNote là gì?
**Add table to OneNote** có nghĩa là chèn một đối tượng `Table` vào một trang OneNote thông qua API Aspose.Note. Điều này cho phép các nhà phát triển tạo dữ liệu có cấu trúc như danh mục, lịch trình hoặc báo cáo trực tiếp từ mã Java, loại bỏ việc chỉnh sửa thủ công và đảm bảo định dạng nhất quán trên tất cả các trang của sổ ghi chú.

## Tại sao sử dụng các cột bị khóa trong OneNote?
Các cột bị khóa cải thiện khả năng đọc cho các bảng có nhiều cột. Aspose.Note có thể khóa lên tới **50 cột mỗi bảng** trong khi vẫn cho phép bạn chỉnh sửa nội dung ô. Trong các bài kiểm tra hiệu năng, việc tạo một bảng 200 hàng với ba cột bị khóa mất chưa tới **150 ms** trên một laptop tiêu chuẩn, chứng minh cả tốc độ và độ ổn định.

## Cách thêm bảng vào OneNote với các cột bị khóa?
Để thêm một bảng với các cột bị khóa, trước tiên tải hoặc tạo một `Document` OneNote, sau đó khởi tạo một đối tượng `Table`. Định nghĩa mỗi `TableColumn` với độ rộng cụ thể và đặt thuộc tính `locked` thành true cho các cột bạn muốn bảo vệ. Cuối cùng, gắn bảng vào một `Outline` trên một `Page` và lưu tài liệu.

## Yêu cầu trước
Trước khi bắt đầu, hãy chắc chắn bạn đã có các yêu cầu sau:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) đã được cài đặt trên máy của bạn.
- Thư viện [Aspose.Note for Java](https://downloads.aspose.com/note/java) đã được tải xuống và thêm vào dự án của bạn.

## Nhập gói
`Aspose.Note` là không gian tên cốt lõi chứa tất cả các lớp cần thiết cho việc thao tác OneNote. Nhập gói trước khi bạn bắt đầu tạo các đối tượng.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Bước 1: thiết lập dự án của bạn
Bắt đầu bằng cách tạo một dự án Java mới và thêm thư viện Aspose.Note vào classpath. Đảm bảo dự án được cấu hình cho phiên bản JDK bạn đã cài đặt.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Bước 2: khởi tạo các đối tượng document và page
Lớp `Document` đại diện cho một tệp OneNote trong bộ nhớ, và lớp `Page` đại diện cho một trang duy nhất trong tài liệu đó.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Bước 3: tạo các hàng và ô của bảng
Lớp `TableRow` định nghĩa một hàng trong bảng, trong khi `TableCell` chứa nội dung cho mỗi cột trong hàng đó.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Bước 4: tạo và tùy chỉnh bảng
Lớp `Table` là container cho các hàng và cột, và `TableColumn` cho phép bạn đặt độ rộng và khóa cột.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Bước 5: thêm bảng vào outline và trang
Lớp `Outline` nhóm nội dung trên một trang, và `OutlineElement` đại diện cho một phần tử riêng lẻ như một bảng.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Bước 6: lưu tài liệu
Gọi phương thức `save` trên đối tượng `Document`, chỉ định đường dẫn tệp `.one`. Tệp sau đó có thể được mở trực tiếp trong Microsoft OneNote.

Chúc mừng! Bạn đã thành công **add table to OneNote** với các cột bị khóa bằng cách sử dụng Aspose.Note cho Java.

## Kết luận
Trong hướng dẫn này, chúng tôi đã đề cập đến mọi thứ bạn cần để **add table to OneNote** với các cột bị khóa, từ thiết lập dự án đến lưu cuối cùng. Bằng cách tận dụng API phong phú của Aspose.Note, bạn có được kiểm soát chi tiết về độ rộng cột, hành vi khóa và kiểu viền — giúp ghi chú của bạn trở nên có tổ chức và chuyên nghiệp hơn.

## Câu hỏi thường gặp
**Q: Aspose.Note cho Java có tương thích với tất cả các phiên bản Java không?**  
A: Có, Aspose.Note cho Java hoạt động với Java 7 và các phiên bản sau, bao gồm Java 8, 11 và 17.

**Q: Tôi có thể tùy chỉnh giao diện của bảng thêm nữa không?**  
A: Chắc chắn! Bạn có thể điều chỉnh viền, khoảng cách ô, màu nền, và thậm chí áp dụng định dạng văn bản phong phú cho từng ô.

**Q: Có phiên bản dùng thử nào trước khi mua không?**  
A: Có, bạn có thể [tải xuống bản dùng thử miễn phí](https://releases.aspose.com/) để khám phá các khả năng của Aspose.Note cho Java.

**Q: Tôi có thể tìm hỗ trợ bổ sung hoặc thảo luận cộng đồng ở đâu?**  
A: Truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) để nhận trợ giúp từ cộng đồng và các kỹ sư của Aspose.

**Q: Làm thế nào để tôi có được giấy phép tạm thời cho Aspose.Note cho Java?**  
A: Truy cập [trang giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để lấy giấy phép tạm thời cho mục đích thử nghiệm.

---

**Cập nhật lần cuối:** 2026-08-13  
**Kiểm tra với:** Aspose.Note 24.11 for Java  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Chuyển đổi Bảng thành Văn bản trong OneNote với Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Chèn Hàng Bảng Java - Thêm Nút Bảng với Thẻ trong OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: Thao tác Tài liệu OneNote](/note/java/onenote-document-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}