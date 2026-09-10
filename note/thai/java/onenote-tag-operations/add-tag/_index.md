---
date: 2026-01-28
description: เรียนรู้วิธีสร้างโครงร่างใน OneNote, เพิ่มแท็กใน OneNote และสร้างไฟล์
  PDF จาก OneNote ด้วย Aspose.Note สำหรับ Java.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: สร้างโครงร่างใน OneNote และเพิ่มแท็ก – Aspose.Note
url: /th/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างโครงร่างใน OneNote และเพิ่มแท็ก – Aspose.Note

## Introduction
คุณกำลังมองหา **การสร้างโครงร่างใน OneNote** และเพิ่มการทำงานร่วมกันด้วยแท็กโดยใช้ Java หรือไม่? Aspose.Note for Java ทำให้การเพิ่มแท็ก, จัดโครงสร้างโน้ตของคุณ, และแม้กระทั่ง **สร้าง PDF จากไฟล์ OneNote** เป็นเรื่องง่าย ในบทแนะนำนี้เราจะเดินผ่านแต่ละขั้นตอน, อธิบาย *เหตุผล* ที่แต่ละส่วนสำคัญ, และแสดงวิธีสร้าง PDF ที่ดูเป็นมืออาชีพในตอนท้าย.

## Quick Answers
- **“การสร้างโครงร่างใน OneNote” หมายถึงอะไร?** มันสร้างโครงสร้างแบบลำดับชั้น (outline) ที่จัดระเบียบเนื้อหาเช่นหัวเรื่องและส่วนย่อย.  
- **ไลบรารีใดที่เพิ่มแท็กให้กับ OneNote?** Aspose.Note for Java มีคลาส `NoteTag` สำหรับตัวบ่งชี้แบบภาพ.  
- **ฉันสามารถส่งออกผลลัพธ์เป็น PDF ได้หรือไม่?** ได้ – ใช้ `SaveFormat.Pdf` เพื่อ **สร้าง PDF จาก OneNote**.  
- **ต้องใช้ไลเซนส์สำหรับการใช้งานจริงหรือไม่?** มีไลเซนส์ชั่วคราวสำหรับการทดสอบ; ต้องมีไลเซนส์เต็มสำหรับการใช้งานเชิงพาณิชย์.  
- **ข้อกำหนดเบื้องต้นหลักคืออะไร?** ติดตั้ง JDK, มีไลบรารี Aspose.Note for Java, และมีความรู้พื้นฐานด้าน Java.

## What is “create outline in OneNote”?
การสร้างโครงร่างใน OneNote หมายถึงการเพิ่มอ็อบเจ็กต์ `Outline` และ `OutlineElement` ที่กำหนดโครงสร้างแบบต้นไม้สำหรับโน้ตของคุณ โครงสร้างนี้ทำให้คุณสามารถยุบ, ขยาย, และจัดระเบียบข้อมูลได้เหมือนกับหัวเรื่องในเอกสาร.

## Why add tag to OneNote?
แท็กเช่นดาว, เครื่องหมายถูก, หรือไอคอนกำหนดเองให้ผู้อ่านเห็นสัญญาณภาพ, ปรับปรุงการค้นหา, และช่วยทีมจัดลำดับความสำคัญของรายการต่าง ๆ ด้วย Aspose.Note คุณสามารถแนบ `NoteTag` ไปยังข้อความใด ๆ ได้โดยอัตโนมัติ.

