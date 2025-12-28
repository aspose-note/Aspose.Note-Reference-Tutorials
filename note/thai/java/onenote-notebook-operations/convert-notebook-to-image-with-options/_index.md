---
date: 2025-12-28
description: เรียนรู้วิธี **แปลง OneNote เป็นภาพ** และตั้งค่าความละเอียดของภาพใน Java
  ด้วย Aspose.Note คู่มือขั้นตอนต่อขั้นตอนนี้ยังแสดงวิธีส่งออกไฟล์ PNG ของ OneNote.
linktitle: Convert OneNote to Image with Options - Aspose.Note
second_title: Aspose.Note Java API
title: แปลง OneNote เป็นภาพพร้อมตัวเลือก - Aspose.Note
url: /th/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง OneNote เป็นภาพพร้อมตัวเลือก - Aspose.Note

## บทนำ

ในบทเรียนนี้ คุณจะได้เรียนรู้วิธี **แปลง OneNote เป็นภาพ** พร้อมตัวเลือกหลากหลายโดยใช้ Aspose.Note สำหรับ Java ไม่ว่าคุณจะต้องการ PNG ความละเอียดสูงสำหรับการรายงานหรือ JPEG ขนาดเล็กสำหรับภาพตัวอย่าง ขั้นตอนต่อไปนี้จะแสดงให้คุณเห็นอย่างชัดเจนว่าทำอย่างไรและจะผสานกระบวนการนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างไร

## คำตอบสั้น
- **“แปลง OneNote เป็นภาพ” หมายถึงอะไร?** คือการแปลงสมุดบันทึก OneNote ทั้งเล่มให้เป็นไฟล์ภาพเรสเตอร์ (PNG, JPEG ฯลฯ)  
- **ฟอร์แมตใดแนะนำสำหรับคุณภาพไม่มีการสูญเสีย?** PNG เนื่องจากรักษารายละเอียดทั้งหมดโดยไม่มีอาร์ติแฟกต์จากการบีบอัด  
- **จะตั้งค่าความละเอียดของภาพใน Java อย่างไร?** ใช้ `ImageSaveOptions.setResolution(int dpi)` ผ่าน `NotebookImageSaveOptions`  
- **สามารถส่งออกสมุดบันทึก OneNote เป็น PNG ได้ในขั้นตอนเดียวหรือไม่?** ได้, Aspose.Note มีเมธอด `save` เพียงครั้งเดียวพร้อมตัวเลือกที่เหมาะสม  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์; มีรุ่นทดลองฟรีสำหรับการประเมิน

## “แปลง OneNote เป็นภาพ” คืออะไร?
การแปลงสมุดบันทึก OneNote เป็นภาพหมายถึงการเรนเดอร์แต่ละหน้าในสมุดบันทึกเป็นไฟล์บิตแมพ ซึ่งมีประโยชน์สำหรับการสร้างตัวอย่างแบบคงที่, การเก็บสำรองข้อมูล, หรือการฝังหน้าสมุดบันทึกลงในรายงานที่ไม่รองรับฟอร์แมต OneNote ดั้งเดิม

## ทำไมต้องใช้ Aspose.Note สำหรับ Java?
- **ควบคุมเต็มรูปแบบ** บนฟอร์แมตผลลัพธ์, ความละเอียด, และความลึกของสี  
- **ไม่ต้องพึ่งพา Microsoft Office** – ทำงานได้บนสภาพแวดล้อม Java ฝั่งเซิร์ฟเวอร์ใดก็ได้  
- **รองรับสมุดบันทึกที่ซับซ้อน** ที่มีไฟล์ฝัง, หมึก, และข้อความที่มีรูปแบบหลากหลาย

## ข้อกำหนดเบื้องต้น

