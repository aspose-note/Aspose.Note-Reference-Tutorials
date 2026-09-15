---
date: 2026-01-10
description: เรียนรู้วิธีดึงเวลาการแก้ไขล่าสุดและดึงประวัติการแก้ไขของหน้า OneNote
  ด้วย Aspose.Note สำหรับ Java. นำไปผสานในแอป Java ของคุณเพื่อการจัดการเอกสารที่มีประสิทธิภาพ.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: วิธีดึงเวลาการแก้ไขล่าสุดของหน้า OneNote – Aspose.Note
url: /th/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ดึงข้อมูลการแก้ไขของหน้าใน OneNote - Aspose.Note

## บทนำ

ในบทแนะนำนี้ คุณจะ **รับเวลาการแก้ไขล่าสุด** ของหน้าภายในเอกสาร OneNote และสำรวจวิธีดึงประวัติการแก้ไขทั้งหมดโดยใช้ Aspose.Note สำหรับ Java ไม่ว่าคุณจะกำลังสร้างระบบจัดการเอกสาร, ตรวจสอบการเปลี่ยนแปลง, หรือเพียงต้องการแสดงเวลาที่หน้าถูกแก้ไขครั้งล่าสุด คู่มือนี้จะแสดงวิธีดึงข้อมูลนั้นโดยโปรแกรม

## คำตอบอย่างรวดเร็ว
- **อะไรคือผลลัพธ์ของ “get last modified time”?** เวลาประทับของการแก้ไขล่าสุดบนหน้า OneNote.  
- **คลาสใดให้ประวัติการแก้ไข?** `PageHistory` ผ่าน `Document.getPageHistory(Page)`.  
- **ต้องการไลเซนส์สำหรับฟีเจอร์นี้หรือไม่?** ใช่, จำเป็นต้องมีไลเซนส์ Aspose.Note ที่ถูกต้องสำหรับการใช้งานในผลิตภัณฑ์.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 หรือสูงกว่า (JDK 8+).  
- **สามารถกรองการแก้ไขตามผู้เขียนได้หรือไม่?** คุณสามารถอ่านคุณสมบัติ `Author` ของแต่ละอ็อบเจ็กต์ `Page` และใช้ตัวกรองของคุณเอง.

## “get last modified time” คืออะไรใน OneNote?

**เวลาการแก้ไขล่าสุด** คือฟิลด์เมตาดาต้าที่เก็บไว้กับแต่ละหน้าเพื่อบันทึกเวลาที่หน้าได้รับการเปลี่ยนแปลงล่าสุด Aspose.Note เปิดเผยค่าดังกล่าวผ่านเมธอด `Page.getLastModifiedTime()` ทำให้การแสดงหรือบันทึกวันที่เปลี่ยนแปลงเป็นเรื่องง่าย.

## ทำไมต้องดึงประวัติการแก้ไขของหน้า?

- **เส้นทางการตรวจสอบ:** เก็บบันทึกว่าใครเปลี่ยนอะไรและเมื่อไหร่.  
- **การเปรียบเทียบเวอร์ชัน:** สร้างฟีเจอร์ที่เปรียบเทียบสองการแก้ไขเคียงข้างกัน.  
- **ข้อมูลเชิงลึกการทำงานร่วมกันของผู้ใช้:** ทำความเข้าใจรูปแบบการแก้ไขในสมุดบันทึกที่แชร์.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

### ติดตั้ง Java Development Kit (JDK)

ติดตั้ง JDK 8 หรือรุ่นที่ใหม่กว่าจากเว็บไซต์ของ Oracle หรือผู้จัดการแพคเกจที่คุณชื่นชอบ.

### ไลบรารี Aspose.Note สำหรับ Java

