---
title: แปลงสมุดบันทึกเป็นรูปภาพด้วยตัวเลือกใน OneNote - Aspose.Note
linktitle: แปลงสมุดบันทึกเป็นรูปภาพด้วยตัวเลือกใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีแปลง Notebook เป็นรูปภาพด้วยตัวเลือกที่ใช้ Aspose.Note สำหรับ Java ปฏิบัติตามบทช่วยสอนทีละขั้นตอนของเราเพื่อการผสานรวมเข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น
type: docs
weight: 14
url: /th/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะเจาะลึกกระบวนการแปลง Notebook เป็นรูปภาพด้วยตัวเลือกต่างๆ โดยใช้ Aspose.Note สำหรับ Java Aspose.Note เป็น Java API อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ช่วยให้สามารถผสานรวมเข้ากับแอปพลิเคชัน Java ได้อย่างราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว
2. Aspose.Note สำหรับไฟล์ Java JAR: ดาวน์โหลด Aspose.Note สำหรับไลบรารี Java จาก[ที่นี่](https://releases.aspose.com/note/java/) และรวมไว้ใน classpath ของโครงการของคุณ

## แพ็คเกจนำเข้า

ขั้นแรก เรามานำเข้าแพ็คเกจที่จำเป็นสำหรับแอปพลิเคชัน Java ของเรากันก่อน:

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## ขั้นตอนที่ 1: โหลดโน้ตบุ๊ก

ในการเริ่มต้น เราต้องโหลดสมุดบันทึก OneNote ที่เราต้องการแปลงเป็นรูปภาพ

```java
String dataDir = "Your Document Directory";
// โหลดสมุดบันทึก OneNote
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการบันทึก

ต่อไป เราจะกำหนดตัวเลือกการบันทึกรูปภาพ รวมถึงรูปแบบที่ต้องการ (PNG, JPEG ฯลฯ) และความละเอียด

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

## ขั้นตอนที่ 3: บันทึกสมุดบันทึกเป็นรูปภาพ

ตอนนี้เราจะบันทึกสมุดบันทึกเป็นรูปภาพพร้อมตัวเลือกที่ระบุ

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// บันทึกสมุดบันทึก
notebook.save(dataDir, notebookSaveOptions);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีแปลง Notebook เป็นรูปภาพด้วยตัวเลือกต่างๆ โดยใช้ Aspose.Note สำหรับ Java เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น โดยเปิดโอกาสให้จัดการไฟล์ OneNote โดยทางโปรแกรม

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สามารถจัดการไฟล์ OneNote ที่ซับซ้อนได้หรือไม่

A1: ได้ Aspose.Note สามารถจัดการไฟล์ OneNote ที่ซับซ้อนได้อย่างมีประสิทธิภาพ ช่วยให้คุณสามารถดำเนินการต่างๆ กับไฟล์เหล่านั้นโดยทางโปรแกรมได้

### คำถามที่ 2: Aspose.Note สำหรับ Java สามารถผสานรวมเข้ากับโปรเจ็กต์ที่มีอยู่ได้อย่างง่ายดายหรือไม่

A2: แน่นอน! Aspose.Note for Java มี API ตรงไปตรงมาซึ่งง่ายต่อการรวมเข้ากับโปรเจ็กต์ Java ของคุณ ซึ่งช่วยประหยัดเวลาและความพยายาม

### คำถามที่ 3: ฉันสามารถปรับแต่งเอาต์พุตรูปภาพเมื่อแปลงโน้ตบุ๊กได้หรือไม่

A3: ใช่ Aspose.Note อนุญาตให้คุณปรับแต่งเอาท์พุตรูปภาพโดยการระบุตัวเลือกต่างๆ เช่น ความละเอียด รูปแบบ และอื่นๆ

### คำถามที่ 4: Aspose.Note ให้การสนับสนุนสำหรับนักพัฒนาหรือไม่

ตอบ 4: ใช่ Aspose ให้การสนับสนุนอย่างดีเยี่ยมสำหรับนักพัฒนาผ่านฟอรัมและเอกสารประกอบของพวกเขา ทำให้มั่นใจได้ว่าการบูรณาการและการแก้ไขปัญหาจะราบรื่น

### คำถามที่ 5: Aspose.Note สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A5: ได้ คุณสามารถทดลองใช้ Aspose.Note สำหรับ Java ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).