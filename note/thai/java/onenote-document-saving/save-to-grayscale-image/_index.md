---
date: 2026-06-30
description: เรียนรู้วิธีส่งออก OneNote โดยบันทึกเอกสารเป็นภาพ PNG ระดับสีเทาโดยใช้
  Aspose.Note สำหรับ Java รวมขั้นตอนการโหลดเอกสาร OneNote และสร้างภาพระดับสีเทา
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: วิธีส่งออก OneNote เป็นภาพระดับสีเทา – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: วิธีส่งออก OneNote เป็นภาพระดับสีเทา – Aspose.Note
url: /th/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกเป็นภาพระดับสีเทาใน OneNote - Aspose.Note

## บทนำ

ในบทแนะนำนี้คุณจะได้ค้นพบ **how to export onenote** โดยการแปลงไฟล์ OneNote `.one` เป็นภาพ PNG ระดับสีเทาคุณภาพสูงโดยใช้ Aspose.Note สำหรับ Java การแปลงเป็นระดับสีเทาเป็นสิ่งที่นักพัฒนา Java มักต้องการสำหรับการพิมพ์ การเก็บถาวร หรือเพื่อ **reduce OneNote size** โดยไม่สูญเสียเนื้อหาที่สำคัญ เราจะอธิบายขั้นตอนการโหลดเอกสาร OneNote การกำหนดค่าตัวเลือกการบันทึก—รวมถึง **adjust image resolution**—และสุดท้ายบันทึกเอกสารเป็น PNG

## คำตอบสั้น
- **What does “how to export onenote” mean?** หมายถึงการแปลงไฟล์ OneNote เป็นรูปแบบอื่นโดยใช้โปรแกรม เช่น แปลงเป็นภาพ ด้วยโค้ด  
- **Which format is best for grayscale output?** PNG ทำงานได้ดีเพราะรักษาคุณภาพ loss‑less และรองรับโหมดสีเทาเฉพาะ  
- **Do I need a license?** ต้องมีใบอนุญาต Aspose.Note ที่ถูกต้องสำหรับการใช้งานในผลิตภัณฑ์; มีใบอนุญาตทดลองชั่วคราวสำหรับการทดสอบ  
- **What Java version is required?** แนะนำให้ใช้ Java 8 หรือใหม่กว่า  
- **Can I change the image size?** ได้, คุณสามารถปรับคุณสมบัติของ `ImageSaveOptions` เช่น `Resolution` หรือ `PageSize` ก่อนบันทึก  

## “how to export onenote” คืออะไร?
การส่งออก OneNote หมายถึงการแปลงไฟล์ OneNote `.one` เป็นรูปแบบอื่นโดยใช้โปรแกรม—เช่น PDF, HTML หรือภาพ ในคู่มือนี้เรามุ่งเน้นที่ **creating grayscale PNG** ซึ่งเป็นความต้องการทั่วไปสำหรับเอกสารหรือกระบวนการพิมพ์ที่พร้อมใช้งาน ด้วย Aspose.Note การแปลงจะทำทั้งหมดในหน่วยความจำ ดังนั้นคุณไม่จำเป็นต้องติดตั้ง Microsoft OneNote บนเซิร์ฟเวอร์

## ทำไมต้องส่งออก OneNote เป็นภาพระดับสีเทา?
PNG ระดับสีเทามักจะมีขนาด **30‑40 % เล็กกว่า** รูปแบบสีเต็ม ซึ่งช่วยเร่งการส่งมอบบนเว็บและลดค่าใช้จ่ายในการจัดเก็บ นอกจากนี้ยังให้ **clearer contrast** บนเครื่องพิมพ์เลเซอร์ ทำให้รายงานอ่านง่ายขึ้น เนื่องจาก PNG รองรับอย่างทั่วโลก ไฟล์ที่ได้จึงทำงานได้บนเบราว์เซอร์, อุปกรณ์มือถือ, และโปรแกรมแก้ไขบนเดสก์ท็อปโดยไม่ต้องใช้โค้ดเพิ่มเติม

