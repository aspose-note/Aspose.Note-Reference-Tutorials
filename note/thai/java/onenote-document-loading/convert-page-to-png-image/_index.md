---
date: 2025-11-29
description: เรียนรู้วิธีการส่งออกหน้า OneNote เป็น PNG ด้วย Aspose.Note สำหรับ Java.
  ทำตามคำแนะนำทีละขั้นตอนเพื่อกำหนดดัชนีหน้า, แปลงหน้า, และบันทึกรูปภาพ.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: ส่งออกหน้า OneNote เป็นภาพ PNG ใน Java ด้วย Aspose.Note
url: /th/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออกหน้า OneNote เป็นภาพ PNG ด้วย Java โดยใช้ Aspose.Note

## คำนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีส่งออกหน้า OneNote** เป็นภาพ PNG ด้วยไลบรารี Aspose.Note for Java เราจะพาคุณผ่านทุกขั้นตอนตั้งแต่การเตรียมสภาพแวดล้อม การกำหนดดัชนีหน้า ไปจนถึงการบันทึกหน้าเป็นไฟล์ PNG คุณภาพสูง เมื่อจบแล้วคุณจะสามารถเพิ่มความสามารถนี้เข้าไปในแอปพลิเคชัน Java ใด ๆ ที่ทำงานกับเอกสาร OneNote ได้

## คำตอบอย่างรวดเร็ว
- **ต้องใช้ไลบรารีอะไร?** Aspose.Note for Java.  
- **สามารถส่งออกหน้าเดียวได้หรือไม่?** ได้ — ใช้ `setPageIndex` เพื่อระบุหน้าที่ต้องการ.  
- **รูปแบบภาพที่รองรับ?** PNG, JPEG, GIF, BMP, TIFF (ที่แสดงเป็น PNG).  
- **ต้องมีลิขสิทธิ์หรือไม่?** มีรุ่นทดลองฟรี; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง.  
- **ใช้เวลานำไปใช้เท่าไหร่?** ปกติไม่เกิน 10 นาทีสำหรับการแปลงพื้นฐาน.

## “ส่งออกหน้า OneNote” คืออะไร?
การส่งออกหน้า OneNote หมายถึงการแปลงหน้าที่กำหนดภายในเอกสาร `.one` ให้เป็นไฟล์ภาพแยก (PNG ในกรณีนี้) ซึ่งมีประโยชน์เมื่อคุณต้องการแชร์, ฝัง, หรือประมวลผลเนื้อหา OneNote นอกสภาพแวดล้อม OneNote

## ทำไมต้องใช้ Aspose.Note for Java เพื่อแปลง OneNote เป็น PNG?
- **ไม่มีการพึ่งพา Microsoft Office** – ทำงานบนทุกแพลตฟอร์มที่รัน Java.  
- **การควบคุมระดับละเอียด** – สามารถเลือกหน้าใดก็ได้ด้วย `setPageIndex`.  
- **ผลลัพธ์คุณภาพสูง** – PNG รักษากราฟิกเวกเตอร์และความคมของข้อความ.  
- **พร้อมสำหรับการประมวลผลเป็นชุด** – ง่ายต่อการวนลูปผ่านหลายหน้าเพื่อแปลงจำนวนมาก.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอนต่อไปนี้ให้ตรวจสอบว่าคุณมี:

