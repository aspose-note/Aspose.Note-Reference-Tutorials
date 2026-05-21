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

## Giới thiệu

Nếu bạn đang tìm kiếm một cách rõ ràng, có thể cài đặt trình **cách khôi phục onenote** các trang khi gặp lỗi, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn sử dụng Aspose.Note for Java để khôi phục trang OneNote về trạng thái trước đó. Dù bạn đang xây dựng công cụ quản lý ghi chú tự động hay cần có một mạng lưới toàn bộ cho ghi chú cộng tác, công việc hoàn thành một trang trợ giúp nội dung của bạn chính xác và đáng tin cậy.

## Trả lời nhanh
- **“Roll back” có nghĩa là gì đối với OneNote?** Khôi phục một trang về bản trước đã được lưu trong phiên lịch sử.
- **API nào xử lý công việc rollback?** Lớp `PageHistory` trong Aspose.Note for Java.
- **Tôi có cần giấy phép không?** Cần có giấy phép Aspose.Note hợp lệ để sử dụng trong môi trường sản xuất.
- **Tôi có thể chọn bất kỳ phiên bản nào trước đó?** Có – bạn có thể chọn bất kỳ mục nào trong danh sách lịch sử của trang.
- **Phương pháp này có toàn bộ ghi chú lớn không?** Hoàn toàn; thao tác chỉ hoạt động trên các trang riêng lẻ mà không cần tải toàn bộ ghi chú sổ vào bộ nhớ.

##Cách hoàn thành phiên bản trang OneNote
Dưới đây là hướng dẫn rút gọn, từng bước được chỉ ra cách thực hiện công việc rollback. Mỗi bước bao gồm giải thích rút gọn để bạn hiểu *tại sao* chúng ta làm như vậy, không chỉ * cần nhập gì*.

## Điều kiện tiên quyết

Trước khi chúng bắt đầu bằng mã hóa, hãy chắc chắn rằng bạn đã chuẩn bị các mục sau:

### Thiết lập môi trường phát triển Java
1. **Cài đặt Bộ công cụ phát triển Java (JDK):** Tải JDK mới nhất từ ​​trang web Oracle hoặc trình quản lý gói yêu thích của bạn.
2. **Cấu hình môi trường biến:** Đặt `Java_HOME` và cập nhật `PATH` để các lệnh `java` và `javac` có thể truy cập từ lệnh dòng.
3. **Thêm Aspose.Note cho Java:** Tải thư viện từ [website](https://purchase.aspose.com/buy) và thêm tệp JAR vào classpath của dự án.

## Nhập gói

Để tương tác với các tệp OneNote, nhập các lớp Aspose.Note cần thiết:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Bước 1: Mở tài liệu OneNote
```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
Đầu tiên, chúng ta chỉ đến thư mục chứa tệp `.one` và tải nó vào một đối tượng `Document`.

## Bước 2: Xem lịch sử trang
```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
`PageHistory` cung cấp quyền truy cập vào mọi phiên bản đã lưu của trang được chọn, cho phép khả năng **khôi phục phiên bản onenote trước**.

## Bước 3: Xóa trang hiện tại
```java
document.removeChild(page);
```
Bằng cách xóa trang hiện tại, chúng ta tạo không gian cho phiên bản muốn khôi phục.

## Bước 4: Thêm phiên bản trang trước
```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
Ở đây chúng ta chọn mục lịch sử mới nhất (bạn có thể thay đổi chỉ số để chọn bất kỳ phiên bản cũ hơn nào) và thêm nó trở lại tài liệu.

## Bước 5: Lưu tài liệu
```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
Cuối cùng, lưu lại sổ ghi chú đã chỉnh sửa. Tệp đầu ra bây giờ chứa trang đã được hoàn tác.

## Khôi phục phiên bản OneNote trước đó
Sự kết hợp của `PageHistory` và `appendChildLast` cho phép bạn **khôi phục phiên bản onenote trước** chỉ với một vài dòng mã. Điều này đặc biệt hữu ích trong các quy trình tự động nơi công việc hoàn thành công việc không khả thi.

## Các vấn đề thường gặp & Mẹo
- **Lịch sử trống:** Nếu `pageHistory.size()` trả về 0, trang chưa lưu phiên bản nào — hãy đảm bảo tính năng phiên bản được bật trong OneNote.
- **Chỉ số ngoài phạm vi:** Hãy nhớ rằng danh sách lịch sử bắt đầu từ 0. Điều chỉnh chỉ số (`size() - 1`) để chọn đúng phiên bản bạn cần.
- **Tính năng nổi bật:** hoạt động với một trang riêng lẻ tránh tải toàn bộ ghi chú vào bộ nhớ, giúp thao tác nhanh chóng hơn với các tệp lớn hơn.

## Phần kết luận

Bây giờ bạn đã có một phương pháp hoàn chỉnh, sẵn sàng cho môi trường sản xuất để **cách khôi phục onenote** các trang bằng Aspose.Note cho Java. Bằng cách sử dụng `PageHistory`, bạn có thể khôi phục toàn bộ bất kỳ trạng thái nào trước đó của một ghi chú trang, đảm bảo tính toàn vẹn dữ liệu và mang lại ý tưởng cho người dùng cuối cùng trong môi trường cộng tác.

## Câu hỏi thường gặp

**Q1: ​​Tôi có thể hoàn thành nhiều phiên bản của một trang không?**
A: Có, bạn có thể truy cập toàn bộ lịch sử trang và hoàn thành bất kỳ phiên bản nào trước đó nếu cần.

**Q2: Aspose.Note có hỗ trợ các trình cài đặt ngôn ngữ khác ngoài Java không?**
A: There, Aspose.Note cung cấp các thư viện cho nhiều trình cài đặt ngôn ngữ, bao gồm .NET, C++ và Python.

**Q3: Aspose.Note có tương thích với mọi phiên bản của OneNote không?**
A: Aspose.Note hỗ trợ nhiều OneNote định dạng, đảm bảo tương thích với việc sắp hết các tài liệu phiên bản.

**Q4: Tôi có thể tự động hóa các tác vụ khác trong OneNote bằng Aspose.Note không?**
A: Chắc chắn, Aspose.Note cung cấp khả năng rộng rãi để lập trình bổ sung, xóa và sửa đổi nội dung.

**Q5: Có diễn đàn cộng đồng hoặc hỗ trợ cho Aspose.Note không?**
A: Có, bạn có thể truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) để nhận hỗ trợ cộng đồng hoặc liên hệ bộ phận hỗ trợ khách hàng của Aspose để được hỗ trợ.

---

**Cập nhật lần cuối:** 2026-01-12
**Đã kiểm tra:** Aspose.Note for Java (bản phát hành mới nhất)
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}