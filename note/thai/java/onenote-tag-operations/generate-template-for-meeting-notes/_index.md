---
date: 2026-03-03
description: เรียนรู้วิธีสร้างโครงร่างใน OneNote และสร้างเทมเพลตบันทึกการประชุมด้วย
  Aspose.Note สำหรับ Java ปรับแต่งสไตล์ฟอนต์และเพิ่มช่องทำเครื่องหมายได้อย่างง่ายดาย.
linktitle: Create Outline in OneNote – Meeting Notes Template
second_title: Aspose.Note Java API
title: สร้างโครงร่างใน OneNote – แม่แบบบันทึกการประชุม
url: /th/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างโครงร่างใน OneNote – แม่แบบบันทึกการประชุม

## Introduction
ในโลกที่เร่งรีบในทุกวันนี้ การ **สร้างโครงร่างใน OneNote** อย่างมีประสิทธิภาพเป็นสิ่งสำคัญสำหรับการบันทึกการประชุมที่ชัดเจน Aspose.Note for Java มอบวิธีที่ทรงพลังในการ **สร้างแม่แบบบันทึกการประชุม** ที่คุณสามารถปรับแต่ง เพิ่มกล่องทำเครื่องหมาย และจัดรูปแบบฟอนต์ได้ตามต้องการ ในคู่มือขั้นตอนนี้ เราจะพาคุณผ่านการสร้างแม่แบบวาระการประชุมที่ใช้ซ้ำได้ โดยอธิบาย **วิธีเพิ่มกล่องทำเครื่องหมาย**, **เพิ่มรายการตรวจสอบใน OneNote**, และ **ปรับแต่งสไตล์ฟอนต์ใน OneNote** เพื่อให้ได้รูปลักษณ์ที่เรียบหรู

## Quick Answers
- **สร้างโครงร่างใน OneNote หมายถึงอะไร?** หมายถึงการสร้างโครงสร้างแบบลำดับขั้น (หัวเรื่อง, ส่วน, จุดหัวข้อ) ภายในไฟล์ OneNote ด้วยโปรแกรม  
- **ไลบรารีใดที่ช่วยในเรื่องนี้?** Aspose.Note for Java.  
- **ฉันสามารถเพิ่มกล่องทำเครื่องหมายในโครงร่างได้หรือไม่?** ใช่ – ใช้ `NoteCheckBox.createBlueCheckBox()`.  
- **ฉันต้องการใบอนุญาตหรือไม่?** มีรุ่นทดลองใช้ฟรี; จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 ขึ้นไป.  

## What is “create outline in OneNote”?
การสร้างโครงร่างใน OneNote หมายถึงการกำหนดหน้าที่มีหัวเรื่อง, ส่วนโครงร่างหลายส่วน, และตัวเลือกการจัดลำดับรายการหรือกล่องทำเครื่องหมาย โครงสร้างนี้สะท้อนวิธีที่คุณพิมพ์หัวเรื่องและจุดหัวข้อด้วยตนเองใน UI ของ OneNote แต่จะถูกสร้างโดยอัตโนมัติด้วยโค้ด

## Why use Aspose.Note for meeting agenda templates?
- **ความสอดคล้อง:** การประชุมทุกครั้งเริ่มต้นด้วยรูปแบบที่เรียบง่ายและเหมือนกัน  
- **การอัตโนมัติ:** ลดการพิมพ์ด้วยมือและรับประกันว่ามีส่วนที่จำเป็นทั้งหมด (วาระ, รายการดำเนินการ, บันทึก) อยู่  
- **การปรับแต่ง:** เปลี่ยนฟอนต์, สี, และเพิ่มกล่องทำเครื่องหมายแบบโต้ตอบเพื่อจัดการงาน  
- **การบูรณาการ:** ทำงานกับ IDE ของ Java ใดก็ได้และสามารถรวมกับไลบรารี Aspose อื่น ๆ สำหรับ PDF, สเปรดชีต ฯลฯ  

## Prerequisites
- ความเข้าใจพื้นฐานของการเขียนโปรแกรม Java  
- ไลบรารี Aspose.Note for Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/note/java/).  
- IDE เช่น Eclipse หรือ IntelliJ IDEA  

## Import Packages
ขั้นแรกให้ทำการนำเข้าคลาสที่เราต้องการใช้ ส่วนโค้ดนี้จะคงเหมือนเดิมตามบทแนะนำต้นฉบับ.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Step 1: Create Document Structure
เราจะเริ่มโดยสร้างเอกสาร ตั้งค่าหัวเรื่อง และเตรียมสไตล์ย่อหน้าที่จะช่วยให้เราสามารถ **ปรับแต่งสไตล์ฟอนต์ใน OneNote** ได้ในภายหลัง.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*สิ่งที่เราทำ:*  
- กำหนดอ็อบเจ็กต์ `ParagraphStyle` สองตัว (`headerStyle` สำหรับหัวเรื่อง, `bodyStyle` สำหรับข้อความปกติ).  
- สร้าง `Document` และเพิ่ม `Title` ที่รวมวันที่ปัจจุบัน เพื่อให้หน้ามีหัวเรื่องที่ชัดเจน.  

## Step 2: Outline Important Points
ต่อไป เรา **สร้างโครงร่างใน OneNote** โดยเพิ่มอ็อบเจ็กต์ `Outline` และใส่ส่วนต่าง ๆ เช่น “Important”. ที่นี่คือที่รายการวาระจะอยู่.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*เหตุผลที่สำคัญ:*  
- อ็อบเจ็กต์ `Outline` แทนรายการแบบลำดับขั้นที่คุณเห็นใน OneNote.  
- โดยใช้ `createListNumberingStyle` เราสร้างรายการลำดับเลขที่สามารถเริ่มใหม่ได้สำหรับแต่ละส่วนใหม่.  

