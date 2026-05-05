---
date: 2025-12-20
description: Tìm hiểu cách thêm hình ảnh vào OneNote bằng Aspose.Note cho Java. Hướng
  dẫn từng bước để tạo tài liệu OneNote và chèn hình ảnh một cách lập trình.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Cách thêm hình ảnh vào OneNote bằng Java – Tạo tài liệu và chèn hình
url: /vi/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách thêm hình ảnh vào OneNote bằng Java – Tạo tài liệu và chèn ảnh

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học **cách thêm hình ảnh vào OneNote** bằng API Aspose.Note Java. Chúng tôi sẽ hướng dẫn tạo tài liệu OneNote từ đầu, chèn một hình ảnh và lưu kết quả dưới dạng PDF. Dù bạn đang xây dựng công cụ báo cáo, ghi chú tự động hay chỉ cần nhúng đồ họa bằng trình cài đặt, hướng dẫn này sẽ cung cấp một hành động rõ ràng, rõ ràng.

## Trả lời nhanh
- **Thư viện tôi cần là gì?** Aspose.Note for Java.
- **Tôi có thể chèn bất kỳ định dạng hình ảnh nào?** JPEG, PNG, BMP, GIF và nhiều định dạng khác được hỗ trợ.
- **Có sẵn các định dạng xuất ra?** Bạn có thể lưu dưới các dạng OneNote, PDF, XPS, HTML, v.v.
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Có, cần giấy phép thương mại cho việc sử dụng không phải thử nghiệm.
- **Không có nền tảng nào?** Chắc chắn – Java chạy trên Windows, Linux và macOS.

## “thêm ảnh vào OneNote” là gì?
Thêm hình ảnh vào OneNote có nghĩa là nhúng một tệp hình ảnh vào một trang OneNote một cách thiết lập trình sao cho nó hiển thị cùng với văn bản, dàn trang hoặc các yếu tố khác. API Aspose.Note được thể hiện dưới dạng biểu tượng OneNote tệp định dạng, cho phép bạn tập trung vào nội dung thay vì bên trong cấu trúc XML.

## Tại sao thêm ảnh vào OneNote bằng Java?
- **Tự động hóa:** Tự động tạo bản trình bày với ảnh chụp màn hình.
- **Nhất quán:** Đảm bảo mọi trang đi kèm theo cùng một bố địa và thương hiệu.
- **Tích hợp:** Kết hợp dữ liệu từ các hệ thống khác (ví dụ, biểu đồ) trực tiếp vào OneNote trong sổ tay.
- **Da nền:** Java cho phép bạn chạy cùng một mã hóa trên bất kỳ môi trường máy chủ hoặc máy tính nào để bàn.

## Điều kiện tiên quyết

Trước khi bắt đầu, hãy đảm bảo rằng bạn có các yêu cầu sau:

1. **Bộ công cụ phát triển Java (JDK)** – bất kỳ phiên bản nào mới (8 trở lên).
2. **Thư viện Aspose.Note for Java** – tải xuống từ [trang web](https://releases.aspose.com/note/java/).
3. **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình chỉnh sửa Java nào mà bạn thích.

## Nhập gói

Bắt đầu bằng cách nhập các lớp cần thiết vào nguồn Java tệp của bạn:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Hướng dẫn từng bước

### Bước 1: Thiết lập tài liệu

Tạo một tài liệu OneNote mới và một container trang nơi nội dung sẽ được đặt.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Bước 2: Khởi tạo dàn ý

Một *outline* hoạt động như một container cho các yếu tố như văn bản và hình ảnh. Chúng ta đặt các offset của nó về 0 để nội dung bắt đầu ở góc trên‑trái.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Bước 3: Tải và căn chỉnh hình ảnh

Tải hình ảnh bạn muốn nhúng và căn chỉnh nó sang phía bên phải của trang. Đây là nơi chúng ta thực sự **thêm hình ảnh vào OneNote**.

```java
Image image = new Image(dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Bước 4: Đính kèm hình ảnh vào một phần tử trong dàn ý

Đóng gói hình ảnh bên trong một `OutlineElement`. Bước này liên kết đối tượng hình ảnh với cấu trúc outline của tài liệu.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Bước 5: Lắp ráp cấu trúc tài liệu

Thêm phần tử outline vào outline, sau đó gắn outline vào trang, và cuối cùng thêm trang vào tài liệu.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Bước 6: Lưu tài liệu OneNote

Lưu tài liệu xuống đĩa. Trong ví dụ này chúng tôi xuất ra PDF, nhưng bạn cũng có thể lưu dưới dạng tệp OneNote gốc (`.one`) bằng cách thay đổi `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách giải quyết |
|-------|--------------------------|-------|
| **Hình ảnh không hiển thị** | Sai hoặc định dạng tệp dẫn không được hỗ trợ. | Xác định `dataDir` trỏ tới đúng thư mục và sử dụng hình ảnh định dạng được hỗ trợ (JPEG, PNG, v.v.). |
| **Tài liệu được lưu dưới dạng PDF trống** | Phần bù của đường viền được đặt không chính xác. | Đảm bảo gọi `setVerticalOffset(0)` và `setHorizontalOffset(0)`, hoặc điều chỉnh offset để đặt nội dung trong giới hạn trang. |
| **IOException khi lưu** | Đích thư mục không tồn tại hoặc thiếu quyền ghi. | Tạo thư mục trước hoặc chạy chương trình phù hợp. |

## Câu hỏi thường gặp

**Q1: ​​Tôi có thể tìm tài liệu cho Aspose.Note for Java ở đâu?**
A1: Bạn có thể truy cập tài liệu [tại đây](https://reference.aspose.com/note/java/).

**Q2: Làm sao để tải Aspose.Note for Java?**
A2: Bạn có thể tải Aspose.Note for Java từ [trang tải xuống](https://releases.aspose.com/note/java/).

**Q3: Có phiên bản dùng thử miễn phí cho Aspose.Note for Java không?**
A3: Có, bạn có thể nhận bản thử miễn phí từ [trang web](https://releases.aspose.com/).

**Q4: Tôi có thể nhận được hỗ trợ cho Aspose.Note for Java ở đâu?**
A4: Để được hỗ trợ, hãy truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28).

**Q5: Tôi có thể lấy giấy phép tạm thời cho Aspose.Note for Java không?**
A5: Có, bạn có thể yêu cầu giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

---

**Cập nhật lần cuối:** 2025-12-20
**Kiểm tra với:** Aspose.Note for Java 26.4 (mới nhất)
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}