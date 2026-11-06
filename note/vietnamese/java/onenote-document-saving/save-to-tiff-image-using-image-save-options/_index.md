---
date: 2026-11-05
description: Tìm hiểu cách giảm kích thước tệp TIFF khi chuyển đổi sổ tay OneNote
  sang TIFF trong Java bằng Aspose.Note. Bao gồm các tùy chọn JPEG, PackBits và TIFF
  đen‑trắng.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Cách giảm kích thước tệp TIFF khi chuyển đổi OneNote trong Java
og_description: Tìm hiểu cách giảm kích thước tệp TIFF khi chuyển đổi sổ tay OneNote
  sang TIFF trong Java bằng Aspose.Note. Bao gồm các tùy chọn JPEG, PackBits và TIFF
  đen‑trắng.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Cách giảm kích thước tệp TIFF khi chuyển đổi OneNote trong Java
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Cách giảm kích thước tệp TIFF khi chuyển đổi OneNote trong Java
url: /vi/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách giảm kích thước tệp TIFF khi chuyển đổi OneNote trong Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá cách **giảm kích thước tệp TIFF** khi chuyển đổi sổ tay OneNote sang ảnh TIFF bằng Aspose.Note cho Java. Chúng tôi sẽ trình bày ba phương pháp nén—TIFF JPEG, PackBits và CCITT Group 3 (TIFF đen‑trắng)—cho bạn cách điều chỉnh chất lượng hình ảnh, kiểm soát chế độ màu và giữ kích thước tệp tối ưu cho web, lưu trữ hoặc các kịch bản kiểu fax.

## Câu trả lời nhanh
- **Nén TIFF JPEG là gì?** Phương pháp nén mất dữ liệu giúp giảm kích thước tệp TIFF trong khi vẫn giữ chất lượng hình ảnh.  
- **Thư viện nào thực hiện việc chuyển đổi?** Aspose.Note for Java.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; cần giấy phép cho môi trường sản xuất.  
- **Tôi có thể thay đổi chất lượng hình ảnh không?** Có, đặt thuộc tính `quality` trên `ImageSaveOptions`.  
- **Có thể thực hiện chuyển đổi hàng loạt không?** Chắc chắn – lặp qua các tài liệu và áp dụng cùng các tùy chọn.  

## Tổng quan nén TIFF JPEG

Nén TIFF JPEG lưu trữ dữ liệu hình ảnh trong một container TIFF nhưng áp dụng thuật toán JPEG mất dữ liệu để giảm kích thước tệp. Nó lý tưởng khi bạn cần cân bằng giữa **chất lượng ảnh TIFF** và kích thước tệp nhỏ hơn, đặc biệt cho các kịch bản web hoặc lưu trữ.

## Tại sao nên sử dụng các loại nén TIFF khác nhau?

Bạn chọn loại nén dựa trên nội dung và nhu cầu lưu trữ: JPEG phù hợp nhất cho ảnh chụp, PackBits cung cấp nén không mất dữ liệu cho đồ họa có các vùng đồng nhất lớn, và CCITT Group 3 mang lại nén tỷ lệ cao cho tài liệu fax đơn sắc. Việc chọn phương pháp phù hợp cho phép bạn **giảm kích thước tệp TIFF** mà không làm giảm độ trung thực hình ảnh cần thiết cho ứng dụng của bạn.

## Lựa chọn nén phù hợp

- **JPEG** – Chất lượng có thể điều chỉnh (0‑100) cho phép bạn cân bằng kích thước và chi tiết, hoàn hảo cho các trang màu phong phú.  
- **PackBits** – Mã hoá run‑length không mất dữ liệu; lý tưởng khi bạn phải giữ nguyên mọi pixel.  
- **CCITT Group 3** – Chỉ dành cho đơn sắc; tối đa hoá nén cho văn bản quét hoặc tài liệu fax.  

## Chuyển đổi OneNote sang TIFF bằng Aspose.Note

Nếu mục tiêu của bạn là **chuyển đổi OneNote sang TIFF**, ba phương pháp dưới đây bao phủ các kịch bản phổ biến nhất. Mỗi phương pháp tải một tệp `.one`, cấu hình `ImageSaveOptions`, và lưu kết quả dưới dạng tệp `.tiff`.

## Yêu cầu trước

- Java Development Kit (JDK) đã được cài đặt.  
- Thư viện Aspose.Note cho Java đã được thêm vào dự án của bạn (Maven/Gradle hoặc JAR thủ công).  
- Kiến thức cơ bản về cú pháp Java.  

## Nhập các gói

Các lớp `ImageSaveOptions`, `TiffCompression` và `ColorMode` là lõi của API chuyển đổi.  

`ImageSaveOptions` định nghĩa các tùy chọn khi lưu ảnh, như định dạng và nén.  
`TiffCompression` liệt kê các thuật toán nén TIFF được hỗ trợ.  
`ColorMode` chỉ định độ sâu màu, ví dụ: màu hoặc đen‑trắng.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Bước 1: lưu dưới dạng TIFF bằng nén TIFF JPEG

### Lưu TIFF với nén JPEG trong Java

Tải tệp OneNote, cấu hình `ImageSaveOptions` với nén JPEG, tùy chọn đặt giá trị `quality`, và gọi phương thức lưu. Mẫu hai bước này cho phép bạn kiểm soát hoàn toàn kích thước đầu ra và độ trung thực hình ảnh.