ดาวน์โหลดไลบรารีจากเว็บไซต์อย่างเป็นทางการ คุณสามารถพบลิงก์ดาวน์โหลด **[ที่นี่](https://releases.aspose.com/note/java/)**. ปฏิบัติตามคำแนะนำการติดตั้งในเอกสาร **[ที่นี่](https://reference.aspose.com/note/java/)**.

## นำเข้าแพ็กเกจ

เพื่อเริ่มต้น, นำเข้าแพ็กเกจที่จำเป็นเข้าสู่โครงการ Java ของคุณ แพ็กเกจเหล่านี้จะช่วยให้คุณใช้ฟังก์ชันที่ Aspose.Note สำหรับ Java ให้ได้.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

ต่อไปนี้เราจะแบ่งโค้ดตัวอย่างที่ให้เป็นหลายขั้นตอนเพื่อทำความเข้าใจแต่ละส่วนและการทำงานของมัน.

## วิธีรับเวลาการแก้ไขล่าสุดของหน้า OneNote

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

กำหนดไดเรกทอรีที่เก็บเอกสาร OneNote ของคุณ.

```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 2: โหลดเอกสาร

โหลดเอกสาร OneNote เข้าไปใน Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### ขั้นตอนที่ 3: ดึงหน้าแรก

ดึงหน้าแรกจากเอกสาร.

```java
Page firstPage = doc.getFirstChild();
```

### ขั้นตอนที่ 4: ดึงประวัติการแก้ไขของหน้า

รับประวัติการแก้ไขของหน้า.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### ขั้นตอนที่ 5: วนลูปประวัติการแก้ไขของหน้า

วนลูปผ่านรายการประวัติการแก้ไขของหน้าและดึงข้อมูลที่เกี่ยวข้อง, รวมถึง **เวลาการแก้ไขล่าสุด**.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## ปัญหาที่พบบ่อยและวิธีแก้

- **`PageHistory` เป็นค่า null:** ตรวจสอบว่าเอกสารมีประวัติการแก้ไขจริงหรือไม่; หากไม่มี `getPageHistory` อาจคืนค่า `null`.  
- **ความแตกต่างของโซนเวลา:** `getLastModifiedTime()` คืนค่า `java.util.Date` ในโซนเวลาปริยายของระบบ. แปลงเป็น UTC หากจำเป็น.  
- **ไลเซนส์ไม่ได้โหลด:** หากไม่มีไลเซนส์ที่ถูกต้อง, Aspose.Note จะทำงานในโหมดประเมินผล, จำกัดจำนวนหน้าที่ประมวลผล.

## คำถามที่พบบ่อย

### คำถาม 1: ฉันสามารถใช้ Aspose.Note สำหรับ Java เพื่อสร้างเอกสาร OneNote ใหม่ได้หรือไม่?

A1: ใช่, Aspose.Note สำหรับ Java มีการสนับสนุนอย่างครบถ้วนสำหรับการสร้าง, อ่าน, และจัดการเอกสาร OneNote ผ่านโปรแกรม.

### คำถาม 2: Aspose.Note สำหรับ Java รองรับไฟล์ OneNote เวอร์ชันต่าง ๆ หรือไม่?

A2: ใช่, Aspose.Note สำหรับ Java รองรับไฟล์ Microsoft OneNote หลายเวอร์ชัน, ทำให้เข้ากันได้ในสภาพแวดล้อมต่าง ๆ.

### คำถาม 3: ฉันสามารถปรับแต่งรูปแบบผลลัพธ์เมื่อส่งออกเอกสาร OneNote ได้หรือไม่?

A3: แน่นอน, Aspose.Note สำหรับ Java มีความยืดหยุ่นในการส่งออกเอกสาร OneNote ไปยังรูปแบบต่าง ๆ เช่น PDF, HTML, และภาพ, พร้อมตัวเลือกการปรับแต่ง.

### คำถาม 4: Aspose.Note สำหรับ Java ต้องการไลเซนส์สำหรับการใช้งานเชิงพาณิชย์หรือไม่?

A4: ใช่, จำเป็นต้องมีไลเซนส์ที่ถูกต้องสำหรับการใช้งานเชิงพาณิชย์ของ Aspose.Note สำหรับ Java. คุณสามารถรับไลเซนส์จากเว็บไซต์ของ Aspose.

### คำถาม 5: ฉันจะขอความช่วยเหลือได้จากที่ไหนหากพบปัญหาหรือมีคำถามเกี่ยวกับ Aspose.Note สำหรับ Java?

A5: สำหรับการสนับสนุนและความช่วยเหลือ, คุณสามารถเยี่ยมชมฟอรั่ม Aspose.Note **[ที่นี่](https://forum.aspose.com/c/note/28)**, ที่คุณสามารถถามคำถาม, แบ่งปันประสบการณ์, และโต้ตอบกับผู้ใช้และผู้เชี่ยวชาญคนอื่น ๆ.

---

**อัปเดตล่าสุด:** 2026-01-10  
**ทดสอบด้วย:** Aspose.Note for Java 23.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}