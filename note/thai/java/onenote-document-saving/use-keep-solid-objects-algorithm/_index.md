---
title: ใช้อัลกอริทึม Keep Solid Objects ใน OneNote - Aspose.Note
linktitle: ใช้อัลกอริทึม Keep Solid Objects ใน OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: เรียนรู้วิธีรักษาวัตถุทึบในเอกสาร Aspose.Note ของคุณเมื่อแปลงเป็น PDF โดยใช้อัลกอริทึม Keep Solid Objects ใน Java
type: docs
weight: 25
url: /th/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีใช้อัลกอริทึม Keep Solid Objects ใน Aspose.Note สำหรับ Java อัลกอริธึมนี้มีคุณค่าอย่างยิ่งในการรักษาความสมบูรณ์ของออบเจ็กต์ทึบภายในเอกสารของคุณเมื่อแปลงเป็นรูปแบบ PDF เราจะแจกแจงกระบวนการทีละขั้นตอนเพื่อให้มั่นใจถึงความชัดเจนและความเข้าใจในแต่ละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
2.  Aspose.Note สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/java/).

## แพ็คเกจนำเข้า

ขั้นแรก เรามานำเข้าแพ็คเกจที่จำเป็นกันก่อน:

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## ขั้นตอนที่ 1: โหลดเอกสาร

โหลดเอกสารลงใน Aspose.Note โดยใช้ข้อมูลโค้ดต่อไปนี้:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการบันทึก PDF

กำหนด PdfSaveOptions และตั้งค่า PageSplittingAlgorithm เป็น KeepSolidObjectsAlgorithm:

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## ขั้นตอนที่ 3: ปรับขีดจำกัดความสูง (ไม่บังคับ)

คุณสามารถปรับขีดจำกัดความสูงของชิ้นส่วนที่โคลนได้หากจำเป็น:

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## ขั้นตอนที่ 4: บันทึกเอกสาร

สุดท้าย ให้บันทึกเอกสารด้วยตัวเลือกการบันทึก PDF ที่ระบุ:

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีใช้อัลกอริทึม Keep Solid Objects ใน Aspose.Note สำหรับ Java อัลกอริธึมนี้ช่วยให้แน่ใจว่าวัตถุทึบภายในเอกสารของคุณจะถูกเก็บรักษาไว้เมื่อแปลงเป็นรูปแบบ PDF โดยรักษาความสมบูรณ์ของเอกสาร

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับขีดจำกัดความสูงของชิ้นส่วนที่โคลนได้หรือไม่

 A1: ได้ คุณสามารถปรับขีดจำกัดความสูงของชิ้นส่วนที่โคลนได้ตามความต้องการของคุณโดยใช้`heightLimitOfClonedPart` พารามิเตอร์.

### Q2: ฉันจะหาเอกสารเพิ่มเติมได้จากที่ไหน?

 A2: คุณสามารถดูเอกสารโดยละเอียดได้ที่ Aspose.Note สำหรับ Java[ที่นี่](https://reference.aspose.com/note/java/).

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 ตอบ 3: ได้ คุณสามารถทดลองใช้ Aspose.Note สำหรับ Java ได้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะได้รับความช่วยเหลือได้อย่างไรหากฉันประสบปัญหาใดๆ

 A4: คุณสามารถรับการสนับสนุนจากชุมชน Aspose[ที่นี่](https://forum.aspose.com/c/note/28).

### คำถามที่ 5: ฉันจะซื้อใบอนุญาตได้ที่ไหน

 A5: คุณสามารถซื้อใบอนุญาตสำหรับ Aspose.Note สำหรับ Java ได้[ที่นี่](https://purchase.aspose.com/buy).
