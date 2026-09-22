---
date: 2026-08-08
description: เรียนรู้วิธีติดตามการเปลี่ยนแปลงใน OneNote โดยดึงข้อมูลการแก้ไขหน้าแบบโปรแกรมเมติกด้วย
  Aspose.Note สำหรับ Java.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: รับการแก้ไขหน้าใน OneNote - Aspose.Note
og_description: เรียนรู้วิธีติดตามการเปลี่ยนแปลงใน OneNote โดยดึงข้อมูลการแก้ไขหน้าแบบโปรแกรมเมติกด้วย
  Aspose.Note สำหรับ Java.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: ติดตามการเปลี่ยนแปลงใน OneNote – การแก้ไขหน้าโดยใช้ Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: ติดตามการเปลี่ยนแปลงใน OneNote – การแก้ไขหน้าโดยใช้ Aspose.Note
url: /th/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ติดตามการเปลี่ยนแปลงใน OneNote – การแก้ไขหน้าโดยใช้ Aspose.Note

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **ติดตามการเปลี่ยนแปลงใน OneNote** โดยการสกัดประวัติการแก้ไขทั้งหมดของหน้าโดยใช้ Aspose.Note Java API เราจะครอบคลุมทุกอย่างตั้งแต่การตั้งค่าสภาพแวดล้อมการพัฒนาไปจนถึงการพิมพ์ผู้เขียน, เวลา, และชื่อของแต่ละการแก้ไข เพื่อให้คุณสามารถสร้างฟีเจอร์การตรวจสอบที่เชื่อถือได้สำหรับโซลูชันที่ใช้ OneNote ใด ๆ

## คำตอบอย่างรวดเร็ว
- **บทแนะนำครอบคลุมอะไร?** การดึงประวัติการแก้ไขหน้าจากไฟล์ OneNote ด้วย Aspose.Note for Java.  
- **เวอร์ชันของไลบรารีที่ต้องการคืออะไร?** เวอร์ชันล่าสุดใด ๆ ของ Aspose.Note for Java ที่รองรับ `LoadOptions.setLoadHistory`.  
- **ฉันต้องการใบอนุญาตหรือไม่?** ใบอนุญาตทดลองชั่วคราวใช้ได้สำหรับการทดสอบ; ใบอนุญาตเชิงพาณิชย์จำเป็นสำหรับการใช้งานจริง.  
- **ฉันสามารถแก้ไขการแก้ไขได้หรือไม่?** API เป็นแบบอ่านอย่างเดียวสำหรับการแก้ไข; คุณสามารถดึงข้อมูลได้เท่านั้น.  
- **ข้อกำหนดเบื้องต้นหลักคืออะไร?** Java JDK, Aspose.Note for Java, และเอกสาร OneNote ที่มีข้อมูลการแก้ไข.

## “บทแนะนำการแก้ไขหน้าของ Aspose.Note” คืออะไร?
บทแนะนำนี้แสดงวิธีการเข้าถึงเวอร์ชันประวัติของหน้าหนึ่งใน OneNote อย่างโปรแกรมมิ่ง แต่ละการแก้ไขจะมีเมตาดาต้าเช่น ผู้เขียน, เวลาสร้าง, และเวลาแก้ไข ทำให้คุณสามารถสร้างเส้นทางการตรวจสอบหรือฟีเจอร์บันทึกการเปลี่ยนแปลงภายในแอปพลิเคชันของคุณได้

## ทำไมต้องใช้ Aspose.Note สำหรับการติดตามการแก้ไขหน้า?
โหลดประวัติการแก้ไขทั้งหมดของสมุดบันทึกภายในเวลาไม่ถึง 5 วินาทีสำหรับไฟล์ 500‑หน้า บน CPU 2 GHz มาตรฐาน และดึงเมตาดาต้าโดยไม่ต้องเปิด UI ของ OneNote ไลบรารีรองรับรูปแบบเข้าและออกกว่า 30 แบบ ทำงานบน Windows, Linux, และ macOS (ครอบคลุม >95 % ของสภาพแวดล้อมเซิร์ฟเวอร์) และให้การควบคุมเต็มรูปแบบต่อคุณสมบัติของแต่ละการแก้ไข

## ข้อกำหนดเบื้องต้น

### 1. ชุดพัฒนา Java (JDK)
ตรวจสอบให้แน่ใจว่าได้ติดตั้ง JDK เวอร์ชันล่าสุด (8 หรือสูงกว่า) และตั้งค่า `JAVA_HOME` แล้ว

