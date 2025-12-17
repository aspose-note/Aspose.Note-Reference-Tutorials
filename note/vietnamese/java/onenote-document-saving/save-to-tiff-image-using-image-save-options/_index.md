---
date: 2025-12-17
description: Tìm hiểu cách lưu tài liệu OneNote dưới dạng tệp TIFF bằng nén TIFF JPEG,
  PackBits hoặc CCITT Group 3 Fax trong Java. Kiểm soát chất lượng hình ảnh, kích
  thước tệp và chế độ màu với Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Lưu ảnh TIFF bằng nén JPEG TIFF trong OneNote
url: /vi/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu hình ảnh TIFF bằng nén TIFF JPEG trong OneNote

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách lưu tài liệu OneNote thành tệp TIFF bằng nén TIFF JPEG** và hai phương pháp nén phổ biến khác. Chúng tôi sẽ hướng dẫn qua các bước thiết lập cần thiết, nhập các gói Java cần thiết, và cung cấp mã chi tiết từng bước cho mỗi tùy chọn nén. Khi hoàn thành, bạn sẽ có thể kiểm soát **chất lượng ảnh TIFF**, giảm kích thước tệp, và thậm chí tạo ra các tệp TIFF đen‑trắng cho đầu ra kiểu fax.

## Câu trả lời nhanh
- **What is TIFF JPEG compression?** Phương pháp nén mất dữ liệu giúp giảm kích thước tệp TIFF trong khi vẫn giữ được chất lượng hình ảnh.  
- **Which library handles the conversion?** Aspose.Note for Java.  
- **Do I need a license?** Bản dùng thử miễn phí hoạt động cho việc thử nghiệm; cần có giấy phép cho môi trường sản xuất.  
- **Can I change the image quality?** Có, đặt thuộc tính `quality` trên `ImageSaveOptions`.  
- **Is batch conversion possible?** Chắc chắn – lặp qua các tài liệu và áp dụng cùng một tùy chọn.

## TIFF JPEG Compression là gì?
Nén TIFF JPEG lưu trữ dữ liệu hình ảnh trong container TIFF nhưng áp dụng thuật toán JPEG mất dữ liệu để thu nhỏ tệp. Đây là lựa chọn lý tưởng khi bạn cần cân bằng giữa **chất lượng ảnh TIFF** và kích thước tệp nhỏ hơn, đặc biệt cho các kịch bản web hoặc lưu trữ.

## Tại sao nên sử dụng các loại nén TIFF khác nhau?
- **JPEG** – Thích hợp cho ảnh chụp; cung cấp khả năng điều chỉnh chất lượng.  
- **PackBits** – Thuật toán run‑length đơn giản, không mất dữ liệu; hữu ích cho đồ họa có vùng màu đồng nhất lớn.  
- **CCITT Group 3 Fax** – Chỉ hỗ trợ đen‑trắng; hoàn hảo cho tài liệu quét và truyền fax.  

Việc chọn đúng loại nén giúp bạn đáp ứng các hạn chế về lưu trữ mà không làm giảm độ trung thực hình ảnh cần thiết cho ứng dụng của mình.

## Yêu cầu trước

- Cài đặt Java Development Kit (JDK).  
- Thêm thư viện Aspose.Note for Java vào dự án (Maven/Gradle hoặc JAR thủ công).  
- Có kiến thức cơ bản về cú pháp Java.

## Nhập gói

Đầu tiên, đưa các lớp Aspose.Note cần thiết vào file Java của bạn:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Bước 1: Lưu dưới dạng TIFF bằng nén TIFF JPEG

Dưới đây là phương thức hoàn chỉnh tải tệp OneNote và lưu nó dưới dạng TIFF với nén JPEG. Điều chỉnh giá trị `quality` (0‑100) để kiểm soát **chất lượng ảnh TIFF**.

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

