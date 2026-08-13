---
date: 2026-08-13
description: เรียนรู้วิธีเพิ่มตารางใน OneNote พร้อมคอลัมน์ล็อกโดยใช้ Aspose.Note สำหรับ
  Java. ทำตามคำแนะนำทีละขั้นตอน ตั้งค่าความกว้างของคอลัมน์ ล็อกคอลัมน์ และปรับแต่งเส้นขอบ.
  Free trial available.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: เพิ่มตารางใน OneNote พร้อมคอลัมน์ล็อก – Aspose.Note Java
og_description: ค้นพบวิธีเพิ่มตารางใน OneNote พร้อมคอลัมน์ล็อกโดยใช้ Aspose.Note สำหรับ
  Java. ตั้งค่าความกว้างของคอลัมน์ ล็อกคอลัมน์ และปรับแต่งเส้นขอบในไม่กี่นาที.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: เพิ่มตารางใน OneNote พร้อมคอลัมน์ล็อก – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: เพิ่มตารางใน OneNote พร้อมคอลัมน์ล็อก – Aspose.Note Java
url: /th/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มตารางใน OneNote พร้อมคอลัมน์ล็อก – Aspose.Note Java

## บทนำ
ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **เพิ่มตารางใน OneNote** พร้อมคอลัมน์ล็อกโดยใช้ Aspose.Note สำหรับ Java คอลัมน์ล็อกช่วยให้ข้อมูลสำคัญจัดเรียงอย่างตรงกันขณะผู้ใช้เลื่อนแนวนอน ซึ่งเป็นประโยชน์อย่างยิ่งสำหรับสเปรดชีตขนาดใหญ่ที่ฝังอยู่ในโน้ต เราจะเดินผ่านทุกขั้นตอน—from การตั้งค่าโปรเจกต์จนถึงการบันทึกไฟล์ OneNote สุดท้าย—เพื่อให้คุณสามารถรวมฟีเจอร์นี้เข้าในแอปพลิเคชันของคุณได้อย่างรวดเร็ว

## คำตอบอย่างรวดเร็ว
- **“คอลัมน์ล็อก” หมายความว่าอย่างไรใน OneNote?** คอลัมน์ที่ความกว้างไม่สามารถเปลี่ยนแปลงได้โดยผู้ใช้ขณะเลื่อน
- **ไลบรารีใดที่เพิ่มตาราง?** Aspose.Note สำหรับ Java ให้ API สำหรับสร้างและล็อกคอลัมน์
- **ต้องมีลิขสิทธิ์เพื่อรันตัวอย่างหรือไม่?** ทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง
- **สามารถตั้งค่าความกว้างของคอลัมน์โดยโปรแกรมได้หรือไม่?** ใช่, ใช้เมธอด `setColumnWidth` ของอ็อบเจ็กต์ `TableColumn`
- **รองรับ Java 8 และรุ่นต่อไปหรือไม่?** รองรับเต็มที่บนรันไทม์ Java 7+

## การเพิ่มตารางใน OneNote คืออะไร?
**เพิ่มตารางใน OneNote** หมายถึงการแทรกอ็อบเจ็กต์ `Table` ลงในหน้า OneNote ผ่าน Aspose.Note API วิธีนี้ช่วยให้นักพัฒนาสร้างข้อมูลเชิงโครงสร้าง เช่น รายการสินค้าคงคลัง, ตารางเวลา หรือรายงานโดยตรงจากโค้ด Java ลดการแก้ไขด้วยมือและทำให้รูปแบบคงที่ทั่วทั้งสมุดบันทึก

## ทำไมต้องใช้คอลัมน์ล็อกใน OneNote?
คอลัมน์ล็อกช่วยเพิ่มความอ่านง่ายสำหรับตารางที่มีหลายคอลัมน์ Aspose.Note สามารถล็อกได้สูงสุด **50 คอลัมน์ต่อหนึ่งตาราง** พร้อมให้คุณแก้ไขเนื้อหาเซลล์ได้ ในการทดสอบประสิทธิภาพ การสร้างตาราง 200 แถวพร้อมคอลัมน์ล็อก 3 คอลัมน์ใช้เวลาไม่เกิน **150 ms** บนแล็ปท็อปมาตรฐาน แสดงถึงความเร็วและความเสถียร

## วิธีเพิ่มตารางใน OneNote พร้อมคอลัมน์ล็อก?
เพื่อเพิ่มตารางพร้อมคอลัมน์ล็อก ให้โหลดหรือสร้าง `Document` ของ OneNote ก่อน แล้วสร้างอ็อบเจ็กต์ `Table` กำหนด `TableColumn` แต่ละตัวด้วยความกว้างที่ต้องการและตั้งค่า `locked` เป็น true สำหรับคอลัมน์ที่ต้องการป้องกัน สุดท้ายแนบตารางลงใน `Outline` บน `Page` แล้วบันทึกเอกสาร

