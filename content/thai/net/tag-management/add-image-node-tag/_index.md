---
title: เพิ่มโหนดรูปภาพพร้อมแท็กใน Aspose.Note
linktitle: เพิ่มโหนดรูปภาพพร้อมแท็กใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีปรับปรุงเอกสาร OneNote ของคุณโดยการเพิ่มรูปภาพด้วยแท็กแบบกำหนดเองโดยใช้ Aspose.Note สำหรับ .NET
type: docs
weight: 10
url: /th/net/tag-management/add-image-node-tag/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีเพิ่มโหนดรูปภาพด้วยแท็กโดยใช้ Aspose.Note สำหรับ .NET คุณลักษณะนี้ช่วยให้คุณสามารถปรับปรุงเอกสาร OneNote ของคุณโดยการเพิ่มรูปภาพด้วยแท็กที่กำหนดเอง

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. Visual Studio: ติดตั้ง Visual Studio IDE บนระบบของคุณ
2.  Aspose.Note สำหรับ .NET: ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note สำหรับ .NET จากไฟล์[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/note/net/).
3. ความรู้พื้นฐาน: ทำความคุ้นเคยกับภาษาการเขียนโปรแกรม C# และกรอบงาน .NET

## นำเข้าเนมสเปซ

ขั้นแรก ตรวจสอบให้แน่ใจว่าได้รวมเนมสเปซที่จำเป็นในโค้ด C# ของคุณ:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## ขั้นตอนที่ 1: เริ่มต้นเอกสารและวัตถุหน้า

 เริ่มต้นด้วยการสร้างอินสแตนซ์ของ`Document` คลาสและก`Page` วัตถุ:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## ขั้นตอนที่ 2: เริ่มต้นออบเจ็กต์ Outline และ OutlineElement

 ถัดไปเริ่มต้น`Outline` และ`OutlineElement` วัตถุ:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## ขั้นตอนที่ 3: โหลดและแทรกรูปภาพ

โหลดรูปภาพที่ต้องการและแทรกลงในโหนดเอกสาร:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## ขั้นตอนที่ 4: เพิ่มแท็กให้กับรูปภาพ

เพิ่มแท็กที่กำหนดเองให้กับรูปภาพ:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## ขั้นตอนที่ 5: ผนวกองค์ประกอบโครงร่างและโหนดหน้า

ผนวกองค์ประกอบเค้าร่างและโหนดเค้าร่างเข้ากับหน้า:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## ขั้นตอนที่ 6: บันทึกเอกสาร

บันทึกเอกสาร OneNote ที่แก้ไขแล้ว:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## บทสรุป

ด้วยการทำตามขั้นตอนเหล่านี้ คุณจะสามารถเพิ่มโหนดรูปภาพด้วยแท็กแบบกำหนดเองได้อย่างราบรื่นโดยใช้ Aspose.Note สำหรับ .NET ซึ่งจะทำให้เอกสาร OneNote ของคุณสมบูรณ์แบบด้วยภาพส่วนบุคคล

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถเพิ่มรูปภาพหลายรูปด้วยแท็กที่แตกต่างกันในเอกสารเดียวโดยใช้ Aspose.Note ได้หรือไม่

ตอบ 1: ได้ คุณสามารถเพิ่มรูปภาพหลายรูปโดยใช้แท็กที่แตกต่างกันได้โดยทำตามขั้นตอนที่คล้ายกันสำหรับแต่ละรูปภาพ

### คำถามที่ 2: Aspose.Note เข้ากันได้กับ OneNote ทุกเวอร์ชันหรือไม่

ตอบ 2: Aspose.Note รองรับ OneNote เวอร์ชันต่างๆ เพื่อให้มั่นใจถึงความเข้ากันได้ในสภาพแวดล้อมที่แตกต่างกัน

### คำถามที่ 3: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของแท็กที่เพิ่มลงในรูปภาพได้หรือไม่

A3: ใช่ Aspose.Note ให้ความยืดหยุ่นในการปรับแต่งลักษณะแท็กให้เหมาะกับความต้องการของคุณ

### คำถามที่ 4: Aspose.Note รองรับการเพิ่มรูปภาพจาก URL หรือไม่

A4: Aspose.Note รองรับการเพิ่มรูปภาพจากไดเร็กทอรีภายในเครื่องเป็นหลัก แต่คุณสามารถรวมรูปภาพภายนอกได้โดยดาวน์โหลดจากในเครื่องก่อน

### คำถามที่ 5: มีข้อจำกัดเกี่ยวกับขนาดหรือรูปแบบของภาพที่สามารถเพิ่มได้หรือไม่?

A5: Aspose.Note รองรับรูปแบบภาพที่หลากหลาย และไม่มีข้อจำกัดที่เข้มงวดเกี่ยวกับขนาดภาพ ทำให้คุณสามารถรวมภาพที่หลากหลายลงในเอกสารของคุณได้