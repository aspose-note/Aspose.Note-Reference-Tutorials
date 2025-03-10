---
title: เน้นการเปลี่ยนแปลงล่าสุดทั้งหมดในข้อความ Aspose.Note
linktitle: เน้นการเปลี่ยนแปลงล่าสุดทั้งหมดในข้อความ Aspose.Note
second_title: Aspose.Note .NET API
description: ปรับปรุงเอกสาร Note ของคุณด้วย Aspose.Note สำหรับ .NET! เรียนรู้วิธีเน้นการเปลี่ยนแปลงล่าสุดในข้อความด้วยบทช่วยสอนทีละขั้นตอนนี้
weight: 19
url: /th/net/text-manipulation/highlight-recent-changes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เน้นการเปลี่ยนแปลงล่าสุดทั้งหมดในข้อความ Aspose.Note

## การแนะนำ
คุณต้องการเพิ่มคุณสมบัติแบบไดนามิกและดึงดูดสายตาให้กับเอกสาร Note ของคุณโดยใช้ .NET หรือไม่? Aspose.Note สำหรับ .NET เป็นโซลูชันอันทรงพลังที่ช่วยให้คุณสามารถจัดการและปรับปรุงไฟล์ Note ของคุณได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะเจาะลึกประเด็นเฉพาะด้านหนึ่ง: เน้นการเปลี่ยนแปลงล่าสุดทั้งหมดในข้อความ Aspose.Note
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่มต้นการเดินทางนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.Note สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Note แล้ว คุณสามารถดาวน์โหลดได้จาก[Aspose.Note สำหรับเอกสาร .NET](https://reference.aspose.com/note/net/).
- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET รวมถึง IDE เช่น Visual Studio
- เอกสารตัวอย่าง: เตรียมเอกสาร Note (ในกรณีนี้คือ "Aspose.one") ที่มีข้อความที่คุณต้องการเน้น
## นำเข้าเนมสเปซ
ในการเริ่มต้น ให้นำเข้าเนมสเปซที่จำเป็นในโปรเจ็กต์ .NET ของคุณ:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
    using System.Linq;
```
## ขั้นตอนที่ 1: โหลดเอกสาร
เริ่มต้นด้วยการโหลดเอกสาร Note ลงใน Aspose หมายเหตุ:
```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one");
```
## ขั้นตอนที่ 2: ระบุการเปลี่ยนแปลงล่าสุด
ถัดไป ระบุโหนด RichText ที่แก้ไขภายในสัปดาห์ที่ผ่านมา:
```csharp
var richTextNodes = document.GetChildNodes<RichText>().Where(e => e.LastModifiedTime >= DateTime.Today.Subtract(TimeSpan.FromDays(7)));
```
## ขั้นตอนที่ 3: ตั้งค่าสีไฮไลท์
ตอนนี้ ตั้งค่าสีไฮไลต์สำหรับโหนดที่ระบุและเรียกใช้ข้อความ:
```csharp
foreach (var node in richTextNodes)
{
    // กำหนดสีไฮไลต์ให้กับย่อหน้า
    node.ParagraphStyle.Highlight = Color.DarkGreen;
    // ตั้งค่าสีไฮไลต์สำหรับการเรียกใช้ข้อความแต่ละครั้ง
    foreach (var run in node.TextRuns)
    {
        run.Style.Highlight = Color.DarkSeaGreen;
    }
}
```
## ขั้นตอนที่ 4: บันทึกเอกสารที่แก้ไข
บันทึกเอกสารโดยเน้นการเปลี่ยนแปลงล่าสุด:
```csharp
document.Save(Path.Combine(dataDir, "HighlightAllRecentChanges.pdf"));
```
## ขั้นตอนที่ 5: แสดงข้อความแสดงความสำเร็จ
สุดท้าย แสดงข้อความแสดงความสำเร็จเพื่อแจ้งให้ผู้ใช้ทราบ:
```csharp
Console.WriteLine("\nText's recent changes are highlighted successfully.");
```
## บทสรุป
ในบทช่วยสอนนี้ เราได้สำรวจวิธีใช้ Aspose.Note สำหรับ .NET เพื่อเน้นการเปลี่ยนแปลงล่าสุดทั้งหมดในข้อความภายในเอกสาร Note คุณสมบัตินี้ช่วยเพิ่มการมองเห็นเอกสาร และเป็นส่วนเสริมที่มีคุณค่าสำหรับชุดเครื่องมือของคุณสำหรับการทำงานกับไฟล์ Note
## คำถามที่พบบ่อย
### ฉันสามารถใช้สีไฮไลต์ที่แตกต่างกันในช่วงเวลาต่างๆ ได้หรือไม่
ใช่ คุณสามารถปรับแต่งโค้ดเพื่อตั้งค่าสีไฮไลต์ต่างๆ ได้ตามความต้องการเฉพาะของคุณ
### Aspose.Note เข้ากันได้กับเฟรมเวิร์ก .NET ล่าสุดหรือไม่
Aspose.Note อัปเดตไลบรารีเป็นประจำเพื่อให้แน่ใจว่าเข้ากันได้กับเฟรมเวิร์ก .NET ล่าสุด
### ฉันจะจัดการกับข้อผิดพลาดขณะใช้งานฟีเจอร์นี้ได้อย่างไร
คุณสามารถรวมบล็อก try-catch เพื่อจัดการกับข้อยกเว้นและมอบประสบการณ์ผู้ใช้ที่ราบรื่น
### Aspose.Note รองรับฟีเจอร์การจัดรูปแบบข้อความอื่นๆ หรือไม่
อย่างแน่นอน! Aspose.Note มีคุณสมบัติมากมายสำหรับการจัดรูปแบบข้อความ รวมถึงลักษณะแบบอักษร ขนาด และอื่นๆ
### ฉันสามารถรวมโซลูชันนี้เข้ากับเว็บแอปพลิเคชันได้หรือไม่
ได้ คุณสามารถรวม Aspose.Note สำหรับ .NET เข้ากับเว็บแอปพลิเคชันเพื่อเพิ่มความสามารถในการประมวลผลเอกสารได้
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
