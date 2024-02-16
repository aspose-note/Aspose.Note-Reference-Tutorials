---
title: แนบไฟล์ตามเส้นทางใน Aspose.Note
linktitle: แนบไฟล์ตามเส้นทางใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีแนบไฟล์ลงในเอกสาร Microsoft OneNote โดยใช้โปรแกรม Aspose.Note สำหรับ .NET ลดความซับซ้อนของกระบวนการพัฒนาของคุณด้วยบทช่วยสอนที่ครอบคลุมนี้
type: docs
weight: 11
url: /th/net/attachments/attach-file-by-path/
---
## การแนะนำ

Aspose.Note for .NET เป็นไลบรารีที่มีประสิทธิภาพซึ่งช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ไม่ว่าคุณจะต้องการสร้าง แก้ไข แปลง หรือจัดการเอกสาร OneNote Aspose.Note สำหรับ .NET ก็มีฟังก์ชันการทำงานที่ครอบคลุมเพื่อปรับปรุงกระบวนการพัฒนาของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเริ่มใช้ Aspose.Note สำหรับ .NET ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. สภาพแวดล้อมการพัฒนา: คุณต้องมีคอมพิวเตอร์ที่ติดตั้ง .NET Framework และมีสภาพแวดล้อมการพัฒนาที่เหมาะสม เช่น Visual Studio

2.  Aspose.Note สำหรับ .NET: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ .NET จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/note/net/).

3. ความรู้เกี่ยวกับ C#: ทำความคุ้นเคยกับภาษาการเขียนโปรแกรม C# เนื่องจาก Aspose.Note สำหรับ .NET จะใช้กับ C# เป็นหลัก

4. ความเข้าใจพื้นฐานของ OneNote: แม้ว่าจะไม่บังคับ แต่การมีความเข้าใจพื้นฐานเกี่ยวกับโครงสร้างและแนวคิดของ OneNote จะเป็นประโยชน์

## นำเข้าเนมสเปซ

หากต้องการใช้ Aspose.Note สำหรับ .NET ในโปรเจ็กต์ของคุณ คุณต้องนำเข้าเนมสเปซที่จำเป็น ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## แนบไฟล์ตามเส้นทางใน Aspose.Note

การแนบไฟล์เข้ากับเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ .NET เป็นกระบวนการที่ไม่ซับซ้อน ลองแบ่งมันออกเป็นหลายขั้นตอน:

### ขั้นตอนที่ 1: เริ่มต้นวัตถุเอกสาร

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = RunExamples.GetDataDir_Attachments();
Document doc = new Document();
```

 สิ่งนี้จะเริ่มต้นอินสแตนซ์ใหม่ของ`Document` คลาสซึ่งแสดงถึงเอกสาร OneNote

### ขั้นตอนที่ 2: เริ่มต้นวัตถุหน้า

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

 ที่นี่เราสร้างอินสแตนซ์ใหม่ของ`Page` คลาสซึ่งแสดงถึงหน้าภายในเอกสาร

### ขั้นตอนที่ 3: เริ่มต้นวัตถุเค้าร่าง

```csharp
Outline outline = new Outline(doc);
```

 หนึ่ง`Outline` วัตถุถูกสร้างขึ้นเพื่อจัดระเบียบเนื้อหาภายในหน้า

### ขั้นตอนที่ 4: เริ่มต้นวัตถุ OutlineElement

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

`OutlineElement` แสดงถึงองค์ประกอบภายในโครงสร้างเค้าร่าง

### ขั้นตอนที่ 5: เริ่มต้นวัตถุ AttachedFile

```csharp
AttachedFile attachedFile = new AttachedFile(doc,  dataDir + "attachment.txt");
```

 ที่นี่เราสร้างอินสแตนซ์ของ`AttachedFile`โดยระบุเส้นทางไปยังไฟล์ที่เราต้องการแนบ

### ขั้นตอนที่ 6: ผนวกไฟล์ที่แนบมา

```csharp
outlineElem.AppendChildLast(attachedFile);
```

ไฟล์ที่แนบมาจะถูกผนวกเข้ากับองค์ประกอบเค้าร่าง

### ขั้นตอนที่ 7: ผนวกองค์ประกอบโครงร่าง

```csharp
outline.AppendChildLast(outlineElem);
```

องค์ประกอบเค้าร่างจะถูกผนวกเข้ากับโครงร่าง

### ขั้นตอนที่ 8: ผนวกโครงร่าง

```csharp
page.AppendChildLast(outline);
```

โครงร่างจะถูกผนวกเข้ากับหน้า

### ขั้นตอนที่ 9: ผนวกหน้า

```csharp
doc.AppendChildLast(page);
```

ในที่สุด หน้าดังกล่าวจะถูกผนวกเข้ากับเอกสาร

### ขั้นตอนที่ 10: บันทึกเอกสาร

```csharp
dataDir = dataDir + "AttachFileByPath_out.one";
doc.Save(dataDir);
```

บันทึกเอกสารและแนบไฟล์เรียบร้อยแล้ว

## บทสรุป

Aspose.Note สำหรับ .NET ช่วยให้กระบวนการทำงานกับเอกสาร OneNote โดยทางโปรแกรมง่ายขึ้น ด้วยการทำตามขั้นตอนที่อธิบายไว้ข้างต้น คุณสามารถแนบไฟล์เข้ากับเอกสาร OneNote ของคุณได้อย่างราบรื่นโดยใช้ Aspose.Note for .NET

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สำหรับ .NET เข้ากันได้กับ OneNote ทุกเวอร์ชันหรือไม่

A1: Aspose.Note สำหรับ .NET รองรับ OneNote เวอร์ชันต่างๆ รวมถึง OneNote 2010, 2013, 2016 และ OneNote ล่าสุดสำหรับ Windows 10

### คำถามที่ 2: ฉันสามารถจัดการไฟล์ OneNote ที่มีอยู่โดยใช้ Aspose.Note for .NET ได้หรือไม่

ตอบ 2: ได้ คุณสามารถแก้ไข ปรับเปลี่ยน และจัดการไฟล์ OneNote ที่มีอยู่โดยทางโปรแกรมโดยใช้ Aspose.Note สำหรับ .NET

### คำถามที่ 3: Aspose.Note สำหรับ .NET จำเป็นต้องมีใบอนุญาตสำหรับการใช้งานเชิงพาณิชย์หรือไม่

A3: ใช่ คุณต้องได้รับใบอนุญาตสำหรับการใช้งานเชิงพาณิชย์ของ Aspose.Note สำหรับ .NET คุณสามารถขอรับใบอนุญาตได้จาก[หน้าซื้อ](https://purchase.aspose.com/buy).

### คำถามที่ 4: Aspose.Note สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถทดลองใช้ Aspose.Note สำหรับ .NET ได้ฟรีจาก[หน้าทดลอง](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.Note สำหรับ .NET ได้ที่ไหน

 A5: คุณสามารถขอการสนับสนุนจากฟอรั่มชุมชน Aspose.Note[ที่นี่](https://forum.aspose.com/c/note/28).