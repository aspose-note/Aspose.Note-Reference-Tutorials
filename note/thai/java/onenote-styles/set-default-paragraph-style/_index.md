---
title: ตั้งค่าลักษณะย่อหน้าเริ่มต้นใน OneNote - Aspose.Note
linktitle: ตั้งค่าลักษณะย่อหน้าเริ่มต้นใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีตั้งค่าสไตล์ย่อหน้าเริ่มต้นใน OneNote โดยใช้ Aspose.Note สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการจัดรูปแบบข้อความที่มีประสิทธิภาพในแอปพลิเคชัน Java ของคุณ
weight: 11
url: /th/java/onenote-styles/set-default-paragraph-style/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าลักษณะย่อหน้าเริ่มต้นใน OneNote - Aspose.Note

## การแนะนำ

Aspose.Note สำหรับ Java นำเสนอความสามารถอันทรงพลังในการจัดการการจัดรูปแบบข้อความ รวมถึงการตั้งค่าสไตล์ย่อหน้าเริ่มต้น บทช่วยสอนนี้จะแนะนำคุณตลอดขั้นตอนการตั้งค่าสไตล์ย่อหน้าเริ่มต้นใน OneNote โดยใช้ Aspose.Note

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว
2.  Aspose.Note สำหรับ Java Library: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ Java จาก[หน้าดาวน์โหลด](https://releases.aspose.com/note/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): คุณควรติดตั้ง IDE เช่น Eclipse หรือ IntelliJ IDEA เพื่อความสะดวกในการเขียนโค้ด

## แพ็คเกจนำเข้า

ขั้นแรก นำเข้าแพ็คเกจที่จำเป็นเพื่อเริ่มเขียนโค้ด:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

ตอนนี้ เรามาแบ่งโค้ดตัวอย่างออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: เริ่มต้นเอกสาร หน้า และโครงร่าง

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## ขั้นตอนที่ 2: สร้างองค์ประกอบเค้าร่าง

```java
OutlineElement outlineElem = new OutlineElement();
```

## ขั้นตอนที่ 3: กำหนดสไตล์ย่อหน้าเริ่มต้น

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## ขั้นตอนที่ 4: สร้าง Rich Text ด้วยสไตล์เริ่มต้น

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## ขั้นตอนที่ 5: เพิ่ม Rich Text ต่อท้ายองค์ประกอบโครงร่าง

```java
outlineElem.appendChildLast(text);
```

## ขั้นตอนที่ 6: ผนวกองค์ประกอบโครงร่างเข้ากับโครงร่าง

```java
outline.appendChildLast(outlineElem);
```

## ขั้นตอนที่ 7: ผนวกโครงร่างเข้ากับหน้า

```java
page.appendChildLast(outline);
```

## ขั้นตอนที่ 8: ผนวกหน้าเข้ากับเอกสาร

```java
document.appendChildLast(page);
```

## ขั้นตอนที่ 9: บันทึกเอกสาร

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

รหัสนี้จะตั้งค่าสไตล์ย่อหน้าเริ่มต้นใน OneNote โดยใช้ Aspose.Note สำหรับ Java

## บทสรุป

การตั้งค่าสไตล์ย่อหน้าเริ่มต้นใน OneNote โดยทางโปรแกรมสามารถทำได้อย่างมีประสิทธิภาพด้วย Aspose.Note for Java ด้วยการทำตามขั้นตอนที่ระบุไว้ในบทช่วยสอนนี้ คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งสไตล์ย่อหน้าเริ่มต้นเพิ่มเติมได้หรือไม่

A1: ได้ คุณสามารถปรับพารามิเตอร์ต่างๆ ได้ เช่น ชื่อแบบอักษร ขนาด สี และการจัดตำแหน่งให้เหมาะกับความต้องการของคุณ

### คำถามที่ 2: Aspose.Note รองรับการดำเนินการจัดรูปแบบข้อความอื่นๆ หรือไม่

คำตอบ 2: แน่นอน Aspose.Note ให้การสนับสนุนอย่างกว้างขวางสำหรับการจัดการการจัดรูปแบบข้อความ รวมถึงลักษณะแบบอักษร สัญลักษณ์แสดงหัวข้อย่อย และการเยื้อง

### คำถามที่ 3: Aspose.Note เข้ากันได้กับ OneNote ทุกเวอร์ชันหรือไม่

ตอบ 3: Aspose.Note ได้รับการออกแบบมาเพื่อทำงานกับไฟล์ Microsoft OneNote ในเวอร์ชันต่างๆ เพื่อให้มั่นใจถึงความเข้ากันได้ในวงกว้าง

### คำถามที่ 4: ฉันสามารถรวม Aspose.Note เข้ากับโปรเจ็กต์ Java ที่มีอยู่ได้หรือไม่

ตอบ 4: ได้ คุณสามารถรวม Aspose.Note เข้ากับโปรเจ็กต์ Java ของคุณได้อย่างง่ายดายโดยเพิ่มการขึ้นต่อกันที่จำเป็นและนำเข้าแพ็คเกจที่จำเป็น

### คำถามที่ 5: Aspose.Note มีเวอร์ชันทดลองใช้งานหรือไม่

 A5: ได้ คุณสามารถเข้าถึง Aspose.Note รุ่นทดลองใช้ฟรีได้จาก[เว็บไซต์](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
