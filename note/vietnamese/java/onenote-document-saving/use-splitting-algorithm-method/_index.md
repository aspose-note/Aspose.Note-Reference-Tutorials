---
date: 2025-12-18
description: Tìm hiểu cách xuất các trang OneNote sang PDF bằng Aspose.Note cho Java.
  Chọn thuật toán chia tách, thiết lập việc chia trang và tạo các tệp PDF một cách
  dễ dàng.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Xuất các trang OneNote bằng phương pháp thuật toán phân tách – Aspose.Note
url: /vi/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất Trang OneNote bằng Phương Pháp Thuật Toán Phân Tách – Aspose.Note

## Giới thiệu

Nếu bạn cần **export OneNote pages** sang tài liệu PDF một cách lập trình, Aspose.Note for Java giúp thực hiện một cách đơn giản. Trong hướng dẫn này, chúng tôi sẽ trình bày Phương Pháp Thuật Toán Phân Tách, cho phép bạn kiểm soát cách nội dung được chia qua các trang, đảm bảo đầu ra PDF sạch sẽ và dễ đọc. Bạn sẽ thấy cách thiết lập các tùy chọn lưu PDF, chọn thuật toán phân tách trang phù hợp, và cuối cùng tạo file PDF—chỉ với vài dòng mã Java.

## Câu trả lời nhanh
- **What does the Splitting Algorithm do?** Nó xác định cách các đối tượng vượt qua ranh giới trang được xử lý khi xuất OneNote pages sang PDF.  
- **Which library is required?** Aspose.Note for Java (tải xuống từ trang chính thức của Aspose).  
- **Do I need a license?** Cần có giấy phép tạm thời hoặc đầy đủ cho việc sử dụng trong môi trường sản xuất; bản dùng thử miễn phí có sẵn.  
- **Can I export large OneNote notebooks?** Có – thư viện xử lý hiệu quả các tệp lớn và cho phép bạn thiết lập quy tắc phân tách trang.  
- **What output formats are supported?** PDF, JPEG, PNG, XPS và các định dạng khác; hướng dẫn này tập trung vào xuất PDF.

## **export onenote pages** là gì?
Xuất OneNote pages có nghĩa là chuyển đổi định dạng tệp gốc `.one` sang một định dạng di động hơn như PDF. Điều này hữu ích cho việc chia sẻ, lưu trữ hoặc in nội dung mà không cần ứng dụng OneNote.

## Tại sao nên sử dụng Thuật Toán Phân Tách cho **export onenote pages**?
Thuật toán cho phép bạn kiểm soát chi tiết cách các đối tượng phức tạp (bảng, hình ảnh, bản vẽ) được xử lý tại các ngắt trang. Bằng cách chọn thuật toán phù hợp, bạn có thể:

* Bảo tồn bố cục trực quan của mỗi trang.  
* Tránh nội dung bị cắt ở ranh giới trang.  
* Giảm số lượng trang tạo ra khi các đối tượng có thể được di chuyển sang trang tiếp theo một cách sạch sẽ.  

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có các yêu cầu sau:

1. Java Development Kit (JDK): Đảm bảo bạn đã cài đặt JDK trên hệ thống. Bạn có thể tải xuống từ [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Thư viện Aspose.Note cho Java: Tải xuống và cài đặt thư viện Aspose.Note cho Java từ [download link](https://releases.aspose.com/note/java/).

## Nhập Gói

Trong dự án Java của bạn, nhập các gói cần thiết để sử dụng các tính năng của Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Bước 1: Xác định Thư mục Tài liệu

Thiết lập thư mục chứa tài liệu OneNote của bạn.

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tải Tài liệu OneNote

Tải tài liệu OneNote bằng cách sử dụng lớp `Document` của Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Bước 3: Thiết lập Tùy chọn Lưu PDF

Tạo một thể hiện của `PdfSaveOptions` để chỉ định các tùy chọn khi lưu tài liệu dưới dạng PDF. Đây là nơi bạn **set page splitting** hành vi và các cài đặt liên quan đến PDF khác.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Bước 4: Thiết lập Thuật Toán Phân Tách Trang

Chọn thuật toán phân tách phù hợp theo yêu cầu của bạn. Ở đây, chúng tôi sử dụng `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, thuật toán giữ một phần của đối tượng trên trang hiện tại và sao chép phần còn lại sang trang tiếp theo.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Bước 5: Lưu Tài liệu

Lưu tài liệu với các tùy chọn lưu PDF đã chỉ định. Bước này **generates PDF onenote** đầu ra mà bạn có thể mở, chia sẻ hoặc in.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Các vấn đề thường gặp và giải pháp

| Issue | Solution |
|-------|----------|
| **Các đối tượng bị cắt ở ranh giới trang** | Thử một thuật toán khác như `AlwaysSplitObjectsAlgorithm` hoặc tăng giá trị ngưỡng trong `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **PDF xuất ra rỗng** | Kiểm tra xem tệp `.one` nguồn có bị hỏng không và đường dẫn `dataDir` có đúng không. |
| **Hiệu năng chậm khi xử lý sổ tay lớn** | Sử dụng `pdfSaveOptions.setCompressImages(true)` để giảm sử dụng bộ nhớ, và cân nhắc xử lý sổ tay thành các phần nhỏ hơn. |

## Câu hỏi thường gặp

**Q: Can I use Aspose.Note for Java with other programming languages?**  
A: Có, Aspose.Note cũng có sẵn cho .NET, C++, và Python.

**Q: Is Aspose.Note suitable for processing large OneNote files?**  
A: Chắc chắn. Thư viện được tối ưu để xử lý các sổ tay lớn một cách hiệu quả.

**Q: Where can I find additional resources and support for Aspose.Note?**  
A: Bạn có thể tham khảo [documentation](https://reference.aspose.com/note/java/) và [forum](https://forum.aspose.com/c/note/28) để được hỗ trợ và hướng dẫn.

**Q: Can I try Aspose.Note before purchasing?**  
A: Có, bạn có thể sử dụng một [free trial](https://releases.aspose.com/) để khám phá các tính năng trước khi mua.

**Q: How can I obtain a temporary license for Aspose.Note?**  
A: Bạn có thể yêu cầu một [temporary license](https://purchase.aspose.com/temporary-license/) để đánh giá sản phẩm trong thời gian dùng thử.

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}