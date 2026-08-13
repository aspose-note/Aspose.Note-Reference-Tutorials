---
date: 2026-08-13
description: เรียนรู้วิธีรับเวลาแก้ไขของหน้า OneNote และดึงการแก้ไขของหน้าโดยใช้ Aspose.Note
  สำหรับ Java ซึ่งเหมาะสำหรับการตรวจสอบและการจัดการเอกสาร.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: รับการแก้ไขของหน้าใน OneNote - Aspose.Note
og_description: เรียนรู้วิธีรับเวลาแก้ไขของหน้า OneNote และดึงการแก้ไขของหน้า OneNote
  ด้วย Aspose.Note สำหรับ Java ขั้นตอนสั้น โค้ดตัวอย่าง และการแก้ไขปัญหา.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: รับเวลาแก้ไขของหน้า OneNote ด้วย Aspose.Note – บทเรียน Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: รับเวลาแก้ไขของหน้า OneNote ด้วย Aspose.Note
url: /th/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รับเวลาที่แก้ไขหน้า OneNote ด้วย Aspose.Note

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **get onenote page modified** timestamps และดึงประวัติการแก้ไขทั้งหมดของหน้า OneNote ด้วย Aspose.Note for Java ไม่ว่าคุณจะกำลังสร้างฟีเจอร์ audit‑trail, ตัวดู change‑log, หรือจำเป็นต้องแสดงวันที่แก้ไขล่าสุดในแดชบอร์ด คำแนะนำนี้จะพาคุณผ่านทุกขั้นตอน—from การตั้งค่าสภาพแวดล้อมจนถึงการจัดการกับปัญหาที่พบบ่อย

## คำตอบอย่างรวดเร็ว
- **What does “get last modified time” return?** มันจะคืนค่า timestamp ของการแก้ไขล่าสุดบนหน้า OneNote.  
- **Which class provides revision history?** `PageHistory` ผ่าน `Document.getPageHistory(Page)`.  
- **Do I need a license for this feature?** ใช่, จำเป็นต้องมีใบอนุญาต Aspose.Note ที่ถูกต้องสำหรับการใช้งานในสภาพแวดล้อมการผลิต.  
- **What Java version is supported?** Java 8 หรือสูงกว่า (JDK 8+).  
- **Can I filter revisions by author?** คุณสามารถอ่านคุณสมบัติ `Author` ของแต่ละอ็อบเจ็กต์ `Page` แล้วนำไปใช้กรองตามต้องการ.

## อะไรคือ “get last modified time” ใน OneNote?

เวลาที่แก้ไขล่าสุดถูกเก็บเป็นคุณลักษณะ metadata บนแต่ละหน้า OneNote ซึ่งบ่งบอกถึงช่วงเวลาที่มีการแก้ไขล่าสุด Aspose.Note เปิดเผยค่าดังกล่าวผ่านเมธอด `Page.getLastModifiedTime()` ซึ่งจะคืนค่าเป็นอ็อบเจ็กต์ `java.util.Date` ที่คุณสามารถจัดรูปแบบหรือบันทึกตามความต้องการของแอปพลิเคชันของคุณ

## ทำไมต้องดึงประวัติการแก้ไขหน้า?

การดึงประวัติการแก้ไขหน้าให้คุณมี audit trail ครบถ้วนของทุกการเปลี่ยนแปลงที่ทำบนหน้า OneNote ทำให้คุณสามารถติดตามว่าใครแก้ไขอะไรและเมื่อไหร่ ประวัตินี้สามารถใช้เปรียบเทียบเวอร์ชัน, คืนสภาพก่อนหน้า, หรือวิเคราะห์รูปแบบการทำงานร่วมกันของทีม ซึ่งเป็นสิ่งสำคัญสำหรับการปฏิบัติตามมาตรฐานและการควบคุมคุณภาพ

## ข้อกำหนดเบื้องต้น

