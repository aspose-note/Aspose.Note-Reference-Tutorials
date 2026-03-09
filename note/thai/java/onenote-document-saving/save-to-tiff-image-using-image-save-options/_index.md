---
date: 2025-12-17
description: เรียนรู้วิธีบันทึกเอกสาร OneNote เป็นไฟล์ TIFF ด้วยการบีบอัด TIFF JPEG,
  PackBits หรือ CCITT Group 3 Fax ใน Java ควบคุมคุณภาพภาพ ขนาดไฟล์ และโหมดสีด้วย Aspose.Note
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: บันทึกเป็นภาพ TIFF ด้วยการบีบอัด JPEG ของ TIFF ใน OneNote
url: /th/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกเป็นภาพ TIFF โดยใช้การบีบอัด TIFF JPEG ใน OneNote

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีบันทึกเอกสาร OneNote เป็นไฟล์ TIFF ด้วยการบีบอัด TIFF JPEG** พร้อมวิธีการบีบอัดที่เป็นที่นิยมอีกสองแบบ เราจะอธิบายขั้นตอนการตั้งค่าที่จำเป็น การนำเข้าแพ็กเกจ Java ที่ต้องใช้ และให้โค้ดตัวอย่างแบบขั้นตอนต่อขั้นตอนสำหรับแต่ละตัวเลือกการบีบอัด เมื่อเสร็จสิ้นคุณจะสามารถควบคุม **คุณภาพภาพ TIFF ** ลดขนาดไฟล์ และแม้กระทั่งสร้างไฟล์ TIFF สีขาว‑ดำสำหรับการส่งแฟกซ์ได้

## คำตอบสั้น ๆ
- **TIFF JPEG compression คืออะไร?** วิธีบีบอัดแบบเสียคุณภาพที่ลดขนาดไฟล์ TIFF ในขณะที่ยังคงคุณภาพภาพที่มองเห็นได้  
- **ไลบรารีใดทำการแปลง?** Aspose.Note for Java  
- **ต้องมีลิขสิทธิ์หรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการทดสอบ; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง  
- **สามารถเปลี่ยนคุณภาพภาพได้หรือไม่?** ได้, ตั้งค่าคุณสมบัติ `quality` ใน `ImageSaveOptions`  
- **สามารถทำการแปลงเป็นชุดได้หรือไม่?** แน่นอน – วนลูปผ่านเอกสารและใช้ตัวเลือกเดียวกัน

## TIFF JPEG Compression คืออะไร?
การบีบอัด TIFF JPEG จะเก็บข้อมูลภาพไว้ในคอนเทนเนอร์ TIFF แต่ใช้ขั้นตอนการบีบอัดแบบ JPEG ที่เสียคุณภาพเพื่อทำให้ไฟล์เล็กลง เหมาะสำหรับกรณีที่ต้องการสมดุลระหว่าง **คุณภาพภาพ TIFF** และขนาดไฟล์ที่เล็กลง โดยเฉพาะสำหรับการใช้งานบนเว็บหรือการจัดเก็บระยะยาว

## ทำไมต้องใช้ประเภทการบีบอัด TIFF ที่แตกต่างกัน?
- **JPEG** – เหมาะสำหรับภาพถ่าย; มีคุณภาพที่ปรับได้  
- **PackBits** – การเข้ารหัสแบบรัน‑เลนธ์ที่ง่ายและไม่มีการสูญเสีย; เหมาะกับกราฟิกที่มีพื้นที่สีเดียวกันขนาดใหญ่  
-CCITT Group 3 Fax** – สีขาว‑ดำเท่านั้น; เหมาะสำหรับเอกสารสแกนและการส่งแฟกซ์  

การเลือกวิธีบีบอัดที่เหมาะสมจะช่วยให้คุณตอบสนองข้อจำกัดด้านพื้นที่จัดเก็บโดยไม่เสียคุณภาพภาพที่จำเป็นต่อแอปพลิเคชันของคุณ

## ข้อกำหนดเบื้องต้น

- ติดตั้ง Java Development Kit (JDK)  
- เพิ่มไลบรารี Aspose.Note for Java ลงในโปรเจกต์ของคุณ (Maven/Gradle หรือ JAR แบบแมนนวล)  
- มีความคุ้นเคยพื้นฐานกับไวยากรณ์ Java

## นำเข้าแพ็กเกจ

ก่อนอื่นให้เรียกใช้คลาส Aspose.Note ที่จำเป็นในไฟล์ Java ของคุณ:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## ขั้นตอนที่ 1: บันทึกเป็น TIFF ด้วยการบีบอัด TIFF JPEG

ด้านล่างเป็นเมธอดเต็มที่โหลดไฟล์ OneNote แล้วบันทึกเป็น TIFF ด้วยการบีบอัด JPEG ปรับค่า `quality` (0‑100) เพื่อควบคุม **คุณภาพภาพ TIFF** ตามต้องการ

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
- `setTiffCompression(TiffCompression.Jpeg)` เลือกการบีบอัดแบบ JPEG  
- `setQuality(93)` (ไม่บังคับ) ปรับคุณภาพภาพ; ค่าต่ำจะทำให้ไฟล์เล็กลง

