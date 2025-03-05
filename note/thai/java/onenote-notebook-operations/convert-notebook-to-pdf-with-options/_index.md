---
title: แปลงโน้ตบุ๊กเป็น PDF ด้วยตัวเลือกใน OneNote - Aspose.Note
linktitle: แปลงโน้ตบุ๊กเป็น PDF ด้วยตัวเลือกใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: ปรับแต่งและส่งออกสมุดบันทึก OneNote เป็น PDF ได้อย่างง่ายดาย! Aspose.Note สำหรับ Java จัดการกับการยกของหนัก รวมคำแนะนำทีละขั้นตอน! #OneNote #Java #Aspose
type: docs
weight: 17
url: /th/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะเจาะลึกโลกของการแปลงสมุดบันทึกเป็น PDF พร้อมตัวเลือกที่ปรับแต่งได้โดยใช้ Aspose.Note สำหรับ Java Aspose.Note เป็น Java API ที่ทรงพลังซึ่งช่วยให้นักพัฒนาจัดการเอกสาร Microsoft OneNote โดยทางโปรแกรม การแปลงสมุดบันทึกเป็นรูปแบบ PDF เป็นข้อกำหนดทั่วไปในแอปพลิเคชันต่างๆ และด้วย Aspose.Note งานนี้มีความคล่องตัวและมีประสิทธิภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว
2. Aspose.Note สำหรับ Java: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ Java จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment): เลือก IDE ที่คุณต้องการสำหรับการพัฒนา Java IntelliJ IDEA, Eclipse หรือ NetBeans เป็นตัวเลือกยอดนิยม

## แพ็คเกจนำเข้า

ขั้นแรก คุณต้องนำเข้าแพ็คเกจที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ แพคเกจเหล่านี้มีคลาสและวิธีการที่จำเป็นสำหรับการทำงานกับเอกสาร OneNote

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## ขั้นตอนที่ 1: โหลดสมุดบันทึก OneNote

หากต้องการแปลงสมุดบันทึกเป็น PDF คุณต้องโหลดสมุดบันทึก OneNote ก่อน ตรวจสอบให้แน่ใจว่าระบุเส้นทางไปยังไฟล์สมุดบันทึกอย่างถูกต้อง

```java
String dataDir = "Your Document Directory";
// โหลดสมุดบันทึก OneNote
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## ขั้นตอนที่ 2: ระบุตัวเลือกการบันทึก PDF

Aspose.Note มีตัวเลือกต่างๆ สำหรับการปรับแต่งเอาต์พุต PDF คุณสามารถระบุตัวเลือกต่างๆ เช่น อัลกอริธึมการแยกหน้า การตั้งค่าส่วนหัว/ส่วนท้าย และอื่นๆ

```java
// ระบุตัวเลือกการบันทึก PDF
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## ขั้นตอนที่ 3: บันทึกสมุดบันทึกเป็น PDF

เมื่อคุณโหลดสมุดบันทึกและระบุตัวเลือกการบันทึกแล้ว ก็ถึงเวลาบันทึกสมุดบันทึกเป็นไฟล์ PDF

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// บันทึกสมุดบันทึก
notebook.save(dataDir, notebookSaveOptions);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจวิธีการแปลงสมุดบันทึก OneNote เป็นรูปแบบ PDF โดยใช้ Aspose.Note สำหรับ Java ด้วยการทำตามขั้นตอนง่ายๆ เหล่านี้ คุณสามารถจัดการการแปลงเอกสารในแอปพลิเคชัน Java ของคุณได้อย่างมีประสิทธิภาพ

---

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของเอาต์พุต PDF ได้หรือไม่

A1: ใช่ Aspose.Note มีตัวเลือกต่างๆ สำหรับการปรับแต่งเอาต์พุต PDF รวมถึงการตั้งค่าส่วนหัว/ส่วนท้าย อัลกอริธึมการแบ่งหน้า และอื่นๆ อีกมากมาย

### คำถามที่ 2: Aspose.Note เข้ากันได้กับ OneNote ทุกเวอร์ชันหรือไม่

A2: Aspose.Note รองรับ Microsoft OneNote 2010 และเวอร์ชันที่ใหม่กว่า

### คำถามที่ 3: Aspose.Note ให้ทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถดาวน์โหลด Aspose.Note รุ่นทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะหาเอกสารสำหรับ Aspose.Note ได้ที่ไหน

 A4: คุณสามารถค้นหาเอกสารที่ครอบคลุมสำหรับ Aspose.Note[ที่นี่](https://reference.aspose.com/note/java/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note ได้อย่างไร

 A5: สำหรับความช่วยเหลือทางเทคนิคหรือข้อสงสัย คุณสามารถไปที่ฟอรัมสนับสนุน Aspose.Note[ที่นี่](https://forum.aspose.com/c/note/28).