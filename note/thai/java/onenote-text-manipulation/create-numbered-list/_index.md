---
title: สร้างรายการลำดับเลขใน OneNote - Aspose.Note
linktitle: สร้างรายการลำดับเลขใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีสร้างรายการลำดับเลขใน OneNote ด้วย Aspose.Note for Java ได้อย่างง่ายดาย ดาวน์โหลดรุ่นทดลองใช้ฟรีและดำดิ่งสู่โลกแห่งการพัฒนา Java!
type: docs
weight: 14
url: /th/java/onenote-text-manipulation/create-numbered-list/
---
## การแนะนำ
Aspose.Note สำหรับ Java ช่วยให้นักพัฒนา Java สามารถทำงานกับไฟล์ Microsoft OneNote ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการสร้างรายการลำดับเลขใน OneNote ด้วย Aspose.Note สำหรับไลบรารี Java อันทรงพลัง
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน โปรดตรวจสอบให้แน่ใจว่าได้มีข้อกำหนดเบื้องต้นต่อไปนี้:
- ติดตั้ง Java Development Kit (JDK) บนเครื่องของคุณแล้ว
-  Aspose.Note สำหรับไลบรารี Java ที่ดาวน์โหลดมาจาก[ที่นี่](https://releases.aspose.com/note/java/).
## การนำเข้าแพ็คเกจ
ขั้นแรก เรามานำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณเพื่อใช้ประโยชน์สูงสุดจากฟังก์ชัน Aspose.Note รวมรหัสต่อไปนี้ในโครงการของคุณ:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## ขั้นตอนที่ 1: การเริ่มต้นเอกสาร หน้า และออบเจ็กต์เค้าร่าง
```java
// ไดเร็กทอรีเอกสารของคุณ
String dataDir = "Your Document Directory";
// สร้างออบเจ็กต์เอกสาร หน้า และเค้าร่าง
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// ตั้งค่ารูปแบบข้อความเริ่มต้น
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## ขั้นตอนที่ 2: การตั้งค่าสไตล์ข้อความเริ่มต้น
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## ขั้นตอนที่ 3: การสร้างองค์ประกอบเค้าร่าง
ตอนนี้ เรามาสร้างองค์ประกอบสำหรับรายการลำดับเลขของคุณกันดีกว่า
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// ทำซ้ำสำหรับองค์ประกอบอื่น ๆ (outlineElem2 และ outlineElem3)
```
## ขั้นตอนที่ 4: การเพิ่มองค์ประกอบโครงร่างลงในโครงร่าง
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## ขั้นตอนที่ 5: การเพิ่มโครงร่างลงในหน้า
```java
page.appendChildLast(outline);
```
## ขั้นตอนที่ 6: บันทึกเอกสาร
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
ทำตามขั้นตอนเหล่านี้อย่างพิถีพิถัน และคุณจะสร้างรายการลำดับเลขใน OneNote ได้อย่างง่ายดายโดยใช้ Aspose.Note for Java
## บทสรุป
ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการที่ราบรื่นของการสร้างรายการลำดับเลขใน OneNote โดยใช้ Aspose.Note สำหรับ Java คุณลักษณะที่แข็งแกร่งของไลบรารีทำให้เป็นเครื่องมืออันล้ำค่าสำหรับนักพัฒนา Java ที่ทำงานกับไฟล์ Microsoft OneNote
## คำถามที่พบบ่อย
### ถาม: ฉันสามารถปรับแต่งรูปแบบลำดับเลขในรายการ OneNote ของฉันได้หรือไม่
ตอบ: แน่นอน! คุณสามารถปรับแต่งรูปแบบการกำหนดหมายเลขได้โดยใช้คลาส NumberList ที่ได้รับจาก Aspose.Note สำหรับ Java
### ถาม: Aspose.Note สำหรับ Java มีเวอร์ชันทดลองใช้งานหรือไม่
 ตอบ: ได้ คุณสามารถดาวน์โหลดรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
### ถาม: ฉันจะรับการสนับสนุน Aspose.Note สำหรับ Java ได้อย่างไร
 ตอบ: เยี่ยมชม[Aspose.Note สำหรับฟอรัม Java](https://forum.aspose.com/c/note/28) เพื่อสนับสนุนชุมชน
### ถาม: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน
 ตอบ: โปรดดูที่[เอกสารประกอบ](https://reference.aspose.com/note/java/) เพื่อข้อมูลที่ครบถ้วน
### ถาม: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร
 ตอบ: คุณสามารถซื้อใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).