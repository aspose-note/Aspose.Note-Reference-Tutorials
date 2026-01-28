---
date: 2026-01-28
description: Tìm hiểu cách chuyển OneNote sang PDF và quản lý giấy phép tính theo
  mức trong Java bằng Aspose.Note. Kiểm soát việc sử dụng, theo dõi tín dụng và giữ
  chi phí thấp.
linktitle: Manage Metered License for OneNote in Java
second_title: Aspose.Note Java API
title: Chuyển đổi OneNote sang PDF và Quản lý Giấy phép Định mức trong Java
url: /vi/java/licensing-java/manage-metered-license/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi OneNote sang PDF và Quản lý Giấy phép Định mức trong Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá cách **chuyển đổi OneNote sang PDF** đồng thời sử dụng giấy phép định mức với thư viện Aspose.Note cho Java. Giấy phép định mức cho phép bạn theo dõi việc tiêu thụ tín dụng theo thời gian thực, mang lại sự linh hoạt để chỉ trả tiền cho những gì bạn sử dụng. Chúng tôi sẽ hướng dẫn toàn bộ quy trình — từ việc thiết lập các khóa giấy phép, tải tệp OneNote, chuyển đổi sang PDF, cho đến việc kiểm tra mức tiêu thụ tín dụng của bạn.

## Câu trả lời nhanh
- **“chuyển đổi OneNote sang PDF” có nghĩa là gì?** Nó biến một tệp .one thành tài liệu PDF di động.  
- **Thư viện nào thực hiện việc chuyển đổi?** Aspose.Note cho Java cung cấp API đơn giản cho nhiệm vụ này.  
- **Tôi có cần giấy phép để chuyển đổi không?** Có, giấy phép định mức là bắt buộc cho môi trường sản xuất.  
- **Làm sao tôi có thể giám sát việc sử dụng?** Sử dụng `Metered.getConsumptionCredit()` và `Metered.getConsumptionQuantity()`.  
- **Có cần thiết lập bổ sung nào không?** Chỉ cần một Java JDK và tệp JAR Aspose.Note.

## Convert OneNote sang PDF là gì?

Việc chuyển đổi OneNote sang PDF tạo ra một bản đại diện tĩnh, được hỗ trợ rộng rãi cho các trang sổ ghi chú của bạn. PDF lý tưởng cho việc chia sẻ, in ấn hoặc lưu trữ vì chúng giữ nguyên bố cục, phông chữ và hình ảnh trên mọi nền tảng.

## Tại sao nên sử dụng giấy phép định mức cho việc chuyển đổi này?

Giấy phép định mức tính phí dựa trên mức tiêu thụ tín dụng thực tế thay vì mức phí cố định. Mô hình này hoàn hảo khi bạn có nhu cầu chuyển đổi không thường xuyên hoặc muốn duy trì chi phí dự đoán được trong khi vẫn tận dụng toàn bộ sức mạnh của Aspose.Note.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

