---
date: 2026-01-10
description: Học hướng dẫn sửa đổi trang Aspose.Note cho Java – truy xuất các phiên
  bản sửa đổi trang OneNote một cách lập trình bằng Aspose.Note. Thực hiện theo hướng
  dẫn từng bước của chúng tôi.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Hướng dẫn sửa đổi trang aspose.note – Lấy sửa đổi trang trong OneNote
url: /vi/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lấy các Phiên bản Trang trong OneNote - Aspose.Note

OneNote là một nền tảng ghi chú mạnh mẽ, và khi bạn cần kiểm tra các thay đổi, **aspose.note page revisions tutorial** cho bạn thấy chính xác cách lấy lịch sử phiên bản chỉ với vài dòng mã Java. Trong hướng dẫn này, chúng tôi sẽ đi qua mọi thứ bạn cần—từ thiết lập môi trường đến in ra chi tiết của mỗi phiên bản—để bạn có thể theo dõi các chỉnh sửa, đóng góp của tác giả và dấu thời gian một cách dễ dàng.

## Câu trả lời nhanh
- **Mục tiêu của hướng dẫn là gì?** Truy xuất lịch sử phiên bản trang từ tệp OneNote bằng Aspose.Note cho Java.  
- **Phiên bản thư viện nào được yêu cầu?** Bất kỳ bản phát hành Aspose.Note cho Java gần đây nào hỗ trợ `LoadOptions.setLoadHistory`.  
- **Tôi có cần giấy phép không?** Giấy phép đánh giá tạm thời hoạt động cho việc thử nghiệm; giấy phép thương mại là bắt buộc cho môi trường sản xuất.  
- **Tôi có thể sửa đổi các phiên bản không?** API chỉ cho phép đọc các phiên bản; bạn chỉ có thể truy xuất chúng.  
- **Các yêu cầu trước tiên là gì?** Java JDK, Aspose.Note cho Java, và một tài liệu OneNote có dữ liệu phiên bản.

## “aspose.note page revisions tutorial” là gì?
Hướng dẫn minh họa cách truy cập các phiên bản lịch sử của một trang OneNote một cách lập trình. Mỗi phiên bản chứa siêu dữ liệu như tác giả, thời gian tạo và thời gian sửa đổi, cho phép bạn xây dựng các chuỗi kiểm tra hoặc tính năng nhật ký thay đổi trong ứng dụng của mình.

## Tại sao nên dùng Aspose.Note để theo dõi phiên bản trang?
- **Không phụ thuộc vào giao diện người dùng** – hoạt động hoàn toàn bằng mã, phù hợp cho các dịch vụ backend.  
- **Đa nền tảng** – Java chạy trên Windows, Linux và macOS.  
- **Kiểm soát đầy đủ** – truy xuất mọi thuộc tính của phiên bản mà không cần mở OneNote thủ công.  
- **Hiệu năng** – việc tải lịch sử được tối ưu, vì vậy ngay cả sổ ghi chú lớn cũng được xử lý nhanh chóng.

## Yêu cầu trước

### 1. Java Development Kit (JDK)
Đảm bảo đã cài đặt JDK mới (phiên bản 8 trở lên) và đã thiết lập `JAVA_HOME`.

### 2. Aspose.Note cho Java
Tải thư viện từ [download link](https://releases.aspose.com/note/java/).

### 3. Tài liệu OneNote mẫu
Tạo hoặc lấy một tệp OneNote (ví dụ, `Sample1.one`) có chứa các trang với lịch sử phiên bản.

## Nhập các gói
Đầu tiên, nhập các lớp Aspose.Note cần thiết.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Triển khai từng bước

### Bước 1: Thiết lập thư mục tài liệu
Xác định thư mục chứa tệp OneNote của bạn.

```java
String dataDir = "Your Document Directory";
```

### Bước 2: Tải tài liệu OneNote với lịch sử được bật
Bật cờ `LoadOptions` để lấy dữ liệu phiên bản.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Bước 3: Lấy trang đầu tiên
Lấy đối tượng trang đầu tiên; đây sẽ là điểm tham chiếu để truy xuất lịch sử của nó.

```java
Page firstPage = document.getFirstChild();
```

### Bước 4: Duyệt qua các phiên bản trang
Lặp qua mỗi phiên bản và in ra siêu dữ liệu hữu ích như dấu thời gian, tiêu đề, cấp độ và tác giả.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **Mẹo chuyên nghiệp:** Nếu bạn cần lọc các phiên bản theo một tác giả cụ thể hoặc khoảng thời gian, chỉ cần thêm các kiểm tra điều kiện bên trong vòng lặp `for`.

## Các vấn đề thường gặp & Giải pháp
- **Không có phiên bản nào được trả về:** Kiểm tra xem `loadOptions.setLoadHistory(true)` đã được gọi trước khi tải tài liệu chưa.  
- **Tác giả hoặc tiêu đề null:** Một số phiên bản OneNote cũ có thể không lưu các trường này; hãy xử lý giá trị `null` một cách mềm mại.  
- **Độ trễ hiệu năng trên sổ ghi chú lớn:** Chỉ tải các phần bạn cần hoặc tăng kích thước heap của JVM.

## Câu hỏi thường gặp

**Q1: Tôi có thể dùng Aspose.Note cho Java để sửa đổi các phiên bản trang không?**  
A1: Không, API hiện chỉ hỗ trợ truy cập chỉ‑đọc tới các phiên bản trang.

**Q2: Aspose.Note cho Java có tương thích với các phiên bản tài liệu OneNote khác nhau không?**  
A2: Có, nó hoạt động với nhiều định dạng tệp OneNote, cho phép xử lý liền mạch qua các phiên bản.

**Q3: Aspose.Note cho Java có yêu cầu giấy phép để sử dụng không?**  
A3: Giấy phép thương mại là bắt buộc cho môi trường sản xuất, nhưng giấy phép đánh giá tạm thời có sẵn cho việc thử nghiệm.

**Q4: Tôi có thể nhận hỗ trợ nếu gặp vấn đề khi sử dụng Aspose.Note cho Java không?**  
A4: Có, bạn có thể đặt câu hỏi trên diễn đàn Aspose.Note [tại đây](https://forum.aspose.com/c/note/28).

**Q5: Có bản dùng thử miễn phí cho Aspose.Note cho Java không?**  
A5: Có, bạn có thể tải bản dùng thử miễn phí từ [website](https://releases.aspose.com/).

---

**Cập nhật lần cuối:** 2026-01-10  
**Kiểm tra với:** Aspose.Note for Java (phiên bản mới nhất)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}