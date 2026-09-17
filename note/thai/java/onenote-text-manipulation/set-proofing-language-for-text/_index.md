---
date: 2026-03-29
description: เรียนรู้วิธีตั้งค่าภาษาสำหรับข้อความใน OneNote ด้วย Aspose.Note สำหรับ
  Java คู่มือแบบขั้นตอนนี้จะแสดงวิธีสร้างเอกสาร OneNote, เปลี่ยนภาษาข้อความ, และบันทึกไฟล์
  OneNote อย่างมีประสิทธิภาพ
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: วิธีตั้งค่าภาษาให้กับข้อความใน OneNote – Aspose.Note
url: /th/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีตั้งค่าภาษาสำหรับข้อความใน OneNote – Aspose.Note

## บทนำ
หากคุณต้องการ **how to set language** สำหรับส่วนของข้อความเฉพาะในสมุดบันทึก OneNote, Aspose.Note for Java ทำให้เรื่องนี้ง่ายดาย ในบทเรียนนี้คุณจะได้เรียนรู้วิธีสร้างเอกสาร OneNote, เปลี่ยนภาษาของข้อความสำหรับคำหรือวลีแต่ละส่วน, และสุดท้ายบันทึกไฟล์ OneNote พร้อมกับภาษาการพิสูจน์ที่ถูกต้อง เมื่อเสร็จคุณจะเข้าใจว่าการตั้งค่าภาษามีความสำคัญต่อการตรวจสอบการสะกดและการแปลภาษาอย่างไร และคุณจะมีตัวอย่างโค้ดที่พร้อมใช้งาน

## คำตอบเร็ว
- **What does “set language” affect?** มันบอกให้ OneNote ใช้พจนานุกรมการพิสูจน์ใดสำหรับการตรวจสอบการสะกดและไวยากรณ์.  
- **Can I set different languages in the same note?** ใช่, คุณสามารถกำหนดภาษาสำหรับแต่ละรันของข้อความได้.  
- **Do I need a license for Aspose.Note?** การทดลองใช้ฟรีทำงานได้สำหรับการทดสอบ; จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง.  
- **Which Java versions are supported?** Aspose.Note for Java รองรับ Java 8 และรุ่นใหม่กว่า.  
- **Is the output a .one file?** ใช่, เอกสารจะถูกบันทึกเป็นไฟล์ OneNote *.one*.