## Step 3: Highlight Action Items (How to add checkboxes)
รายการดำเนินการต้องการสัญญาณภาพ โดยการแนบแท็กกล่องทำเครื่องหมายไปยังแต่ละองค์ประกอบ `RichText` เราจะทำให้ **วิธีเพิ่มกล่องทำเครื่องหมาย** สามารถทำได้โดยตรงในโครงร่าง.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*เคล็ดลับ:* ใช้ `NoteCheckBox.createBlueCheckBox()` เพื่อสร้างกล่องทำเครื่องหมายสีน้ำเงิน; มีสีอื่น ๆ ให้เลือกหากต้องการสไตล์ภาพที่แตกต่าง  

## Step 4: Save the Document
สุดท้าย ให้บันทึกไฟล์ OneNote ลงดิสก์ ไฟล์นี้สามารถเปิดโดยตรงในแอป OneNote บนเดสก์ท็อป.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Common Issues and Solutions
| ปัญหา | วิธีแก้ |
|-------|----------|
| **กล่องทำเครื่องหมายไม่แสดง** | ตรวจสอบว่าคุณได้เรียก `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` หลังจากตั้งค่าสไตล์ย่อหน้าแล้ว. |
| **ฟอนต์แสดงผลแตกต่างใน OneNote** | ตรวจสอบว่าชื่อฟอนต์ (เช่น “Calibri”) ติดตั้งอยู่บนเครื่องที่ OneNote เปิดไฟล์ |
| **โครงร่างไม่เยื้อง** | ปรับ `setVerticalOffset` และ `setHorizontalOffset` บนอ็อบเจ็กต์ `Outline` |
| **การจัดลำดับเลขเริ่มใหม่โดยไม่คาดคิด** | ใช้ `restartFlag` อย่างถูกต้อง; ตั้งค่าเป็น `true` เฉพาะรายการแรกในส่วนใหม่. |

## Frequently Asked Questions
### ฉันสามารถปรับแต่งสไตล์ฟอนต์ในบันทึกการประชุมของฉันได้หรือไม่?
ได้, Aspose.Note อนุญาตให้คุณกำหนดสไตล์ฟอนต์แบบกำหนดเองสำหรับหัวเรื่องและข้อความหลัก.

### Aspose.Note เข้ากันได้กับไลบรารี Java อื่นหรือไม่?
Aspose.Note สามารถบูรณาการกับไลบรารี Java อื่น ๆ ได้อย่างราบรื่นเพื่อเพิ่มฟังก์ชันการทำงาน

### ฉันจะเพิ่มส่วนเพิ่มเติมในบันทึกการประชุมได้อย่างไร?
คุณสามารถขยายโครงสร้างโครงร่างได้อย่างง่ายดายโดยทำตามรูปแบบเดียวกันที่แสดงในบทแนะนำ

### มีข้อพิจารณาเรื่องใบอนุญาตสำหรับ Aspose.Note หรือไม่?
ดูรายละเอียดใบอนุญาตได้ที่ [เอกสาร Aspose.Note](https://reference.aspose.com/note/java/)

### มีเวอร์ชันทดลองใช้สำหรับ Aspose.Note หรือไม่?
มี, คุณสามารถเข้าถึง [รุ่นทดลองใช้ฟรีที่นี่](https://releases.aspose.com/)

## FAQ
**ถาม: ฉันจะเพิ่มรายการตรวจสอบใน OneNote โดยไม่ใช้กล่องทำเครื่องหมายได้อย่างไร?**  
ตอบ: คุณสามารถสร้างรายการแบบหัวข้อย่อยและทำเครื่องหมายรายการด้วยตนเอง, แต่การใช้ `NoteCheckBox` จะให้กล่องทำเครื่องหมายแบบโต้ตอบที่ซิงค์กับ UI ของ OneNote.

**ถาม: ฉันสามารถใช้แม่แบบนี้เพื่อสร้างแม่แบบวาระการประชุมสำหรับการทำซ้ำรายสัปดาห์ได้หรือไม่?**  
ตอบ: แน่นอน. เพียงเปลี่ยนรูปแบบวันที่หรือส่งสตริงหัวเรื่องที่กำหนดเองเพื่อใช้โครงสร้างเดียวกันในแต่ละสัปดาห์.

**ถาม: วิธีที่ดีที่สุดในการ **ปรับแต่งสไตล์ฟอนต์ใน OneNote** สำหรับการสร้างแบรนด์คืออะไร?**  
ตอบ: กำหนดอ็อบเจ็กต์ `ParagraphStyle` ด้วยชื่อฟอนต์ของบริษัท, ขนาด, และสี, แล้วนำไปใช้กับแต่ละองค์ประกอบ `RichText` ตามที่แสดงในขั้นตอน 1.

**ถาม: Aspose.Note รองรับการส่งออกโครงร่างเป็น PDF หรือไม่?**  
ตอบ: ใช่. หลังจากบันทึกไฟล์ OneNote, คุณสามารถโหลดด้วย Aspose.Note และส่งออกเป็น PDF โดยใช้ `Document.save("output.pdf", SaveFormat.Pdf)`.

**ถาม: มีวิธีใดที่จะทำเครื่องหมายกล่องทำเครื่องหมายว่าเสร็จสมบูรณ์โดยโปรแกรมได้หรือไม่?**  
ตอบ: คุณสามารถตั้งค่าสถานะของกล่องทำเครื่องหมายโดยเพิ่มแท็ก `NoteCheckBox` ที่มีคุณสมบัติ `Checked` ตั้งค่าเป็น `true`.

---

**อัปเดตล่าสุด:** 2026-03-03  
**ทดสอบกับ:** Aspose.Note for Java 24.11 (รุ่นล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}