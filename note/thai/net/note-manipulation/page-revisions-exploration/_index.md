---
title: สำรวจการแก้ไขหน้าในเอกสาร Aspose.Note
linktitle: สำรวจการแก้ไขหน้าในเอกสาร Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีสำรวจการแก้ไขหน้าในเอกสาร Aspose.Note โดยใช้เฟรมเวิร์ก .NET พร้อมคำแนะนำทีละขั้นตอน
weight: 14
url: /th/net/note-manipulation/page-revisions-exploration/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สำรวจการแก้ไขหน้าในเอกสาร Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะเจาะลึกการสำรวจการแก้ไขหน้าในเอกสาร Aspose.Note โดยใช้เฟรมเวิร์ก .NET Aspose.Note เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม โดยนำเสนอฟีเจอร์ที่หลากหลายเพื่อจัดการและแยกข้อมูลจากไฟล์เหล่านี้

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:

### 1. ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ .NET

 เยี่ยมชม[หน้าดาวน์โหลด](https://releases.aspose.com/note/net/) และดาวน์โหลดไลบรารี Aspose.Note สำหรับ .NET ปฏิบัติตามคำแนะนำในการติดตั้งที่ให้ไว้เพื่อตั้งค่าไลบรารีในสภาพแวดล้อมการพัฒนาของคุณ

### 2. โหลดเนมสเปซที่จำเป็น

ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นในโปรเจ็กต์ .NET ของคุณเพื่อเข้าถึงฟังก์ชัน Aspose.Note ได้อย่างราบรื่น

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

ตอนนี้ เรามาแจกแจงขั้นตอนการสำรวจการแก้ไขหน้าเป็นคำแนะนำทีละขั้นตอน:

## ขั้นตอนที่ 1: โหลดเอกสาร

ขั้นแรก เราต้องโหลดเอกสาร Aspose.Note เพื่อให้แน่ใจว่าสามารถเปิดใช้งานการโหลดประวัติเอกสารได้

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## ขั้นตอนที่ 2: ดึงข้อมูลการแก้ไขหน้า

เมื่อโหลดเอกสารแล้ว เราจะสามารถเรียกดูการแก้ไขสำหรับหน้าใดหน้าหนึ่งได้ ในตัวอย่างนี้ เราจะได้รับการแก้ไขสำหรับหน้าแรก

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## ขั้นตอนที่ 3: ทำซ้ำผ่านการแก้ไข

ภายในลูป วนซ้ำการแก้ไขเพจแต่ละครั้งและเข้าถึงคุณสมบัติต่างๆ เช่น เวลาที่แก้ไขล่าสุด เวลาสร้าง ชื่อเรื่อง ระดับ และผู้แต่ง

## บทสรุป

การสำรวจการแก้ไขหน้าในเอกสาร Aspose.Note โดยใช้ .NET นั้นเป็นกระบวนการที่ไม่ซับซ้อน ด้วยการทำตามขั้นตอนที่อธิบายไว้ในบทช่วยสอนนี้ คุณสามารถดึงข้อมูลและวิเคราะห์ประวัติการแก้ไขของไฟล์ OneNote ของคุณโดยทางโปรแกรมได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.Note สำหรับ .NET เพื่อสร้างเอกสาร OneNote ใหม่ได้หรือไม่

A1: ใช่ Aspose.Note สำหรับ .NET อนุญาตให้คุณสร้าง แก้ไข และจัดการเอกสาร OneNote โดยทางโปรแกรม

### คำถามที่ 2: Aspose.Note รองรับประวัติการโหลดสำหรับไฟล์ OneNote ทุกประเภทหรือไม่

A2: Aspose.Note รองรับประวัติการโหลดสำหรับทั้งรูปแบบไฟล์ .one และ .onepkg

### คำถามที่ 3: Aspose.Note สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

A3: ได้ คุณสามารถดาวน์โหลด Aspose.Note สำหรับ .NET รุ่นทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ .NET ได้อย่างไร

 A4: คุณสามารถขอใบอนุญาตชั่วคราวได้จาก[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Note สำหรับ .NET ได้ที่ไหน

 A5: คุณสามารถค้นหาการสนับสนุนและแหล่งข้อมูลได้ที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
