---
date: 2026-01-12
description: Tìm hiểu cách chỉnh sửa lịch sử trang OneNote, thay đổi tiêu đề trang
  OneNote và xóa lịch sử trang OneNote bằng Aspose.Note cho Java.
linktitle: Modify Page History in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Cách sửa đổi lịch sử trang OneNote bằng Aspose.Note
url: /vi/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách sửa đổi lịch sử trang OneNote bằng Aspose.Note

Trong hướng dẫn này, bạn sẽ khám phá **cách sửa đổi OneNote** tài liệu một cách lập trình bằng cách làm việc với lịch sử trang. Chúng tôi sẽ hướng dẫn cách tải tệp OneNote, chỉnh sửa các mục lịch sử, thay đổi tiêu đề trang và cuối cùng lưu sổ ghi chú đã cập nhật — tất cả đều sử dụng API Aspose.Note cho Java. Dù bạn cần dọn dẹp các phiên bản cũ hay đổi tên các trang, các bước dưới đây sẽ cung cấp cho bạn một giải pháp hoàn chỉnh, sẵn sàng cho môi trường sản xuất.

## Câu trả lời nhanh
- **“Lịch sử trang” có nghĩa là gì trong OneNote?**  
  Đó là tập hợp các phiên bản trang trước đó được lưu trong tệp OneNote.
- **Tôi có thể xóa một mục lịch sử cụ thể không?**  
  Có, sử dụng các phương thức `removeRange` hoặc `removeItem` trên đối tượng `PageHistory`.
- **Thay đổi tiêu đề trang có phải là một phần của việc thao tác lịch sử không?**  
  Chắc chắn—mỗi mục lịch sử có tiêu đề riêng mà bạn có thể chỉnh sửa.
- **Tôi có cần giấy phép để chạy đoạn mã này không?**  
  Giấy phép đánh giá tạm thời đủ cho việc thử nghiệm; giấy phép đầy đủ cần thiết cho môi trường sản xuất.
- **Phiên bản Java nào được hỗ trợ?**  
  Aspose.Note cho Java hỗ trợ JDK 8 trở lên.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

1. **Java Development Kit (JDK)** – JDK 8 hoặc mới hơn đã được cài đặt trên máy của bạn.  
2. **Thư viện Aspose.Note cho Java** – tải xuống từ [trang tải xuống](https://releases.aspose.com/note/java/).  
3. **Một tài liệu OneNote mẫu** – ví dụ, `Sample1.one` mà bạn có thể sửa đổi một cách an toàn.

## Nhập các gói

Đầu tiên, nhập các lớp bạn sẽ cần. Khối mã dưới đây phải giữ nguyên như đã hiển thị.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Hướng dẫn từng bước

### Bước 1: Tải tài liệu OneNote

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### Bước 2: Lấy trang đầu tiên và lịch sử của nó

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### Bước 3: Xóa một phạm vi các mục lịch sử

Nếu bạn cần **xóa các mục lịch sử trang OneNote**, gọi `removeRange`. Ví dụ này sẽ xóa mục đầu tiên.

```java
pageHistory.removeRange(0, 1);
```

### Bước 4: Thay thế một mục lịch sử

Bạn có thể thay thế một mục lịch sử hiện có bằng một đối tượng `Page` mới.

```java
pageHistory.set_Item(0, new Page());
```

### Bước 5: Thay đổi tiêu đề của một trang lịch sử

Thay đổi tiêu đề là một yêu cầu phổ biến khi bạn muốn **đổi tiêu đề trang OneNote** cho một phiên bản cụ thể.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### Bước 6: Thêm một mục lịch sử mới

Thêm một trang mới hoàn toàn vào bộ sưu tập lịch sử.

```java
pageHistory.addItem(new Page());
```

### Bước 7: Chèn một trang vào vị trí cụ thể

Chèn một trang vào chỉ mục 1, đẩy các mục hiện có lên phía sau.

```java
pageHistory.insertItem(1, new Page());
```

### Bước 8: Lưu sổ ghi chú đã sửa đổi

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## Tại sao cần sửa đổi lịch sử trang OneNote?

- **Kiểm soát phiên bản:** Giữ lại chỉ các phiên bản liên quan và loại bỏ các bản nháp không cần thiết.  
- **Tính nhất quán:** Đồng bộ tiêu đề trang trên tất cả các phiên bản lịch sử để dễ dàng điều hướng hơn.  
- **Hiệu suất:** Bộ sưu tập lịch sử nhỏ hơn giảm kích thước tệp và cải thiện tốc độ tải.

## Những lỗi thường gặp & Mẹo

- **Chỉ mục vượt quá phạm vi:** Luôn kiểm tra kích thước của bộ sưu tập trước khi gọi `removeRange` hoặc `insertItem`.  
- **Tiêu đề null:** Một số trang lịch sử có thể không có tiêu đề; cần kiểm tra `null` khi gọi `getTitle()`.  
- **Vị trí lưu:** Đảm bảo đường dẫn đầu ra (`ModifyPageHistory_out.one`) có quyền ghi; nếu không, sẽ ném ra `IOException`.

## Câu hỏi thường gặp

**H: Tôi có thể sử dụng Aspose.Note cho Java với các framework Java khác không?**  
Đ: Có, Aspose.Note cho Java tương thích với nhiều framework Java như Spring, Hibernate, v.v.

**H: Aspose.Note cho Java có tương thích với các phiên bản tệp OneNote khác nhau không?**  
Đ: Aspose.Note cho Java hỗ trợ làm việc với cả phiên bản cũ và mới của tệp OneNote.

**H: Aspose.Note cho Java có yêu cầu bất kỳ phụ thuộc bổ sung nào không?**  
Đ: Không, Aspose.Note cho Java là một thư viện độc lập và không cần bất kỳ phụ thuộc nào khác.

**H: Tôi có thể thực hiện sửa đổi hàng loạt trên nhiều tệp OneNote cùng lúc không?**  
Đ: Có, Aspose.Note cho Java cung cấp các API để xử lý sửa đổi hàng loạt một cách hiệu quả.

**H: Có diễn đàn cộng đồng nào cho Aspose.Note cho Java để tôi có thể hỏi trợ giúp không?**  
Đ: Có, bạn có thể truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) để nhận hỗ trợ hoặc đặt câu hỏi liên quan đến thư viện.

---

**Cập nhật lần cuối:** 2026-01-12  
**Đã kiểm tra với:** Aspose.Note cho Java 24.11 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}