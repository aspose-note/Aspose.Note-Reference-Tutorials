---
title: Thay đổi kiểu bảng trong OneNote - Aspose.Note
linktitle: Thay đổi kiểu bảng trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Dễ dàng nâng cao các bảng OneNote của bạn với Aspose.Note for Java. Làm theo hướng dẫn từng bước của chúng tôi để thay đổi kiểu bảng. Tải thư viện ngay bây giờ!
type: docs
weight: 10
url: /vi/java/onenote-table-manipulation/change-table-style/
---
## Giới thiệu
Aspose.Note for Java là một thư viện mạnh mẽ cho phép các nhà phát triển thao tác với các tệp OneNote một cách dễ dàng. Trong hướng dẫn này, chúng tôi sẽ tập trung vào việc thay đổi kiểu bảng trong tài liệu OneNote bằng Aspose.Note cho Java. Thực hiện theo hướng dẫn từng bước để nâng cao sức hấp dẫn trực quan cho bảng của bạn.
## Điều kiện tiên quyết
Trước khi bắt đầu, hãy đảm bảo bạn có những điều sau:
- Môi trường phát triển Java: Đảm bảo rằng bạn đã thiết lập môi trường phát triển Java trên máy của mình.
-  Aspose.Note for Java Library: Tải xuống và cài đặt thư viện Aspose.Note for Java từ[trang tải xuống](https://releases.aspose.com/note/java/).
- Thư mục tài liệu: Chuẩn bị một thư mục để lưu trữ tài liệu OneNote của bạn.
## Gói nhập khẩu
Trong dự án Java của bạn, hãy nhập các gói cần thiết để hoạt động với Aspose.Lưu ý:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## Bước 1: Thiết lập tài liệu
Tải tài liệu OneNote vào Aspose.Note và truy xuất danh sách các nút bảng
```java
// Thiết lập tài liệu và lấy danh sách các nút bảng
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## Bước 2: Đặt kiểu hàng
Lặp lại qua từng bảng, đặt kiểu cho từng hàng, bao gồm cả việc đánh dấu hàng đầu tiên sau tiêu đề.

```java
// Đặt kiểu hàng cho mỗi bảng trong tài liệu
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Đánh dấu hàng đầu tiên sau phần đầu.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## Phương thức setRowStyle
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```
## Bước 3: Lưu tài liệu
Lưu tài liệu đã sửa đổi với các kiểu bảng mới.
Bằng cách làm theo các bước này, bạn có thể dễ dàng thay đổi kiểu bảng trong tài liệu OneNote bằng Aspose.Note for Java.

```java
// Lưu tài liệu đã sửa đổi
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## Phần kết luận
Aspose.Note for Java đơn giản hóa quá trình thao tác với tệp OneNote. Bằng cách tận dụng các khả năng của thư viện, bạn có thể dễ dàng nâng cao cách trình bày trực quan các bảng của mình.

## Câu hỏi thường gặp
### Tôi có thể tìm tài liệu về Aspose.Note for Java ở đâu?
 Tham quan[tài liệu](https://reference.aspose.com/note/java/) để được hướng dẫn toàn diện.
### Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.Note cho Java?
 Theo dõi cái này[liên kết](https://purchase.aspose.com/temporary-license/) để có được giấy phép tạm thời.
### Có bản dùng thử miễn phí cho Aspose.Note cho Java không?
 Có, bạn có thể tải xuống phiên bản dùng thử miễn phí từ[đây](https://releases.aspose.com/).
### Tôi có thể nhận hỗ trợ cho Aspose.Note cho Java ở đâu?
 Tham gia[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) để tìm kiếm sự giúp đỡ từ cộng đồng.
### Làm cách nào để mua Aspose.Note cho Java?
 Bạn có thể mua thư viện[đây](https://purchase.aspose.com/buy).