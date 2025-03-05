---
title: บันทึกเป็น PDF โดยใช้การตั้งค่าหน้าใน OneNote - Aspose.Note
linktitle: บันทึกเป็น PDF โดยใช้การตั้งค่าหน้าใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีบันทึกเอกสาร OneNote เป็น PDF ใน Java โดยใช้ไลบรารี Aspose.Note คำแนะนำทีละขั้นตอนพร้อมตัวอย่างโค้ดสำหรับการตั้งค่าหน้าต่างๆ
type: docs
weight: 19
url: /th/java/onenote-document-saving/save-to-pdf-using-page-settings/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะเรียนรู้วิธีบันทึกเอกสาร OneNote เป็นรูปแบบ PDF โดยใช้การตั้งค่าหน้าต่างๆ ด้วย Aspose.Note สำหรับ Java เราจะกล่าวถึงสองวิธี: การบันทึกด้วยการตั้งค่าหน้า Letter และการบันทึกด้วยการตั้งค่าหน้า A4 โดยไม่จำกัดความสูง

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
2. Aspose.Note สำหรับไลบรารี Java ที่ดาวน์โหลดและรวมอยู่ในโปรเจ็กต์ Java ของคุณ
3. ความเข้าใจพื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม Java

## แพ็คเกจนำเข้า

ตรวจสอบให้แน่ใจว่าคุณได้นำเข้าแพ็คเกจที่จำเป็นสำหรับการใช้ Aspose.Note สำหรับ Java ในโปรเจ็กต์ของคุณ นี่คือคำสั่งการนำเข้า:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## บันทึกเป็น PDF โดยใช้การตั้งค่าหน้าจดหมาย

### ขั้นตอนที่ 1: โหลดเอกสาร

ขั้นแรก ให้โหลดเอกสาร OneNote ลงใน Aspose หมายเหตุ:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### ขั้นตอนที่ 2: กำหนดเส้นทางปลายทาง

ระบุเส้นทางปลายทางสำหรับไฟล์ PDF:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### ขั้นตอนที่ 3: บันทึกเอกสาร

บันทึกเอกสารด้วยการตั้งค่าหน้า Letter:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## บันทึกเป็น PDF โดยใช้การตั้งค่าหน้า A4 โดยไม่มีขีดจำกัดความสูง

### ขั้นตอนที่ 1: โหลดเอกสาร

ในทำนองเดียวกัน ให้โหลดเอกสาร OneNote ลงใน Aspose หมายเหตุ:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### ขั้นตอนที่ 2: กำหนดเส้นทางปลายทาง

ระบุเส้นทางปลายทางสำหรับไฟล์ PDF:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### ขั้นตอนที่ 3: บันทึกเอกสาร

บันทึกเอกสารด้วยการตั้งค่าหน้า A4 โดยไม่มีขีดจำกัดความสูง:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

หลังจากทำตามขั้นตอนเหล่านี้ คุณจะบันทึกเอกสาร OneNote ของคุณเป็น PDF ได้สำเร็จโดยใช้การตั้งค่าหน้าอื่น

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจวิธีการบันทึกเอกสาร OneNote เป็นรูปแบบ PDF โดยใช้ Aspose.Note สำหรับไลบรารี Java ด้วยการทำตามคำแนะนำทีละขั้นตอน คุณสามารถรวมฟังก์ชันนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งการตั้งค่าหน้าเพิ่มเติมได้หรือไม่

ตอบ 1: ได้ คุณสามารถปรับแต่งการตั้งค่าเพจได้ตามความต้องการของคุณโดยใช้ Aspose.Note สำหรับ Java

### คำถามที่ 2: Aspose.Note รองรับรูปแบบเอาต์พุตอื่นๆ นอกเหนือจาก PDF หรือไม่

ตอบ 2: ใช่ Aspose.Note รองรับรูปแบบเอาต์พุตที่หลากหลาย รวมถึงรูปภาพและ HTML

### คำถามที่ 3: Aspose.Note เข้ากันได้กับไฟล์ OneNote เวอร์ชันต่างๆ หรือไม่

A3: ใช่ Aspose.Note รองรับไฟล์ OneNote จากเวอร์ชันต่างๆ รวมถึง .one และ .onetoc2

### คำถามที่ 4: ฉันสามารถแปลงไฟล์ OneNote หลายไฟล์เป็น PDF ได้ในคราวเดียวหรือไม่

A4: ได้ คุณสามารถประมวลผลไฟล์ OneNote หลายไฟล์เป็นชุดโดยใช้ Aspose.Note for Java

### คำถามที่ 5: มีเวอร์ชันทดลองใช้งานสำหรับการทดสอบหรือไม่

A5: ได้ คุณสามารถทดลองใช้ Aspose.Note สำหรับ Java ได้ฟรีจากเว็บไซต์