1. **Java Development Kit (JDK)** – เวอร์ชัน 8 หรือสูงกว่า  
2. **Aspose.Note สำหรับ Java JAR files** – ดาวน์โหลดไลบรารีล่าสุดจาก [here](https://releases.aspose.com/note/java/) แล้วเพิ่มลงใน classpath ของโปรเจกต์ของคุณ  

## นำเข้าแพ็กเกจ

ก่อนอื่นให้นำเข้าคลาสที่จำเป็นสำหรับการโหลดสมุดบันทึกและกำหนดค่าการส่งออกภาพ

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## ขั้นตอนที่ 1: โหลดสมุดบันทึก

โหลดสมุดบันทึก OneNote ที่ต้องการแปลง แทนที่พาธด้วยตำแหน่งที่ตั้งไฟล์ `.onetoc2` ของคุณ

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการบันทึก (วิธี **set image resolution java**)

สร้างอินสแตนซ์ของ `NotebookImageSaveOptions` เลือกฟอร์แมตผลลัพธ์และระบุความละเอียดที่ต้องการ ในตัวอย่างนี้เราใช้ PNG ที่ 400 dpi

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

> **เคล็ดลับ:** สำหรับการประมวลผลที่เร็วขึ้นกับสมุดบันทึกขนาดใหญ่ ให้ลดความละเอียดลง (เช่น 150 dpi) และเพิ่มขึ้นหากต้องการกราฟิกพร้อมพิมพ์

## ขั้นตอนที่ 3: บันทึกสมุดบันทึกเป็นภาพ (วิธี **export OneNote PNG**)

กำหนดชื่อไฟล์ผลลัพธ์และเรียกเมธอด `save` ตัวเลือกเดียวกันจะถูกนำไปใช้กับทุกหน้าของสมุดบันทึก

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

โค้ดด้านบนจะสร้างไฟล์ PNG (หรือชุดไฟล์ PNG หนึ่งไฟล์ต่อหนึ่งหน้า) ตามความละเอียดที่คุณตั้งค่าไว้

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **OutOfMemoryError** บนสมุดบันทึกขนาดใหญ่ | เพิ่มขนาด heap ของ JVM (`-Xmx2g`) หรือ ลดความละเอียด |
| **หน้าว่างในผลลัพธ์** | ตรวจสอบว่าสมุดบันทึกไม่ได้ถูกป้องกันด้วยรหัสผ่าน; ใช้ `Notebook.load(path, password)` หากจำเป็น |
| **ฟอร์แมตภาพที่ไม่รองรับ** | ใช้เฉพาะ `SaveFormat.Png`, `SaveFormat.Jpeg` หรือ `SaveFormat.Bmp` – ฟอร์แมตอื่น ๆ ไม่รองรับการส่งออกสมุดบันทึก |

## คำถามที่พบบ่อย

**Q: Aspose.Note สามารถจัดการไฟล์ OneNote ที่ซับซ้อนได้หรือไม่?**  
A: ได้, มันประมวลผลสมุดบันทึกที่มีไฟล์ฝัง, หมึกบันทึก, และการจัดรูปแบบที่หลากหลายได้อย่างมีประสิทธิภาพ  

**Q: Aspose.Note สำหรับ Java ใช้งานง่ายกับโปรเจกต์ที่มีอยู่แล้วหรือไม่?**  
A: แน่นอน, API มีความเรียบง่ายและคุณเพียงแค่เพิ่ม JAR ลงใน classpath  

**Q: สามารถปรับแต่งผลลัพธ์ภาพเมื่อแปลงสมุดบันทึกได้หรือไม่?**  
A: ได้, คุณสามารถตั้งค่าความละเอียด, ฟอร์แมต, และแม้แต่ความลึกของสีผ่าน `ImageSaveOptions`  

**Q: Aspose.Note มีการสนับสนุนสำหรับนักพัฒนาหรือไม่?**  
A: มี, Aspose มีเอกสารประกอบละเอียด, ฟอรั่ม, และช่องทางสนับสนุนที่ตอบสนองเร็ว  

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.Note สำหรับ Java หรือไม่?**  
A: มี, คุณสามารถดาวน์โหลดรุ่นทดลองได้จาก [here](https://releases.aspose.com/)

---

**อัปเดตล่าสุด:** 2025-12-28  
**ทดสอบด้วย:** Aspose.Note 24.11 สำหรับ Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}