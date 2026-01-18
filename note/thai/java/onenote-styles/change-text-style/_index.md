---
date: 2026-01-18
description: เรียนรู้วิธีตั้งค่าสีฟอนต์ใน Java สำหรับ OneNote ด้วย Aspose.Note, เน้นข้อความ,
  ปรับขนาดฟอนต์, และบันทึก OneNote เป็น PDF. คู่มือแบบขั้นตอนพร้อมโค้ด.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: ตั้งค่าสีฟอนต์ Java ใน OneNote – Aspose.Note
url: /th/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าสีฟอนต์ Java ใน OneNote – Aspose.Note

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **ตั้งค่าสีฟอนต์ Java** สำหรับข้อความภายในเอกสาร OneNote ด้วย Aspose.Note for Java API เราจะอธิบายขั้นตอนการโหลดไฟล์ `.one` การเข้าถึงโหนด RichText การกำหนดสี การไฮไลท์ และการเปลี่ยนขนาดฟอนต์ และสุดท้าย **บันทึก OneNote เป็น PDF** ไม่ว่าคุณจะต้องการ **ไฮไลท์ข้อความใน OneNote**, **ปรับขนาดฟอนต์ใน OneNote**, หรือเพียงแค่เปลี่ยนสไตล์ข้อความโดยรวม ขั้นตอนต่อไปนี้ให้โซลูชันที่ครบถ้วนและพร้อมใช้งานในระดับผลิตภัณฑ์

## คำตอบสั้น
- **ฉันสามารถเปลี่ยนสีฟอนต์ของคำเฉพาะได้หรือไม่?** ใช่ – ทำการวนซ้ำผ่านอ็อบเจกต์ `TextRun` แล้วเรียก `setFontColor`  
- **Aspose.Note สามารถบันทึก OneNote เป็น PDF ได้หรือไม่?** แน่นอน; ใช้ `document.save("output.pdf")`  
- **ต้องการเวอร์ชัน Java ใด?** Java 8 หรือสูงกว่า  
- **รองรับการไฮไลท์หรือไม่?** ใช้ `setHighlight(Color)` บน `TextStyle`  
- **ฉันสามารถแปลง OneNote เป็น PDF ด้วยบรรทัดเดียวได้หรือไม่?** ไม่โดยตรง แต่เมธอด `save` จะจัดการการแปลงให้  

## อะไรคือ “set font color java”

วลีนี้หมายถึงการกำหนดสีฟอนต์ใหม่ให้กับองค์ประกอบข้อความในไฟล์ OneNote ด้วยโค้ด Java อย่างโปรแกรมเมติก ด้วย Aspose.Note คุณจะได้การควบคุมเต็มรูปแบบของคุณลักษณะสไตล์ เช่น สีฟอนต์, ไฮไลท์, และขนาดโดยไม่ต้องเปิด UI ของ OneNote  

## ทำไมต้องเปลี่ยนสไตล์ข้อความใน OneNote?

- **เพิ่มความอ่านง่าย** – ข้อความที่มีสีหรือไฮไลท์จะดึงความสนใจไปยังจุดสำคัญ  
- **ความสอดคล้องของแบรนด์** – บังคับใช้สีขององค์กรในบันทึกการประชุม  
- **คุณภาพการส่งออก** – บันทึกที่มีสไตล์ดูเป็นมืออาชีพเมื่อคุณ **แปลง OneNote เป็น PDF** เพื่อแชร์  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น โปรดตรวจสอบว่าคุณมี:

1. ความรู้พื้นฐานการเขียนโปรแกรม Java  
2. ติดตั้ง JDK 8 หรือใหม่กว่า  
3. ไลบรารี Aspose.Note for Java ถูกเพิ่มในโปรเจกต์ของคุณ (Maven/Gradle หรือ JAR แบบแมนนวล)  
4. ไฟล์ตัวอย่าง OneNote (`Sample1.one`) สำหรับทดลอง  

## นำเข้าแพ็กเกจ

ก่อนอื่นให้ import คลาสที่เราต้องใช้:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## คู่มือทีละขั้นตอน

### ขั้นตอนที่ 1: โหลดเอกสาร

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

เราโหลดไฟล์ OneNote (`Sample1.one`) เพื่อให้ Aspose.Note สามารถทำงานกับโครงสร้างภายในของมันได้  

