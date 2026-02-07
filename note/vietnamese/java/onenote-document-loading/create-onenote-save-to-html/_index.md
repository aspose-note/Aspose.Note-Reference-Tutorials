---
date: 2026-02-07
description: Tìm hiểu cách xuất phông chữ khi lưu OneNote dưới dạng HTML bằng Aspose.Note
  cho Java. Hướng dẫn này chỉ cho bạn cách tạo OneNote một cách lập trình và nhúng
  phông chữ, CSS và hình ảnh.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Cách xuất phông chữ khi lưu OneNote dưới dạng HTML – Java
url: /vi/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách xuất phông chữ khi lưu OneNote dưới dạng HTML – Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách xuất phông chữ** khi **lưu OneNote dưới dạng HTML** bằng Aspose.Note for Java. Chúng tôi sẽ hướng dẫn tạo tài liệu OneNote bằng chương trình, cấu hình các tùy chọn lưu HTML, và nhúng các tệp phông chữ cần thiết để HTML kết quả trông giống hệt các trang OneNote gốc. Cách tiếp cận này hoàn hảo khi bạn cần giữ nguyên độ chính xác hình ảnh của nội dung OneNote trong định dạng thân thiện với web.

## Câu trả lời nhanh
- **Thư viện nào xử lý việc xuất?** Aspose.Note for Java  
- **Có thể nhúng phông chữ vào HTML không?** Có – đặt `ExportFonts` thành `ExportEmbedded`  
- **Có cần giấy phép cho môi trường sản xuất không?** Cần giấy phép Aspose.Note hợp lệ cho việc sử dụng thương mại  
- **Phiên bản Java nào được hỗ trợ?** Java 8 hoặc cao hơn  
- **Có thể lưu tài nguyên thành các tệp riêng không?** Chắc chắn – cấu hình `ResourceExportType` tương ứng  

## “Cách xuất phông chữ” là gì trong ngữ cảnh chuyển đổi OneNote sang HTML?

Khi bạn chuyển đổi một sổ tay OneNote sang HTML, diện mạo trực quan phụ thuộc vào CSS, hình ảnh và đặc biệt là các phông chữ được sử dụng trong các trang gốc. **Xuất phông chữ** có nghĩa là nhúng các tệp phông chữ (ví dụ: TTF) trực tiếp vào gói HTML để trình duyệt có thể hiển thị văn bản chính xác như trong OneNote, ngay cả khi người dùng cuối không cài đặt các phông chữ đó trên máy tính.

## Tại sao tạo OneNote bằng chương trình và lưu dưới dạng HTML?

- **Tự động hóa:** Tạo báo cáo, tài liệu, hoặc bài viết kiến thức từ OneNote mà không cần sao chép‑dán thủ công.  
- **Nhất quán:** Bảo toàn bố cục, kiểu dáng và phông chữ tùy chỉnh trên mọi thiết bị.  
- **Di động:** HTML có thể xem trên mọi nền tảng—không cần client OneNote.  

## Yêu cầu trước

