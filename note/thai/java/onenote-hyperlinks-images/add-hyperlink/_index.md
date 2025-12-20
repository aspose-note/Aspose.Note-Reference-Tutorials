---
date: 2025-12-20
description: เรียนรู้วิธีบันทึก OneNote เป็น PDF และเพิ่มไฮเปอร์ลิงก์ใน OneNote ด้วย
  Java พร้อมไลบรารี Aspose.Note สร้าง PDF จาก OneNote อย่างง่ายดาย.
linktitle: Save OneNote as PDF and Add Hyperlink in OneNote with Java
second_title: Aspose.Note Java API
title: บันทึก OneNote เป็น PDF และเพิ่มไฮเปอร์ลิงก์ใน OneNote ด้วย Java
url: /th/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก OneNote เป็น PDF และเพิ่มไฮเปอร์ลิงก์ใน OneNote ด้วย Java

## คำแนะนำ

การเพิ่มไฮเปอร์ลิงก์ในเอกสาร OneNote ของคุณพร้อมกับการบันทึกเป็น PDF สามารถปรับปรุงการโต้ตอบของโน้ตของคุณอย่างมากและทำให้การแชร์ง่ายขึ้น ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีบันทึก OneNote เป็น PDF** และฝังลิงก์ที่คลิกได้โดยใช้ Java และไลบรารี Aspose.Note มาดำเนินการตามขั้นตอนด้วยกัน!

## คำตอบอย่างรวดเร็ว
- **ฉันสามารถบันทึก OneNote เป็น PDF ด้วย Java ได้หรือไม่?** ใช่, Aspose.Note for Java มีเมธอด `save` เพียงหนึ่งครั้งเพื่อสร้าง PDF.
- **ฉันจะฝังไฮเปอร์ลิงก์อย่างไร?** ใช้ `TextStyle.setHyperlinkAddress` บนส่วน `RichText`.
- **ข้อกำหนดเบื้องต้นคืออะไร?** JDK 8 ขึ้นไปและไลบรารี Aspose.Note for Java.
- **รูปแบบผลลัพธ์ที่รองรับมีอะไรบ้าง?** PDF, DOCX, XPS และอื่น ๆ
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** ใช่, จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่การประเมินผล.

## “save onenote as pdf” คืออะไร?

การบันทึกสมุดบันทึก OneNote เป็น PDF จะสร้างเวอร์ชันพกพาแบบอ่าน‑อย่างเดียวของโน้ตของคุณที่สามารถเปิดได้บนอุปกรณ์ใดก็ได้โดยไม่ต้องใช้แอป OneNote ซึ่งเป็นประโยชน์อย่างยิ่งสำหรับการเก็บถาวร, การพิมพ์, หรือการแชร์กับผู้ใช้ที่ไม่มี OneNote

## ทำไมต้องสร้าง PDF จาก OneNote ด้วย Aspose.Note Java?

- **ความแม่นยำเต็มรูปแบบ:** รักษาการจัดรูปแบบ, รูปภาพ, และไฮเปอร์ลิงก์
- **การควบคุมแบบโปรแกรม:** ทำการแปลงเป็นชุดโดยอัตโนมัติในบริการแบ็กเอนด์
- **ข้ามแพลตฟอร์ม:** ทำงานบน Windows, Linux, และ macOS
- **API ครบครัน:** สามารถเพิ่มหรือแก้ไขเนื้อหาได้ง่ายก่อนบันทึก

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม, โปรดตรวจสอบว่าคุณได้ติดตั้งและตั้งค่าข้อกำหนดต่อไปนี้บนระบบของคุณแล้ว:

### Java Development Kit (JDK)