## ข้อกำหนดเบื้องต้น
1. ติดตั้ง Java Development Kit (JDK) 8 หรือใหม่กว่า  
2. ไลบรารี Aspose.Note สำหรับ Java – ดาวน์โหลดเวอร์ชันล่าสุดจาก [here](https://releases.aspose.com/note/java/)  
3. มีความเข้าใจพื้นฐานเกี่ยวกับไวยากรณ์ Java และการตั้งค่าโครงการ Maven/Gradle  

## นำเข้าแพ็กเกจ
คลาส `ImageSaveOptions` ควบคุมวิธีการเรนเดอร์เอกสารเป็นภาพ  
`ColorMode` เป็น enumeration ที่ให้คุณสลับระหว่างการแสดงผลสีเต็มและระดับสีเทา

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote
`Document` แสดงถึงสมุดบันทึก OneNote และให้เมธอดสำหรับโหลด, แก้ไข, และบันทึกเนื้อหาของมัน ขั้นแรก, **load the OneNote document** เข้าไปใน Aspose.Note แทนที่ `"Your Document Directory"` ด้วยเส้นทางไปยังโฟลเดอร์ในเครื่องของคุณและ `"Aspose.one"` ด้วยชื่อไฟล์ OneNote ของคุณ

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางและตัวเลือกการส่งออก
`ImageSaveOptions` กำหนดวิธีการเรนเดอร์เอกสาร OneNote เป็นไฟล์ภาพ `ColorMode` enumeration เลือกโหมดการเรนเดอร์สี เช่น grayscale หรือ full‑color กำหนดเส้นทางการส่งออกสำหรับภาพระดับสีเทาและระบุตัวเลือกการบันทึก เราจะตั้งค่า `ColorMode` เป็น `GrayScale` และใช้รูปแบบ **save document as PNG** คุณยังสามารถ **adjust image resolution** เป็น 300 DPI เพื่อการพิมพ์คุณภาพสูงได้

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## ขั้นตอนที่ 3: บันทึกเอกสาร
สุดท้าย, บันทึกเอกสารเป็นภาพ PNG ระดับสีเทาโดยใช้ตัวเลือกที่กำหนดไว้ เมธอด `save` จะเขียนไฟล์ลงดิสก์โดยไม่ต้องใช้ไฟล์ชั่วคราวใด ๆ

```java
oneFile.save(dataDir, options);
```

## ปัญหาทั่วไปและวิธีแก้
- **FileNotFoundException** – ตรวจสอบว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและไฟล์ `.one` มีอยู่  
- **LicenseException** – ตรวจสอบว่าคุณได้ใส่ใบอนุญาต Aspose.Note ที่ถูกต้องก่อนเรียก `save`  
- **Low‑resolution output** – ปรับ `options.setResolution(300)` เพื่อเพิ่ม DPI; DPI ที่สูงขึ้นให้การพิมพ์คมชัดขึ้นแต่ไฟล์ใหญ่ขึ้น  

## คำถามที่พบบ่อย
**Q1: Can I save the grayscale image in a different format?**  
A1: ใช่, เพียงเปลี่ยนพารามิเตอร์ `SaveFormat` ในคอนสตรัคเตอร์ `ImageSaveOptions` เป็น `Jpeg`, `Bmp`, หรือรูปแบบภาพที่รองรับกว่า 20 รูปแบบ  

**Q2: Is Aspose.Note compatible with all versions of OneNote documents?**  
A2: Aspose.Note รองรับ Microsoft OneNote 2010 และรุ่นต่อไป, ครอบคลุมกว่า 95 % ของสมุดบันทึกที่ใช้งานอยู่ในปัจจุบัน  

**Q3: Does Aspose.Note require a license to use?**  
A3: จำเป็นต้องมีใบอนุญาตที่ถูกต้องสำหรับการใช้งานในผลิตภัณฑ์, แต่สามารถขอใบอนุญาตทดลองชั่วคราวเพื่อการประเมินได้ฟรี  

**Q4: Can I manipulate other aspects of the document before saving it as an image?**  
A4: แน่นอน! Aspose.Note มี API ให้แก้ไขส่วน, หน้า, และองค์ประกอบแต่ละอย่าง เช่น ข้อความ, ตาราง, และภาพ ก่อนทำการส่งออก  

**Q5: Where can I find support if I encounter issues?**  
A5: คุณสามารถหาการสนับสนุนได้ในฟอรั่ม Aspose.Note [here](https://forum.aspose.com/c/note/28)  

## สรุป
คุณได้เรียนรู้ **how to export onenote** โดยการโหลดไฟล์ OneNote, กำหนดค่าตัวเลือกการบันทึกเพื่อ **create a grayscale image**, และ **saving the document as PNG** วิธีนี้เหมาะสำหรับการสร้างภาพที่มีน้ำหนักเบาและพร้อมพิมพ์จากสมุดบันทึก OneNote อย่าลังเลที่จะทดลองตั้งค่า `ColorMode` อื่น ๆ, ค่า DPI ที่สูงขึ้น, หรือรูปแบบภาพทางเลือกเพื่อให้ตรงกับความต้องการของโครงการของคุณ

---

**อัปเดตล่าสุด:** 2026-06-30  
**ทดสอบด้วย:** Aspose.Note 27.0 for Java  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง
- [ส่งออกหน้า OneNote เป็นภาพ PNG ใน Java โดยใช้ Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote set jpeg resolution – ตั้งค่าความละเอียดภาพเอาต์พุตใน OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [วิธีบันทึก OneNote เป็น PDF ด้วย Aspose.Note สำหรับ Java](/note/java/onenote-document-loading/load-save-format/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}