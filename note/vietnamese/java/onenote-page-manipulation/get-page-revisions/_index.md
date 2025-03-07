---
title: Nhận các bản sửa đổi trang trong OneNote - Aspose.Note
linktitle: Nhận các bản sửa đổi trang trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Tìm hiểu cách truy xuất các bản sửa đổi trang trong OneNote bằng Aspose.Note for Java. Hãy làm theo hướng dẫn từng bước của chúng tôi để theo dõi các thay đổi một cách hiệu quả.
weight: 14
url: /vi/java/onenote-page-manipulation/get-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nhận các bản sửa đổi trang trong OneNote - Aspose.Note

## Giới thiệu

OneNote là một công cụ mạnh mẽ để sắp xếp và quản lý ghi chú của bạn, nhưng đôi khi bạn cần theo dõi các thay đổi và sửa đổi được thực hiện trên trang của mình. Với Aspose.Note for Java, bạn có thể dễ dàng truy xuất các bản sửa đổi trang theo chương trình. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình nhận các bản sửa đổi trang trong OneNote bằng Aspose.Note for Java.

## Điều kiện tiên quyết

Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

### 1. Bộ công cụ phát triển Java (JDK)

Đảm bảo bạn đã cài đặt Bộ công cụ phát triển Java (JDK) trên hệ thống của mình. Bạn có thể tải xuống và cài đặt JDK từ trang web của Oracle.

### 2. Aspose.Note cho Java

Tải xuống và cài đặt Aspose.Note cho Java từ[Liên kết tải xuống](https://releases.aspose.com/note/java/).

### 3. Tài liệu OneNote mẫu

Chuẩn bị một tài liệu OneNote mẫu (`Sample1.one`) có chứa các trang bạn muốn truy xuất các bản sửa đổi.

## Gói nhập khẩu

Trước tiên, bạn cần nhập các gói cần thiết từ Aspose.Note cho Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Bây giờ, hãy chia ví dụ được cung cấp thành nhiều bước:

## Bước 1: Thiết lập thư mục tài liệu

Xác định đường dẫn thư mục nơi chứa tài liệu OneNote của bạn.

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tải tài liệu OneNote

 Tải tài liệu OneNote bằng cách sử dụng`LoadOptions` để kích hoạt lịch sử tải.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Bước 3: Nhận trang đầu tiên

Truy xuất trang đầu tiên từ tài liệu đã tải.

```java
Page firstPage = document.getFirstChild();
```

## Bước 4: Lặp lại các lần sửa đổi trang

Lặp lại qua từng bản sửa đổi trang và truy xuất thông tin liên quan như thời gian sửa đổi lần cuối, thời gian tạo, tiêu đề, cấp độ và tác giả.

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

## Phần kết luận

Trong hướng dẫn này, chúng ta đã tìm hiểu cách truy xuất các bản sửa đổi trang trong OneNote bằng Aspose.Note for Java. Bằng cách làm theo các bước này, bạn có thể theo dõi các thay đổi được thực hiện trên các trang OneNote của mình một cách hiệu quả theo chương trình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.Note for Java để sửa đổi các bản sửa đổi trang không?

Câu trả lời 1: Không, Aspose.Note for Java hiện hỗ trợ truy xuất các bản sửa đổi trang nhưng không sửa đổi chúng.

### Câu hỏi 2: Aspose.Note for Java có tương thích với các phiên bản khác nhau của tài liệu OneNote không?

Câu trả lời 2: Có, Aspose.Note for Java hỗ trợ nhiều phiên bản khác nhau của tài liệu OneNote, cho phép bạn làm việc liền mạch với các định dạng tệp khác nhau.

### Câu hỏi 3: Aspose.Note dành cho Java có cần giấy phép sử dụng không?

Câu trả lời 3: Có, bạn cần mua giấy phép để sử dụng Aspose.Note cho Java trong các dự án thương mại. Tuy nhiên, bạn cũng có thể có được giấy phép tạm thời cho mục đích đánh giá.

### Câu hỏi 4: Tôi có thể tìm kiếm hỗ trợ nếu gặp bất kỳ sự cố nào khi sử dụng Aspose.Note cho Java không?

 Câu trả lời 4: Có, bạn có thể tìm kiếm sự hỗ trợ từ diễn đàn Aspose.Note[đây](https://forum.aspose.com/c/note/28).

### Câu hỏi 5: Có bản dùng thử miễn phí cho Aspose.Note cho Java không?

 Câu trả lời 5: Có, bạn có thể truy cập bản dùng thử miễn phí Aspose.Note dành cho Java từ[trang mạng](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
