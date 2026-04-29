---
date: 2026-01-18
description: Học cách xuất OneNote một cách hiệu quả và cách xuất OneNote với hiệu
  suất tối ưu bằng Aspose.Note cho Java. Bao gồm các bước thiết lập kiểu văn bản mặc
  định và lưu OneNote dưới dạng hình ảnh.
linktitle: How to Export OneNote – Optimize Performance for Export Operations in Java
second_title: Aspose.Note Java API
title: Cách xuất OneNote – Tối ưu hiệu suất cho các thao tác xuất trong Java
url: /vi/java/onenote-performance-optimization/optimize-performance-consequent-export/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách xuất OneNote – Tối ưu hiệu suất cho các hoạt động xuất trong Java

## Giới thiệu

Việc xuất sổ tay OneNote có thể là một nút thắt khi bạn cần tạo báo cáo, chia sẻ nội dung hoặc lưu trữ dữ liệu. Trong hướng dẫn này, chúng tôi sẽ chỉ **cách xuất OneNote** một cách nhanh chóng và đáng tin cậy bằng cách sử dụng Aspose.Note cho Java. Bạn sẽ học các kỹ thuật thực tế để cải thiện tốc độ xuất, đặt kiểu văn bản mặc định, và thậm chí **lưu OneNote dưới dạng hình ảnh** như JPG hoặc BMP.

## Câu trả lời nhanh
- **Thư viện chính là gì?** Aspose.Note for Java  
- **Các định dạng có thể xuất là gì?** HTML, PDF, JPG, BMP (và hơn nữa)  
- **Làm thế nào để cải thiện hiệu suất?** Tắt phát hiện bố cục tự động và tái sử dụng các đối tượng tài liệu  
- **Có thể đặt kiểu văn bản mặc định không?** Có – sử dụng `ParagraphStyle` trước khi thêm nội dung  
- **Xuất ra hình ảnh có được hỗ trợ không?** Chắc chắn, sử dụng `doc.save(...".jpg")` hoặc `.bmp`  

## “how to export onenote” là gì?

Xuất OneNote có nghĩa là chuyển đổi cấu trúc tệp OneNote gốc sang một định dạng di động (HTML, PDF, hình ảnh, v.v.). Điều này cho phép chia sẻ trên các nền tảng, truy cập ngoại tuyến và tích hợp với các quy trình công việc kinh doanh khác.

## Tại sao cần tối ưu hiệu suất xuất?

Các sổ tay lớn với nhiều trang và đa phương tiện phong phú có thể gây ra quá trình chuyển đổi chậm. Bằng cách điều chỉnh một vài cài đặt—như tắt phát hiện thay đổi bố cục tự động—bạn giảm tải CPU và sử dụng bộ nhớ, mang lại việc xuất nhanh hơn và dự đoán được hơn.

## Yêu cầu trước

Trước khi bắt đầu, hãy đảm bảo các mục sau đã được cài đặt:

### 1. Java Development Kit (JDK)

