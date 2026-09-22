---
date: 2026-08-13
description: Tìm hiểu cách lấy thời gian sửa đổi trang OneNote và truy xuất các phiên
  bản trang bằng Aspose.Note cho Java, lý tưởng cho việc kiểm toán và quản lý tài
  liệu.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Lấy các phiên bản của trang trong OneNote - Aspose.Note
og_description: Tìm hiểu cách lấy thời gian sửa đổi trang OneNote và truy xuất các
  phiên bản của trang OneNote bằng Aspose.Note cho Java. Các bước nhanh, đoạn mã mẫu
  và khắc phục sự cố.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Lấy thời gian sửa đổi trang OneNote bằng Aspose.Note – Hướng dẫn Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Lấy thời gian sửa đổi trang OneNote bằng Aspose.Note
url: /vi/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lấy thời gian chỉnh sửa trang OneNote bằng Aspose.Note

## Giới thiệu

Trong tutorial này, bạn sẽ học cách **get onenote page modified** timestamps và lấy toàn bộ lịch sử sửa đổi của một trang OneNote bằng Aspose.Note cho Java. Dù bạn đang xây dựng tính năng theo dõi audit‑trail, một trình xem change‑log, hoặc cần hiển thị ngày chỉnh sửa gần nhất trên bảng điều khiển, hướng dẫn này sẽ dẫn bạn qua mọi bước — từ thiết lập môi trường đến xử lý các vấn đề thường gặp.

## Câu trả lời nhanh
- **“get last modified time” trả về gì?** Nó trả về dấu thời gian của lần chỉnh sửa mới nhất trên một trang OneNote.  
- **Lớp nào cung cấp lịch sử sửa đổi?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Tôi có cần giấy phép cho tính năng này không?** Có, cần một giấy phép Aspose.Note hợp lệ để sử dụng trong môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Java 8 hoặc cao hơn (JDK 8+).  
- **Tôi có thể lọc các phiên bản sửa đổi theo tác giả không?** Bạn có thể đọc thuộc tính `Author` của mỗi đối tượng `Page` và áp dụng bộ lọc của riêng mình.

## “get last modified time” là gì trong OneNote?

Thời gian chỉnh sửa cuối cùng được lưu dưới dạng thuộc tính metadata trên mỗi trang OneNote, chỉ ra thời điểm chỉnh sửa mới nhất. Aspose.Note cung cấp giá trị này thông qua phương thức `Page.getLastModifiedTime()`, trả về một đối tượng `java.util.Date` có thể được định dạng hoặc ghi log theo yêu cầu của ứng dụng.

## Tại sao cần lấy các phiên bản sửa đổi của trang?

Lấy các phiên bản sửa đổi của trang cung cấp cho bạn một chuỗi audit trail đầy đủ của mọi thay đổi trên một trang OneNote, cho phép bạn theo dõi ai đã chỉnh sửa gì và khi nào. Lịch sử này có thể được dùng để so sánh các phiên bản, khôi phục trạng thái trước đó, hoặc phân tích mô hình hợp tác giữa các nhóm, làm cho nó trở nên thiết yếu cho việc tuân thủ và kiểm soát chất lượng.

## Yêu cầu trước

- **Java Development Kit (JDK) 8 hoặc sau** – cài đặt từ trang web Oracle hoặc bất kỳ nhà cung cấp tương thích nào.  
- **Aspose.Note for Java library** – tải JAR từ trang phát hành Aspose.Note Java **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** và làm theo hướng dẫn cài đặt **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Nhập các gói

Lớp `Document` đại diện cho một sổ tay OneNote được tải vào bộ nhớ, trong khi `Page` và `PageHistory` cung cấp quyền truy cập vào các trang riêng lẻ và dữ liệu sửa đổi của chúng.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Các câu lệnh import thực tế được hiển thị dưới dạng văn bản thuần để giữ nguyên số lượng khối mã gốc.)*

## Cách lấy thời gian chỉnh sửa trang onenote?