1. **Java Development Kit (JDK)** – รุ่น 8 หรือสูงกว่า.  
2. **Aspose.Note for Java** – ดาวน์โหลด JAR ล่าสุดจาก [เว็บไซต์ Aspose](https://releases.aspose.com/note/java/).  
3. **เอกสาร OneNote** (`.one`) ที่มีหน้าที่คุณต้องการส่งออก.

## นำเข้าแพ็กเกจ

แรกเริ่มให้นำเข้าคลาส Java ที่จำเป็น:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: โหลดเอกสาร OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

เราใช้คลาส `Document` เพื่ออ่านไฟล์ OneNote จากดิสก์ วัตถุ `LoadOptions` สามารถใช้ปรับแต่งพฤติกรรมการโหลดได้หากต้องการ

### ขั้นตอนที่ 2: เริ่มต้น ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` บอก Aspose.Note ว่าเราต้องการผลลัพธ์ในรูปแบบ **PNG** คุณสามารถเปลี่ยนเป็น JPEG, BMP ฯลฯ ได้โดยเปลี่ยนค่า `SaveFormat`

### ขั้นตอนที่ 3: ตั้งค่าดัชนีหน้า (วิธีแปลงหน้า OneNote)

```java
// set page index
opts.setPageIndex(0);
```

เมธอด `setPageIndex` เลือกหน้าที่จะส่งออก การนับหน้าจะเริ่มจาก **0** ดังนั้น `0` คือหน้าที่แรก ปรับค่าตามต้องการเพื่อส่งออกหน้าต่าง ๆ

### ขั้นตอนที่ 4: บันทึกเอกสารเป็น PNG (บันทึก OneNote เป็น PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

การเรียก `save` จะเขียนหน้าที่เลือกเป็นไฟล์ PNG ลงดิสก์ ชื่อไฟล์ `ConvertSpecificPageToPngImage_out.png` เป็นเพียงตัวอย่าง คุณสามารถตั้งชื่อไฟล์ตามที่ต้องการได้

## ปัญหาที่พบบ่อยและเคล็ดลับ

- **ดัชนีหน้าผิด** – จำไว้ว่าการนับเริ่มจาก 0 หากได้ภาพว่างเปล่า ให้ตรวจสอบค่าดัชนี.  
- **ไม่พบ JAR ของ Aspose.Note** – ตรวจสอบให้แน่ใจว่า JAR อยู่ใน classpath; หากไม่จะพบ `ClassNotFoundException`.  
- **หน้าขนาดใหญ่** – สำหรับหน้าที่ใหญ่มาก ควรเพิ่มขนาด heap ของ JVM (`-Xmx`) เพื่อหลีกเลี่ยง `OutOfMemoryError`.

## คำถามที่พบบ่อย

### Q1: สามารถแปลงหลายหน้าเป็นภาพ PNG พร้อมกันได้หรือไม่โดยใช้ Aspose.Note for Java?
A1: ได้ คุณสามารถวนลูปผ่านหน้าต่าง ๆ ของเอกสาร, ตั้งค่า `opts.setPageIndex(i)` แล้วเรียก `save` ในแต่ละรอบ

### Q2: Aspose.Note for Java รองรับรูปแบบภาพอื่นนอกจาก PNG หรือไม่?
A2: รองรับเต็มที่ คุณสามารถตั้งค่า `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` หรือ `SaveFormat.Tiff` ใน `ImageSaveOptions`

### Q3: มีรุ่นทดลองฟรีสำหรับ Aspose.Note for Java หรือไม่?
A3: มี คุณสามารถดาวน์โหลดรุ่นทดลองฟรีจาก [เว็บไซต์](https://releases.aspose.com/)

### Q4: จะได้รับการสนับสนุนทางเทคนิคหากเจอปัญหากับ Aspose.Note for Java หรือไม่?
A4: ได้เลย คุณสามารถขอความช่วยเหลือจากฟอรั่มชุมชน Aspose [ที่นี่](https://forum.aspose.com/c/note/28)

### Q5: จะซื้อไลเซนส์สำหรับ Aspose.Note for Java ได้จากที่ไหน?
A5: คุณสามารถซื้อไลเซนส์ได้จาก [หน้าซื้อขาย](https://purchase.aspose.com/buy)

### Q6: จะส่งออกหน้าที่มีรูปภาพฝังอยู่ได้อย่างไร?
A6: รูปภาพที่ฝังอยู่จะถูกเรนเดอร์โดยอัตโนมัติในไฟล์ PNG; ไม่ต้องเขียนโค้ดเพิ่มเติม

### Q7: สามารถตั้งค่า DPI หรือความละเอียดของภาพได้หรือไม่?
A7: ได้ ใช้ `opts.setResolution(int dpi)` ก่อนเรียก `save` เพื่อควบคุมคุณภาพของผลลัพธ์

---

**อัปเดตล่าสุด:** 2025-11-29  
**ทดสอบด้วย:** Aspose.Note for Java 24.11 (ล่าสุด)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}