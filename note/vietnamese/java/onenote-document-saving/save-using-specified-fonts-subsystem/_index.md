---
date: 2025-12-18
description: Tìm hiểu cách **lưu OneNote dưới dạng PDF** bằng cách sử dụng hệ thống
  phông chữ được chỉ định trong Java với Aspose.Note. Hướng dẫn này cũng chỉ ra cách
  chuyển đổi OneNote sang PDF, tải các tệp phông chữ tùy chỉnh và chỉ định phông chữ
  mặc định.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Lưu OneNote dưới dạng PDF bằng Hệ thống Phông chữ Được chỉ định
url: /vi/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu OneNote dưới dạng PDF bằng Hệ thống Phông chữ Được chỉ định

## Giới thiệu

Trong nhiều tình huống kinh doanh, bạn cần **lưu OneNote dưới dạng PDF** đồng thời giữ nguyên giao diện của các trang gốc. Aspose.Note for Java giúp thực hiện việc này một cách đơn giản bằng cách cho phép bạn kiểm soát hệ thống phông chữ trong quá trình chuyển đổi. Trong hướng dẫn này, chúng ta sẽ đi qua ba cách thực tế để **chuyển đổi OneNote sang PDF**, bao gồm **tải tệp phông chữ tùy chỉnh**, **chỉ định phông chữ mặc định**, và thậm chí **sử dụng luồng phông chữ** khi phông chữ không có trên máy đích.

## Trả lời nhanh
- **“Lưu OneNote dưới dạng PDF” có nghĩa là gì?** Nó chuyển đổi tệp .one thành PDF trong khi giữ nguyên bố cục và kiểu dáng.  
- **API nào quản lý phông chữ?** `DocumentFontsSubsystem` cho phép bạn định nghĩa phông chữ mặc định hoặc tải tệp/luồng phông chữ tùy chỉnh.  
- **Có cần giấy phép cho môi trường sản xuất không?** Có, cần giấy phép thương mại của Aspose.Note cho việc sử dụng không phải bản dùng thử.  
- **Có thể chuyển đổi nhiều tệp cùng lúc không?** Chắc chắn – chỉ cần lặp lại logic tải và lưu `Document`.  
- **Yêu cầu phiên bản Java nào?** Java 15 trở lên (ví dụ sử dụng JDK 15).

## “Lưu OneNote dưới dạng PDF” với hệ thống phông chữ là gì?

Lưu OneNote dưới dạng PDF với hệ thống phông chữ có nghĩa là trong quá trình chuyển đổi, Aspose.Note sẽ thay thế bất kỳ glyph nào còn thiếu bằng phông chữ bạn cung cấp. Điều này đảm bảo PDF trông giống hệt trên mọi thiết bị, ngay cả khi phông chữ gốc không được cài đặt.

## Tại sao cần kiểm soát hệ thống phông chữ khi **chuyển đổi OneNote sang PDF**?

- **Nhận diện thương hiệu nhất quán** – tài liệu công ty giữ nguyên kiểu chữ.  
- **Độ tin cậy đa nền tảng** – PDF hiển thị giống nhau trên Windows, macOS, Linux và thiết bị di động.  
- **Giảm lỗi** – các cảnh báo thiếu phông chữ biến mất, tạo ra đầu ra sạch sẽ.

## Yêu cầu trước

### 1. Java Development Kit (JDK)

Đảm bảo bạn cài đặt Java Development Kit (JDK) trên hệ thống. Bạn có thể tải về từ [tại đây](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) nếu chưa có.

### 2. Thư viện Aspose.Note for Java