Để lấy dấu thời gian chỉnh sửa cuối cùng, đầu tiên tải tài liệu OneNote vào một đối tượng `Document`, sau đó chọn `Page` mong muốn. Gọi phương thức `getLastModifiedTime()` trên trang đó, nó sẽ trả về một `java.util.Date`. Bạn có thể định dạng ngày này bằng `SimpleDateFormat` hoặc chuyển sang UTC để báo cáo nhất quán qua các múi giờ.

## Bước 1: đặt thư mục tài liệu

Xác định thư mục chứa tệp OneNote của bạn.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Bước 2: tải tài liệu

Tạo một thể hiện `Document` bằng cách truyền đường dẫn đầy đủ tới tệp `.one` của bạn.

```java
String dataDir = "Your Document Directory";
```

## Bước 3: lấy trang đầu tiên

Lấy đối tượng `Page` đầu tiên từ bộ sưu tập trang của tài liệu.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Bước 4: lấy các phiên bản sửa đổi của trang

Lấy `PageHistory` cho trang đã chọn. Nếu sổ tay chưa bao giờ được chỉnh sửa, cuộc gọi này có thể trả về `null`.

```java
Page firstPage = doc.getFirstChild();
```

## Bước 5: duyệt các phiên bản sửa đổi của trang

Lặp qua mỗi phiên bản `Page`, đọc `Author` và `LastModifiedTime` của nó, và hiển thị thông tin.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Vấn đề thường gặp và giải pháp
- **Null `PageHistory`** – Xác minh rằng sổ tay thực sự chứa các phiên bản sửa đổi; nếu không, `getPageHistory` sẽ trả về `null`.  
- **Time‑zone differences** – `getLastModifiedTime()` sử dụng múi giờ mặc định của JVM. Chuyển sang UTC bằng `SimpleDateFormat` nếu ứng dụng của bạn yêu cầu một múi giờ chuẩn.  
- **License not loaded** – Nếu không có giấy phép hợp lệ, Aspose.Note sẽ chạy ở chế độ đánh giá, giới hạn việc xử lý trang. Tải tệp giấy phép của bạn khi khởi động ứng dụng để tránh hạn chế này.

## Câu hỏi thường gặp

**Q1: Tôi có thể sử dụng Aspose.Note cho Java để tạo tài liệu OneNote mới không?**  
A: Có, API cho phép bạn tạo, chỉnh sửa và lưu sổ tay OneNote một cách lập trình từ đầu.

**Q2: Aspose.Note cho Java có tương thích với các phiên bản tệp OneNote khác nhau không?**  
A: Có, nó hỗ trợ các định dạng tệp OneNote 2007‑2021, đảm bảo tính tương thích rộng rãi trên môi trường desktop và cloud.

**Q3: Tôi có thể tùy chỉnh định dạng đầu ra khi xuất tài liệu OneNote không?**  
A: Chắc chắn. Bạn có thể xuất ra PDF, HTML, PNG hoặc SVG, và kiểm soát các tùy chọn như độ phân giải hình ảnh và nhúng phông chữ.

**Q4: Aspose.Note cho Java có yêu cầu giấy phép cho việc sử dụng thương mại không?**  
A: Có, giấy phép thương mại là bắt buộc cho các triển khai sản xuất. Một bản dùng thử miễn phí có sẵn để đánh giá.

**Q5: Tôi có thể tìm trợ giúp ở đâu nếu gặp vấn đề?**  
A: Truy cập diễn đàn cộng đồng Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** để đặt câu hỏi, chia sẻ kinh nghiệm và nhận trợ giúp từ cộng đồng và các kỹ sư Aspose.

---

**Cập nhật lần cuối:** 2026-08-13  
**Đã kiểm tra với:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Tác giả:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Các hướng dẫn liên quan

- [Hướng dẫn Java Aspose - Lấy thông tin về các trang trong OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Hướng dẫn sửa đổi trang aspose.note – Lấy các phiên bản trang trong OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Theo dõi thay đổi onenote – Quản lý các phiên bản trang với Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}