---
date: 2026-03-05
description: เรียนรู้การจัดรูปแบบตาราง OneNote ด้วย Aspose.Note สำหรับ Java คู่มือนี้แสดงวิธีตั้งค่าสีพื้นหลังของเซลล์,
  ใช้พื้นหลังเซลล์, และเปลี่ยนสีเซลล์ OneNote อย่างง่ายดาย.
linktitle: 'Onenote Table Formatting: Setting Cell Background Color with Aspose.Note'
second_title: Aspose.Note Java API
title: 'การจัดรูปแบบตารางใน OneNote: การตั้งค่าสีพื้นหลังของเซลล์ด้วย Aspose.Note'
url: /th/java/onenote-table-manipulation/setting-cell-background-color/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การจัดรูปแบบตาราง Onenote: ตั้งค่าสีพื้นหลังของเซลล์

## Introduction
ในบทเรียนนี้คุณจะได้ค้นพบวิธีทำ **onenote table formatting** โดยการตั้งค่าสีพื้นหลังของเซลล์ด้วย Aspose.Note for Java ไม่ว่าคุณจะสร้างรายงาน คู่มือการศึกษา หรือสมุดบันทึกแบบทำงานร่วมกัน การปรับสีเซลล์ช่วยให้คุณเน้นข้อมูลสำคัญและเพิ่มความอ่านง่าย มาดำเนินการตามขั้นตอนร่วมกัน

## Quick Answers
- **ต้องการไลบรารีอะไร?** Aspose.Note for Java.  
- **เมธอดใดที่เปลี่ยนสี?** `setBackgroundColor(Color)` บน `TableCell`.  
- **สามารถใช้สีกับหลายเซลล์ได้หรือไม่?** ได้ – วนลูปผ่านแถวและเซลล์.  
- **ต้องใช้ไลเซนส์สำหรับการผลิตหรือไม่?** จำเป็นต้องมีไลเซนส์ Aspose ที่ถูกต้อง; มีรุ่นทดลองฟรีให้ใช้.  
- **รองรับเวอร์ชัน Java ใด?** Java 8+ (หรือใหม่กว่า) ทำงานกับรุ่นล่าสุดของ Aspose.Note.

## What is onenote table formatting?
Onenote table formatting หมายถึงชุดของตัวเลือกการจัดสไตล์—เช่น เส้นขอบ การจัดแนว และสีพื้นหลัง—ที่คุณสามารถนำไปใช้กับตารางภายในหน้า OneNote การปรับสีพื้นหลังของเซลล์เป็นวิธีทั่วไปในการดึงความสนใจไปยังข้อมูลสำคัญ

## Why set cell background color in OneNote?
- **Visual hierarchy:** เน้นผลรวม คำเตือน หรือหัวข้อส่วน.  
- **Brand consistency:** ทำให้สีของบริษัทสอดคล้องกันในเอกสาร.  
- **Readability:** ทำให้ตารางที่หนาแน่นอ่านง่ายขึ้น โดยเฉพาะบนหน้าจอขนาดใหญ่.  

