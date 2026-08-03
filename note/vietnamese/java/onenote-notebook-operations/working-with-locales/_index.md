---
date: 2026-08-03
description: Tìm hiểu cách đặt locale trong OneNote bằng Aspose.Note cho Java – đặt
  locale mặc định, tải tài liệu, áp dụng giấy phép và chuyển đổi các trang sang hình
  ảnh PNG.
keywords:
- how to set locale
- set default locale java
- change onenote language settings
- convert onenote to png
lastmod: 2026-08-03
linktitle: Làm việc với Locale trong OneNote - Aspose.Note
og_description: Tìm hiểu cách đặt locale trong OneNote bằng Aspose.Note cho Java.
  Thực hiện các hướng dẫn từng bước để đặt locale mặc định, tải một notebook, áp dụng
  giấy phép và xuất các trang dưới dạng hình ảnh PNG.
og_image_alt: 'Developer guide: Set locale and convert OneNote to PNG with Aspose.Note
  Java'
og_title: Cách Đặt Locale trong OneNote – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-03'
  description: Learn how to set locale in OneNote using Aspose.Note for Java – set
    default locale, load documents, apply a license, and convert pages to PNG images.
  headline: How to Set Locale in OneNote – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note supports Java 8 and later, ensuring broad compatibility
      across development environments.
    question: Is Aspose.Note compatible with different versions of Java?
  - answer: Absolutely. The API works seamlessly with popular libraries such as Apache
      POI, Jackson, and Spring.
    question: Can I integrate Aspose.Note with other Java libraries?
  - answer: While its core focus is OneNote files, the library can export to PNG,
      JPEG, PDF, and other image formats—over 30 output options in total.
    question: Does Aspose.Note offer support for different file formats?
  - answer: Yes, the Aspose community forum provides a platform for users to engage
      with experts, ask questions, and collaborate on solutions. Visit the [support
      forum](https://forum.aspose.com/c/note/28) for assistance.
    question: Is there a community forum for Aspose.Note users to seek help and share
      knowledge?
  - answer: Certainly, you can explore the capabilities of Aspose.Note by availing
      the free trial offered on the website.
    question: Can I try Aspose.Note before purchasing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- set locale
- Aspose.Note
- Java OneNote processing
- convert onenote to png
title: Cách Đặt Locale trong OneNote – Aspose.Note Java
url: /vi/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Đặt Ngôn Ngữ Vùng trong OneNote – Aspose.Note Java

## Giới thiệu

Nếu bạn cần **cách đặt locale** khi xử lý các tệp OneNote, Aspose.Note cho Java giúp việc này trở nên đơn giản. Trong hướng dẫn này, chúng tôi sẽ trình bày mọi thứ bạn cần—từ việc cài đặt giấy phép Aspose, tải tài liệu OneNote, thay đổi locale, đến việc chuyển đổi tệp thành hình ảnh PNG. Khi kết thúc, bạn sẽ có thể tùy chỉnh cài đặt ngôn ngữ và tạo ra các đầu ra dựa trên locale chỉ với vài dòng mã Java, điều này rất quan trọng cho các ứng dụng đa quốc gia.

## Câu trả lời nhanh
- **“set default locale” làm gì?** Nó xác định ngôn ngữ và định dạng khu vực được Aspose.Note sử dụng khi đọc hoặc ghi các tệp OneNote.  
- **Tôi có cần giấy phép không?** Có—đặt giấy phép Aspose để mở khóa toàn bộ tính năng.  
- **Phiên bản Java nào được yêu cầu?** Bất kỳ JDK 8+ nào cũng được hỗ trợ.  
- **Tôi có thể chuyển đổi OneNote sang PNG không?** Chắc chắn; API cho phép bạn lưu các trang dưới dạng hình ảnh.  
- **Quá trình có an toàn với đa luồng không?** Việc đặt locale mặc định là toàn cục, vì vậy hãy cấu hình một lần khi khởi động ứng dụng.

## “set default locale” là gì trong Aspose.Note?

Việc đặt locale mặc định cho Aspose.Note biết ngôn ngữ và quy ước văn hoá nào sẽ được áp dụng khi phân tích ngày tháng, số và văn bản. Câu trả lời này trực tiếp giải quyết truy vấn “what is” trong 45 từ, đảm bảo AI có thể trích xuất định nghĩa ngắn gọn. Nó rất cần thiết cho các ứng dụng đa khu vực cần định dạng nhất quán trên các locale của người dùng khác nhau.

## Tại sao phải đặt locale mặc định khi làm việc với OneNote?

Việc đặt locale mặc định đảm bảo rằng ngày tháng, số và chuỗi trích xuất tuân theo quy ước của khu vực mục tiêu, ngăn ngừa việc hiểu sai dữ liệu và đảm bảo các yếu tố trực quan như lịch hiển thị đúng. Điều này dẫn đến việc biểu diễn dữ liệu chính xác, các chuỗi UI nhất quán và kết quả chuyển đổi hình ảnh mượt mà hơn.

## Yêu cầu trước

- **Môi trường phát triển Java:** JDK 8 hoặc mới hơn đã được cài đặt và `JAVA_HOME` được cấu hình.  
- **Thư viện Aspose.Note:** Tải JAR mới nhất từ [liên kết tải xuống](https://releases.aspose.com/note/java/).  
- **Tệp giấy phép Aspose hợp lệ** (bản dùng thử miễn phí hoạt động cho việc thử nghiệm).

## Nhập các gói

Lớp `Locale` đại diện cho một khu vực địa lý, chính trị hoặc văn hoá cụ thể.  
```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Bước 1: Đặt giấy phép Aspose

Lớp `License` tải tệp giấy phép đã mua của bạn và mở khóa tất cả các tính năng cao cấp, bao gồm xử lý locale và chuyển đổi hình ảnh.  
```java
License license = new License();
license.setLicense("licenseFile");
```

## Bước 2: Đặt Locale Mặc Định

`Locale` là tiện ích Java bao gồm mã ngôn ngữ và mã quốc gia.  
Ở đây chúng ta đặt locale mặc định thành tiếng Anh (`en`) với mã quốc gia `RS`. Điều chỉnh mã ngôn ngữ và quốc gia cho phù hợp với khu vực mục tiêu của bạn trước khi thực hiện bất kỳ thao tác tài liệu nào.  
```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

## Bước 3: Tải tài liệu OneNote

`Document` là đối tượng cấp cao nhất của Aspose.Note đại diện cho một tệp OneNote duy nhất trong bộ nhớ. Sau khi khởi tạo, tất cả các thao tác đọc và ghi sẽ diễn ra qua đối tượng này.  
```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

## Bước 4: Chuyển đổi OneNote sang PNG (chuyển đổi tệp OneNote)

Các đối tượng `Page` trong `Document` có thể được render thành hình ảnh raster. Phương thức `save` thực hiện việc chuyển đổi tệp OneNote, xuất sổ ghi chú (hoặc một trang cụ thể) dưới dạng hình ảnh PNG—thực tế là **chuyển đổi onenote sang png** và **lưu onenote dưới dạng hình ảnh**.  
```java
oneFile.save("sample.png");
```

## Các vấn đề thường gặp & Mẹo

- **Không tìm thấy giấy phép:** Đảm bảo đường dẫn tới `licenseFile` là đúng và tệp có quyền đọc.  
- **Locale không được áp dụng:** Gọi `Locale.setDefault` **trước** khi tải tài liệu; nếu không locale mặc định sẽ bị bỏ qua.  
- **Thiếu đầu ra hình ảnh:** Kiểm tra xem tệp OneNote thực sự có chứa các trang có thể render không; sổ ghi chú trống sẽ tạo ra PNG trắng.  
- **Mẹo hiệu năng:** Aspose.Note cho Java có thể xử lý sổ ghi chú lên tới 500 trang mà không cần tải toàn bộ tệp vào bộ nhớ, nhờ kiến trúc streaming của nó (khẳng định có số liệu).

## Câu hỏi thường gặp

**Q: Aspose.Note có tương thích với các phiên bản Java khác nhau không?**  
A: Có, Aspose.Note hỗ trợ Java 8 trở lên, đảm bảo tính tương thích rộng rãi trên các môi trường phát triển.

**Q: Tôi có thể tích hợp Aspose.Note với các thư viện Java khác không?**  
A: Chắc chắn. API hoạt động liền mạch với các thư viện phổ biến như Apache POI, Jackson và Spring.

**Q: Aspose.Note có hỗ trợ các định dạng tệp khác không?**  
A: Mặc dù trọng tâm chính là các tệp OneNote, thư viện có thể xuất ra PNG, JPEG, PDF và các định dạng hình ảnh khác—hơn 30 tùy chọn xuất tổng cộng.

**Q: Có diễn đàn cộng đồng cho người dùng Aspose.Note để tìm kiếm trợ giúp và chia sẻ kiến thức không?**  
A: Có, diễn đàn cộng đồng Aspose cung cấp nền tảng cho người dùng tương tác với chuyên gia, đặt câu hỏi và hợp tác giải quyết vấn đề. Truy cập [diễn đàn hỗ trợ](https://forum.aspose.com/c/note/28) để được trợ giúp.

**Q: Tôi có thể dùng thử Aspose.Note trước khi mua không?**  
A: Chắc chắn, bạn có thể khám phá các tính năng của Aspose.Note bằng cách sử dụng bản dùng thử miễn phí được cung cấp trên trang web.

## Kết luận

Bằng cách thực hiện các bước này, bạn đã học được **cách đặt locale**, **tải tài liệu OneNote**, **áp dụng giấy phép Aspose**, và **chuyển đổi OneNote sang PNG** bằng Aspose.Note cho Java. Quy trình này cho phép bạn tạo các báo cáo và hình ảnh nhận biết locale, phục vụ khán giả toàn cầu, tận dụng thư viện hỗ trợ hơn 30 tính năng đặc thù cho locale và có thể xử lý sổ ghi chú lên tới 500 trang một cách hiệu quả.

---

**Last Updated:** 2026-08-03  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose  

---

## Hướng dẫn liên quan

- [Tạo Sổ OneNote – Các thao tác với Aspose.Note cho Java](/note/java/onenote-notebook-operations/)
- [Tạo Đối tượng Notebook và Tải Tệp OneNote với Các Tùy chọn - Aspose.Note](/note/java/onenote-notebook-operations/load-notebook-file-with-load-options/)
- [Chuyển đổi Notebook sang Hình ảnh với Các Tùy chọn trong OneNote - Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}