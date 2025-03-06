---
title: Tạo bảng có cột bị khóa trong OneNote - Aspose.Note
linktitle: Tạo bảng có cột bị khóa trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Nâng cao trải nghiệm OneNote của bạn với Aspose.Note for Java. Tìm hiểu cách tạo bảng có cột bị khóa bằng hướng dẫn từng bước. Tải về dùng thử ngay!
weight: 12
url: /vi/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo bảng có cột bị khóa trong OneNote - Aspose.Note

## Giới thiệu
OneNote là một công cụ mạnh mẽ để sắp xếp thông tin và Aspose.Note dành cho Java nâng cao khả năng của nó bằng cách cung cấp một cách liền mạch để tạo các bảng có các cột bị khóa. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình sử dụng Aspose.Note cho Java để tạo bảng có các cột bị khóa trong OneNote.
## Điều kiện tiên quyết
Trước khi bắt đầu, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:
- [Bộ công cụ phát triển Java (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)được cài đặt trên máy của bạn.
- [Aspose.Note cho Java](https://downloads.aspose.com/note/java) thư viện được tải xuống và thêm vào dự án của bạn.
## Gói nhập khẩu
Trong dự án Java của bạn, hãy nhập các gói cần thiết để làm việc với Aspose.Lưu ý:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Bước 1: Thiết lập dự án của bạn
Bắt đầu bằng cách tạo một dự án Java mới và thêm thư viện Aspose.Note vào đường dẫn lớp của bạn. Đảm bảo rằng dự án của bạn được cấu hình để sử dụng JDK.
## Bước 2: Khởi tạo đối tượng tài liệu và trang
```java
// Đường dẫn đến thư mục tài liệu.
String dataDir = "Your Document Directory";
//Tạo một đối tượng của lớp Tài liệu
Document doc = new Document();
// Khởi tạo đối tượng lớp Trang
Page page = new Page();
```
## Bước 3: Tạo hàng và ô trong bảng
```java
// Khởi tạo đối tượng lớp TableRow
TableRow row1 = new TableRow();
// Khởi tạo đối tượng lớp TableCell và thiết lập nội dung văn bản
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Khởi tạo đối tượng lớp TableRow
TableRow row2 = new TableRow();
// Khởi tạo đối tượng lớp TableCell và thiết lập nội dung văn bản
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Bước 4: Tạo và tùy chỉnh bảng
```java
// Khởi tạo đối tượng lớp Bảng
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Thêm hàng
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Bước 5: Thêm bảng vào dàn ý và trang
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Thêm nút bảng
outlineElem.appendChildLast(table);
// Thêm nút phần tử phác thảo
outline.appendChildLast(outlineElem);
// Thêm nút phác thảo
page.appendChildLast(outline);
// Thêm nút trang
doc.appendChildLast(page);
```
## Bước 6: Lưu tài liệu
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Chúc mừng! Bạn đã tạo thành công bảng có các cột bị khóa trong OneNote bằng Aspose.Note for Java.
## Phần kết luận
Trong hướng dẫn này, chúng tôi đã khám phá quy trình sử dụng Aspose.Note cho Java để nâng cao trải nghiệm OneNote của bạn bằng cách tạo các bảng có các cột bị khóa. Chức năng này thêm một lớp tổ chức và cấu trúc mới vào ghi chú của bạn.
## Câu hỏi thường gặp
### Aspose.Note for Java có tương thích với tất cả các phiên bản Java không?
Có, Aspose.Note for Java tương thích với Java 6 và các phiên bản mới hơn.
### Tôi có thể tùy chỉnh thêm hình thức của bảng không?
Tuyệt đối! Aspose.Note for Java cung cấp các tùy chọn mở rộng để tùy chỉnh bảng, chẳng hạn như điều chỉnh đường viền, khoảng cách ô, v.v.
### Có bản dùng thử trước khi mua không?
 Vâng, bạn có thể[tải về dùng thử miễn phí](https://releases.aspose.com/) để khám phá các khả năng của Aspose.Note dành cho Java.
### Tôi có thể tìm thêm hỗ trợ hoặc thảo luận cộng đồng ở đâu?
 Tham quan[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) để được hỗ trợ và thảo luận cộng đồng.
### Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.Note cho Java?
 Thăm nom[liên kết này](https://purchase.aspose.com/temporary-license/) để có được giấy phép tạm thời cho mục đích thử nghiệm.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
