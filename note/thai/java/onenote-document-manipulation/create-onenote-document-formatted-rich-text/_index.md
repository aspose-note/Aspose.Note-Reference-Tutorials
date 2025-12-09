---
date: 2025-12-09
description: เรียนรู้วิธีบันทึก OneNote เป็น PDF พร้อมข้อความที่จัดรูปแบบอย่างสมบูรณ์ใน
  Java โดยใช้ Aspose.Note for Java. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อการอัตโนมัติเอกสารที่ราบรื่น.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: บันทึก OneNote เป็น PDF พร้อมข้อความ Rich Text ที่จัดรูปแบบใน Java
url: /th/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก OneNote เป็น PDF พร้อมข้อความรูปแบบ Rich Text ใน Java

## คำแนะนำ

หากคุณต้องการ **save OneNote as PDF** พร้อมคงรูปแบบ rich‑text ไว้ คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะอธิบายขั้นตอนการสร้างเอกสาร OneNote, ใส่สไตล์ที่กำหนดเอง, และส่งออกเป็น PDF โดยตรงด้วย Aspose.Note for Java เมื่อทำครบคุณจะได้โค้ดสแนปช็อตที่สามารถนำไปใช้ในโปรเจกต์ Java ใดก็ได้เพื่อทำการแปลง OneNote‑to‑PDF อย่างอัตโนมัติและดูเป็นมืออาชีพ

## คำตอบอย่างรวดเร็ว
- **What does this tutorial teach?** วิธีสร้างเอกสาร OneNote พร้อมข้อความที่มีสไตล์และบันทึกเป็น PDF.  
- **Which library is required?** Aspose.Note for Java (ดาวน์โหลดได้จากเว็บไซต์อย่างเป็นทางการ).  
- **Do I need a license?** ใบอนุญาตชั่วคราวใช้ได้สำหรับการทดสอบ; ต้องมีใบอนาตเต็มสำหรับการผลิต.  
- **What IDE can I use?** IDE Java ใดก็ได้—IntelliJ IDEA, Eclipse หรือ NetBeans.  
- **Can I change the output format?** ได้, Aspose.Note รองรับ PDF, HTML, PNG และอื่น ๆ

## “save onenote as pdf” คืออะไร?
การบันทึก OneNote เป็น PDF หมายถึงการแปลงโครงสร้างหน้า OneNote—including ข้อความ, รูปภาพ, และการจัดรูปแบบ—เป็นไฟล์ PDF แบบคงที่ที่สามารถดูได้บนทุกแพลตฟอร์มโดยไม่ต้องใช้ OneNote

## ทำไมต้องจัดรูปแบบ rich text ใน Java?
การใช้ rich‑text formatting (ฟอนต์, สี, สไตล์) โดยตรงใน Java ช่วยให้คุณสร้างเอกสารที่ดูเป็นมืออาชีพและสอดคล้องกับแนวทางแบรนด์ของคุณโดยไม่ต้องแก้ไขด้วยมือ

## ข้อกำหนดเบื้องต้น

1. **Java Development Kit (JDK)** – เวอร์ชันล่าสุดใดก็ได้ (8 หรือสูงกว่า).  
2. **Aspose.Note for Java JAR** – ดาวน์โหลดจาก [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse หรือโปรแกรมแก้ไขใดที่คุณชอบ.  

## นำเข้าแพ็กเกจ

ก่อนอื่นคุณต้องนำเข้าแพ็กเกจที่จำเป็นเข้าสู่โปรเจกต์ Java ของคุณ เพิ่มคำสั่ง import ต่อไปนี้ที่ส่วนต้นของไฟล์ Java ของคุณ:

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

## ขั้นตอนที่ 1: ตั้งค่า Document และ Page

เริ่มต้นโดยการสร้างอ็อบเจ็กต์ `Document` และ `Page`:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## ขั้นตอนที่ 2: สร้างหัวเรื่องพร้อมการจัดรูปแบบ

ต่อไปเราจะสร้างหัวเรื่องด้วยข้อความที่จัดรูปแบบ:

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

## ขั้นตอนที่ 3: สร้าง Rich Text พร้อมการจัดรูปแบบ

ต่อไปเราจะสร้าง rich text ด้วยสไตล์การจัดรูปแบบต่าง ๆ:

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

## ขั้นตอนที่ 4: เพิ่มองค์ประกอบลงใน Page และ Document

ต่อไปเราจะเพิ่มหัวเรื่องและ rich text ลงในหน้าและโครงสร้างเอกสาร:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## ขั้นตอนที่ 5: บันทึก Document

สุดท้ายบันทึกเอกสาร OneNote ที่สร้างขึ้นเป็น PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## ปัญหาที่พบบ่อยและวิธีแก้ไข

| ปัญหา | วิธีแก้ |
|-------|----------|
| **File not found** | ตรวจสอบว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่มีอยู่และคุณมีสิทธิ์เขียน. |
| **Missing fonts** | ตรวจสอบว่าฟอนต์ที่คุณอ้างอิง (เช่น *Calibri*) ถูกติดตั้งบนเครื่องโฮสต์. |
| **License not applied** | โหลดใบอนุญาต Aspose ของคุณก่อนสร้าง `Document` เพื่อหลีกเลี่ยงลายน้ำการประเมิน. |

## คำถามที่พบบ่อย

**Q: Can I customize the font styles further?**  
A: ใช่, คุณสามารถปรับคุณสมบัติเพิ่มเติมเช่นขีดเส้นใต้, เส้นขีดฆ่า, และการจัดแนวข้อความผ่านคลาส `TextStyle` และ `ParagraphStyle`.

**Q: Is Aspose.Note for Java compatible with all Java IDEs?**  
A: แน่นอน. ตราบใดที่ IDE รองรับการพัฒนา Java มาตรฐาน คุณสามารถเพิ่ม JAR ของ Aspose.Note ไปยัง classpath ของโปรเจกต์ได้.

**Q: Can I integrate this functionality into web applications?**  
A: ใช่, โค้ดเดียวกันทำงานในแอปพลิเคชันแบบ servlet หรือ Spring Boot, ทำให้สามารถสร้าง OneNote‑to‑PDF แบบไดนามิกบนเซิร์ฟเว.

**Q: Are there licensing requirements for using Aspose.Note for Java?**  
A: จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์. ใบอนุญาตชั่วคราวมีให้สำหรับการประเมินและทดสอบ.

**Q: Does Aspose.Note for Java support other document formats besides OneNote?**  
A: รองรับ PDF, HTML, PNG, JPEG และหลายรูปแบบการส่งออกอื่น ๆ ให้คุณมีความยืดหยุ่นในการแปลงหน้า OneNote ไปเป็นรูปแบบที่ต้องการ.

## สรุป

ในคู่มือนี้เราได้สาธิตวิธี **save OneNote as PDF** พร้อมการจัดรูปแบบ rich‑text ด้วย Aspose.Note for Java โดยทำตามขั้นตอนทีละขั้นตอน คุณสามารถอัตโนมัติการสร้างเอกสาร OneNote ที่ดูเป็นมืออาชีพและแปลงเป็น PDF ในโซลูชันที่ใช้ Java ใด ๆ

---

**อัปเดตล่าสุด:** 2025-12-09  
**ทดสอบกับ:** Aspose.Note for Java 24.11 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}