---
date: 2026-01-10
description: Tìm hiểu cách lấy thời gian chỉnh sửa cuối cùng và truy xuất các phiên
  bản của các trang OneNote bằng Aspose.Note cho Java. Tích hợp tính năng này vào
  các ứng dụng Java của bạn để quản lý tài liệu hiệu quả.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Cách lấy thời gian sửa đổi lần cuối của các trang OneNote – Aspose.Note
url: /vi/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lấy các Phiên bản của Trang trong OneNote - Aspose.Note

## Introduction

Trong hướng dẫn này, bạn sẽ **lấy thời gian sửa đổi lần cuối** cho các trang trong tài liệu OneNote và khám phá cách truy xuất lịch sử phiên bản đầy đủ bằng Aspose.Note cho Java. Dù bạn đang xây dựng hệ thống quản lý tài liệu, kiểm toán các thay đổi, hay chỉ cần hiển thị thời gian trang được chỉnh sửa lần cuối, hướng dẫn này sẽ chỉ cho bạn cách trích xuất thông tin đó một cách lập trình.

## Quick Answers
- **“get last modified time” trả về gì?** Dấu thời gian của lần chỉnh sửa gần nhất trên một trang OneNote.  
- **Lớp nào cung cấp lịch sử phiên bản?** `PageHistory` thông qua `Document.getPageHistory(Page)`.  
- **Tôi có cần giấy phép cho tính năng này không?** Có, cần một giấy phép Aspose.Note hợp lệ để sử dụng trong môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Java 8 hoặc cao hơn (JDK 8+).  
- **Tôi có thể lọc các phiên bản theo tác giả không?** Bạn có thể đọc thuộc tính `Author` của mỗi đối tượng `Page` và tự áp dụng bộ lọc.

## What is “get last modified time” in OneNote?

Thời gian **sửa đổi lần cuối** là một trường siêu dữ liệu được lưu cùng với mỗi trang, ghi lại thời điểm trang được thay đổi gần nhất. Aspose.Note cung cấp giá trị này thông qua phương thức `Page.getLastModifiedTime()`, giúp dễ dàng hiển thị hoặc ghi lại ngày thay đổi.

## Why retrieve page revisions?

- **Dấu vết kiểm toán:** Giữ bản ghi ai đã thay đổi gì và khi nào.  
- **So sánh phiên bản:** Xây dựng tính năng so sánh hai phiên bản cạnh nhau.  
- **Nhận thức về cộng tác người dùng:** Hiểu các mẫu chỉnh sửa trong sổ ghi chú được chia sẻ.  

## Prerequisites

Before you start, make sure you have the following:

### Java Development Kit (JDK) Installed
Cài đặt JDK 8 hoặc phiên bản mới hơn từ trang web Oracle hoặc trình quản lý gói ưa thích của bạn.

### Aspose.Note for Java Library
Tải thư viện từ trang chính thức. Bạn có thể tìm liên kết tải xuống **[tại đây](https://releases.aspose.com/note/java/)**. Thực hiện theo hướng dẫn cài đặt trong tài liệu **[tại đây](https://reference.aspose.com/note/java/)**.

## Import Packages

To begin, import the necessary packages into your Java project. These packages will allow you to leverage the functionality provided by Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Now, let's break down the example code provided into multiple steps to understand each component and its functionality.

## How to Get Last Modified Time of a OneNote Page

### Step 1: Set Document Directory
Define the directory where your OneNote document is located.

```java
String dataDir = "Your Document Directory";
```

### Step 2: Load the Document
Load the OneNote document into Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Step 3: Get First Page
Retrieve the first page from the document.

```java
Page firstPage = doc.getFirstChild();
```

### Step 4: Get Page Revisions
Obtain the revisions history of the page.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Step 5: Traverse Page Revisions
Iterate through the list of page revisions and retrieve relevant information, including the **last modified time**.

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

## Common Issues and Solutions
- **`PageHistory` null:** Đảm bảo tài liệu thực sự chứa các phiên bản; nếu không `getPageHistory` có thể trả về `null`.  
- **Khác biệt múi giờ:** `getLastModifiedTime()` trả về một `java.util.Date` theo múi giờ mặc định của hệ thống. Chuyển sang UTC nếu cần.  
- **Giấy phép chưa được tải:** Nếu không có giấy phép hợp lệ, Aspose.Note có thể chạy ở chế độ đánh giá, giới hạn số trang được xử lý.

## Frequently Asked Questions

### Q1: Can I use Aspose.Note for Java to create new OneNote documents?
A1: Có, Aspose.Note cho Java cung cấp hỗ trợ toàn diện để tạo, đọc và thao tác các tài liệu OneNote một cách lập trình.

### Q2: Is Aspose.Note for Java compatible with different versions of OneNote files?
A2: Có, Aspose.Note cho Java hỗ trợ nhiều phiên bản tệp Microsoft OneNote, đảm bảo tính tương thích trên các môi trường khác nhau.

### Q3: Can I customize the output format when exporting OneNote documents?
A3: Chắc chắn, Aspose.Note cho Java cung cấp tính linh hoạt trong việc xuất tài liệu OneNote sang các định dạng khác nhau như PDF, HTML và hình ảnh, với các tùy chọn tùy chỉnh.

### Q4: Does Aspose.Note for Java require a license for commercial use?
A4: Có, cần một giấy phép hợp lệ để sử dụng Aspose.Note cho Java trong môi trường thương mại. Bạn có thể lấy giấy phép từ trang web Aspose.

### Q5: Where can I seek assistance if I encounter issues or have questions about Aspose.Note for Java?
A5: Để được hỗ trợ và trợ giúp, bạn có thể truy cập diễn đàn Aspose.Note **[tại đây](https://forum.aspose.com/c/note/28)**, nơi bạn có thể đặt câu hỏi, chia sẻ kinh nghiệm và tương tác với các người dùng và chuyên gia khác.

---

**Cập nhật lần cuối:** 2026-01-10  
**Đã kiểm tra với:** Aspose.Note for Java 23.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}