- `ImageSaveOptions` chỉ định cho Aspose.Note xuất ra tệp TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` chọn nén JPEG.  
- `setQuality(93)` (tùy chọn) tinh chỉnh chất lượng ảnh; giá trị thấp hơn tạo tệp nhỏ hơn.

### Cách lưu TIFF với nén JPEG trong Java
1. Đặt `dataDir` trỏ tới thư mục chứa tệp `.one` của bạn.  
2. Gọi `SaveToTiffUsingJpegCompression()` từ phương thức `main` hoặc dịch vụ của bạn.  
3. Tệp `.tiff` kết quả sẽ xuất hiện trong cùng thư mục.

## Bước 2: Lưu dưới dạng TIFF bằng nén PackBits

Nếu bạn cần một tùy chọn không mất dữ liệu, PackBits là thuật toán run‑length đơn giản hoạt động tốt cho đồ họa có màu đồng nhất.

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

- `setTiffCompression(TiffCompression.PackBits)` chuyển sang phương pháp nén này.  
- Không cần thiết lập chất lượng vì PackBits không mất dữ liệu.

## Bước 3: Lưu dưới dạng TIFF bằng nén CCITT Group 3 Fax (TIFF đen‑trắng)

Đối với tài liệu kiểu fax, bạn thường muốn một **TIFF đen‑trắng**. CCITT Group 3 cung cấp mức nén cao cho ảnh đơn sắc.

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

- `setColorMode(ColorMode.BlackAndWhite)` buộc đầu ra ở chế độ đơn sắc.  
- `setTiffCompression(TiffCompression.Ccitt3)` áp dụng nén hướng fax.

## Các vấn đề thường gặp & Mẹo

| Issue | Solution |
|-------|----------|
| **Output file is larger than expected** | Thử giảm giá trị `quality` của JPEG hoặc chuyển sang PackBits nếu chấp nhận được nén không mất dữ liệu. |
| **Colors appear washed out** | Đảm bảo bạn không vô tình đặt `ColorMode.BlackAndWhite` khi cần màu đầy đủ. |
| **Unsupported image format error** | Kiểm tra bạn đang dùng phiên bản mới nhất của Aspose.Note; các bản cũ có thể thiếu một số enum nén. |
| **LicenseException at runtime** | Cài đặt giấy phép Aspose.Note hợp lệ (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Câu hỏi thường gặp

**Q: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these options?**  
A: Có. Aspose.Note tập trung vào tệp OneNote, nhưng các thư viện khác của Aspose (PDF, Words) cung cấp `ImageSaveOptions` tương tự cho các định dạng tương ứng.

**Q: How does TIFF JPEG compression differ from standard JPEG files?**  
A: Dữ liệu ảnh được lưu trong container TIFF, giữ nguyên metadata và cho phép nhiều trang, trong khi thuật toán nén vẫn là JPEG.

**Q: Is it possible to batch‑process many `.one` files?**  
A: Chắc chắn. Lặp qua một thư mục, gọi bất kỳ phương pháp nào trong ba phương pháp trên cho mỗi tệp, và thu thập các TIFF kết quả.

**Q: Can I control the DPI/resolution of the output TIFF?**  
A: Có. Sử dụng `options.setResolution(int dpi)` trước khi lưu.

**Q: Does Aspose.Note support asynchronous processing?**  
A: API của nó đồng bộ, nhưng bạn có thể bọc các lời gọi trong `CompletableFuture` của Java hoặc các pool thread để thực thi song song.

## Kết luận

Bạn đã có một bộ công cụ **java tiff conversion** hoàn chỉnh, cho phép lưu tài liệu OneNote dưới dạng TIFF bằng nén JPEG, PackBits, hoặc CCITT Group 3 Fax. Điều chỉnh chất lượng, chế độ màu và độ phân giải để đáp ứng yêu cầu **chất lượng ảnh TIFF** của bạn, và tích hợp các phương pháp này vào quy trình batch để đạt năng suất tối đa.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note for Java 23.12 (phiên bản mới nhất tại thời điểm viết)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}