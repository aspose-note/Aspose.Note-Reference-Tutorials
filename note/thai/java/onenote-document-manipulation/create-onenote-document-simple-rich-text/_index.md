---
date: 2026-02-18
description: เรียนรู้วิธีตั้งค่ารูปแบบย่อหน้าและเพิ่มองค์ประกอบโครงร่างเมื่อสร้างเอกสาร
  OneNote ด้วย Java โดยใช้ Aspose.Note ส่งออก OneNote เป็น PDF บันทึก OneNote เป็น
  PDF และสร้างไฟล์ OneNote ได้อย่างง่ายดาย
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: ส่งออก OneNote เป็น PDF – ตั้งค่ารูปแบบย่อหน้าขณะสร้างเอกสาร OneNote ด้วย Java
url: /th/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

 Thai is LTR, fine.

Let's produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งสไตล์ย่อหน้าในขณะสร้างเอกสาร OneNote ด้วย Java

## บทนำ

ในยุคการพัฒนาที่เคลื่อนที่อย่างรวดเร็วในปัจจุบัน การ **ส่งออก OneNote เป็น PDF** ด้วยโปรแกรมเป็นสิ่งสำคัญสำหรับการสร้างเอกสารที่ดูเป็นมืออาชีพและพร้อมแชร์ได้อย่างสมบูรณ์ บทเรียนนี้จะพาคุณผ่านการสร้างไฟล์ OneNote การกำหนดสไตล์ย่อหน้าแบบกำหนดเอง และสุดท้าย **ส่งออก OneNote เป็น PDF** ด้วย Aspose.Note for Java ไม่ว่าคุณจะกำลังสร้างเอนจินรายงาน โซลูชันบันทึกโน้ตอัตโนมัติ หรือบริการแปลงเอกสาร เทคนิคที่อธิบายไว้ที่นี่จะช่วยให้คุณ **บันทึก OneNote เป็น PDF** พร้อมการควบคุมรูปแบบที่แม่นยำ

## คำตอบสั้น ๆ
- **“ตั้งสไตล์ย่อหน้า” หมายถึงอะไร?** หมายถึงการกำหนดฟอนต์ ขนาด สี และการจัดรูปแบบอื่น ๆ ให้กับย่อหน้าข้อความหนึ่ง  
- **ฉันสามารถส่งออกผลลัพธ์เป็น PDF ได้หรือไม่?** ได้ – บทเรียนจะจบด้วยการบันทึกไฟล์ OneNote เป็น PDF  
- **ต้องใช้ไลเซนส์สำหรับ Aspose.Note หรือไม่?** สามารถใช้รุ่นทดลองฟรีเพื่อประเมินผลได้; ต้องมีไลเซนส์สำหรับการใช้งานจริง  
- **IDE ที่รองรับมีอะไรบ้าง?** ทุก IDE ของ Java – Eclipse, IntelliJ IDEA, NetBeans ฯลฯ  
- **การทำงานนี้ใช้เวลานานแค่ไหน?** ประมาณ 10‑15 นาทีสำหรับเอกสารพื้นฐาน

## “ตั้งสไตล์ย่อหน้า” ใน Aspose.Note คืออะไร?
การตั้งสไตล์ย่อหน้าหมายถึงการกำหนดอ็อบเจกต์ `ParagraphStyle` (ชื่อฟอนต์, ขนาด, สี ฯลฯ) แล้วผูกกับโหนด `RichText` ซึ่งทำให้คุณควบคุมการแสดงผลของข้อความภายในหน้า OneNote ได้อย่างเต็มที่

## วิธีตั้งสไตล์ย่อหน้าใน OneNote?
การใช้สไตล์ทำได้ง่ายเพียงสร้างอินสแตนซ์ `ParagraphStyle` ปรับคุณสมบัติตามต้องการ แล้วกำหนดให้กับองค์ประกอบ `RichText` การเรียก API จะเป็นการทำงานหนึ่งบรรทัดเมื่ออ็อบเจกต์สไตล์พร้อมใช้งาน

