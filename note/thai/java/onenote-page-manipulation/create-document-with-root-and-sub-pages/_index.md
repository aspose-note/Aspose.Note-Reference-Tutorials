---
title: สร้างเอกสารด้วยรูทและเพจย่อยใน OneNote
linktitle: สร้างเอกสารด้วยรูทและเพจย่อยใน OneNote
second_title: Aspose.Note Java API
description: สร้างเอกสารที่มีรูทและเพจย่อยใน OneNote โดยใช้ Aspose.Note สำหรับ Java ทำตามคำแนะนำทีละขั้นตอนเพื่อจัดระเบียบบันทึกย่อของคุณอย่างมีประสิทธิภาพ
weight: 11
url: /th/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างเอกสารด้วยรูทและเพจย่อยใน OneNote

## การแนะนำ

ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการสร้างเอกสารที่มีรูทเพจและเพจย่อยใน OneNote โดยใช้ Aspose.Note for Java เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถจัดระเบียบเอกสาร OneNote ของคุณด้วยโครงสร้างแบบลำดับชั้นได้อย่างมีประสิทธิภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณ
2. Aspose.Note สำหรับ Java: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ Java จาก[เว็บไซต์](https://purchase.aspose.com/buy).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): เลือก Java IDE เช่น IntelliJ IDEA, Eclipse หรือ NetBeans

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณ:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

กำหนดไดเรกทอรีที่คุณต้องการบันทึกเอกสาร OneNote ของคุณ:

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: สร้างวัตถุเอกสาร

 ยกตัวอย่าง`Document` วัตถุ:

```java
Document doc = new Document();
```

## ขั้นตอนที่ 3: สร้างเพจ

เริ่มต้นวัตถุหน้าและตั้งค่าระดับ:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## ขั้นตอนที่ 4: เพิ่มโหนดลงในเพจ

### การเพิ่มโหนดในหน้าแรก

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### การเพิ่มโหนดในหน้าที่สอง

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### การเพิ่มโหนดในหน้าที่สาม

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## ขั้นตอนที่ 5: เพิ่มหน้าลงในเอกสาร

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## ขั้นตอนที่ 6: บันทึกเอกสาร

บันทึกเอกสาร OneNote:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // จัดการข้อยกเว้น
}
```

ยินดีด้วย! คุณสร้างเอกสารที่มีรูทและเพจย่อยใน OneNote สำเร็จแล้วโดยใช้ Aspose.Note for Java

## บทสรุป

การจัดระเบียบเอกสาร OneNote ของคุณด้วยโครงสร้างแบบลำดับชั้นถือเป็นสิ่งสำคัญสำหรับการจัดการและการนำทางที่ดียิ่งขึ้น ด้วย Aspose.Note สำหรับ Java คุณสามารถสร้างเอกสารที่มีรูทและเพจย่อยได้อย่างมีประสิทธิภาพ โดยให้เค้าโครงที่ชัดเจนและเป็นระเบียบสำหรับบันทึกย่อของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถสร้างเพจย่อยหลายระดับโดยใช้ Aspose.Note สำหรับ Java ได้หรือไม่

A1: ได้ คุณสามารถสร้างเพจย่อยได้หลายระดับโดยการตั้งค่าระดับที่เหมาะสมสำหรับแต่ละเพจ

### คำถามที่ 2: Aspose.Note สำหรับ Java เข้ากันได้กับ Java IDE ที่แตกต่างกันหรือไม่

ตอบ 2: ใช่ Aspose.Note สำหรับ Java เข้ากันได้กับ Java IDE ยอดนิยม เช่น IntelliJ IDEA, Eclipse และ NetBeans

### คำถามที่ 3: ฉันสามารถปรับแต่งการจัดรูปแบบของข้อความในเอกสาร OneNote ของฉันได้หรือไม่

A3: ได้ คุณสามารถปรับแต่งแบบอักษร สี ขนาด และตัวเลือกการจัดรูปแบบอื่นๆ ได้โดยใช้ Aspose.Note สำหรับฟีเจอร์ Rich Text ของ Java

### คำถามที่ 4: Aspose.Note สำหรับ Java รองรับการบันทึกเอกสารในรูปแบบที่แตกต่างกันหรือไม่

ตอบ 4: ใช่ Aspose.Note สำหรับ Java รองรับการบันทึกเอกสารในรูปแบบต่างๆ รวมถึง BMP, PDF, PNG และอื่นๆ

### คำถามที่ 5: Aspose.Note สำหรับ Java มีเวอร์ชันทดลองใช้งานหรือไม่

A5: ได้ คุณสามารถดาวน์โหลด Aspose.Note สำหรับ Java เวอร์ชันทดลองใช้ฟรีได้จากเว็บไซต์
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