1. **Java Development Kit (JDK)** – bất kỳ phiên bản mới nào (khuyến nghị JDK 11+). Tải về từ [đây](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Thư viện Aspose.Note cho Java** – lấy tệp JAR mới nhất từ [trang web chính thức](https://releases.aspose.com/note/java/).  

> **Mẹo chuyên nghiệp:** Thêm JAR Aspose.Note vào classpath của dự án hoặc sử dụng công cụ xây dựng như Maven/Gradle để quản lý phụ thuộc.

## Nhập các gói

Đầu tiên, nhập các lớp cần thiết. Giữ khối này chính xác như đã hiển thị — không thay đổi bất kỳ đoạn mã nào.

```java
import com.aspose.note.Document;
import com.aspose.note.Metered;



import java.nio.file.Paths;
```

## Bước 1: Thiết lập Giấy phép Định mức

```java
Metered metered = new Metered();
metered.setMeteredKey("MyPublicKey", "MyPrivateKey");
```

Ở đây chúng ta tạo một đối tượng `Metered` và chèn các khóa công khai/riêng tư bạn nhận được từ Aspose. Bước này kích hoạt chế độ giấy phép định mức cho tất cả các thao tác tiếp theo, bao gồm cả lời gọi **chuyển đổi OneNote sang PDF**.

## Bước 2: Tải tài liệu OneNote và chuyển đổi sang PDF

```java
String dataDir = "Your Document Directory";
Document doc = new Document(Paths.get(dataDir,"Sample1.one").toString());
doc.save(Paths.get(dataDir,"MeteredLicense.pdf").toString());
```

- **Tải**: `Document` đọc tệp `.one` nằm trong `dataDir`. Đây là cách truyền thống để **tải tài liệu OneNote** để xử lý.  
- **Chuyển đổi & Lưu**: Gọi `save` với phần mở rộng `.pdf` sẽ tự động **chuyển đổi .one sang .pdf**. Thao tác này cũng **lưu PDF từ OneNote** trong cùng thư mục. Thay `"Your Document Directory"` bằng đường dẫn thực tế trên máy của bạn.

## Bước 3: Kiểm tra tiêu thụ tín dụng Trước và Sau khi chuyển đổi

```java
System.out.println(String.format("Credit before operation: %.02f", Metered.getConsumptionCredit()));
System.out.println(String.format("Consumption quantity before operation: %.02f", Metered.getConsumptionQuantity()));
```

Hai dòng này in ra số dư tín dụng còn lại và lượng tín dụng đã dùng cho việc chuyển đổi. Khi chạy các lệnh này sau thao tác `save`, bạn sẽ thấy giá trị cập nhật, giúp xác nhận rằng giấy phép định mức đang theo dõi việc sử dụng một cách chính xác.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|----------|
| **Khóa định mức không hợp lệ** | Khóa bị gõ sai hoặc đã hết hạn. | Kiểm tra lại các khóa từ tài khoản Aspose; tạo lại nếu cần. |
| **Không tìm thấy tệp** | Đường dẫn `dataDir` không đúng. | Sử dụng đường dẫn tuyệt đối hoặc xác minh đường dẫn tương đối từ thư mục gốc dự án. |
| **Không đủ tín dụng** | Đã tiêu hết tất cả tín dụng. | Mua thêm tín dụng hoặc chuyển sang giấy phép vĩnh viễn cho khối lượng công việc lớn. |

## Câu hỏi thường gặp

**H: Giấy phép định mức là gì?**  
Đ: Giấy phép định mức cho phép bạn trả tiền cho việc sử dụng API dựa trên tín dụng, cung cấp kiểm soát chi phí chi tiết.

**H: Làm sao để lấy khóa định mức cho sản phẩm Aspose?**  
Đ: Mua giấy phép từ trang web Aspose hoặc yêu cầu khóa đánh giá tạm thời qua bảng điều khiển tài khoản của bạn.

**H: Tôi có thể sử dụng giấy phép định mức cho nhiều ứng dụng không?**  
Đ: Có, nhưng mọi tiêu thụ sẽ được tổng hợp dưới cùng một khóa, vì vậy hãy giám sát tổng mức sử dụng cẩn thận.

**H: Có bản dùng thử miễn phí cho Aspose.Note cho Java không?**  
Đ: Có, bạn có thể tải bản dùng thử miễn phí từ [đây](https://releases.aspose.com/).

**H: Tôi có thể nhận hỗ trợ cho Aspose.Note cho Java ở đâu?**  
Đ: Đặt câu hỏi trên diễn đàn cộng đồng Aspose [tại đây](https://forum.aspose.com/c/note/28).

## Kết luận

Bạn đã có một quy trình hoàn chỉnh, sẵn sàng cho môi trường sản xuất để **chuyển đổi OneNote sang PDF** đồng thời quản lý giấy phép định mức trong Java. Bằng cách kiểm tra tiêu thụ tín dụng trước và sau khi chuyển đổi, bạn có thể đảm bảo ứng dụng của mình luôn nằm trong ngân sách và mở rộng hiệu quả.

---

**Cập nhật lần cuối:** 2026-01-28  
**Được kiểm tra với:** Aspose.Note cho Java 24.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}