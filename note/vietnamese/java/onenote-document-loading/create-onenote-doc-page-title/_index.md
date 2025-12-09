---
date: 2025-12-02
description: Tìm hiểu cách tạo trang OneNote có tiêu đề bằng Java sử dụng Aspose.Note
  cho Java. Hướng dẫn này cho thấy cách đặt tiêu đề cho trang OneNote và tùy chỉnh
  phông chữ tiêu đề.
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: Cách tạo trang OneNote có tiêu đề - Java
url: /vi/java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Tạo Trang OneNote với Tiêu Đề - Java

## Giới thiệu

Nếu bạn cần **cách tạo trang OneNote** một cách lập trình, Aspose.Note for Java giúp việc này trở nên đơn giản. Trong hướng dẫn này, bạn sẽ học cách tạo một tệp OneNote, đặt tiêu đề cho trang, và thậm chí tùy chỉnh phông chữ của tiêu đề — tất cả từ mã Java. Khi hoàn thành, bạn sẽ có một tài liệu OneNote sẵn sàng sử dụng mà có thể tích hợp vào bất kỳ ứng dụng Java nào.

## Câu trả lời nhanh
- **Thư viện nào được yêu cầu?** Aspose.Note for Java.  
- **Tôi có thể đặt phông chữ tùy chỉnh cho tiêu đề không?** Có – sử dụng `ParagraphStyle` để xác định tên phông, kích thước và màu.  
- **Phiên bản Java nào được hỗ trợ?** Bất kỳ JDK 8+ nào (API tương thích ngược).  
- **Tôi có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; cần giấy phép cho môi trường sản xuất.  
- **Đầu ra được lưu ở đâu?** Bạn định nghĩa đường dẫn trong biến `dataDir`.

## Tiêu đề Trang OneNote là gì?
Tiêu đề trang OneNote là phần đầu hiển thị ở trên cùng của mỗi trang. Thông thường nó bao gồm tên trang, ngày tạo và thời gian. Đặt tiêu đề này bằng mã giúp bạn tạo ra các sổ ghi chép nhất quán và có cấu trúc tốt.

## Tại sao nên đặt tiêu đề trang OneNote một cách lập trình?
- **Tự động hoá:** Tạo báo cáo hoặc biên bản cuộc họp mà không cần chỉnh sửa thủ công.  
- **Nhất quán:** Thực thi quy tắc đặt tên đồng nhất cho tất cả các trang.  
- **Tích hợp:** Kết hợp OneNote với các hệ thống khác (ví dụ: CRM, công cụ quản lý dự án).  

## Yêu cầu trước

- **Bộ công cụ phát triển Java (JDK)** – phiên bản 8 trở lên.  
- **Aspose.Note for Java** – tải xuống từ trang chính thức **[here](https://releases.aspose.com/note/java/)**.  
- **IDE** – IntelliJ IDEA, Eclipse hoặc NetBeans (tùy chọn).

## Nhập các gói

Đầu tiên, nhập các lớp cần thiết từ thư viện Aspose.Note.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### Bước 1: Thiết lập Thư mục Tài liệu  
Xác định nơi sẽ lưu tệp OneNote được tạo.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### Bước 2: Tạo Đối tượng Document  
Khởi tạo một `Document` mới – đại diện cho tệp OneNote bạn sẽ xây dựng.

```java
// Create an object of the Document class
Document doc = new Document();
```

### Bước 3: Khởi tạo Đối tượng Page  
Tạo một đối tượng `Page` sẽ chứa tiêu đề và bất kỳ nội dung nào khác.

```java
// Initialize Page class object
Page page = new Page();
```

### Bước 4: Đặt Kiểu Văn bản Mặc định  
Xác định một `ParagraphStyle` mặc định sẽ được áp dụng cho văn bản tiêu đề. Đây là nơi chúng ta **tùy chỉnh phông tiêu đề OneNote**.

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### Bước 5: Đặt Thuộc tính Tiêu đề Trang  
Ở đây chúng ta **đặt chi tiết tiêu đề trang OneNote** – văn bản tiêu đề, ngày và thời gian. Bạn có thể sửa đổi các chuỗi này để phù hợp với nhu cầu của mình.

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### Bước 6: Gán Tiêu đề cho Trang  
Bây giờ chúng ta **thêm tiêu đề vào OneNote** bằng cách liên kết đối tượng `Title` với `Page`.

```java
page.setTitle(title);
```

### Bước 7: Thêm Trang vào Document  
Thêm trang đã cấu hình vào cấu trúc tài liệu.

```java
doc.appendChildLast(page);
```

### Bước 8: Lưu Tài liệu OneNote  
Xác định tên tệp đầu ra và lưu sổ ghi chú. Điều này hoàn thành quy trình **java create onenote file**.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## Các vấn đề thường gặp & Mẹo

| Vấn đề | Giải pháp |
|-------|----------|
| **Đường dẫn tệp không hợp lệ** | Đảm bảo `dataDir` kết thúc bằng dấu phân cách thích hợp (`/` hoặc `\\`) và thư mục tồn tại. |
| **Tiêu đề không hiển thị** | Kiểm tra rằng `ParagraphStyle` đã được áp dụng cho mỗi phần tử `RichText`. |
| **Ngoại lệ giấy phép** | Sử dụng giấy phép dùng thử để thử nghiệm; áp dụng giấy phép đầy đủ trước khi triển khai. |
| **Ngày hiển thị tháng sai** | Các tháng trong Java bắt đầu từ 0; `cal.set(2018, 04, 03)` thực tế đặt là tháng 5. Điều chỉnh cho phù hợp. |

## Câu hỏi thường gặp

**Q: Aspose.Note for Java có tương thích với các phiên bản Java khác nhau không?**  
A: Có, thư viện hoạt động với Java 8 và các phiên bản mới hơn, mang lại sự linh hoạt cho môi trường của bạn.

**Q: Tôi có thể tùy chỉnh kiểu và kích thước phông chữ của tiêu đề trang không?**  
A: Chắc chắn! Sử dụng `ParagraphStyle` (như trong Bước 4) để đặt bất kỳ tên phông, kích thước và màu nào.

**Q: Làm sao để thêm nội dung khác (ví dụ: đoạn văn, hình ảnh) vào trang?**  
A: Tạo các đối tượng `RichText` hoặc `Image` bổ sung, đặt kiểu cho chúng, và thêm vào `Page` bằng `page.appendChildLast(yourObject)`.

**Q: Có phiên bản dùng thử cho Aspose.Note for Java không?**  
A: Có, bạn có thể tải bản dùng thử miễn phí từ trang web Aspose để đánh giá toàn bộ tính năng.

**Q: Tôi có thể nhận hỗ trợ ở đâu nếu gặp vấn đề?**  
A: Truy cập [diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) để nhận trợ giúp từ cộng đồng hoặc mở ticket hỗ trợ với Aspose.

---

**Cập nhật lần cuối:** 2025-12-02  
**Được kiểm tra với:** Aspose.Note for Java 24.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}