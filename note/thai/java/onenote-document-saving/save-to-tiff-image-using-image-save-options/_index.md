---
date: 2026-11-05
description: เรียนรู้วิธีลดขนาดไฟล์ TIFF เมื่อแปลงโน้ตบุ๊ก OneNote เป็น TIFF ด้วย
  Java โดยใช้ Aspose.Note รวมถึงตัวเลือก JPEG, PackBits และ TIFF ขาว‑ดำ
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: วิธีลดขนาดไฟล์ TIFF เมื่อแปลง OneNote ด้วย Java
og_description: เรียนรู้วิธีลดขนาดไฟล์ TIFF เมื่อแปลงโน้ตบุ๊ก OneNote เป็น TIFF ด้วย
  Java โดยใช้ Aspose.Note รวมถึงตัวเลือก JPEG, PackBits และ TIFF ขาว‑ดำ
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: วิธีลดขนาดไฟล์ TIFF เมื่อแปลง OneNote ด้วย Java
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: วิธีลดขนาดไฟล์ TIFF เมื่อแปลง OneNote ด้วย Java
url: /th/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีลดขนาดไฟล์ TIFF เมื่อแปลง OneNote ด้วย Java

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **ลดขนาดไฟล์ TIFF** ขณะแปลงสมุดบันทึก OneNote เป็นภาพ TIFF ด้วย Aspose.Note for Java เราจะอธิบายวิธีการบีบอัดสามแบบ—TIFF JPEG, PackBits, และ CCITT Group 3 (TIFF ขาว‑ดำ)—และแสดงวิธีปรับคุณภาพภาพ, ควบคุมโหมดสี, และทำให้ขนาดไฟล์เหมาะสมสำหรับเว็บ, การเก็บถาวร, หรือสถานการณ์แบบแฟกซ์

## คำตอบอย่างรวดเร็ว
- **What is TIFF JPEG compression?** วิธีบีบอัดแบบเสียคุณภาพที่ลดขนาดไฟล์ TIFF ขณะยังคงคุณภาพภาพไว้  
- **Which library handles the conversion?** Aspose.Note for Java.  
- **Do I need a license?** สามารถใช้รุ่นทดลองฟรีสำหรับการทดสอบ; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง  
- **Can I change the image quality?** ได้, ตั้งค่า property `quality` บน `ImageSaveOptions`.  
- **Is batch conversion possible?** แน่นอน – สามารถวนลูปผ่านเอกสารและใช้ตัวเลือกเดียวกัน  

## ภาพรวมการบีบอัด TIFF JPEG

การบีบอัด TIFF JPEG เก็บข้อมูลภาพในคอนเทนเนอร์ TIFF แต่ใช้ขั้นตอนการบีบอัดแบบเสียคุณภาพของ JPEG เพื่อลดขนาดไฟล์ เหมาะเมื่อคุณต้องการสมดุลระหว่าง **tiff image quality** กับขนาดไฟล์ที่เล็กลง, โดยเฉพาะสำหรับเว็บหรือการเก็บถาวร

## ทำไมต้องใช้ประเภทการบีบอัด TIFF ที่แตกต่างกัน?

คุณเลือกประเภทการบีบอัดตามเนื้อหาและความต้องการการจัดเก็บ: JPEG ทำงานดีที่สุดกับภาพถ่าย, PackBits ให้การบีบอัดแบบไม่เสียคุณภาพสำหรับกราฟิกที่มีพื้นที่สีเดียวขนาดใหญ่, และ CCITT Group 3 ให้การบีบอัดอัตราสูงสำหรับเอกสารแบบแฟกซ์สีขาว‑ดำ การเลือกวิธีที่เหมาะสมทำให้คุณ **ลดขนาดไฟล์ TIFF** โดยไม่กระทบคุณภาพภาพที่แอปพลิเคชันของคุณต้องการ

## การเลือกการบีบอัดที่เหมาะสม
- **JPEG** – คุณภาพที่ปรับได้ (0‑100) ช่วยให้คุณแลกเปลี่ยนระหว่างขนาดกับรายละเอียด, เหมาะกับหน้าที่มีสีสันมาก  
- **PackBits** – การบีบอัดแบบไม่เสียคุณภาพแบบ run‑length; เหมาะเมื่อคุณต้องการรักษาพิกเซลทุกพิกเซลให้ตรงกัน  
- **CCITT Group 3** – เฉพาะสีขาว‑ดำ; ให้การบีบอัดสูงสุดสำหรับข้อความสแกนหรือเอกสารแฟกซ์  

