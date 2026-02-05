---
date: 2026-02-05
description: เรียนรู้วิธีส่งออกหน้าของ OneNote และบันทึก OneNote เป็นรูปภาพ คู่มือนี้แสดงวิธีแปลงไฟล์
  .one เป็น PNG ตั้งค่าดัชนีหน้า และส่งออกภาพหน้าของ OneNote โดยใช้ Aspose.Note สำหรับ
  Java.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: วิธีส่งออกหน้า OneNote เป็นภาพ PNG ใน Java ด้วย Aspose.Note
url: /th/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออกหน้า OneNote เป็นภาพ PNG ใน Java ด้วย Aspose.Note

## บทนำ

ในบทเรียนนี้คุณจะได้ค้นพบ **วิธีส่งออกหน้า OneNote** เป็นภาพ PNG โดยใช้ไลบรารี Aspose.Note สำหรับ Java. **วิธีส่งออก onenote** เป็นความต้องการทั่วไปเมื่อคุณต้องการแชร์โน้ตนอกระบบนิเวศของ OneNote, ฝังลงในรายงาน, หรือประมวลผลด้วยเครื่องมือการประมวลผลภาพ. เราจะอธิบายทุกขั้นตอนที่คุณต้องการ—ตั้งแต่การเตรียมสภาพแวดล้อม, การตั้งค่าดัชนีหน้า, การแปลงหน้า, และการบันทึกผลลัพธ์เป็นไฟล์ PNG คุณภาพสูง. เมื่อเสร็จสิ้นคุณจะสามารถ **บันทึก onenote เป็นภาพ** ในแอปพลิเคชัน Java ใดก็ได้.

## คำตอบสั้น

- **ไลบรารีที่ต้องการคืออะไร?** Aspose.Note for Java.  
- **ฉันสามารถส่งออกหน้าเดียวได้หรือไม่?** ใช่—ใช้ `setPageIndex` เพื่อเลือกหน้าที่ต้องการ.  
- **รูปแบบภาพที่รองรับ?** PNG, JPEG, GIF, BMP, TIFF (ที่นี่แสดง PNG).  
- **ต้องการไลเซนส์หรือไม่?** มีรุ่นทดลองฟรี; ต้องมีไลเซนส์สำหรับการใช้งานจริง.  
- **การดำเนินการใช้เวลานานเท่าไหร่?** ปกติใช้เวลาน้อยกว่า 10 นาทีสำหรับการแปลงพื้นฐาน.  
- **วิธีแปลง .one เป็น png?** โหลดไฟล์ `.one` ด้วย `Document`, ตั้งค่าดัชนีหน้า, และบันทึกด้วย `ImageSaveOptions`.  

## “ส่งออกหน้า OneNote” คืออะไร?

การส่งออกหน้า OneNote หมายถึงการแปลงหน้าที่เฉพาะภายในเอกสาร `.one` ให้เป็นไฟล์ภาพแยก (PNG ในกรณีนี้). สิ่งนี้มีประโยชน์เมื่อคุณต้องการ **ส่งออกภาพหน้า onenote** เพื่อแชร์, ฝัง, หรือทำการวิเคราะห์ต่อด้วยภาพ.

## ทำไมต้องใช้ Aspose.Note สำหรับ Java เพื่อแปลง OneNote เป็น PNG?

- **ไม่มีการพึ่งพา Microsoft Office** – ทำงานบนแพลตฟอร์มใดก็ได้ที่รัน Java.  
- **การควบคุมระดับละเอียด** – คุณสามารถเลือกหน้าใดก็ได้ผ่าน `setPageIndex`.  
- **ผลลัพธ์คุณภาพสูง** – PNG รักษากราฟิกเวกเตอร์และความคมชัดของข้อความ.  
- **พร้อมสำหรับการประมวลผลเป็นชุด** – ง่ายต่อการวนลูปผ่านหน้าเพื่อการแปลงจำนวนมาก, ทำให้การ **แปลง onenote เป็น png** หลายหน้าในครั้งเดียวเป็นเรื่องง่าย.  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, ตรวจสอบว่าคุณมี:

