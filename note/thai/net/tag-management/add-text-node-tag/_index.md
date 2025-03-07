---
title: เพิ่มโหนดข้อความพร้อมแท็กใน Aspose.Note
linktitle: เพิ่มโหนดข้อความพร้อมแท็กใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีเพิ่มโหนดข้อความด้วยแท็กลงในเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ .NET
weight: 12
url: /th/net/tag-management/add-text-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มโหนดข้อความพร้อมแท็กใน Aspose.Note

## การแนะนำ

Aspose.Note for .NET เป็นไลบรารีที่มีประสิทธิภาพซึ่งช่วยให้นักพัฒนาสามารถสร้าง จัดการ และแปลงไฟล์ Microsoft OneNote โดยทางโปรแกรมโดยใช้เฟรมเวิร์ก .NET ในบทช่วยสอนนี้ เราจะสำรวจวิธีเพิ่มโหนดข้อความด้วยแท็กลงในเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1. Visual Studio: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Visual Studio บนระบบของคุณ
2.  Aspose.Note สำหรับ .NET: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ .NET จาก[เว็บไซต์](https://releases.aspose.com/note/net/).
3. ความรู้พื้นฐานของ C#: ทำความคุ้นเคยกับพื้นฐานภาษาการเขียนโปรแกรม C#

## นำเข้าเนมสเปซ

ขั้นแรก คุณต้องนำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงคลาสและวิธีการที่จำเป็นสำหรับการทำงานกับ Aspose.Note สำหรับ .NET

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## ขั้นตอนที่ 1: สร้างวัตถุเอกสาร

เตรียมใช้งานวัตถุเอกสารเพื่อเริ่มทำงานกับเอกสาร OneNote

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## ขั้นตอนที่ 2: เริ่มต้นออบเจ็กต์เพจและเค้าร่าง

สร้างออบเจ็กต์เพจและเค้าร่างเพื่อจัดโครงสร้างเนื้อหาของเอกสาร OneNote

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## ขั้นตอนที่ 3: เพิ่มโหนดข้อความด้วยแท็ก

สร้างออบเจ็กต์ RichText ด้วยข้อความและสไตล์ที่ต้องการ จากนั้นเพิ่มลงใน OutlineElement

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## ขั้นตอนที่ 4: ผนวกองค์ประกอบโครงร่างและโหนดหน้า

ผนวก OutlineElement เข้ากับ Outline จากนั้นจึงผนวก OutlineElement เข้ากับเพจ สุดท้าย ผนวกเพจเข้ากับเอกสาร

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## ขั้นตอนที่ 5: บันทึกเอกสาร

บันทึกเอกสาร OneNote ที่แก้ไขไปยังตำแหน่งที่ระบุ

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีเพิ่มโหนดข้อความด้วยแท็กลงในเอกสาร OneNote โดยใช้ Aspose.Note สำหรับ .NET เรียบร้อยแล้ว ด้วยความรู้นี้ คุณสามารถปรับแต่งและปรับปรุงไฟล์ OneNote ของคุณโดยทางโปรแกรมได้

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถเพิ่มโหนดข้อความหลายรายการที่มีแท็กต่างกันในเอกสารเดียวกันได้หรือไม่

A1: ได้ คุณสามารถเพิ่มโหนดข้อความหลายรายการด้วยแท็กที่แตกต่างกันได้โดยทำตามขั้นตอนเดียวกันสำหรับแต่ละโหนด

### คำถามที่ 2: Aspose.Note สำหรับ .NET เข้ากันได้กับ OneNote ทุกเวอร์ชันหรือไม่

A2: Aspose.Note สำหรับ .NET รองรับ OneNote เวอร์ชันต่างๆ รวมถึง 2010, 2013, 2016 และใหม่กว่า

### คำถามที่ 3: ฉันสามารถปรับแต่งสีและรูปแบบของแท็กได้หรือไม่

A3: ได้ คุณสามารถปรับแต่งสีและสไตล์ของแท็กได้ตามความต้องการของคุณ

### คำถามที่ 4: Aspose.Note สำหรับ .NET รองรับการเข้ารหัสเอกสารหรือไม่

ตอบ 4: ใช่ Aspose.Note สำหรับ .NET รองรับการเข้ารหัสเอกสารเพื่อให้มั่นใจในความปลอดภัยของข้อมูล

### คำถามที่ 5: ฉันจะค้นหาแหล่งข้อมูลเพิ่มเติมและการสนับสนุนสำหรับ Aspose.Note สำหรับ .NET ได้ที่ไหน

 A5: คุณสามารถสำรวจ[Aspose.Note สำหรับเอกสาร .NET](https://reference.aspose.com/note/net/)และขอความช่วยเหลือจาก[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
