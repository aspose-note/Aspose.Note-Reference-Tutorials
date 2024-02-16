---
title: รับการแก้ไขหน้าใน OneNote - Aspose.Note
linktitle: รับการแก้ไขหน้าใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีดึงข้อมูลการแก้ไขหน้าใน OneNote โดยใช้ Aspose.Note สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการติดตามการเปลี่ยนแปลงอย่างมีประสิทธิภาพ
type: docs
weight: 14
url: /th/java/onenote-page-manipulation/get-page-revisions/
---
## การแนะนำ

OneNote เป็นเครื่องมือที่ทรงพลังสำหรับการจัดระเบียบและจัดการบันทึกย่อของคุณ แต่บางครั้งคุณจำเป็นต้องติดตามการเปลี่ยนแปลงและการแก้ไขที่ทำกับเพจของคุณ ด้วย Aspose.Note สำหรับ Java คุณสามารถดึงข้อมูลการแก้ไขหน้าโดยทางโปรแกรมได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการรับการแก้ไขหน้าใน OneNote โดยใช้ Aspose.Note for Java

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

### 1. ชุดพัฒนาจาวา (JDK)

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ คุณสามารถดาวน์โหลดและติดตั้ง JDK ได้จากเว็บไซต์ Oracle

### 2. Aspose.Note สำหรับ Java

ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ Java จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/note/java/).

### 3. ตัวอย่างเอกสาร OneNote

เตรียมเอกสาร OneNote ตัวอย่าง (`Sample1.one`) ที่มีหน้าที่คุณต้องการดึงข้อมูลการแก้ไข

## แพ็คเกจนำเข้า

ขั้นแรก คุณต้องนำเข้าแพ็คเกจที่จำเป็นจาก Aspose.Note สำหรับ Java

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

ตอนนี้ เรามาแบ่งตัวอย่างที่ให้ไว้ออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

กำหนดเส้นทางไดเรกทอรีที่มีเอกสาร OneNote ของคุณอยู่

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดเอกสาร OneNote

 โหลดเอกสาร OneNote โดยใช้`LoadOptions` เพื่อเปิดใช้งานประวัติการโหลด

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## ขั้นตอนที่ 3: รับหน้าแรก

ดึงหน้าแรกจากเอกสารที่โหลด

```java
Page firstPage = document.getFirstChild();
```

## ขั้นตอนที่ 4: ทำซ้ำผ่านการแก้ไขหน้า

วนซ้ำการแก้ไขแต่ละหน้าและดึงข้อมูลที่เกี่ยวข้อง เช่น เวลาที่แก้ไขล่าสุด เวลาที่สร้าง ชื่อเรื่อง ระดับ และผู้แต่ง

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

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีดึงการแก้ไขหน้าใน OneNote โดยใช้ Aspose.Note สำหรับ Java ด้วยการทำตามขั้นตอนเหล่านี้ คุณสามารถติดตามการเปลี่ยนแปลงที่ทำกับหน้า OneNote ของคุณโดยทางโปรแกรมได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.Note สำหรับ Java เพื่อแก้ไขการแก้ไขหน้าได้หรือไม่

ตอบ 1: ไม่ ปัจจุบัน Aspose.Note สำหรับ Java รองรับการดึงข้อมูลการแก้ไขหน้าแต่ไม่สามารถแก้ไขได้

### คำถามที่ 2: Aspose.Note สำหรับ Java เข้ากันได้กับเอกสาร OneNote เวอร์ชันต่างๆ หรือไม่

ตอบ 2: ใช่ Aspose.Note for Java รองรับเอกสาร OneNote เวอร์ชันต่างๆ ช่วยให้คุณสามารถทำงานกับไฟล์รูปแบบต่างๆ ได้อย่างราบรื่น

### คำถามที่ 3: Aspose.Note สำหรับ Java จำเป็นต้องมีใบอนุญาตในการใช้งานหรือไม่

ตอบ 3: ใช่ คุณต้องซื้อใบอนุญาตเพื่อใช้ Aspose.Note สำหรับ Java ในโครงการเชิงพาณิชย์ อย่างไรก็ตาม คุณยังสามารถขอรับใบอนุญาตชั่วคราวเพื่อวัตถุประสงค์ในการประเมินได้อีกด้วย

### คำถามที่ 4: ฉันสามารถขอความช่วยเหลือได้หรือไม่หากฉันประสบปัญหาใดๆ ในขณะที่ใช้ Aspose.Note สำหรับ Java

 A4: ได้ คุณสามารถขอการสนับสนุนจากฟอรัม Aspose.Note ได้[ที่นี่](https://forum.aspose.com/c/note/28).

### คำถามที่ 5: Aspose.Note สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A5: ได้ คุณสามารถเข้าถึง Aspose.Note สำหรับ Java รุ่นทดลองใช้ฟรีได้จาก[เว็บไซต์](https://releases.aspose.com/).