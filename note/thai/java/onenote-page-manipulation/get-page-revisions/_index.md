---
date: 2026-01-10
description: เรียนรู้บทแนะนำการแก้ไขหน้า Aspose.Note สำหรับ Java – ดึงข้อมูลการแก้ไขหน้าของ
  OneNote อย่างอัตโนมัติด้วย Aspose.Note. ทำตามคู่มือขั้นตอนต่อขั้นตอนของเรา.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: บทแนะนำการแก้ไขหน้าใน aspose.note – รับการแก้ไขหน้าใน OneNote
url: /th/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ดึงประวัติการแก้ไขหน้าใน OneNote - Aspose.Note

OneNote เป็นแพลตฟอร์มจดบันทึกที่ทรงพลัง และเมื่อคุณต้องการตรวจสอบการเปลี่ยนแปลง **aspose.note page revisions tutorial** จะแสดงให้คุณเห็นว่าการดึงประวัติการแก้ไขทำได้อย่างไรด้วยเพียงไม่กี่บรรทัดของโค้ด Java ในคู่มือนี้เราจะพาคุณผ่านทุกขั้นตอนตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการพิมพ์รายละเอียดของแต่ละการแก้ไข เพื่อให้คุณสามารถติดตามการแก้ไข ผู้เขียน และเวลาประทับได้อย่างง่ายดาย

## คำตอบอย่างรวดเร็ว
- **บทเรียนนี้ครอบคลุมอะไรบ้าง?** การดึงประวัติการแก้ไขหน้าจากไฟล์ OneNote ด้วย Aspose.Note สำหรับ Java  
- **ต้องใช้เวอร์ชันของไลบรารีใด?** เวอร์ชัน Aspose.Note สำหรับ Java ใดก็ได้ที่สนับสนุน `LoadOptions.setLoadHistory`  
- **ต้องใช้ไลเซนส์หรือไม่?** ไลเซนส์ทดลองชั่วคราวใช้ได้สำหรับการทดสอบ; ต้องใช้ไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **สามารถแก้ไขการแก้ไขได้หรือไม่?** API มีเพียงการอ่านข้อมูลการแก้ไข; คุณสามารถดึงข้อมูลได้เท่านั้น  
- **ข้อกำหนดเบื้องต้นหลักคืออะไร?** Java JDK, Aspose.Note สำหรับ Java, และเอกสาร OneNote ที่มีข้อมูลการแก้ไข

## “aspose.note page revisions tutorial” คืออะไร?
บทเรียนนี้แสดงวิธีเข้าถึงเวอร์ชันประวัติของหน้าหนึ่งใน OneNote อย่างโปรแกรมมิ่ง แต่ละการแก้ไขจะมีเมตาดาต้าเช่น ผู้เขียน, เวลาสร้าง, และเวลาแก้ไข ซึ่งช่วยให้คุณสร้างเส้นทางการตรวจสอบหรือฟีเจอร์บันทึกการเปลี่ยนแปลงในแอปพลิเคชันของคุณได้

## ทำไมต้องใช้ Aspose.Note สำหรับการติดตามการแก้ไขหน้า?
- **ไม่พึ่งพา UI** – ทำงานทั้งหมดในโค้ด เหมาะสำหรับบริการแบ็กเอนด์  
- **ข้ามแพลตฟอร์ม** – Java ทำงานบน Windows, Linux, และ macOS  
- **ควบคุมเต็มรูปแบบ** – ดึงคุณสมบัติของทุกการแก้ไขโดยไม่ต้องเปิด OneNote ด้วยตนเอง  
- **ประสิทธิภาพ** – การโหลดประวัติได้รับการปรับให้เร็ว จึงสามารถประมวลผลสมุดบันทึกขนาดใหญ่ได้อย่างรวดเร็ว

## ข้อกำหนดเบื้องต้น

### 1. Java Development Kit (JDK)
ตรวจสอบให้แน่ใจว่ามี JDK เวอร์ชันล่าสุด (8 หรือสูงกว่า) ติดตั้งและตั้งค่า `JAVA_HOME` แล้ว

