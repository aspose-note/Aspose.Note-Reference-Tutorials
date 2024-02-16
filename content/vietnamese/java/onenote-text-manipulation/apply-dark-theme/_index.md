---
title: Áp dụng chủ đề tối cho văn bản trong OneNote - Aspose.Note
linktitle: Áp dụng chủ đề tối cho văn bản trong OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Khám phá các bước đơn giản để áp dụng chủ đề tối cho văn bản OneNote của bạn bằng Aspose.Note for Java. Nâng cao trải nghiệm tài liệu kỹ thuật số của bạn một cách dễ dàng.
type: docs
weight: 11
url: /vi/java/onenote-text-manipulation/apply-dark-theme/
---
## Giới thiệu
Trong bối cảnh tài liệu kỹ thuật số ngày càng phát triển, tính thẩm mỹ của ghi chú của bạn có thể tác động đáng kể đến khả năng đọc và trải nghiệm người dùng. Một khía cạnh đáng chú ý là việc triển khai chủ đề tối, mang lại một môi trường thoải mái và hấp dẫn về mặt hình ảnh. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình áp dụng chủ đề tối cho văn bản trong OneNote bằng Aspose.Note cho Java.
## Điều kiện tiên quyết
Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:
-  Aspose.Note for Java: Tải xuống và cài đặt thư viện Aspose.Note for Java từ[đây](https://releases.aspose.com/note/java/).
- Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt Java trên máy của mình.
- Môi trường phát triển tích hợp (IDE): Chọn một IDE như Eclipse hoặc IntelliJ để phát triển liền mạch.
## Gói nhập khẩu
Để bắt đầu, hãy nhập các gói cần thiết vào dự án Java của bạn:
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
```
## Bước 1: Đặt màu nền trang
```java
// Đường dẫn đến thư mục tài liệu.
String dataDir = "Your Document Directory";
// Tải tài liệu vào Aspose.Note.
Document doc = new Document(Paths.get(dataDir, "Aspose.one").toString());
for (Page page: doc)
{
    page.setBackgroundColor(Color.BLACK);
}
```
## Bước 2: Điều chỉnh màu văn bản
```java
for (RichText node: doc.getChildNodes(RichText.class))
{
    Color c = node.getParagraphStyle().getFontColor();
    if (c.getAlpha() <= 10 || Math.abs(c.getRed() - Color.BLACK.getRed()) + Math.abs(c.getGreen() - Color.BLACK.getGreen()) + Math.abs(c.getBlue() - Color.BLACK.getBlue()) <= 30)
    {
        node.getParagraphStyle().setFontColor(Color.WHITE);
    }
}
```
## Bước 3: Lưu tài liệu
```java
doc.save(Paths.get(dataDir, "AsposeDarkTheme.pdf").toString());
```
Lặp lại các bước này cho từng tài liệu và bạn sẽ áp dụng thành công chủ đề tối cho văn bản OneNote của mình bằng Aspose.Note for Java.
## Phần kết luận
Tóm lại, việc nâng cao sự hấp dẫn trực quan cho các ghi chú kỹ thuật số của bạn thật đơn giản với Aspose.Note dành cho Java. Bằng cách làm theo hướng dẫn từng bước này, bạn có thể dễ dàng áp dụng chủ đề tối cho văn bản trong OneNote, nâng cao trải nghiệm tài liệu của bạn.
## Câu hỏi thường gặp
### Tôi có thể chỉ áp dụng chủ đề tối cho các phần cụ thể không?
Có, bạn có thể sửa đổi mã để áp dụng chủ đề tối một cách có chọn lọc cho các phần cụ thể trong tài liệu của mình.
### Có các chủ đề tối được xác định trước trong Aspose.Note cho Java không?
Tính đến thời điểm hiện tại, Aspose.Note for Java cho phép bạn tùy chỉnh các chủ đề nhưng không có chủ đề tối được xác định trước.
### Aspose.Note for Java có hỗ trợ các định dạng tài liệu khác không?
Có, Aspose.Note for Java hỗ trợ nhiều định dạng tài liệu khác nhau, bao gồm PDF, DOCX và HTML.
### Có phiên bản dùng thử cho Aspose.Note cho Java không?
 Có, bạn có thể truy cập phiên bản dùng thử miễn phí[đây](https://releases.aspose.com/).
### Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.Note cho Java?
 Tham quan[Diễn đàn Aspose.Note](https://forum.aspose.com/c/note/28) để được hỗ trợ cộng đồng hoặc khám phá các tùy chọn hỗ trợ cao cấp[đây](https://purchase.aspose.com/temporary-license/).