---
title: แปลงสมุดบันทึกเป็นรูปภาพใน OneNote - Aspose.Note
linktitle: แปลงสมุดบันทึกเป็นรูปภาพใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีแปลงสมุดบันทึกเป็นรูปภาพใน OneNote โดยใช้ Aspose.Note สำหรับ Java รวมฟังก์ชันนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างง่ายดาย
weight: 12
url: /th/java/onenote-notebook-operations/convert-notebook-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลงสมุดบันทึกเป็นรูปภาพใน OneNote - Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีการแปลงสมุดบันทึกเป็นรูปภาพใน OneNote โดยใช้ Aspose.Note สำหรับไลบรารี Java การแปลงสมุดบันทึกเป็นรูปภาพอาจมีประโยชน์สำหรับวัตถุประสงค์ต่างๆ เช่น การแชร์บันทึก การฝังบันทึกลงในเอกสาร หรือการรวมไว้ในงานนำเสนอ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดและติดตั้งเวอร์ชันล่าสุดได้จาก[เว็บไซต์](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Aspose.Note สำหรับไลบรารี Java: ดาวน์โหลดและรวม Aspose.Note สำหรับไลบรารี Java ในโปรเจ็กต์ของคุณ คุณสามารถขอรับห้องสมุดได้จาก[เว็บไซต์กำหนด](https://releases.aspose.com/note/java/).

## แพ็คเกจนำเข้า

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

ตอนนี้ เรามาแบ่งกระบวนการแปลงออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: โหลดเอกสารสมุดบันทึก

```java
//ระบุไดเร็กทอรีที่มีไฟล์สมุดบันทึกของคุณอยู่
String dataDir = "Your Document Directory";

// โหลดเอกสารลงใน Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

 ในขั้นตอนนี้ เราจะกำหนดเส้นทางไดเรกทอรีซึ่งมีไฟล์สมุดบันทึกอยู่ จากนั้นเราก็ใช้`Document` คลาสจากไลบรารี Aspose.Note เพื่อโหลดเอกสารสมุดบันทึกชื่อ "Sample1.one" ลงในหน่วยความจำ

## ขั้นตอนที่ 2: เริ่มต้น ImageSaveOptions

```java
// เตรียมใช้งานวัตถุ PdfSaveOptions
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

 ที่นี่เราเริ่มต้น`ImageSaveOptions` object และระบุรูปแบบที่เราต้องการบันทึกเอกสารโน้ตบุ๊ก ในกรณีนี้ เราเลือกรูปแบบ PNG

## ขั้นตอนที่ 3: บันทึกเอกสารเป็นรูปภาพ

```java
// บันทึกเอกสารเป็น PNG
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

 ตอนนี้เราใช้`save()` วิธีบันทึกเอกสารสมุดบันทึกที่โหลดเป็นไฟล์รูปภาพ เราจัดเตรียมเส้นทางของไฟล์ที่เราต้องการบันทึกภาพและส่งผ่านการกำหนดค่าเริ่มต้น`ImageSaveOptions` วัตถุ.

## ขั้นตอนที่ 4: การยืนยันการพิมพ์

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

สุดท้าย เราจะพิมพ์ข้อความยืนยันไปยังคอนโซลเพื่อระบุการแปลงสำเร็จและตำแหน่งที่บันทึกไฟล์ภาพ

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีแปลงสมุดบันทึกเป็นรูปภาพใน OneNote โดยใช้ Aspose.Note สำหรับไลบรารี Java ด้วยการทำตามขั้นตอนที่อธิบายไว้ข้างต้น คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถแปลงสมุดบันทึกเป็นรูปแบบรูปภาพอื่นนอกเหนือจาก PNG ได้หรือไม่

 A1: ใช่คุณทำได้ ไลบรารี Aspose.Note รองรับรูปแบบรูปภาพที่หลากหลาย เช่น JPEG, BMP, GIF, TIFF เป็นต้น คุณสามารถระบุรูปแบบที่ต้องการได้ใน`ImageSaveOptions` วัตถุตามนั้น

### คำถามที่ 2: Aspose.Note เข้ากันได้กับ OneNote ทุกเวอร์ชันหรือไม่

ตอบ 2: Aspose.Note ให้การสนับสนุน OneNote เวอร์ชันต่างๆ อย่างครอบคลุม เพื่อให้มั่นใจถึงความเข้ากันได้ในสภาพแวดล้อมและรูปแบบไฟล์ที่แตกต่างกัน

### คำถามที่ 3: ฉันสามารถปรับแต่งการตั้งค่าเอาต์พุตภาพระหว่างการแปลงได้หรือไม่

A3: แน่นอน. Aspose.Note มีตัวเลือกมากมายสำหรับการปรับแต่งภาพที่ส่งออก รวมถึงความละเอียด คุณภาพ ความลึกของสี และอื่นๆ คุณสามารถปรับแต่งการตั้งค่าเหล่านี้ได้ตามความต้องการของคุณ

### คำถามที่ 4: Aspose.Note รองรับการแปลงสมุดบันทึกหลายเครื่องเป็นชุดหรือไม่

A4: ได้ คุณสามารถแปลงสมุดบันทึกหลายชุดเป็นรูปภาพได้อย่างมีประสิทธิภาพโดยใช้ Aspose.Note เพียงวนซ้ำรายการไฟล์สมุดบันทึกของคุณ และใช้กระบวนการแปลงที่อธิบายไว้ในบทช่วยสอนนี้

### คำถามที่ 5: ฉันจะค้นหาแหล่งข้อมูลเพิ่มเติมและการสนับสนุนสำหรับ Aspose.Note ได้ที่ไหน

 A5: สำหรับเอกสารประกอบ ตัวอย่าง และการสนับสนุนชุมชนเพิ่มเติม โปรดไปที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) และสำรวจ[เอกสารประกอบ](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
