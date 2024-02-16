---
title: สร้างเอกสารด้วยชื่อหน้าใน Aspose.Note
linktitle: สร้างเอกสารด้วยชื่อหน้าใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีสร้างเอกสารที่มีหน้าชื่อเรื่องโดยใช้ Aspose.Note สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
type: docs
weight: 13
url: /th/net/loading-and-saving-operations/create-doc-with-page-title/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการสร้างเอกสารที่มีหน้าชื่อเรื่องโดยใช้ Aspose.Note สำหรับ .NET Aspose.Note เป็น API อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งและตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:

### การติดตั้ง Visual Studio

1. ดาวน์โหลด Visual Studio: หากคุณยังไม่ได้ดาวน์โหลด ให้ดาวน์โหลดและติดตั้ง Visual Studio จากเว็บไซต์ Microsoft

2. ติดตั้งปริมาณงานการพัฒนา .NET: ในระหว่างกระบวนการติดตั้ง ตรวจสอบให้แน่ใจว่าได้เลือกปริมาณงาน "การพัฒนาเดสก์ท็อป .NET" เพื่อให้แน่ใจว่าคุณมีส่วนประกอบที่จำเป็นทั้งหมดสำหรับการพัฒนา .NET

3. สร้างโปรเจ็กต์ใหม่: เปิด Visual Studio และสร้างโปรเจ็กต์ใหม่ (แอปพลิเคชันคอนโซลหรือประเภทอื่น ๆ ที่คุณต้องการ)

### การติดตั้ง Aspose.Note

1.  รับ Aspose.Note: ดาวน์โหลดไลบรารี Aspose.Note สำหรับ .NET จาก[เว็บไซต์](https://releases.aspose.com/note/net/).

2. ติดตั้ง Aspose.Note ผ่าน NuGet: หรือคุณสามารถติดตั้ง Aspose.Note สำหรับ .NET ผ่าน NuGet Package Manager ใน Visual Studio เพียงค้นหา "Aspose.Note" และติดตั้งเวอร์ชันล่าสุด

## การนำเข้าเนมสเปซ

ขั้นแรก คุณต้องนำเข้าเนมสเปซที่จำเป็นเพื่อใช้ Aspose.Note ในโปรเจ็กต์ของคุณ

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

ตอนนี้ เรามาแจกแจงขั้นตอนการสร้างเอกสารที่มีชื่อหน้าเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: สร้างวัตถุเอกสาร

```csharp
//สร้างวัตถุของคลาสเอกสาร
Document doc = new Aspose.Note.Document();
```

## ขั้นตอนที่ 2: เริ่มต้นวัตถุคลาสหน้า

```csharp
// เริ่มต้นวัตถุคลาสหน้า
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## ขั้นตอนที่ 3: ตั้งค่าสไตล์เริ่มต้นสำหรับข้อความ

```csharp
// สไตล์เริ่มต้นสำหรับข้อความทั้งหมดในเอกสาร
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## ขั้นตอนที่ 4: ตั้งค่าคุณสมบัติชื่อหน้า

```csharp
// ตั้งค่าคุณสมบัติชื่อหน้า
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## ขั้นตอนที่ 5: ผนวกโหนดหน้าในเอกสาร

```csharp
// ผนวกโหนดหน้าในเอกสาร
doc.AppendChildLast(page);
```

## ขั้นตอนที่ 6: บันทึกเอกสาร OneNote

```csharp
// บันทึกเอกสาร OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## บทสรุป

ยินดีด้วย! คุณสร้างเอกสารที่มีหน้าชื่อเรื่องโดยใช้ Aspose.Note สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ให้คำแนะนำทีละขั้นตอนเพื่อช่วยคุณรวม Aspose.Note เข้ากับแอปพลิเคชัน .NET ของคุณสำหรับการจัดการไฟล์ OneNote โดยทางโปรแกรม

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งรูปแบบข้อความชื่อเรื่องได้หรือไม่

A1: ได้ คุณสามารถปรับแต่งสีฟอนต์ ชื่อฟอนต์ และขนาดฟอนต์ของข้อความชื่อเรื่องได้ตามความต้องการของคุณ

### คำถามที่ 2: Aspose.Note เข้ากันได้กับ .NET Core หรือไม่

ตอบ 2: ใช่ Aspose.Note รองรับ .NET Core ซึ่งช่วยให้คุณสามารถพัฒนาแอปพลิเคชันข้ามแพลตฟอร์มได้

### คำถามที่ 3: ฉันสามารถเพิ่มรูปภาพและไฟล์แนบลงในเอกสารได้หรือไม่

A3: แน่นอน! Aspose.Note มี API เพื่อเพิ่มรูปภาพ ไฟล์แนบ และองค์ประกอบอื่นๆ ลงในเอกสาร OneNote ของคุณได้อย่างราบรื่น

### คำถามที่ 4: Aspose.Note รองรับการอ่านไฟล์ OneNote ที่มีอยู่หรือไม่

A4: ได้ คุณสามารถใช้ Aspose.Note เพื่ออ่าน แก้ไข และจัดการไฟล์ OneNote ที่มีอยู่ได้อย่างง่ายดาย

### คำถามที่ 5: ฉันจะขอความช่วยเหลือได้ที่ไหนหากฉันประสบปัญหาใดๆ

 A5: คุณสามารถค้นหาการสนับสนุนและความช่วยเหลือได้ที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28)ซึ่งผู้เชี่ยวชาญและสมาชิกชุมชนสามารถช่วยตอบคำถามของคุณได้