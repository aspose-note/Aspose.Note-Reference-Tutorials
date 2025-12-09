---
date: 2025-11-29
description: เรียนรู้วิธีส่งออกหน้าของ OneNote เป็นภาพโดยใช้ Java และค้นหาวิธีแปลงภาพหน้าของ
  OneNote ด้วย Aspose.Note ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อการผสานรวมอย่างรวดเร็ว
linktitle: How to Export OneNote Page to Image Using Java
second_title: Aspose.Note Java API
title: วิธีส่งออกหน้า OneNote เป็นภาพโดยใช้ Java
url: /th/java/onenote-document-loading/convert-page-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีส่งออกหน้า OneNote เป็นภาพโดยใช้ Java

## บทนำ

ในบทแนะนำนี้ คุณจะได้เรียนรู้ **วิธีส่งออกหน้า OneNote** เป็นไฟล์ภาพโดยใช้ Java กับ Aspose.Note การแปลงหน้า OneNote เป็นภาพเป็นประโยชน์เมื่อคุณต้องฝังเนื้อหาโน้ตบุ๊กลงในรายงาน, แชร์ภาพหน้าจอให้ผู้ที่ไม่ได้ใช้ OneNote, หรือสร้างรูปย่อสำหรับระบบจัดการเอกสาร เราจะเดินผ่านแต่ละขั้นตอน, อธิบายว่าทำไมบรรทัดโค้ดแต่ละบรรทัดจึงสำคัญ, และแสดงวิธีปรับแต่งผลลัพธ์

## คำตอบอย่างรวดเร็ว
- **ต้องใช้ไลบรารีอะไร?** Aspose.Note for Java  
- **สามารถเลือกฟอร์แมตของภาพได้หรือไม่?** ได้ – JPEG, PNG, BMP ฯลฯ ผ่าน `ImageSaveOptions`  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีลิขสิทธิ์ Aspose.Note ที่ถูกต้องสำหรับการใช้งานเชิงพาณิชย์  
- **สามารถส่งออกหน้าใดได้บ้าง?** หน้าใดก็ได้โดยตั้งค่า `PageIndex` (เริ่มจากศูนย์)  
- **การแปลงใช้เวลานานแค่ไหน?** ปกติใช้เวลาน้อยกว่าวินาทีสำหรับหน้าแบบมาตรฐาน

## การส่งออกหน้า OneNote เป็นภาพคืออะไร?
การส่งออกหน้า OneNote หมายถึงการเรนเดอร์เนื้อหาที่หลากหลายของหน้า—ข้อความ, การวาด, ตาราง—เป็นไฟล์ภาพคงที่ (เช่น JPEG) กระบวนการนี้สร้างการแสดงผลภาพที่พกพาได้ซึ่งสามารถแสดงได้ทุกที่ แม้ในที่ที่ไม่มีไคลเอนต์ OneNote ติดตั้งอยู่

## ทำไมต้องใช้ Aspose.Note สำหรับการแปลงหน้า OneNote?
- **ความแม่นยำเต็มรูปแบบ** – รักษาเลย์เอาต์, ฟอนต์, และเส้นหมึก  
- **ไม่ต้องพึ่งพา Microsoft Office** – ทำงานบนแพลตฟอร์มใดก็ได้ที่รองรับ Java  
- **การควบคุมระดับละเอียด** – เลือกฟอร์แมตของภาพ, คุณภาพ, และดัชนีหน้าที่ต้องการ  
- **ขยายได้** – เหมาะสำหรับการประมวลผลหลายหน้าพร้อมกัน

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

