---
date: 2026-01-20
description: เรียนรู้วิธีตั้งสไตล์ย่อหน้าเริ่มต้นใน OneNote โดยใช้ Aspise.Note สำหรับ
  Java และเพิ่มฟอนต์เริ่มต้นใน OneNote ด้วยฟอนต์ย่อหน้าที่กำหนดเอง
linktitle: Set Default Paragraph Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: ตั้งค่ารูปแบบย่อหน้าตั้งต้นใน OneNote - Aspose.Note
url: /th/java/onenote-styles/set-default-paragraph-style/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าแบบย่อหน้าเริ่มต้นใน OneNote - Aspose.Note

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีตั้งค่าแบบย่อหน้าเริ่มต้น** ใน OneNote อย่างโปรแกรมเมติกด้วย Aspose.Note สำหรับ Java การกำหนดแบบเริ่มต้นช่วยให้คุณเพิ่มฟอนต์เริ่มต้นในหน้า OneNote และปรับแต่งฟอนต์ของย่อหน้าทั่วทั้งเอกสารได้โดยไม่ต้องเขียนโค้ดฟอร์แมตซ้ำสำหรับแต่ละย่อหน้า

## คำตอบอย่างรวดเร็ว
- **“set default paragraph style” ทำอะไร?** มันกำหนดเทมเพลตการฟอร์แมตระดับย่อหน้าที่ทุกย่อหน้าใหม่จะสืบทอด เว้นแต่คุณจะเขียนทับ  
- **ต้องใช้ไลบรารีใด?** Aspose.Note สำหรับ Java  
- **ต้องมีลิขสิทธิ์หรือไม่?** รุ่นทดลองฟรีใช้ได้สำหรับการประเมิน; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **ขั้นตอนหลักคืออะไร?** เริ่มต้นเอกสาร, สร้าง `ParagraphStyle`, นำไปใช้กับ `RichText`, แล้วบันทึกไฟล์ OneNote  
- **สามารถเปลี่ยนฟอนต์ภายหลังได้หรือไม่?** ได้ – คุณสามารถแก้ไขสไตล์หรือใช้ `TextStyle` ที่แตกต่างกันกับแต่ละรันได้  

