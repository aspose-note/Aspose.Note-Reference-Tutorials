---
date: 2026-01-23
description: เรียนรู้วิธีเพิ่มตารางใน OneNote อย่างเป็นโปรแกรมโดยใช้ Aspose.Note สำหรับ
  Java คู่มือขั้นตอนต่อขั้นตอนเพื่อการสร้างเอกสารอย่างมีประสิทธิภาพ
linktitle: How to add table to OneNote with Aspose.Note for Java
second_title: Aspose.Note Java API
title: วิธีเพิ่มตารางใน OneNote ด้วย Aspose.Note สำหรับ Java
url: /th/java/onenote-table-manipulation/compose-table/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มตารางใน OneNote ด้วย Aspose.Note สำหรับ Java

## บทนำ
ในบทเรียนนี้ คุณจะได้เรียนรู้วิธี **เพิ่มตารางใน OneNote** ด้วย Aspose.Note สำหรับ Java ซึ่งช่วยให้คุณสร้างเอกสารที่มีโครงสร้างและความสมบูรณ์แบบโดยอัตโนมัติ เพื่อเพิ่มประสิทธิภาพการทำงานร่วมกันและการรายงาน Aspose.Note มี API ที่ทรงพลังสำหรับสร้างหน้า OneNote, โครงร่าง และตารางโดยไม่ต้องแก้ไขด้วยตนเอง

## คำตอบอย่างรวดเร็ว
- **บทเรียนนี้ครอบคลุมอะไร?** การเพิ่มตารางใน OneNote ด้วย Aspose.Note สำหรับ Java.  
- **ต้องใช้เวลานานเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับการทำงานพื้นฐาน.  
- **ฉันต้องการไลเซนส์หรือไม่?** สามารถใช้รุ่นทดลองฟรีเพื่อประเมิน; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 ขึ้นไป.  
- **ฉันสามารถปรับแต่งสไตล์ของตารางได้หรือไม่?** ได้ – คุณสามารถแก้ไขแบบอักษร, สี, และเส้นขอบเซลล์ผ่าน API.

## ข้อกำหนดเบื้องต้น
ก่อนเริ่มทำตามบทเรียน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:
- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java.  
- ไลบรารี Aspose.Note สำหรับ Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/note/java/).  
- สภาพแวดล้อมการพัฒนาแบบบูรณาการ (IDE) ที่ตั้งค่าไว้สำหรับการพัฒนา Java.

## นำเข้าแพ็กเกจ
ตรวจสอบให้แน่ใจว่าได้นำเข้าแพ็กเกจที่จำเป็นเพื่อเริ่มโครงการของคุณ เพิ่มคำสั่ง import ด้านล่างนี้ในคลาส Java ของคุณ:

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร
```java
String dataDir = "Your Document Directory";
```
แทนที่ `"Your Document Directory"` ด้วยเส้นทางจริงที่คุณต้องการบันทึกเอกสาร OneNote ของคุณ.

## ขั้นตอนที่ 2: สร้างหัวเรื่อง
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
สร้างหัวเรื่องที่ดึงดูดสายตาสำหรับเอกสารของคุณ ปรับขนาดฟอนต์, ความหนา, และการจัดแนวตามต้องการ.

## ขั้นตอนที่ 3: สร้างหน้าและโครงร่าง
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
ตั้งค่าหน้าและโครงร่างใหม่ แล้วเพิ่มหัวเรื่องที่สร้างไว้ก่อนหน้านี้ลงในโครงร่าง.

## ขั้นตอนที่ 4: เพิ่มข้อความสรุป
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
ใส่ข้อความสรุปสั้น ๆ เพื่อให้บริบทกับตาราง.

## ขั้นตอนที่ 5: เพิ่มตารางใน OneNote
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// Remaining steps are involved in setting up the table structure, header row, and adding empty rows.
// Refer to the provided code for detailed implementation.
```
สร้างโครงสร้างตารางและเติมข้อมูลที่เกี่ยวข้อง โค้ดตัวอย่างรวมการเพิ่มคอลัมน์, แถวหัวตาราง, แถวว่าง, และเนื้อหาเทมเพลตสำหรับคอลัมน์ “Contacts”.

## ขั้นตอนที่ 6: บันทึกเอกสาร
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
บันทึกเอกสารที่คุณสร้างไว้โดยระบุชื่อไฟล์และเส้นทางไดเรกทอรีที่ต้องการ.

## สรุป
ขอแสดงความยินดี! คุณได้ **เพิ่มตารางใน OneNote** สำเร็จโดยใช้ Aspose.Note สำหรับ Java บทเรียนนี้แสดงกระบวนการทีละขั้นตอน ช่วยให้คุณสามารถเพิ่มศักยภาพการสร้างเอกสารโดยอัตโนมัติได้อย่างเต็มที่

## คำถามที่พบบ่อย
### Q: ฉันสามารถหาเอกสาร Aspose.Note สำหรับ Java ได้ที่ไหน?
คุณสามารถอ้างอิงเอกสารได้จาก [ที่นี่](https://reference.aspose.com/note/java/).

### Q: ฉันจะดาวน์โหลด Aspose.Note สำหรับ Java ได้อย่างไร?
คุณสามารถดาวน์โหลดได้จาก [ลิงก์นี้](https://releases.aspose.com/note/java/).

### Q: มีการทดลองใช้ฟรีหรือไม่?
ใช่, คุณสามารถเข้าถึงการทดลองใช้ฟรีได้จาก [ที่นี่](https://releases.aspose.com/).

### Q: ฉันสามารถรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้จากที่ไหน?
เยี่ยมชมฟอรั่มสนับสนุนได้ที่ [ที่นี่](https://forum.aspose.com/c/note/28).

### Q: ฉันสามารถขอรับไลเซนส์ชั่วคราวได้หรือไม่?
ใช่, คุณสามารถขอรับไลเซนส์ชั่วคราวได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2026-01-23  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}