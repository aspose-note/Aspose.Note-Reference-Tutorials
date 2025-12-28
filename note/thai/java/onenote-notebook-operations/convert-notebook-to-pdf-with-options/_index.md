---
date: 2025-12-28
description: เรียนรู้วิธีการส่งออก OneNote เป็น PDF ด้วยการควบคุมเต็มที่โดยใช้ Aspose.Note
  สำหรับ Java รวมถึงตัวเลือกการส่งออกโน้ตบุ๊ก OneNote เป็น PDF และคู่มือการแปลงโน้ตบุ๊กเป็น
  PDF ด้วย Java
linktitle: How to Export OneNote to PDF with Options – Convert Notebook to PDF using
  Aspose.Note
second_title: Aspose.Note Java API
title: วิธีส่งออก OneNote เป็น PDF พร้อมตัวเลือก – แปลงสมุดบันทึกเป็น PDF ด้วย Aspose.Note
url: /th/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการส่งออก OneNote เป็น PDF พร้อมตัวเลือก – Aspose.Note Java API

## บทนำ

ในบทแนะนำนี้ คุณจะได้เรียนรู้ **วิธีการส่งออก OneNote เป็น PDF** พร้อมตัวเลือกที่ปรับแต่งได้โดยใช้ Aspose.Note สำหรับ Java การแปลงสมุดบันทึก OneNote เป็น PDF เป็นความต้องการที่พบบ่อย—ไม่ว่าจะเป็นการแชร์บันทึกการประชุม, เก็บเอกสารเป็นถาวร, หรือสร้างรายงานที่พิมพ์ได้ ด้วย Aspose.Note กระบวนการนี้ง่ายต่อการเขียนโปรแกรมอย่างเต็มรูปแบบและให้คุณควบคุมผลลัพธ์ PDF อย่างละเอียด

## คำตอบอย่างรวดเร็ว
- **API ทำอะไร?** มันโหลดสมุดบันทึก OneNote แล้วบันทึกเป็น PDF พร้อมการตั้งค่าเพิ่มเติม.  
- **ใช้ภาษาอะไร?** Java – เหมาะสำหรับแอปพลิเคชันฝั่งเซิร์ฟเวอร์หรือเดสก์ท็อป.  
- **ต้องการไลเซนส์หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **สามารถควบคุมการจัดหน้าได้หรือไม่?** ได้, คุณสามารถตั้งค่าอัลกอริทึมการแยกหน้า, ส่วนหัว, ส่วนท้าย, และอื่น ๆ  
- **โค้ดตัวอย่างสามารถรันได้หรือไม่?** แน่นอน – เพียงแทนที่พาธตัวอย่างด้วยตำแหน่งของสมุดบันทึกของคุณ.

## อะไรคือ “วิธีการส่งออก onenote เป็น pdf”

การส่งออก OneNote เป็น PDF หมายถึงการแปลงสมุดบันทึก OneNote ดั้งเดิม (`*.onetoc2` และไฟล์ส่วนที่เกี่ยวข้อง) ให้เป็นเอกสาร PDF แบบพกพาที่มีการจัดหน้าแบบคงที่ การแปลงนี้จะรักษาการจัดรูปแบบ, รูปภาพ, และวัตถุที่ฝังอยู่ในขณะเดียวกันทำให้เนื้อหาแสดงผลได้บนอุปกรณ์ใด ๆ โดยไม่ต้องใช้ OneNote

## ทำไมต้องใช้ Aspose.Note สำหรับ Java?

- **ไม่มีการพึ่งพา Microsoft Office** – ทำงานบนแพลตฟอร์มใดก็ได้ที่รัน Java.  
- **ตัวเลือก PDF ที่หลากหลาย** – ควบคุมการแยกหน้า, ส่วนหัว/ส่วนท้าย, และการจัดการวัตถุ.  
- **ความแม่นยำสูง** – ผลลัพธ์ PDF จะตรงกับลักษณะของ OneNote ดั้งเดิมอย่างใกล้เคียง.  
- **สามารถขยายได้** – เหมาะสำหรับการประมวลผลเป็นชุดหลายพันสมุดบันทึก.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามรายการต่อไปนี้:

