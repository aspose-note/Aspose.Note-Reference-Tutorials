---
date: 2026-06-30
description: Tìm hiểu cách xuất OneNote bằng cách lưu tài liệu dưới dạng hình ảnh
  PNG thang xám bằng Aspose.Note cho Java. Bao gồm các bước tải tài liệu OneNote và
  tạo hình ảnh thang xám.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Cách xuất OneNote dưới dạng hình ảnh thang xám – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Cách xuất OneNote dưới dạng hình ảnh thang xám – Aspose.Note
url: /vi/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu thành Hình ảnh Đen trắng trong OneNote - Aspose.Note

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách xuất onenote** bằng cách chuyển đổi tệp OneNote `.one` thành một hình ảnh PNG đen‑trắng chất lượng cao bằng Aspose.Note cho Java. Chuyển đổi sang thang độ xám thường được các nhà phát triển Java cần cho việc in ấn, lưu trữ, hoặc để **giảm kích thước OneNote** mà không mất nội dung quan trọng. Chúng tôi sẽ hướng dẫn cách tải tài liệu OneNote, cấu hình các tùy chọn lưu — bao gồm **điều chỉnh độ phân giải hình ảnh** — và cuối cùng lưu tài liệu dưới dạng PNG.

## Câu trả lời nhanh
- **Câu hỏi “cách xuất onenote” có nghĩa là gì?** Nó đề cập đến việc chuyển đổi một tệp OneNote thành định dạng khác một cách lập trình, chẳng hạn như hình ảnh, bằng mã.  
- **Định dạng nào là tốt nhất cho đầu ra đen‑trắng?** PNG hoạt động tốt vì nó giữ chất lượng không mất dữ liệu và hỗ trợ chế độ màu đen‑trắng riêng.  
- **Tôi có cần giấy phép không?** Một giấy phép Aspose.Note hợp lệ là bắt buộc cho việc sử dụng trong môi trường sản xuất; giấy phép dùng thử tạm thời có sẵn để thử nghiệm.  
- **Yêu cầu phiên bản Java nào?** Java 8 hoặc cao hơn được khuyến nghị.  
- **Tôi có thể thay đổi kích thước hình ảnh không?** Có, bạn có thể điều chỉnh các thuộc tính của `ImageSaveOptions` như `Resolution` hoặc `PageSize` trước khi lưu.  

## “cách xuất onenote” là gì?

Xuất OneNote có nghĩa là chuyển đổi một tệp OneNote `.one` thành một dạng biểu diễn khác—chẳng hạn PDF, HTML, hoặc hình ảnh—một cách lập trình. Trong hướng dẫn này, chúng tôi tập trung vào **tạo hình ảnh PNG đen‑trắng**, một yêu cầu phổ biến cho tài liệu hoặc quy trình chuẩn bị in. Sử dụng Aspose.Note, quá trình chuyển đổi diễn ra hoàn toàn trong bộ nhớ, vì vậy bạn không bao giờ cần cài đặt Microsoft OneNote trên máy chủ.

## Tại sao xuất OneNote dưới dạng hình ảnh đen‑trắng?

Các tệp PNG đen‑trắng thường **nhỏ hơn 30‑40 %** so với phiên bản màu đầy đủ, giúp tăng tốc độ truyền tải trên web và giảm chi phí lưu trữ. Chúng cũng cung cấp **độ tương phản rõ ràng hơn** trên máy in laser, làm cho báo cáo dễ đọc hơn. Vì PNG được hỗ trợ rộng rãi, các tệp tạo ra có thể hoạt động trên trình duyệt, thiết bị di động và trình soạn thảo trên máy tính mà không cần codec bổ sung.

## Yêu cầu trước

