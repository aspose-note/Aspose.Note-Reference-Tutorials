---
date: 2025-12-02
description: Học cách xuất phông chữ khi lưu OneNote dưới dạng HTML bằng Aspose.Note
  cho Java. Hướng dẫn này chỉ cho bạn cách tạo OneNote bằng lập trình và nhúng phông
  chữ, CSS và hình ảnh.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Cách xuất phông chữ khi lưu OneNote dưới dạng HTML – Java
url: /vi/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Xuất Phông Khi Lưu OneNote dưới dạng HTML – Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách xuất phông** khi **lưu OneNote dưới dạng HTML** bằng Aspose.Note for Java. Chúng tôi sẽ hướng dẫn bạn tạo tài liệu OneNote bằng mã, cấu hình các tùy chọn lưu HTML, và nhúng các tệp phông cần thiết để HTML tạo ra trông hoàn toàn giống như các trang OneNote gốc. Cách tiếp cận này rất phù hợp khi bạn cần bảo toàn độ chính xác hình ảnh của nội dung OneNote trong định dạng thân thiện với web.

## Trả lời nhanh
- **Thư viện nào chịu trách nhiệm xuất?** Aspose.Note for Java  
- **Có thể nhúng phông vào HTML không?** Có – đặt `ExportFonts` thành `ExportEmbedded`  
- **Có cần giấy phép cho môi trường sản xuất không?** Cần giấy phép Aspose.Note hợp lệ cho việc sử dụng thương mại  
- **Phiên bản Java nào được hỗ trợ?** Java 8 hoặc cao hơn  
- **Có thể lưu tài nguyên vào các tệp riêng biệt không?** Chắc chắn – cấu hình `ResourceExportType` cho phù hợp  

## “Cách xuất phông” trong ngữ cảnh chuyển đổi OneNote sang HTML là gì?

Khi bạn chuyển đổi một sổ tay OneNote sang HTML, diện mạo trực quan phụ thuộc vào CSS, hình ảnh và đặc biệt là các phông chữ được sử dụng trong các trang gốc. **Xuất phông** có nghĩa là nhúng các tệp phông (ví dụ: TTF) trực tiếp vào gói HTML để trình duyệt có thể hiển thị văn bản chính xác như trong OneNote, ngay cả khi người dùng cuối không có các phông đó được cài đặt trên máy tính.

## Tại sao lại tạo OneNote bằng mã và lưu dưới dạng HTML?

- **Tự động hoá:** Tạo báo cáo, tài liệu, hoặc bài viết kiến thức từ OneNote mà không cần sao chép thủ công.  
- **Nhất quán:** Bảo toàn bố cục, kiểu dáng và phông chữ tùy chỉnh trên mọi thiết bị.  
- **Di động:** HTML có thể xem ở mọi nơi—không cần client OneNote.  

## Yêu cầu trước

1. Java Development Kit (JDK) 8 hoặc mới hơn đã được cài đặt.  
2. Thư viện Aspose.Note for Java – tải về từ [đây](https://releases.aspose.com/note/java/).  
3. Một tệp OneNote mẫu (`.one`) để tải, hoặc bạn có thể tạo một tệp mới bằng mã.  

## Nhập gói

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

## Cách Xuất Phông Khi Lưu OneNote dưới dạng HTML?

Dưới đây là hướng dẫn từng bước cho bạn **cách xuất phông** và các tài nguyên khác.

### Bước 1: Tạo tài liệu OneNote bằng mã  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Dòng này tải một tệp `.one` hiện có. Nếu bạn cần **tạo OneNote bằng mã**, bạn có thể khởi tạo một đối tượng `Document` mới và thêm các phần/điểm bằng API (không được hiển thị ở đây để tập trung vào việc xuất phông).

### Bước 2: Lưu vào luồng bộ nhớ với phông được nhúng  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` yêu cầu Aspose.Note **xuất phông** trực tiếp vào gói HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` đảm bảo sử dụng phông TrueType, có hỗ trợ rộng rãi trên trình duyệt.

### Bước 3: Lưu dưới dạng HTML với các tệp tài nguyên riêng (vẫn xuất phông)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Mặc dù CSS và hình ảnh đã được nhúng, bạn vẫn có thể thay đổi `ResourceExportType` thành `ExportExternal` nếu muốn các tệp riêng để dễ dàng cache. Phần quan trọng—**xuất phông**—vẫn không thay đổi.

### Bước 4: Sử dụng callback để kiểm soát vị trí lưu từng tài nguyên  

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

Lớp `UserSavingCallbacks` (bạn cần triển khai `ICssSavingCallback`, `IImageSavingCallback`, và `IFontSavingCallback`) cho phép bạn kiểm soát toàn bộ cấu trúc thư mục, giúp lưu phông vào thư mục `fonts` riêng biệt trong khi vẫn **xuất phông** đúng cách.

## Vấn đề thường gặp & Mẹo

- **Phông bị thiếu trong kết quả:** Kiểm tra lại rằng `setExportFonts(ResourceExportType.ExportEmbedded)` đã được đặt và tệp OneNote nguồn thực sự sử dụng phông được nhúng.  
- **HTML lớn:** Nhúng phông có thể làm tăng kích thước. Nếu lo ngại về băng thông, chuyển `ExportFonts` sang `ExportExternal` và lưu phông trên CDN.  
- **Lỗi triển khai callback:** Đảm bảo các lớp callback của bạn ghi đúng luồng và đóng tài nguyên để tránh hỏng tệp.  

## Câu hỏi thường gặp

**H: Tôi có thể chuyển đổi nhiều tài liệu OneNote sang HTML cùng lúc không?**  
Đ: Có, lặp qua từng đối tượng `Document` và áp dụng cùng một `HtmlSaveOptions`.  

**H: Aspose.Note for Java có hỗ trợ các định dạng xuất khác ngoài HTML không?**  
Đ: Chắc chắn. Bạn có thể xuất ra PDF, DOCX, PNG, JPEG, và nhiều định dạng khác bằng các tùy chọn lưu phù hợp.  

**H: Có phiên bản dùng thử cho Aspose.Note for Java không?**  
Đ: Có, tải bản dùng thử miễn phí từ [đây](https://releases.aspose.com/).  

**H: Tôi có thể nhận hỗ trợ cho Aspose.Note for Java ở đâu?**  
Đ: Truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) để nhận trợ giúp từ cộng đồng và đội ngũ chính thức.  

**H: Làm sao để mua giấy phép cho Aspose.Note for Java?**  
Đ: Giấy phép có sẵn tại [trang web Aspose](https://purchase.aspose.com/buy).  

## Kết luận

Bây giờ bạn đã biết **cách xuất phông** khi **lưu OneNote dưới dạng HTML** bằng Aspose.Note for Java. Bằng cách cấu hình `HtmlSaveOptions` và (nếu cần) sử dụng callback, bạn có thể bảo toàn giao diện chính xác của các trang OneNote—including phông tùy chỉnh—khi đưa chúng lên web. Hãy thử các thiết lập `ResourceExportType` khác nhau để phù hợp với yêu cầu hiệu năng và lưu trữ của dự án.

---

**Cập nhật lần cuối:** 2025-12-02  
**Đã kiểm tra với:** Aspose.Note for Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}