1. **Java Development Kit (JDK)** – ติดตั้ง JDK 11 หรือใหม่กว่า คุณสามารถดาวน์โหลดได้จาก [เว็บไซต์อย่างเป็นทางการของ Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) หากยังไม่มี  
2. **Aspose.Note for Java** – รับไลบรารีล่าสุดจาก [หน้าดาวน์โหลด Aspose.Note](https://releases.aspose.com/note/java/) แล้วเพิ่มไฟล์ JAR ไปยัง classpath ของโปรเจกต์ของคุณ

## นำเข้าแพ็กเกจ

ก่อนอื่น ให้เรานำเข้าแพ็กเกจที่จำเป็นเพื่อให้เข้าถึงการจัดการเอกสารและตัวเลือกการบันทึกภาพ

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

เราจะเริ่มโดยการโหลดไฟล์ `.one` เข้าไปยังอ็อบเจ็กต์ `Aspose.Note` `Document`

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **เคล็ดลับ:** ใช้เส้นทางแบบเต็มหรือสตรีมทรัพยากรหากไฟล์ของคุณอยู่ภายใน JAR

## ขั้นตอนที่ 2: กำหนดค่า Image Save Options

สร้างอินสแตนซ์ `ImageSaveOptions` เพื่อกำหนดฟอร์แมตของผลลัพธ์ (JPEG ในตัวอย่างนี้) คุณสามารถเปลี่ยนเป็น PNG, BMP หรือ GIF ได้โดยแก้ `SaveFormat`

```java
// Initialize ImageSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
```

## ขั้นตอนที่ 3: ระบุดัชนีหน้า

หน้าถูกนับจากศูนย์, ดังนั้น `1` จะเลือก **หน้าที่สอง** ปรับค่าตัวนี้เพื่อส่งออกหน้าที่คุณต้องการ

```java
// Specify second page for conversion
options.setPageIndex(1);
```

## ขั้นตอนที่ 4: บันทึกเอกสารเป็นภาพ

ตอนนี้เราจะเรียก `save` บนอ็อบเจ็กต์ `Document` โดยส่งชื่อไฟล์เป้าหมายและตัวเลือกที่กำหนดไว้

```java
// Save the document
oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);
```

## ขั้นตอนที่ 5: พิมพ์ข้อความยืนยัน

ข้อความคอนโซลง่าย ๆ จะบอกว่าภาพถูกสร้างสำเร็จแล้ว

```java
// Print confirmation message
System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
```

## วิธีแปลงหน้า OneNote เป็นภาพ (สถานการณ์ทางเลือก)

หากคุณต้องการ **แปลงไฟล์ภาพหน้า OneNote** เป็นจำนวนมาก เพียงใส่โค้ดข้างต้นไว้ในลูปที่วนผ่าน `Document.getPages()` เปลี่ยน `options.setPageIndex(i)` สำหรับแต่ละรอบ และอาจปรับ `options.setQuality(90)` เพื่อควบคุมการบีบอัด JPEG

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **ภาพเป็นสีขาว** | ดัชนีหน้านอกช่วงหรือเอกสารไม่โหลดอย่างถูกต้อง | ตรวจสอบให้ `options.setPageIndex` อยู่ในช่วง `0 .. document.getPages().size() - 1` |
| **ฟอร์แมตไม่รองรับ** | ใช้เวอร์ชัน Aspose.Note เก่าที่ไม่มีฟอร์แมตบางประเภท | อัปเดตเป็นรุ่นล่าสุดของ Aspose.Note for Java |
| **OutOfMemoryError** | แปลงหน้าขนาดใหญ่มากบน JVM ที่มีหน่วยความจำจำกัด | เพิ่มขนาด heap (`-Xmx2g`) หรือประมวลผลหน้าแบบทีละหน้า |

## คำถามที่พบบ่อย

**Q1: สามารถแปลงหลายหน้าเป็นภาพพร้อมกันได้หรือไม่?**  
A: ได้. ให้วนลูปบล็อกการบันทึกและเปลี่ยน `options.setPageIndex(i)` สำหรับแต่ละหน้าที่ต้องการส่งออก

**Q2: Aspose.Note รองรับไฟล์ OneNote เวอร์ชันต่าง ๆ หรือไม่?**  
A: รองรับแน่นอน. Aspose.Note รองรับไฟล์ .one จาก OneNote 2007, 2010, 2013 และเวอร์ชันต่อ ๆ มา

**Q3: สามารถปรับฟอร์แมตและคุณภาพของภาพระหว่างการแปลงได้หรือไม่?**  
A: ได้. เลือก `SaveFormat.Png`, `SaveFormat.Bmp` ฯลฯ และตั้งค่า `options.setQuality(int)` สำหรับคุณภาพ JPEG (0‑100)

**Q4: Aspose.Note มีการสนับสนุนภาษาโปรแกรมอื่น ๆ หรือไม่?**  
A: มี. มีไลบรารีสำหรับ .NET, Python, C++, และอื่น ๆ อีกมาก

**Q5: จะหาการสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้จากที่ไหน?**  
A: เยี่ยมชม [ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) หรือดูเอกสารอย่างเป็นทางการ [ที่นี่](https://reference.aspose.com/note/java/)

---

**อัปเดตล่าสุด:** 2025-11-29  
**ทดสอบกับ:** Aspose.Note for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}