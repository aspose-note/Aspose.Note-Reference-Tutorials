---
title: สร้างเอกสารจากเทมเพลตใน Aspose.Note
linktitle: สร้างเอกสารจากเทมเพลตใน Aspose.Note
second_title: Aspose.Note .NET API
description: สร้างเอกสารแบบไดนามิกได้อย่างง่ายดายด้วย Aspose.Note สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราสำหรับการสร้างเอกสารที่เป็นส่วนตัวและขับเคลื่อนด้วยข้อมูล
type: docs
weight: 18
url: /th/net/text-manipulation/generate-document-from-template/
---
## การแนะนำ
ในภูมิทัศน์ของการสร้างเอกสารที่มีการพัฒนาอยู่ตลอดเวลา Aspose.Note สำหรับ .NET มีความโดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับการสร้างเอกสารแบบไดนามิกได้อย่างง่ายดาย ไม่ว่าคุณจะจัดการกับรายงาน ใบแจ้งหนี้ หรือเอกสารส่วนตัว บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการสร้างเอกสารจากเทมเพลตโดยใช้ Aspose.Note สำหรับ .NET
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเจาะลึกคำแนะนำทีละขั้นตอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
1.  Aspose.Note สำหรับ .NET Library: ดาวน์โหลดและติดตั้งไลบรารีจาก[Aspose.Note สำหรับเอกสาร .NET](https://reference.aspose.com/note/net/).
2. เทมเพลตเอกสาร: เตรียมเอกสารเทมเพลตในรูปแบบ OneNote (พร้อมนามสกุล .one) สิ่งนี้จะทำหน้าที่เป็นรากฐานสำหรับเอกสารที่สร้างขึ้นแบบไดนามิกของคุณ
## นำเข้าเนมสเปซ
ตรวจสอบให้แน่ใจว่าได้รวมเนมสเปซที่จำเป็นในโครงการของคุณ:
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
ตอนนี้ เรามาดูรายละเอียดแต่ละขั้นตอนในคำแนะนำกัน
## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีเอกสารของคุณ
```csharp
string dataDir = "Your Document Directory";
```
แทนที่ "Your Document Directory" ด้วยเส้นทางที่คุณต้องการบันทึกเอกสารที่คุณสร้างขึ้น
## ขั้นตอนที่ 2: สร้างพจนานุกรมที่มีค่าการแทนที่
```csharp
var templateData = new Dictionary<string, string>
{
    { "Company", "Atlas Shrugged Ltd" },
    { "CandidateName", "John Galt" },
    { "JobTitle", "Chief Entrepreneur Officer" },
    { "Department", "Sales" },
    { "Salary", "123456 USD" },
    { "Vacation", "30" },
    { "StartDate", "29 Feb 2024" },
    { "YourName", "Ayn Rand" }
};
```
กำหนดพจนานุกรมโดยที่คีย์เป็นส่วนที่สำรองไว้ในเทมเพลตของคุณ และค่าคือข้อมูลที่คุณต้องการแทนที่ด้วย

## ขั้นตอนที่ 3: โหลดเอกสารเทมเพลต
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
โหลดเอกสารเทมเพลต OneNote ของคุณลงใน Aspose.Note

## ขั้นตอนที่ 4: แทนที่คำเทมเพลตด้วยข้อมูลไดนามิก
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
วนซ้ำแต่ละย่อหน้าในเทมเพลต โดยแทนที่ตัวยึดตำแหน่งด้วยข้อมูลไดนามิก

## ขั้นตอนที่ 5: บันทึกเอกสารที่สร้างขึ้น
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
บันทึกเอกสารที่สร้างขึ้นแบบไดนามิกไปยังไดเร็กทอรีที่คุณระบุ

## บทสรุป
ยินดีด้วย! คุณสร้างเอกสารแบบไดนามิกโดยใช้ Aspose.Note สำหรับ .NET สำเร็จแล้ว กระบวนการนี้เปิดโลกแห่งความเป็นไปได้ในการสร้างเอกสารที่เป็นส่วนตัวและขับเคลื่อนด้วยข้อมูลได้อย่างราบรื่น

## คำถามที่พบบ่อย
### ฉันสามารถใช้ Aspose.Note สำหรับ .NET กับเอกสารรูปแบบอื่นได้หรือไม่
ใช่ Aspose.Note สำหรับ .NET เกี่ยวข้องกับเอกสาร OneNote เป็นหลัก แต่ Aspose มีไลบรารีที่หลากหลายสำหรับรูปแบบที่แตกต่างกัน
### มี Aspose.Note สำหรับ .NET รุ่นทดลองใช้ฟรีหรือไม่
 ใช่ คุณสามารถสำรวจความสามารถของ Aspose.Note สำหรับ .NET ได้ด้วยการทดลองใช้ฟรี เยี่ยม[ที่นี่](https://releases.aspose.com/) สำหรับข้อมูลเพิ่มเติม.
### ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ .NET ได้อย่างไร
 เยี่ยมชม[Aspose.Note สำหรับฟอรัม .NET](https://forum.aspose.com/c/note/28) เพื่อรับความช่วยเหลือจากชุมชนและผู้เชี่ยวชาญ
### มีใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ .NET หรือไม่
 ใช่ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อวัตถุประสงค์ในการทดสอบและประเมินผล
### ฉันจะหาเอกสารที่ครอบคลุมสำหรับ Aspose.Note สำหรับ .NET ได้ที่ไหน
 อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/note/net/) สำหรับข้อมูลเชิงลึกเกี่ยวกับการใช้ Aspose.Note for .NET