1. Đặt `dataDir` tới thư mục chứa tệp `.one` của bạn.  
2. Gọi `SaveToTiffUsingJpegCompression()` từ phương thức `main` hoặc dịch vụ của bạn.  
3. Tệp `.tiff` kết quả sẽ xuất hiện trong cùng thư mục.  

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Giải thích**

- `ImageSaveOptions` cho Aspose.Note biết xuất ra tệp TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` chọn nén JPEG.  
- `setQuality(93)` (tùy chọn) tinh chỉnh chất lượng ảnh; giá trị thấp hơn tạo ra tệp nhỏ hơn.  

## Tổng quan nén TIFF PackBits

PackBits là một thuật toán nén không mất dữ liệu, hoạt động tốt nhất cho các ảnh có các vùng màu đồng nhất lớn. Nó thường được gọi là **nén tiff packbits** trong tài liệu.

## Lưu TIFF với nén PackBits trong Java

Nếu bạn cần một tùy chọn không mất dữ liệu, PackBits là một thuật toán run‑length đơn giản, hoạt động tốt cho đồ họa có màu đồng nhất. Cấu hình `ImageSaveOptions` với `TiffCompression.PackBits` và lưu tài liệu.

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Giải thích**

- `setTiffCompression(TiffCompression.PackBits)` chuyển đổi phương pháp nén.  
- Không cần thiết lập chất lượng vì PackBits là không mất dữ liệu.  

## Lưu TIFF với nén CCITT Group 3 trong Java

Đối với tài liệu kiểu fax, bạn thường muốn một **TIFF đen và trắng**. CCITT Group 3 cung cấp nén cao cho ảnh đơn sắc. Đặt chế độ màu thành đen‑trắng và chọn enum nén CCITT 3.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Giải thích**

- `setColorMode(ColorMode.BlackAndWhite)` buộc đầu ra thành đơn sắc.  
- `setTiffCompression(TiffCompression.Ccitt3)` áp dụng nén hướng fax.  

## Các vấn đề thường gặp & mẹo

| Vấn đề | Giải pháp |
|-------|----------|
| **Tệp đầu ra lớn hơn mong đợi** | Thử giảm giá trị `quality` của JPEG hoặc chuyển sang PackBits nếu chấp nhận nén không mất dữ liệu. |
| **Màu sắc bị nhạt** | Đảm bảo bạn không vô tình đặt `ColorMode.BlackAndWhite` khi cần màu đầy đủ. |
| **Lỗi định dạng ảnh không được hỗ trợ** | Kiểm tra bạn đang sử dụng phiên bản mới nhất của Aspose.Note; các bản cũ có thể thiếu một số enum nén. |
| **LicenseException khi chạy** | Cài đặt giấy phép Aspose.Note hợp lệ (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Câu hỏi thường gặp

**Q: Tôi có thể chuyển đổi các loại tài liệu khác (ví dụ: PDF, DOCX) sang TIFF với các tùy chọn này không?**  
A: Có. Mặc dù Aspose.Note tập trung vào tệp OneNote, Aspose.PDF, Aspose.Words và các thư viện khác cung cấp `ImageSaveOptions` tương tự cho các định dạng của chúng.  

**Q: Nén TIFF JPEG khác gì so với tệp JPEG tiêu chuẩn?**  
A: Thuật toán JPEG là giống nhau, nhưng dữ liệu ảnh được lưu trong một container TIFF, có thể chứa nhiều trang và siêu dữ liệu phong phú hơn.  

**Q: Có thể xử lý hàng loạt nhiều tệp `.one` không?**  
A: Chắc chắn. Lặp qua một thư mục, gọi bất kỳ một trong ba phương pháp cho mỗi tệp, và thu thập các tệp TIFF kết quả.  

**Q: Tôi có thể kiểm soát DPI/độ phân giải của TIFF đầu ra không?**  
A: Có. Sử dụng `options.setResolution(int dpi)` trước khi lưu.  

**Q: Aspose.Note có hỗ trợ xử lý bất đồng bộ không?**  
A: API này đồng bộ, nhưng bạn có thể bọc các lời gọi trong `CompletableFuture` của Java hoặc một pool luồng để thực thi song song.  

## Kết luận

Bây giờ bạn đã có một bộ công cụ **chuyển đổi TIFF trong Java** hoàn chỉnh cho phép bạn **giảm kích thước tệp TIFF** khi lưu tài liệu OneNote dưới dạng tệp TIFF bằng nén JPEG, PackBits hoặc CCITT Group 3 Fax. Điều chỉnh chất lượng, chế độ màu và độ phân giải để đáp ứng yêu cầu cụ thể, và tích hợp các phương pháp này vào quy trình làm việc hàng loạt để đạt năng suất tối đa.

---

**Cập nhật lần cuối:** 2026-11-05  
**Kiểm tra với:** Aspose.Note for Java 26.4 (latest at time of writing)  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Cách hiển thị hình ảnh trang OneNote (JPEG) bằng Save Format với Aspose.Note cho Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Sử dụng Aspose.Note cho Java để lưu OneNote dưới dạng PNG với các tùy chọn – Chuyển đổi sổ tay thành hình ảnh](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [Cách xuất OneNote dưới dạng ảnh xám – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}