1. **Java Development Kit (JDK)** – เวอร์ชัน 8 หรือสูงกว่า.  
2. **Aspose.Note for Java** – ดาวน์โหลด JAR ล่าสุดจาก [Aspose website](https://releases.aspose.com/note/java/).  
3. **เอกสาร OneNote** (`.one`) ที่มีหน้าที่คุณต้องการส่งออก.  

## นำเข้าแพ็กเกจ

ขั้นแรก, นำเข้าคลาส Java ที่จำเป็น:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

การนำเข้าดังกล่าวทำให้คุณเข้าถึง API หลักของ Aspose.Note, รวมถึงการโหลดเอกสารและการกำหนดค่าตัวเลือกการบันทึกภาพ.

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: โหลดเอกสาร OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

เราใช้คลาส `Document` เพื่ออ่านไฟล์ OneNote จากดิสก์. อ็อบเจ็กต์ `LoadOptions` ให้คุณปรับแต่งพฤติกรรมการโหลดตามต้องการ. ขั้นตอนนี้เป็นพื้นฐานสำหรับ **convert .one to png**.

### ขั้นตอนที่ 2: เริ่มต้น ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` บอก Aspose.Note ว่าเราต้องการผลลัพธ์ในรูปแบบ **PNG**. คุณสามารถเปลี่ยนเป็น JPEG, BMP, ฯลฯ ได้โดยเปลี่ยน `SaveFormat`. อ็อบเจ็กต์นี้ยังให้คุณควบคุม DPI, ความลึกสี, และการตั้งค่าเฉพาะภาพอื่น ๆ.

### ขั้นตอนที่ 3: ตั้งค่าดัชนีหน้า (วิธีแปลงหน้า OneNote)

```java
// set page index
opts.setPageIndex(0);
```

เมธอด `setPageIndex` เลือกหน้าที่จะส่งออก. การนับหน้าจะเริ่มที่ **0**, ดังนั้น `0` หมายถึงหน้าที่แรก. ปรับค่าตัวนี้เพื่อ **ส่งออกหน้าที่แตกต่าง** หรือวนลูปผ่านหน้าเมื่อคุณต้องการ **บันทึก onenote เป็นภาพ** สำหรับแต่ละหน้า.

### ขั้นตอนที่ 4: บันทึกเอกสารเป็น PNG (บันทึก OneNote เป็น PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

การเรียก `save` จะเขียนหน้าที่เลือกลงในไฟล์ PNG บนดิสก์. ชื่อไฟล์ `ConvertSpecificPageToPngImage_out.png` เป็นเพียงตัวอย่าง—คุณสามารถตั้งชื่อตามต้องการ. ขั้นตอนสุดท้ายนี้ **exports onenote page image** พร้อมใช้ในรายงาน, หน้าเว็บ, หรือการประมวลผลต่อ.

## ปัญหาทั่วไปและเคล็ดลับ

- **ดัชนีหน้าผิด** – จำไว้ว่าการนับเริ่มที่ 0. หากได้ภาพว่าง, ตรวจสอบค่าดัชนี.  
- **ไม่มีไฟล์ JAR ของ Aspose.Note** – ตรวจสอบให้แน่ใจว่า JAR อยู่ใน classpath; มิฉะนั้นคุณจะเจอ `ClassNotFoundException`.  
- **หน้าขนาดใหญ่** – สำหรับหน้าที่ใหญ่มาก, พิจารณาเพิ่มขนาด heap ของ JVM (`-Xmx`) เพื่อหลีกเลี่ยง `OutOfMemoryError`.  
- **การควบคุมความละเอียด** – ใช้ `opts.setResolution(300)` (หรือ DPI ที่ต้องการ) ก่อนเรียก `save` เพื่อเพิ่มความคมชัดของภาพ.  

## คำถามที่พบบ่อย

### Q1: ฉันสามารถแปลงหลายหน้เป็นภาพ PNG พร้อมกันได้หรือไม่โดยใช้ Aspose.Note สำหรับ Java?

A1: ใช่, คุณสามารถวนลูปผ่านหน้าของเอกสาร, อัปเดต `opts.setPageIndex(i)`, และเรียก `save` ในแต่ละรอบ.

### Q2: Aspose.Note สำหรับ Java รองรับรูปแบบภาพอื่นนอกจาก PNG หรือไม่?

A2: แน่นอน. คุณสามารถตั้งค่า `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp`, หรือ `SaveFormat.Tiff` ใน `ImageSaveOptions`.

### Q3: มีรุ่นทดลองฟรีสำหรับ Aspose.Note สำหรับ Java หรือไม่?

A3: มี, คุณสามารถดาวน์โหลดรุ่นทดลองฟรีจาก [website](https://releases.aspose.com/).

### Q4: ฉันสามารถขอความช่วยเหลือด้านเทคนิคได้หรือไม่หากเจอปัญหากับ Aspose.Note สำหรับ Java?

A4: แน่นอน, คุณสามารถขอรับการสนับสนุนจากฟอรั่มชุมชน Aspose [ที่นี่](https://forum.aspose.com/c/note/28).

### Q5: ฉันสามารถซื้อไลเซนส์สำหรับ Aspose.Note สำหรับ Java ได้จากที่ไหน?

A5: คุณสามารถซื้อไลเซนส์ได้จาก [purchase page](https://purchase.aspose.com/buy).

### Q6: ฉันจะส่งออกหน้าที่มีภาพฝังอยู่ได้อย่างไร?

A6: ภาพที่ฝังอยู่จะถูกเรนเดอร์โดยอัตโนมัติในผลลัพธ์ PNG; ไม่ต้องเขียนโค้ดเพิ่มเติม.

### Q7: ฉันสามารถตั้งค่า DPI หรือความละเอียดของภาพได้หรือไม่?

A7: ใช่, ใช้ `opts.setResolution(int dpi)` ก่อนเรียก `save` เพื่อควบคุมคุณภาพของผลลัพธ์.

---

**อัปเดตล่าสุด:** 2026-02-05  
**ทดสอบกับ:** Aspose.Note for Java 24.11 (latest)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}