Tải và thiết lập thư viện Aspose.Note for Java. Bạn có thể tải về từ [trang web](https://releases.aspose.com/note/java/).

## Nhập gói

Đảm bảo nhập các gói cần thiết trong dự án Java của bạn:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Bây giờ hãy phân tích từng ví dụ thành nhiều bước để hiểu quy trình tốt hơn.

## Cách **lưu OneNote dưới dạng PDF** bằng Document Fonts Subsystem với phông chữ mặc định

### Bước 1: Lưu bằng Document Fonts Subsystem với tên phông chữ mặc định

Bước này minh họa cách **lưu OneNote dưới dạng PDF** một cách đơn giản bằng cách chỉ định tên phông chữ mặc định.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Trong bước này:
- Tài liệu OneNote được tải bằng Aspose.Note.
- **Phông chữ mặc định** được chỉ định là **"Times New Roman"**.
- Tài liệu được lưu dưới dạng PDF với phông chữ đã chọn.

### Bước 2: Lưu bằng Document Fonts Subsystem với phông chữ mặc định từ tệp

Ở đây chúng ta **tải một tệp phông chữ tùy chỉnh** và sử dụng nó làm dự phòng khi chuyển đổi sang PDF.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Các điểm chính:
- **Tệp phông chữ tùy chỉnh** `geo_1.ttf` được **tải từ đĩa**.
- `usingDefaultFontFromFile` **chỉ định phông chữ mặc định từ tệp**, đảm bảo PDF sử dụng phông chữ này khi phông chữ gốc thiếu.
- PDF kết quả giữ nguyên giao diện mong muốn.

### Bước 3: Lưu bằng Document Fonts Subsystem với phông chữ mặc định từ luồng

Đôi khi phông chữ có thể được lưu trong cơ sở dữ liệu hoặc nhận qua mạng. Ví dụ này cho thấy cách **sử dụng luồng phông chữ**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Điều xảy ra ở đây:
- Tệp phông chữ được mở dưới dạng **InputStream**, hữu ích khi phông chữ nằm ở nguồn không phải tệp.
- `usingDefaultFontFromStream` **sử dụng luồng phông chữ** để định nghĩa phông chữ dự phòng.
- Tệp OneNote được lưu dưới dạng PDF với phông chữ dựa trên luồng.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **Cảnh báo thiếu phông chữ** | Tệp .one tham chiếu tới phông chữ không có trên máy. | Cung cấp phông chữ mặc định qua `usingDefaultFont`, `usingDefaultFontFromFile`, hoặc `usingDefaultFontFromStream`. |
| **Không tìm thấy tệp phông chữ tùy chỉnh** | Đường dẫn tới tệp `.ttf` không đúng. | Sử dụng đường dẫn tuyệt đối hoặc kiểm tra đường dẫn tương đối từ thư mục làm việc. |
| **Luồng không được đóng** | Ngoại lệ xảy ra trước khi gọi `close()`. | Sử dụng try‑with‑resources (`try (InputStream stream = ...) { ... }`) để tự động đóng. |

## Câu hỏi thường gặp

**H: Tôi có thể chỉ định các phông chữ khác nhau cho các phần khác nhau của tài liệu không?**  
Đ: Có, bạn có thể áp dụng cài đặt phông chữ tùy chỉnh cho các phần văn bản riêng lẻ bằng lớp `Font` trong Aspose.Note.

**H: Aspose.Note có tương thích với mọi phiên bản OneNote không?**  
Đ: Aspose.Note hỗ trợ các tệp OneNote từ các phiên bản desktop và mobile gần đây, đảm bảo tính tương thích rộng.

**H: Làm sao xử lý phông chữ thiếu khi lưu tài liệu?**  
Đ: Sử dụng các phương pháp trong hệ thống phông chữ đã nêu ở trên (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) để cung cấp phông chữ dự phòng.

**H: Tôi có thể tùy chỉnh các thuộc tính phông chữ như kích thước và kiểu không?**  
Đ: Chắc chắn – API cho phép bạn đặt kích thước, kiểu, màu và các thuộc tính khác cho từng đoạn văn bản.

**H: Có phiên bản dùng thử của Aspose.Note for Java không?**  
Đ: Có, bạn có thể tải bản dùng thử miễn phí từ trang web Aspose.

## Kết luận

Trong hướng dẫn này, chúng ta đã học cách **lưu OneNote dưới dạng PDF** đồng thời kiểm soát hệ thống phông chữ trong Java bằng Aspose.Note. Bằng cách thực hiện ba cách tiếp cận—chỉ định tên phông chữ mặc định, tải tệp phông chữ tùy chỉnh, hoặc sử dụng luồng phông chữ—bạn có thể đảm bảo việc hiển thị phông chữ nhất quán trên mọi nền t khi xuất hoặc lưu tài liệu OneNote của mình.

---

**Cập nhật lần cuối:** 2025-12-18  
**Đã kiểm tra với:** Aspose.Note for Java 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}