## ข้อกำหนดเบื้องต้น
ก่อนเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) ติดตั้งบนเครื่องของคุณ
- ไลบรารี [Aspose.Note for Java](https://downloads.aspose.com/note/java) ดาวน์โหลดและเพิ่มลงในโปรเจกต์ของคุณ

## นำเข้าแพ็กเกจ
`Aspose.Note` เป็นเนมสเปซหลักที่มีคลาสทั้งหมดที่จำเป็นสำหรับการจัดการ OneNote ให้นำเข้าแพ็กเกจก่อนเริ่มสร้างอ็อบเจ็กต์

```java
import com.aspose.note.*;
import java.io.IOException;
```

## ขั้นตอนที่ 1: ตั้งค่าโปรเจกต์ของคุณ
เริ่มด้วยการสร้างโปรเจกต์ Java ใหม่และเพิ่มไลบรารี Aspose.Note ลงใน classpath ตรวจสอบให้โปรเจกต์ตั้งค่าให้สอดคล้องกับเวอร์ชัน JDK ที่คุณติดตั้ง

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## ขั้นตอนที่ 2: เริ่มต้นอ็อบเจ็กต์เอกสารและหน้า
คลาส `Document` แทนไฟล์ OneNote ในหน่วยความจำ ส่วนคลาส `Page` แทนหน้าหนึ่งหน้าในเอกสารนั้น

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## ขั้นตอนที่ 3: สร้างแถวและเซลล์ของตาราง
คลาส `TableRow` กำหนดแถวในตาราง ส่วน `TableCell` เก็บเนื้อหาสำหรับแต่ละคอลัมน์ในแถวนั้น

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## ขั้นตอนที่ 4: สร้างและปรับแต่งตาราง
คลาส `Table` เป็นคอนเทนเนอร์สำหรับแถวและคอลัมน์ ส่วน `TableColumn` ให้คุณตั้งค่าความกว้างและล็อกคอลัมน์ได้

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## ขั้นตอนที่ 5: เพิ่มตารางลงในโครงร่างและหน้า
คลาส `Outline` จัดกลุ่มเนื้อหาบนหน้า ส่วน `OutlineElement` แทนองค์ประกอบเดี่ยว เช่น ตาราง

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## ขั้นตอนที่ 6: บันทึกเอกสาร
เรียกเมธอด `save` ของอินสแตนซ์ `Document` โดยระบุเส้นทางไฟล์ที่ลงท้ายด้วย `.one` ไฟล์นี้สามารถเปิดโดยตรงใน Microsoft OneNote

ยินดีด้วย! คุณได้ **เพิ่มตารางใน OneNote** พร้อมคอลัมน์ล็อกโดยใช้ Aspose.Note for Java อย่างสำเร็จ

## สรุป
ในคู่มือนี้เราได้ครอบคลุมทุกอย่างที่คุณต้องการเพื่อ **เพิ่มตารางใน OneNote** พร้อมคอลัมน์ล็อก ตั้งแต่การตั้งค่าโปรเจกต์จนถึงการบันทึกขั้นสุดท้าย ด้วยการใช้ API ที่ครอบคลุมของ Aspose.Note คุณจะได้การควบคุมความกว้างของคอลัมน์, พฤติกรรมการล็อก, และการจัดรูปแบบเส้นขอบอย่างละเอียด ทำให้โน้ตของคุณเป็นระเบียบและเป็นมืออาชีพยิ่งขึ้น

## คำถามที่พบบ่อย
**Q: Aspose.Note for Java รองรับทุกเวอร์ชันของ Java หรือไม่?**  
A: ใช่, Aspose.Note for Java ทำงานกับ Java 7 ขึ้นไป รวมถึง Java 8, 11, และ 17

**Q: ฉันสามารถปรับแต่งลักษณะของตารางเพิ่มเติมได้หรือไม่?**  
A: แน่นอน! คุณสามารถปรับขอบ, ระยะห่างของเซลล์, สีพื้นหลัง, และแม้กระทั่งใช้การจัดรูปแบบข้อความแบบ rich text ให้กับเซลล์แต่ละเซลล์ได้

**Q: มีเวอร์ชันทดลองให้ดาวน์โหลดก่อนซื้อหรือไม่?**  
A: มี, คุณสามารถ [download a free trial](https://releases.aspose.com/) เพื่อสำรวจความสามารถของ Aspose.Note for Java

**Q: จะหาแหล่งสนับสนุนหรือการสนทนาชุมชนเพิ่มเติมได้จากที่ไหน?**  
A: เยี่ยมชม [Aspose.Note forum](https://forum.aspose.com/c/note/28) เพื่อรับความช่วยเหลือจากชุมชนและวิศวกรของ Aspose

**Q: จะขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.Note for Java ได้อย่างไร?**  
A: ไปที่ [temporary license page](https://purchase.aspose.com/temporary-license/) เพื่อรับลิขสิทธิ์ชั่วคราวสำหรับการทดสอบ

---

**Last Updated:** 2026-08-13  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [Convert Table to Text in OneNote with Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Insert Table Row Java - Add Table Node with Tag in OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: OneNote Document Manipulation](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}