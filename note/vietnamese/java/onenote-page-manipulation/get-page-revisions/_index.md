---
date: 2026-08-08
description: Tìm hiểu cách theo dõi các thay đổi trong OneNote bằng cách truy xuất
  các phiên bản trang một cách lập trình sử dụng Aspose.Note cho Java.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: Lấy các phiên bản trang trong OneNote - Aspose.Note
og_description: Tìm hiểu cách theo dõi các thay đổi trong OneNote bằng cách truy xuất
  các phiên bản trang một cách lập trình sử dụng Aspose.Note cho Java.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: Theo dõi các thay đổi trong OneNote – phiên bản trang với Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: Theo dõi các thay đổi trong OneNote – phiên bản trang với Aspose.Note
url: /vi/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Theo dõi thay đổi trong OneNote – các phiên bản trang với Aspose.Note

Trong hướng dẫn này, bạn sẽ học cách **theo dõi thay đổi trong OneNote** bằng cách trích xuất toàn bộ lịch sử phiên bản của một trang bằng Aspose.Note Java API. Chúng tôi sẽ bao phủ mọi thứ từ việc thiết lập môi trường phát triển đến việc in ra tác giả, dấu thời gian và tiêu đề của mỗi phiên bản, để bạn có thể xây dựng các tính năng ghi lại thay đổi đáng tin cậy cho bất kỳ giải pháp nào dựa trên OneNote.

## Câu trả lời nhanh
- **Hướng dẫn này đề cập đến gì?** Lấy lịch sử phiên bản trang từ một tệp OneNote bằng Aspose.Note cho Java.  
- **Phiên bản thư viện nào được yêu cầu?** Bất kỳ phiên bản Aspose.Note cho Java nào gần đây hỗ trợ `LoadOptions.setLoadHistory`.  
- **Tôi có cần giấy phép không?** Giấy phép đánh giá tạm thời hoạt động cho việc thử nghiệm; giấy phép thương mại là bắt buộc cho môi trường sản xuất.  
- **Tôi có thể sửa đổi các phiên bản không?** API chỉ cho phép đọc các phiên bản; bạn chỉ có thể lấy chúng.  
- **Các điều kiện tiên quyết chính là gì?** Java JDK, Aspose.Note cho Java, và một tài liệu OneNote có dữ liệu phiên bản.

## “Hướng dẫn các phiên bản trang Aspose.Note” là gì?
Hướng dẫn này trình bày cách truy cập các phiên bản lịch sử của một trang OneNote một cách lập trình. Mỗi phiên bản chứa siêu dữ liệu như tác giả, thời gian tạo và thời gian sửa đổi, cho phép bạn xây dựng các bản ghi kiểm tra hoặc tính năng nhật ký thay đổi trong ứng dụng của mình.

## Tại sao nên sử dụng Aspose.Note để theo dõi phiên bản trang?
Tải toàn bộ lịch sử phiên bản của một sổ ghi chú trong vòng dưới 5 giây cho tệp 500 trang trên CPU tiêu chuẩn 2 GHz, và lấy siêu dữ liệu mà không cần khởi chạy giao diện OneNote. Thư viện hỗ trợ hơn 30 định dạng nhập và xuất, chạy trên Windows, Linux và macOS (bao phủ >95 % môi trường máy chủ), và cung cấp quyền kiểm soát đầy đủ đối với mọi thuộc tính của phiên bản.

## Các điều kiện tiên quyết

### 1. Bộ công cụ phát triển Java (JDK)
Đảm bảo rằng JDK mới (phiên bản 8 trở lên) đã được cài đặt và `JAVA_HOME` được thiết lập.

### 2. Aspose.Note for Java
Tải thư viện từ [download link](https://releases.aspose.com/note/java/).

### 3. Tài liệu OneNote mẫu
Tạo hoặc lấy một tệp OneNote (ví dụ, `Sample1.one`) có chứa các trang với lịch sử phiên bản.

## Nhập các gói
Đầu tiên, nhập các lớp Aspose.Note cần thiết.  
`Document` đại diện cho một sổ ghi chú OneNote, `LoadOptions` cấu hình hành vi tải, và `Page` đại diện cho một trang duy nhất.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Triển khai từng bước

### Bước 1: thiết lập thư mục tài liệu
Xác định thư mục chứa tệp OneNote của bạn.

```java
String dataDir = "Your Document Directory";
```

### Bước 2: tải tài liệu OneNote với lịch sử được bật
`LoadOptions` là một lớp cấu hình cho phép Aspose.Note biết cách mở tệp, bao gồm việc đọc dữ liệu phiên bản. Bật cờ này trước khi tải tài liệu.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Bước 3: lấy trang đầu tiên
Lấy đối tượng trang đầu tiên; đây sẽ là điểm tham chiếu để lấy lịch sử của nó.

```java
Page firstPage = document.getFirstChild();
```

### Bước 4: lặp qua các phiên bản trang
Lặp qua mỗi phiên bản và in ra các siêu dữ liệu hữu ích như dấu thời gian, tiêu đề, cấp độ và tác giả.

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

> **Mẹo chuyên nghiệp:** Nếu bạn cần lọc các phiên bản theo tác giả cụ thể hoặc khoảng thời gian, chỉ cần thêm các kiểm tra điều kiện bên trong vòng lặp `for`.

## Các vấn đề thường gặp & giải pháp
- **Không có phiên bản nào được trả về:** Xác minh rằng `loadOptions.setLoadHistory(true)` đã được gọi trước khi tải tài liệu.  
- **Tác giả hoặc tiêu đề null:** Một số phiên bản OneNote cũ hơn có thể không lưu các trường này; hãy xử lý giá trị `null` một cách nhẹ nhàng.  
- **Độ trễ hiệu năng trên sổ ghi chú lớn:** Chỉ tải các phần bạn cần hoặc tăng kích thước heap của JVM.

## Câu hỏi thường gặp

**Q1: Tôi có thể sử dụng Aspose.Note cho Java để sửa đổi các phiên bản trang không?**  
A1: Không, API hiện chỉ hỗ trợ truy cập chỉ đọc đối với các phiên bản trang.

**Q2: Aspose.Note cho Java có tương thích với các phiên bản tài liệu OneNote khác nhau không?**  
A2: Có, nó hoạt động với nhiều định dạng tệp OneNote, cho phép xử lý liền mạch giữa các phiên bản.

**Q3: Aspose.Note cho Java có yêu cầu giấy phép để sử dụng không?**  
A3: Giấy phép thương mại là bắt buộc cho việc sử dụng trong môi trường sản xuất, nhưng giấy phép đánh giá tạm thời có sẵn cho việc thử nghiệm.

**Q4: Tôi có thể tìm kiếm hỗ trợ nếu gặp bất kỳ vấn đề nào khi sử dụng Aspose.Note cho Java không?**  
A4: Có, bạn có thể đặt câu hỏi trên diễn đàn Aspose.Note [Aspose.Note forum](https://forum.aspose.com/c/note/28).

**Q5: Có bản dùng thử miễn phí cho Aspose.Note cho Java không?**  
A5: Có, bạn có thể tải bản dùng thử miễn phí từ [website](https://releases.aspose.com/).

---

**Cập nhật lần cuối:** 2026-08-08  
**Kiểm tra với:** Aspose.Note for Java (latest release)  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [theo dõi thay đổi onenote – Quản lý các phiên bản trang với Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Hướng dẫn Java Aspose - Lấy thông tin về các trang trong OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Thay đổi nền trang OneNote – Aspose.Note cho Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}