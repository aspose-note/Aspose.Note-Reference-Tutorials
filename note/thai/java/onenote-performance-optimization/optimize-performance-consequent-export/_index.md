---
date: 2026-01-18
description: เรียนรู้วิธีการส่งออก OneNote อย่างมีประสิทธิภาพและวิธีการส่งออก OneNote
  ด้วยประสิทธิภาพที่เพิ่มขึ้นโดยใช้ Aspose.Note สำหรับ Java รวมถึงขั้นตอนการตั้งค่ารูปแบบข้อความเริ่มต้นและบันทึก
  OneNote เป็นภาพ
linktitle: How to Export OneNote – Optimize Performance for Export Operations in Java
second_title: Aspose.Note Java API
title: วิธีส่งออก OneNote – ปรับประสิทธิภาพการทำงานของการส่งออกใน Java
url: /th/java/onenote-performance-optimization/optimize-performance-consequent-export/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการส่งออก OneNote – ปรับประสิทธิภาพการทำงานของการส่งออกใน Java

## บทนำ

การส่งออกสมุดบันทึก OneNote อาจเป็นคอขวดเมื่อคุณต้องสร้างรายงาน, แบ่งปันเนื้อหา, หรือเก็บข้อมูลเป็นถาวร ในบทแนะนำนี้เราจะแสดง **วิธีการส่งออก OneNote** อย่างรวดเร็วและเชื่อถือได้โดยใช้ Aspose.Note for Java คุณจะได้เรียนรู้เทคนิคการปรับปรุงความเร็วการส่งออก, ตั้งค่ารูปแบบข้อความเริ่มต้น, และแม้แต่ **บันทึก OneNote เป็นไฟล์รูปภาพ** เช่น JPG หรือ BMP

## คำตอบอย่างรวดเร็ว
- **ไลบรารีหลักคืออะไร?** Aspose.Note for Java  
- **สามารถส่งออกเป็นรูปแบบใดได้บ้าง?** HTML, PDF, JPG, BMP (และอื่น ๆ)  
- **จะปรับปรุงประสิทธิภาพอย่างไร?** ปิดการตรวจจับการจัดวางอัตโนมัติและใช้วัตถุเอกสารซ้ำ  
- **สามารถตั้งค่ารูปแบบข้อความเริ่มต้นได้หรือไม่?** ใช่ – ใช้ `ParagraphStyle` ก่อนเพิ่มเนื้อหา  
- **การส่งออกเป็นรูปภาพรองรับหรือไม่?** แน่นอน, ใช้ `doc.save(...".jpg")` หรือ `.bmp`  

## อะไรคือ “วิธีการส่งออก OneNote”?

การส่งออก OneNote หมายถึงการแปลงโครงสร้างไฟล์ OneNote ดั้งเดิมให้เป็นรูปแบบพกพา (HTML, PDF, รูปภาพ ฯลฯ) ซึ่งทำให้สามารถแชร์ข้ามแพลตฟอร์ม, เข้าถึงแบบออฟไลน์, และรวมเข้ากับกระบวนการทำงานทางธุรกิจอื่น ๆ ได้

## ทำไมต้องปรับประสิทธิภาพการส่งออก?

สมุดบันทึกขนาดใหญ่ที่มีหลายหน้าและสื่อหลากหลายอาจทำให้การแปลงช้าโดยการปรับตั้งค่าบางอย่าง—เช่นการปิดการตรวจจับการเปลี่ยนแปลงการจัดวางอัตโนมัติ—คุณจะลดภาระการใช้ CPU และหน่วยความจำ ส่งผลให้การส่งออกเร็วขึ้นและคาดการณ์ได้ง่ายขึ้น

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน, โปรดตรวจสอบว่ามีการติดตั้งสิ่งต่อไปนี้แล้ว:

### 1. Java Development Kit (JDK)
ตรวจสอบให้แน่ใจว่าคุณมี JDK เวอร์ชันล่าสุด สามารถดาวน์โหลดได้จาก [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)

### 2. Aspose.Note for Java
รับแพคเกจ Aspose.Note for Java ล่าสุดจาก [download link](https://releases.aspose.com/note/java/)

### 3. Integrated Development Environment (IDE)
IDE สำหรับ Java ใดก็ได้—IntelliJ IDEA, Eclipse หรือ NetBeans ล้วนเป็นตัวเลือกที่ดี

## นำเข้าแพ็กเกจ

ก่อนจะลงลึกในโค้ด, ให้นำเข้าคลาสที่จำเป็น:

```java
import java.awt.Color;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1. เริ่มต้น Document และ Page

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
doc.setAutomaticLayoutChangesDetectionEnabled(false);
Page page = new Page();
```

เราจะสร้างอินสแตนซ์ `Document` ใหม่และ **ปิดการตรวจจับการเปลี่ยนแปลงการจัดวางอัตโนมัติ**—การปรับจูนสำคัญสำหรับการส่งออกที่เร็วขึ้น จากนั้นเพิ่มอ็อบเจกต์ `Page` ใหม่ที่ใช้เก็บเนื้อหา

### ขั้นตอนที่ 2. ตั้งค่ารูปแบบข้อความเริ่มต้น *(set default text style)*

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.BLACK)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

การกำหนด **รูปแบบข้อความเริ่มต้น** ครั้งเดียวและนำไปใช้ซ้ำสำหรับทุกองค์ประกอบข้อความจะช่วยลดเวลาในการประมวลผลและทำให้ลักษณะการแสดงผลสอดคล้องกัน

### ขั้นตอนที่ 3. เพิ่มหัวเรื่อง