## ข้อกำหนดเบื้องต้น
ก่อนที่จะลงลึกในโค้ด, ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. **Java Development Environment** – JDK 8 หรือสูงกว่า ที่ติดตั้งและกำหนดค่าแล้ว.  
2. **Aspose.Note for Java Library** – ดาวน์โหลดและติดตั้งไลบรารีจาก [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – สร้างโฟลเดอร์บนเครื่องของคุณเพื่อบันทึกไฟล์ OneNote ที่สร้างขึ้น.

## ทำไมต้องตั้งค่าภาษาสำหรับข้อความใน OneNote?
การตั้งค่าภาษาการพิสูจน์ทำให้การตรวจสอบการสะกด, คำแนะนำไวยากรณ์, และการทำดัชนีการค้นหา ทำงานอย่างถูกต้องสำหรับเนื้อหาหลายภาษา สิ่งนี้มีประโยชน์เป็นพิเศษสำหรับ:

- **Global teams** ที่ทำงานร่วมกันในสมุดบันทึกเดียว.  
- **Localized documentation** ที่แต่ละส่วนอาจอยู่ในภาษาต่างกัน.  
- **Data‑driven applications** ที่สร้างโน้ตโดยอัตโนมัติสำหรับผู้ใช้ทั่วโลก.

## นำเข้าแพ็กเกจ
เริ่มต้นด้วยการนำเข้าคลาส Aspose.Note ที่จำเป็นและยูทิลิตี้ของ Java.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## ขั้นตอนที่ 1: ตั้งค่าเอกสารและหน้า
สร้างเอกสาร OneNote ใหม่และหน้าที่จะบรรจุเนื้อหาของคุณ ขั้นตอนนี้ยังแสดงตัวอย่าง **create OneNote document**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## ขั้นตอนที่ 2: สร้าง Outline และ Outline Element
Outline คือคอนเทนเนอร์สำหรับเนื้อหาของสมุดบันทึก ที่นี่เราจะสร้างโครงสร้างที่จะบรรจุข้อความที่กำหนดภาษาต่อมา.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## ขั้นตอนที่ 3: เพิ่ม Rich Text พร้อมการตั้งค่าภาษา
ตอนนี้เราจะ **change text language** โดยแนบ `TextStyle` พร้อม `Locale` เฉพาะให้กับแต่ละส่วนของข้อความ นี่เป็นการสาธิต **set language for text**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## ขั้นตอนที่ 4: จัดระเบียบ Elements และบันทึก
ประกอบลำดับชั้นของ outline, แนบเข้ากับหน้า, และสุดท้าย **save OneNote file** พร้อมกับการตั้งค่าภาษาที่ได้กำหนดไว้.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## ข้อผิดพลาดทั่วไปและเคล็ดลับ
- **Locale format** – ใช้แท็ก IETF BCP‑47 (เช่น `en-US`, `de-DE`). แท็กที่ไม่ถูกต้องจะใช้ภาษาของเอกสารเป็นค่าเริ่มต้น.  
- **File path** – ตรวจสอบให้แน่ใจว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่มีอยู่; หากไม่เช่นนั้น `document.save` จะโยน `IOException`.  
- **Pro tip:** หากต้องการตั้งค่าภาษาให้กับย่อหน้าทั้งหมด, ให้ใช้ `TextStyle` กับ `ParagraphStyle` แทนการเรียก `append` แต่ละครั้ง.

## สรุป
คุณเพิ่งเรียนรู้ **how to set language** สำหรับส่วนข้อความแต่ละส่วนในสมุดบันทึก OneNote ด้วย Aspose.Note for Java ความสามารถนี้ทำให้คุณสามารถ **create OneNote document** อย่างอัตโนมัติ, **change text language** ได้ทันที, และ **save OneNote file** พร้อมเมทาดาต้าการพิสูจน์ที่แม่นยำ.

## คำถามที่พบบ่อย

**Q: ฉันสามารถตั้งค่าภาษาการพิสูจน์สำหรับภาษาอื่นที่ไม่ได้ระบุในตัวอย่างได้หรือไม่?**  
A: แน่นอน! เพิ่มการเรียก `append` เพิ่มเติมพร้อม `Locale.forLanguageTag("xx-XX")` ที่ต้องการ.

**Q: Aspose.Note for Java รองรับเวอร์ชัน Java ล่าสุดหรือไม่?**  
A: ใช่, ไลบรารีจะอัปเดตเป็นประจำเพื่อรองรับการปล่อย Java รุ่นใหม่ล่าสุด.

**Q: ฉันจะจัดการข้อผิดพลาดระหว่างกระบวนการตั้งค่าภาษาได้อย่างไร?**  
A: ห่อการดำเนินการบันทึกในบล็อก `try‑catch` เพื่อจับ `IOException` หรือ `AsposeException`.

**Q: ฉันสามารถรวมโค้ดนี้เข้าในเว็บแอปพลิเคชันได้หรือไม่?**  
A: แน่นอน. เพียงแค่ใส่ Aspose.Note JAR ลงใน classpath ของโปรเจกต์เว็บของคุณและตรวจสอบให้เซิร์ฟเวอร์มีสิทธิ์เขียนไปยังไดเรกทอรีเป้าหมาย.

**Q: ฉันจะหา ตัวอย่างและเอกสารเพิ่มเติมสำหรับ Aspose.Note for Java ได้จากที่ไหน?**  
A: สำรวจ [documentation](https://reference.aspose.com/note/java/) เพื่อดูรายการ API ทั้งหมดและโครงการตัวอย่าง.

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}