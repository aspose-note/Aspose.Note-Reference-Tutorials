---
title: สร้างเอกสารด้วยรูทและเพจย่อยโดยใช้ Aspose.Note
linktitle: สร้างเอกสารด้วยรูทและเพจย่อยโดยใช้ Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีใช้ Aspose.Note สำหรับ .NET เพื่อสร้างเอกสาร OneNote แบบไดนามิกที่มีโครงสร้างแบบลำดับชั้น
type: docs
weight: 11
url: /th/net/note-manipulation/create-documents-root-sub-pages/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนของเราเกี่ยวกับการสร้างเอกสารด้วยรูทและเพจย่อยโดยใช้ Aspose.Note สำหรับ .NET! Aspose.Note เป็นไลบรารีที่มีประสิทธิภาพซึ่งช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ช่วยให้สามารถสร้าง จัดการ และแปลงเอกสาร OneNote ได้

ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการสร้างเอกสาร OneNote พร้อมรูทและเพจย่อยทีละขั้นตอน เราจะให้คำอธิบายโดยละเอียดและข้อมูลโค้ดโดยใช้ Aspose.Note สำหรับ .NET ทำให้คุณปฏิบัติตามและนำไปใช้ในโครงการของคุณเองได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1. Visual Studio: คุณจะต้องติดตั้ง Visual Studio บนระบบของคุณเพื่อเขียนและคอมไพล์โค้ด .NET
2.  Aspose.Note สำหรับ .NET: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ .NET จาก[หน้าดาวน์โหลด](https://releases.aspose.com/note/net/).
3. ความรู้พื้นฐาน C#: จำเป็นต้องมีความคุ้นเคยกับภาษาการเขียนโปรแกรม C# เพื่อทำความเข้าใจและนำตัวอย่างโค้ดไปใช้

เมื่อคุณตั้งค่าทุกอย่างเรียบร้อยแล้ว เรามาดำดิ่งเข้าสู่บทแนะนำกันดีกว่า!

## นำเข้าเนมสเปซ

ขั้นแรก เรามานำเข้าเนมสเปซที่จำเป็นเข้าสู่โปรเจ็กต์ของเรา:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## ขั้นตอนที่ 1: เริ่มต้นวัตถุเอกสาร

```csharp
// สร้างวัตถุของคลาสเอกสาร
Document doc = new Document();
```

## ขั้นตอนที่ 2: สร้างรูทเพจและเพจย่อย

```csharp
// เริ่มต้นออบเจ็กต์คลาส Page และตั้งค่าระดับ
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### สำหรับหน้า 1:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### สำหรับหน้า 2:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### สำหรับหน้า 3:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## ขั้นตอนที่ 4: เพิ่มหน้าลงในเอกสาร

```csharp
// เพิ่มหน้าลงในเอกสาร OneNote
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## ขั้นตอนที่ 5: บันทึกเอกสาร

```csharp
// บันทึกเอกสาร OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีสร้างเอกสารด้วยรูทและเพจย่อยโดยใช้ Aspose.Note สำหรับ .NET เรียบร้อยแล้ว ตอนนี้คุณสามารถใช้ความรู้นี้เพื่อสร้างเอกสาร OneNote ที่ซับซ้อนในแอปพลิเคชันของคุณได้แบบไดนามิก

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สามารถจัดการเอกสาร OneNote ขนาดใหญ่ได้หรือไม่

ตอบ 1: ใช่ Aspose.Note ได้รับการออกแบบมาเพื่อจัดการเอกสาร OneNote ขนาดใหญ่อย่างมีประสิทธิภาพโดยไม่กระทบต่อประสิทธิภาพการทำงาน

### คำถามที่ 2: Aspose.Note เข้ากันได้กับ .NET Core หรือไม่

ตอบ 2: ใช่ Aspose.Note รองรับ .NET Core พร้อมกับ .NET Framework แบบดั้งเดิม

### คำถามที่ 3: ฉันสามารถแปลงเอกสาร OneNote เป็นรูปแบบอื่นโดยใช้ Aspose.Note ได้หรือไม่

ตอบ 3: แน่นอน Aspose.Note มอบความสามารถในการแปลงเป็นรูปแบบต่างๆ รวมถึง PDF, DOCX, HTML และอื่นๆ

### คำถามที่ 4: Aspose.Note มีการบูรณาการระบบคลาวด์หรือไม่

ตอบ 4: Aspose.Note มุ่งเน้นไปที่การพัฒนาภายในองค์กรเป็นหลัก แต่คุณสามารถใช้งานได้ภายในสภาพแวดล้อมคลาวด์ด้วยการตั้งค่าที่เหมาะสม

### คำถามที่ 5: Aspose.Note มีการสนับสนุนด้านเทคนิคหรือไม่

A5: ใช่ Aspose ให้การสนับสนุนด้านเทคนิคโดยเฉพาะผ่านฟอรัม ซึ่งคุณสามารถถามคำถามและรับความช่วยเหลือได้