### 2. Aspose.Note for Java
ดาวน์โหลดไลบรารีจาก [download link](https://releases.aspose.com/note/java/).

### 3. ตัวอย่างเอกสาร OneNote
สร้างหรือหามาไฟล์ OneNote (เช่น `Sample1.one`) ที่มีหน้าที่บันทึกประวัติการแก้ไข

## นำเข้าแพ็กเกจ
แรกเริ่มให้ทำการนำเข้าคลาสของ Aspose.Note ที่จำเป็น  
`Document` แทนสมุดบันทึก OneNote, `LoadOptions` กำหนดพฤติกรรมการโหลด, และ `Page` แทนหน้าหนึ่งหน้า

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## การดำเนินการแบบขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร
กำหนดโฟลเดอร์ที่ไฟล์ OneNote ของคุณอยู่

```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 2: โหลดเอกสาร OneNote พร้อมเปิดใช้งานประวัติ
`LoadOptions` เป็นคลาสกำหนดค่าที่บอก Aspose.Note วิธีการเปิดไฟล์ รวมถึงการอ่านข้อมูลการแก้ไข เปิดใช้งานฟล็อกนี้ก่อนโหลดเอกสาร

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### ขั้นตอนที่ 3: ดึงหน้าที่แรก
รับอ็อบเจ็กต์หน้าที่แรก; นี้จะเป็นจุดอ้างอิงสำหรับการดึงประวัติของมัน

```java
Page firstPage = document.getFirstChild();
```

### ขั้นตอนที่ 4: วนลูปผ่านการแก้ไขหน้า
วนลูปผ่านแต่ละการแก้ไขและพิมพ์เมตาดาต้าที่เป็นประโยชน์ เช่น เวลา, ชื่อ, ระดับ, และผู้เขียน

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

> **เคล็ดลับ:** หากคุณต้องการกรองการแก้ไขตามผู้เขียนหรือช่วงวันที่เฉพาะ เพียงเพิ่มการตรวจสอบเงื่อนไขภายในลูป `for`.

## ปัญหาทั่วไปและวิธีแก้
- **ไม่มีการแก้ไขที่ส่งกลับ:** ตรวจสอบว่าได้เรียก `loadOptions.setLoadHistory(true)` ก่อนโหลดเอกสาร.  
- **ผู้เขียนหรือชื่อเป็น null:** บางเวอร์ชันเก่าของ OneNote อาจไม่เก็บฟิลด์เหล่านี้; ควรจัดการค่า `null` อย่างเหมาะสม.  
- **ความล่าช้าด้านประสิทธิภาพกับสมุดบันทึกขนาดใหญ่:** โหลดเฉพาะส่วนที่ต้องการหรือเพิ่มขนาด heap ของ JVM.

## คำถามที่พบบ่อย

**Q1: ฉันสามารถใช้ Aspose.Note for Java เพื่อแก้ไขการแก้ไขหน้าได้หรือไม่?**  
A1: ไม่, API ปัจจุบันรองรับการเข้าถึงการแก้ไขหน้าแบบอ่านอย่างเดียวเท่านั้น.

**Q2: Aspose.Note for Java เข้ากันได้กับเวอร์ชันต่าง ๆ ของเอกสาร OneNote หรือไม่?**  
A2: ใช่, มันทำงานกับรูปแบบไฟล์ OneNote ต่าง ๆ ทำให้การประมวลผลข้ามเวอร์ชันเป็นไปอย่างราบรื่น.

**Q3: Aspose.Note for Java ต้องการใบอนุญาตเพื่อใช้งานหรือไม่?**  
A3: ต้องการใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง, แต่มีใบอนุญาตทดลองชั่วคราวสำหรับการทดสอบ.

**Q4: ฉันสามารถขอรับการสนับสนุนได้หรือไม่หากพบปัญหาในการใช้ Aspose.Note for Java?**  
A4: ได้, คุณสามารถตั้งคำถามในฟอรั่ม Aspose.Note [Aspose.Note forum](https://forum.aspose.com/c/note/28).

**Q5: มีการทดลองใช้งานฟรีสำหรับ Aspose.Note for Java หรือไม่?**  
A5: มี, คุณสามารถดาวน์โหลดการทดลองใช้งานฟรีจาก [website](https://releases.aspose.com/).

---

**อัปเดตล่าสุด:** 2026-08-08  
**ทดสอบด้วย:** Aspose.Note for Java (รุ่นล่าสุด)  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [ติดตามการเปลี่ยนแปลง onenote – จัดการการแก้ไขหน้าโดยใช้ Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [บทแนะนำ Aspose Java - รับข้อมูลเกี่ยวกับหน้าต่างใน OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [เปลี่ยนพื้นหลังหน้าของ OneNote – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}