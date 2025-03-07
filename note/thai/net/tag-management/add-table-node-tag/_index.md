---
title: เพิ่มโหนดตารางด้วยแท็กใน Aspose.Note
linktitle: เพิ่มโหนดตารางด้วยแท็กใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีเพิ่มตารางด้วยแท็กใน Aspose.Note สำหรับ .NET พัฒนาทักษะการจัดการเอกสารของคุณโดยทางโปรแกรม
weight: 11
url: /th/net/tag-management/add-table-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มโหนดตารางด้วยแท็กใน Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการเพิ่มโหนดตารางด้วยแท็กโดยใช้ Aspose.Note สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อให้บรรลุเป้าหมายนี้

## นำเข้าเนมสเปซ

ก่อนที่จะเริ่มต้น ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นเพื่อทำงานกับ Aspose หมายเหตุ:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## ข้อกำหนดเบื้องต้น

ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้ก่อนดำเนินการต่อ:

1.  การติดตั้ง: ดาวน์โหลดและติดตั้งไลบรารี Aspose.Note สำหรับ .NET จาก[ที่นี่](https://releases.aspose.com/note/net/).
2.  ใบอนุญาต: ได้รับใบอนุญาตหรือใช้[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อใช้ห้องสมุด
3. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนาที่เข้ากันได้ เช่น Visual Studio

## ขั้นตอนที่ 1: เริ่มต้นเอกสารและวัตถุหน้า

 เริ่มต้นด้วยการสร้างอินสแตนซ์ของ`Document` คลาสและการเริ่มต้น`Page` วัตถุ:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## ขั้นตอนที่ 2: สร้างวัตถุตาราง แถว และเซลล์

 เริ่มต้น`Table`, `TableRow` , และ`TableCell` วัตถุ:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## ขั้นตอนที่ 3: แทรกเนื้อหาลงในเซลล์

 เพิ่มเนื้อหาลงในเซลล์โดยใช้`AppendChildLast` วิธี:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## ขั้นตอนที่ 4: เริ่มต้นโหนดตาราง

 เริ่มต้น`Table` วัตถุที่มีคุณสมบัติระบุ:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## ขั้นตอนที่ 5: เพิ่มแถวลงในตาราง

เพิ่มโหนดแถวลงในตาราง:

```csharp
table.AppendChildLast(row);
```

## ขั้นตอนที่ 6: เพิ่มแท็กลงในโหนดตาราง

รวมแท็กสำหรับโหนดตาราง:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## ขั้นตอนที่ 7: เพิ่มโหนดตารางให้กับองค์ประกอบเค้าร่าง

 สร้าง`Outline` และ`OutlineElement` เพื่อเพิ่มโหนดตาราง:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## ขั้นตอนที่ 8: บันทึกเอกสาร

บันทึกเอกสาร OneNote:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

หลังจากทำตามขั้นตอนเหล่านี้ คุณควรเพิ่มโหนดตารางด้วยแท็กโดยใช้ Aspose.Note สำหรับ .NET ได้สำเร็จ

## บทสรุป

ในบทช่วยสอนนี้ เราได้กล่าวถึงกระบวนการเพิ่มโหนดตารางด้วยแท็กใน Aspose.Note สำหรับ .NET เมื่อทำตามขั้นตอนเหล่านี้ คุณจะจัดการเอกสาร OneNote ได้อย่างมีประสิทธิภาพโดยทางโปรแกรม ซึ่งช่วยเพิ่มความสามารถในการจัดการเอกสารของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note เข้ากันได้กับ .NET ทุกเวอร์ชันหรือไม่

A1: Aspose.Note สำหรับ .NET รองรับ .NET Framework เวอร์ชัน 2.0 ขึ้นไป รวมถึง .NET Core และ .NET Standard

### คำถามที่ 2: ฉันสามารถลองใช้ Aspose.Note ก่อนซื้อใบอนุญาตได้หรือไม่

 ตอบ 2: ได้ คุณสามารถขอรับ Aspose.Note รุ่นทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะได้รับใบอนุญาตชั่วคราวสำหรับ Aspose.Note ได้อย่างไร

 A3: คุณสามารถขอรับใบอนุญาตชั่วคราวได้จาก[ลิงค์นี้](https://purchase.aspose.com/temporary-license/)ซึ่งมีอายุ 30 วัน

### คำถามที่ 4: Aspose.Note รองรับการเข้ารหัสเอกสารหรือไม่

ตอบ 4: ใช่ Aspose.Note ให้การสนับสนุนการเข้ารหัสเอกสาร OneNote เพื่อรับรองความปลอดภัยของข้อมูล

### คำถามที่ 5: มีการสนับสนุนทางเทคนิคสำหรับผู้ใช้ Aspose.Note หรือไม่

 A5: ใช่ มีการสนับสนุนทางเทคนิคผ่านฟอรัม Aspose[ที่นี่](https://forum.aspose.com/c/note/28)โดยคุณสามารถขอความช่วยเหลือจากผู้เชี่ยวชาญได้
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
