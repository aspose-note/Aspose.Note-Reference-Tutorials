---
title: แปลงโน้ตบุ๊กเป็นรูปภาพที่แบนใน OneNote - Aspose.Note
linktitle: แปลงโน้ตบุ๊กเป็นรูปภาพที่แบนใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีแปลงสมุดบันทึกเป็นรูปภาพที่แบนใน OneNote โดยใช้ Aspose.Note for Java รักษาองค์ประกอบทั้งหมดไว้ในไฟล์ภาพเดียวได้อย่างง่ายดาย
weight: 13
url: /th/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลงโน้ตบุ๊กเป็นรูปภาพที่แบนใน OneNote - Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงสมุดบันทึกเป็นรูปภาพที่แบนราบใน OneNote โดยใช้ Aspose.Note สำหรับ Java วิธีนี้ช่วยให้คุณสามารถบันทึกสมุดบันทึกของคุณเป็นไฟล์ภาพได้ เพื่อให้แน่ใจว่าองค์ประกอบทั้งหมดจะถูกเก็บรักษาไว้ในรูปแบบภาพเดียว

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
2.  Aspose.Note สำหรับไลบรารี Java ที่ดาวน์โหลดและตั้งค่าในโปรเจ็กต์ Java ของคุณ คุณสามารถดาวน์โหลดห้องสมุดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).
3. ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java

## แพ็คเกจนำเข้า

ในการเริ่มต้น คุณจะต้องนำเข้าแพ็คเกจที่จำเป็นจาก Aspose.Note สำหรับ Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

ขั้นแรก กำหนดไดเร็กทอรีที่มีไฟล์สมุดบันทึกของคุณ:

```java
String dataDir = "Your Document Directory";
```

 แทนที่`"Your Document Directory"` พร้อมเส้นทางไปยังไฟล์สมุดบันทึกของคุณ

## ขั้นตอนที่ 2: โหลดสมุดบันทึก

 จากนั้นให้โหลดไฟล์สมุดบันทึกโดยใช้นามสกุล`Notebook` ระดับ:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 ให้แน่ใจว่าจะเปลี่ยน`"test.onetoc2"` พร้อมชื่อไฟล์สมุดบันทึกของคุณ

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการบันทึกรูปภาพ

ตอนนี้ให้ตั้งค่าตัวเลือกสำหรับการบันทึกสมุดบันทึกเป็นรูปภาพ เราจะระบุรูปแบบการบันทึกเป็น PNG และตั้งค่าความละเอียดเป็น 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

คุณสามารถปรับความละเอียดได้ตามความต้องการของคุณ

## ขั้นตอนที่ 4: แผ่สมุดบันทึก

เพื่อให้แน่ใจว่าองค์ประกอบทั้งหมดถูกทำให้เป็นภาพเดียว ให้ตั้งค่า`flatten` ตัวเลือกในการ`true`: :

```java
saveOptions.setFlatten(true);
```

เพื่อให้แน่ใจว่าภาพที่ได้จะคงเค้าโครงของโน้ตบุ๊กของคุณไว้

## ขั้นตอนที่ 5: บันทึกรูปภาพ

สุดท้าย ให้บันทึกสมุดบันทึกเป็นรูปภาพที่เรียบ:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 แทนที่`"ExportImageasFlattenedNotebook_out.png"` ด้วยชื่อไฟล์เอาต์พุตที่คุณต้องการ

## บทสรุป

โดยสรุป เมื่อใช้ Aspose.Note สำหรับ Java คุณสามารถแปลงสมุดบันทึกของคุณเป็นรูปภาพที่แบนใน OneNote ได้อย่างง่ายดาย กระบวนการนี้ทำให้แน่ใจได้ว่าองค์ประกอบทั้งหมดจะถูกเก็บรักษาไว้ในรูปแบบภาพเดียว ช่วยให้สามารถแชร์และดูได้ง่าย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับความละเอียดของภาพที่ส่งออกได้หรือไม่

 A1: ได้ คุณสามารถปรับความละเอียดได้ตามความต้องการของคุณโดยการปรับเปลี่ยน`setResolution` พารามิเตอร์วิธีการ

### คำถามที่ 2: Aspose.Note รองรับรูปแบบรูปภาพอื่นๆ เพื่อการส่งออกหรือไม่

ตอบ 2: ใช่ Aspose.Note รองรับรูปแบบภาพต่างๆ เช่น PNG, JPEG, BMP ฯลฯ สำหรับการส่งออกสมุดบันทึก

### คำถามที่ 3: ฉันสามารถปรับแต่งภาพที่ส่งออกเพิ่มเติมได้หรือไม่

A3: ใช่ Aspose.Note มีตัวเลือกมากมายสำหรับการปรับแต่งภาพที่ส่งออก รวมถึงขนาดหน้า การวางแนว และการตั้งค่าคุณภาพ

### คำถามที่ 4: Aspose.Note สำหรับ Java มีเวอร์ชันทดลองใช้งานหรือไม่

 A4: ได้ คุณสามารถขอรับเวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 A5: คุณสามารถค้นหาการสนับสนุนและแหล่งข้อมูลได้จากฟอรัม Aspose.Note[ที่นี่](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
