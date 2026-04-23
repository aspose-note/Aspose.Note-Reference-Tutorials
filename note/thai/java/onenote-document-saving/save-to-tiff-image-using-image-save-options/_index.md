---
date: 2026-03-14
description: เรียนรู้วิธีบันทึกเอกสาร OneNote เป็นไฟล์ TIFF โดยใช้การบีบอัด TIFF JPEG,
  การบีบอัด TIFF PackBits หรือ CCITT Group 3 Fax ใน Java ควบคุมคุณภาพภาพ ขนาดไฟล์
  และโหมดสีด้วย Aspose.Note
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: บันทึกเป็นไฟล์ TIFF โดยใช้การบีบอัด JPEG ของ TIFF ใน OneNote
url: /th/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

 final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกเป็นภาพ TIFF ด้วยการบีบอัด TIFF JPEG ใน OneNote

## คำแนะนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีบันทึกเอกสาร OneNote เป็นไฟล์ TIFF ด้วยการบีบอัด TIFF JPEG** และสองวิธีการบีบอัดที่เป็นที่นิยมอื่น ๆ เราจะอธิบายขั้นตอนการตั้งค่าที่จำเป็น, การนำเข้าแพ็กเกจ Java ที่ต้องใช้, และให้โค้ดแบบขั้นตอนต่อขั้นตอนสำหรับแต่ละตัวเลือกการบีบอัด เมื่อเสร็จคุณจะสามารถควบคุม **คุณภาพภาพ TIFF **, ลดขนาดไฟล์, และแม้กระทั่งสร้างไฟล์ TIFF ขาว‑ดำสำหรับการส่งแฟกซ์ได้

## คำตอบสั้น
- **TIFF JPEG compression คืออะไร?** วิธีบีบอัดแบบเสียคุณภาพที่ลดขนาดไฟล์ TIFF ในขณะที่ยังคงคุณภาพภาพไว้.  
- **ไลบรารีใดที่จัดการการแปลง?** Aspose.Note for Java.  
- **ฉันต้องมีลิขสิทธิ์หรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการทดสอบ; จำเป็นต้องมีลิขสิทธิ์สำหรับการใช้งานจริง.  
- **ฉันสามารถเปลี่ยนคุณภาพภาพได้หรือไม่?** ได้, ตั้งค่า property `quality` ใน `ImageSaveOptions`.  
- **สามารถทำการแปลงเป็นชุดได้หรือไม่?** แน่นอน – วนลูปผ่านเอกสารและใช้ตัวเลือกเดียวกัน.

## TIFF JPEG Compression คืออะไร?
การบีบอัด TIFF JPEG จะเก็บข้อมูลภาพในคอนเทนเนอร์ TIFF แต่ใช้อัลกอริทึม JPEG แบบเสียคุณภาพเพื่อทำให้ไฟล์เล็กลง เหมาะอย่างยิ่งเมื่อคุณต้องการสมดุลระหว่าง **คุณภาพภาพ TIFF** กับขนาดไฟล์ที่เล็กลง, โดยเฉพาะสำหรับการใช้งานบนเว็บหรือการเก็บถาวร

## ทำไมต้องใช้ประเภทการบีบอัด TIFF ที่แตกต่างกัน?
- **JPEG** – เหมาะสำหรับภาพถ่าย; มีคุณภาพที่ปรับได้.  
- **PackBits** – การเข้ารหัสแบบรันเลนธ์ที่ง่ายและไม่มีการสูญเสีย; มีประโยชน์สำหรับกราฟิกที่มีพื้นที่สีเดียวขนาดใหญ่.  
- **CCITT Group 3 Fax** – สีขาว‑ดำเท่านั้น; เหมาะสำหรับเอกสารสแกนและการส่งแฟกซ์.  

การเลือกการบีบอัดที่เหมาะสมจะทำให้คุณตอบสนองข้อจำกัดด้านพื้นที่จัดเก็บโดยไม่สูญเสียความคมชัดของภาพที่แอปพลิเคชันของคุณต้องการ