## “set default paragraph style” คืออะไร?
การตั้งค่าแบบย่อหน้าเริ่มต้นหมายถึงการสร้างอ็อบเจกต์ `ParagraphStyle` (ชื่อฟอนต์, ขนาด, สี ฯลฯ) แล้วกำหนดให้กับองค์ประกอบ `RichText` เมื่อเชื่อมต่อแล้ว ทุกบรรทัดภายใน `Richแต่ `TextStyle`ท่อหน้าแบบแมนนวล  
- **การสร้างแบรนด์:** ทำให้การบังคับใช้แนวทางสไตล์ขององค์กรเป็นเรื่องง่าย  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. Java Development Kit (JDK) ติดตั้งบนระบบของคุณ  
2. ไลบรารี Aspose.Note สำหรับ Java – ดาวน์โหลดจาก [download page](https://releases.aspose.com/note/java/)  
3. IDE เช่น Eclipse หรือ IntelliJ IDEA สำหรับเขียนและรันโค้ด Java  

## นำเข้าแพ็กเกจ

ก่อนอื่นให้นำเข้าแพ็กเกจที่จำเป็นเพื่อเริ่มเขียนโค้ด:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

ต่อไปเราจะอธิบายโค้ดตัวอย่างเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: เริ่มต้น Document, Page, และ Outline

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## ขั้นตอนที่ 2: สร้างองค์ประกอบ Outline

```java
OutlineElement outlineElem = new OutlineElement();
```

## ขั้นตอนที่ 3: กำหนดแบบย่อหน้าเริ่มต้น

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## ขั้นตอนที่ 4: สร้าง Rich Text ด้วยแบบเริ่มต้น

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## ขั้นตอนที่ 5: เพิ่ม Rich Text ไปยังองค์ประกอบ Outline

```java
outlineElem.appendChildLast(text);
```

## ขั้นตอนที่ 6: เพิ่มองค์ประกอบ Outline ไปยัง Outline

```java
outline.appendChildLast(outlineElem);
```

## ขั้นตอนที่ 7: เพิ่ม Outline ไปยัง Page

```java
page.appendChildLast(outline);
```

## ขั้นตอนที่ 8: เพิ่ม Page ไปยัง Document

```java
document.appendChildLast(page);
```

## ขั้นตอนที่ 9: บันทึก Document

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

โค้ดนี้จะตั้งค่าแบบย่อหน้าเริ่มต้นใน OneNote ด้วย Aspose.Note สำหรับ Java

## ปัญหาที่พบบ่อยและวิธีแก้
- **ฟอนต์หายบนเครื่องเป้าหมาย:** ฟอนต์ต้องติดตั้งบนระบบที่เปิดไฟล์ OneNote; หากไม่เช่นนั้น OneNote จะใช้ฟอนต์เริ่มต้นแทน  
- **ข้อผิดพลาดของพาธ:** ตรวจสอบให้ `dataDir` ชี้ไปยังโฟลเดอร์ที่มีอยู่และสามารถเขียนได้; มิฉะนั้น `document.save` จะโยน `IOException`  
- **ไม่ได้ตั้งค่าลิขสิทธิ์:** หากรันโดยไม่มีลิขสิทธิ์ที่ถูกต้อง ไฟล์ที่สร้างจะมีลายน้ำ  

## สรุป

การตั้งค่าแบบย่อหน้าเริ่มต้นใน OneNote อย่างโปรแกรมเมติกสามารถทำได้อย่างมีประสิทธิภาพด้วย Aspose.Note สำหรับ Java โดยทำตามขั้นตอนที่อธิบายในบทแนะนำนี้ คุณจะสามารถผสานฟังก์ชันนี้เข้ากับแอปพลิเคชัน Java ของคุณ เพิ่มฟอนต์เริ่มต้นในหน้า OneNote และปรับแต่งฟอนต์ย่อหน้าให้สอดคล้องกับแบรนด์หรือมาตรฐานเอกสารของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

**Q1: ฉันสามารถปรับแต่งแบบย่อหน้าเริ่มต้นเพิ่มเติมได้หรือไม่?**  
A1: ได้, คุณสามารถปรับพารามิเตอร์เช่นชื่อฟอนต์, ขนาด, สี, การจัดแนว, และระยะห่างบรรทัดให้ตรงกับความต้องการของคุณ

**Q2: Aspose.Note รองรับการดำเนินการฟอร์แมตข้อความอื่น ๆ หรือไม่?**  
A2: แน่นอน, Aspose.Note มีการสนับสนุนอย่างกว้างขวางสำหรับการจัดการฟอร์แมตข้อความ รวมถึงสไตล์ฟอนต์, จุดหัวข้อ, การเยื้อง, และอื่น ๆ

**Q3: Aspose.Note เข้ากันได้กับทุกเวอร์ชันของ OneNote หรือไม่?**  
A3: Aspose.Note ถูกออกแบบให้ทำงานกับไฟล์ Microsoft OneNote ในหลายเวอร์ชัน, เพื่อให้มีความเข้ากันได้อย่างกว้างขวาง

**Q4: ฉันสามารถผสาน Aspose.Note เข้าในโครงการ Java ที่มีอยู่ของฉันได้หรือไม่?**  
A4: ได้, คุณสามารถเพิ่ม Aspose.Note ลงในโครงการของคุณได้ง่าย ๆ โดยใส่ไฟล์ JAR หรือใช้การพึ่งพา Maven/Gradle แล้วนำเข้าแพ็กเกจที่จำเป็น

**Q5: มีเวอร์ชันทดลองสำหรับ Aspose.Note หรือไม่?**  
A5: มี, คุณสามารถเข้าถึงเวอร์ชันทดลองฟรีของ Aspose.Note ได้จาก [website](https://releases.aspose.com/)

**Q6: ฉันจะเปลี่ยนส: ดึง `ParagraphStyleกต์ `RichText` ที่มีอยู่, แก้ไขคุณสมบัติของมัน, แล้วกำหนดใหม่, หรือสร้างสไตล์ใหม่และนำไปใช้กับย่อหน้าเพิ่มเติม

**Q7: สไตล์เริ่มต้นจะมีผลต่อย่อหน้าที่มีอยู่ในเอกสารที่โหลดหรือไม่?**  
A7: ไม่, สไตล์เริ่มต้นจะใช้กับย่อหน้าใหม่ที่คุณเพิ่มหลังจากตั้งค่าเท่านั้น ย่อหน้าเดิมจะคงฟอร์แมตเดิมไว้ เว้นแต่คุณจะแก้ไขโดยเจตนา

---

**อัปเดตล่าสุด:** 2026-01-20  
**ทดสอบกับ:** Aspose.Note 24.11 สำหรับ Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}