1. Java Development Kit (JDK) 8 hoặc mới hơn đã được cài đặt.  
2. Thư viện Aspose.Note for Java – tải về từ [here](https://releases.aspose.com/note/java/).  
3. Một tệp OneNote mẫu (`.one`) để tải, hoặc bạn có thể tạo tệp mới bằng chương trình.  

## Nhập các gói

Đầu tiên, nhập các lớp cần thiết vào dự án Java của bạn:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Cách xuất phông chữ khi lưu OneNote dưới dạng HTML?

Dưới đây là hướng dẫn chi tiết từng bước cho bạn **cách xuất phông chữ** và các tài nguyên khác.

### Bước 1: Tạo tài liệu OneNote bằng chương trình  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Dòng này tải một tệp `.one` hiện có. Nếu bạn cần **tạo OneNote bằng chương trình**, bạn có thể khởi tạo một đối tượng `Document` mới và thêm các phần/đánh dấu qua API (không hiển thị ở đây để tập trung vào việc xuất phông chữ).

### Bước 2: Lưu vào luồng bộ nhớ với phông chữ được nhúng  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` yêu cầu Aspose.Note **xuất phông chữ** trực tiếp vào gói HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` đảm bảo sử dụng phông chữ TrueType, có hỗ trợ rộng rãi trên trình duyệt.

### Bước 3: Lưu dưới dạng HTML với các tệp tài nguyên riêng (vẫn xuất phông chữ)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Mặc dù CSS và hình ảnh đã được nhúng, bạn vẫn có thể thay đổi `ResourceExportType` thành `ExportExternal` nếu muốn các tệp riêng để dễ dàng cache. Phần quan trọng—**xuất phông chữ**—vẫn không thay đổi.

### Bước 4: Sử dụng callbacks để kiểm soát nơi lưu trữ mỗi tài nguyên  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Lớp `UserSavingCallbacks` (bạn cần triển khai `ICssSavingCallback`, `IImageSavingCallback`, và `IFontSavingCallback`) cho phép bạn kiểm soát toàn bộ cấu trúc thư mục, giúp lưu phông chữ trong thư mục `fonts` riêng biệt đồng thời **xuất phông chữ** một cách chính xác.

## Cách nhúng phông chữ tùy chỉnh khi chuyển đổi OneNote sang HTML

Nhúng phông chữ tùy chỉnh đảm bảo việc hiển thị HTML khớp với bố cục OneNote gốc, ngay cả trên các thiết bị không có sẵn các phông chữ đó. Khi sử dụng `ExportEmbedded` cùng với `FontFaceType.Ttf`, các tệp TrueType sẽ được mã hoá base‑64 và chèn trực tiếp vào CSS được tạo, loại bỏ nhu cầu lưu trữ phông chữ bên ngoài.

## Sử dụng ResourceExportType để kiểm soát việc xuất tài nguyên

`ResourceExportType` cho phép bạn quyết định liệu CSS, hình ảnh và phông chữ sẽ được lưu **bên trong** tệp HTML (`ExportEmbedded`) hay dưới dạng **tệp bên ngoài** (`ExportExternal`). Chọn `ExportEmbedded` cho giải pháp một tệp duy nhất, hoặc `ExportExternal` khi bạn muốn tận dụng cache của trình duyệt cho các tài nguyên lớn.

## Tạo OneNote bằng chương trình để xuất HTML

Nếu bạn bắt đầu từ đầu, có thể xây dựng một tài liệu OneNote hoàn toàn bằng mã, thêm các phần, trang và văn bản phong phú, sau đó áp dụng cùng `HtmlSaveOptions` như trên. Điều này cho phép tự động hoá toàn bộ quy trình: từ tạo dữ liệu đến xuất HTML có phong cách đầy đủ và nhúng phông chữ tùy chỉnh.

## Các vấn đề thường gặp & Mẹo

- **Phông chữ bị thiếu trong kết quả:** Kiểm tra rằng `setExportFonts(ResourceExportType.ExportEmbedded)` đã được đặt và tệp OneNote nguồn thực sự sử dụng phông chữ được nhúng.  
- **HTML lớn:** Nhúng phông chữ có thể làm tăng kích thước. Nếu lo ngại về băng thông, chuyển `ExportFonts` sang `ExportExternal` và lưu trữ phông chữ trên CDN.  
- **Lỗi triển khai callback:** Đảm bảo các lớp callback của bạn ghi đúng luồng và đóng tài nguyên để tránh hỏng tệp.  

## Câu hỏi thường gặp

**Q: Tôi có thể chuyển đổi nhiều tài liệu OneNote sang HTML cùng lúc không?**  
A: Có, lặp qua từng đối tượng `Document` và áp dụng cùng `HtmlSaveOptions`.  

**Q: Aspose.Note for Java có hỗ trợ các định dạng xuất khác ngoài HTML không?**  
A: Chắc chắn. Bạn có thể xuất sang PDF, DOCX, PNG, JPEG và nhiều định dạng khác bằng các tùy chọn lưu tương ứng.  

**Q: Có phiên bản dùng thử cho Aspose.Note for Java không?**  
A: Có, tải bản dùng thử miễn phí từ [here](https://releases.aspose.com/).  

**Q: Tôi có thể nhận hỗ trợ cho Aspose.Note for Java ở đâu?**  
A: Truy cập [Aspose.Note forum](https://forum.aspose.com/c/note/28) để được cộng đồng và hỗ trợ chính thức giúp đỡ.  

**Q: Làm sao để mua giấy phép cho Aspose.Note for Java?**  
A: Giấy phép có sẵn tại [Aspose website](https://purchase.aspose.com/buy).  

## Kết luận

Bây giờ bạn đã biết **cách xuất phông chữ** khi **lưu OneNote dưới dạng HTML** bằng Aspose.Note for Java. Bằng cách cấu hình `HtmlSaveOptions` và (nếu cần) sử dụng callbacks, bạn có thể bảo toàn giao diện chính xác của các trang OneNote—including phông chữ tùy chỉnh—khi đưa chúng lên web. Hãy thử nghiệm các thiết lập `ResourceExportType` khác nhau để phù hợp với yêu cầu hiệu năng và lưu trữ của dự án.

---

**Cập nhật lần cuối:** 2026-02-07  
**Được kiểm tra với:** Aspose.Note for Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}