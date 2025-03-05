---
title: สร้างตารางที่มีคอลัมน์ที่ถูกล็อคใน OneNote - Aspose.Note
linktitle: สร้างตารางที่มีคอลัมน์ที่ถูกล็อคใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: ปรับปรุงประสบการณ์ OneNote ของคุณด้วย Aspose.Note สำหรับ Java เรียนรู้วิธีสร้างตารางที่มีคอลัมน์ที่ถูกล็อกโดยใช้คำแนะนำทีละขั้นตอน ดาวน์โหลดทดลองใช้ฟรีตอนนี้!
type: docs
weight: 12
url: /th/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## การแนะนำ
OneNote เป็นเครื่องมือที่มีประสิทธิภาพสำหรับการจัดระเบียบข้อมูล และ Aspose.Note สำหรับ Java ช่วยเพิ่มขีดความสามารถโดยมอบวิธีที่ราบรื่นในการสร้างตารางที่มีคอลัมน์ที่ถูกล็อก ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการใช้ Aspose.Note สำหรับ Java เพื่อสร้างตารางที่มีคอลัมน์ที่ถูกล็อคใน OneNote
## ข้อกำหนดเบื้องต้น
ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- [ชุดพัฒนาจาวา (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)ติดตั้งบนเครื่องของคุณ
- [Aspose.Note สำหรับ Java](https://downloads.aspose.com/note/java) ดาวน์โหลดและเพิ่มไลบรารีลงในโครงการของคุณแล้ว
## แพ็คเกจนำเข้า
ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นสำหรับการทำงานกับ Aspose หมายเหตุ:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ
เริ่มต้นด้วยการสร้างโปรเจ็กต์ Java ใหม่และเพิ่มไลบรารี Aspose.Note ให้กับ classpath ของคุณ ตรวจสอบให้แน่ใจว่าโปรเจ็กต์ของคุณได้รับการกำหนดค่าให้ใช้ JDK
## ขั้นตอนที่ 2: เริ่มต้นเอกสารและออบเจ็กต์หน้า
```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory";
//สร้างวัตถุของคลาสเอกสาร
Document doc = new Document();
// เริ่มต้นวัตถุคลาสหน้า
Page page = new Page();
```
## ขั้นตอนที่ 3: สร้างแถวและเซลล์ของตาราง
```java
// เริ่มต้นวัตถุคลาส TableRow
TableRow row1 = new TableRow();
// เริ่มต้นวัตถุคลาส TableCell และตั้งค่าเนื้อหาข้อความ
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// เริ่มต้นวัตถุคลาส TableRow
TableRow row2 = new TableRow();
// เริ่มต้นวัตถุคลาส TableCell และตั้งค่าเนื้อหาข้อความ
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## ขั้นตอนที่ 4: สร้างและปรับแต่งตาราง
```java
// เริ่มต้นวัตถุคลาสตาราง
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// เพิ่มแถว
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## ขั้นตอนที่ 5: เพิ่มตารางลงในโครงร่างและหน้า
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// เพิ่มโหนดตาราง
outlineElem.appendChildLast(table);
// เพิ่มโหนดองค์ประกอบเค้าร่าง
outline.appendChildLast(outlineElem);
// เพิ่มโหนดเค้าร่าง
page.appendChildLast(outline);
// เพิ่มโหนดหน้า
doc.appendChildLast(page);
```
## ขั้นตอนที่ 6: บันทึกเอกสาร
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
ยินดีด้วย! คุณสร้างตารางที่มีคอลัมน์ที่ถูกล็อคใน OneNote สำเร็จแล้วโดยใช้ Aspose.Note for Java
## บทสรุป
ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการใช้ Aspose.Note สำหรับ Java เพื่อปรับปรุงประสบการณ์ OneNote ของคุณโดยการสร้างตารางที่มีคอลัมน์ที่ถูกล็อค ฟังก์ชันนี้จะเพิ่มการจัดระเบียบและโครงสร้างเลเยอร์ใหม่ให้กับบันทึกย่อของคุณ
## คำถามที่พบบ่อย
### Aspose.Note สำหรับ Java เข้ากันได้กับ Java เวอร์ชันทั้งหมดหรือไม่
ใช่ Aspose.Note สำหรับ Java เข้ากันได้กับ Java 6 และเวอร์ชันที่ใหม่กว่า
### ฉันสามารถปรับแต่งลักษณะที่ปรากฏของตารางเพิ่มเติมได้หรือไม่?
อย่างแน่นอน! Aspose.Note for Java มีตัวเลือกมากมายสำหรับการปรับแต่งตาราง เช่น การปรับเส้นขอบ ระยะห่างเซลล์ และอื่นๆ
### มีรุ่นทดลองใช้ก่อนซื้อหรือไม่?
 ใช่คุณสามารถ[ดาวน์โหลดรุ่นทดลองใช้ฟรี](https://releases.aspose.com/) เพื่อสำรวจความสามารถของ Aspose.Note สำหรับ Java
### ฉันจะรับการสนับสนุนเพิ่มเติมหรือการสนทนาในชุมชนได้จากที่ไหน
 เยี่ยมชม[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) สำหรับการสนับสนุนและการอภิปรายในชุมชน
### ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร
 เยี่ยม[ลิงค์นี้](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราวเพื่อการทดสอบ