## Prerequisites
ก่อนเริ่มทำงาน, โปรดตรวจสอบว่าคุณมี:
- ติดตั้ง Java Development Kit (JDK) แล้ว.  
- ดาวน์โหลดไลบรารี Aspose.Note for Java. คุณสามารถรับได้จาก [ที่นี่](https://releases.aspose.com/note/java/).  
- มีความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java.

## Import Packages
ตรวจสอบว่าคุณได้นำเข้าชุดแพ็กเกจที่จำเป็นเพื่อเริ่มโครงการของคุณ:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
เราจะอธิบายโค้ดด้านบนเป็นขั้นตอนทีละขั้นตอน.

## Step 1: Set up Document and Page
เริ่มต้นด้วยการสร้างอ็อบเจ็กต์ `Document` ใหม่และกำหนดค่าอ็อบเจ็กต์ `Page`:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```
ในขั้นตอนนี้ เรากำหนดเส้นทางไปยังโฟลเดอร์เอกสาร, สร้าง `Document` ใหม่, และเริ่มต้น `Page`.

## Step 2: Create an Outline
ต่อไป, สร้างอ็อบเจ็กต์ `Outline` เพื่อจัดโครงสร้างเนื้อหาของคุณ:
```java
Outline outline = new Outline();
```
Outline ให้โครงสร้างแบบลำดับชั้นกับเอกสารของคุณ ทำให้การ **สร้างโครงร่างใน OneNote** เป็นเรื่องง่ายและช่วยให้ข้อมูลเป็นระเบียบ.

## Step 3: Initialize OutlineElement and ParagraphStyle
จากนั้น, กำหนดค่า `OutlineElement` และตั้งค่า `ParagraphStyle` สำหรับการจัดรูปแบบข้อความ:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
`OutlineElement` แทนส่วนหนึ่งของโครงร่าง, ส่วน `ParagraphStyle` กำหนดคุณสมบัติการจัดรูปแบบข้อความ.

## Step 4: Add RichText with NoteTag
สร้างอ็อบเจ็กต์ `RichText`, เพิ่มข้อความ OneNote ของคุณ, แล้วแนบ `NoteTag`:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
`RichText` ช่วยให้คุณใส่ข้อความที่มีการจัดรูปแบบ, ส่วน `NoteTag` **เพิ่มแท็กให้กับ OneNote** เป็นสัญญาณภาพ.

## Step 5: Build Outline Structure
เพิ่มโหนดข้อความ, โหนด `OutlineElement`, และโหนด `Outline` เพื่อสร้างโครงสร้างของเอกสาร:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
ขั้นตอนนี้ทำให้เนื้อหาของคุณถูกจัดระเบียบภายในเอกสาร, เสร็จสิ้นกระบวนการ **สร้างโครงร่างใน OneNote**.

## Step 6: Save the Document
บันทึกเอกสารในรูปแบบ PDF, ซึ่ง **สร้าง PDF จาก OneNote**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
ตอนนี้เอกสาร OneNote ของคุณที่มีการเพิ่มแท็กถูกบันทึกเป็นไฟล์ PDF แล้ว.

โดยทำตามขั้นตอนเหล่านี้ คุณสามารถปรับปรุงเอกสาร OneNote ของคุณได้อย่างง่ายดายด้วย Aspose.Note for Java.

## Conclusion
ในบทแนะนำนี้เราได้สำรวจวิธี **สร้างโครงร่างใน OneNote**, เพิ่มแท็กให้กับ OneNote, และจากนั้น **สร้าง PDF จาก OneNote** ด้วย Aspose.Note for Java การใช้ Java ทำให้คุณควบคุมโครงสร้างโน้ต, การแท็กแบบภาพ, และตัวเลือกการส่งออกได้เต็มที่ ทำให้โน้ตของคุณเป็นระเบียบและแชร์ได้ง่ายขึ้น.

## FAQs
### 1. ฉันสามารถใช้ Aspose.Note for Java กับภาษาโปรแกรมอื่นได้หรือไม่?
Aspose.Note รองรับหลัก ๆ คือ Java, แต่ยังมีเวอร์ชันสำหรับ .NET ด้วย.

### 2. Aspose.Note for Java เหมาะกับผู้เริ่มต้นหรือไม่?
ใช่, Aspose.Note for Java มีเอกสารและการสนับสนุนที่ครบถ้วน ทำให้ผู้เริ่มต้นและนักพัฒนาที่มีประสบการณ์สามารถใช้งานได้อย่างง่ายดาย.

### 3. ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.Note for Java ได้อย่างไร?
คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/).

### 4. จะหาแหล่งสนับสนุนเพิ่มเติมได้จากที่ไหน?
สำหรับคำถามหรือความช่วยเหลือใด ๆ, เยี่ยมชม [ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).

### 5. มีการทดลองใช้ฟรีหรือไม่?
มี, คุณสามารถสำรวจการทดลองใช้ฟรีได้จาก [ที่นี่](https://releases.aspose.com/).

**Additional Q&A**

**Q: ฉันสามารถปรับแต่งไอคอนของแท็กได้หรือไม่?**  
A: ได้ – Aspose.Note มีไอคอนที่กำหนดไว้ล่วงหน้าหลายแบบผ่าน `TagIcon` และยังรองรับการใช้รูปภาพกำหนดเอง.

**Q: ฉันจะเปลี่ยนการตั้งค่าเอาต์พุตของ PDF ได้อย่างไร?**  
A: ใช้ `PdfSaveOptions` เพื่อควบคุมคุณภาพภาพ, การบีบอัด, และความปลอดภัยก่อนเรียก `doc.save`.

**Q: สามารถเพิ่มหลายแท็กให้กับข้อความเดียวกันได้หรือไม่?**  
A: แน่นอน. เรียก `text.getTags().add()` หลายครั้งพร้อมอินสแตนซ์ `NoteTag` ที่แตกต่างกัน.

---

**Last Updated:** 2026-01-28  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}