---
date: 2026-08-18
description: เรียนรู้วิธีส่งออก OneNote เป็น PDF, ตั้งค่าการจัดรูปแบบย่อหน้าใน Java,
  และบันทึก OneNote เป็น PDF ด้วย Aspose.Note สำหรับ Java.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: ตั้งค่าสไตล์ย่อหน้าเมื่อสร้างเอกสาร OneNote ใน Java
og_description: ส่งออก OneNote เป็น PDF และตั้งค่าสไตล์ย่อหน้าใน Java ด้วย Aspose.Note.
  ทำตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อสร้าง PDF ที่เรียบหรูอย่างง่ายดาย.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: ส่งออก OneNote เป็น PDF พร้อมสไตล์ย่อหน้าใน Java (58 ตัวอักษร)
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  headline: How to export OneNote to PDF with paragraph style in Java
  type: TechArticle
- description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  name: How to export OneNote to PDF with paragraph style in Java
  steps:
  - name: set document directory
    text: Define where the generated files will be saved. Replace `"Your Document
      Directory"` with an absolute or relative path on your machine.
  - name: initialize document object
    text: Create the root `Document` that represents the OneNote file. **Definition
      anchor:** `Document` is Aspose.Note’s top‑level object that holds one or more
      pages in memory.
  - name: initialize page object
    text: A OneNote file consists of one or more pages; we start with a single page.
      **Definition anchor:** `Page` represents a single OneNote page, containing outlines,
      images, and other elements.
  - name: initialize outline object
    text: Outlines act as containers for outline elements (think of them as sections).
      **Definition anchor:** `Outline` groups related `OutlineElement` objects and
      defines their visual hierarchy.
  - name: initialize outline element object
    text: Here we **add outline element** that will hold our rich text. **Definition
      anchor:** `OutlineElement` is a leaf node inside an `Outline` that can contain
      text, images, or other media.
  - name: set text style (set paragraph style)
    text: '`ParagraphStyle` defines the font family, size, color, and other typographic
      attributes for a paragraph. The `ParagraphStyle` instance defines the font,
      size, and color—this is where we **set paragraph style** for the upcoming text
      node.'
  - name: initialize rich text object
    text: '`RichText` is the node that stores styled text within an `OutlineElement`.
      We create a `RichText` node, insert a simple string, and attach the previously
      defined style.'
  - name: add rich text node to outline element
    text: Now the styled text lives inside the outline element.
  - name: add outline element node to outline
    text: The outline now contains the element that holds our paragraph.
  - name: add outline node to page
    text: We place the outline onto the page.
  type: HowTo
