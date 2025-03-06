---
title: แทรกรูปภาพโดยใช้ Image Stream ใน Aspose.Note
linktitle: แทรกรูปภาพโดยใช้ Image Stream ใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีแทรกรูปภาพลงในเอกสาร Aspose.Note ได้อย่างราบรื่นโดยใช้สตรีมรูปภาพใน .NET ปรับปรุงไฟล์ Note ของคุณด้วยภาพได้อย่างง่ายดาย
weight: 11
url: /th/net/images/insert-image-using-image-stream/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แทรกรูปภาพโดยใช้ Image Stream ใน Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีการแทรกรูปภาพลงในเอกสาร Aspose.Note โดยใช้สตรีมรูปภาพใน .NET Aspose.Note เป็น API อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม ด้วยการทำตามขั้นตอนที่ระบุไว้ในคู่มือนี้ คุณจะได้เรียนรู้วิธีรวมรูปภาพเข้ากับเอกสาร Note ของคุณได้อย่างราบรื่น เพิ่มความดึงดูดสายตาและฟังก์ชันการทำงานโดยรวม

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
1. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนาด้วยความสามารถของ .NET
2.  ไลบรารี Aspose.Note: ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note สำหรับ .NET คุณสามารถค้นหาลิงค์ดาวน์โหลด[ที่นี่](https://releases.aspose.com/note/net/).
3. ไฟล์รูปภาพ: เตรียมไฟล์รูปภาพที่คุณต้องการแทรกลงในเอกสาร Note ของคุณ
4. ความเข้าใจพื้นฐาน: ทำความคุ้นเคยกับแนวคิดพื้นฐานของภาษาการเขียนโปรแกรม C# และการจัดการไฟล์

## นำเข้าเนมสเปซ
ขั้นแรก เรามานำเข้าเนมสเปซที่จำเป็นให้กับโปรเจ็กต์ของเรากันก่อน เนมสเปซเหล่านี้จะให้การเข้าถึงคลาสและวิธีการที่จำเป็นในการทำงานกับ Aspose.Note และจัดการการแทรกรูปภาพ

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

ตอนนี้ เรามาแบ่งขั้นตอนการแทรกรูปภาพโดยใช้สตรีมรูปภาพออกเป็นหลายขั้นตอนกัน

## ขั้นตอนที่ 1: เริ่มต้นวัตถุเอกสาร
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
Document doc = new Document();
```
เราเริ่มต้นอินสแตนซ์ใหม่ของคลาสเอกสารซึ่งแสดงถึงเอกสาร OneNote

## ขั้นตอนที่ 2: สร้างวัตถุหน้า
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```
เราสร้างวัตถุหน้าใหม่เพื่อเพิ่มเนื้อหาลงไป

## ขั้นตอนที่ 3: เริ่มต้นออบเจ็กต์ Outline และ OutlineElement
```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```
เราสร้างอินสแตนซ์ของคลาส Outline และ OutlineElement เพื่อจัดโครงสร้างเนื้อหาของเราภายในเพจ

## ขั้นตอนที่ 4: โหลดรูปภาพจากสตรีม
```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```
เราเปิดไฟล์รูปภาพโดยใช้ FileStream และโหลดลงในออบเจ็กต์รูปภาพ เราสามารถระบุคุณสมบัติเช่นการจัดตำแหน่งให้กับรูปภาพได้

## ขั้นตอนที่ 5: ผนวกรูปภาพเข้ากับ OutlineElement
```csharp
outlineElem1.AppendChildLast(image1);
```
เราเพิ่มรูปภาพต่อท้าย OutlineElement ซึ่งเป็นการเพิ่มลงในโครงสร้างเอกสารอย่างมีประสิทธิภาพ

## ขั้นตอนที่ 6: ผนวก OutlineElement เข้ากับ Outline
```csharp
outline1.AppendChildLast(outlineElem1);
```
เราเพิ่ม OutlineElement ที่มีรูปภาพต่อท้าย OutlineElement

## ขั้นตอนที่ 7: ผนวกโครงร่างเข้ากับหน้า
```csharp
page.AppendChildLast(outline1);
```
เราต่อท้ายโครงร่างเข้ากับเพจ เพื่อสรุปโครงสร้างเนื้อหา

## ขั้นตอนที่ 8: ผนวกหน้าเข้ากับเอกสาร
```csharp
doc.AppendChildLast(page);
```
เราต่อท้ายหน้าเอกสารเพื่อประกอบเอกสารให้สมบูรณ์

## ขั้นตอนที่ 9: บันทึกเอกสาร
```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```
สุดท้าย เราจะบันทึกเอกสารที่ประกอบพร้อมรูปภาพที่แทรกไว้

## บทสรุป
เมื่อทำตามบทช่วยสอนนี้ คุณได้เรียนรู้วิธีแทรกรูปภาพลงในเอกสาร Aspose.Note โดยใช้สตรีมรูปภาพใน .NET ด้วยการใช้ประโยชน์จากความสามารถของ Aspose.Note คุณสามารถรวมภาพเข้ากับไฟล์ Note ของคุณได้อย่างราบรื่น ปรับปรุงอรรถประโยชน์และรูปลักษณ์ที่น่าดึงดูด

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถแทรกรูปภาพหลายรูปลงในเอกสารเดียวโดยใช้วิธีนี้ได้หรือไม่

A1: ได้ คุณสามารถแทรกรูปภาพหลายรูปลงในเอกสารเดียวได้โดยทำซ้ำขั้นตอนการแทรกรูปภาพสำหรับแต่ละรูปภาพ

### คำถามที่ 2: Aspose.Note รองรับรูปแบบรูปภาพอื่นนอกเหนือจาก JPG หรือไม่

ตอบ 2: ใช่ Aspose.Note รองรับรูปแบบรูปภาพที่หลากหลาย รวมถึง PNG, BMP, GIF และ TIFF

### คำถามที่ 3: ฉันสามารถปรับแต่งการจัดตำแหน่งและขนาดของรูปภาพที่แทรกได้หรือไม่

A3: แน่นอนว่า Aspose.Note มีตัวเลือกมากมายสำหรับการปรับแต่งการจัดตำแหน่ง ขนาด และคุณสมบัติอื่นๆ ของรูปภาพที่แทรก

### คำถามที่ 4: Aspose.Note เข้ากันได้กับ .NET ทุกเวอร์ชันหรือไม่

ตอบ 4: Aspose.Note สำหรับ .NET เข้ากันได้กับเฟรมเวิร์ก .NET หลายเวอร์ชัน ทำให้มั่นใจถึงความเข้ากันได้ในวงกว้างในสภาพแวดล้อมการพัฒนาที่แตกต่างกัน

### คำถามที่ 5: ฉันจะค้นหาแหล่งข้อมูลเพิ่มเติมและการสนับสนุนสำหรับ Aspose.Note ได้ที่ไหน

 A5: คุณสามารถค้นหาเอกสาร ฟอรั่ม และการสนับสนุนที่ครอบคลุมสำหรับ Aspose.Note ได้ที่[ตั้งฟอรั่ม](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