```java
RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);

RichText titleDate = new RichText().append("2011,11,11");
titleDate.setParagraphStyle(textStyle);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);

Title title = new Title();
title.setTitleText(titleText);
title.setTitleDate(titleDate);
title.setTitleTime(titleTime);
page.setTitle(title);
```

ที่นี่เราจะสร้างส่วนหัวเรื่องด้วยวัตถุ `RichText` สามตัว (หัวเรื่อง, วันที่, เวลา) และใช้ **รูปแบบข้อความเริ่มต้น** ที่เรากำหนดไว้ก่อนหน้า

### ขั้นตอนที่ 4. เพิ่มโหนด Page

```java
doc.appendChildLast(page);
```

ตอนนี้หน้าได้เป็นส่วนหนึ่งของโครงสร้างเอกสารพร้อมสำหรับการส่งออกแล้ว

### ขั้นตอนที่ 5. บันทึกเอกสารในรูปแบบต่าง ๆ *(save onenote as image, convert onenote jpg)*

```java
doc.save(dataDir + "OptimizePerformanceForConsequentExportOperations_out.html");
doc.save(dataDir + "OptimizePerformanceForConsequentExportOperations_out.pdf");
doc.save(dataDir + "OptimizePerformanceForConsequentExportOperations_out.jpg");
doc.save(dataDir + "OptimizePerformanceForConsequentExportOperations_out.bmp");
```

เราจะแสดง **การบันทึก OneNote เป็นไฟล์รูปภาพ** (JPG, BMP) รวมถึง HTML และ PDF ซึ่งครอบคลุมสถานการณ์การส่งออกที่พบบ่อยที่สุด รวมถึงกรณีการ **แปลง OneNote เป็น JPG** ด้วย

### ขั้นตอนที่ 6. ตั้งค่าขนาดฟอนต์และตรวจจับการเปลี่ยนแปลงการจัดวาง

```java
textStyle.setFontSize(11);
doc.detectLayoutChanges();
```

หากต้องการปรับขนาดฟอนต์หลังการส่งออกครั้งแรก เพียงอัปเดต `ParagraphStyle` แล้วเรียก `detectLayoutChanges()` เพื่อให้การจัดวางอัปเดตโดยไม่ต้องสร้างเอกสารใหม่

## ปัญหาทั่วไป & เคล็ดลับ

- **ยังคงช้าอยู่?** ตรวจสอบว่าได้เรียก `setAutomaticLayoutChangesDetectionEnabled(false)` ก่อนเพิ่มหน้าใด ๆ  
- **รูปภาพแสดงเป็นสีขาว?** ตรวจสอบว่าโฟลเดอร์ปลายทางมีสิทธิ์เขียนและนามสกุลไฟล์รูปภาพตรงกับชื่อไฟล์  
- **สมุดบันทึกขนาดใหญ่ทำให้เกิด OutOfMemoryError?** ประมวลผลหน้าเป็นชุดหรือเพิ่มขนาด heap ของ JVM (`-Xmx2g`)  

## คำถามที่พบบ่อย

**ถาม: สามารถใช้ Aspose.Note for Java ส่งออกเอกสาร OneNote แบบโปรแกรมได้หรือไม่?**  
ตอบ: ใช่, Aspose.Note for Java มี API ครบถ้วนสำหรับจัดการและส่งออกสมุดบันทึก OneNote โดยไม่ต้องใช้แอปพลิเคชันเดสก์ท็อป

**ถาม: Aspose.Note for Java รองรับ IDE ของ Java ต่าง ๆ หรือไม่?**  
ตอบ: แน่นอน. ไลบรารีทำงานได้กับ IntelliJ IDEA, Eclipse, NetBeans และ IDE ใด ๆ ที่รองรับโครงการ Java มาตรฐาน

**ถาม: จะขอรับใบอนุญาตชั่วคราวสำหรับการทดสอบได้อย่างไร?**  
ตอบ: คุณสามารถขอใบอนุญาตชั่วคราวจาก [website](https://purchase.aspose.com/temporary-license/) ซึ่งช่วยให้คุณประเมินผลิตภัณฑ์ก่อนตัดสินใจซื้อ

**ถาม: Aspose.Note รองรับการส่งออกเป็นรูปแบบภาพเช่น JPG และ BMP หรือไม่?**  
ตอบ: ใช่, เมธอด `doc.save(...".jpg")` และ `doc.save(...".bmp")` ทำให้คุณ **บันทึก OneNote เป็นไฟล์รูปภาพ** ได้ง่าย ๆ เพื่อนำไปใส่ในรายงานหรือการนำเสนอ

**ถาม: จะหาแหล่งสนับสนุนจากชุมชนหรือถามคำถามทางเทคนิคได้ที่ไหน?**  
ตอบ: เยี่ยมชมฟอรั่มอย่างเป็นทางการของ Aspose ที่ [forum](https://forum.aspose.com/c/note/28) เพื่อรับความช่วยเหลือจากชุมชนและวิศวกรของ Aspose

## สรุป

โดยทำตามคู่มือนี้ คุณจะรู้ **วิธีการส่งออก OneNote** อย่างมีประสิทธิภาพ, วิธี **ตั้งค่ารูปแบบข้อความเริ่มต้น**, และวิธี **บันทึก OneNote เป็นไฟล์รูปภาพ** เช่น JPG และ BMP เทคนิคเหล่านี้ช่วยให้คุณสร้างไพป์ไลน์การส่งออกที่เร็วและเชื่อถือได้สำหรับแอปพลิเคชัน Java ใด ๆ

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-01-18  
**ทดสอบด้วย:** Aspose.Note for Java 24.12 (ล่าสุด)  
**ผู้เขียน:** Aspose  

---