- questions:
  - answer: Yes, the API supports tables, images, hyperlinks, and advanced layout
      features in addition to plain text.
    question: Can Aspose.Note handle complex formatting such as tables or images?
  - answer: Direct conversion isn’t provided, but you can extract PDF content and
      rebuild a OneNote document using the API.
    question: Is it possible to convert a OneNote PDF back to a OneNote file?
  - answer: Absolutely. Aspose.Note for Java is platform‑independent; just ensure
      a compatible JDK is installed.
    question: Does the library work on Linux/macOS environments?
  - answer: Create additional `Page` and `Outline` objects, then append them to the
      `Document` just like the single‑page example.
    question: How do I add multiple pages or outlines?
  - answer: The official Aspose.Note documentation and the [support forum](https://forum.aspose.com/c/note/28)
      contain many code samples and real‑world scenarios.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- export onenote
- aspose.note
- java document processing
title: วิธีส่งออก OneNote เป็น PDF พร้อมสไตล์ย่อหน้าใน Java
url: /th/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่ารูปแบบย่อหน้าในขณะสร้างเอกสาร OneNote ด้วย Java

## บทนำ

การส่งออก OneNote เป็น PDF โดยอัตโนมัติเป็นความต้องการทั่วไปสำหรับเครื่องมือรายงาน, บริการจดบันทึกอัตโนมัติ, และสายงานแปลงเอกสาร. ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **ส่งออก OneNote เป็น PDF**, ใช้การจัดรูปแบบย่อหน้าแบบกำหนดเอง, และบันทึกไฟล์ OneNote — ทั้งหมดโดยใช้ Aspose.Note for Java. เมื่อเสร็จคุณจะมีโค้ดสแนปป์ Java ที่พร้อมใช้ซึ่งสร้าง PDF ที่ดูเป็นมืออาชีพตามที่คุณกำหนดไว้.

## คำตอบสั้น
- **“set paragraph style” หมายถึงอะไร?** มันใช้ฟอนต์, ขนาด, สี, และคุณลักษณะการจัดรูปแบบอื่น ๆ กับย่อหน้าของข้อความ.  
- **ฉันสามารถส่งออกผลลัพธ์เป็น PDF ได้หรือไม่?** ได้ – คู่มือสรุปด้วยการบันทึกไฟล์ OneNote เป็น PDF.  
- **ต้องใช้ลิขสิทธิ์ Aspose.Note หรือไม่?** สามารถใช้รุ่นทดลองฟรีเพื่อประเมิน; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์.  
- **IDE ที่รองรับมีอะไรบ้าง?** IDE ของ Java ใดก็ได้ – Eclipse, IntelliJ IDEA, NetBeans ฯลฯ.  
- **การทำงานนี้ใช้เวลานานแค่ไหน?** ประมาณ 10‑15 นาทีสำหรับเอกสารพื้นฐาน.

## วิธีส่งออก OneNote เป็น PDF ด้วย Java?

`Document` แทนไฟล์ OneNote ที่มีหน้า, โครงร่าง, และองค์ประกอบอื่น ๆ. โหลดเอกสาร OneNote ของคุณด้วย `new Document()` (หรือสร้างใหม่) แล้วเรียก `document.save("output.pdf", SaveFormat.Pdf)`. Aspose.Note จะเขียน PDF ในขั้นตอนเดียว, รักษารูปแบบ, รูปภาพ, และโครงร่างโดยไม่ต้องติดตั้ง Microsoft OneNote. วิธีนี้ทำงานบน Windows, Linux, และ macOS กับ JDK 1.8+ ใดก็ได้.

## “set paragraph style” ใน Aspose.Note คืออะไร?

`ParagraphStyle` คือคลาสที่เก็บชื่อฟอนต์, ขนาด, สี, การจัดแนว, และการตั้งค่าทิปอกราฟิกอื่น ๆ สำหรับย่อหน้า. โดยการเชื่อม `ParagraphStyle` กับโหนด `RichText` คุณจะควบคุมว่าย่อหน้านั้นปรากฏอย่างไรในหน้า OneNote สุดท้ายและใน PDF ที่ส่งออก.

## ทำไมต้องส่งออก OneNote เป็น PDF?

การส่งออก OneNote เป็น PDF ทำให้แบรนด์คงที่โดยรักษาฟอนต์และสีขององค์กร, เพิ่มความอ่านง่ายโดยคงรูปแบบเดิมสำหรับการพิมพ์หรือเก็บถาวร, และให้การเข้าถึงข้ามแพลตฟอร์มเพื่อให้ผู้รับสามารถดูเอกสารบนอุปกรณ์ใดก็ได้โดยไม่ต้องใช้ OneNote. นอกจากนี้ยังให้ประสิทธิภาพที่ดีขึ้น, ทำให้เอกสารขนาดใหญ่ประมวลผลได้อย่างรวดเร็ว.

## ข้อกำหนดเบื้องต้น

1. **Java Development Kit (JDK) 1.8+** – JDK เวอร์ชันล่าสุดใดก็ได้.  
2. **Aspose.Note for Java** – ดาวน์โหลด JAR ล่าสุดจาก [หน้าดาวน์โหลด Aspose.Note](https://releases.aspose.com/note/java/).  
3. **IDE** (Eclipse, IntelliJ IDEA, หรือ NetBeans) สำหรับคอมไพล์และรันตัวอย่าง.  

> **เคล็ดลับ:** เพิ่ม JAR ของ Aspose.Note ไปยัง classpath ของโปรเจกต์ผ่าน Maven (`<dependency>`) หรืออ้างอิง JAR ด้วยตนเองใน IDE ของคุณ.

## นำเข้าแพ็กเกจ

ก่อนอื่นให้นำเข้าเนมสเปซที่จำเป็น. ส่วนนี้ไม่ต้องเปลี่ยนแปลง.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> คลาส `ParagraphStyle` คือกุญแจสำคัญสำหรับ **set paragraph style** ในบทแนะนำต่อไป.

## คู่มือขั้นตอนโดยละเอียด

ต่อไปนี้เป็นการเดินผ่านแต่ละขั้นตอนอย่างกระชับ. โค้ดบล็อกคงเหมือนกับตัวอย่างต้นฉบับ; เราเพียงเพิ่มข้อความอธิบายเท่านั้น.

### ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสาร
กำหนดตำแหน่งที่ไฟล์ที่สร้างขึ้นจะถูกบันทึก.

```java
String dataDir = "Your Document Directory";
```

เปลี่ยน `"Your Document Directory"` เป็นพาธแบบ absolute หรือ relative ที่เครื่องของคุณ.

### ขั้นตอนที่ 2: เริ่มต้นอ็อบเจ็กต์ Document
สร้าง `Document` รากที่แทนไฟล์ OneNote.

```java
Document doc = new Document();
```

**คำอธิบาย:** `Document` คืออ็อบเจ็กต์ระดับบนสุดของ Aspose.Note ที่เก็บหนึ่งหรือหลายหน้าในหน่วยความจำ.

### ขั้นตอนที่ 3: เริ่มต้นอ็อบเจ็กต์ Page
ไฟล์ OneNote ประกอบด้วยหนึ่งหรือหลายหน้า; เราเริ่มด้วยหน้าเดียว.

```java
Page page = new Page();
```

**คำอธิบาย:** `Page` แทนหน้า OneNote หนึ่งหน้า, มีโครงร่าง, รูปภาพ, และองค์ประกอบอื่น ๆ.

### ขั้นตอนที่ 4: เริ่มต้นอ็อบเจ็กต์ Outline
Outline ทำหน้าที่เป็นคอนเทนเนอร์สำหรับองค์ประกอบโครงร่าง (คิดว่าเป็นส่วน).

```java
Outline outline = new Outline();
```

**คำอธิบาย:** `Outline` จัดกลุ่ม `OutlineElement` ที่เกี่ยวข้องและกำหนดลำดับชั้นการแสดงผล.

### ขั้นตอนที่ 5: เริ่มต้นอ็อบเจ็กต์ OutlineElement
ที่นี่เราจะ **add outline element** ที่จะเก็บข้อความที่มีรูปแบบ.

```java
OutlineElement outlineElem = new OutlineElement();
```

**คำอธิบาย:** `OutlineElement` เป็นโหนดใบไม้ภายใน `Outline` ที่สามารถบรรจุข้อความ, รูปภาพ, หรือสื่ออื่น ๆ.

### ขั้นตอนที่ 6: ตั้งค่ารูปแบบข้อความ (set paragraph style)

`ParagraphStyle` กำหนดฟอนต์, ขนาด, สี, และคุณลักษณะทิปอกราฟิกอื่น ๆ สำหรับย่อหน้า.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

อินสแตนซ์ `ParagraphStyle` กำหนดฟอนต์, ขนาด, และสี — ที่นี่เราจะ **set paragraph style** ให้กับโหนดข้อความที่กำลังจะสร้าง.

### ขั้นตอนที่ 7: เริ่มต้นอ็อบเจ็กต์ RichText

`RichText` คือโหนดที่เก็บข้อความที่มีรูปแบบภายใน `OutlineElement`.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

เราสร้างโหนด `RichText`, ใส่สตริงง่าย ๆ, แล้วผูกสไตล์ที่กำหนดไว้ก่อนหน้า.

### ขั้นตอนที่ 8: เพิ่มโหนด RichText ไปยัง OutlineElement

```java
outlineElem.appendChildLast(text);
```

ตอนนี้ข้อความที่มีรูปแบบอยู่ภายในโหนด OutlineElement แล้ว.

### ขั้นตอนที่ 9: เพิ่มโหนด OutlineElement ไปยัง Outline

```java
outline.appendChildLast(outlineElem);
```

Outline ตอนนี้มีองค์ประกอบที่เก็บย่อหน้าของเราแล้ว.

### ขั้นตอนที่ 10: เพิ่มโหนด Outline ไปยัง Page

```java
page.appendChildLast(outline);
```

เราวาง Outline ลงบนหน้า.

### ขั้นตอนที่ 11: เพิ่มโหนด Page ไปยัง Document

```java
doc.appendChildLast(page);
```

Document ตอนนี้มีหน้าเดียวที่มีข้อความที่มีรูปแบบแล้ว.

### ขั้นตอนที่ 12: บันทึกเอกสาร (export OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

เมธอด `save` จะเขียนไฟล์ OneNote และ **export OneNote to PDF** ในขั้นตอนเดียว. คุณยังสามารถบันทึกเป็น `.one` โดยใช้ `SaveFormat.One` หากต้องการรูปแบบดั้งเดิม.

## ปัญหาทั่วไป & วิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **ไม่พบไฟล์** | `dataDir` ชี้ไปยังโฟลเดอร์ที่ไม่มีอยู่. | ตรวจสอบให้แน่ใจว่าโฟลเดอร์มีอยู่หรือสร้างโดยโปรแกรม (`new File(dataDir).mkdirs();`). |
| **PDF ว่างเปล่า** | ไม่มีเนื้อหาใดถูกเพิ่มก่อนบันทึก. | ยืนยันว่าโหนด `RichText` ถูกเพิ่มและสไตล์ถูกตั้งค่า. |
| **ฟอนต์ไม่รองรับ** | ชื่อฟอนต์ไม่ได้ติดตั้งบนระบบ. | ใช้ฟอนต์ทั่วไปเช่น `"Arial"` หรือฝังฟอนต์ในโปรเจกต์. |

## คำถามที่พบบ่อย

**ถาม: Aspose.Note รองรับการจัดรูปแบบซับซ้อนเช่น ตารางหรือรูปภาพหรือไม่?**  
ตอบ: ใช้, API รองรับตาราง, รูปภาพ, ไฮเปอร์ลิงก์, และคุณลักษณะการจัดวางขั้นสูงนอกเหนือจากข้อความธรรมดา.

**ถาม: สามารถแปลง OneNote PDF กลับเป็นไฟล์ OneNote ได้หรือไม่?**  
ตอบ: การแปลงโดยตรงไม่พร้อมให้บริการ, แต่คุณสามารถดึงเนื้อหา PDF แล้วสร้างเอกสาร OneNote ใหม่ด้วย API.

**ถาม: ไลบรารีทำงานบน Linux/macOS ได้หรือไม่?**  
ตอบ: แน่นอน. Aspose.Note for Java เป็นอิสระแพลตฟอร์ม; เพียงตรวจสอบให้ JDK ที่เข้ากันได้ถูกติดตั้ง.

**ถาม: จะเพิ่มหลายหน้า หรือหลาย Outline อย่างไร?**  
ตอบ: สร้างอ็อบเจ็กต์ `Page` และ `Outline` เพิ่มเติม, แล้วต่อเข้ากับ `Document` เช่นเดียวกับตัวอย่างหน้าเดียว.

**ถาม: จะหา ตัวอย่างเพิ่มเติมได้จากที่ไหน?**  
ตอบ: ดูเอกสารอย่างเป็นทางการของ Aspose.Note และ [ฟอรั่มสนับสนุน](https://forum.aspose.com/c/note/28) ซึ่งมีโค้ดตัวอย่างและกรณีการใช้งานจริงมากมาย.

## สรุป

คุณได้เรียนรู้วิธี **set paragraph style**, **add outline element**, และ **export OneNote to PDF** ด้วย Aspose.Note for Java. การใช้ข้อความที่มีสไตล์ตั้งแต่ต้นทำให้ PDF สุดท้ายดูเป็นมืออาชีพ, และการเรียก `save` เพียงครั้งเดียวจัดการการแปลงได้อย่างมีประสิทธิภาพ. คุณสามารถต่อยอดจากพื้นฐานนี้ด้วยรูปภาพ, ตาราง, หรือเมตาดาต้าตามความต้องการของแอปพลิเคชันของคุณ.

---

**อัปเดตล่าสุด:** 2026-08-18  
**ทดสอบกับ:** Aspose.Note for Java 26.5 (รุ่นล่าสุด)  
**ผู้เขียน:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [วิธีบันทึก OneNote เป็น PDF ด้วย Aspose.Note สำหรับ Java](/note/java/onenote-document-loading/load-save-format/)
- [เรียนรู้การแปลง OneNote เป็น PDF ด้วย Aspose.Note โดยใช้ PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [ตั้งค่ารูปแบบย่อหน้าเริ่มต้นใน OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}