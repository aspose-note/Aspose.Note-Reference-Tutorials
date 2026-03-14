---
date: 2026-03-14
description: Tìm hiểu cách lưu tài liệu OneNote dưới dạng tệp TIFF bằng việc sử dụng
  nén TIFF JPEG, nén TIFF PackBits hoặc CCITT Group 3 Fax trong Java. Kiểm soát chất
  lượng hình ảnh, kích thước tệp và chế độ màu với Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Lưu ảnh TIFF bằng nén JPEG TIFF trong OneNote
url: /vi/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu ảnh TIFF bằng nén TIFF JPEG trong OneNote

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách lưu tài liệu OneNote thành tệp TIFF bằng nén TIFF JPEG** và hai phương pháp nén phổ biến khác. Chúng tôi sẽ hướng dẫn qua các bước thiết lập cần thiết, nhập các gói Java cần thiết, và cung cấp mã rõ ràng từng bước cho mỗi tùy chọn nén. Khi hoàn thành, bạn sẽ có thể kiểm soát **TIFF image quality**, giảm kích thước tệp, và thậm chí tạo ra các TIFF đen‑trắng cho đầu ra kiểu fax.

## Câu trả lời nhanh
- **TIFF JPEG compression là gì?** Một phương pháp nén mất dữ liệu giảm kích thước tệp TIFF trong khi vẫn giữ chất lượng hình ảnh.  
- **Thư viện nào xử lý việc chuyển đổi?** Aspose.Note for Java.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; cần giấy phép cho môi trường sản xuất.  
- **Tôi có thể thay đổi chất lượng ảnh không?** Có, đặt thuộc tính `quality` trên `ImageSaveOptions`.  
- **Có thể chuyển đổi hàng loạt không?** Chắc chắn – lặp qua các tài liệu và áp dụng cùng các tùy chọn.

## TIFF JPEG Compression là gì?

Nén TIFF JPEG lưu trữ dữ liệu hình ảnh trong một container TIFF nhưng áp dụng thuật toán mất dữ liệu của JPEG để giảm kích thước tệp. Nó lý tưởng khi bạn cần cân bằng giữa **tiff image quality** và kích thước tệp nhỏ hơn, đặc biệt cho các kịch bản web hoặc lưu trữ.

## Tại sao nên sử dụng các loại nén TIFF khác nhau?
- **JPEG** – Thích hợp cho ảnh chụp; cung cấp khả năng điều chỉnh chất lượng.  
- **PackBits** – Mã hoá độ dài chạy đơn giản, không mất dữ liệu; hữu ích cho đồ họa có các vùng đồng màu lớn.  
- **CCITT Group 3 Fax** – Chỉ đen‑trắng; hoàn hảo cho tài liệu quét và truyền fax.  

Việc chọn loại nén phù hợp giúp bạn đáp ứng các giới hạn lưu trữ mà không làm giảm độ trung thực hình ảnh cần thiết cho ứng dụng của mình.

## Chuyển đổi One sang TIFF bằng Aspose.Note
Nếu mục tiêu của bạn là **chuyển đổi OneNote sang TIFF**, ba phương pháp dưới đây bao phủ các kịch bản phổ biến nhất. Mỗi phương pháp tải một tệp `.one`, cấu hình `ImageSaveOptions`, và lưu kết quả dưới dạng tệp `.tiff`.

## Yêu cầu trước

- Java Development Kit (JDK) đã được cài đặt.  
- Thư viện Aspose.Note for Java đã được thêm vào dự án của bạn (Maven/Gradle hoặc JAR thủ công).  
- Kiến thức cơ bản về cú pháp Java.

## Nhập các gói

Đầu tiên, nhập các lớp Aspose.Note cần thiết vào tệp Java của bạn:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Bước 1: Lưu dưới dạng TIFF bằng nén TIFF JPEG

Dưới đây là phương thức hoàn chỉnh tải tệp OneNote và lưu nó dưới dạng TIFF với nén JPEG. Điều chỉnh giá trị `quality` (0‑100) để kiểm soát **tiff image quality**.

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

