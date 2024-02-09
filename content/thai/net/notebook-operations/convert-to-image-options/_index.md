---
title: แปลงโน้ตบุ๊กเป็นรูปภาพด้วยตัวเลือกใน Aspose Note .NET
linktitle: แปลงโน้ตบุ๊กเป็นรูปภาพด้วยตัวเลือกใน Aspose Note .NET
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีแปลงสมุดบันทึกเป็นรูปภาพด้วยตัวเลือกที่ปรับแต่งได้โดยใช้ Aspose.Note สำหรับ .NET
type: docs
weight: 13
url: /th/net/notebook-operations/convert-to-image-options/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะเจาะลึกการแปลงสมุดบันทึกเป็นรูปภาพด้วยตัวเลือกต่างๆ โดยใช้ไลบรารี Aspose.Note สำหรับ .NET Aspose.Note เป็น .NET API อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ด้วยการทำตามขั้นตอนที่ระบุไว้ในคู่มือนี้ คุณจะได้เรียนรู้วิธีแปลงสมุดบันทึกเป็นรูปภาพอย่างง่ายดาย พร้อมปรับแต่งเอาต์พุตตามความต้องการของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1. ความรู้พื้นฐานเกี่ยวกับ C#: ความคุ้นเคยกับภาษาการเขียนโปรแกรม C# เป็นสิ่งสำคัญในการทำความเข้าใจและใช้งานตัวอย่างโค้ดที่ให้มา

2.  Aspose.Note สำหรับ .NET: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ .NET จาก[เว็บไซต์](https://releases.aspose.com/note/net/). คุณสามารถขอรับรุ่นทดลองใช้ฟรีหรือซื้อใบอนุญาตได้ตามความต้องการของคุณ

3. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนาที่คุณต้องการด้วย Visual Studio หรือ IDE อื่น ๆ ที่รองรับการพัฒนา .NET

## นำเข้าเนมสเปซ

ในการเริ่มต้น เรามานำเข้าเนมสเปซที่จำเป็นเพื่อทำงานกับ Aspose.Note สำหรับ .NET กัน

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

ตอนนี้ เรามาแจกแจงขั้นตอนการแปลงสมุดบันทึกเป็นรูปภาพพร้อมตัวเลือกต่างๆ ออกเป็นหลายขั้นตอน

## ขั้นตอนที่ 1: โหลดโน้ตบุ๊ก

ขั้นแรก โหลดไฟล์สมุดบันทึกที่คุณต้องการแปลงเป็นรูปภาพ

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";

// โหลดสมุดบันทึก OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการบันทึกรูปภาพ

ระบุตัวเลือกสำหรับการบันทึกสมุดบันทึกเป็นรูปภาพ ที่นี่ เราจะตั้งค่ารูปแบบรูปภาพเป็น PNG และปรับแต่งความละเอียด

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
```

## ขั้นตอนที่ 3: บันทึกสมุดบันทึกเป็นรูปภาพ

บันทึกสมุดบันทึกเป็นรูปภาพโดยใช้ตัวเลือกที่ระบุ

```csharp
dataDir = dataDir + "ConvertToImageWithOptions_out.png";

// บันทึกสมุดบันทึก
notebook.Save(dataDir, notebookSaveOptions);
```

## บทสรุป

โดยสรุป เราได้สำรวจวิธีการแปลงสมุดบันทึกเป็นรูปภาพด้วยตัวเลือกต่างๆ โดยใช้ Aspose.Note สำหรับ .NET ด้วยการทำตามขั้นตอนที่ระบุไว้ในบทช่วยสอนนี้ คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่น ช่วยให้สามารถจัดการไฟล์ Microsoft OneNote ได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถแปลงสมุดบันทึกหลายเครื่องพร้อมกันโดยใช้ Aspose.Note สำหรับ .NET ได้หรือไม่

ตอบ 1: ได้ คุณสามารถวนซ้ำไฟล์สมุดบันทึกหลายไฟล์แล้วแปลงเป็นรูปภาพโดยใช้วิธีการที่คล้ายกันดังที่แสดงในบทช่วยสอนนี้

### คำถามที่ 2: Aspose.Note สำหรับ .NET เข้ากันได้กับ .NET Core หรือไม่

ตอบ 2: ใช่ Aspose.Note สำหรับ .NET เข้ากันได้กับทั้งสภาพแวดล้อม .NET Framework และ .NET Core

### คำถามที่ 3: มีข้อจำกัดเกี่ยวกับขนาดของสมุดบันทึกที่สามารถแปลงเป็นรูปภาพได้หรือไม่

A3: Aspose.Note สำหรับ .NET ไม่ได้กำหนดข้อจำกัดเฉพาะเกี่ยวกับขนาดของสมุดบันทึกที่สามารถแปลงได้ แต่ประสิทธิภาพอาจแตกต่างกันไปตามขนาดและความซับซ้อนของสมุดบันทึก

### คำถามที่ 4: ฉันสามารถปรับแต่งภาพที่ส่งออกไปเกินกว่าการตั้งค่าความละเอียดได้หรือไม่

A4: ใช่ Aspose.Note สำหรับ .NET มีตัวเลือกต่างๆ สำหรับการปรับแต่งเอาท์พุตรูปภาพ เช่น การปรับระยะขอบ สี และระดับการบีบอัด

### คำถามที่ 5: Aspose.Note สำหรับ .NET รองรับรูปแบบรูปภาพอื่นๆ นอกเหนือจาก PNG หรือไม่

A5: ใช่ Aspose.Note สำหรับ .NET รองรับรูปแบบรูปภาพหลายรูปแบบ รวมถึง JPEG, BMP, GIF และ TIFF