---
title: บันทึกเป็นภาพระดับสีเทาใน Aspose.Note
linktitle: บันทึกเป็นภาพระดับสีเทาใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีบันทึกเอกสาร OneNote เป็นรูปภาพระดับสีเทาโดยใช้ Aspose.Note สำหรับ .NET ปฏิบัติตามบทช่วยสอนที่ครอบคลุมนี้เพื่อการประมวลผลเอกสารที่มีประสิทธิภาพ
weight: 24
url: /th/net/loading-and-saving-operations/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกเป็นภาพระดับสีเทาใน Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีใช้ Aspose.Note สำหรับ .NET เพื่อบันทึกเอกสารเป็นรูปภาพระดับสีเทา Aspose.Note เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม โดยมีฟังก์ชันการทำงานที่หลากหลาย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะดำเนินการ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

- ความเข้าใจพื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C#
- ติดตั้ง Visual Studio บนระบบของคุณแล้ว
-  ติดตั้ง Aspose.Note สำหรับไลบรารี .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/note/net/).
- ความคุ้นเคยกับการเข้าถึงและจัดการไฟล์โดยใช้ .NET

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;

using Aspose.Note.Saving;

```

## ขั้นตอนที่ 1: โหลดเอกสาร

ขั้นแรก โหลดเอกสารลงใน Aspose.Note 

```csharp
string dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## ขั้นตอนที่ 2: บันทึกเป็นภาพระดับสีเทา

จากนั้น ระบุเส้นทางสำหรับบันทึกภาพระดับสีเทาและบันทึกเอกสารตามลำดับ

```csharp
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
oneFile.Save(dataDir, new ImageSaveOptions(SaveFormat.Png)
					  {
						  ColorMode = ColorMode.GrayScale
					  });
```

## ขั้นตอนที่ 3: ตรวจสอบและแสดงผล

สุดท้าย ตรวจสอบและแสดงข้อความการแปลงที่สำเร็จพร้อมกับเส้นทางของไฟล์

```csharp
Console.WriteLine("\nOneNote document converted successfully to grayscale image.\nFile saved at " + dataDir);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีใช้ Aspose.Note สำหรับ .NET เพื่อแปลงเอกสารให้เป็นภาพระดับสีเทา ด้วยการทำตามขั้นตอนง่ายๆ เหล่านี้ นักพัฒนาสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชันของตนได้อย่างมีประสิทธิภาพ เพิ่มความสามารถในการประมวลผลเอกสาร

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สามารถจัดการไฟล์ OneNote ที่ซับซ้อนได้หรือไม่

ตอบ 1: ได้ Aspose.Note สามารถจัดการไฟล์ OneNote ที่ซับซ้อนได้อย่างมีประสิทธิภาพ โดยมีฟังก์ชันการทำงานที่แข็งแกร่งสำหรับการจัดการเอกสาร

### คำถามที่ 2: Aspose.Note เข้ากันได้กับรูปแบบไฟล์ที่แตกต่างกันหรือไม่

ตอบ 2: แน่นอนว่า Aspose.Note รองรับไฟล์ได้หลากหลายรูปแบบ ทำให้มั่นใจได้ถึงความยืดหยุ่นในการประมวลผลเอกสาร

### คำถามที่ 3: Aspose.Note ให้การสนับสนุนสำหรับนักพัฒนาหรือไม่

ตอบ 3: ได้ นักพัฒนาสามารถเข้าถึงการสนับสนุนที่ครอบคลุมผ่านทางฟอรัมและเอกสารประกอบของ Aspose

### คำถามที่ 4: ฉันสามารถลองใช้ Aspose.Note ก่อนซื้อได้หรือไม่

A4: ได้ คุณสามารถสำรวจ Aspose.Note ได้ผ่านการทดลองใช้ฟรีบนเว็บไซต์ของพวกเขา

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note ได้อย่างไร

A5: คุณสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note ได้โดยไปที่ลิงก์ที่ให้ไว้และทำตามคำแนะนำ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
