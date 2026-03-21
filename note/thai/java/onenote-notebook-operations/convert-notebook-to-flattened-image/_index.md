---
date: 2026-03-21
description: เรียนรู้วิธีทำให้สมุดโน้ตแบนโดยการแปลง OneNote เป็น PNG ด้วย Aspose.Note
  สำหรับ Java คู่มือนี้ครอบคลุมการตั้งค่าความละเอียดของภาพ การบันทึก OneNote เป็นภาพ
  และการทำให้สมุดโน้ตแบนอย่างมีประสิทธิภาพ
linktitle: How to Flatten Notebook – Convert OneNote to PNG
second_title: Aspose.Note Java API
title: วิธีทำให้สมุดบันทึกแบน – แปลง OneNote เป็น PNG
url: /th/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีทำให้ Notebook แบนราบ – แปลง OneNote เป็น PNG

## Introduction

ในบทเรียนนี้คุณจะได้ค้นพบ **วิธีทำให้ notebook แบนราบ** โดยการแปลงโน้ตบุ๊ก OneNote เป็นภาพ PNG คุณภาพสูงโดยใช้ Aspose.Note for Java ไม่ว่าคุณจะต้องการฝังภาพสแนปชอตของโน้ตบุ๊กในรายงาน, แชร์มุมมองแบบอ่านอย่างเดียวกับเพื่อนร่วมงาน, หรือเก็บเป็นภาพที่สอดคล้องตามข้อกำหนด, คู่มือขั้นตอนนี้จะแสดงให้คุณเห็นอย่างชัดเจนว่าจะแปลง OneNote เป็นภาพอย่างไรพร้อมควบคุมความละเอียด

## Quick Answers
- **'flatten notebook' หมายถึงอะไร?** มันจะรวมองค์ประกอบทั้งหมดของหน้าเป็นภาพเรสเตอร์เดียว.  
- **ใช้รูปแบบใด?** PNG เป็นค่าเริ่มต้น ให้คุณภาพแบบไม่มีการสูญเสีย.  
- **สามารถเปลี่ยน DPI ได้หรือไม่?** ได้, ใช้ `setResolution` บน `ImageSaveOptions`.  
- **ต้องการไลเซนส์หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการประเมิน; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **รองรับบนทุกระบบปฏิบัติการหรือไม่?** API ของ Java ทำงานได้ทุกที่ที่ Java ทำงาน.  

## What is converting OneNote to PNG?

การแปลง OneNote เป็น PNG สร้างการแสดงผลแบบบิตแมพของทุกหน้าภายในโน้ตบุ๊ก, รักษาข้อความ, การวาด, และวัตถุที่ฝังไว้ในไฟล์ภาพเดียว. สิ่งนี้มีประโยชน์อย่างยิ่งสำหรับเอกสาร, การนำเสนอ, หรือการเก็บข้อมูลตามข้อกำหนด.

## Why convert OneNote to PNG with Aspose.Note?

- **ความสมบูรณ์แบบเต็มรูปแบบ** – ทุกองค์ประกอบภาพยังคงอยู่.  
- **ผลลัพธ์ไฟล์เดียว** – ไม่ต้องจัดการไฟล์หลายหน้า.  
- **ความละเอียดที่ปรับได้** – ปรับ DPI ให้ตรงตามความต้องการคุณภาพ.  
- **ไม่ต้องติดตั้ง Office** – ทำงานโดยอิสระจาก Microsoft OneNote อย่างสมบูรณ์.  

## Prerequisites