### ขั้นตอนที่ 2: เข้าถึงโหนด RichText

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

อ็อบเจกต์ `RichText` มีบรรทัดย่อหน้าจริง ๆ โดยการดึงโหนดแรกเราจะได้ตัวชี้ไปยังข้อความที่ต้องการจัดรูปแบบ  

### ขั้นตอนที่ 3: เปลี่ยนสไตล์ข้อความ (set font color java)

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

ภายในลูปเราจะ **ตั้งค่าสีฟอนต์ Java** เป็นสีเหลือง, ใช้ไฮไลท์สีน้ำเงิน (เป็นตัวอย่างของ **highlight text onenote**), และเพิ่มขนาดเป็น 20 พอยต์, แสดงตัวอย่างของ **modify font size onenote**  

### ขั้นตอนที่ 4: บันทึกเอกสาร (save onenote as pdf)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

การเรียก `save` พร้อมส่วนขยาย `.pdf` จะทำการ **convert onenote to pdf** โดยอัตโนมัติ ให้คุณได้ไฟล์พร้อมแชร์  

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| ไม่มีการเปลี่ยนสีที่มองเห็นได้ | เอกสารถูกเปิดใน OneNote ก่อนบันทึก | ปิด OneNote หรือโหลดไฟล์ใหม่หลังจากกระบวนการ Java เสร็จสิ้น |
| ไฮไลท์ไม่แสดงผล | ใช้สีที่ตรงกับพื้นหลัง | เลือก `Color` ที่ตัดกัน (เช่น `Color.yellow`) |
| `document.save` ขว้าง `IOException` | เส้นทางออกไม่ถูกต้อง | ตรวจสอบให้แน่ใจว่าไดเรกทอรีมีอยู่และคุณมีสิทธิ์เขียน |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถใช้การเปลี่ยนแปลงสไตล์เหล่านี้กับบางส่วนของไฟล์ OneNote ของฉันเท่านั้นได้หรือไม่?**  
ตอบ: ได้ – กรองโหนด `RichText` ตาม `Section` หรือ `Page` พ่อแม่ก่อนทำการวนซ้ำ `TextRun`  

**ถาม: นอกจากสี, ไฮไลท์, และขนาดแล้ว Aspose.Note สามารถจัดการรูปแบบอื่นอะไรได้บ้าง?**  
ตอบ: คุณสามารถเปลี่ยนฟอนต์, ทำให้เป็นตัวหนา/เอียง/ขีดเส้นใต้, การจัดแนว, และแม้กระทั่งระยะห่างระหว่างย่อหน้า  

**ถาม: สามารถประมวลผลหลายไฟล์ OneNote พร้อมกันได้หรือไม่?**  
ตอบ: แน่นอน. ห่อหุ้มการโหลดและตรรกะการจัดรูปแบบในลูปที่ประมวลผลไฟล์ `.one` แต่ละไฟล์ในโฟลเดอร์  

**ถาม: ไลบรารีรองรับการบันทึกโดยตรงเป็นรูปแบบอื่นเช่น DOCX หรือไม่?**  
ตอบ: ใช่ – Aspose.Note สามารถส่งออกเป็น PDF, DOCX, HTML, และรูปแบบภาพหลายประเภท  

**ถาม: ฉันจะหา ตัวอย่างและอ้างอิง API เพิ่มเติมได้จากที่ไหน?**  
ตอบ: เยี่ยมชมเว็บไซต์เอกสารอย่างเป็นทางการของ Aspose.Note, สำรวจอ้างอิง API, และดาวน์โหลดเวอร์ชันทดลองฟรีเพื่อทดลองใช้งาน  

## สรุป

ตอนนี้คุณมีตัวอย่างครบวงจรจากต้นจนจบของวิธีการ **ตั้งค่าสีฟอนต์ Java**, ไฮไลท์ข้อความ, ปรับขนาดฟอนต์, และ **บันทึก OneNote เป็น PDF** ด้วย Aspose.Note คุณสามารถปรับโค้ดให้ทำงานกับหน้าเฉพาะ, ใช้การจัดรูปแบบตามเงื่อนไข, หรือรวมเข้ากับกระบวนการประมวลผลเอกสารขนาดใหญ่ได้ตามต้องการ  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-18  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose