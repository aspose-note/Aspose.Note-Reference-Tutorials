---
date: 2025-12-11
description: Học cách tải tài liệu OneNote được bảo vệ bằng mật khẩu với Aspose.Note
  cho Java. Hướng dẫn từng bước này cho bạn biết cách lấy định dạng tệp OneNote và
  xử lý các tệp được mã hóa một cách dễ dàng.
linktitle: Load Password-Protected OneNote Document - Java
second_title: Aspose.Note Java API
title: Tải tài liệu OneNote được bảo vệ bằng mật khẩu bằng Java
url: /vi/java/onenote-document-loading/load-password-protected-onenote/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tải tài liệu OneNote được bảo vệ bằng mật khẩu bằng Java

Trong hướng dẫn này, bạn sẽ khám phá **cách tải các tệp OneNote được bảo vệ bằng mật khẩu** bằng Aspose.Note cho Java. Dù bạn đang xây dựng một tiện ích desktop hay một dịch vụ phía máy chủ, khả năng mở các sổ tay OneNote đã được mã hóa là cần thiết cho quy trình công việc tài liệu an toàn. Chúng tôi cũng sẽ chỉ cho bạn cách **lấy thông tin định dạng tệp OneNote** sau khi tải tài liệu.

## Câu trả lời nhanh
- **Thư viện nào xử lý các tệp OneNote được mã hóa?** Aspose.Note cho Java.
- **Tôi có cần giấy phép để tải các sổ tay được bảo vệ bằng mật khẩu không?** Bản dùng thử miễn phí hoạt động cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.
- **Phiên bản Java nào được yêu cầu?** Java 8 hoặc mới hơn.
- **Tôi có thể lấy định dạng tệp sau khi tải không?** Có, sử dụng `doc.getFileFormat()`.
- **Cần xử lý lỗi cho mật khẩu sai không?** Chắc chắn – bắt `IOException` hoặc `InvalidPasswordException`.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có những thứ sau:

### 1. Java Development Kit (JDK)
Một JDK mới (8 hoặc mới hơn) được cài đặt trên máy của bạn. Bạn có thể tải xuống từ trang web Oracle hoặc sử dụng bản phân phối OpenJDK.

### 2. Aspose.Note for Java
Thêm thư viện Aspose.Note vào dự án của bạn qua Maven, Gradle, hoặc tải JAR từ trang web Aspose.

## Nhập các gói

Đầu tiên, nhập các lớp chúng ta sẽ cần. Khối này phải giữ nguyên như đã hiển thị.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
```

## Hướng dẫn từng bước

### Bước 1: Xác định thư mục tài liệu
Cho ứng dụng biết tệp OneNote nằm ở đâu.

```java
String dataDir = "Your Document Directory";
```

### Bước 2: Tạo tùy chọn tải với mật khẩu
Cấu hình `LoadOptions` để cung cấp mật khẩu cho sổ tay đã được mã hóa.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setDocumentPassword("password");
```

### Bước 3: Tải tài liệu OneNote được bảo vệ bằng mật khẩu
Truyền đường dẫn tệp và thể hiện `LoadOptions` vào hàm khởi tạo `Document`.

```java
Document doc = new Document(dataDir + "Sample1.one", loadOptions);
```

### Bước 4: Lấy định dạng tệp OneNote (tùy chọn)
Nếu bạn cần xác minh loại tệp, bạn có thể truy vấn định dạng sau khi tải.

```java
System.out.println(doc.getFileFormat());
```

## Tại sao bạn có thể cần **lấy định dạng tệp OneNote**

Biết định dạng chính xác (ví dụ: OneNote 2007, OneNote 2010, OneNote 2016) giúp khi bạn cần chuyển đổi, xuất hoặc áp dụng logic theo phiên bản. Lệnh gọi `getFileFormat()` cung cấp thông tin này ngay lập tức.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Mật khẩu không đúng** | Bao quanh mã tải trong khối try‑catch và hiển thị thông báo thân thiện. |
| **Không tìm thấy tệp** | Kiểm tra `dataDir` kết thúc bằng dấu phân cách đường dẫn và tên tệp là đúng. |
| **Phiên bản OneNote không được hỗ trợ** | Đảm bảo bạn đang sử dụng bản phát hành Aspose.Note mới nhất, bản này bổ sung hỗ trợ cho các định dạng mới hơn. |

## Câu hỏi thường gặp

**Q: Tôi có thể tải nhiều tài liệu OneNote được bảo vệ bằng mật khẩu cùng lúc không?**  
A: Có. Chỉ cần lặp lại các bước tải cho mỗi tệp, cung cấp mật khẩu phù hợp mỗi lần.

**Q: Aspose.Note cho Java có tương thích với mọi phiên bản OneNote không?**  
A: Thư viện hỗ trợ nhiều định dạng OneNote, bao gồm các phiên bản cũ và sổ tay Office 365 mới nhất.

**Q: Tôi nên xử lý lỗi giải mã như thế nào trong chương trình?**  
A: Bắt `IOException` hoặc `InvalidPasswordException` cụ thể, ghi lại sự cố, và tùy chọn yêu cầu người dùng nhập lại mật khẩu mới.

**Q: Có phiên bản dùng thử của Aspose.Note cho Java không?**  
A: Chắc chắn. Bạn có thể tải bản dùng thử đầy đủ chức năng 30 ngày từ trang web Aspose.

**Q: Tôi có thể sử dụng thư viện này trong cả ứng dụng desktop và web không?**  
A: Có. API không phụ thuộc vào nền tảng và hoạt động tốt trong các container servlet, dịch vụ Spring Boot, hoặc ứng dụng Java độc lập.

**Q: Thư viện có hỗ trợ trích xuất hình ảnh từ sổ tay được bảo vệ bằng mật khẩu không?**  
A: Khi tài liệu được tải thành công, bạn có thể duyệt các trang và trích xuất hình ảnh bằng API chuẩn của Aspose.Note.

**Cập nhật lần cuối:** 2025-12-11  
**Được kiểm tra với:** Aspose.Note cho Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}