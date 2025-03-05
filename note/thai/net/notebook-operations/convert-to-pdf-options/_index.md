---
title: แปลงโน้ตบุ๊กเป็น PDF ด้วยตัวเลือกใน Aspose Note .NET
linktitle: แปลงโน้ตบุ๊กเป็น PDF ด้วยตัวเลือกใน Aspose Note .NET
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีแปลงสมุดบันทึก Microsoft OneNote เป็นรูปแบบ PDF โดยใช้ Aspose.Note สำหรับไลบรารี .NET พร้อมตัวเลือกที่ปรับแต่งได้
type: docs
weight: 16
url: /th/net/notebook-operations/convert-to-pdf-options/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะอธิบายขั้นตอนการแปลงสมุดบันทึกเป็นรูปแบบ PDF โดยใช้ Aspose.Note สำหรับไลบรารี .NET Aspose.Note สำหรับ .NET มีชุดคุณลักษณะที่มีประสิทธิภาพในการทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

### 1. Aspose.Note สำหรับ .NET Library
 ตรวจสอบให้แน่ใจว่าคุณได้ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์](https://releases.aspose.com/note/net/).

### 2. สภาพแวดล้อมการพัฒนา
คุณควรตั้งค่าสภาพแวดล้อมการพัฒนา เช่น Visual Studio พร้อมติดตั้ง .NET Framework ที่จำเป็น

## นำเข้าเนมสเปซ

ก่อนที่เราจะเริ่มใช้ Aspose.Note สำหรับ .NET ในโปรเจ็กต์ของเรา เรามานำเข้าเนมสเปซที่จำเป็นก่อน:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

ตอนนี้ เรามาแจกแจงขั้นตอนการแปลงสมุดบันทึกเป็น PDF โดยมีตัวเลือกต่างๆ ออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: โหลดโน้ตบุ๊ก

ขั้นแรก เราต้องโหลดสมุดบันทึก OneNote ที่เราต้องการแปลงเป็นไฟล์ PDF

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";

// โหลดสมุดบันทึก OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## ขั้นตอนที่ 2: ระบุตัวเลือกการบันทึก PDF

ต่อไป เราจะระบุตัวเลือกในการบันทึกสมุดบันทึกเป็นไฟล์ PDF เราสามารถปรับแต่งการตั้งค่าต่างๆ ได้ เช่น อัลกอริธึมการแบ่งหน้า ระยะขอบ และขนาดหน้า

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## ขั้นตอนที่ 3: บันทึกสมุดบันทึกเป็น PDF

ตอนนี้เราจะบันทึกสมุดบันทึกเป็นไฟล์ PDF โดยใช้ตัวเลือกที่ระบุ

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// บันทึกสมุดบันทึก
notebook.Save(dataDir, notebookSaveOptions);
```

## ขั้นตอนที่ 4: ตรวจสอบการแปลง

สุดท้ายนี้ มาตรวจสอบว่าการแปลงสำเร็จแล้วและพิมพ์ตำแหน่งที่บันทึกไฟล์ PDF

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีแปลงสมุดบันทึก OneNote เป็นรูปแบบ PDF โดยใช้ Aspose.Note สำหรับไลบรารี .NET ด้วยการทำตามขั้นตอนที่อธิบายไว้ข้างต้น คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สำหรับ .NET เข้ากันได้กับ Microsoft OneNote ทุกเวอร์ชันหรือไม่

ตอบ 1: ใช่ Aspose.Note สำหรับ .NET รองรับ Microsoft OneNote เวอร์ชันต่างๆ รวมถึงรูปแบบ .one และ .onetoc2

### คำถามที่ 2: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของเอาต์พุต PDF ได้หรือไม่

A2: ได้ คุณสามารถระบุตัวเลือกต่างๆ ได้ เช่น ขนาดหน้า ระยะขอบ และอัลกอริธึมการแยกหน้า เพื่อปรับแต่งลักษณะที่ปรากฏของเอาต์พุต PDF

### คำถามที่ 3: Aspose.Note สำหรับ .NET ให้การสนับสนุนรูปแบบไฟล์อื่นๆ หรือไม่

ตอบ 3: ใช่ Aspose.Note สำหรับ .NET รองรับการแปลงเป็นรูปแบบอื่นๆ ที่หลากหลาย เช่น รูปภาพ, HTML และเอกสาร Microsoft Word

### คำถามที่ 4: Aspose.Note สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

ตอบ 4: ได้ คุณสามารถดาวน์โหลด Aspose.Note สำหรับ .NET รุ่นทดลองใช้ฟรีได้จากเว็บไซต์เพื่อประเมินคุณสมบัติต่างๆ ก่อนตัดสินใจซื้อ

### คำถามที่ 5: ฉันจะได้รับการสนับสนุนทางเทคนิคสำหรับ Aspose.Note สำหรับ .NET ได้อย่างไร

 A5: คุณสามารถรับการสนับสนุนด้านเทคนิคสำหรับ Aspose.Note สำหรับ .NET ได้โดยไปที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) หรือติดต่อทีมสนับสนุน Aspose โดยตรง