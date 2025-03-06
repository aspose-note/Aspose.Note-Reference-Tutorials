---
title: เขียนตารางใน OneNote - Aspose.Note
linktitle: เขียนตารางใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีการเขียนตารางใน OneNote โดยทางโปรแกรมโดยใช้ Aspose.Note สำหรับ Java คำแนะนำทีละขั้นตอนสำหรับการสร้างเอกสารอย่างมีประสิทธิภาพ
weight: 11
url: /th/java/onenote-table-manipulation/compose-table/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เขียนตารางใน OneNote - Aspose.Note

## การแนะนำ
ในสภาพแวดล้อมทางธุรกิจที่มีการแข่งขันสูงในปัจจุบัน การสื่อสารและการทำงานร่วมกันอย่างมีประสิทธิภาพเป็นปัจจัยสำคัญในการบรรลุความสำเร็จ Aspose.Note for Java มอบโซลูชันอันทรงพลังสำหรับการสร้างและจัดการเอกสาร OneNote โดยทางโปรแกรม ในบทช่วยสอนนี้ เราจะสำรวจวิธีการเขียนตารางใน OneNote โดยใช้ Aspose.Note สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนด้านล่างเพื่อปรับปรุงกระบวนการสร้างเอกสารของคุณ
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  Aspose.Note สำหรับไลบรารี Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).
- สภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่ตั้งค่าไว้สำหรับการพัฒนา Java
## แพ็คเกจนำเข้า
ตรวจสอบให้แน่ใจว่าได้นำเข้าแพ็คเกจที่จำเป็นเพื่อเริ่มต้นโปรเจ็กต์ของคุณ เพิ่มคำสั่งนำเข้าต่อไปนี้ให้กับคลาส Java ของคุณ:
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```
## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร
```java
String dataDir = "Your Document Directory";
```
ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางจริงที่คุณต้องการบันทึกเอกสาร OneNote ของคุณ
## ขั้นตอนที่ 2: เขียนส่วนหัว
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
สร้างส่วนหัวที่สะดุดตาให้กับเอกสารของคุณ ปรับขนาดตัวอักษร ตัวหนา และการจัดแนวตามต้องการ
## ขั้นตอนที่ 3: สร้างหน้าและโครงร่าง
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
ตั้งค่าหน้าและโครงร่างใหม่ จากนั้นเพิ่มส่วนหัวที่สร้างไว้ก่อนหน้านี้ให้กับโครงร่าง
## ขั้นตอนที่ 4: เพิ่มข้อความสรุป
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
รวมข้อความสรุปสั้นๆ เพื่อให้บริบทของตาราง
## ขั้นตอนที่ 5: เขียนตาราง
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// ขั้นตอนที่เหลือเกี่ยวข้องกับการตั้งค่าโครงสร้างตาราง แถวส่วนหัว และการเพิ่มแถวว่าง
// อ้างถึงรหัสที่ให้มาสำหรับการใช้งานโดยละเอียด
```
เขียนโครงสร้างตารางและเติมข้อมูลที่เกี่ยวข้อง รหัสที่ให้มาประกอบด้วยการเพิ่มคอลัมน์ แถวส่วนหัว แถวว่าง และเนื้อหาเทมเพลตสำหรับคอลัมน์ 'ผู้ติดต่อ'
## ขั้นตอนที่ 6: บันทึกเอกสาร
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
บันทึกเอกสารที่เรียบเรียงของคุณด้วยชื่อไฟล์และเส้นทางไดเร็กทอรีที่ระบุ
## บทสรุป
ยินดีด้วย! คุณสร้างตารางใน OneNote สำเร็จแล้วโดยใช้ Aspose.Note for Java บทช่วยสอนนี้สาธิตกระบวนการทีละขั้นตอน ซึ่งช่วยให้คุณปรับปรุงความสามารถในการสร้างเอกสารโดยทางโปรแกรม
## คำถามที่พบบ่อย
### ถาม: ฉันจะหาเอกสารประกอบ Aspose.Note สำหรับ Java ได้ที่ไหน
 คุณสามารถดูเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/note/java/).
### ถาม: ฉันจะดาวน์โหลด Aspose.Note สำหรับ Java ได้อย่างไร
 คุณสามารถดาวน์โหลดได้จาก[ลิงค์นี้](https://releases.aspose.com/note/java/).
### ถาม: มีการทดลองใช้ฟรีหรือไม่?
 ใช่ คุณสามารถเข้าถึงการทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
### ถาม: ฉันจะรับการสนับสนุน Aspose.Note สำหรับ Java ได้ที่ไหน
 เยี่ยมชมฟอรั่มการสนับสนุน[ที่นี่](https://forum.aspose.com/c/note/28).
### ถาม: ฉันสามารถขอรับใบอนุญาตชั่วคราวได้หรือไม่
 ใช่ คุณสามารถรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
