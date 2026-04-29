---
date: 2026-01-12
description: Tìm hiểu cách khôi phục lại các trang OneNote và khôi phục phiên bản
  OneNote trước đó bằng Aspose.Note cho Java. Hãy làm theo hướng dẫn từng bước này
  để quản lý tài liệu hiệu quả.
linktitle: How to Roll Back OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Cách quay lại OneNote - Aspose.Note
url: /vi/java/onenote-page-manipulation/roll-back-to-previous-page-version/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách hoàn tác OneNote - Aspose.Note

## Introduction

Nếu bạn đang tìm kiếm một cách rõ ràng, có thể lập trình để **how to roll back onenote** các trang khi có lỗi, bạn đã đến đúng nơi. Trong hướng dẫn này chúng tôi sẽ hướng dẫn sử dụng Aspose.Note for Java để khôi phục một trang OneNote về trạng thái trước đó. Dù bạn đang xây dựng công cụ quản lý ghi chú tự động hay cần một lưới an toàn cho sổ ghi chú cộng tác, việc hoàn tác một trang giúp nội dung của bạn chính xác và đáng tin cậy.

## Quick Answers
- **“Roll back” có nghĩa là gì đối với OneNote?** Khôi phục một trang về phiên bản trước đã được lưu trong lịch sử.  
- **API nào xử lý việc rollback?** Lớp `PageHistory` trong Aspose.Note for Java.  
- **Tôi có cần giấy phép không?** Cần có giấy phép Aspose.Note hợp lệ để sử dụng trong môi trường sản xuất.  
- **Tôi có thể chọn bất kỳ phiên bản trước nào không?** Có – bạn có thể chọn bất kỳ mục nào trong danh sách lịch sử của trang.  
- **Phương pháp này có an toàn cho sổ ghi chú lớn không?** Hoàn toàn; thao tác chỉ làm việc trên các trang riêng lẻ mà không cần tải toàn bộ sổ ghi chú vào bộ nhớ.

## Cách hoàn tác phiên bản trang OneNote
Dưới đây là hướng dẫn ngắn gọn, từng bước cho thấy cách thực hiện việc rollback. Mỗi bước bao gồm giải thích ngắn gọn để bạn hiểu *tại sao* chúng ta làm như vậy, không chỉ *cần gõ gì*.

## Prerequisites

Trước khi chúng ta bắt đầu với mã, hãy chắc chắn rằng bạn đã chuẩn bị các mục sau:

### Java Development Environment Setup
1. **Cài đặt Java Development Kit (JDK):** Tải JDK mới nhất từ trang web Oracle hoặc trình quản lý gói ưa thích của bạn.  
2. **Cấu hình biến môi trường:** Đặt `JAVA_HOME` và cập nhật `PATH` để các lệnh `java` và `javac` có thể truy cập từ dòng lệnh.  
3. **Thêm Aspose.Note cho Java:** Tải thư viện từ [website](https://purchase.aspose.com/buy) và thêm file JAR vào classpath của dự án.

## Import Packages

Để tương tác với các tệp OneNote, nhập các lớp Aspose.Note cần thiết:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Step 1: Load OneNote Document
```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
Đầu tiên, chúng ta chỉ đến thư mục chứa tệp `.one` và tải nó vào một đối tượng `Document`.

## Step 2: Get Page History
```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
`PageHistory` cung cấp quyền truy cập vào mọi phiên bản đã lưu của trang được chọn, cho phép khả năng **khôi phục phiên bản onenote trước**.

## Step 3: Remove Current Page
```java
document.removeChild(page);
```
Bằng cách xóa trang hiện tại, chúng ta tạo không gian cho phiên bản muốn khôi phục.

## Step 4: Append Previous Page Version
```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
Ở đây chúng ta chọn mục lịch sử mới nhất (bạn có thể thay đổi chỉ số để chọn bất kỳ phiên bản cũ hơn nào) và thêm nó trở lại tài liệu.

## Step 5: Save Document
```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
Cuối cùng, lưu lại sổ ghi chú đã chỉnh sửa. Tệp đầu ra bây giờ chứa trang đã được hoàn tác.

## Restore Previous OneNote Version
Sự kết hợp của `PageHistory` và `appendChildLast` cho phép bạn **khôi phục phiên bản onenote trước** chỉ với vài dòng mã. Điều này đặc biệt hữu ích trong các quy trình tự động nơi việc hoàn tác thủ công không khả thi.

## Common Issues & Tips
- **Lịch sử trống:** Nếu `pageHistory.size()` trả về 0, trang không có phiên bản đã lưu — hãy đảm bảo tính năng phiên bản được bật trong OneNote.  
- **Chỉ số ngoài phạm vi:** Nhớ rằng danh sách lịch sử bắt đầu từ 0. Điều chỉnh chỉ số (`size() - 1`) để chọn đúng phiên bản bạn cần.  
- **Hiệu năng:** Làm việc với một trang riêng lẻ tránh việc tải toàn bộ sổ ghi chú vào bộ nhớ, giúp thao tác nhanh ngay cả với các tệp lớn.

## Conclusion

Bây giờ bạn đã có một phương pháp hoàn chỉnh, sẵn sàng cho môi trường sản xuất để **how to roll back onenote** các trang bằng Aspose.Note cho Java. Bằng cách sử dụng `PageHistory`, bạn có thể an toàn khôi phục bất kỳ trạng thái trước nào của một trang sổ ghi chú, đảm bảo tính toàn vẹn dữ liệu và mang lại sự tin tưởng cho người dùng cuối trong môi trường cộng tác.

## Frequently Asked Questions

**Q1: Tôi có thể hoàn tác nhiều phiên bản của một trang không?**  
A: Có, bạn có thể truy cập toàn bộ lịch sử trang và hoàn tác về bất kỳ phiên bản trước nào khi cần.

**Q2: Aspose.Note có hỗ trợ các ngôn ngữ lập trình khác ngoài Java không?**  
A: Có, Aspose.Note cung cấp các thư viện cho nhiều ngôn ngữ lập trình, bao gồm .NET, C++ và Python.

**Q3: Aspose.Note có tương thích với mọi phiên bản của OneNote không?**  
A: Aspose.Note hỗ trợ nhiều định dạng OneNote, đảm bảo tương thích với hầu hết các phiên bản tài liệu.

**Q4: Tôi có thể tự động hóa các tác vụ khác trong OneNote bằng Aspose.Note không?**  
A: Chắc chắn, Aspose.Note cung cấp khả năng rộng rãi để lập trình thêm, xóa và sửa đổi nội dung.

**Q5: Có diễn đàn cộng đồng hoặc hỗ trợ cho Aspose.Note không?**  
A: Có, bạn có thể truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) để nhận hỗ trợ cộng đồng hoặc liên hệ bộ phận hỗ trợ khách hàng của Aspose để được trợ giúp.

---

**Cập nhật lần cuối:** 2026-01-12  
**Đã kiểm tra với:** Aspose.Note for Java (latest release)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}