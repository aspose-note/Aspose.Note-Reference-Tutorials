---
title: บันทึกเป็นรูปภาพ JPEG โดยใช้รูปแบบบันทึกใน OneNote
linktitle: บันทึกเป็นรูปภาพ JPEG โดยใช้รูปแบบบันทึกใน OneNote
second_title: Aspose.Note Java API
description: เปลี่ยนเอกสาร OneNote ให้เป็นภาพ JPEG ได้อย่างง่ายดาย! บทช่วยสอน Java นี้แสดงวิธีการใช้ Aspose.Note แปลงและทำให้เป็นอัตโนมัติด้วยตัวอย่างโค้ด! #OneNote #Java #Aspose
type: docs
weight: 18
url: /th/java/onenote-document-saving/save-to-jpeg-image-using-save-format/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะเจาะลึกกระบวนการบันทึกเอกสารเป็นรูปแบบภาพ JPEG โดยใช้ Aspose.Note สำหรับ Java Aspose.Note เป็น Java API อันทรงประสิทธิภาพที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ทำให้สามารถดำเนินการต่างๆ ได้ เช่น การแปลง การจัดการ และการแตกเนื้อหา

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
2.  Aspose.Note สำหรับไลบรารี Java: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).

## แพ็คเกจนำเข้า

ขั้นแรก เรามานำเข้าแพ็คเกจที่จำเป็นสำหรับโค้ด Java ของเรากันก่อน:

```java
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## ขั้นตอนที่ 1: โหลดเอกสาร

 ขั้นตอนแรกคือการโหลดเอกสารลงใน Aspose.Note ซึ่งสามารถทำได้โดยใช้`Document` คลาสจัดทำโดย Aspose.Note

```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory";

// โหลดเอกสารลงใน Aspose.Note
Document oneFile = new Document(dataDir + "Aspose.one");
```

## ขั้นตอนที่ 2: บันทึกเป็นภาพ JPEG

 ต่อไป เราจะระบุเส้นทางของไฟล์เอาต์พุตและบันทึกเอกสารในรูปแบบภาพ JPEG โดยใช้ไฟล์`save()` วิธีการควบคู่กับ`SaveFormat.Jpeg` พารามิเตอร์.

```java
// ระบุเส้นทางไฟล์เอาต์พุต
dataDir = dataDir + "SaveToJpegImageUsingSaveFormat_out.jpg";

// บันทึกเอกสาร
oneFile.save(dataDir, SaveFormat.Jpeg);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีบันทึกเอกสารเป็นรูปภาพ JPEG โดยใช้ Aspose.Note สำหรับ Java ด้วยการทำตามขั้นตอนที่ให้ไว้ คุณสามารถแปลงไฟล์ OneNote ของคุณเป็นรูปแบบ JPEG ได้อย่างราบรื่นโดยทางโปรแกรม ช่วยให้สามารถรวมและทำงานอัตโนมัติในแอปพลิเคชัน Java ของคุณได้หลากหลาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สามารถจัดการไฟล์ OneNote ที่ซับซ้อนได้หรือไม่

ตอบ 1: ใช่ Aspose.Note ได้รับการออกแบบมาเพื่อจัดการไฟล์ OneNote ที่ซับซ้อนได้อย่างมีประสิทธิภาพ ช่วยให้มั่นใจในการแปลงและการจัดการที่แม่นยำ

### คำถามที่ 2: Aspose.Note สำหรับ Java มีเวอร์ชันทดลองใช้งานหรือไม่

 ตอบ 2: ได้ คุณสามารถขอรับ Aspose.Note สำหรับ Java เวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้อย่างไร

 A3: คุณสามารถรับการสนับสนุนสำหรับ Aspose.Note สำหรับ Java ได้โดยไปที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).

### คำถามที่ 4: ฉันสามารถซื้อใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ Java ได้หรือไม่

 A4: ได้ คุณสามารถซื้อใบอนุญาตชั่วคราวได้จาก[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

A5: คุณสามารถดูเอกสารประกอบโดยละเอียดสำหรับ Aspose.Note สำหรับ Java ได้[ที่นี่](https://reference.aspose.com/note/java/).