---
title: แปลงเพจเฉพาะเป็นรูปภาพ PNG ใน OneNote - Java
linktitle: แปลงเพจเฉพาะเป็นรูปภาพ PNG ใน OneNote - Java
second_title: Aspose.Note Java API
description: เรียนรู้การใช้ Aspose.Note สำหรับ Java การแปลงหน้า OneNote เป็น PNG ทำตามขั้นตอนง่ายๆ โหลดเอกสาร และตั้งค่าตัวเลือก ปรับปรุงแอป Java ด้วยฟังก์ชันนี้
type: docs
weight: 13
url: /th/java/onenote-document-loading/convert-page-to-png-image/
---
## การแนะนำ

ในบทช่วยสอนนี้ คุณจะได้เรียนรู้วิธีใช้ Aspose.Note สำหรับ Java เพื่อแปลงหน้าเฉพาะจากเอกสาร OneNote เป็นรูปภาพ PNG เราจะแบ่งกระบวนการออกเป็นขั้นตอนที่ปฏิบัติตามได้ง่ายเพื่อช่วยให้คุณรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนระบบของคุณแล้ว
2.  Aspose.Note สำหรับไลบรารี Java: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับไลบรารี Java จาก[เว็บไซต์](https://releases.aspose.com/note/java/).
3. เอกสาร OneNote: เตรียมเอกสาร OneNote ที่คุณต้องการแปลงหน้าใดหน้าหนึ่งเป็น PNG ให้พร้อม

## แพ็คเกจนำเข้า

ขั้นแรก คุณต้องนำเข้าแพ็คเกจที่จำเป็นไปยังไฟล์ Java ของคุณ:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

```java
// โหลดเอกสารลงใน Aspose.Note
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

 ในขั้นตอนนี้ เราโหลดเอกสาร OneNote โดยใช้ Aspose.Note's`Document` ระดับ.

## ขั้นตอนที่ 2: เริ่มต้นวัตถุ ImageSaveOptions

```java
// เริ่มต้นวัตถุ ImageSaveOptions
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

 ที่นี่เราเริ่มต้น`ImageSaveOptions` object และระบุรูปแบบการบันทึกเป็น PNG

## ขั้นตอนที่ 3: ตั้งค่าดัชนีหน้า

```java
// กำหนดดัชนีหน้า
opts.setPageIndex(0);
```

ตั้งค่าดัชนีของหน้าที่คุณต้องการแปลง โปรดทราบว่าการจัดทำดัชนีหน้าเริ่มต้นจาก 0

## ขั้นตอนที่ 4: บันทึกเอกสารเป็น PNG

```java
// บันทึกเอกสารเป็น PNG
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

สุดท้าย ให้บันทึกเอกสารโดยแปลงหน้าที่ระบุเป็นรูปภาพ PNG

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีแปลงหน้าเฉพาะจากเอกสาร OneNote เป็นรูปภาพ PNG โดยใช้ Aspose.Note สำหรับ Java เรียบร้อยแล้ว การรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณจะช่วยให้คุณจัดการเอกสาร OneNote โดยทางโปรแกรม เพิ่มประสิทธิภาพการทำงาน และขยายขีดความสามารถของซอฟต์แวร์ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถแปลงหลายหน้าเป็นภาพ PNG ในคราวเดียวโดยใช้ Aspose.Note สำหรับ Java ได้หรือไม่

A1: ได้ คุณสามารถบรรลุการแปลงเป็นชุดได้โดยการวนซ้ำหน้าต่างๆ และบันทึกทีละหน้า

### คำถามที่ 2: Aspose.Note สำหรับ Java รองรับรูปแบบรูปภาพอื่นๆ นอกเหนือจาก PNG หรือไม่

ตอบ 2: ใช่ Aspose.Note รองรับรูปแบบรูปภาพที่หลากหลาย เช่น JPEG, GIF, BMP และ TIFF

### คำถามที่ 3: Aspose.Note สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ใช่ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้จาก[เว็บไซต์](https://releases.aspose.com/).

### คำถามที่ 4: ฉันสามารถรับความช่วยเหลือทางเทคนิคได้หรือไม่ หากฉันประสบปัญหาใดๆ กับ Aspose.Note สำหรับ Java

 A4: แน่นอน คุณสามารถขอการสนับสนุนจากฟอรัมชุมชน Aspose ได้[ที่นี่](https://forum.aspose.com/c/note/28).

### คำถามที่ 5: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.Note สำหรับ Java ได้ที่ไหน

 A5: คุณสามารถซื้อใบอนุญาตได้จาก[หน้าซื้อ](https://purchase.aspose.com/buy).