- `ImageSaveOptions` cho Aspose.Note biết sẽ xuất ra tệp TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` chọn nén JPEG.  
- `setQuality(93)` (tùy chọn) tinh chỉnh chất lượng ảnh; giá trị thấp hơn tạo ra tệp nhỏ hơn.

### Cách lưu TIFF với nén JPEG trong Java
1. Đặt `dataDir` tới thư mục chứa tệp `.one` của bạn.  
2. Gọi `SaveToTiffUsingJpegCompression()` từ phương thức `main` hoặc dịch vụ của bạn.  
3. Tệp `.tiff` kết quả sẽ xuất hiện trong cùng thư mục.

## Tổng quan về nén TIFF PackBits

PackBits là thuật toán nén không mất dữ liệu hoạt động tốt nhất cho các hình ảnh có các khu vực màu đồng nhất lớn. Nó thường được gọi là **tiff packbits compression** trong tài liệu.

## Bước 2: Lưu dưới dạng TIFF bằng nén PackBits

Nếu bạn cần một tùy chọn không mất dữ liệu, PackBits là thuật toán độ dài chạy đơn giản hoạt động tốt cho đồ họa có màu đồng nhất.

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

## Bước 3: Lưu dưới dạng TIFF bằng nén CCITT Group 3 Fax (TIFF đen‑trắng)

Đối với tài liệu kiểu fax, bạn thường muốn một **black and white TIFF**. CCITT Group 3 cung cấp mức nén cao cho hình ảnh đơn sắc.

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

## Các vấn đề thường gặp & Mẹo

| Vấn đề | Giải pháp |
|-------|----------|
| **Tệp đầu ra lớn hơn mong đợi** | Thử giảm giá trị `quality` của JPEG hoặc chuyển sang PackBits nếu chấp nhận được nén không mất dữ liệu. |
| **Màu sắc bị nhạt** | Đảm bảo bạn không vô tình đặt `ColorMode.BlackAndWhite` khi cần màu đầy đủ. |
| **Lỗi định dạng ảnh không được hỗ trợ** | Kiểm tra bạn đang sử dụng phiên bản mới nhất của Aspose.Note; các bản cũ có thể thiếu một số enum nén. |
| **LicenseException khi chạy** | Cài đặt giấy phép Aspose.Note hợp lệ (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Câu hỏi thường gặp

**Q: Tôi có thể chuyển đổi các loại tài liệu khác (ví dụ, PDF, DOCX) sang TIFF với các tùy chọn này không?**  
A: Có. Mặc dù Aspose.Note tập trung vào tệp OneNote, Aspose.PDF, Aspose.Words và các thư viện khác cung cấp `ImageSaveOptions` tương tự cho các định dạng của chúng.

**Q: Nén TIFF JPEG khác gì so với tệp JPEG tiêu chuẩn?**  
A: Thuật toán JPEG là giống nhau, nhưng dữ liệu hình ảnh nằm trong một container TIFF, có thể chứa nhiều trang và siêu dữ liệu phong phú hơn.

**Q: Có thể xử lý hàng loạt nhiều tệp `.one` không?**  
A: Chắc chắn. Duyệt qua một thư mục, gọi bất kỳ phương pháp nào trong ba phương pháp cho mỗi tệp, và thu thập các TIFF kết quả.

**Q: Tôi có thể kiểm soát DPI/độ phân giải của TIFF đầu ra không?**  
A: Có. Sử dụng `options.setResolution(int dpi)` trước khi lưu.

**Q: Aspose.Note có hỗ trợ xử lý bất đồng bộ không?**  
A: API tự nó là đồng bộ, nhưng bạn có thể bọc các cuộc gọi trong `CompletableFuture` của Java hoặc một pool luồng để thực thi song song.

## Kết luận

Bây giờ bạn đã có một bộ công cụ **java tiff conversion** hoàn chỉnh cho phép lưu tài liệu OneNote dưới dạng tệp TIFF bằng nén JPEG, PackBits hoặc CCITT Group 3 Fax. Điều chỉnh chất lượng, chế độ màu và độ phân giải để đáp ứng yêu cầu **tiff image quality** cụ thể của bạn, và tích hợp các phương pháp này vào quy trình làm việc hàng loạt để đạt năng suất tối đa.

---

**Cập nhật lần cuối:** 2026-03-14  
**Kiểm tra với:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}