ก่อนที่เราจะเริ่ม, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. Java Development Kit (JDK) ติดตั้งอยู่ในระบบของคุณ.  
2. ไลบรารี Aspose.Note for Java ดาวน์โหลดและตั้งค่าในโปรเจค Java ของคุณ คุณสามารถดาวน์โหลดไลบรารีได้จาก [here](https://releases.aspose.com/note/java/).  
3. ความรู้พื้นฐานด้านการเขียนโปรแกรม Java.  

## Import Packages

เพื่อเริ่มต้น, คุณต้องนำเข้าแพ็กเกจที่จำเป็นจาก Aspose.Note for Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

### Step 1: Set Up Document Directory

ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

ก่อนอื่น, กำหนดไดเรกทอรีที่ไฟล์โน้ตบุ๊กของคุณอยู่:

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยพาธไปยังไฟล์โน้ตบุ๊กของคุณ.

### Step 2: Load Notebook

ขั้นตอนที่ 2: โหลดโน้ตบุ๊ก

ต่อไป, โหลดไฟล์โน้ตบุ๊กโดยใช้คลาส `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ `"test.onetoc2"` ด้วยชื่อไฟล์โน้ตบุ๊กของคุณ.

### Step 3: Set Image Save Options (set image resolution java)

ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการบันทึกภาพ (ตั้งค่าความละเอียดภาพใน Java)

ตอนนี้, ตั้งค่าตัวเลือกสำหรับบันทึกโน้ตบุ๊กเป็นภาพ เราจะระบุรูปแบบการบันทึกเป็น PNG และตั้งค่าความละเอียดเป็น 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

คุณสามารถปรับความละเอียดตามความต้องการของคุณได้ ที่นี่คือที่คุณ **ตั้งค่าความละเอียดภาพ** เพื่อควบคุมคุณภาพของผลลัพธ์.

### Step 4: Flatten Notebook (how to flatten notebook)

ขั้นตอนที่ 4: ทำให้โน้ตบุ๊กแบนราบ (วิธีทำให้โน้ตบุ๊กแบนราบ)

เพื่อให้แน่ใจว่าทุกองค์ประกอบถูกแบนราบเป็นภาพเดียว, ตั้งค่าตัวเลือก `flatten` เป็น `true`:

```java
saveOptions.setFlatten(true);
```

การตั้งค่า `flatten` เป็น `true` รับประกันว่าภาพ PNG ที่ได้จะคงรูปแบบการจัดวางของโน้ตบุ๊กอย่างแม่นยำ.

### Step 5: Save Image (save onenote as image)

ขั้นตอนที่ 5: บันทึกภาพ (บันทึก OneNote เป็นภาพ)

สุดท้าย, บันทึกโน้ตบุ๊กเป็นภาพที่แบนราบ:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

แทนที่ `"ExportImageasFlattenedNotebook_out.png"` ด้วยชื่อไฟล์ผลลัพธ์ที่คุณต้องการ ขั้นตอนนี้ **บันทึก OneNote เป็นภาพ** ที่คุณสามารถแชร์หรือฝังได้ทุกที่.

## Common Use Cases

- **เอกสาร:** ฝังภาพโน้ตบุ๊กในคู่มือเทคนิคหรือคู่มือผู้ใช้.  
- **การนำเสนอ:** ใช้สไลด์ PNG ความละเอียดสูงใน PowerPoint โดยไม่ต้องกังวลเรื่องฟอนต์หรือความเข้ากันของวัตถุ.  
- **การเก็บถาวร:** เก็บภาพสแนปชอตแบบอ่านอย่างเดียวของโน้ตบุ๊กสำหรับการตรวจสอบตามข้อกำหนด.  

## Troubleshooting Tips

- **ไฟล์ไม่พบ:** ตรวจสอบพาธ `dataDir` อีกครั้งและยืนยันว่าไฟล์ `.onetoc2` มีอยู่.  
- **ภาพคุณภาพต่ำ:** เพิ่ม DPI โดยเปลี่ยนเป็น `documentSaveOptions.setResolution(600);`.  
- **องค์ประกอบหายไป:** ตรวจสอบว่าได้เปิดใช้งาน `saveOptions.setFlatten(true);` หากไม่เปิดใช้งานบางเลเยอร์อาจยังคงแยกกันอยู่.  

## Frequently Asked Questions

**Q1: ฉันสามารถปรับความละเอียดของภาพผลลัพธ์ได้หรือไม่?**  
A1: ได้, คุณสามารถปรับความละเอียดตามความต้องการของคุณโดยแก้ไขพารามิเตอร์ของเมธอด `setResolution`.

**Q2: Aspose.Note รองรับรูปแบบภาพอื่นสำหรับการส่งออกหรือไม่?**  
A2: ได้, Aspose.Note รองรับรูปแบบภาพหลายประเภทเช่น PNG, JPEG, BMP, ฯลฯ สำหรับการส่งออกโน้ตบุ๊ก.

**Q3: ฉันสามารถปรับแต่งภาพผลลัพธ์เพิ่มเติมได้หรือไม่?**  
A3: ได้, Aspose.Note มีตัวเลือกหลากหลายสำหรับการปรับแต่งภาพผลลัพธ์ รวมถึงขนาดหน้า, การวางแนว, และการตั้งค่าคุณภาพ.

**Q4: มีเวอร์ชันทดลองสำหรับ Aspose.Note for Java หรือไม่?**  
A4: มี, คุณสามารถรับเวอร์ชันทดลองฟรีได้จาก [here](https://releases.aspose.com/).

**Q5: ฉันสามารถหาแหล่งสนับสนุนสำหรับ Aspose.Note for Java ได้ที่ไหน?**  
A5: คุณสามารถหาแหล่งสนับสนุนและทรัพยากรได้ที่ฟอรั่ม Aspose.Note [here](https://forum.aspose.com/c/note/28).

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}