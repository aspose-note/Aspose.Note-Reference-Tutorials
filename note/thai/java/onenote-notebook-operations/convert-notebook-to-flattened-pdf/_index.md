---
title: แปลงสมุดบันทึกเป็น PDF แบบเรียบใน OneNote - Aspose.Note
linktitle: แปลงสมุดบันทึกเป็น PDF แบบเรียบใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: แปลงโน้ตบุ๊กเป็น PDF แบบเรียบๆ ได้อย่างง่ายดายด้วย Aspose.Note สำหรับ Java เพลิดเพลินกับตัวเลือกการผสานรวมและการปรับแต่งที่ราบรื่น
type: docs
weight: 16
url: /th/java/onenote-notebook-operations/convert-notebook-to-flattened-pdf/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีแปลงสมุดบันทึกให้เป็นรูปแบบ PDF ที่แบนราบโดยใช้ Aspose.Note สำหรับ Java การแปลงสมุดบันทึกเป็น PDF เป็นข้อกำหนดทั่วไปสำหรับแอปพลิเคชันจำนวนมาก และ Aspose.Note ทำให้กระบวนการนี้ง่ายขึ้นด้วยชุดคุณสมบัติที่ครอบคลุมและ API ที่ใช้งานง่าย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว
2.  Aspose.Note สำหรับไลบรารี Java: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับไลบรารี Java จาก[ที่นี่](https://releases.aspose.com/note/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): เลือก IDE ตามที่คุณต้องการ เช่น IntelliJ IDEA หรือ Eclipse

## แพ็คเกจนำเข้า

ขั้นแรก เรามานำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณกันก่อน:

```java
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import java.io.IOException;
```

## ขั้นตอนที่ 1: โหลดสมุดบันทึก OneNote

ในการเริ่มต้น ให้โหลดสมุดบันทึก OneNote ที่คุณต้องการแปลงเป็น PDF:

```java
String dataDir = "Your Document Directory";
Notebook notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการแปลง

 กำหนดตัวเลือกสำหรับการแปลงสมุดบันทึกเป็น PDF ที่นี่เราจะตั้งค่า`flatten` ถึง`true` เพื่อทำให้ PDF แบนลง:

```java
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
notebookSaveOptions.setFlatten(true);
```

## ขั้นตอนที่ 3: บันทึกสมุดบันทึกเป็น PDF

ระบุไดเร็กทอรีเอาต์พุตและบันทึกสมุดบันทึกเป็น PDF ด้วยตัวเลือกที่กำหนดไว้:

```java
dataDir = dataDir + "ExportNotebookToPDFAsFlattened_out.pdf";
// บันทึกสมุดบันทึก
notebook.save(dataDir, notebookSaveOptions);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีแปลงสมุดบันทึกเป็นรูปแบบ PDF ที่แบนราบโดยใช้ Aspose.Note สำหรับ Java กระบวนการนี้ตรงไปตรงมาและสามารถรวมเข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สำหรับ Java เข้ากันได้กับ OneNote เวอร์ชันต่างๆ หรือไม่

ตอบ 1: ใช่ Aspose.Note สำหรับ Java รองรับ OneNote เวอร์ชันต่างๆ เพื่อให้มั่นใจถึงความเข้ากันได้ในสภาพแวดล้อมที่แตกต่างกัน

### คำถามที่ 2: ฉันสามารถปรับแต่งเอาต์พุต PDF โดยใช้ Aspose.Note สำหรับ Java ได้หรือไม่

A2: แน่นอน คุณสามารถปรับแต่งเอาต์พุต PDF ได้ตามความต้องการของคุณ รวมถึงเค้าโครงหน้า รูปแบบตัวอักษร และอื่นๆ อีกมากมาย

### คำถามที่ 3: Aspose.Note สำหรับ Java รองรับการแปลงโน้ตบุ๊กเป็นชุดหรือไม่

ตอบ 3: ได้ คุณสามารถแปลงสมุดบันทึกหลายชุดเป็น PDF ได้อย่างมีประสิทธิภาพโดยใช้ Aspose.Note สำหรับ Java

### คำถามที่ 4: Aspose.Note สำหรับ Java มีเวอร์ชันทดลองใช้งานหรือไม่

 ตอบ 4: ได้ คุณสามารถเข้าถึง Aspose.Note for Java รุ่นทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 A5: คุณสามารถค้นหาการสนับสนุนและความช่วยเหลือสำหรับ Aspose.Note สำหรับ Java ได้ที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).