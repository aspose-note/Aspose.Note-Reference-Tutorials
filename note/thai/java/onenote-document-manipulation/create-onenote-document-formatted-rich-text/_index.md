---
title: สร้างเอกสาร OneNote ด้วย Rich Text ที่จัดรูปแบบใน Java
linktitle: สร้างเอกสาร OneNote ด้วย Rich Text ที่จัดรูปแบบใน Java
second_title: Aspose.Note Java API
description: เรียนรู้วิธีสร้างเอกสาร OneNote ที่มีรูปแบบสมบูรณ์โดยทางโปรแกรมใน Java โดยใช้ Aspose.Note สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อให้เอกสารอัตโนมัติราบรื่น
weight: 11
url: /th/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างเอกสาร OneNote ด้วย Rich Text ที่จัดรูปแบบใน Java

## การแนะนำ

การสร้างเอกสาร OneNote ที่มีรูปแบบสมบูรณ์โดยทางโปรแกรมสามารถเป็นเครื่องมืออันทรงพลังสำหรับนักพัฒนาที่ต้องการสร้างงานสร้างเอกสารในแอปพลิเคชัน Java โดยอัตโนมัติ Aspose.Note สำหรับ Java มีชุดคุณสมบัติและฟังก์ชันการทำงานที่ครอบคลุมเพื่อให้บรรลุเป้าหมายนี้ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการสร้างเอกสาร OneNote ด้วย Rich Text ที่จัดรูปแบบโดยใช้ Aspose.Note สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว
2.  Aspose.Note สำหรับ Java JAR: ดาวน์โหลดและรวมไฟล์ Aspose.Note สำหรับ Java JAR ในโปรเจ็กต์ของคุณ คุณสามารถรับได้จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/note/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): ใช้ IDE ที่คุณต้องการ เช่น IntelliJ IDEA หรือ Eclipse

## แพ็คเกจนำเข้า

ขั้นแรก คุณต้องนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ เพิ่มคำสั่งนำเข้าต่อไปนี้ที่จุดเริ่มต้นของไฟล์ Java ของคุณ:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## ขั้นตอนที่ 1: ตั้งค่าเอกสารและหน้า

เริ่มต้นด้วยการเริ่มต้นวัตถุ Document และ Page:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## ขั้นตอนที่ 2: สร้างชื่อเรื่องด้วยการจัดรูปแบบ

ตอนนี้ เรามาสร้างชื่อเรื่องด้วยข้อความที่จัดรูปแบบ:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## ขั้นตอนที่ 3: สร้าง Rich Text ด้วยการจัดรูปแบบ

ต่อไป เรามาสร้าง Rich Text ด้วยสไตล์การจัดรูปแบบต่างๆ:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## ขั้นตอนที่ 4: เพิ่มองค์ประกอบลงในหน้าและเอกสาร

ตอนนี้ เรามาเพิ่มชื่อเรื่องและ Rich Text ให้กับหน้าและองค์ประกอบเค้าร่าง:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## ขั้นตอนที่ 5: บันทึกเอกสาร

สุดท้าย ให้บันทึกเอกสาร OneNote ที่สร้างขึ้น:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีสร้างเอกสาร OneNote ด้วย Rich Text ที่จัดรูปแบบใน Java โดยใช้ Aspose.Note สำหรับ Java ด้วยการทำตามคำแนะนำทีละขั้นตอนเหล่านี้ คุณสามารถสร้างเอกสาร OneNote แบบกำหนดเองได้อย่างง่ายดายโดยทางโปรแกรม ซึ่งช่วยเพิ่มความสามารถด้านเอกสารอัตโนมัติของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งลักษณะแบบอักษรเพิ่มเติมได้หรือไม่

A1: ได้ คุณสามารถปรับคุณสมบัติต่างๆ ได้ เช่น สีตัวอักษร ขนาด สไตล์ ฯลฯ เพื่อให้เหมาะกับความต้องการของคุณ

### คำถามที่ 2: Aspose.Note สำหรับ Java เข้ากันได้กับ Java IDE ทั้งหมดหรือไม่

ตอบ 2: ได้ คุณสามารถใช้ Aspose.Note สำหรับ Java กับ Java IDE ใดก็ได้ที่รองรับการพัฒนา Java

### คำถามที่ 3: ฉันสามารถรวมฟังก์ชันนี้เข้ากับเว็บแอปพลิเคชันได้หรือไม่

ตอบ 3: แน่นอน Aspose.Note สำหรับ Java สามารถรวมเข้ากับเว็บแอปพลิเคชันได้อย่างราบรื่นสำหรับการสร้างเอกสารแบบไดนามิก

### คำถามที่ 4: มีข้อกำหนดสิทธิ์การใช้งาน Aspose.Note สำหรับ Java หรือไม่

ตอบ 4: ใช่ คุณต้องได้รับสิทธิ์การใช้งานเพื่อใช้ Aspose.Note สำหรับ Java ในโครงการเชิงพาณิชย์ อย่างไรก็ตาม คุณยังสามารถใช้ใบอนุญาตชั่วคราวเพื่อการทดสอบได้

### คำถามที่ 5: Aspose.Note for Java รองรับรูปแบบเอกสารอื่นๆ นอกเหนือจาก OneNote หรือไม่

A5: ใช่ Aspose.Note สำหรับ Java รองรับรูปแบบเอกสารที่หลากหลาย รวมถึง PDF, HTML และรูปแบบรูปภาพ

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