ตรวจสอบว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดและติดตั้ง JDK ได้จาก [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Aspose.Note for Java Library

ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note for Java คุณสามารถค้นหาเอกสารและลิงก์ดาวน์โหลดได้ [ที่นี่](https://reference.aspose.com/note/java/).

## นำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าแพ็กเกจที่จำเป็นสำหรับการทำงานกับ Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

ตอนนี้, เราจะแบ่งตัวอย่างที่ให้ไว้เป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าโครงสร้างเอกสาร

ขั้นแรก, สร้างเอกสารใหม่และหน้าที่จะบรรจุเนื้อหา.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## ขั้นตอนที่ 2: กำหนดสไตล์ข้อความเริ่มต้น

กำหนดสไตล์ย่อหน้าตั้งต้นที่จะนำไปใช้กับส่วนใหญ่ขององค์ประกอบข้อความ.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## ขั้นตอนที่ 3: ตั้งค่าข้อความหัวเรื่อง

สร้างหัวเรื่องสำหรับหน้าและใช้สไตล์ตั้งต้น.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## ขั้นตอนที่ 4: สร้าง Outline และองค์ประกอบ Outline

Outline ทำหน้าที่เป็นคอนเทนเนอร์สำหรับย่อหน้าและองค์ประกอบอื่น ๆ.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## ขั้นตอนที่ 5: กำหนดสไตล์ข้อความสำหรับไฮเปอร์ลิงก์

ที่นี่เรากำหนดสไตล์สีแดงที่จะใช้สำหรับส่วนที่คลิกได้.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## ขั้นตอนที่ 6: เพิ่มข้อความพร้อมไฮเปอร์ลิงก์

ตอนนี้เราจะสร้างอ็อบเจ็กต์ `RichText` ที่ผสมข้อความปกติและไฮเปอร์ลิงก์  เมธอด `setHyperlinkAddress` จะบอก Aspose.Note ว่าส่วนนี้ควรเป็นลิงก์ที่คลิกได้.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## ขั้นตอนที่ 7: เพิ่ม Outline ไปยังหน้าและหน้าไปยังเอกสาร

แนบองค์ประกอบ outline ไปยัง outline, แนบ outline ไปยังหน้า, และสุดท้ายแนบหน้าไปยังเอกสาร.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## ขั้นตอนที่ 8: บันทึกเอกสารเป็น PDF

ขั้นตอนสุดท้ายคือการบันทึกเอกสาร OneNote เป็นไฟล์ PDF ซึ่งเป็นจุดที่คีย์เวิร์ดหลัก **save onenote as pdf** มีบทบาท.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## สรุป

ขอแสดงความยินดี! คุณได้ **บันทึก OneNote เป็น PDF** และเพิ่มไฮเปอร์ลิงก์ในเอกสารโดยใช้ Java และไลบรารี Aspose.Note อย่างสำเร็จ ความสามารถนี้ช่วยให้คุณสร้าง PDF ที่โต้ตอบได้และสามารถแชร์ได้โดยตรงจากเนื้อหา OneNote ของคุณ.

## คำถามที่พบบ่อย

### Q1: Aspose.Note รองรับทุกเวอร์ชันของ Java หรือไม่?

A1: ใช่, Aspose.Note for Java รองรับเวอร์ชันหลักทั้งหมดของ Java รวมถึง JDK 8 ขึ้นไป.

### Q2: ฉันสามารถเพิ่มหลายไฮเปอร์ลิงก์ในเอกสารเดียวโดยใช้ Aspose.Note ได้หรือไม่?

A2: แน่นอน! คุณสามารถเพิ่มไฮเปอร์ลิงก์ได้ตามต้องการภายในเอกสาร OneNote ของคุณโดยใช้ Aspose.Note for Java.

### Q3: Aspose.Note มีการสนับสนุนภาษาโปรแกรมอื่น ๆ หรือไม่?

A3: ใช่, Aspose.Note มีไลบรารีสำหรับหลายภาษาโปรแกรม รวมถึง .NET, Python, และ Android.

### Q4: Aspose.Note ง่ายต่อการรวมเข้ากับโปรเจกต์ Java ที่มีอยู่หรือไม่?

A4: ใช่, การรวม Aspose.Note เข้าในโปรเจกต์ Java ของคุณเป็นเรื่องง่ายและมีเอกสารที่ครบถ้วน ทำให้เริ่มต้นได้อย่างรวดเร็ว.

### Q5: ฉันจะหาแหล่งข้อมูลและความช่วยเหลือเพิ่มเติมสำหรับการใช้ Aspose.Note ได้จากที่ไหน?

A5: คุณสามารถค้นหาเอกสารเชิงลึก, บทแนะนำ, และการสนับสนุนจากชุมชนได้ที่ [Aspose.Note forum](https://forum.aspose.com/c/note/28).

## คำถามที่พบบ่อย

**Q: ฉันจะปรับแต่งลักษณะของไฮเปอร์ลิงก์ได้อย่างไร?**  
A: ใช้คุณสมบัติของ `TextStyle` เช่น `setFontColor`, `setUnderline`, หรือ `setFontName` ก่อนเรียก `setHyperlinkAddress`.

**Q: ฉันสามารถบันทึกเอกสารในรูปแบบอื่นนอกจาก PDF ได้หรือไม่?**  
A: ใช่, Aspose.Note รองรับ DOCX, XPS, HTML และรูปแบบการส่งออกอื่น ๆ อีกหลายรูปแบบ.

**Q: ถ้าฉันต้องการเพิ่มไฮเปอร์ลิงก์ในไฟล์ OneNote ที่มีอยู่แล้วจะทำอย่างไร?**  
A: โหลดไฟล์ที่มีอยู่ด้วย `new Document("input.one")`, แก้ไขเนื้อหาตามที่แสดง, แล้วเรียก `save` ด้วยรูปแบบที่ต้องการ.

**Q: มีวิธีเปิดไฮเปอร์ลิงก์โดยโปรแกรมหลังจากสร้าง PDF แล้วหรือไม่?**  
A: โปรแกรมดู PDF จะจัดการลิงก์ที่คลิกได้โดยอัตโนมัติ; ไม่จำเป็นต้องเขียนโค้ดเพิ่มเติม.

**Q: ฉันต้องการลิขสิทธิ์สำหรับการพัฒนาใช่หรือไม่?**  
A: ลิขสิทธิ์การประเมินผลชั่วคราวเพียงพอสำหรับการพัฒนาและทดสอบ, แต่ต้องมีลิขสิทธิ์เต็มสำหรับการใช้งานในผลิตภัณฑ์.

---

**Last Updated:** 2025-12-20  
**Tested With:** Aspose.Note for Java 23.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}