## Prerequisites
ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อม:
1. Aspose.Note for Java Library: ดาวน์โหลดและติดตั้งจาก [here](https://releases.aspose.com/note/java/).  
2. Java Development Environment: ตั้งค่าสภาพแวดล้อมการพัฒนา Java ของคุณ.  
3. Document Directory: มีโฟลเดอร์พร้อมที่เก็บเอกสาร OneNote ของคุณ.  

ตอนนี้มาดำดิ่งสู่บทเรียนกันเลย!

## Import Packages
เริ่มต้นโดยการนำเข้าแพ็กเกจที่จำเป็นเข้าสู่โครงการ Java ของคุณ:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.OutlineElement;
import com.aspose.note.RichText;
import com.aspose.note.TableCell;
import com.aspose.note.TableRow;
import com.aspose.note.ParagraphStyle;
```

## How to set cell background color in OneNote tables?
### Step 1: Set up Your Project
ตรวจสอบให้แน่ใจว่าสภาพแวดล้อมการพัฒนา Java ของคุณพร้อมใช้งานและคุณได้รวม Aspose.Note for Java เข้าในโครงการของคุณแล้ว

### Step 2: Load Your OneNote Document
```java
Document doc = new Document();
```

### Step 3: Initialize TableRow Object
สร้างอ็อบเจ็กต์ `TableRow` เพื่อเป็นตัวแทนของแถวในตาราง OneNote ของคุณ:
```java
TableRow row1 = new TableRow();
```

### Step 4: Initialize TableCell Object
เริ่มต้นอ็อบเจ็กต์ `TableCell` ภายในแถวและกำหนดเนื้อหาข้อความที่ต้องการ:
```java
TableCell cell11 = new TableCell();
cell11.appendChildLast(GetOutlineElementWithText("Small text"));
```

### Step 5: Set Cell Background Color
ใช้เมธอด `setBackgroundColor` เพื่อกำหนดสีพื้นหลังของเซลล์ (ในตัวอย่างนี้ตั้งเป็นสีดำ):
```java
cell11.setBackgroundColor(Color.BLACK);
```

### Step 6: Save Your Document
อย่าลืมบันทึกเอกสาร OneNote ที่แก้ไขแล้วหลังจากทำการเปลี่ยนแปลงที่จำเป็น

> **Pro tip:** หากต้องการใช้สีพื้นหลังเดียวกันกับคอลัมน์ทั้งหมด ให้วนลูปผ่านแต่ละแถวและเรียก `setBackgroundColor` บนเซลล์ที่สอดคล้องกัน

## How to apply cell background color to multiple cells?
คุณสามารถวนลูปผ่านแถวและเซลล์ของตาราง เพื่อนำการเรียก `setBackgroundColor` ไปใช้ในที่ที่ต้องการ วิธีนี้มีประสิทธิภาพเมื่อคุณทำงานกับตารางขนาดใหญ่หรืออยากทำสีโค้ดให้กับส่วนทั้งหมด

## How to change onenote cell color programmatically?
นอกจากสีทึบแล้ว Aspose.Note ยังรองรับค่ารหัสสี RGB แบบกำหนดเอง เปลี่ยน `Color.BLACK` เป็น `new Color(r, g, b)` เพื่อให้ตรงกับพาเลตสีของแบรนด์ใดก็ได้

## Common Issues and Solutions
- **NullPointerException when accessing a cell:** ตรวจสอบให้แน่ใจว่าเซลล์ได้ถูกเพิ่มเข้าแถวก่อนตั้งค่าสีพื้นหลัง.  
- **Color not appearing after save:** ยืนยันว่าคุณบันทึกเอกสารด้วย `doc.save("output.one")` และเวอร์ชัน OneNote ปลายทางรองรับการจัดสไตล์ตาราง.  
- **License errors:** รุ่นทดลองใช้ได้สำหรับการประเมินผล แต่ต้องมีไลเซนส์เต็มสำหรับการใช้งานในสภาพแวดล้อมการผลิต.

## Frequently Asked Questions

**Q: Can I apply this method to multiple cells at once?**  
A: ใช่ คุณสามารถวนลูปผ่านแถวและเซลล์ของตารางเพื่อใช้สีพื้นหลังกับหลายเซลล์พร้อมกันได้

**Q: Are there predefined colors I can use?**  
A: Aspose.Note รองรับสีหลากหลาย รวมถึงค่าสีที่กำหนดไว้ล่วงหน้าเช่น `Color.BLACK`. ตรวจสอบเอกสาร [here](https://reference.aspose.com/note/java/) สำหรับรายการเต็ม

**Q: Is there a trial version available?**  
A: มี คุณสามารถรับรุ่นทดลองฟรีได้ [here](https://releases.aspose.com/)

**Q: How can I get support if I encounter issues?**  
A: เยี่ยมชมฟอรั่มสนับสนุน [here](https://forum.aspose.com/c/note/28) เพื่อรับความช่วยเหลือจากชุมชน Aspose

**Q: Where can I purchase Aspose.Note for Java?**  
A: คุณสามารถซื้อไลบรารีได้ [here](https://purchase.aspose.com/buy)

## Conclusion
ขอแสดงความยินดี! คุณได้เรียนรู้วิธีทำ **onenote table formatting** โดยการตั้งค่าสีพื้นหลังของเซลล์ใน OneNote ด้วย Aspose.Note for Java แล้ว ทดลองใช้สีต่าง ๆ ประยุกต์เทคนิคนี้กับแถวหรือคอลัมน์ทั้งหมด และผสานเข้ากับกระบวนการรายงานอัตโนมัติของคุณเพื่อให้ได้ผลลัพธ์ที่ดูเป็นมืออาชีพและสวยงาม

---

**อัปเดตล่าสุด:** 2026-03-05  
**ทดสอบด้วย:** Aspose.Note for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}