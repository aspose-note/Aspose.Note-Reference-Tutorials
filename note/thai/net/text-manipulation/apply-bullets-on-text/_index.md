---
title: ใช้สัญลักษณ์แสดงหัวข้อย่อยกับข้อความใน Aspose.Note
linktitle: ใช้สัญลักษณ์แสดงหัวข้อย่อยกับข้อความใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีใช้สัญลักษณ์แสดงหัวข้อย่อยกับข้อความใน Aspose.Note สำหรับ .NET เพื่อปรับปรุงเอกสาร OneNote ของคุณ ทำตามคำแนะนำทีละขั้นตอนนี้เพื่อการจัดรูปแบบที่มีประสิทธิภาพ
type: docs
weight: 10
url: /th/net/text-manipulation/apply-bullets-on-text/
---
## การแนะนำ
ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนเกี่ยวกับการใช้สัญลักษณ์แสดงหัวข้อย่อยกับข้อความโดยใช้ Aspose.Note สำหรับ .NET Aspose.Note เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote ในแอปพลิเคชัน .NET ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการใช้สัญลักษณ์แสดงหัวข้อย่อยกับข้อความ ซึ่งจะช่วยเพิ่มความน่าสนใจให้กับเอกสาร OneNote ของคุณ
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม C# และ .NET
-  ติดตั้ง Aspose.Note สำหรับไลบรารี .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/note/net/).
## นำเข้าเนมสเปซ
ในโค้ด C# ของคุณ ตรวจสอบให้แน่ใจว่าได้รวมเนมสเปซที่จำเป็น:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## ขั้นตอนที่ 1: ตั้งค่าเอกสารของคุณ
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
//สร้างวัตถุของคลาสเอกสาร
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## ขั้นตอนที่ 2: เริ่มต้นเพจและโครงร่าง
```csharp
// เริ่มต้นวัตถุคลาสหน้า
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// เริ่มต้นวัตถุคลาสเค้าร่าง
Outline outline = new Outline(doc);
```
## ขั้นตอนที่ 3: ตั้งค่ารูปแบบข้อความเริ่มต้น
```csharp
// เริ่มต้นวัตถุคลาส TextStyle และตั้งค่าคุณสมบัติการจัดรูปแบบ
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## ขั้นตอนที่ 4: สร้างองค์ประกอบโครงร่างด้วยสัญลักษณ์แสดงหัวข้อย่อย
```csharp
// เริ่มต้นวัตถุคลาส OutlineElement และใช้สัญลักษณ์แสดงหัวข้อย่อย
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// ทำซ้ำกับองค์ประกอบโครงร่างอื่นๆ
```
## ขั้นตอนที่ 5: เพิ่มองค์ประกอบโครงร่างลงในโครงร่าง
```csharp
// เพิ่มองค์ประกอบโครงร่าง
outline.AppendChildLast(outlineElem1);
// ทำซ้ำกับองค์ประกอบโครงร่างอื่นๆ
```
## ขั้นตอนที่ 6: เพิ่มโครงร่างลงในเพจ
```csharp
// เพิ่มโหนดเค้าร่าง
page.AppendChildLast(outline);
```
## ขั้นตอนที่ 7: เพิ่มหน้าลงในเอกสาร
```csharp
//เพิ่มโหนดหน้า
doc.AppendChildLast(page);
```
## ขั้นตอนที่ 8: บันทึกเอกสาร OneNote
```csharp
// บันทึกเอกสาร OneNote
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## บทสรุป
ยินดีด้วย! คุณได้เรียนรู้วิธีใช้สัญลักษณ์แสดงหัวข้อย่อยกับข้อความโดยใช้ Aspose.Note สำหรับ .NET เรียบร้อยแล้ว คุณลักษณะนี้สามารถปรับปรุงการจัดรูปแบบของเอกสาร OneNote ของคุณได้อย่างมาก ทำให้เอกสารเหล่านั้นดูน่าดึงดูดยิ่งขึ้น
## คำถามที่พบบ่อย
### ฉันสามารถใช้รูปแบบสัญลักษณ์แสดงหัวข้อย่อยที่แตกต่างกันกับแต่ละรายการในรายการได้หรือไม่
 ใช่ คุณสามารถปรับแต่งสไตล์สัญลักษณ์แสดงหัวข้อย่อยได้โดยการแก้ไข`NumberList` คุณสมบัติสำหรับแต่ละ`OutlineElement`.
### Aspose.Note เข้ากันได้กับ Microsoft OneNote เวอร์ชันล่าสุดหรือไม่
Aspose.Note รองรับ Microsoft OneNote เวอร์ชันต่างๆ เพื่อให้มั่นใจว่าเข้ากันได้กับทั้งเวอร์ชันเก่าและใหม่กว่า
### ฉันสามารถใช้ Aspose.Note เพื่อวัตถุประสงค์ทางการค้าได้หรือไม่
 ได้ คุณสามารถใช้ Aspose.Note สำหรับ .NET ในโครงการเชิงพาณิชย์ได้ หากต้องการรับใบอนุญาต โปรดไปที่[ที่นี่](https://purchase.aspose.com/buy).
### มีรุ่นทดลองใช้สำหรับ Aspose.Note สำหรับ .NET หรือไม่
 ใช่ คุณสามารถดาวน์โหลดรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
### ฉันจะหาการสนับสนุนและแหล่งข้อมูลเพิ่มเติมได้จากที่ไหน?
 คุณสามารถเยี่ยมชมฟอรัมชุมชน Aspose.Note[ที่นี่](https://forum.aspose.com/c/note/28) สำหรับการสนับสนุนและการอภิปราย