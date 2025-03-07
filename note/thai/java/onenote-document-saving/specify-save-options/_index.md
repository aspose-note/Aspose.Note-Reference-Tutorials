---
title: ระบุตัวเลือกการบันทึกใน OneNote - Aspose.Note
linktitle: ระบุตัวเลือกการบันทึกใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีระบุตัวเลือกการบันทึกใน OneNote โดยใช้ Aspose.Note for Java ปรับแต่งการตั้งค่าดัชนีหน้า จำนวน และการบีบอัดได้อย่างง่ายดาย
weight: 24
url: /th/java/onenote-document-saving/specify-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ระบุตัวเลือกการบันทึกใน OneNote - Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะเรียนรู้วิธีระบุตัวเลือกการบันทึกใน OneNote โดยใช้ Aspose.Note for Java Aspose.Note เป็นไลบรารี Java ที่ทรงพลังซึ่งช่วยให้นักพัฒนาสามารถสร้าง จัดการ และแปลงเอกสาร OneNote โดยทางโปรแกรม ด้วย Aspose.Note คุณสามารถควบคุมตัวเลือกการบันทึกต่างๆ ได้อย่างง่ายดายเพื่อปรับแต่งเอาต์พุตตามความต้องการของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. ความรู้พื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม Java
2. ติดตั้ง JDK (Java Development Kit) บนระบบของคุณ
3.  Aspose.Note สำหรับไลบรารี Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นในโค้ด Java ของคุณ:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

มาแบ่งตัวอย่างออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory";

// โหลดเอกสารลงใน Aspose.Note
Document doc = new Document(dataDir + "Aspose.one");
```

 ในขั้นตอนนี้ เราระบุเส้นทางไปยังเอกสาร OneNote และโหลดลงใน`Document` วัตถุ.

## ขั้นตอนที่ 2: เริ่มต้นวัตถุ PdfSaveOptions

```java
// เตรียมใช้งานวัตถุ PdfSaveOptions
PdfSaveOptions opts = new PdfSaveOptions();
```

 ที่นี่เราเริ่มต้น a`PdfSaveOptions` วัตถุที่จะใช้ระบุตัวเลือกในการบันทึกเอกสารเป็น PDF

## ขั้นตอนที่ 3: ตั้งค่าดัชนีหน้าและจำนวน

```java
// ตั้งค่าดัชนีหน้า
opts.setPageIndex(2);

// กำหนดจำนวนหน้า
opts.setPageCount(3);
```

บรรทัดเหล่านี้จะตั้งค่าดัชนีและจำนวนหน้าที่จะบันทึก ในตัวอย่างนี้ เรากำลังบันทึกหน้าเว็บโดยเริ่มจากดัชนี 2 และทั้งหมด 3 หน้า

## ขั้นตอนที่ 4: ระบุการตั้งค่าการบีบอัด

```java
// ระบุการบีบอัดหากจำเป็น
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

ที่นี่ เราระบุการตั้งค่าการบีบอัดรูปภาพสำหรับ PDF เราตั้งค่าการบีบอัดเป็นรูปแบบ JPEG และระบุคุณภาพ JPEG เป็น 90%

## ขั้นตอนที่ 5: บันทึกเอกสารพร้อมตัวเลือก

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

สุดท้ายเราบันทึกเอกสารด้วยตัวเลือกที่ระบุ ผลลัพธ์ PDF จะถูกบันทึกในตำแหน่งที่ระบุพร้อมตัวเลือกที่กำหนด

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีระบุตัวเลือกการบันทึกใน OneNote โดยใช้ Aspose.Note for Java ด้วยการปรับแต่งตัวเลือกการบันทึก คุณสามารถควบคุมลักษณะต่างๆ ของเอกสารเอาต์พุต เช่น ดัชนีหน้า จำนวน และการตั้งค่าการบีบอัด

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สามารถจัดการเอกสาร OneNote ขนาดใหญ่ได้หรือไม่

A1: ใช่ Aspose.Note ได้รับการออกแบบมาเพื่อจัดการเอกสาร OneNote ขนาดใหญ่อย่างมีประสิทธิภาพ

### คำถามที่ 2: Aspose.Note เข้ากันได้กับ Java เวอร์ชันล่าสุดหรือไม่

ตอบ 2: ใช่ Aspose.Note เข้ากันได้กับ Java เวอร์ชันล่าสุด

### คำถามที่ 3: ฉันสามารถแปลงเอกสาร OneNote เป็นรูปแบบอื่นโดยใช้ Aspose.Note ได้หรือไม่

A3: ใช่ Aspose.Note รองรับการแปลงเอกสาร OneNote เป็นรูปแบบต่างๆ เช่น PDF, DOCX และ HTML

### คำถามที่ 4: Aspose.Note ให้การสนับสนุนการเข้ารหัสและการถอดรหัสเอกสาร OneNote หรือไม่

ตอบ 4: ใช่ Aspose.Note มี API สำหรับการเข้ารหัสและถอดรหัสเอกสาร OneNote

### คำถามที่ 5: Aspose.Note เหมาะสำหรับการใช้งานเชิงพาณิชย์หรือไม่

A5: ได้ Aspose.Note สามารถใช้เพื่อวัตถุประสงค์ทางการค้าได้โดยการซื้อใบอนุญาต
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
