---
title: บันทึกลงในภาพไบนารีโดยใช้เกณฑ์คงที่ใน OneNote
linktitle: บันทึกลงในภาพไบนารีโดยใช้เกณฑ์คงที่ใน OneNote
second_title: Aspose.Note Java API
description: บันทึกเอกสาร Microsoft OneNote เป็นอิมเมจไบนารีได้อย่างง่ายดายโดยใช้เกณฑ์คงที่ด้วย Aspose.Note Java ยกระดับความสามารถในการจัดการไฟล์ OneNote ของคุณ
type: docs
weight: 14
url: /th/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---
## การแนะนำ

Aspose.Note สำหรับ Java เป็น API ที่ทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ในบทช่วยสอนนี้ เราจะสำรวจวิธีการบันทึกเอกสารเป็นภาพไบนารี่โดยใช้เกณฑ์คงที่ ทำตามขั้นตอนด้านล่างเพื่อให้บรรลุเป้าหมายนี้

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
2.  Aspose.Note สำหรับไลบรารี Java ที่ดาวน์โหลด คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).
3. ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java

## แพ็คเกจนำเข้า

ขั้นแรก นำเข้าแพ็คเกจที่จำเป็นไปยังไฟล์ Java ของคุณ

```java
import com.aspose.note.*;
import java.io.IOException;
```

## ขั้นตอนที่ 1: โหลดเอกสาร

โหลดเอกสาร OneNote โดยใช้ Aspose.Note API

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกไบนารี

กำหนดตัวเลือกไบนารีสำหรับการบันทึกเอกสารเป็นรูปภาพไบนารี

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการบันทึกรูปภาพ

ตั้งค่าตัวเลือกการบันทึกรูปภาพ รวมถึงโหมดสีและตัวเลือกไบนารี

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## ขั้นตอนที่ 4: บันทึกเอกสาร

บันทึกเอกสารเป็นภาพไบนารี่ด้วยตัวเลือกที่ระบุ

```java
oneFile.save(dataDir, options);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีบันทึกเอกสารเป็นอิมเมจไบนารี่โดยใช้เกณฑ์คงที่ใน Aspose.Note สำหรับ Java เมื่อทำตามขั้นตอนเหล่านี้ คุณสามารถจัดการไฟล์ OneNote โดยทางโปรแกรมได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับค่าเกณฑ์สำหรับไบนาไรเซชันได้หรือไม่

 A1: ได้ คุณสามารถปรับค่าเกณฑ์ตามความต้องการของคุณได้โดยการแก้ไข`setBinarizationThreshold()` พารามิเตอร์วิธีการ

### คำถามที่ 2: Aspose.Note สำหรับ Java เข้ากันได้กับ Microsoft OneNote ทุกเวอร์ชันหรือไม่

คำตอบ 2: Aspose.Note สำหรับ Java รองรับ Microsoft OneNote เวอร์ชันต่างๆ รวมถึง 2010, 2013 และ 2016

### Q3: มีข้อจำกัดเกี่ยวกับขนาดของเอกสารที่สามารถประมวลผลได้หรือไม่?

A3: Aspose.Note สำหรับ Java ไม่มีข้อจำกัดเกี่ยวกับขนาดของเอกสารที่สามารถประมวลผลได้ ช่วยให้คุณสามารถจัดการไฟล์ขนาดใหญ่ได้อย่างมีประสิทธิภาพ

### คำถามที่ 4: ฉันสามารถแปลงเอกสาร OneNote หลายฉบับพร้อมกันได้หรือไม่

A4: ได้ คุณสามารถประมวลผลเอกสาร OneNote หลายชุดได้โดยการวนซ้ำแต่ละไฟล์และใช้การดำเนินการที่จำเป็น

### คำถามที่ 5: Aspose.Note สำหรับ Java มีการสนับสนุนด้านเทคนิคหรือไม่

 A5: ใช่ การสนับสนุนทางเทคนิคมีให้ผ่านทาง[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28)โดยคุณสามารถถามคำถามและขอความช่วยเหลือจากผู้เชี่ยวชาญได้