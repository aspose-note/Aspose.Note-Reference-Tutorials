---
date: 2025-12-08
description: เรียนรู้วิธีตั้งค่ารูปแบบย่อหน้าและเพิ่มองค์ประกอบโครงร่างเมื่อสร้างเอกสาร
  OneNote ด้วย Java โดยใช้ Aspose.Note ส่งออก OneNote เป็น PDF และสร้างไฟล์ OneNote
  อย่างง่ายดาย
language: th
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: ตั้งค่ารูปแบบย่อหน้าในขณะสร้างเอกสาร OneNote ด้วย Java
url: /java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่ารูปแบบย่อหน้าเมื่อสร้างเอกสาร OneNote ด้วย Java

## Introduction

ในสภาพแวดล้อมการพัฒนาที่เปลี่ยนแปลงอย่างรวดเร็วในปัจจุบัน การสามารถ **set paragraph style** ด้วยโปรแกรมเป็นสิ่งสำคัญสำหรับการสร้างไฟล์ OneNote ที่ดูเป็นมืออาชีพ บทแนะนำนี้จะแสดงให้คุณเห็นขั้นตอนต่อขั้นตอนว่าอย่างไรในการสร้างเอกสาร OneNote ด้วยข้อความแบบ rich text ง่าย ๆ การกำหนดรูปแบบย่อหน้าแบบกำหนดเอง และสุดท้าย **export OneNote to PDF** ด้วย Aspose.Note for Java ไม่ว่าคุณจะกำลังสร้างเอนจิ้นรายงาน โซลูชันบันทึกโน้ตอัตโนมัติ หรือบริการแปลงเอกสาร เทคนิคที่อธิบายไว้ที่นี่จะช่วยให้คุณ **generate OneNote files** ที่มีลักษณะตรงตามที่ต้องการ

## Quick Answers
- **What does “set paragraph style” mean?** มันหมายถึงการกำหนดฟอนต์, ขนาด, สี, และการจัดรูปแบบอื่น ๆ ให้กับย่อหน้าของข้อความ  
- **Can I export the result to PDF?** ได้ – บทแนะนำจะจบด้วยการบันทึกไฟล์ OneNote เป็น PDF  
- **Do I need a license for Aspose.Note?** สามารถใช้เวอร์ชันทดลองฟรีเพื่อประเมินค่าใช้จ่าย; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง  
- **Which IDEs are supported?** IDE ของ Java ใดก็ได้ – Eclipse, IntelliJ IDEA, NetBeans ฯลฯ  
- **How long does the implementation take?** ประมาณ 10‑15 นาทีสำหรับเอกสารพื้นฐาน

## What is “set paragraph style” in Aspose.Note?
การตั้งค่า paragraph style หมายถึงการกำหนดอ็อบเจกต์ `ParagraphStyle` (ชื่อฟอนต์, ขนาด, สี ฯลฯ) แล้วผูกกับโหนด `RichText` ซึ่งทำให้คุณควบคุมการแสดงผลของข้อความภายในหน้า OneNote ได้อย่างเต็มที่

## Why set paragraph style when generating OneNote files?
- **Consistent branding:** ใช้ฟอนต์และสีขององค์กรโดยอัตโนมัติ  
- **Readability:** ฟอนต์ขนาดใหญ่หรือสีเฉพาะช่วยเพิ่มการเข้าถึง  
- **Export fidelity:** ข้อความที่มีรูปแบบจะคงอยู่เมื่อคุณ **convert OneNote PDF** ในภายหลัง  

## Prerequisites

ก่อนเริ่มทำงาน ให้ตรวจสอบว่าคุณมี:

