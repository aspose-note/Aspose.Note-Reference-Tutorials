---
title: Nhận bản sửa đổi của các trang trong OneNote - Aspose.Note
linktitle: Nhận bản sửa đổi của các trang trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Tìm hiểu cách truy xuất bản sửa đổi của các trang trong tài liệu OneNote bằng Aspose.Note Java. Tích hợp tính năng này vào ứng dụng Java của bạn để quản lý tài liệu hiệu quả.
type: docs
weight: 15
url: /vi/java/onenote-page-manipulation/get-revisions-of-pages/
---
## Giới thiệu

Trong hướng dẫn này, chúng ta sẽ đi sâu vào các khả năng của Aspose.Note for Java, một thư viện mạnh mẽ cho phép bạn làm việc liền mạch với các tệp Microsoft OneNote trong các ứng dụng Java của mình. Cụ thể, chúng tôi sẽ tập trung vào cách truy xuất các bản sửa đổi của các trang trong tài liệu OneNote. Đến cuối hướng dẫn này, bạn sẽ được trang bị kiến thức để trích xuất các bản sửa đổi trang một cách hiệu quả, bao gồm các chi tiết như thời gian sửa đổi lần cuối, thời gian tạo, tiêu đề, cấp độ và tác giả.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn này, hãy đảm bảo bạn đã thiết lập các điều kiện tiên quyết sau:

### Đã cài đặt Bộ công cụ phát triển Java (JDK)

Đảm bảo bạn đã cài đặt Bộ công cụ phát triển Java trên hệ thống của mình. Bạn có thể tải xuống và cài đặt nó từ trang web của Oracle hoặc sử dụng trình quản lý gói nếu bạn đang sử dụng hệ thống dựa trên Unix.

### Aspose.Note cho Thư viện Java

 Tải xuống và cài đặt thư viện Aspose.Note for Java từ trang web. Bạn có thể tìm thấy liên kết tải xuống[đây](https://releases.aspose.com/note/java/) . Thực hiện theo các hướng dẫn cài đặt được cung cấp trong tài liệu[đây](https://reference.aspose.com/note/java/).

## Gói nhập khẩu

Để bắt đầu, hãy nhập các gói cần thiết vào dự án Java của bạn. Các gói này sẽ cho phép bạn tận dụng chức năng do Aspose.Note for Java cung cấp.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Bây giờ, hãy chia mã ví dụ được cung cấp thành nhiều bước để hiểu từng thành phần và chức năng của nó.

## Bước 1: Đặt thư mục tài liệu

Xác định thư mục chứa tài liệu OneNote của bạn.

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tải tài liệu

Tải tài liệu OneNote vào Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Bước 3: Nhận trang đầu tiên

Lấy trang đầu tiên từ tài liệu.

```java
Page firstPage = doc.getFirstChild();
```

## Bước 4: Nhận bản sửa đổi trang

Lấy lịch sử sửa đổi của trang.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Bước 5: Duyệt qua các bản sửa đổi trang

Lặp lại danh sách các sửa đổi trang và truy xuất thông tin liên quan.

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

## Phần kết luận

Trong hướng dẫn này, chúng ta đã khám phá cách truy xuất các bản sửa đổi của các trang trong tài liệu OneNote bằng Aspose.Note for Java. Bằng cách làm theo hướng dẫn từng bước và tận dụng mã ví dụ được cung cấp, bạn có thể dễ dàng tích hợp chức năng này vào các ứng dụng Java của mình, cho phép quản lý hiệu quả các tệp OneNote.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.Note for Java để tạo tài liệu OneNote mới không?

Câu trả lời 1: Có, Aspose.Note for Java cung cấp hỗ trợ toàn diện cho việc tạo, đọc và thao tác các tài liệu OneNote theo chương trình.

### Câu hỏi 2: Aspose.Note for Java có tương thích với các phiên bản khác nhau của tệp OneNote không?

Câu trả lời 2: Có, Aspose.Note for Java hỗ trợ nhiều phiên bản khác nhau của tệp Microsoft OneNote, đảm bảo khả năng tương thích trên các môi trường khác nhau.

### Câu hỏi 3: Tôi có thể tùy chỉnh định dạng đầu ra khi xuất tài liệu OneNote không?

Câu trả lời 3: Hoàn toàn có thể, Aspose.Note for Java mang đến sự linh hoạt trong việc xuất tài liệu OneNote sang các định dạng khác nhau như PDF, HTML và hình ảnh, cùng với các tùy chọn để tùy chỉnh.

### Câu hỏi 4: Aspose.Note for Java có yêu cầu giấy phép sử dụng thương mại không?

Câu trả lời 4: Có, cần có giấy phép hợp lệ để sử dụng Aspose.Note cho Java vì mục đích thương mại. Bạn có thể lấy giấy phép từ trang web Aspose.

### Câu hỏi 5: Tôi có thể tìm kiếm hỗ trợ ở đâu nếu gặp sự cố hoặc có thắc mắc về Aspose.Note dành cho Java?

 Câu trả lời 5: Để được hỗ trợ và trợ giúp, bạn có thể truy cập diễn đàn Aspose.Note[đây](https://forum.aspose.com/c/note/28)nơi bạn có thể đặt câu hỏi, chia sẻ kinh nghiệm và tương tác với những người dùng và chuyên gia khác.