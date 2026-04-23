---
date: 2026-03-19
description: Học cách thêm hình ảnh vào OneNote bằng Java với Aspose.Note for Java,
  bao gồm cách đặt kích thước hình ảnh trong Java và lưu OneNote dưới dạng PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Thêm hình ảnh vào OneNote bằng Java
url: /vi/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chèn Hình Ảnh vào Tài liệu OneNote bằng Java

## Introduction

Trong hướng dẫn này, bạn sẽ học **cách thêm hình ảnh vào OneNote** bằng cách lập trình sử dụng Java và thư viện Aspose.Note for Java. Nhúng hình ảnh vào các trang OneNote rất hữu ích khi bạn cần tạo biên bản họp, báo cáo tự động, hoặc tài liệu kết hợp văn bản với dữ liệu hình ảnh. Khi hoàn thành hướng dẫn, bạn sẽ có thể tải một tệp OneNote hiện có, chèn một hình ảnh, tùy chọn điều chỉnh kích thước và vị trí, và thậm chí **lưu OneNote dưới dạng PDF** – tất cả mà không cần mở giao diện người dùng OneNote.

## Quick Answers
- **Cách dễ nhất để thêm hình ảnh vào OneNote bằng Java là gì?**  
  Sử dụng lớp `Image` của Aspose.Note for Java và thêm nó vào một trang.
- **Tôi có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?**  
  Có, cần giấy phép thương mại cho các triển khai sản xuất.
- **Tôi có thể đặt kích thước tùy chỉnh cho hình ảnh không?**  
  Chắc chắn – gọi `setWidth()` và `setHeight()` trên đối tượng `Image`.
- **Có thể lưu tệp OneNote dưới dạng PDF sau khi thêm hình ảnh không?**  
  Có, gọi `save(..., SaveFormat.Pdf)` để **lưu OneNote dưới dạng PDF**.
- **Phiên bản Java nào được hỗ trợ?**  
  Aspose.Note for Java hoạt động với JDK 8 trở lên.

## Why add image to OneNote?

Thêm các yếu tố hình ảnh làm cho ghi chú dễ hiểu hơn và hấp dẫn hơn. Hình ảnh có thể minh họa sơ đồ, ảnh chụp màn hình, hoặc biểu đồ dữ liệu mà nếu không sẽ cần mô tả bằng văn bản dài dòng. Tự động hoá bước này tiết kiệm thời gian, đặc biệt khi tạo ra một lượng lớn ghi chú từ các nguồn dữ liệu.

## Prerequisites

Trước khi bắt đầu, hãy chắc chắn bạn đã chuẩn bị các mục sau:

### 1. Java Development Kit (JDK)
Cài đặt JDK 8 hoặc mới hơn. Bạn có thể tải xuống từ trang web Oracle hoặc sử dụng bản phân phối OpenJDK.

### 2. Aspose.Note for Java Library
Tải thư viện Aspose.Note for Java mới nhất và thêm vào classpath của dự án. Hướng dẫn cài đặt chi tiết có sẵn trong [tài liệu chính thức](https://reference.aspose.com/note/java/).

## Import Packages

Bắt đầu bằng việc nhập các lớp cần thiết. Các import này cung cấp quyền truy cập vào chức năng cốt lõi của Aspose.Note cũng như các tiện ích cơ bản của Java.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

Dưới đây là một hướng dẫn ngắn gọn, được đánh số. Mỗi bước bao gồm một giải thích ngắn gọn và đoạn mã chính xác bạn cần sao chép.

### Step 1: Load the OneNote document

Chúng ta tạo một thể hiện `LoadOptions` (hữu ích cho các tùy chỉnh trong tương lai) và mở tệp `.one` hiện có.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### Step 2: Get the target page

Để đơn giản, chúng ta làm việc với trang đầu tiên trong tài liệu, nhưng bạn có thể điều hướng tới bất kỳ trang nào bạn cần.

```java
Page page = oneFile.getFirstChild();
```

### Step 3: Load the image you want to embed

Khởi tạo một đối tượng `Image` bằng cách truyền tham chiếu tài liệu và đường dẫn tới tệp hình ảnh.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### Step 4: Set image dimensions Java (optional)

Nếu bạn cần hình ảnh vừa với một khu vực cụ thể, hãy điều chỉnh chiều rộng, chiều cao và độ lệch. Đây là nơi từ khóa phụ **set image dimensions java** tỏa sáng.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### Step 5: Append the image to the page

Phương thức `appendChildLast` thêm hình ảnh vào vị trí cuối cùng trên trang đã chọn.

```java
page.appendChildLast(image);
```

### Step 6: Save the document – you can also save OneNote as PDF

Cuối cùng, lưu các thay đổi. Ví dụ minh họa việc lưu tệp dưới dạng PDF, đáp ứng từ khóa phụ **save onenote as pdf**.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Common Issues and Solutions

| Triệu chứng | Nguyên nhân có thể | Cách khắc phục |
|-------------|--------------------|----------------|
| `FileNotFoundException` khi tải hình ảnh | Đường dẫn hình ảnh không đúng | Kiểm tra lại `dataDir` và tên tệp hình ảnh. |
| Hình ảnh bị biến dạng | Chiều rộng/chiều cao được đặt không đúng | Sử dụng kích thước gốc của hình ảnh hoặc tính toán tỷ lệ phù hợp trước khi gọi `setWidth`/`setHeight`. |
| Kết quả PDF trống | Thiếu giấy phép cho Aspose.Note | Áp dụng giấy phép hợp lệ trước khi gọi `save`. |

## Frequently Asked Questions

### Q1: Tôi có thể chèn nhiều hình ảnh vào một tài liệu OneNote duy nhất bằng phương pháp này không?

**A:** Có. Chỉ cần lặp lại Các bước 3‑5 cho mỗi hình ảnh bạn muốn thêm, hướng tới cùng một trang hoặc các trang khác.

### Q2: Aspose.Note for Java có tương thích với mọi phiên bản OneNote không?

**A:** Aspose.Note for Java hỗ trợ các tệp OneNote được tạo bằng Microsoft OneNote 2010 và các phiên bản sau.

### Q3: Tôi có thể chèn hình ảnh ở các định dạng khác nhau, như PNG hoặc GIF, vào tài liệu OneNote không?

**A:** Chắc chắn. Thư viện chấp nhận PNG, JPEG, GIF, BMP và một số định dạng phổ biến khác.

### Q4: Có phiên bản dùng thử của Aspose.Note for Java để thử nghiệm không?

**A:** Có, bạn có thể tải bản dùng thử miễn phí từ trang web Aspose để đánh giá API trước khi mua.

### Q5: Làm thế nào để tôi nhận được hỗ trợ kỹ thuật cho Aspose.Note for Java?

**A:** Bạn có thể nhận trợ giúp bằng cách truy cập [diễn đàn](https://forum.aspose.com/c/note/28) dành cho các sản phẩm Aspose.Note.

## Conclusion

Bạn giờ đã có một ví dụ hoàn chỉnh, sẵn sàng cho môi trường sản xuất, cho thấy **cách thêm hình ảnh vào OneNote** bằng Java, tùy chỉnh giao diện của nó, và tùy chọn **lưu OneNote dưới dạng PDF**. Hãy tự do điều chỉnh mã cho quy trình làm việc của mình—cho dù bạn đang xây dựng một công cụ báo cáo, hệ thống tài liệu tự động, hoặc một ứng dụng ghi chú tùy chỉnh.

---

**Last Updated:** 2026-03-19  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}