## แปลง One เป็น TIFF ด้วย Aspose.Note
หากเป้าหมายของคุณคือ **แปลง OneNote เป็น TIFF**, วิธีทั้งสามด้านล่างครอบคลุมสถานการณ์ที่พบบ่อยที่สุด แต่ละวิธีจะโหลดไฟล์ `.one`, ตั้งค่า `ImageSaveOptions`, และบันทึกผลลัพธ์เป็นไฟล์ `.tiff`

## ข้อกำหนดเบื้องต้น

- ติดตั้ง Java Development Kit (JDK) แล้ว.  
- เพิ่มไลบรารี Aspose.Note for Java ลงในโปรเจคของคุณ (Maven/Gradle หรือ JAR แบบแมนนวล).  
- มีความคุ้นเคยพื้นฐานกับไวยากรณ์ของ Java.

## นำเข้าแพ็กเกจ

ขั้นแรก, นำคลาส Aspose.Note ที่จำเป็นเข้ามาในไฟล์ Java ของคุณ:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## ขั้นตอนที่ 1: บันทึกเป็น TIFF ด้วยการบีบอัด TIFF JPEG

ด้านล่างเป็นเมธอดเต็มที่โหลดไฟล์ OneNote และบันทึกเป็น TIFF ด้วยการบีบอัด JPEG. ปรับค่า `quality` (0‑100) เพื่อควบคุม **คุณภาพภาพ TIFF**.

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

