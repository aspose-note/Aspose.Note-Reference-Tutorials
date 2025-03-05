---
title: แทรกตารางใน OneNote - Aspose.Note
linktitle: แทรกตารางใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีแทรกตารางใน OneNote โดยใช้ Aspose.Note สำหรับ Java คำแนะนำทีละขั้นตอนสำหรับการสร้างเนื้อหาแบบไดนามิก ปรับปรุงเอกสารของคุณได้อย่างง่ายดาย
type: docs
weight: 16
url: /th/java/onenote-table-manipulation/insert-table/
---
## การแนะนำ
หากคุณต้องการปรับปรุงเอกสาร OneNote ของคุณด้วยการแทรกตารางโดยทางโปรแกรม Aspose.Note for Java คือโซลูชันที่เหมาะกับคุณ ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแทรกตารางลงในเอกสาร OneNote โดยใช้ไลบรารี Java อันทรงพลังของ Aspose.Note
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณ
-  Aspose.Note สำหรับ Java: ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note สำหรับ Java จาก[ที่นี่](https://releases.aspose.com/note/java/).
## แพ็คเกจนำเข้า
เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ แพ็คเกจเหล่านี้จำเป็นสำหรับการใช้คุณสมบัติของ Aspose.Note สำหรับ Java
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException
```

## ขั้นตอนที่ 1: สร้างเอกสาร OneNote
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory";
Document doc = new Document();
// ... (คำชี้แจงการนำเข้าอื่น ๆ )
// ... (โค้ดที่เหลือ)
```
## ขั้นตอนที่ 2: เตรียมใช้งานเอกสาร หน้า และตาราง
```java
// เริ่มต้นวัตถุคลาสหน้า
Page page = new Page();
// เริ่มต้นวัตถุคลาส TableRow
TableRow row1 = new TableRow();
// เตรียมใช้งานวัตถุคลาส TableCell
TableCell cell11 = new TableCell();
TableCell cell12 = new TableCell();
TableCell cell13 = new TableCell();
// ... (โค้ดสำหรับต่อท้ายองค์ประกอบโครงร่างในเซลล์ตาราง)
// ผนวกเซลล์ตารางเข้ากับแถว
row1.appendChildLast(cell11);
row1.appendChildLast(cell12);
row1.appendChildLast(cell13);
// ... (โค้ดสำหรับเตรียมใช้งานและต่อท้ายแถวอื่นๆ)
// เริ่มต้นวัตถุคลาสตารางและตั้งค่าความกว้างของคอลัมน์
Table table = new Table();
table.setBordersVisible(true);
// ... (โค้ดสำหรับเพิ่มคอลัมน์)
// ผนวกแถวของตารางเข้ากับตาราง
table.appendChildLast(row1);
table.appendChildLast(row2);
// ... (โค้ดสำหรับเพิ่มตารางไปยังโหนดองค์ประกอบเค้าร่าง)
```
## ขั้นตอนที่ 3: เริ่มต้นโครงร่างและ OutlineElement
```java
//เริ่มต้นวัตถุเค้าร่าง
Outline outline = new Outline();
// เริ่มต้นวัตถุ OutlineElement
OutlineElement outlineElem = new OutlineElement();
// ... (โค้ดสำหรับเพิ่มตารางไปยังโหนดองค์ประกอบเค้าร่าง)
// เพิ่มองค์ประกอบโครงร่างเพื่อร่าง
outline.appendChildLast(outlineElem);
// เพิ่มเค้าร่างให้กับโหนดหน้า
page.appendChildLast(outline);
// เพิ่มหน้าไปยังโหนดเอกสาร
doc.appendChildLast(page);
dataDir = dataDir + "InsertTable_out.one";
doc.save(dataDir);
```
## ขั้นตอนที่ 4: รับ OutlineElement พร้อมข้อความ
```java
public static OutlineElement GetOutlineElementWithText(String text)
{
    OutlineElement outlineElem = new OutlineElement();
    ParagraphStyle textStyle = new ParagraphStyle()
                                        .setFontColor(Color.BLACK)
                                        .setFontName("Arial")
                                        .setFontSize(10);
    RichText richText = new RichText().append(text);
    richText.setParagraphStyle(textStyle);
    outlineElem.appendChildLast(richText);
    return outlineElem;
} 
```
## บทสรุป
ยินดีด้วย! คุณได้เรียนรู้วิธีแทรกตารางลงในเอกสาร OneNote โดยใช้ Aspose.Note for Java เรียบร้อยแล้ว ไลบรารีอันทรงพลังนี้มีฟังก์ชันการทำงานที่ครอบคลุม ช่วยให้คุณสร้างเนื้อหาแบบไดนามิกและน่าสนใจโดยทางโปรแกรม
## คำถามที่พบบ่อย
### ถาม: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของตารางโดยใช้ Aspose.Note สำหรับ Java ได้หรือไม่
ตอบ: ได้ คุณสามารถปรับแต่งลักษณะต่างๆ ได้ รวมถึงเส้นขอบ ความกว้างของคอลัมน์ และการจัดรูปแบบเซลล์
### ถาม: Aspose.Note สำหรับ Java เหมาะสำหรับทั้งโปรเจ็กต์ส่วนตัวและเชิงพาณิชย์หรือไม่
ตอบ: ได้ Aspose.Note สำหรับ Java สามารถใช้ได้ทั้งในโครงการส่วนบุคคลและเชิงพาณิชย์
### ถาม: ฉันจะรับการสนับสนุนเพิ่มเติมสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน
 ตอบ: เยี่ยมชม[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) สำหรับการสนับสนุนและการอภิปรายของชุมชน
### ถาม: ฉันสามารถลองใช้ Aspose.Note สำหรับ Java ก่อนซื้อได้หรือไม่
 ตอบ: ได้ คุณสามารถสำรวจห้องสมุดได้ด้วย[ทดลองฟรี](https://releases.aspose.com/).
### ถาม: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร
 ตอบ: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).