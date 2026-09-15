---
date: 2026-03-29
description: Tìm hiểu cách đặt ngôn ngữ cho văn bản trong OneNote bằng Aspose.Note
  cho Java. Hướng dẫn chi tiết này chỉ cho bạn cách tạo tài liệu OneNote, thay đổi
  ngôn ngữ văn bản và lưu tệp OneNote một cách hiệu quả.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Cách đặt ngôn ngữ cho văn bản trong OneNote – Aspose.Note
url: /vi/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Đặt Ngôn Ngữ cho Văn Bản trong OneNote – Aspose.Note

## Giới thiệu
Nếu bạn cần **how to set language** cho các đoạn văn bản cụ thể trong một sổ tay OneNote, Aspose.Note cho Java giúp thực hiện một cách đơn giản. Trong hướng dẫn này, bạn sẽ học cách tạo tài liệu OneNote, thay đổi ngôn ngữ văn bản cho từng từ hoặc cụm từ, và cuối cùng lưu tệp OneNote với ngôn ngữ kiểm tra chính tả đúng được áp dụng. Khi kết thúc, bạn sẽ hiểu vì sao việc đặt ngôn ngữ quan trọng đối với kiểm tra chính tả và bản địa hoá, và bạn sẽ có một mẫu mã sẵn sàng chạy.

## Câu trả lời nhanh
- **What does “set language” affect?** Nó cho OneNote biết từ điển kiểm tra chính tả nào sẽ được sử dụng cho việc kiểm tra chính tả và ngữ pháp.  
- **Can I set different languages in the same note?** Có, bạn có thể gán một ngôn ngữ cho mỗi đoạn văn bản.  
- **Do I need a license for Aspose.Note?** Bản dùng thử miễn phí hoạt động cho việc thử nghiệm; giấy phép thương mại là bắt buộc cho môi trường sản xuất.  
- **Which Java versions are supported?** Aspose.Note cho Java hỗ trợ Java 8 và các phiên bản mới hơn.  
- **Is the output a .one file?** Có, tài liệu được lưu dưới dạng tệp OneNote *.one*.

## Yêu cầu trước
Trước khi bắt đầu với mã, hãy chắc chắn rằng bạn có những thứ sau:

1. **Java Development Environment** – JDK 8 hoặc cao hơn đã được cài đặt và cấu hình.  
2. **Aspose.Note for Java Library** – Tải xuống và cài đặt thư viện từ [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Tạo một thư mục trên máy của bạn để lưu tệp OneNote được tạo.

## Tại sao cần đặt ngôn ngữ cho văn bản trong OneNote?
Việc đặt ngôn ngữ kiểm tra giúp đảm bảo rằng kiểm tra chính tả, đề xuất ngữ pháp và lập chỉ mục tìm kiếm hoạt động chính xác cho nội dung đa ngôn ngữ. Điều này đặc biệt hữu ích cho:

- **Global teams** hợp tác trên một sổ tay duy nhất.  
- **Localized documentation** nơi mỗi phần có thể ở một ngôn ngữ khác nhau.  
- **Data‑driven applications** tạo ghi chú một cách tự động cho người dùng trên toàn thế giới.

## Nhập Gói
Bắt đầu bằng cách nhập các lớp Aspose.Note cần thiết và các tiện ích Java.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Bước 1: Thiết lập Tài liệu và Trang
Tạo một tài liệu OneNote mới và một trang sẽ chứa nội dung của bạn. Bước này cũng minh họa **create OneNote document**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Bước 2: Tạo Outline và Phần tử Outline
Outline là container cho nội dung sổ tay. Ở đây chúng ta xây dựng cấu trúc sẽ chứa văn bản theo ngôn ngữ sau này.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Bước 3: Thêm Rich Text với Cài đặt Ngôn ngữ
Bây giờ chúng ta **change text language** bằng cách gắn một `TextStyle` với một `Locale` cụ thể vào mỗi đoạn văn bản. Điều này minh họa **set language for text**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Bước 4: Tổ chức Các Phần tử và Lưu
Ghép nối cấu trúc outline, gắn nó vào trang, và cuối cùng **save OneNote file** với các cài đặt ngôn ngữ đã được áp dụng.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Những Sai Lầm Thường Gặp & Mẹo
- **Locale format** – Sử dụng thẻ IETF BCP‑47 (ví dụ, `en-US`, `de-DE`). Thẻ không đúng sẽ mặc định về ngôn ngữ của tài liệu.  
- **File path** – Đảm bảo `dataDir` trỏ tới một thư mục tồn tại; nếu không, `document.save` sẽ ném ra một `IOException`.  
- **Pro tip:** Nếu bạn cần đặt ngôn ngữ cho toàn bộ đoạn văn, áp dụng `TextStyle` vào `ParagraphStyle` thay vì mỗi lần gọi `append`.

## Kết luận
Bạn vừa học được **how to set language** cho các đoạn văn bản riêng lẻ trong một sổ tay OneNote bằng cách sử dụng Aspose.Note cho Java. Khả năng này cho phép bạn **create OneNote document** một cách lập trình, **change text language** ngay lập tức, và **save OneNote file** với siêu dữ liệu kiểm tra chính tả chính xác.

## Câu hỏi thường gặp

**Q: Tôi có thể đặt ngôn ngữ kiểm tra cho các ngôn ngữ khác không được đề cập trong ví dụ không?**  
A: Chắc chắn! Thêm các lời gọi `append` bổ sung với `Locale.forLanguageTag("xx-XX")` mong muốn.

**Q: Aspose.Note cho Java có tương thích với các phiên bản Java mới nhất không?**  
A: Có, thư viện được cập nhật thường xuyên để hỗ trợ các phiên bản Java mới nhất.

**Q: Làm thế nào tôi có thể xử lý lỗi trong quá trình đặt ngôn ngữ?**  
A: Bao quanh thao tác lưu trong một khối `try‑catch` để bắt `IOException` hoặc `AsposeException`.

**Q: Tôi có thể tích hợp mã này vào một ứng dụng web không?**  
A: Chắc chắn. Chỉ cần bao gồm JAR Aspose.Note vào classpath của dự án web và đảm bảo máy chủ có quyền ghi vào thư mục đích.

**Q: Tôi có thể tìm các ví dụ và tài liệu bổ sung cho Aspose.Note cho Java ở đâu?**  
A: Khám phá [documentation](https://reference.aspose.com/note/java/) để xem danh sách đầy đủ các API và dự án mẫu.

---

**Cập nhật lần cuối:** 2026-03-29  
**Kiểm tra với:** Aspose.Note for Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}