1. **Java Development Kit (JDK)** – เวอร์ชัน 8 หรือสูงกว่า.  
2. **Aspose.Note for Java** – ดาวน์โหลดจาก [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse หรือ NetBeans (ตามที่คุณเลือก).  
4. **สมุดบันทึก OneNote** ที่คุณต้องการแปลง (เช่น `Notizbuch öffnen.onetoc2`).

## นำเข้าแพ็กเกจ

ขั้นแรก ให้นำเข้าคลาสที่ให้การจัดการสมุดบันทึกและฟังก์ชันการบันทึกเป็น PDF

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## ขั้นตอนที่ 1: โหลดสมุดบันทึก OneNote

โหลดไฟล์สมุดบันทึกจากดิสก์ แทนที่ `Your Document Directory` ด้วยโฟลเดอร์จริงที่มีไฟล์ `.onetoc2` ของคุณ

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## ขั้นตอนที่ 2: ระบุตัวเลือกการบันทึก PDF

ที่นี่คุณกำหนดวิธีการสร้าง PDF ตัวอย่างตั้งค่าอัลกอริทึมการแยกหน้าเพื่อให้วัตถุที่เป็นของแข็งอยู่ด้วยกัน ซึ่งมีประโยชน์เมื่อคุณมีแผนภาพหรือ ตารางที่ต้องอยู่ในหน้าเดียว

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## ขั้นตอนที่ 3: บันทึกสมุดบันทึกเป็น PDF

สุดท้าย ให้เขียนสมุดบันทึกออกเป็นไฟล์ PDF พาธผลลัพธ์สามารถเป็นตำแหน่งใดก็ได้ที่คุณต้องการ

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **ไฟล์ไม่พบ** | `dataDir` หรือชื่อไฟล์ไม่ถูกต้อง. | ตรวจสอบพาธอีกครั้งและยืนยันว่าไฟล์สมุดบันทึกมีอยู่. |
| **ฟอนต์หาย** | การเรนเดอร์ PDF ต้องการฟอนต์เดียวกับ OneNote. | ติดตั้งฟอนต์ที่จำเป็นบนเซิร์ฟเวอร์หรือฝังฟอนต์ผ่านตัวเลือก Aspose เพิ่มเติม. |
| **สมุดบันทึกขนาดใหญ่ทำให้เกิด OutOfMemoryError** | โหลดสมุดบันทึกทั้งหมดเข้าสู่หน่วยความจำ. | ประมวลผลส่วนย่อยแยกกันหรือเพิ่มขนาด heap ของ JVM (`-Xmx`). |

## สรุป

เราได้อธิบาย **วิธีการส่งออก OneNote เป็น PDF** ด้วย Aspose.Note สำหรับ Java ครอบคลุมการโหลดสมุดบันทึก, การกำหนดค่าตัวเลือก PDF, และการบันทึกผลลัพธ์ โดยทำตามขั้นตอนเหล่านี้ คุณสามารถรวมการแปลงสมุดบันทึกเป็น PDF เข้าไปในแอปพลิเคชัน Java ใดก็ได้ ไม่ว่าจะเป็นเครื่องมือเดสก์ท็อป, เว็บเซอร์วิส, หรือระบบประมวลผลแบบชุด.

## คำถามที่พบบ่อย

### Q1: ฉันสามารถปรับแต่งลักษณะของผลลัพธ์ PDF ได้หรือไม่?

A1: ได้, Aspose.Note มีตัวเลือกหลายอย่างสำหรับการปรับแต่งผลลัพธ์ PDF รวมถึงการตั้งค่าส่วนหัว/ส่วนท้าย, อัลกอริทึมการแยกหน้า, และอื่น ๆ

### Q2: Aspose.Note รองรับทุกเวอร์ชันของ OneNote หรือไม่?

A2: Aspose.Note รองรับ Microsoft OneNote ตั้งแต่เวอร์ชัน 2010 ขึ้นไป.

### Q3: Aspose.Note มีเวอร์ชันทดลองฟรีหรือไม่?

A3: มี, คุณสามารถดาวน์โหลดเวอร์ชันทดลองฟรีของ Aspose.Note ได้จาก [here](https://releases.aspose.com/).

### Q4: ฉันจะหาเอกสารประกอบของ Aspose.Note ได้จากที่ไหน?

A4: คุณสามารถค้นหาเอกสารประกอบที่ครบถ้วนของ Aspose.Note ได้ที่ [here](https://reference.aspose.com/note/java/).

### Q5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note อย่างไร?

A5: สำหรับความช่วยเหลือทางเทคนิคหรือคำถามใด ๆ คุณสามารถเยี่ยมชมฟอรั่มสนับสนุนของ Aspose.Note ได้ที่ [here](https://forum.aspose.com/c/note/28).

## คำถามเพิ่มเติมที่พบบ่อย

**Q: ฉันจะส่งออกสมุดบันทึก onenote เป็น pdf โดยไม่สูญเสียรูปภาพได้อย่างไร?**  
A: ตรวจสอบให้แน่ใจว่าได้ตั้งค่า `KeepSolidObjectsAlgorithm` (ตามที่แสดง) และไฟล์รูปภาพของสมุดบันทึกต้นทางสามารถเข้าถึงได้ในไดเรกทอรีเดียวกัน.

**Q: ฉันสามารถแปลงหลายสมุดบันทึกเป็นชุดในครั้งเดียวได้หรือไม่?**  
A: ได้. ทำการวนลูปผ่านรายการพาธของสมุดบันทึก, สร้าง `Notebook` สำหรับแต่ละรายการ, ใช้ `NotebookPdfSaveOptions` เดียวกัน, แล้วเรียก `save()`.

**Q: มีวิธีตั้งค่าเมตาดาต้า PDF (ผู้เขียน, ชื่อเรื่อง) ระหว่างการแปลงหรือไม่?**  
A: ใช้ `PdfSaveOptions.setMetadata()` เพื่อกำหนดผู้เขียน, ชื่อเรื่อง, หัวข้อ, และคีย์เวิร์ดก่อนบันทึก.

**Q: API รองรับ PDF ที่มีการป้องกันด้วยรหัสผ่านหรือไม่?**  
A: คุณสามารถตั้งรหัสผ่านบน `PdfSaveOptions` ผ่าน `setEncryptionPassword()` หลังจากกำหนดตัวเลือกอื่น ๆ.

**Q: เวอร์ชันของ Aspose.Note ที่ใช้ในบทแนะนำนี้คืออะไร?**  
A: โค้ดได้ทดสอบกับ Aspose.Note for Java 23.12.

**อัปเดตล่าสุด:** 2025-12-28  
**ทดสอบด้วย:** Aspose.Note for Java 23.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}