## ทำไมต้องส่งออก OneNote เป็น PDF?
- **การสร้างแบรนด์ที่สม่ำเสมอ:** รักษาฟอนต์และสีขององค์กรเมื่อนำโน้ตไปแชร์ภายนอก  
- **ความอ่านง่าย:** PDF คงรูปแบบการจัดวางอย่างแม่นยำ ทำให้เหมาะสำหรับการพิมพ์หรือเก็บรักษา  
- **การเข้าถึงข้ามแพลตฟอร์ม:** ผู้รับสามารถดู PDF บนอุปกรณ์ใดก็ได้โดยไม่ต้องมี OneNote  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมี:

1. **Java Development Kit (JDK) 1.8+** – JDK เวอร์ชันล่าสุดใดก็ได้จะทำงานได้  
2. **Aspose.Note for Java** – ดาวน์โหลด JAR ล่าสุดจาก [หน้าดาวน์โหลด Aspose.Note](https://releases.aspose.com/note/java/)  
3. **IDE** (Eclipse, IntelliJ IDEA หรือ NetBeans) สำหรับคอมไพล์และรันตัวอย่าง  

> **เคล็ดลับ:** เพิ่ม JAR ของ Aspose.Note ลงใน classpath ของโปรเจกต์ผ่าน Maven หรืออ้างอิง JAR ด้วยตนเองใน IDE ของคุณ

## นำเข้าแพ็กเกจ

ก่อนอื่นให้ทำการนำเข้าคลาสที่จำเป็น บล็อกนี้จะไม่เปลี่ยนแปลง

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

> คลาส `ParagraphStyle` คือกุญแจสำคัญสำหรับ **ตั้งสไตล์ย่อหน้า** ในบทเรียนต่อไป

## คู่มือขั้นตอนโดยละเอียด

ต่อไปนี้เป็นการเดินผ่านแต่ละขั้นตอนอย่างกระชับ โค้ดบล็อกจะเหมือนกับตัวอย่างต้นฉบับ; เราเพียงเพิ่มข้อความอธิบายเท่านั้น

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร
กำหนดตำแหน่งที่ไฟล์ที่สร้างจะถูกบันทึก

```java
String dataDir = "Your Document Directory";
```

เปลี่ยน `"Your Document Directory"` ให้เป็นพาธแบบ absolute หรือ relative บนเครื่องของคุณ

### ขั้นตอนที่ 2: เริ่มต้นอ็อบเจกต์ Document
สร้าง `Document` รากที่แทนไฟล์ OneNote

```java
Document doc = new Document();
```

### ขั้นตอนที่ 3: เริ่มต้นอ็อบเจกต์ Page
ไฟล์ OneNote ประกอบด้วยหน้าอย่างน้อยหนึ่งหน้า; เราเริ่มด้วยหน้าเดียว

```java
Page page = new Page();
```

### ขั้นตอนที่ 4: เริ่มต้นอ็อบเจกต์ Outline
Outline ทำหน้าที่เป็นคอนเทนเนอร์สำหรับองค์ประกอบ outline (คิดว่าเป็นส่วน)

```java
Outline outline = new Outline();
```

### ขั้นตอนที่ 5: เริ่มต้นอ็อบเจกต์ OutlineElement
ที่นี่เราจะ **เพิ่ม outline element** ที่จะเก็บ rich text ของเรา

```java
OutlineElement outlineElem = new OutlineElement();
```

### ขั้นตอนที่ 6: ตั้งค่าสไตล์ข้อความ (ตั้งสไตล์ย่อหน้า)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

อินสแตนซ์ `ParagraphStyle` กำหนดฟอนต์, ขนาด, สี – นี่คือจุดที่เราจะ **ตั้งสไตล์ย่อหน้า** ให้กับโหนดข้อความที่กำลังจะสร้าง

### ขั้นตอนที่ 7: เริ่มต้นอ็อบเจกต์ RichText

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

เราสร้างโหนด `RichText` ใส่สตริงง่าย ๆ แล้วผูกสไตล์ที่กำหนดไว้ก่อนหน้า

### ขั้นตอนที่ 8: เพิ่มโหนด RichText ลงใน OutlineElement

```java
outlineElem.appendChildLast(text);
```

ตอนนี้ข้อความที่มีสไตล์อยู่ภายใน outline element แล้ว

### ขั้นตอนที่ 9: เพิ่มโหนด OutlineElement ลงใน Outline

```java
outline.appendChildLast(outlineElem);
```

Outline ตอนนี้มี element ที่บรรจุย่อหน้าของเราแล้ว

### ขั้นตอนที่ 10: เพิ่มโหนด Outline ลงใน Page

```java
page.appendChildLast(outline);
```

เราวาง outline บนหน้า

### ขั้นตอนที่ 11: เพิ่มโหนด Page ลงใน Document

```java
doc.appendChildLast(page);
```

เอกสารตอนนี้มีหน้าเดียวที่มีข้อความสไตล์แล้ว

### ขั้นตอนที่ 12: บันทึกเอกสาร (ส่งออก OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

เมธอด `save` จะเขียนไฟล์ OneNote และ **ส่งออก OneNote PDF** ในขั้นตอนเดียว คุณยังสามารถบันทึกเป็น `.one` โดยใช้ `SaveFormat.One` หากต้องการรูปแบบดั้งเดิม

## ปัญหาที่พบบ่อย & วิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|--------|
| **ไม่พบไฟล์** | `dataDir` ชี้ไปยังโฟลเดอร์ที่ไม่มีอยู่ | ตรวจสอบให้แน่ใจว่าโฟลเดอร์มีอยู่หรือสร้างขึ้นโดยโปรแกรม (`new File(dataDir).mkdirs();`) |
| **PDF ว่างเปล่า** | ไม่มีเนื้อหาใดถูกเพิ่มก่อนบันทึก | ยืนยันว่าโหนด `RichText` ถูกเพิ่มและสไตล์ถูกตั้งค่า |
| **ฟอนต์ไม่รองรับ** | ชื่อฟอนต์ไม่ได้ติดตั้งบนระบบ | ใช้ฟอนต์ทั่วไปเช่น `"Arial"` หรือฝังฟอนต์ในโปรเจกต์ |

## คำถามที่พบบ่อย

**ถาม: Aspose.Note สามารถจัดการรูปแบบซับซ้อนเช่น ตารางหรือรูปภาพได้หรือไม่?**  
ตอบ: ได้, API รองรับตาราง, รูปภาพ, ไฮเปอร์ลิงก์ และคุณลักษณะการจัดวางขั้นสูงอื่น ๆ

**ถาม: สามารถ **แปลง OneNote PDF** กลับเป็นไฟล์ OneNote ได้หรือไม่?**  
ตอบ: การแปลงโดยตรงยังไม่มีให้บริการ, แต่คุณสามารถดึงข้อมูลจาก PDF แล้วสร้างไฟล์ OneNote ใหม่ด้วย API

**ถาม: ไลบรารีทำงานบน Linux/macOS ได้หรือไม่?**  
ตอบ: แน่นอน. Aspose.Note for Java เป็นแบบ platform‑independent; เพียงแค่ติดตั้ง JDK

**ถาม: จะเพิ่มหลายหน้า หรือหลาย outline ได้อย่างไร?**  
ตอบ: สร้างอ็อบเจกต์ `Page` และ `Outline` เพิ่มเติม แล้วผนวกเข้ากับ `Document` เช่นเดียวกับตัวอย่างหน้าเดียว

**ถาม: จะหา ตัวอย่างเพิ่มเติมได้จากที่ไหน?**  
ตอบ: เอกสารอย่างเป็นทางการของ Aspose.Note และ [ฟอรั่มสนับสนุน](https://forum.aspose.com/c/note/28) มีตัวอย่างโค้ดมากมาย

## สรุป

คุณได้เรียนรู้วิธี **ตั้งสไตล์ย่อหน้า**, **เพิ่ม outline element**, และ **สร้างไฟล์ OneNote** ที่สามารถ **ส่งออกเป็น PDF** ด้วย Aspose.Note for Java การใส่สไตล์ข้อความตั้งแต่ขั้นตอนแรกทำให้เอกสารสุดท้ายดูเป็นมืออาชีพและการทำ **convert OneNote PDF** จะคงรูปแบบได้อย่างแม่นยำ อย่าลังเลที่จะต่อยอดพื้นฐานนี้ด้วยรูปภาพ, ตาราง หรือเมตาดาต้าตามความต้องการของโครงการของคุณ

---

**อัปเดตล่าสุด:** 2026-02-18  
**ทดสอบกับ:** Aspose.Note for Java 24.11 (รุ่นล่าสุด)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}