## แปลง OneNote เป็น TIFF ด้วย Aspose.Note

หากเป้าหมายของคุณคือ **convert OneNote to TIFF**, วิธีทั้งสามด้านล่างครอบคลุมสถานการณ์ที่พบบ่อยที่สุด แต่ละวิธีจะโหลดไฟล์ `.one`, ตั้งค่า `ImageSaveOptions`, และบันทึกผลลัพธ์เป็นไฟล์ `.tiff`

## ข้อกำหนดเบื้องต้น
- ติดตั้ง Java Development Kit (JDK)  
- เพิ่มไลบรารี Aspose.Note for Java ลงในโปรเจกต์ของคุณ (Maven/Gradle หรือ JAR แบบแมนนวล)  
- มีความคุ้นเคยพื้นฐานกับไวยากรณ์ Java  

## นำเข้าแพ็กเกจ

คลาส `ImageSaveOptions`, `TiffCompression`, และ `ColorMode` เป็นแกนหลักของ API การแปลง  

`ImageSaveOptions` กำหนดตัวเลือกสำหรับการบันทึกภาพ, เช่น รูปแบบและการบีบอัด  
`TiffCompression` แสดงรายการอัลกอริทึมการบีบอัด TIFF ที่รองรับ  
`ColorMode` ระบุความลึกของสี, เช่น สีหรือขาว‑ดำ  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## ขั้นตอนที่ 1: บันทึกเป็น TIFF ด้วยการบีบอัด TIFF JPEG

### การบันทึก TIFF ด้วยการบีบอัด JPEG ใน Java

โหลดไฟล์ OneNote, ตั้งค่า `ImageSaveOptions` ด้วยการบีบอัด JPEG, ตั้งค่า `quality` หากต้องการ, แล้วเรียกเมธอดบันทึก รูปแบบสองขั้นตอนนี้ให้คุณควบคุมขนาดผลลัพธ์และคุณภาพภาพได้เต็มที่

1. ชี้ `dataDir` ไปยังโฟลเดอร์ที่มีไฟล์ `.one` ของคุณ  
2. เรียก `SaveToTiffUsingJpegCompression()` จากเมธอดหลักหรือเซอร์วิสของคุณ  
3. ไฟล์ `.tiff` ที่ได้จะปรากฏในไดเรกทอรีเดียวกัน  

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**คำอธิบาย**
- `ImageSaveOptions` บอก Aspose.Note ให้ส่งออกเป็นไฟล์ TIFF  
- `setTiffCompression(TiffCompression.Jpeg)` เลือกการบีบอัด JPEG  
- `setQuality(93)` (ไม่บังคับ) ปรับคุณภาพภาพอย่างละเอียด; ค่าต่ำกว่าจะทำให้ไฟล์เล็กลง  

## ภาพรวมการบีบอัด TIFF PackBits

PackBits เป็นอัลกอริทึมการบีบอัดแบบไม่เสียคุณภาพที่ทำงานดีที่สุดกับภาพที่มีพื้นที่สีเดียวขนาดใหญ่ มักถูกเรียกว่า **tiff packbits compression** ในเอกสาร

## การบันทึก TIFF ด้วยการบีบอัด PackBits ใน Java

หากคุณต้องการตัวเลือกแบบไม่เสียคุณภาพ, PackBits เป็นอัลกอริทึม run‑length ง่ายที่ทำงานดีสำหรับกราฟิกที่มีสีเดียว ตั้งค่า `ImageSaveOptions` ด้วย `TiffCompression.PackBits` แล้วบันทึกเอกสาร

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**คำอธิบาย**
- `setTiffCompression(TiffCompression.PackBits)` สลับวิธีการบีบอัด  
- ไม่ต้องตั้งค่าคุณภาพเพราะ PackBits เป็นการบีบอัดแบบไม่เสียคุณภาพ  

