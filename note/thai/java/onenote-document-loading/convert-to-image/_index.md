---
title: แปลงเอกสาร OneNote เป็นรูปภาพ - Java
linktitle: แปลงเอกสาร OneNote เป็นรูปภาพ - Java
second_title: Aspose.Note Java API
description: เรียนรู้วิธีการแปลง OneNote เป็นรูปภาพโดยใช้ Aspose.Note สำหรับ Java ทำตามขั้นตอนง่ายๆ โหลดเอกสาร เริ่มต้นตัวเลือก และบันทึกเป็น PNG
weight: 14
url: /th/java/onenote-document-loading/convert-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลงเอกสาร OneNote เป็นรูปภาพ - Java

## การแนะนำ

ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการใช้ Aspose.Note สำหรับ Java เพื่อแปลงเอกสาร OneNote ให้เป็นรูปภาพ เราจะแบ่งแต่ละขั้นตอนออกเป็นคำแนะนำที่ง่ายต่อการปฏิบัติตาม

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
2.  Aspose.Note สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).

## แพ็คเกจนำเข้า

ขั้นแรก นำเข้าแพ็คเกจที่จำเป็นในโค้ด Java ของคุณ:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

ตอนนี้เรามาแบ่งโค้ดตัวอย่างออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

กำหนดไดเรกทอรีที่มีเอกสาร OneNote ของคุณ:

```java
String dataDir = "Your Document Directory";
```

 แทนที่`"Your Document Directory"` พร้อมเส้นทางไปยังเอกสาร OneNote ของคุณ

## ขั้นตอนที่ 2: โหลดเอกสาร

โหลดเอกสาร OneNote ลงใน Aspose หมายเหตุ:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 ทำให้มั่นใจ`"Sample1.one"` ตรงกับชื่อไฟล์เอกสาร OneNote ของคุณ

## ขั้นตอนที่ 3: เริ่มต้น ImageSaveOptions

 เริ่มต้น`ImageSaveOptions` วัตถุเพื่อระบุรูปแบบการบันทึก:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

ที่นี่ เรากำลังบันทึกเอกสารเป็นรูปภาพ PNG คุณสามารถเลือกรูปแบบอื่นๆ เช่น JPEG หรือ BMP ได้หากต้องการ

## ขั้นตอนที่ 4: บันทึกเอกสารเป็นรูปภาพ

บันทึกเอกสารที่โหลดเป็นรูปภาพ:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

บรรทัดนี้จะบันทึกเอกสารเป็นรูปภาพ PNG พร้อมตัวเลือกที่ระบุ

## ขั้นตอนที่ 5: การยืนยันการพิมพ์

พิมพ์ข้อความเพื่อยืนยันว่าไฟล์ได้รับการบันทึกแล้ว:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

บรรทัดนี้จะแจ้งให้คุณทราบเกี่ยวกับการแปลงสำเร็จและตำแหน่งของไฟล์รูปภาพที่บันทึกไว้

## บทสรุป

ด้วยการทำตามขั้นตอนที่อธิบายไว้ข้างต้น คุณสามารถแปลงเอกสาร OneNote เป็นรูปภาพได้อย่างง่ายดายโดยใช้ Aspose.Note for Java เป็นวิธีที่ง่ายและมีประสิทธิภาพในการจัดการการแปลงเอกสารในแอปพลิเคชัน Java ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถแปลงเอกสาร OneNote หลายฉบับในคราวเดียวได้หรือไม่

A1: ได้ คุณสามารถวนซ้ำรายการเอกสารและดำเนินการแปลงสำหรับแต่ละเอกสารได้

### คำถามที่ 2: Aspose.Note รองรับรูปแบบเอาต์พุตอื่นๆ นอกเหนือจากรูปภาพหรือไม่

ตอบ 2: ใช่ Aspose.Note รองรับรูปแบบเอาต์พุตที่หลากหลาย เช่น รูปแบบ PDF, HTML และ Microsoft Word

### คำถามที่ 3: Aspose.Note เข้ากันได้กับไฟล์ OneNote ทุกเวอร์ชันหรือไม่

A3: Aspose.Note มีความเข้ากันได้กับไฟล์ OneNote ที่สร้างใน Microsoft OneNote เวอร์ชันต่างๆ

### คำถามที่ 4: ฉันสามารถปรับแต่งความละเอียดของภาพที่ส่งออกได้หรือไม่

A4: ได้ คุณสามารถปรับความละเอียดและพารามิเตอร์อื่นๆ ได้โดยใช้ตัวเลือกที่มีอยู่ใน Aspose.Note

### คำถามที่ 5: Aspose.Note ต้องใช้การเชื่อมต่ออินเทอร์เน็ตสำหรับการแปลงเอกสารหรือไม่

A5: ไม่ Aspose.Note ทำงานภายในเครื่องโดยไม่จำเป็นต้องเชื่อมต่ออินเทอร์เน็ต
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
