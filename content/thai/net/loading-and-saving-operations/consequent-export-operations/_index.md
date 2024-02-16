---
title: การดำเนินการส่งออกที่ตามมาใน Aspose.Note
linktitle: การดำเนินการส่งออกที่ตามมาใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีการดำเนินการส่งออกที่ตามมาใน Aspose.Note สำหรับ .NET เพื่อบันทึกเอกสาร OneNote ในรูปแบบต่างๆ ได้อย่างมีประสิทธิภาพ
type: docs
weight: 10
url: /th/net/loading-and-saving-operations/consequent-export-operations/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะเจาะลึกการดำเนินการส่งออกที่ตามมาโดยใช้ Aspose.Note สำหรับ .NET Aspose.Note เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม การส่งออกเอกสารเป็นรูปแบบต่างๆ เป็นข้อกำหนดทั่วไป และ Aspose.Note ช่วยให้งานนี้ง่ายขึ้นอย่างมีประสิทธิภาพ มาดูวิธีการบันทึกเอกสารในรูปแบบต่างๆ กันทีละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนดำเนินการบทช่วยสอนนี้ โปรดแน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. ความเข้าใจพื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C#
2. ติดตั้ง Visual Studio บนระบบของคุณแล้ว
3. Aspose.Note สำหรับไลบรารี .NET ที่ผสานรวมเข้ากับโปรเจ็กต์ของคุณ

## นำเข้าเนมสเปซ

ขั้นแรก ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นในโค้ด C# ของคุณ:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Drawing;
using System.Globalization;
```

## ขั้นตอนที่ 1: เริ่มต้นเอกสาร

 ก่อนอื่นให้เริ่มต้นใหม่`Document` วัตถุที่ปิดใช้งานการตรวจจับการเปลี่ยนแปลงเค้าโครงอัตโนมัติ:

```csharp
Document doc = new Document() { AutomaticLayoutChangesDetectionEnabled = false };
```

## ขั้นตอนที่ 2: เริ่มต้นหน้าใหม่

 สร้างใหม่`Page`วัตถุและระบุคุณสมบัติ:

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## ขั้นตอนที่ 3: ตั้งชื่อหน้า

กำหนดชื่อเรื่องสำหรับเพจพร้อมกับข้อมูลวันที่และเวลา:

```csharp
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## ขั้นตอนที่ 4: ผนวกโหนดหน้า

เพิ่มโหนดหน้าให้กับเอกสาร:

```csharp
doc.AppendChildLast(page);
```

## ขั้นตอนที่ 5: บันทึกเอกสารในรูปแบบที่แตกต่างกัน

ตอนนี้ ให้บันทึกเอกสาร OneNote ในรูปแบบต่างๆ:

```csharp
string dataDir = "Your Document Directory";
doc.Save(dataDir + "ConsequentExportOperations_out.html");            
doc.Save(dataDir + "ConsequentExportOperations_out.pdf");            
doc.Save(dataDir + "ConsequentExportOperations_out.jpg");            
textStyle.FontSize = 11;           
doc.DetectLayoutChanges();            
doc.Save(dataDir + "ConsequentExportOperations_out.bmp");
```

## บทสรุป

โดยสรุป เราได้เรียนรู้วิธีการดำเนินการส่งออกที่ตามมาโดยใช้ Aspose.Note สำหรับ .NET เมื่อทำตามขั้นตอนที่ระบุไว้ในบทช่วยสอนนี้ คุณจะสามารถบันทึกเอกสาร OneNote ในรูปแบบต่างๆ ได้อย่างราบรื่น ซึ่งจะช่วยเพิ่มความคล่องตัวให้กับแอปพลิเคชันของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งชื่อหน้าเพิ่มเติมได้หรือไม่

A1: ได้ คุณสามารถแก้ไขข้อความชื่อเรื่อง วันที่ และเวลาได้ตามความต้องการของคุณก่อนที่จะบันทึกเอกสาร

### คำถามที่ 2: ฉันจะจัดการกับการตรวจจับการเปลี่ยนแปลงเค้าโครงได้อย่างไร

 A2: ตามที่แสดงไว้ คุณสามารถตรวจจับการเปลี่ยนแปลงเลย์เอาต์ได้ด้วยตนเองโดยใช้`DetectLayoutChanges()` วิธีการจัดทำโดย Aspose.Note

### คำถามที่ 3: Aspose.Note รองรับรูปแบบการส่งออกอื่นๆ นอกเหนือจากรูปแบบที่กล่าวถึงหรือไม่

A3: ใช่ Aspose.Note รองรับรูปแบบการส่งออกที่หลากหลาย รวมถึง DOCX, PNG, TIFF และอื่นๆ

### คำถามที่ 4: Aspose.Note เข้ากันได้กับ .NET Core หรือไม่

A4: ใช่ Aspose.Note เข้ากันได้กับทั้งสภาพแวดล้อม .NET Framework และ .NET Core

### คำถามที่ 5: ฉันจะหาแหล่งข้อมูลเพิ่มเติมและการสนับสนุนสำหรับ Aspose.Note ได้ที่ไหน

A5: คุณสามารถเยี่ยมชมเอกสารและฟอรัมของ Aspose.Note เพื่อดูคำแนะนำแบบครอบคลุม บทช่วยสอน และการสนับสนุนชุมชน