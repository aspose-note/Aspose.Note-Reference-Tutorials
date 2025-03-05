---
title: รับข้อมูลรูปภาพใน Aspose.Note
linktitle: รับข้อมูลรูปภาพใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีแยกข้อมูลรูปภาพจากไฟล์ Microsoft OneNote โดยใช้ Aspose.Note สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการพัฒนาที่มีประสิทธิภาพ
type: docs
weight: 13
url: /th/net/images/get-info-of-images/
---
## การแนะนำ

ในโลกของการพัฒนา .NET นั้น Aspose.Note มอบชุดเครื่องมืออันทรงพลังสำหรับการทำงานกับไฟล์ Microsoft OneNote งานทั่วไปอย่างหนึ่งที่นักพัฒนามักเผชิญคือการดึงข้อมูลจากรูปภาพที่ฝังอยู่ในบันทึกย่อเหล่านี้ ไม่ว่าจะเป็นการรับมิติ ชื่อไฟล์ หรือเวลาในการแก้ไข Aspose.Note จะทำให้กระบวนการนี้ง่ายขึ้น

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกการดึงข้อมูลรูปภาพด้วย Aspose.Note ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. ความรู้พื้นฐานของ C#: ความคุ้นเคยกับภาษาการเขียนโปรแกรม C# เป็นสิ่งสำคัญในการทำความเข้าใจตัวอย่างโค้ด
2.  ติดตั้ง Aspose.Note สำหรับ .NET แล้ว: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Note ในสภาพแวดล้อมการพัฒนาของคุณ คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/note/net/).

## นำเข้าเนมสเปซ

ก่อนที่เราจะเริ่ม เรามานำเข้าเนมสเปซที่จำเป็นก่อน:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## ขั้นตอนที่ 1: โหลดเอกสาร

ขั้นแรก ให้โหลดเอกสาร OneNote เป้าหมายลงใน Aspose หมายเหตุ:

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";

// โหลดเอกสารลงใน Aspose.Note
Document oneFile = new Document(dataDir + "Aspose.one");
```

 แทนที่`"Your Document Directory"` พร้อมเส้นทางไปยังไฟล์ OneNote ของคุณ

## ขั้นตอนที่ 2: ดึงข้อมูลรูปภาพ

ถัดไป ดึงโหนดรูปภาพทั้งหมดจากเอกสาร:

```csharp
// รับโหนดรูปภาพทั้งหมด
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

ข้อมูลโค้ดนี้จะดึงโหนดรูปภาพทั้งหมดภายในเอกสาร OneNote ที่โหลด

## ขั้นตอนที่ 3: วนซ้ำผ่านรูปภาพ

ตอนนี้ เรามาวนซ้ำแต่ละโหนดรูปภาพเพื่อแยกข้อมูลเมตาของมัน:

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

การวนซ้ำนี้จะพิมพ์คุณลักษณะต่างๆ ของแต่ละภาพ เช่น ความกว้าง ความสูง ขนาดดั้งเดิม ชื่อไฟล์ และเวลาที่แก้ไขล่าสุด

## บทสรุป

ด้วย Aspose.Note สำหรับ .NET การดึงข้อมูลรูปภาพจากเอกสาร OneNote จะกลายเป็นกระบวนการที่ราบรื่น ด้วยการทำตามขั้นตอนที่ระบุไว้ในบทช่วยสอนนี้ นักพัฒนาสามารถดึงข้อมูลเมตาจากรูปภาพที่ฝังไว้ได้อย่างมีประสิทธิภาพ ช่วยให้พวกเขาสร้างแอปพลิเคชันที่แข็งแกร่งได้

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note เข้ากันได้กับ Microsoft OneNote ทุกเวอร์ชันหรือไม่

A1: Aspose.Note รองรับไฟล์ OneNote รูปแบบต่างๆ รวมถึง .one, .onepkg และ .onetoc2 เพื่อให้มั่นใจถึงความเข้ากันได้ในเวอร์ชันต่างๆ

### คำถามที่ 2: ฉันสามารถแก้ไขคุณสมบัติรูปภาพโดยใช้ Aspose.Note ได้หรือไม่

ตอบ 2: ใช่ Aspose.Note ช่วยให้คุณสามารถจัดการคุณสมบัติของรูปภาพ เช่น ขนาด ชื่อไฟล์ และเวลาในการแก้ไขโดยทางโปรแกรม

### คำถามที่ 3: Aspose.Note รองรับ .NET Core หรือไม่

ตอบ 3: ใช่ Aspose.Note ให้การสนับสนุน .NET Core ซึ่งช่วยให้สามารถพัฒนาข้ามแพลตฟอร์มสำหรับแอปพลิเคชันของคุณได้

### คำถามที่ 4: Aspose.Note มีรุ่นทดลองใช้ฟรีหรือไม่

ตอบ 4: ได้ คุณสามารถเข้าถึง Aspose รุ่นทดลองใช้ฟรีได้ หมายเหตุ เพื่อสำรวจฟีเจอร์ต่างๆ ก่อนตัดสินใจซื้อ

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือความช่วยเหลือเพิ่มเติมเกี่ยวกับ Aspose.Note ได้ที่ไหน

A5: หากมีข้อสงสัยหรือความช่วยเหลือ คุณสามารถไปที่ฟอรัม Aspose.Note[ที่นี่](https://forum.aspose.com/c/note/28).