---
date: 2025-12-20
description: Tìm hiểu cách thêm hình ảnh vào OneNote bằng Aspose.Note cho Java. Hướng
  dẫn từng bước để tạo tài liệu OneNote và chèn hình ảnh một cách lập trình.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Cách thêm hình ảnh vào OneNote bằng Java – Tạo tài liệu và chèn hình
url: /vi/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách thêm hình ảnh vào OneNote bằng Java – Tạo tài liệu và chèn ảnh

## Introduction

Trong hướng dẫn này, bạn sẽ học **cách thêm hình ảnh vào OneNote** bằng API Aspose.Note Java. Chúng tôi sẽ hướng dẫn tạo tài liệu OneNote từ đầu, chèn một hình ảnh, và lưu kết quả dưới dạng PDF. Dù bạn đang xây dựng công cụ báo cáo, tự động ghi chú, hay chỉ cần nhúng đồ họa bằng lập trình, hướng dẫn này cung cấp một lộ trình rõ ràng, thực hành.

## Quick Answers
- **Thư viện tôi cần là gì?** Aspose.Note for Java.  
- **Tôi có thể chèn bất kỳ định dạng hình ảnh nào không?** JPEG, PNG, BMP, GIF và nhiều định dạng khác được hỗ trợ.  
- **Các định dạng xuất nào có sẵn?** Bạn có thể lưu dưới dạng OneNote, PDF, XPS, HTML, v.v.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Có, cần giấy phép thương mại cho việc sử dụng không phải thử nghiệm.  
- **Mã có đa nền tảng không?** Chắc chắn – Java chạy trên Windows, Linux và macOS.

## What is “add picture to OneNote”?
Thêm hình ảnh vào OneNote có nghĩa là nhúng một tệp hình ảnh vào một trang OneNote một cách lập trình sao cho nó hiển thị cùng với văn bản, dàn trang hoặc các yếu tố khác. API Aspose.Note trừu tượng hoá định dạng tệp OneNote, cho phép bạn tập trung vào nội dung thay vì cấu trúc XML bên trong.

## Why add picture to OneNote using Java?
- **Tự động hoá:** Tự động tạo biên bản họp với ảnh chụp màn hình.  
- **Nhất quán:** Đảm bảo mọi trang tuân theo cùng một bố cục và thương hiệu.  
- **Tích hợp:** Kết hợp dữ liệu từ các hệ thống khác (ví dụ, biểu đồ) trực tiếp vào sổ tay OneNote.  
- **Đa nền tảng:** Java cho phép bạn chạy cùng một mã trên bất kỳ môi trường máy chủ hoặc máy tính để bàn nào.

## Prerequisites

Trước khi bắt đầu, hãy chắc chắn rằng bạn có các yêu cầu sau:

1. **Java Development Kit (JDK)** – bất kỳ phiên bản mới nào (8 trở lên).  
2. **Thư viện Aspose.Note for Java** – tải xuống từ [website](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình chỉnh sửa Java nào bạn thích.  

## Import Packages

Bắt đầu bằng cách nhập các lớp cần thiết vào tệp nguồn Java của bạn:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

### Step 1: Set Up the Document

Tạo một tài liệu OneNote mới và một container trang nơi nội dung sẽ được đặt.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Step 2: Initialize the Outline

Một *outline* hoạt động như một container cho các yếu tố như văn bản và hình ảnh. Chúng ta đặt các offset của nó về 0 để nội dung bắt đầu ở góc trên‑trái.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Step 3: Load and Align the Image

Tải hình ảnh bạn muốn nhúng và căn chỉnh nó sang phía bên phải của trang. Đây là nơi chúng ta thực sự **thêm hình ảnh vào OneNote**.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Step 4: Attach the Image to an Outline Element

Đóng gói hình ảnh bên trong một `OutlineElement`. Bước này liên kết đối tượng hình ảnh với cấu trúc outline của tài liệu.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Step 5: Assemble the Document Structure

Thêm phần tử outline vào outline, sau đó gắn outline vào trang, và cuối cùng thêm trang vào tài liệu.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Step 6: Save the OneNote Document

Lưu tài liệu xuống đĩa. Trong ví dụ này chúng tôi xuất ra PDF, nhưng bạn cũng có thể lưu dưới dạng tệp OneNote gốc (`.one`) bằng cách thay đổi `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Common Issues and Solutions

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **Hình ảnh không hiển thị** | Đường dẫn tệp sai hoặc định dạng không được hỗ trợ. | Xác minh `dataDir` trỏ tới thư mục đúng và sử dụng định dạng hình ảnh được hỗ trợ (JPEG, PNG, v.v.). |
| **Tài liệu được lưu dưới dạng PDF rỗng** | Các offset của outline được đặt không đúng. | Đảm bảo gọi `setVerticalOffset(0)` và `setHorizontalOffset(0)`, hoặc điều chỉnh offset để đặt nội dung trong giới hạn trang. |
| **IOException khi lưu** | Thư mục đích không tồn tại hoặc thiếu quyền ghi. | Tạo thư mục trước hoặc chạy chương trình với quyền phù hợp. |

## Frequently Asked Questions

**Q1: Tôi có thể tìm tài liệu cho Aspose.Note for Java ở đâu?**  
A1: Bạn có thể truy cập tài liệu [tại đây](https://reference.aspose.com/note/java/).

**Q2: Làm sao để tải Aspose.Note for Java?**  
A2: Bạn có thể tải Aspose.Note for Java từ [trang tải xuống](https://releases.aspose.com/note/java/).

**Q3: Có bản dùng thử miễn phí cho Aspose.Note for Java không?**  
A3: Có, bạn có thể nhận bản dùng thử miễn phí từ [website](https://releases.aspose.com/).

**Q4: Tôi có thể nhận hỗ trợ cho Aspose.Note for Java ở đâu?**  
A4: Để được hỗ trợ, hãy truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28).

**Q5: Tôi có thể lấy giấy phép tạm thời cho Aspose.Note for Java không?**  
A5: Có, bạn có thể yêu cầu giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

---

**Cập nhật lần cuối:** 2025-12-20  
**Kiểm tra với:** Aspose.Note for Java 24.12 (latest)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}