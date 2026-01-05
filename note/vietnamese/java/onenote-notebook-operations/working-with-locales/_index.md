---
date: 2026-01-05
description: Tìm hiểu cách thiết lập ngôn ngữ mặc định, tải tài liệu OneNote, thiết
  lập giấy phép Aspose, chuyển đổi OneNote sang PNG và lưu OneNote dưới dạng hình
  ảnh bằng Aspose.Note cho Java.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Đặt Ngôn ngữ Mặc định trong OneNote – Aspose.Note Java
url: /vi/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt Ngôn Ngữ Mặc Định trong OneNote – Aspose.Note Java

## Giới thiệu

Nếu bạn cần **đặt ngôn ngữ mặc định** khi xử lý các tệp OneNote, Aspose.Note cho Java sẽ giúp việc này trở nên dễ dàng. Trong hướng dẫn này, chúng tôi sẽ đi qua mọi thứ bạn cần—từ việc cấp phép sản phẩm đến tải tài liệu OneNote, thay đổi ngôn ngữ, và cuối cùng chuyển đổi tệp thành ảnh PNG. Khi kết thúc, bạn sẽ có thể tùy chỉnh cài đặt ngôn ngữ và tạo ra các đầu ra phù hợp với ngôn ngữ chỉ với vài dòng mã.

## Câu trả lời nhanh
- **Câu hỏi: “đặt ngôn ngữ mặc định” làm gì?** Nó xác định ngôn ngữ và định dạng khu vực được Aspose.Note sử dụng khi đọc hoặc ghi các tệp OneNote.  
- **Tôi có cần giấy phép không?** Có—đặt giấy phép Aspose để mở khóa toàn bộ chức năng.  
- **Yêu cầu phiên bản Java nào?** Bất kỳ JDK 8+ nào cũng được hỗ trợ.  
- **Tôi có thể chuyển đổi OneNote sang PNG không?** Chắc chắn; API cho phép bạn lưu các trang dưới dạng hình ảnh.  
- **Quá trình này có an toàn với đa luồng không?** Đặt ngôn ngữ mặc định là toàn cục, vì vậy chỉ cần cấu hình một lần khi khởi động ứng dụng.

## “Đặt ngôn ngữ mặc định” trong Aspose.Note là gì?
Việc đặt ngôn ngữ mặc định cho Aspose.Note chỉ cho nó biết ngôn ngữ và quy ước văn hoá nào sẽ được áp dụng khi phân tích ngày tháng, số và văn bản. Điều này rất quan trọng đối với các ứng dụng đa khu vực cần định dạng nhất quán trên các ngôn ngữ người dùng khác nhau.

## Tại sao cần đặt ngôn ngữ mặc định khi làm việc với OneNote?
- **Đại diện dữ liệu chính xác:** Ngày tháng và số xuất hiện đúng cho đối tượng mục tiêu.  
- **Chuỗi UI nhất quán:** Văn bản trích xuất từ OneNote tuân theo cài đặt ngôn ngữ.  
- **Chuyển đổi đơn giản:** Khi bạn chuyển đổi tệp OneNote sang PNG hoặc các định dạng khác, bố cục hình ảnh sẽ phù hợp với ngôn ngữ mong muốn.

## Yêu cầu trước

- **Môi trường phát triển Java:** JDK đã được cài đặt và `JAVA_HOME` được cấu hình.  
- **Thư viện Aspose.Note:** Tải JAR mới nhất từ [download link](https://releases.aspose.com/note/java/).  
- **Tệp giấy phép Aspose hợp lệ** (bản dùng thử miễn phí cũng hoạt động cho việc thử nghiệm).

## Nhập các gói

Trước khi viết bất kỳ mã nào, hãy nhập các lớp cung cấp chức năng cần thiết.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Bước 1: Đặt giấy phép Aspose

```java
License license = new License();
license.setLicense("licenseFile");
```

Đặt giấy phép Aspose sẽ mở khóa tất cả các tính năng, bao gồm xử lý ngôn ngữ và chuyển đổi hình ảnh.

## Bước 2: Đặt Ngôn Ngữ Mặc Định

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Ở đây chúng tôi **đặt ngôn ngữ mặc định** thành tiếng Anh (`en`) với mã quốc gia `rs`. Điều chỉnh mã ngôn ngữ và quốc gia cho phù hợp với khu vực mục tiêu của bạn.

## Bước 3: Tải tài liệu OneNote

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Bước này **tải tài liệu OneNote** vào đối tượng `Document` để bạn có thể làm việc với nội dung của nó.

## Bước 4: Chuyển đổi OneNote sang PNG (chuyển đổi tệp OneNote)

```java
oneFile.save("sample.png");
```

Phương thức `save` thực hiện một **chuyển đổi tệp onenote**, xuất sổ ghi chú (hoặc một trang cụ thể) dưới dạng ảnh PNG—thực chất **chuyển đổi onenote sang png** và **lưu onenote dưới dạng hình ảnh**.

## Các vấn đề thường gặp & Mẹo

- **Không tìm thấy giấy phép:** Đảm bảo đường dẫn tới `licenseFile` là đúng và tệp có quyền đọc.  
- **Ngôn ngữ không được áp dụng:** Gọi `Locale.setDefault` **trước** khi tải tài liệu.  
- **Không có ảnh xuất ra:** Kiểm tra xem tệp OneNote có thực sự chứa các trang có thể render không; sổ ghi chú trống sẽ tạo ra PNG trắng.

## Câu hỏi thường gặp

**Q: Aspose.Note có tương thích với các phiên bản Java khác nhau không?**  
A: Có, Aspose.Note hỗ trợ Java 8 trở lên, đảm bảo tính tương thích rộng rãi trên các môi trường phát triển.

**Q: Tôi có thể tích hợp Aspose.Note với các thư viện Java khác không?**  
A: Chắc chắn. API hoạt động liền mạch với các thư viện phổ biến như Apache POI, Jackson và Spring.

**Q: Aspose.Note có hỗ trợ các định dạng tệp khác không?**  
A: Mặc dù trọng tâm chính là các tệp OneNote, thư viện có thể xuất ra PNG, JPEG, PDF và các định dạng hình ảnh khác.

**Q: Có diễn đàn cộng đồng cho người dùng Aspose.Note để tìm kiếm trợ giúp và chia sẻ kiến thức không?**  
A: Có, diễn đàn cộng đồng Aspose cung cấp nền tảng cho người dùng giao lưu với chuyên gia, đặt câu hỏi và hợp tác giải quyết vấn đề. Truy cập [support forum](https://forum.aspose.com/c/note/28) để được hỗ trợ.

**Q: Tôi có thể dùng thử Aspose.Note trước khi mua không?**  
A: Chắc chắn, bạn có thể khám phá các tính năng của Aspose.Note bằng cách sử dụng bản dùng thử miễn phí được cung cấp trên trang web.

## Kết luận

Bằng cách thực hiện các bước này, bạn đã học cách **đặt ngôn ngữ mặc định**, **tải tài liệu OneNote**, **đặt giấy phép Aspose**, và **chuyển đổi OneNote sang PNG** bằng Aspose.Note cho Java. Quy trình này cho phép bạn tạo ra các báo cáo và hình ảnh có nhận thức ngôn ngữ, phù hợp với khán giả toàn cầu.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-05  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose