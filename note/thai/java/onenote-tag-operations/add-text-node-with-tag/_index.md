---
title: เพิ่มโหนดข้อความด้วยแท็กใน OneNote - Aspose.Note
linktitle: เพิ่มโหนดข้อความด้วยแท็กใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: สำรวจวิธีเพิ่มโหนดข้อความด้วยแท็กใน OneNote โดยใช้ Aspose.Note สำหรับ Java ง่าย มีประสิทธิภาพ และเป็นมิตรกับนักพัฒนา ดาวน์โหลดห้องสมุดทันที!
weight: 13
url: /th/java/onenote-tag-operations/add-text-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มโหนดข้อความด้วยแท็กใน OneNote - Aspose.Note

## การแนะนำ
ในบทช่วยสอนนี้ เราจะสำรวจวิธีเพิ่มโหนดข้อความด้วยแท็กใน OneNote โดยใช้ Aspose.Note สำหรับ Java Aspose.Note เป็นไลบรารี Java ที่ทรงพลังซึ่งช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม การเพิ่มโหนดข้อความด้วยแท็กเป็นข้อกำหนดทั่วไปในการประมวลผลเอกสาร และ Aspose.Note ช่วยให้งานนี้ง่ายขึ้น
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  Aspose.Note สำหรับไลบรารี Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/note/java/).
- สภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่ตั้งค่าสำหรับการพัฒนา Java
## แพ็คเกจนำเข้า
เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นสำหรับโปรเจ็กต์ Java ของคุณ ในโค้ดของคุณ ให้รวมการนำเข้าต่อไปนี้:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## ขั้นตอนที่ 1: สร้างวัตถุเอกสาร
เตรียมใช้งานวัตถุคลาสเอกสารเพื่อแสดงเอกสาร OneNote:
```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory";
//สร้างวัตถุของคลาสเอกสาร
Document doc = new Document();
```
## ขั้นตอนที่ 2: เริ่มต้นวัตถุคลาสหน้า
เริ่มต้นวัตถุคลาสหน้าเพื่อแสดงหน้าภายในเอกสาร:
```java
// เริ่มต้นวัตถุคลาสหน้า
Page page = new Page();
```
## ขั้นตอนที่ 3: เริ่มต้นออบเจ็กต์ Outline Class
เริ่มต้นออบเจ็กต์คลาส Outline เพื่อจัดโครงสร้างเนื้อหาภายในเพจ:
```java
// เริ่มต้นวัตถุคลาสเค้าร่าง
Outline outline = new Outline();
```
## ขั้นตอนที่ 4: เริ่มต้นวัตถุคลาส OutlineElement
เริ่มต้นวัตถุคลาส OutlineElement เพื่อแสดงองค์ประกอบภายในโครงร่าง:
```java
// เริ่มต้นวัตถุคลาส OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## ขั้นตอนที่ 5: ปรับแต่งสไตล์ข้อความ
ตั้งค่าสไตล์สำหรับโหนดข้อความ เช่น สีฟอนต์ ชื่อ และขนาด:
```java
// ปรับแต่งสไตล์ข้อความ
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## ขั้นตอนที่ 6: สร้างวัตถุ RichText
สร้างวัตถุ RichText และต่อท้ายข้อความที่ต้องการ:
```java
// สร้างวัตถุ RichText
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## ขั้นตอนที่ 7: เพิ่มแท็กบันทึกย่อ
เพิ่มแท็กบันทึกย่อ เช่น ดาวสีเหลือง ลงในข้อความ:
```java
// เพิ่มแท็กบันทึก
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## ขั้นตอนที่ 8: เพิ่มโหนดข้อความ
เพิ่มโหนดข้อความให้กับองค์ประกอบเค้าร่าง:
```java
// เพิ่มโหนดข้อความ
outlineElem.appendChildLast(text);
```
## ขั้นตอนที่ 9: เพิ่มองค์ประกอบโครงร่างลงในโครงร่าง
เพิ่มองค์ประกอบโครงร่างให้กับโครงร่าง:
```java
// เพิ่มโหนดองค์ประกอบเค้าร่าง
outline.appendChildLast(outlineElem);
```
## ขั้นตอนที่ 10: เพิ่มโครงร่างไปที่หน้า
เพิ่มโครงร่างไปที่หน้า:
```java
// เพิ่มโหนดเค้าร่าง
page.appendChildLast(outline);
```
## ขั้นตอนที่ 11: เพิ่มหน้าลงในเอกสาร
เพิ่มหน้าลงในเอกสาร:
```java
// เพิ่มโหนดหน้า
doc.appendChildLast(page);
```
## ขั้นตอนที่ 12: บันทึกเอกสาร OneNote
บันทึกเอกสาร OneNote ไปยังไดเร็กทอรีที่ระบุ:
```java
// บันทึกเอกสาร OneNote
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
ยินดีด้วย! คุณได้เพิ่มโหนดข้อความด้วยแท็กใน OneNote เรียบร้อยแล้วโดยใช้ Aspose.Note for Java
## บทสรุป
ในบทช่วยสอนนี้ เราได้กล่าวถึงกระบวนการทีละขั้นตอนในการเพิ่มโหนดข้อความด้วยแท็กใน OneNote โดยใช้ Aspose.Note สำหรับไลบรารี Java ไลบรารีอันทรงพลังนี้ทำให้งานการประมวลผลเอกสารง่ายขึ้น ทำให้นักพัฒนาจัดการไฟล์ OneNote โดยทางโปรแกรมได้ง่าย
## คำถามที่พบบ่อย
### ถาม: ฉันสามารถใช้ Aspose.Note สำหรับ Java กับไลบรารี Java อื่นๆ ได้หรือไม่
ตอบ: ได้ Aspose.Note สำหรับ Java สามารถผสานรวมกับไลบรารี Java อื่นๆ ได้อย่างราบรื่น เพื่อเพิ่มความสามารถในการประมวลผลเอกสาร
### ถาม: Aspose.Note สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่
 ตอบ: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
### ถาม: ฉันจะรับการสนับสนุน Aspose.Note สำหรับ Java ได้อย่างไร
ตอบ: คุณสามารถขอการสนับสนุนจากชุมชน Aspose.Note ได้[ฟอรั่ม](https://forum.aspose.com/c/note/28).
### ถาม: Aspose.Note สำหรับ Java มีใบอนุญาตชั่วคราวหรือไม่
 ตอบ: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
### ถาม: ฉันจะหาเอกสารสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน
 ตอบ: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