### 2. Aspose.Note สำหรับ Java
ดาวน์โหลดไลบรารีจาก [ลิงก์ดาวน์โหลด](https://releases.aspose.com/note/java/)

### 3. ตัวอย่างเอกสาร OneNote
สร้างหรือหาไฟล์ OneNote (เช่น `Sample1.one`) ที่มีหน้าที่มีประวัติการแก้ไข

## นำเข้าแพ็กเกจ
เริ่มต้นด้วยการนำเข้าคลาส Aspose.Note ที่จำเป็น

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## การดำเนินการตามขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าโฟลเดอร์เอกสาร
กำหนดโฟลเดอร์ที่ไฟล์ OneNote ของคุณอยู่

```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 2: โหลดเอกสาร OneNote พร้อมเปิดใช้งานประวัติ
เปิดใช้แฟล็ก `LoadOptions` เพื่อดึงข้อมูลการแก้ไข

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### ขั้นตอนที่ 3: ดึงหน้าแรก
รับอ็อบเจ็กต์หน้าที่แรก; จะเป็นจุดอ้างอิงสำหรับการดึงประวัติของมัน

```java
Page firstPage = document.getFirstChild();
```

### ขั้นตอนที่ 4: วนลูปผ่านการแก้ไขหน้า
วนลูปแต่ละการแก้ไขและพิมพ์เมตาดาต้าที่เป็นประโยชน์ เช่น เวลา, ชื่อเรื่อง, ระดับ, และผู้เขียน

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **เคล็ดลับ:** หากต้องการกรองการแก้ไขตามผู้เขียนหรือช่วงวันที่เฉพาะ เพียงเพิ่มเงื่อนไขตรวจสอบภายในลูป `for`

## ปัญหาที่พบบ่อยและวิธีแก้
- **ไม่มีการแก้ไขใดแสดงผล:** ตรวจสอบว่าได้เรียก `loadOptions.setLoadHistory(true)` ก่อนโหลดเอกสารหรือไม่  
- **ผู้เขียนหรือชื่อเรื่องเป็น null:** บางเวอร์ชัน OneNote เก่าอาจไม่เก็บฟิลด์เหล่านี้; ควรจัดการค่า `null` อย่างเหมาะสม  
- **ประสิทธิภาพช้าบนสมุดบันทึกขนาดใหญ่:** โหลดเฉพาะส่วนที่ต้องการหรือเพิ่มขนาด heap ของ JVM

## คำถามที่พบบ่อย

**Q1: สามารถใช้ Aspose.Note สำหรับ Java แก้ไขการแก้ไขหน้าได้หรือไม่?**  
A1: ไม่ได้, API ปัจจุบันรองรับการเข้าถึงการแก้ไขหน้าแบบอ่านอย่างเดียวเท่านั้น

**Q2: Aspose.Note สำหรับ Java รองรับเวอร์ชันไฟล์ OneNote ต่าง ๆ หรือไม่?**  
A2: รองรับ, ทำงานกับรูปแบบไฟล์ OneNote หลากหลายเวอร์ชัน ทำให้การประมวลผลข้ามเวอร์ชันเป็นไปอย่างราบรื่น

**Q3: Aspose.Note สำหรับ Java ต้องการไลเซนส์เพื่อใช้งานหรือไม่?**  
A3: ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์, แต่มีไลเซนส์ทดลองชั่วคราวสำหรับการทดสอบ

**Q4: สามารถขอรับการสนับสนุนได้หากพบปัญหาในการใช้ Aspose.Note สำหรับ Java หรือไม่?**  
A4: ได้, คุณสามารถถามคำถามในฟอรั่ม Aspose.Note [ที่นี่](https://forum.aspose.com/c/note/28)

**Q5: มีการทดลองใช้ฟรีสำหรับ Aspose.Note สำหรับ Java หรือไม่?**  
A5: มี, คุณสามารถดาวน์โหลดการทดลองใช้ฟรีจาก [เว็บไซต์](https://releases.aspose.com/)

---

**อัปเดตล่าสุด:** 2026-01-10  
**ทดสอบด้วย:** Aspose.Note สำหรับ Java (รุ่นล่าสุด)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}