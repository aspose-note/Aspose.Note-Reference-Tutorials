---
title: แทรกรายการหมายเลขภาษาจีนในข้อความ Aspose.Note
linktitle: แทรกรายการหมายเลขภาษาจีนในข้อความ Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีแทรกรายการหมายเลขภาษาจีนใน Aspose.Note สำหรับเอกสาร .NET ได้อย่างง่ายดาย ยกระดับทักษะการจัดรูปแบบเอกสารของคุณด้วยคำแนะนำทีละขั้นตอนนี้
type: docs
weight: 20
url: /th/net/text-manipulation/insert-chinese-number-list/
---
## การแนะนำ
คุณต้องการพัฒนาทักษะ Aspose.Note สำหรับ .NET โดยการรวมรายการตัวเลขภาษาจีนไว้ในเอกสารของคุณหรือไม่? ถ้าเป็นเช่นนั้น คุณมาถูกที่แล้ว! ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแทรกรายการหมายเลขภาษาจีนโดยใช้ Aspose.Note สำหรับ .NET ไลบรารีอันทรงพลังนี้ช่วยให้คุณจัดการเอกสาร OneNote ได้อย่างราบรื่น
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม C#
-  ติดตั้ง Aspose.Note สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/note/net/).
## นำเข้าเนมสเปซ
ในการเริ่มต้น ให้นำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ของคุณ:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## ขั้นตอนที่ 1: เตรียมใช้งานเอกสาร OneNote
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## ขั้นตอนที่ 2: เริ่มต้นหน้า OneNote
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## ขั้นตอนที่ 3: ใช้การตั้งค่าสไตล์ข้อความ
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## ขั้นตอนที่ 4: สร้างองค์ประกอบเค้าร่าง
ตอนนี้ เรามาสร้างองค์ประกอบเค้าร่างสามองค์ประกอบด้วยรายการตัวเลขภาษาจีน:
### ขั้นตอนที่ 4.1: องค์ประกอบแรก
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### ขั้นตอนที่ 4.2: องค์ประกอบที่สอง
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### ขั้นตอนที่ 4.3: องค์ประกอบที่สาม
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## ขั้นตอนที่ 5: ผนวกองค์ประกอบเข้ากับโครงร่าง
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## ขั้นตอนที่ 6: ผนวกโครงร่างเข้ากับหน้า
```csharp
page.AppendChildLast(outline);
```
## ขั้นตอนที่ 7: ผนวกหน้าเข้ากับเอกสาร
```csharp
doc.AppendChildLast(page);
```
## ขั้นตอนที่ 8: บันทึกเอกสาร OneNote
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
ยินดีด้วย! คุณได้แทรกรายการหมายเลขภาษาจีนลงในเอกสาร Aspose.Note ของคุณสำเร็จแล้วโดยใช้ไลบรารี .NET
## บทสรุป
ในบทช่วยสอนนี้ เราได้กล่าวถึงกระบวนการทีละขั้นตอนในการรวมรายการหมายเลขภาษาจีนลงในเอกสาร Aspose.Note สำหรับ .NET พัฒนาทักษะการจัดรูปแบบเอกสารของคุณและทำให้เนื้อหาของคุณน่าดึงดูดยิ่งขึ้นด้วยเทคนิคเหล่านี้
## คำถามที่พบบ่อย
### ถาม: ฉันสามารถปรับแต่งการจัดรูปแบบของรายการตัวเลขภาษาจีนได้หรือไม่
 ตอบ: ได้ คุณสามารถปรับแต่งการจัดรูปแบบได้โดยการปรับพารามิเตอร์ใน`NumberList` ตัวสร้าง
### ถาม: Aspose.Note เข้ากันได้กับ .NET เวอร์ชันล่าสุดหรือไม่
ตอบ: ใช่ Aspose.Note ได้รับการอัปเดตเป็นประจำเพื่อรองรับ .NET เวอร์ชันล่าสุด
### ถาม: ฉันจะหาตัวอย่างและเอกสารเพิ่มเติมได้จากที่ไหน
 ตอบ: สำรวจอย่างครอบคลุม[เอกสาร Aspose.Note](https://reference.aspose.com/note/net/).
### ถาม: ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note ได้อย่างไร
 ตอบ: ขอรับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).
### ถาม: ฉันจะขอความช่วยเหลือหรือหารือเกี่ยวกับคำถามที่เกี่ยวข้องกับ Aspose.Note ได้ที่ไหน
 ตอบ: เยี่ยมชม[ฟอรัมสนับสนุน Aspose.Note](https://forum.aspose.com/c/note/28) เพื่อสนับสนุนชุมชน