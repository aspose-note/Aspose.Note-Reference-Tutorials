---
title: สร้างรายการสัญลักษณ์แสดงหัวข้อย่อยใน OneNote - Aspose.Note
linktitle: สร้างรายการสัญลักษณ์แสดงหัวข้อย่อยใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: สำรวจคำแนะนำทีละขั้นตอนเกี่ยวกับการสร้างรายการสัญลักษณ์แสดงหัวข้อย่อยใน OneNote โดยใช้ Aspose.Note สำหรับ Java ยกระดับการสร้างเอกสารของคุณอย่างง่ายดาย
weight: 12
url: /th/java/onenote-text-manipulation/create-bulleted-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างรายการสัญลักษณ์แสดงหัวข้อย่อยใน OneNote - Aspose.Note

## การแนะนำ
ในภูมิทัศน์แบบไดนามิกของการพัฒนา Java การสร้างเอกสารที่มีส่วนร่วมและจัดระเบียบถือเป็นสิ่งสำคัญ Aspose.Note สำหรับ Java มีชุดเครื่องมืออันทรงพลังเพื่อปรับปรุงกระบวนการสร้างเอกสารของคุณ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการสร้างรายการสัญลักษณ์แสดงหัวข้อย่อยใน OneNote โดยใช้ Aspose.Note สำหรับ Java มาดูรายละเอียดกันดีกว่า
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  Aspose.Note สำหรับไลบรารี Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก[Aspose.Note สำหรับเอกสารประกอบ Java](https://reference.aspose.com/note/java/).
- การตั้งค่า Java Integrated Development Environment (IDE) บนเครื่องของคุณ
## แพ็คเกจนำเข้า
เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ สิ่งนี้ทำให้แน่ใจได้ว่าคุณจะสามารถเข้าถึงฟังก์ชัน Aspose.Note สำหรับ Java ได้
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
// อิมพอร์ต Aspose.Note สำหรับแพ็คเกจ Java
```
## ขั้นตอนที่ 1: เริ่มต้นเอกสารและหน้า
สร้างวัตถุของคลาส Document และเริ่มต้นวัตถุคลาส Page
```java
String dataDir = "Your Document Directory";
// สร้างวัตถุของคลาสเอกสาร
Document doc = new Document();
// เริ่มต้นวัตถุคลาสหน้า
Page page = new Page();
```
## ขั้นตอนที่ 2: เริ่มต้นโครงร่างและ TextStyle
ตอนนี้ เริ่มต้นวัตถุคลาส Outline และวัตถุคลาส TextStyle ด้วยคุณสมบัติการจัดรูปแบบ
```java
// เริ่มต้นวัตถุคลาสเค้าร่าง
Outline outline = new Outline();
// เริ่มต้นวัตถุคลาส TextStyle และตั้งค่าคุณสมบัติการจัดรูปแบบ
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```
## ขั้นตอนที่ 3: สร้างองค์ประกอบรายการสัญลักษณ์แสดงหัวข้อย่อย
สร้างออบเจ็กต์คลาส OutlineElement และใช้สัญลักษณ์แสดงหัวข้อย่อยเพื่อสร้างรายการสัญลักษณ์แสดงหัวข้อย่อย
```java
// เริ่มต้นวัตถุคลาส OutlineElement และใช้สัญลักษณ์แสดงหัวข้อย่อย
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// เริ่มต้นวัตถุคลาส RichText และใช้สไตล์ข้อความ
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```
ทำซ้ำขั้นตอนข้างต้นสำหรับแต่ละองค์ประกอบในรายการสัญลักษณ์แสดงหัวข้อย่อยของคุณ
## ขั้นตอนที่ 4: เพิ่มองค์ประกอบโครงร่างลงในโครงร่าง
เพิ่มออบเจ็กต์ OutlineElement ที่สร้างขึ้นใน Outline
```java
// เพิ่มองค์ประกอบโครงร่าง
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## ขั้นตอนที่ 5: เพิ่มโครงร่างลงในเพจและบันทึก
เพิ่มโหนดเค้าร่างลงในเพจ และจากนั้น เพิ่มโหนดเพจลงในเอกสาร สุดท้ายให้บันทึกเอกสาร
```java
// เพิ่มโหนดเค้าร่าง
page.appendChildLast(outline);
// เพิ่มโหนดเพจ
doc.appendChildLast(page);
// บันทึกเอกสาร
doc.save(dataDir + "CreateBulletedList_out.pdf");
```
ยินดีด้วย! คุณสร้างรายการสัญลักษณ์แสดงหัวข้อย่อยใน OneNote สำเร็จแล้วโดยใช้ Aspose.Note for Java
## บทสรุป
Aspose.Note สำหรับ Java ช่วยให้กระบวนการสร้างเอกสารที่มีการจัดรูปแบบอย่างดีง่ายขึ้น บทช่วยสอนนี้จะอธิบายขั้นตอนต่างๆ ในการสร้างรายการสัญลักษณ์แสดงหัวข้อย่อยใน OneNote สำรวจความเป็นไปได้เพิ่มเติมด้วย Aspose.Note เพื่อปรับปรุงประสบการณ์การสร้างเอกสารของคุณ
## คำถามที่พบบ่อย
### Aspose.Note สำหรับ Java เข้ากันได้กับ Java IDE ทั้งหมดหรือไม่
ใช่ Aspose.Note สำหรับ Java เข้ากันได้กับ Java Integrated Development Environment ยอดนิยม เช่น Eclipse และ IntelliJ IDEA
### ฉันสามารถปรับแต่งการจัดรูปแบบของรายการหัวข้อย่อยได้หรือไม่
อย่างแน่นอน! คุณสามารถปรับเปลี่ยนแบบอักษร สี และขนาดขององค์ประกอบรายการสัญลักษณ์แสดงหัวข้อย่อยได้ตามความต้องการของคุณ
### ฉันจะรับการสนับสนุนเพิ่มเติมสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน
 เยี่ยมชม[Aspose.Note สำหรับฟอรัมสนับสนุน Java](https://forum.aspose.com/c/note/28) เพื่อขอความช่วยเหลือจากชุมชน
### มีการทดลองใช้ฟรีสำหรับ Aspose.Note สำหรับ Java หรือไม่
 ใช่ คุณสามารถสำรวจเวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
### ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร
 รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
