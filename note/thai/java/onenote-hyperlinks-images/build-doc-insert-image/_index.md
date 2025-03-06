---
title: สร้างเอกสารและแทรกรูปภาพใน OneNote โดยใช้ Java
linktitle: สร้างเอกสารและแทรกรูปภาพใน OneNote โดยใช้ Java
second_title: Aspose.Note Java API
description: เรียนรู้วิธีสร้างเอกสาร OneNote และแทรกรูปภาพโดยใช้ Aspose.Note สำหรับ Java บทช่วยสอนทีละขั้นตอนเพื่อการผสานรวมที่ราบรื่น
weight: 12
url: /th/java/onenote-hyperlinks-images/build-doc-insert-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างเอกสารและแทรกรูปภาพใน OneNote โดยใช้ Java

## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีใช้ Aspose.Note สำหรับ Java เพื่อสร้างเอกสาร OneNote และแทรกรูปภาพลงในเอกสารเหล่านั้น Aspose.Note เป็น Java API อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม เราจะแจกแจงรายละเอียดแต่ละขั้นตอนเพื่อแนะนำคุณตลอดกระบวนการ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว
2.  Aspose.Note สำหรับไลบรารี Java: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับไลบรารี Java จาก[เว็บไซต์](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment): ใช้ IDE ที่รองรับ Java เช่น IntelliJ IDEA หรือ Eclipse ในการเขียนโค้ด

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นในโค้ด Java ของคุณ:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## ขั้นตอนที่ 1: ตั้งค่าเอกสาร

ขั้นแรก สร้างเอกสาร OneNote ใหม่และเริ่มต้นวัตถุที่จำเป็น:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## ขั้นตอนที่ 2: เริ่มต้นโครงร่าง

ตั้งค่าเค้าร่างสำหรับเอกสารและระบุคุณสมบัติออฟเซ็ต:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## ขั้นตอนที่ 3: เพิ่มรูปภาพ

โหลดรูปภาพและระบุการจัดตำแหน่ง:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## ขั้นตอนที่ 4: เพิ่มรูปภาพลงในองค์ประกอบโครงร่าง

แนบรูปภาพเข้ากับองค์ประกอบโครงร่าง:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## ขั้นตอนที่ 5: เพิ่มโครงร่างและโหนดหน้า

เพิ่มโครงร่างและโหนดหน้าให้กับเอกสาร:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## ขั้นตอนที่ 6: บันทึกเอกสาร

สุดท้าย ให้บันทึกเอกสาร OneNote:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีสร้างเอกสาร OneNote และแทรกรูปภาพลงในเอกสารเหล่านั้นโดยใช้ Aspose.Note สำหรับ Java เรียบร้อยแล้ว เมื่อทำตามขั้นตอนเหล่านี้ คุณสามารถจัดการและจัดการไฟล์ OneNote ในแอปพลิเคชัน Java ของคุณได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันจะหาเอกสารสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 A1: คุณสามารถเข้าถึงเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/note/java/).

### คำถามที่ 2: ฉันจะดาวน์โหลด Aspose.Note สำหรับ Java ได้อย่างไร

 A2: คุณสามารถดาวน์โหลด Aspose.Note สำหรับ Java ได้จาก[หน้าดาวน์โหลด](https://releases.aspose.com/note/java/).

### คำถามที่ 3: Aspose.Note สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถทดลองใช้ฟรีได้จาก[เว็บไซต์](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 A4: สำหรับการสนับสนุน โปรดไปที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).

### คำถามที่ 5: ฉันสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ Java ได้หรือไม่

 A5: ได้ คุณสามารถขอใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
