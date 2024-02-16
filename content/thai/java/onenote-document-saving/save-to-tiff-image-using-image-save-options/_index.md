---
title: บันทึกเป็น TIFF Image โดยใช้ตัวเลือกการบันทึกรูปภาพใน OneNote
linktitle: บันทึกเป็น TIFF Image โดยใช้ตัวเลือกการบันทึกรูปภาพใน OneNote
second_title: Aspose.Note Java API
description: แปลงเอกสาร OneNote เป็น TIFF และควบคุมขนาดและคุณภาพไฟล์! เลือกการบีบอัด JPEG, PackBits หรือแฟกซ์ใน Java รับตัวอย่างโค้ดและเรียนรู้วิธีการ! #OneNote #Java #Aspose
type: docs
weight: 21
url: /th/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---
## การแนะนำ

ในบทช่วยสอนนี้ คุณจะได้เรียนรู้วิธีบันทึกเอกสารเป็นรูปแบบภาพ TIFF โดยใช้วิธีการบีบอัดแบบต่างๆ ใน Aspose.Note สำหรับ Java เราจะครอบคลุมข้อกำหนดเบื้องต้น การนำเข้าแพ็คเกจ และให้คำแนะนำทีละขั้นตอนสำหรับวิธีการบีบอัดแต่ละวิธี

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
- Aspose.Note สำหรับไลบรารี Java ที่ดาวน์โหลดและกำหนดค่า
- ความเข้าใจพื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม Java

## แพ็คเกจนำเข้า

ขั้นแรก คุณต้องนำเข้าแพ็คเกจที่จำเป็นไปยังไฟล์ Java ของคุณ:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## ขั้นตอนที่ 1: บันทึกเป็น TIFF โดยใช้การบีบอัด JPEG

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    String dataDir = "Your Document Directory";

    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  โหลดเอกสารโดยใช้`Document` ระดับ.
-  สร้างอินสแตนซ์ของ`ImageSaveOptions` และระบุประเภทการบีบอัด TIFF เป็น JPEG
- ตั้งค่าคุณภาพที่ต้องการ (ไม่บังคับ)
- บันทึกเอกสารเป็นรูปแบบ TIFF โดยใช้ตัวเลือกที่ระบุ

## ขั้นตอนที่ 2: บันทึกเป็น TIFF โดยใช้การบีบอัด PackBits

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    String dataDir = "Your Document Directory";

    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  โหลดเอกสารโดยใช้`Document` ระดับ.
-  สร้างอินสแตนซ์ของ`ImageSaveOptions` และระบุประเภทการบีบอัด TIFF เป็น PackBits
- บันทึกเอกสารเป็นรูปแบบ TIFF โดยใช้ตัวเลือกที่ระบุ

## ขั้นตอนที่ 3: บันทึกเป็น TIFF โดยใช้การบีบอัดแฟกซ์ CCITT Group 3

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    String dataDir = "Your Document Directory";

    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  โหลดเอกสารโดยใช้`Document` ระดับ.
-  สร้างอินสแตนซ์ของ`ImageSaveOptions` และระบุประเภทการบีบอัด TIFF เป็น CCITT Group 3 Fax
- ตั้งค่าโหมดสีเป็นขาวดำ
- บันทึกเอกสารเป็นรูปแบบ TIFF โดยใช้ตัวเลือกที่ระบุ

## บทสรุป

ในบทช่วยสอนนี้ คุณได้เรียนรู้วิธีบันทึกเอกสารเป็นรูปแบบ TIFF โดยใช้วิธีการบีบอัดแบบต่างๆ ใน Aspose.Note สำหรับ Java ด้วยการทำตามคำแนะนำทีละขั้นตอน คุณจะสามารถใช้ความสามารถของ Aspose.Note ได้อย่างมีประสิทธิภาพเพื่อตอบสนองความต้องการของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.Note สำหรับ Java เพื่อแปลงรูปแบบเอกสารอื่นเป็น TIFF ได้หรือไม่

ตอบ 1: ใช่ Aspose.Note สำหรับ Java รองรับการแปลงจากรูปแบบเอกสารต่างๆ เป็น TIFF รวมถึงเอกสาร OneNote

### คำถามที่ 2: การระบุประเภทการบีบอัดเมื่อบันทึกเป็น TIFF มีความสำคัญอย่างไร

A2: การระบุประเภทการบีบอัดจะทำให้คุณสามารถควบคุมคุณภาพของภาพและขนาดไฟล์ได้ วิธีการบีบอัดที่แตกต่างกันทำให้เกิดการแลกเปลี่ยนระหว่างคุณภาพและอัตราส่วนการบีบอัด

### คำถามที่ 3: Aspose.Note สำหรับ Java เหมาะสำหรับการประมวลผลเอกสารเป็นชุดหรือไม่

ตอบ 3: ใช่ Aspose.Note สำหรับ Java มี API สำหรับการประมวลผลเป็นชุด ช่วยให้คุณสามารถทำงานการแปลงเอกสารอัตโนมัติได้อย่างมีประสิทธิภาพ

### คำถามที่ 4: ฉันสามารถปรับแต่งการตั้งค่าการบีบอัดเพิ่มเติมได้หรือไม่

A4: ได้ คุณสามารถปรับพารามิเตอร์ต่างๆ เช่น คุณภาพ ความละเอียด และวิธีการบีบอัด เพื่อปรับแต่งผลลัพธ์ตามความต้องการของคุณได้

### คำถามที่ 5: Aspose.Note สำหรับ Java มีการสนับสนุนทางเทคนิคหรือไม่

A5: ใช่ Aspose ให้การสนับสนุนด้านเทคนิคอย่างครอบคลุมผ่านทางฟอรัมและระบบตามตั๋ว