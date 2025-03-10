---
title: รับการแก้ไขหน้าใน OneNote - Aspose.Note
linktitle: รับการแก้ไขหน้าใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีดึงข้อมูลการแก้ไขของหน้าภายในเอกสาร OneNote โดยใช้ Aspose.Note Java รวมสิ่งนี้เข้ากับแอป Java ของคุณเพื่อการจัดการเอกสารที่มีประสิทธิภาพ
weight: 15
url: /th/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รับการแก้ไขหน้าใน OneNote - Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะเจาะลึกความสามารถของ Aspose.Note สำหรับ Java ซึ่งเป็นไลบรารีอันทรงพลังที่ช่วยให้คุณทำงานกับไฟล์ Microsoft OneNote ในแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น โดยเฉพาะอย่างยิ่ง เราจะเน้นไปที่วิธีการดึงข้อมูลการแก้ไขของหน้าภายในเอกสาร OneNote ในตอนท้ายของคู่มือนี้ คุณจะมีความรู้ในการแยกการแก้ไขหน้าได้อย่างมีประสิทธิภาพ รวมถึงรายละเอียดต่างๆ เช่น เวลาที่แก้ไขล่าสุด เวลาในการสร้าง ชื่อเรื่อง ระดับ และผู้แต่ง

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอนนี้ ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:

### ติดตั้ง Java Development Kit (JDK) แล้ว

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดและติดตั้งได้จากเว็บไซต์ Oracle หรือใช้ตัวจัดการแพ็คเกจ หากคุณใช้ระบบ Unix

### Aspose.Note สำหรับไลบรารี Java

 ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับไลบรารี Java จากเว็บไซต์ คุณสามารถค้นหาลิงค์ดาวน์โหลด[ที่นี่](https://releases.aspose.com/note/java/) . ปฏิบัติตามคำแนะนำในการติดตั้งที่ให้ไว้ในเอกสารประกอบ[ที่นี่](https://reference.aspose.com/note/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ แพ็คเกจเหล่านี้จะช่วยให้คุณใช้ประโยชน์จากฟังก์ชันการทำงานของ Aspose.Note สำหรับ Java ได้

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

ตอนนี้ เรามาแจกแจงโค้ดตัวอย่างที่ให้ไว้เป็นหลายขั้นตอนเพื่อทำความเข้าใจส่วนประกอบแต่ละส่วนและฟังก์ชันการทำงานของส่วนประกอบต่างๆ

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

กำหนดไดเร็กทอรีที่มีเอกสาร OneNote ของคุณอยู่

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดเอกสาร

โหลดเอกสาร OneNote ลงใน Aspose.Note

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## ขั้นตอนที่ 3: รับหน้าแรก

ดึงหน้าแรกจากเอกสาร

```java
Page firstPage = doc.getFirstChild();
```

## ขั้นตอนที่ 4: รับการแก้ไขหน้า

รับประวัติการแก้ไขของเพจ

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## ขั้นตอนที่ 5: การแก้ไขหน้าสำรวจ

วนซ้ำรายการการแก้ไขหน้าและดึงข้อมูลที่เกี่ยวข้อง

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

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจวิธีการดึงข้อมูลการแก้ไขของหน้าภายในเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ Java ด้วยการทำตามคำแนะนำทีละขั้นตอนและใช้ประโยชน์จากโค้ดตัวอย่างที่ให้มา คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างง่ายดาย ช่วยให้สามารถจัดการไฟล์ OneNote ได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.Note สำหรับ Java เพื่อสร้างเอกสาร OneNote ใหม่ได้หรือไม่

ตอบ 1: ใช่ Aspose.Note for Java ให้การสนับสนุนที่ครอบคลุมสำหรับการสร้าง การอ่าน และการจัดการเอกสาร OneNote โดยทางโปรแกรม

### คำถามที่ 2: Aspose.Note สำหรับ Java เข้ากันได้กับไฟล์ OneNote เวอร์ชันต่างๆ หรือไม่

ตอบ 2: ใช่ Aspose.Note สำหรับ Java รองรับไฟล์ Microsoft OneNote เวอร์ชันต่างๆ ทำให้มั่นใจได้ถึงความเข้ากันได้ในสภาพแวดล้อมที่แตกต่างกัน

### คำถามที่ 3: ฉันสามารถปรับแต่งรูปแบบผลลัพธ์เมื่อส่งออกเอกสาร OneNote ได้หรือไม่

ตอบ 3: แน่นอนว่า Aspose.Note สำหรับ Java มอบความยืดหยุ่นในการส่งออกเอกสาร OneNote เป็นรูปแบบต่างๆ เช่น PDF, HTML และรูปภาพ พร้อมตัวเลือกสำหรับการปรับแต่ง

### คำถามที่ 4: Aspose.Note สำหรับ Java จำเป็นต้องมีใบอนุญาตสำหรับการใช้งานเชิงพาณิชย์หรือไม่

ตอบ 4: ใช่ จำเป็นต้องมีใบอนุญาตที่ถูกต้องสำหรับการใช้งาน Aspose.Note สำหรับ Java ในเชิงพาณิชย์ คุณสามารถขอรับใบอนุญาตได้จากเว็บไซต์ Aspose

### คำถามที่ 5: ฉันจะขอความช่วยเหลือได้ที่ไหนหากฉันประสบปัญหาหรือมีคำถามเกี่ยวกับ Aspose.Note สำหรับ Java

 A5: สำหรับการสนับสนุนและความช่วยเหลือ คุณสามารถไปที่ฟอรัม Aspose.Note[ที่นี่](https://forum.aspose.com/c/note/28)ซึ่งคุณสามารถถามคำถาม แบ่งปันประสบการณ์ และโต้ตอบกับผู้ใช้และผู้เชี่ยวชาญคนอื่นๆ ได้
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