### วิธีบันทึก TIFF ด้วยการบีบอัด JPEG ใน Java
1. ตั้งค่า `dataDir` ให้ชี้ไปยังโฟลเดอร์ที่มีไฟล์ `.one` ของคุณ  
2. เรียก `SaveToTiffUsingJpegCompression()` จากเมธอด `main` หรือเซอร์วิสของคุณ  
3. ไฟล์ `.tiff` ที่ได้จะปรากฏในโฟลเดอร์เดียวกัน

## ขั้นตอนที่ 2: บันทึกเป็น TIFF ด้วยการบีบอัด PackBits

หากต้องการตัวเลือกที่ไม่มีการสูญเสียข้อมูล PackBits เป็นอัลกอริทึมรัน‑เลนธ์ที่ง่ายและทำงานได้ดีสำหรับกราฟิกสีเดียว

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

- `setTiffCompression(TiffCompression.PackBits)` เปลี่ยนวิธีบีบอัดเป็น PackBits  
- ไม่ต้องตั้งค่าคุณภาพเพราะ PackBits เป็นการบีบอัดแบบไม่มีการสูญเสีย

## ขั้นตอนที่ 3: บันทึกเป็น TIFF ด้วยการบีบอัด CCITT Group 3 Fax (TIFF สีขาว‑ดำ)

สำหรับเอกสารสไตล์แฟกซ์คุณมักต้องการ **TIFF สีขาว‑ดำ** CCITT Group 3 ให้การบีบอัดสูงสำหรับภาพโมโนโครม

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

- `setColorMode(ColorMode.BlackAndWhite)` บังคับให้ผลลัพธ์เป็นสีขาว‑ดำ  
- `setTiffCompression(TiffCompression.Ccitt3)` ใช้การบีบอัดที่ออกแบบมาสำหรับแฟกซ์

## ปัญหาทั่วไป & เคล็ดลับ

| ปัญหา | วิธีแก้ |
|-------|----------|
| **ไฟล์ผลลัพธ์ใหญ่กว่าที่คาด** | ลดค่าคุณภาพ JPEG หรือเปลี่ยนเป็น PackBits หากยอมรับการบีบอัดแบบไม่มีการสูญเสีย |
| **สีดูซีด** | ตรวจสอบว่าไม่ได้ตั้งค่า `ColorMode.BlackAndWhite` โดยไม่ได้ตั้งใจเมื่อต้องการสีเต็ม |
| **เกิดข้อผิดพลาด Unsupported image format** | ยืนยันว่าคุณใช้ Aspose.Note เวอร์ชันล่าสุด; รุ่นเก่าอาจไม่มี enum การบีบอัดบางตัว |
| **LicenseException ขณะรันไทม์** | ติดตั้งลิขสิทธิ์ Aspose.Note ที่ถูกต้อง (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) |

## คำถามที่พบบ่อย

**ถาม: สามารถแปลงประเภทเอกสารอื่น (เช่น PDF, DOCX) เป็น TIFF ด้วยตัวเลือกเหล่านี้ได้หรือไม่?**  
ตอบ: ได้. Aspose.Note เน้นที่ไฟล์ OneNote, แต่ไลบรารี Aspose อื่น (PDF, Words) มี `ImageSaveOptions` ที่คล้ายกันสำหรับฟอร์แมตของตน

**ถาม: การบีบอัด TIFF JPEG แตกต่างจากไฟล์ JPEG ปกติอย่างไร?**  
ตอบ: ข้อมูลภาพถูกเก็บไว้ในคอนเทนเนอร์ TIFF, รักษา metadata และรองรับหลายหน้า, ส่วนอัลกอริทึมการบีบอัดยังคงเป็น JPEG

**ถาม: สามารถประมวลผลหลายไฟล์ `.one` พร้อมกันได้หรือไม่?**  
ตอบ: แน่นอน. วนลูปผ่านโฟลเดอร์, เรียกเมธอดใดเมธอดหนึ่งต่อไฟล์, แล้วเก็บไฟล์ TIFF ที่ได้ไว้

**ถาม: สามารถควบคุม DPI/ความละเอียดของ TIFF ที่ส่งออกได้หรือไม่?**  
ตอบ: ได้. ใช้ `options.setResolution(int dpi)` ก่อนบันทึก

**ถาม: Aspose.Note รองรับการประมวลผลแบบอะซิงโครนัสหรือไม่?**  
ตอบ: API เองทำงานแบบซิงโครนัส, แต่คุณสามารถห่อการเรียกใน `CompletableFuture` หรือ thread pool ของ Java เพื่อทำงานแบบขนานได้

## สรุป

คุณมีชุดเครื่องมือ **java tiff conversion** ครบถ้วนที่ช่วยให้บันทึกเอกสาร OneNote เป็นไฟล์ TIFF ด้วยการบีบอัด JPEG, PackBits หรือ CCITT Group 3 Fax ปรับคุณภาพ, โหมดสี, และความละเอียดให้ตรงตามความต้องการ **คุณภาพภาพ TIFF** ของคุณ และสามารถนำเมธอดเหล่านี้ไปใช้ในกระบวนการแบชเพื่อเพิ่มประสิทธิภาพการทำงานสูงสุด

---

**อัปเดตล่าสุด:** 2025-12-17  
**ทดสอบกับ:** Aspose.Note for Java 23.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}