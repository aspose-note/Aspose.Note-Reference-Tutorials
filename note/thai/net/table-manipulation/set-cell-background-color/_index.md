---
title: ตั้งค่าสีพื้นหลังของเซลล์ในตาราง Aspose.Note
linktitle: ตั้งค่าสีพื้นหลังของเซลล์ในตาราง Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีตั้งค่าสีพื้นหลังของเซลล์ในตาราง Aspose.Note โดยใช้คำแนะนำทีละขั้นตอน ปรับปรุงภาพเอกสารได้อย่างง่ายดาย
weight: 17
url: /th/net/table-manipulation/set-cell-background-color/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าสีพื้นหลังของเซลล์ในตาราง Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะเจาะลึกวิธีการตั้งค่าสีพื้นหลังของเซลล์ภายในตารางโดยใช้ Aspose.Note สำหรับ .NET คุณลักษณะนี้สามารถปรับปรุงรูปลักษณ์ที่สวยงามและความสามารถในการอ่านเอกสารของคุณได้อย่างมาก ทำตามขั้นตอนด้านล่างเพื่อเรียนรู้วิธีการบรรลุเป้าหมายนี้

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1.  การติดตั้ง Aspose.Note สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Note สำหรับ .NET คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/net/).
2. ความคุ้นเคยกับ C#: จำเป็นต้องมีความเข้าใจพื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C# เพื่อใช้งานโค้ดที่ให้มา

## นำเข้าเนมสเปซ

ขั้นแรก เรามานำเข้าเนมสเปซที่จำเป็นให้กับโปรเจ็กต์ของเรา:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## ขั้นตอนที่ 1: สร้างวัตถุเอกสาร

เริ่มต้นวัตถุเอกสาร:

```csharp
Document doc = new Document();
```

## ขั้นตอนที่ 2: เริ่มต้น TableCell และตั้งค่าเนื้อหาข้อความ

สร้างวัตถุ TableCell และตั้งค่าเนื้อหาข้อความพร้อมกับสีพื้นหลัง:

```csharp
TableCell cell11 = new TableCell(doc);
cell11.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Small text"));
cell11.BackgroundColor = Color.Coral;
```

## ขั้นตอนที่ 3: เริ่มต้น TableRow และผนวกเซลล์

เริ่มต้นวัตถุ TableRow และผนวกเซลล์ที่สร้างไว้ก่อนหน้านี้:

```csharp
TableRow row = new TableRow(doc);
row.AppendChildLast(cell11);
```

## ขั้นตอนที่ 4: สร้างตารางด้วยคอลัมน์ที่ระบุ

สร้างตารางที่มีคอลัมน์ที่ระบุและทำให้เส้นขอบมองเห็นได้:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn() { Width = 200 } }
};
table.AppendChildLast(row);
```

## ขั้นตอนที่ 5: สร้างองค์ประกอบเค้าร่างและหน้า

สร้างองค์ประกอบเค้าร่างและหน้า และผนวกตารางเข้ากับหน้า:

```csharp
OutlineElement oe = new OutlineElement(doc);
oe.AppendChildLast(table);

Outline o = new Outline(doc);
o.AppendChildLast(oe);

Page page = new Page(doc);
page.AppendChildLast(o);

doc.AppendChildLast(page);
```

## ขั้นตอนที่ 6: บันทึกเอกสาร

บันทึกเอกสารด้วยไดเร็กทอรีและชื่อไฟล์ที่ระบุ:

```csharp
doc.Save(Path.Combine("Your Document Directory", "SettingCellBackGroundColor.pdf"));
```

เมื่อทำตามขั้นตอนเหล่านี้ คุณจะตั้งค่าสีพื้นหลังของเซลล์ภายในตารางโดยใช้ Aspose.Note สำหรับ .NET ได้สำเร็จ

## บทสรุป

โดยสรุป Aspose.Note สำหรับ .NET มอบวิธีที่สะดวกและมีประสิทธิภาพในการจัดการคุณสมบัติของตาราง เช่น การตั้งค่าสีพื้นหลังของเซลล์ ด้วย API ที่ใช้งานง่ายและเอกสารประกอบที่ครอบคลุม คุณสามารถปรับปรุงการนำเสนอด้วยภาพเอกสารของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งสีพื้นหลังเพิ่มเติม เช่น การใช้การไล่ระดับสีหรือลวดลายได้หรือไม่

A1: Aspose.Note สำหรับ .NET รองรับสีทึบสำหรับพื้นหลังของเซลล์ อย่างไรก็ตาม คุณสามารถจำลองการไล่ระดับสีหรือลวดลายได้โดยใช้รูปภาพเป็นพื้นหลัง

### คำถามที่ 2: Aspose.Note สำหรับ .NET รองรับตัวเลือกการจัดรูปแบบตารางอื่นๆ หรือไม่

ตอบ 2: ใช่ Aspose.Note สำหรับ .NET มีตัวเลือกการจัดรูปแบบตารางที่หลากหลาย รวมถึงเส้นขอบเซลล์ การจัดตำแหน่งข้อความ และความกว้างของคอลัมน์

### คำถามที่ 3: เป็นไปได้ไหมที่จะเปลี่ยนสีพื้นหลังของเซลล์แบบไดนามิกตามเงื่อนไขบางประการ

คำตอบ 3: แน่นอน คุณสามารถแก้ไขคุณสมบัติของเซลล์โดยทางโปรแกรม รวมถึงสีพื้นหลัง ตามเงื่อนไขใดๆ ที่คุณกำหนดในตรรกะของแอปพลิเคชันของคุณ

### คำถามที่ 4: ฉันสามารถใช้ Aspose.Note สำหรับ .NET เพื่อทำงานกับตารางในรูปแบบเอกสารอื่นๆ เช่น Word หรือ Excel ได้หรือไม่

A4: Aspose.Note สำหรับ .NET กำหนดเป้าหมายรูปแบบไฟล์ OneNote โดยเฉพาะ สำหรับการทำงานกับตารางในเอกสาร Word หรือ Excel คุณจะต้องใช้ Aspose.Words หรือ Aspose.Cells ตามลำดับ

### คำถามที่ 5: ฉันจะค้นหาแหล่งข้อมูลเพิ่มเติมและการสนับสนุนสำหรับ Aspose.Note สำหรับ .NET ได้ที่ไหน

 A5: คุณสามารถสำรวจ[เอกสาร Aspose.Note](https://reference.aspose.com/note/net/) สำหรับการอ้างอิงและตัวอย่าง API โดยละเอียด นอกจากนี้ คุณสามารถขอความช่วยเหลือจากชุมชน Aspose ได้ที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