1. Java Development Kit (JDK) 8 hoặc mới hơn đã được cài đặt.  
2. Thư viện Aspose.Note cho Java – tải bản phát hành mới nhất từ [tại đây](https://releases.aspose.com/note/java/).  
3. Hiểu biết cơ bản về cú pháp Java và cấu hình dự án Maven/Gradle.  

## Nhập gói

Lớp `ImageSaveOptions` kiểm soát cách tài liệu được render thành hình ảnh.  
`ColorMode` là một enumeration cho phép bạn chuyển đổi giữa đầu ra màu đầy đủ và đen‑trắng.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Bước 1: Tải tài liệu OneNote

`Document` đại diện cho một sổ tay OneNote và cung cấp các phương thức để tải, chỉnh sửa và lưu nội dung của nó. Đầu tiên, **tải tài liệu OneNote** vào Aspose.Note. Thay thế `"Your Document Directory"` bằng đường dẫn tới thư mục cục bộ của bạn và `"Aspose.one"` bằng tên tệp OneNote của bạn.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Bước 2: Đặt đường dẫn và tùy chọn đầu ra

`ImageSaveOptions` cấu hình cách một tài liệu OneNote được render thành tệp hình ảnh. Enumeration `ColorMode` chọn chế độ render màu, như đen‑trắng hoặc màu đầy đủ. Xác định đường dẫn đầu ra cho hình ảnh đen‑trắng và chỉ định các tùy chọn lưu. Chúng tôi sẽ đặt `ColorMode` thành `GrayScale` và sử dụng định dạng **lưu tài liệu dưới dạng PNG**. Bạn cũng có thể **điều chỉnh độ phân giải hình ảnh** lên 300 DPI cho các bản in chất lượng cao.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Bước 3: Lưu tài liệu

Cuối cùng, lưu tài liệu dưới dạng hình ảnh PNG đen‑trắng bằng các tùy chọn đã cấu hình. Phương thức `save` ghi tệp vào đĩa mà không cần bất kỳ tệp tạm thời trung gian nào.

```java
oneFile.save(dataDir, options);
```

## Các vấn đề thường gặp và giải pháp
- **FileNotFoundException** – Kiểm tra xem `dataDir` có trỏ tới thư mục đúng và tệp `.one` có tồn tại hay không.  
- **LicenseException** – Đảm bảo bạn đã áp dụng giấy phép Aspose.Note hợp lệ trước khi gọi `save`.  
- **Low‑resolution output** – Điều chỉnh `options.setResolution(300)` để tăng DPI; DPI cao hơn cho bản in sắc nét hơn nhưng kích thước tệp lớn hơn.  

## Câu hỏi thường gặp

**Q1: Tôi có thể lưu hình ảnh đen‑trắng ở định dạng khác không?**  
A1: Có, chỉ cần thay đổi tham số `SaveFormat` trong hàm khởi tạo `ImageSaveOptions` thành `Jpeg`, `Bmp`, hoặc bất kỳ định dạng hình ảnh nào trong hơn 20 định dạng được hỗ trợ.

**Q2: Aspose.Note có tương thích với mọi phiên bản tài liệu OneNote không?**  
A2: Aspose.Note hỗ trợ Microsoft OneNote 2010 và các phiên bản sau, bao phủ hơn 95 % sổ tay đang được sử dụng hiện nay.

**Q3: Aspose.Note có yêu cầu giấy phép để sử dụng không?**  
A3: Một giấy phép hợp lệ là bắt buộc cho việc sử dụng trong môi trường sản xuất, nhưng giấy phép dùng thử tạm thời có thể được lấy để đánh giá mà không mất phí.

**Q4: Tôi có thể thao tác các khía cạnh khác của tài liệu trước khi lưu dưới dạng hình ảnh không?**  
A4: Chắc chắn! Aspose.Note cung cấp các API để chỉnh sửa các phần, trang và các yếu tố riêng lẻ như văn bản, bảng và hình ảnh trước khi xuất.

**Q5: Tôi có thể tìm hỗ trợ ở đâu nếu gặp vấn đề?**  
A5: Bạn có thể tìm hỗ trợ trên diễn đàn Aspose.Note [tại đây](https://forum.aspose.com/c/note/28).

## Kết luận

Bạn đã học được **cách xuất onenote** bằng cách tải tệp OneNote, cấu hình các tùy chọn lưu để **tạo hình ảnh đen‑trắng**, và **lưu tài liệu dưới dạng PNG**. Cách tiếp cận này lý tưởng để tạo ra các hình ảnh nhẹ, sẵn sàng in từ sổ tay OneNote. Hãy thoải mái thử nghiệm các cài đặt `ColorMode` khác, giá trị DPI cao hơn, hoặc các định dạng hình ảnh thay thế để phù hợp với yêu cầu dự án của bạn.

---

**Cập nhật lần cuối:** 2026-06-30  
**Kiểm tra với:** Aspose.Note 27.0 for Java  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Xuất trang OneNote thành hình ảnh PNG trong Java bằng Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote đặt độ phân giải jpeg – Đặt độ phân giải hình ảnh đầu ra trong OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Cách lưu OneNote dưới dạng PDF với Aspose.Note cho Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}