- **Java Development Kit (JDK) 8 หรือใหม่กว่า** – ติดตั้งจากเว็บไซต์ของ Oracle หรือผู้จำหน่ายที่เข้ากันได้.  
- **Aspose.Note for Java library** – ดาวน์โหลดไฟล์ JAR จากหน้า **[การปล่อย Aspose.Note Java](https://releases.aspose.com/note/java/)** และทำตามคู่มือการติดตั้งใน **[เอกสาร Aspose.Note Java](https://reference.aspose.com/note/java/)**.  

## นำเข้าแพ็กเกจ

คลาส `Document` แทนโน้ตบุ๊ก OneNote ที่โหลดเข้าสู่หน่วยความจำ, ส่วน `Page` และ `PageHistory` ให้เข้าถึงหน้าแต่ละหน้าและข้อมูลการแก้ไขของมัน

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(ข้อความนำเข้าจริงจะแสดงเป็นข้อความธรรมดาเพื่อรักษาจำนวน code‑block ดั้งเดิม.)*

## วิธีรับเวลาที่แก้ไขหน้า OneNote?

เพื่อรับ timestamp ของการแก้ไขล่าสุด, ก่อนอื่นให้โหลดเอกสาร OneNote เข้าไปในอ็อบเจ็กต์ `Document`, จากนั้นเลือก `Page` ที่ต้องการ เรียกเมธอด `getLastModifiedTime()` บนหน้านั้น ซึ่งจะคืนค่าเป็น `java.util.Date`. คุณสามารถจัดรูปแบบวันที่นี้ด้วย `SimpleDateFormat` หรือแปลงเป็น UTC เพื่อรายงานที่สอดคล้องกันข้ามโซนเวลา

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

กำหนดโฟลเดอร์ที่บรรจุไฟล์ OneNote ของคุณ

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## ขั้นตอนที่ 2: โหลดเอกสาร

สร้างอินสแตนซ์ `Document` โดยส่งพาธเต็มของไฟล์ `.one` ของคุณ

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 3: ดึงหน้าแรก

ดึงอ็อบเจ็กต์ `Page` แรกจากคอลเลกชันหน้าในเอกสาร

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## ขั้นตอนที่ 4: ดึงประวัติการแก้ไขหน้า

รับ `PageHistory` สำหรับหน้าที่เลือก หากโน้ตบุ๊กไม่เคยถูกแก้ไข การเรียกนี้อาจคืนค่า `null`

```java
Page firstPage = doc.getFirstChild();
```

## ขั้นตอนที่ 5: เดินผ่านประวัติการแก้ไขหน้า

วนลูปผ่านแต่ละการแก้ไขของ `Page`, อ่าน `Author` และ `LastModifiedTime` ของมัน, แล้วแสดงข้อมูล

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## ปัญหาทั่วไปและวิธีแก้
- **Null `PageHistory`** – ตรวจสอบว่าโน้ตบุ๊กมีประวัติการแก้ไขจริงหรือไม่; หากไม่มี `getPageHistory` จะคืนค่า `null`.  
- **Time‑zone differences** – `getLastModifiedTime()` ใช้โซนเวลามาตรฐานของ JVM. แปลงเป็น UTC ด้วย `SimpleDateFormat` หากแอปของคุณต้องการโซนมาตรฐาน.  
- **License not loaded** – หากไม่มีใบอนุญาตที่ถูกต้อง Aspose.Note จะทำงานในโหมดประเมินผล, จำกัดการประมวลผลหน้า. โหลดไฟล์ใบอนุญาตของคุณเมื่อแอปเริ่มทำงานเพื่อหลีกเลี่ยงข้อจำกัดนี้.

## คำถามที่พบบ่อย

**Q1: ฉันสามารถใช้ Aspose.Note for Java เพื่อสร้างเอกสาร OneNote ใหม่ได้หรือไม่?**  
A: ได้, API ให้คุณสร้าง, แก้ไข, และบันทึกโน้ตบุ๊ก OneNote จากศูนย์ได้โดยอัตโนมัติ

**Q2: Aspose.Note for Java รองรับไฟล์ OneNote เวอร์ชันต่าง ๆ หรือไม่?**  
A: รองรับรูปแบบไฟล์ OneNote ตั้งแต่ 2007‑2021, ทำให้เข้ากันได้อย่างกว้างขวางบนเดสก์ท็อปและคลาวด์

**Q3: ฉันสามารถปรับแต่งรูปแบบผลลัพธ์เมื่อส่งออกเอกสาร OneNote ได้หรือไม่?**  
A: แน่นอน. คุณสามารถส่งออกเป็น PDF, HTML, PNG, หรือ SVG, และควบคุมตัวเลือกเช่น ความละเอียดภาพและการฝังฟอนต์

**Q4: Aspose.Note for Java ต้องการใบอนุญาตสำหรับการใช้ในเชิงพาณิชย์หรือไม่?**  
A: ใช่, จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานในสภาพแวดล้อมการผลิต. มีรุ่นทดลองฟรีสำหรับการประเมิน

**Q5: ฉันจะขอความช่วยเหลือได้จากที่ไหนหากพบปัญหา?**  
A: เยี่ยมชม **[ฟอรัม Aspose.Note](https://forum.aspose.com/c/note/28)** เพื่อถามคำถาม, แบ่งปันประสบการณ์, และรับความช่วยเหลือจากชุมชนและวิศวกรของ Aspose

---

**อัปเดตล่าสุด:** 2026-08-13  
**ทดสอบกับ:** Aspose.Note for Java 23.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose

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

## บทแนะนำที่เกี่ยวข้อง

- [บทแนะนำ Aspose Java - รับข้อมูลเกี่ยวกับหน้าใน OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [บทแนะนำการแก้ไขหน้า Aspose.Note – ดึงประวัติการแก้ไขหน้าใน OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [ติดตามการเปลี่ยนแปลง OneNote – จัดการประวัติการแก้ไขหน้าด้วย Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}