## การบันทึก TIFF ด้วยการบีบอัด CCITT Group 3 ใน Java

สำหรับเอกสารแบบแฟกซ์คุณมักต้องการ **black and white TIFF** CCITT Group 3 ให้การบีบอัดสูงสำหรับภาพโมโนโครม ตั้งค่าโหมดสีเป็นขาว‑ดำและเลือก enum การบีบอัด CCITT 3

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**คำอธิบาย**
- `setColorMode(ColorMode.BlackAndWhite)` บังคับให้ผลลัพธ์เป็นโมโนโครม  
- `setTiffCompression(TiffCompression.Ccitt3)` ใช้การบีบอัดที่ออกแบบมาสำหรับแฟกซ์  

## ปัญหาทั่วไป & เคล็ดลับ

| Issue | Solution |
|-------|----------|
| **Output file is larger than expected** | ลองลดค่า `quality` ของ JPEG หรือเปลี่ยนเป็น PackBits หากยอมรับการบีบอัดแบบไม่เสียคุณภาพ |
| **Colors appear washed out** | ตรวจสอบว่าคุณไม่ได้ตั้งค่า `ColorMode.BlackAndWhite` โดยไม่ได้ตั้งใจเมื่อต้องการสีเต็ม |
| **Unsupported image format error** | ยืนยันว่าคุณใช้เวอร์ชันล่าสุดของ Aspose.Note; รุ่นเก่าอาจไม่มี enum การบีบอัดบางตัว |
| **LicenseException at runtime** | ติดตั้งลิขสิทธิ์ Aspose.Note ที่ถูกต้อง (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) |

## คำถามที่พบบ่อย

**Q: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these options?**  
A: ใช่. แม้ Aspose.Note จะเน้นไฟล์ OneNote, ไลบรารี Aspose.PDF, Aspose.Words และอื่น ๆ มี `ImageSaveOptions` ที่คล้ายกันสำหรับฟอร์แมตของพวกเขา  

**Q: How does TIFF JPEG compression differ from a standard JPEG file?**  
A: อัลกอริทึม JPEG เหมือนกัน, แต่ข้อมูลภาพอยู่ในคอนเทนเนอร์ TIFF ซึ่งสามารถเก็บหลายหน้าและเมตาดาต้าที่สมบูรณ์กว่า  

**Q: Is it possible to batch‑process many `.one` files?**  
A: แน่นอน. วนลูปผ่านไดเรกทอรี, เรียกใช้วิธีใดวิธีหนึ่งสำหรับแต่ละไฟล์, แล้วเก็บ TIFF ที่ได้  

**Q: Can I control the DPI/resolution of the output TIFF?**  
A: ได้. ใช้ `options.setResolution(int dpi)` ก่อนบันทึก  

**Q: Does Aspose.Note support asynchronous processing?**  
A: API เองทำงานแบบ synchronous, แต่คุณสามารถห่อเมธอดด้วย `CompletableFuture` ของ Java หรือใช้ thread pool เพื่อประมวลผลแบบขนาน  

## สรุป

คุณมีชุดเครื่องมือ **Java TIFF conversion** ครบถ้วนที่ช่วยให้คุณ **reduce TIFF file size** ขณะบันทึกเอกสาร OneNote เป็นไฟล์ TIFF ด้วยการบีบอัด JPEG, PackBits, หรือ CCITT Group 3 Fax ปรับคุณภาพ, โหมดสี, และความละเอียดให้ตรงตามความต้องการของคุณ, แล้วรวมวิธีเหล่านี้เข้าไปในกระบวนการทำงานแบบ batch เพื่อเพิ่มประสิทธิภาพสูงสุด

---

**อัปเดตล่าสุด:** 2026-11-05  
**ทดสอบด้วย:** Aspose.Note for Java 26.4 (latest at time of writing)  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [วิธีเรนเดอร์ภาพหน้า OneNote (JPEG) โดยใช้ Save Format กับ Aspose.Note for Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [ใช้ Aspose.Note for Java เพื่อบันทึก OneNote เป็น PNG พร้อมตัวเลือก – แปลงสมุดบันทึกเป็นภาพ](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [วิธีส่งออก OneNote เป็นภาพระดับสีเทา – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}