Đảm bảo bạn có một JDK mới. Bạn có thể tải xuống từ [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### 2. Aspose.Note for Java

Lấy gói Aspose.Note for Java mới nhất từ [liên kết tải xuống](https://releases.aspose.com/note/java/).

### 3. Môi trường phát triển tích hợp (IDE)

Bất kỳ IDE Java nào cũng hoạt động—IntelliJ IDEA, Eclipse hoặc NetBeans đều là lựa chọn tốt.

## Nhập các gói

Trước khi bắt đầu viết mã, nhập các lớp mà chúng ta sẽ cần:

```java
import java.awt.Color;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Hướng dẫn từng bước

### Bước 1. Khởi tạo Document và Page

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
doc.setAutomaticLayoutChangesDetectionEnabled(false);
Page page = new Page();
```

Chúng ta tạo một thể hiện `Document` mới và **tắt phát hiện thay đổi bố cục tự động**—một điều chỉnh quan trọng để xuất nhanh hơn. Sau đó chúng ta thêm một đối tượng `Page` mới sẽ chứa nội dung của chúng ta.

### Bước 2. Đặt kiểu văn bản mặc định *(set default text style)*

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.BLACK)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Định nghĩa một **kiểu văn bản mặc định** một lần và tái sử dụng cho mọi phần tử văn bản giúp tiết kiệm thời gian xử lý và đảm bảo giao diện nhất quán.

### Bước 3. Thêm tiêu đề

```java
RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);

RichText titleDate = new RichText().append("2011,11,11");
titleDate.setParagraphStyle(textStyle);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);

Title title = new Title();
title.setTitleText(titleText);
title.setTitleDate(titleDate);
title.setTitleTime(titleTime);
page.setTitle(title);
```

Ở đây chúng ta xây dựng một phần tiêu đề với ba đối tượng `RichText` riêng biệt (tiêu đề, ngày, giờ) và áp dụng **kiểu văn bản mặc định** mà chúng ta đã định nghĩa trước đó.

### Bước 4. Gắn nút Page

```java
doc.appendChildLast(page);
```

Trang hiện đã là một phần của cây tài liệu, sẵn sàng để xuất.

### Bước 5. Lưu tài liệu ở các định dạng khác nhau *(save onenote as image, convert onenote jpg)*

```java
doc.save(dataDir + "OptimizePerformanceForConsequentExportOperations_out.html");
doc.save(dataDir + "OptimizePerformanceForConsequentExportOperations_out.pdf");
doc.save(dataDir + "OptimizePerformanceForConsequentExportOperations_out.jpg");
doc.save(dataDir + "OptimizePerformanceForConsequentExportOperations_out.bmp");
```

Chúng tôi trình diễn **lưu OneNote dưới dạng hình ảnh** (JPG, BMP) cũng như HTML và PDF. Điều này bao phủ các kịch bản xuất phổ biến nhất, bao gồm trường hợp sử dụng **convert onenote jpg**.

### Bước 6. Đặt kích thước phông chữ và phát hiện thay đổi bố cục

```java
textStyle.setFontSize(11);
doc.detectLayoutChanges();
```

Nếu bạn cần điều chỉnh kích thước phông chữ sau khi xuất lần đầu, chỉ cần cập nhật `ParagraphStyle` và gọi `detectLayoutChanges()` để áp dụng lại logic bố cục mà không cần tạo lại tài liệu.

## Vấn đề thường gặp & Mẹo

- **Hiệu suất vẫn chậm?** Kiểm tra rằng `setAutomaticLayoutChangesDetectionEnabled(false)` được gọi trước khi bất kỳ trang nào được thêm.  
- **Hình ảnh xuất hiện trống?** Đảm bảo thư mục đầu ra có quyền ghi và các phần mở rộng định dạng hình ảnh khớp với tên tệp.  
- **Sổ tay lớn gây OutOfMemoryError?** Xử lý các trang theo lô hoặc tăng kích thước heap JVM (`-Xmx2g`).  

## Câu hỏi thường gặp

**Q: Tôi có thể sử dụng Aspose.Note cho Java để xuất tài liệu OneNote một cách lập trình không?**  
A: Có, Aspose.Note cho Java cung cấp một API đầy đủ để thao tác và xuất sổ tay OneNote mà không cần ứng dụng desktop.

**Q: Aspose.Note cho Java có tương thích với các IDE Java khác nhau không?**  
A: Chắc chắn. Thư viện hoạt động với IntelliJ IDEA, Eclipse, NetBeans và bất kỳ IDE nào hỗ trợ dự án Java tiêu chuẩn.

**Q: Làm sao tôi có thể nhận được giấy phép tạm thời để thử nghiệm?**  
A: Bạn có thể yêu cầu giấy phép tạm thời từ [website](https://purchase.aspose.com/temporary-license/), cho phép bạn đánh giá sản phẩm trước khi mua.

**Q: Aspose.Note có hỗ trợ xuất sang các định dạng hình ảnh như JPG và BMP không?**  
A: Có, các phương thức `doc.save(...".jpg")` và `doc.save(...".bmp")` cho phép bạn **lưu OneNote dưới dạng hình ảnh** để dễ dàng nhúng các trang vào báo cáo hoặc bản trình bày.

**Q: Tôi có thể nhận hỗ trợ cộng đồng hoặc đặt câu hỏi kỹ thuật ở đâu?**  
A: Truy cập diễn đàn chính thức của Aspose tại [forum](https://forum.aspose.com/c/note/28) để nhận trợ giúp từ cộng đồng và các kỹ sư Aspose.

## Kết luận

Bằng cách làm theo hướng dẫn này, bạn giờ đã biết **cách xuất OneNote** một cách hiệu quả, cách **đặt kiểu văn bản mặc định**, và cách **lưu OneNote dưới dạng hình ảnh** như JPG và BMP. Những kỹ thuật này giúp bạn xây dựng các quy trình xuất nhanh, đáng tin cậy cho bất kỳ ứng dụng nào dựa trên Java.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-18  
**Tested With:** Aspose.Note for Java 24.12 (latest)  
**Author:** Aspose  

---