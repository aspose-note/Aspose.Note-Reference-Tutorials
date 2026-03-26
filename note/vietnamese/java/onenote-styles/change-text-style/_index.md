---
date: 2026-01-18
description: Tìm hiểu cách đặt màu phông chữ Java trong OneNote bằng Aspose.Note,
  làm nổi bật văn bản, chỉnh sửa kích thước phông chữ và lưu OneNote dưới dạng PDF.
  Hướng dẫn từng bước kèm mã nguồn.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Thiết lập màu phông chữ Java trong OneNote – Aspose.Note
url: /vi/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt Màu Chữ Java trong OneNote – Aspose.Note

## Giới thiệu

Trong hướng dẫn này bạn sẽ khám phá cách **đặt màu chữ Java** cho văn bản trong tài liệu OneNote bằng API Aspose.Note cho Java. Chúng ta sẽ thực hiện các bước tải tệp `.one`, truy cập các nút RichText, áp dụng thay đổi màu, tô sáng và kích thước phông chữ, và cuối cùng **lưu OneNote dưới dạng PDF**. Dù bạn cần **tô sáng văn bản onenote**, **thay đổi kích thước phông chữ onenote**, hay chỉ đơn giản là thay đổi kiểu chữ chung, các bước dưới đây cung cấp một giải pháp hoàn chỉnh, sẵn sàng cho môi trường sản xuất.

## Câu trả lời nhanh
- **Tôi có thể thay đổi màu chữ của các từ cụ thể không?** Có – lặp qua các đối tượng `TextRun` và gọi `setFontColor`.
- **Aspose.Note có cho phép lưu OneNote dưới dạng PDF không?** Chắc chắn; sử dụng `document.save("output.pdf")`.
- **Yêu cầu phiên bản Java nào?** Java 8 hoặc cao hơn.
- **Có hỗ trợ tô sáng không?** Dùng `setHighlight(Color)` trên `TextStyle`.
- **Tôi có thể chuyển OneNote sang PDF trong một dòng không?** Không trực tiếp, nhưng phương thức `save` thực hiện việc chuyển đổi.

## “set font color java” là gì?

Cụm từ này đề cập đến việc gán màu chữ mới cho các thành phần văn bản trong tệp OneNote một cách lập trình bằng mã Java. Với Aspose.Note, bạn có toàn quyền kiểm soát các thuộc tính kiểu dáng như màu chữ, tô sáng và kích thước mà không cần mở giao diện OneNote.

## Tại sao phải thay đổi kiểu chữ onenote?

- **Cải thiện khả năng đọc** – Văn bản có màu hoặc được tô sáng sẽ thu hút sự chú ý tới các điểm quan trọng.
- **Đồng nhất thương hiệu** – Áp dụng màu sắc công ty trên các ghi chú cuộc họp.
- **Chất lượng xuất khẩu** – Các ghi chú được định dạng sẽ trông chuyên nghiệp hơn khi bạn **chuyển đổi onenote sang pdf** để chia sẻ.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

1. Kiến thức cơ bản về lập trình Java.  
2. JDK 8 hoặc mới hơn đã được cài đặt.  
3. Thư viện Aspose.Note cho Java đã được thêm vào dự án (Maven/Gradle hoặc JAR thủ công).  
4. Một tệp OneNote mẫu (`Sample1.one`) để thực hành.  

## Nhập các gói

Đầu tiên, nhập các lớp cần thiết:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## Hướng dẫn từng bước

### Bước 1: Tải tài liệu

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

Chúng ta tải tệp OneNote (`Sample1.one`) để Aspose.Note có thể làm việc với cấu trúc nội bộ của nó.

### Bước 2: Truy cập các nút RichText

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

Các đối tượng `RichText` chứa các đoạn văn thực tế. Bằng cách lấy nút đầu tiên, chúng ta có được một tham chiếu tới văn bản cần định dạng.

### Bước 3: Thay đổi kiểu chữ (set font color java)

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

Trong vòng lặp, chúng ta **đặt màu chữ Java** thành màu vàng, áp dụng tô sáng màu xanh dương (để minh họa **highlight text onenote**), và tăng kích thước lên 20 điểm, thể hiện **modify font size onenote**.

### Bước 4: Lưu tài liệu (save onenote as pdf)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

Gọi `save` với phần mở rộng `.pdf` sẽ tự động **convert onenote to pdf**, cung cấp cho bạn một tệp sẵn sàng chia sẻ.

## Các vấn đề thường gặp & Giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| Không thấy thay đổi màu | Tài liệu đã được mở trong OneNote trước khi lưu | Đóng OneNote hoặc tải lại tệp sau khi quá trình Java kết thúc |
| Tô sáng không áp dụng | Sử dụng màu trùng với nền | Chọn một `Color` tương phản (ví dụ, `Color.yellow`) |
| `document.save` ném `IOException` | Đường dẫn đầu ra không hợp lệ | Đảm bảo thư mục tồn tại và bạn có quyền ghi |

## Câu hỏi thường gặp

**H: Tôi có thể áp dụng các thay đổi kiểu này chỉ cho một số phần nhất định trong tệp OneNote không?**  
Đ: Có – lọc các nút `RichText` theo `Section` hoặc `Page` cha trước khi lặp qua các `TextRun`.

**H: Ngoài màu, tô sáng và kích thước, Aspose.Note còn hỗ trợ định dạng nào khác?**  
Đ: Bạn có thể thay đổi họ phông chữ, in đậm/nghiêng/gạch chân, căn chỉnh, và thậm chí khoảng cách đoạn văn.

**H: Có thể xử lý hàng loạt nhiều tệp OneNote không?**  
Đ: Chắc chắn. Đặt logic tải và định dạng trong một vòng lặp để xử lý từng tệp `.one` trong một thư mục.

**H: Thư viện có hỗ trợ lưu trực tiếp sang các định dạng khác như DOCX không?**  
Đ: Có – Aspose.Note có thể xuất ra PDF, DOCX, HTML và một số định dạng ảnh.

**H: Tôi có thể tìm thêm ví dụ và tài liệu API ở đâu?**  
Đ: Truy cập trang tài liệu chính thức của Aspose.Note, khám phá tham chiếu API, và tải bản dùng thử miễn phí để thử nghiệm thực tế.

## Kết luận

Bạn đã có một ví dụ hoàn chỉnh, từ đầu đến cuối, về cách **đặt màu chữ Java**, tô sáng văn bản, điều chỉnh kích thước phông chữ, và **lưu OneNote dưới dạng PDF** bằng Aspose.Note. Hãy tự do tùy chỉnh mã để nhắm tới các trang cụ thể, áp dụng định dạng có điều kiện, hoặc tích hợp vào các pipeline xử lý tài liệu lớn hơn.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2026-01-18  
**Kiểm tra với:** Aspose.Note 24.11 cho Java  
**Tác giả:** Aspose  

---