---
title: บันทึกเป็นรูปภาพระดับสีเทาใน OneNote - Aspose.Note
linktitle: บันทึกเป็นรูปภาพระดับสีเทาใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีบันทึกเอกสารเป็นรูปภาพระดับสีเทาใน OneNote โดยใช้ Aspose.Note for Java จัดการเอกสาร Microsoft OneNote โดยทางโปรแกรมได้อย่างง่ายดาย
type: docs
weight: 17
url: /th/java/onenote-document-saving/save-to-grayscale-image/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีการบันทึกเอกสารเป็นรูปภาพระดับสีเทาใน OneNote โดยใช้ Aspose.Note for Java ภาพระดับสีเทาเป็นภาพเอกรงค์ซึ่งข้อมูลสีจะแสดงด้วยเฉดสีเทาเท่านั้น Aspose.Note เป็น Java API ที่ทรงพลังซึ่งช่วยให้สามารถจัดการเอกสาร Microsoft OneNote โดยทางโปรแกรม

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
2.  Aspose.Note สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).
3. ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็น:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## ขั้นตอนที่ 1: โหลดเอกสาร

 ขั้นแรก ให้โหลดเอกสารลงใน Aspose.Note แทนที่`"Your Document Directory"` พร้อมเส้นทางไปยังไดเร็กทอรีเอกสารของคุณและ`"Aspose.one"` ด้วยชื่อเอกสาร OneNote ของคุณ

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางเอาต์พุตและตัวเลือก

กำหนดเส้นทางเอาต์พุตสำหรับรูปภาพระดับสีเทาและระบุตัวเลือกการบันทึก เราจะตั้งค่าโหมดสีเป็นโทนสีเทา

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## ขั้นตอนที่ 3: บันทึกเอกสาร

สุดท้าย ให้บันทึกเอกสารเป็นภาพระดับสีเทาโดยใช้ตัวเลือกที่ระบุ

```java
oneFile.save(dataDir, options);
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีบันทึกเอกสารเป็นรูปภาพระดับสีเทาใน OneNote โดยใช้ Aspose.Note for Java เรียบร้อยแล้ว สิ่งนี้มีประโยชน์อย่างเหลือเชื่อสำหรับแอพพลิเคชั่นต่างๆ ที่จำเป็นต้องใช้ภาพระดับสีเทา

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถบันทึกภาพระดับสีเทาในรูปแบบอื่นได้หรือไม่

 A1: ใช่คุณทำได้ เพียงแค่เปลี่ยน`SaveFormat` พารามิเตอร์ใน`ImageSaveOptions` Constructor ในรูปแบบที่คุณต้องการ

### คำถามที่ 2: Aspose.Note เข้ากันได้กับเอกสาร OneNote ทุกเวอร์ชันหรือไม่

ตอบ 2: Aspose.Note รองรับ Microsoft OneNote 2010 ขึ้นไป

### คำถามที่ 3: Aspose.Note จำเป็นต้องมีใบอนุญาตในการใช้งานหรือไม่

A3: ใช่ คุณต้องมีใบอนุญาตที่ถูกต้องเพื่อใช้ Aspose.Note ในสภาพแวดล้อมการใช้งานจริง อย่างไรก็ตาม คุณสามารถขอรับใบอนุญาตชั่วคราวเพื่อการทดสอบได้

### คำถามที่ 4: ฉันสามารถจัดการส่วนอื่นๆ ของเอกสารก่อนที่จะบันทึกเป็นรูปภาพได้หรือไม่

A4: แน่นอน! Aspose.Note มีคุณสมบัติที่หลากหลายสำหรับการแก้ไขเอกสาร OneNote โดยทางโปรแกรม

### คำถามที่ 5: ฉันจะรับการสนับสนุนได้ที่ไหนหากฉันประสบปัญหา

A5: คุณสามารถค้นหาการสนับสนุนได้ที่ฟอรั่ม Aspose.Note[ที่นี่](https://forum.aspose.com/c/note/28).