1. **Java Development Kit (JDK) 1.8+** – JDK เวอร์ชันล่าสุดใดก็ใช้ได้  
2. **Aspose.Note for Java** – ดาวน์โหลด JAR ล่าสุดจาก [Aspose.Note download page](https://releases.aspose.com/note/java/)  
3. **An IDE** (Eclipse, IntelliJ IDEA, หรือ NetBeans) สำหรับคอมไพล์และรันตัวอย่าง  

> **Pro tip:** เพิ่ม Aspose.Note JAR ไปยัง classpath ของโปรเจกต์ผ่าน Maven หรืออ้างอิง JAR ด้วยตนเองใน IDE ของคุณ

## Import Packages

เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็น บล็อกนี้จะไม่เปลี่ยนแปลง

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> คลาส `ParagraphStyle` คือกุญแจสำคัญสำหรับการ **set paragraph style** ในขั้นตอนต่อไปของบทแนะนำ

## Step‑by‑Step Guide

ต่อไปนี้เป็นขั้นตอนสรุปการทำงานแต่ละขั้นตอน โค้ดบล็อกจะเหมือนกับตัวอย่างต้นฉบับ; เราเพียงเพิ่มคำอธิบายเท่านั้น

### Step 1: Set Document Directory
กำหนดตำแหน่งที่ไฟล์ที่สร้างจะถูกบันทึก

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยพาธแบบ absolute หรือ relative บนเครื่องของคุณ

### Step 2: Initialize Document Object
สร้างอ็อบเจกต์ `Document` รากที่แทนไฟล์ OneNote

```java
Document doc = new Document();
```

### Step 3: Initialize Page Object
ไฟล์ OneNote ประกอบด้วยหนึ่งหรือหลายหน้า; เราเริ่มด้วยหน้าเดียว

```java
Page page = new Page();
```

### Step 4: Initialize Outline Object
`Outline` ทำหน้าที่เป็นคอนเทนเนอร์สำหรับองค์ประกอบของ outline (คิดว่าเป็นส่วน)

```java
Outline outline = new Outline();
```

### Step 5: Initialize OutlineElement Object
ที่นี่เราจะ **add outline element** ที่จะเก็บข้อความ rich text ของเรา

```java
OutlineElement outlineElem = new OutlineElement();
```

### Step 6: Set Text Style (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

อินสแตนซ์ `ParagraphStyle` กำหนดฟอนต์, ขนาด, และสี – นี้คือจุดที่เราจะ **set paragraph style** ให้กับโหนดข้อความที่จะสร้างต่อไป

### Step 7: Initialize RichText Object

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

เราสร้างโหนด `RichText` ใส่สตริงง่าย ๆ แล้วผูกสไตล์ที่กำหนดไว้ก่อนหน้า

### Step 8: Add RichText Node to OutlineElement

```java
outlineElem.appendChildLast(text);
```

ตอนนี้ข้อความที่มีรูปแบบอยู่ภายใน outline element แล้ว

### Step 9: Add OutlineElement Node to Outline

```java
outline.appendChildLast(outlineElem);
```

`Outline` ตอนนี้มี element ที่เก็บย่อหน้าของเราแล้ว

### Step 10: Add Outline Node to Page

```java
page.appendChildLast(outline);
```

เราวาง `Outline` ลงบนหน้า

### Step 11: Add Page Node to Document

```java
doc.appendChildLast(page);
```

เอกสารตอนนี้มีหน้าเดียวที่มีข้อความที่กำหนดรูปแบบแล้ว

### Step 12: Save the Document (Export OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

เมธอด `save` จะเขียนไฟล์ OneNote และ **export OneNote PDF** ในขั้นตอนเดียว คุณยังสามารถบันทึกเป็น `.one` โดยใช้ `SaveFormat.One` หากต้องการรูปแบบดั้งเดิม

## Common Issues & Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **File not found** | `dataDir` ชี้ไปยังโฟลเดอร์ที่ไม่มีอยู่ | ตรวจสอบให้แน่ใจว่าโฟลเดอร์มีอยู่หรือสร้างด้วยโปรแกรม (`new File(dataDir).mkdirs();`) |
| **Blank PDF** | ไม่มีเนื้อหาใดถูกเพิ่มก่อนบันทึก | ยืนยันว่าโหนด `RichText` ถูกเพิ่มและสไตล์ถูกตั้งค่า |
| **Unsupported font** | ชื่อฟอนต์ไม่ได้ติดตั้งบนระบบ | ใช้ฟอนต์ทั่วไปเช่น `"Arial"` หรือฝังฟอนต์ในโปรเจกต์ |

## Frequently Asked Questions

**Q: Aspose.Note สามารถจัดการรูปแบบซับซ้อนเช่น ตารางหรือรูปภาพได้หรือไม่?**  
A: ได้, API รองรับตาราง, รูปภาพ, ลิงก์, และคุณลักษณะการจัดวางขั้นสูงอื่น ๆ  

**Q: สามารถ **convert OneNote PDF** กลับเป็นไฟล์ OneNote ได้หรือไม่?**  
A: การแปลงโดยตรงยังไม่มีให้บริการ, แต่คุณสามารถดึงข้อมูลจาก PDF แล้วสร้าง OneNote ใหม่ด้วย API  

**Q: ไลบรารีทำงานบน Linux/macOS ได้หรือไม่?**  
A: แน่นอน, Aspose.Note for Java เป็นแบบ platform‑independent; เพียงแค่ติดตั้ง JDK  

**Q: จะเพิ่มหลายหน้าหรือหลาย outline อย่างไร?**  
A: สร้างอ็อบเจกต์ `Page` และ `Outline` เพิ่มเติม แล้วผนวกเข้ากับ `Document` เช่นเดียวกับตัวอย่างหน้าเดียว  

**Q: จะหาโค้ดตัวอย่างเพิ่มเติมได้จากที่ไหน?**  
A: เอกสารอย่างเป็นทางการของ Aspose.Note และ [support forum](https://forum.aspose.com/c/note/28) มีตัวอย่างโค้ดมากมาย  

## Conclusion

คุณได้เรียนรู้วิธี **set paragraph style**, **add outline element**, และ **generate a OneNote file** ที่สามารถ **export to PDF** ด้วย Aspose.Note for Java การใส่ข้อความที่มีรูปแบบตั้งแต่ต้นกระบวนการสร้างเอกสารจะทำให้ผลลัพธ์ดูเป็นมืออาชีพและการ **convert OneNote PDF** ในภายหลังจะคงรูปแบบเดิมไว้ได้อย่างสมบูรณ์ อย่าลังเลที่จะต่อยอดพื้นฐานนี้ด้วยรูปภาพ, ตาราง, หรือเมทาดาต้าตามความต้องการของโครงการของคุณ

---

**Last Updated:** 2025-12-08  
**Tested With:** Aspose.Note for Java 24.11 (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}