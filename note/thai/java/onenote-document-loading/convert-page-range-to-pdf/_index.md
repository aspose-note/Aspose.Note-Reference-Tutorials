---
title: แปลงช่วงหน้าเฉพาะเป็น PDF ใน OneNote ด้วย Java
linktitle: แปลงช่วงหน้าเฉพาะเป็น PDF ใน OneNote ด้วย Java
second_title: Aspose.Note Java API
description: เรียนรู้วิธีแปลงช่วงหน้าเฉพาะจาก OneNote เป็น PDF ได้อย่างราบรื่นด้วย Aspose.Note สำหรับ Java รักษาการจัดรูปแบบและเค้าโครงได้อย่างง่ายดาย
weight: 11
url: /th/java/onenote-document-loading/convert-page-range-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลงช่วงหน้าเฉพาะเป็น PDF ใน OneNote ด้วย Java

## การแนะนำ

OneNote เป็นเครื่องมือที่ทรงพลังสำหรับการจัดระเบียบบันทึกย่อ แต่บางครั้งคุณอาจต้องส่งออกช่วงหน้าเฉพาะเป็น PDF เพื่อวัตถุประสงค์ในการแชร์หรือเก็บถาวร ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงช่วงหน้าที่ต้องการเป็น PDF โดยใช้ Aspose.Note สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณ
2.  Aspose.Note สำหรับ Java: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ Java จาก[ที่นี่](https://releases.aspose.com/note/java/).
3. ตัวอย่างเอกสาร OneNote: เตรียมเอกสาร OneNote ตัวอย่างที่คุณต้องการแยกช่วงหน้าเฉพาะ

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นสำหรับการใช้ Aspose หมายเหตุ:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

## ขั้นตอนที่ 1: โหลดเอกสาร OneNote

โหลดเอกสาร OneNote โดยใช้ Aspose หมายเหตุ:

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

## ขั้นตอนที่ 2: เริ่มต้นตัวเลือกการบันทึก PDF

เตรียมใช้งานวัตถุ PdfSaveOptions และระบุดัชนีหน้าและจำนวน:

```java
PdfSaveOptions opts = new PdfSaveOptions();
opts.setPageIndex(2);  // ดัชนีหน้าเริ่มต้น
opts.setPageCount(3);  // จำนวนหน้าที่จะรวม
```

## ขั้นตอนที่ 3: บันทึกเป็น PDF

บันทึกช่วงหน้าที่ระบุเป็นไฟล์ PDF:

```java
oneFile.save(dataDir + "ConvertSpecificPageRangeToPdf_out.pdf", opts);
System.out.println("File saved: " + dataDir + "ConvertSpecificPageRangeToPdf_out.pdf");
```

ยินดีด้วย! คุณได้แปลงช่วงหน้าเฉพาะจากเอกสาร OneNote เป็น PDF โดยใช้ Aspose.Note สำหรับ Java สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีแปลงช่วงหน้าเฉพาะจากเอกสาร OneNote เป็น PDF โดยใช้ Aspose.Note สำหรับ Java ฟังก์ชันนี้มีประโยชน์สำหรับวัตถุประสงค์ต่างๆ เช่น การแชร์ข้อมูลที่เลือกสรร หรือการสร้างสำเนาเอกสารสำคัญ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถระบุช่วงหน้าที่ไม่ต่อเนื่องกันหลายช่วงสำหรับการแปลงได้หรือไม่

คำตอบ 1: ขออภัย ปัจจุบัน Aspose.Note สำหรับ Java รองรับการแปลงเฉพาะช่วงหน้าที่ต่อเนื่องกันเป็น PDF

### คำถามที่ 2: Aspose.Note สำหรับ Java รักษาการจัดรูปแบบของเอกสาร OneNote ต้นฉบับหรือไม่

A2: ใช่ Aspose.Note ตรวจสอบให้แน่ใจว่าการจัดรูปแบบและเค้าโครงของเอกสาร OneNote ต้นฉบับจะยังคงอยู่ใน PDF ที่สร้างขึ้น

### คำถามที่ 3: เป็นไปได้หรือไม่ที่จะแปลงเอกสาร OneNote ที่มีการป้องกันด้วยรหัสผ่านเป็น PDF

A3: Aspose.Note สำหรับ Java ไม่รองรับการแปลงเอกสาร OneNote ที่มีการป้องกันด้วยรหัสผ่านโดยตรง คุณต้องลบการป้องกันด้วยรหัสผ่านก่อนการแปลง

### คำถามที่ 4: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของไฟล์ PDF ที่สร้างขึ้นได้หรือไม่

A4: ได้ คุณสามารถปรับแต่งลักษณะต่างๆ เช่น ขนาดหน้า การวางแนว และการตั้งค่าส่วนหัว/ส่วนท้ายได้โดยใช้ตัวเลือกการบันทึก PDF ของ Aspose.Note

### คำถามที่ 5: Aspose.Note สำหรับ Java รองรับการแปลงเอกสาร OneNote หลายชุดเป็นชุดหรือไม่

A5: ได้ คุณสามารถแปลงเอกสาร OneNote หลายชุดเป็น PDF เป็นกลุ่มได้โดยการวนซ้ำแต่ละเอกสารและใช้กระบวนการแปลง
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
