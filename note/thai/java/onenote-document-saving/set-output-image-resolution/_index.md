---
title: ตั้งค่าความละเอียดของรูปภาพเอาต์พุตใน OneNote - Aspose.Note
linktitle: ตั้งค่าความละเอียดของรูปภาพเอาต์พุตใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีปรับความละเอียดของรูปภาพในเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการนำไปปฏิบัติที่ง่ายดาย
weight: 23
url: /th/java/onenote-document-saving/set-output-image-resolution/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าความละเอียดของรูปภาพเอาต์พุตใน OneNote - Aspose.Note

## การแนะนำ

คุณต้องการจัดการความละเอียดของรูปภาพภายในเอกสาร OneNote ของคุณโดยใช้ Java หรือไม่? Aspose.Note สำหรับ Java นำเสนอโซลูชันที่มีประสิทธิภาพสำหรับงานดังกล่าว ในบทช่วยสอนนี้ เราจะอธิบายขั้นตอนต่างๆ เพื่อตั้งค่าความละเอียดของภาพที่ส่งออกโดยใช้ Aspose.Note

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1. Java Development Kit (JDK): ติดตั้ง JDK บนระบบของคุณ
2. Aspose.Note สำหรับ Java: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ Java จาก[เว็บไซต์](https://releases.aspose.com/note/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): เลือก IDE ที่คุณต้องการ เช่น Eclipse หรือ IntelliJ IDEA

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจ Aspose.Note ที่จำเป็น:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

เริ่มต้นด้วยการโหลดเอกสาร OneNote ลงในแอปพลิเคชัน Java ของคุณ:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 แทนที่`"Your Document Directory"` ด้วยไดเรกทอรีจริงที่มีเอกสาร OneNote ของคุณอยู่

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการบันทึกรูปภาพ

กำหนดตัวเลือกการบันทึกรูปภาพและระบุความละเอียดที่ต้องการ:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 ที่นี่เรากำลังตั้งค่าความละเอียดเป็น`120 dpi`. คุณสามารถปรับค่านี้ได้ตามความต้องการของคุณ

## ขั้นตอนที่ 3: บันทึกเอกสารด้วยการแก้ไขความละเอียด

บันทึกเอกสารด้วยความละเอียดของภาพที่อัปเดต:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

สิ่งนี้จะบันทึกเอกสารที่แก้ไขด้วยความละเอียดที่ระบุ

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจวิธีตั้งค่าความละเอียดของรูปภาพเอาต์พุตในเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ Java ด้วยการทำตามขั้นตอนง่ายๆ เหล่านี้ คุณสามารถจัดการความละเอียดของภาพให้ตรงกับความต้องการของแอปพลิเคชันของคุณได้อย่างมีประสิทธิภาพ


## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับความละเอียดของภาพเป็นค่าที่สูงกว่า 120 dpi ได้หรือไม่

A1: ได้ คุณสามารถตั้งค่าความละเอียดเป็นค่าที่ต้องการได้ตามความต้องการของคุณ

### คำถามที่ 2: Aspose.Note รองรับรูปแบบรูปภาพอื่นนอกเหนือจาก JPEG หรือไม่

ตอบ 2: ใช่ Aspose.Note รองรับรูปแบบรูปภาพที่หลากหลาย เช่น PNG, BMP, GIF เป็นต้น

### คำถามที่ 3: Aspose.Note เข้ากันได้กับ Java ทุกเวอร์ชันหรือไม่

A3: Aspose.Note เข้ากันได้กับ Java 1.6 หรือเวอร์ชันที่ใหม่กว่า

### คำถามที่ 4: ฉันสามารถจัดการลักษณะอื่นๆ ของรูปภาพในเอกสาร OneNote โดยใช้ Aspose.Note ได้หรือไม่

A4: ใช่ Aspose.Note มีคุณสมบัติที่ครอบคลุมสำหรับการจัดการรูปภาพ รวมถึงการปรับขนาด การครอบตัด และการหมุน

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับการสอบถามที่เกี่ยวข้องกับ Aspose.Note ได้ที่ไหน

 A5: คุณสามารถขอความช่วยเหลือได้จากฟอรัมชุมชน Aspose.Note[ที่นี่](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