- `ImageSaveOptions` บอก Aspose.Note ให้สร้างไฟล์ TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` เลือกการบีบอัดแบบ JPEG.  
- `setQuality(93)` (ไม่บังคับ) ปรับคุณภาพของภาพ; ค่าต่ำจะทำให้ไฟล์เล็กลง.

### วิธีบันทึก TIFF ด้วยการบีบอัด JPEG ใน Java
1. ตั้งค่า `dataDir` ให้ชี้ไปยังโฟลเดอร์ที่มีไฟล์ `.one` ของ **คุณ **.  
2. เรียก `SaveToTiffUsingJpegCompression()` จากเมธอด `main` ของ **คุณ ** หรือจาก **service**.  
3. ไฟล์ `.tiff` ที่ได้จะปรากฏในไดเรกทอรีเดียวกัน.

## ภาพรวมการบีบอัด TIFF PackBits

PackBits เป็นอัลกอริทึมการบีบอัดแบบไม่มีการสูญเสียที่ทำงานได้ดีที่สุดกับภาพที่มีพื้นที่สีเดียวขนาดใหญ่ มักเรียกว่า **tiff packbits compression** ในเอกสาร

## ขั้นตอนที่ 2: บันทึกเป็น TIFF ด้วยการบีบอัด PackBits

หากคุณต้องการตัวเลือกแบบไม่มีการสูญเสีย, PackBits เป็นอัลกอริทึมรัน‑เลนธ์แบบง่ายที่ทำงานได้ดีสำหรับกราฟิกที่มีสีเดียว

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

- `setTiffCompression(TiffCompression.PackBits)` เปลี่ยนวิธีการบีบอัด.  
- ไม่จำเป็นต้องตั้งค่าคุณภาพเนื่องจาก PackBits เป็นการบีบอัดแบบไม่มีการสูญเสีย.

## ขั้นตอนที่ 3: บันทึกเป็น TIFF ด้วยการบีบอัด CCITT Group 3 Fax (TIFF ขาว‑ดำ)

สำหรับเอกสารสไตล์แฟกซ์คุณมักต้องการ **TIFF ขาว‑ดำ**. CCITT Group 3 ให้การบีบอัดสูงสำหรับภาพโมโนโครม

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

- `setColorMode(ColorMode.BlackAndWhite)` บังคับให้ผลลัพธ์เป็นโมโนโครม.  
- `setTiffCompression(TiffCompression.Ccitt3)` ใช้การบีบอัดที่ออกแบบมาสำหรับแฟกซ์.

## ปัญหาทั่วไป & เคล็ดลับ

| ปัญหา | วิธีแก้ |
|-------|----------|
| **ไฟล์ผลลัพธ์ใหญ่กว่าที่คาดไว้** | ลองลดค่า JPEG `quality` หรือเปลี่ยนเป็น PackBits หากการบีบอัดแบบไม่มีการสูญเสียเป็นที่ยอมรับได้. |
| **สีดูซีด** | ตรวจสอบว่าคุณไม่ได้ตั้งค่า `ColorMode.BlackAndWhite` โดยไม่ได้ตั้งใจเมื่อคุณต้องการสีเต็ม. |
| **ข้อผิดพลาดรูปแบบภาพที่ไม่รองรับ** | ตรวจสอบว่าคุณใช้เวอร์ชันล่าสุดของ Aspose.Note; เวอร์ชันเก่าอาจไม่มี enum การบีบอัดบางอย่าง. |
| **LicenseException ระหว่างรัน** | ติดตั้งลิขสิทธิ์ Aspose.Note ที่ถูกต้อง (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## คำถามที่พบบ่อย

**Q: ฉันสามารถแปลงประเภทเอกสารอื่น (เช่น PDF, DOCX) เป็น TIFF ด้วยตัวเลือกเหล่านี้ได้หรือไม่?**  
A: ได้. แม้ว่า Aspose.Note จะเน้นที่ไฟล์ OneNote, Aspose.PDF, Aspose.Words, และไลบรารีอื่น ๆ มี `ImageSaveOptions` ที่คล้ายกันสำหรับฟอร์แมตของพวกเขา

**Q: การบีบอัด TIFF JPEG แตกต่างจากไฟล์ JPEG มาตรฐานอย่างไร?**  
A: อัลกอริทึม JPEG เหมือนกัน, แต่ข้อมูลภาพอยู่ในคอนเทนเนอร์ TIFF ซึ่งสามารถเก็บหลายหน้าและเมทาดาต้าที่หลากหลายกว่า

**Q: สามารถประมวลผลหลายไฟล์ `.one` เป็นชุดได้หรือไม่?**  
A: แน่นอน. วนลูปผ่านไดเรกทอรี, เรียกใช้เมธอดใดเมธอดหนึ่งสำหรับแต่ละไฟล์, แล้วเก็บไฟล์ TIFF ที่ได้

**Q: ฉันสามารถควบคุม DPI/ความละเอียดของ TIFF ผลลัพธ์ได้หรือไม่?**  
A: ได้. ใช้ `options.setResolution(int dpi)` ก่อนบันทึก

**Q: Aspose.Note รองรับการประมวลผลแบบอะซิงโครนัสหรือไม่?**  
A: API เองทำงานแบบซิงโครนัส, แต่คุณสามารถห่อหุ้มการเรียกใช้ด้วย `CompletableFuture` ของ Java หรือใช้ thread pool เพื่อการทำงานแบบขนานได้

## สรุป

ตอนนี้คุณมีชุดเครื่องมือ **java tiff conversion** ที่ครบถ้วนซึ่งช่วยให้คุณบันทึกเอกสาร OneNote เป็นไฟล์ TIFF ด้วยการบีบอัด JPEG, PackBits, หรือ CCITT Group 3 Fax. ปรับคุณภาพ, โหมดสี, และความละเอียดให้ตรงกับความต้องการ **คุณภาพภาพ TIFF** ของคุณ, และรวมเมธอดเหล่านี้เข้าในกระบวนการทำงานเป็นชุดเพื่อเพิ่มประสิทธิภาพสูงสุด

---

**อัปเดตล่าสุด:** 2026-03-14  
**ทดสอบกับ:** Aspose.Note for Java 23.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}