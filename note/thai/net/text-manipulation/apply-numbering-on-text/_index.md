---
title: ใช้การกำหนดหมายเลขกับข้อความใน Aspose.Note
linktitle: ใช้การกำหนดหมายเลขกับข้อความใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีใช้การกำหนดหมายเลขข้อความใน Aspose.Note สำหรับ .NET ด้วยบทช่วยสอนที่ครอบคลุมนี้ ปรับปรุงการจัดรูปแบบเอกสารของคุณได้อย่างง่ายดาย
weight: 12
url: /th/net/text-manipulation/apply-numbering-on-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ใช้การกำหนดหมายเลขกับข้อความใน Aspose.Note

## การแนะนำ
Aspose.Note สำหรับ .NET มีเครื่องมืออันทรงพลังสำหรับการจัดการเอกสารในแอปพลิเคชัน C# ในบทช่วยสอนนี้ เราจะสำรวจกระบวนการใส่ลำดับเลขกับข้อความโดยใช้ Aspose.Note ทำตามคำแนะนำทีละขั้นตอนเหล่านี้เพื่อปรับปรุงการจัดรูปแบบเอกสารของคุณได้อย่างง่ายดาย
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- ความเข้าใจพื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C#
-  ติดตั้ง Aspose.Note สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/note/net/).
- สภาพแวดล้อมการพัฒนาแบบรวม (IDE) เช่น Visual Studio
## นำเข้าเนมสเปซ
ในการเริ่มต้น ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นในโปรเจ็กต์ C# ของคุณ:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## ขั้นตอนที่ 1: ตั้งค่าเอกสารของคุณ
เริ่มต้นด้วยการสร้างเอกสารใหม่และเตรียมใช้งานออบเจ็กต์ที่ต้องการ:
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
//สร้างวัตถุของคลาสเอกสาร
Document doc = new Document();
// เริ่มต้นวัตถุคลาสหน้า
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// เริ่มต้นวัตถุคลาสเค้าร่าง
Outline outline = new Outline(doc);
```
## ขั้นตอนที่ 2: กำหนดสไตล์เริ่มต้น
ตั้งค่าสไตล์เริ่มต้นสำหรับข้อความของคุณโดยใช้คลาส ParagraphStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## ขั้นตอนที่ 3: ใช้การกำหนดหมายเลข
เริ่มต้นออบเจ็กต์คลาส OutlineElement และใช้การกำหนดหมายเลขกับแต่ละองค์ประกอบ:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## ขั้นตอนที่ 4: เพิ่มองค์ประกอบเค้าร่าง
ผนวกองค์ประกอบโครงร่างเข้ากับโครงร่าง:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## ขั้นตอนที่ 5: บันทึกเอกสาร
บันทึกเอกสาร OneNote โดยใช้การกำหนดหมายเลข:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## บทสรุป
ยินดีด้วย! คุณได้เรียนรู้วิธีใช้การกำหนดหมายเลขกับข้อความใน Aspose.Note สำหรับ .NET เรียบร้อยแล้ว ทดลองใช้ตัวเลือกการจัดรูปแบบต่างๆ เพื่อสร้างเอกสารที่ดึงดูดสายตาได้อย่างง่ายดาย
## คำถามที่พบบ่อย
### 1. ฉันสามารถปรับแต่งรูปแบบการกำหนดหมายเลขได้หรือไม่?
ใช่ คลาส NumberList ช่วยให้คุณปรับแต่งรูปแบบการกำหนดหมายเลขตามความต้องการของคุณได้
### 2. มีตัวเลือกการจัดรูปแบบอื่นหรือไม่?
Aspose.Note มีตัวเลือกการจัดรูปแบบที่หลากหลาย รวมถึงการจัดรูปแบบแบบอักษร สี และอื่นๆ อีกมากมาย
### 3. Aspose.Note เข้ากันได้กับ Visual Studio หรือไม่
อย่างแน่นอน! Aspose.Note ผสานรวมกับ Visual Studio ได้อย่างราบรื่นเพื่อประสบการณ์การพัฒนาที่ราบรื่น
### 4. ฉันสามารถลองใช้ Aspose.Note ก่อนซื้อได้หรือไม่
 แน่นอน! คุณสามารถสำรวจการทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
### 5. ฉันจะรับการสนับสนุนสำหรับ Aspose.Note ได้ที่ไหน
 สำหรับความช่วยเหลือหรือข้อสงสัยใด ๆ โปรดไปที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
