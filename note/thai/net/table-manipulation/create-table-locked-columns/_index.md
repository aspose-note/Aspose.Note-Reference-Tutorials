---
title: สร้างตารางที่มีคอลัมน์ที่ถูกล็อคโดยใช้ Aspose.Note
linktitle: สร้างตารางที่มีคอลัมน์ที่ถูกล็อคโดยใช้ Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีสร้างตารางที่มีคอลัมน์ที่ถูกล็อคโดยใช้ Aspose.Note สำหรับ .NET คำแนะนำทีละขั้นตอนสำหรับงานประมวลผลเอกสารที่มีประสิทธิภาพ
weight: 12
url: /th/net/table-manipulation/create-table-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างตารางที่มีคอลัมน์ที่ถูกล็อคโดยใช้ Aspose.Note

## การแนะนำ

การสร้างตารางที่มีคอลัมน์ที่ถูกล็อกเป็นข้อกำหนดทั่วไปในแอปพลิเคชันการประมวลผลเอกสาร Aspose.Note สำหรับ .NET มีเครื่องมือที่มีประสิทธิภาพเพื่อให้งานนี้สำเร็จได้อย่างมีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการสร้างตารางที่มีคอลัมน์ที่ถูกล็อคทีละขั้นตอนโดยใช้ Aspose.Note สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความเข้าใจพื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C#
- ติดตั้ง Visual Studio บนระบบของคุณแล้ว
-  ติดตั้ง Aspose.Note สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/net/).
- ความคุ้นเคยกับแนวคิดการจัดการเอกสาร

## นำเข้าเนมสเปซ

ขั้นแรก คุณต้องนำเข้าเนมสเปซที่จำเป็นไปยังโปรเจ็กต์ของคุณ:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## ขั้นตอนที่ 1: เริ่มต้นวัตถุเอกสาร

เริ่มต้นด้วยการสร้างวัตถุของคลาสเอกสาร:

```csharp
Document doc = new Document();
```

## ขั้นตอนที่ 2: เริ่มต้นวัตถุหน้า

เริ่มต้นวัตถุคลาสหน้า:

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## ขั้นตอนที่ 3: เริ่มต้นวัตถุ TableRow

สร้างวัตถุ TableRow สำหรับตาราง:

```csharp
TableRow row1 = new TableRow(doc);
TableRow row2 = new TableRow(doc);
```

## ขั้นตอนที่ 4: เริ่มต้นวัตถุ TableCell

สร้างวัตถุ TableCell และตั้งค่าเนื้อหาข้อความสำหรับแต่ละเซลล์:

```csharp
TableCell cell11 = new TableCell(doc);
cell11.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Small text"));

TableCell cell21 = new TableCell(doc);
cell21.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Long text with several words and spaces."));
```

## ขั้นตอนที่ 5: เริ่มต้นวัตถุตาราง

เริ่มต้นวัตถุคลาสตารางและตั้งค่าคุณสมบัติเช่นความกว้างของคอลัมน์และความกว้างที่ล็อค:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70, LockedWidth = true } }
};
```

## ขั้นตอนที่ 6: เพิ่มแถวลงในตาราง

เพิ่มแถวที่เตรียมใช้งานแล้วลงในตาราง:

```csharp
table.AppendChildLast(row1);
table.AppendChildLast(row2);
```

## ขั้นตอนที่ 7: เพิ่มตารางลงในโครงร่าง

เพิ่มโหนดตารางให้กับ OutlineElement:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
```

## ขั้นตอนที่ 8: เพิ่มโครงร่างลงในหน้า

เพิ่มโหนดเค้าร่างในหน้า:

```csharp
page.AppendChildLast(outline);
```

## ขั้นตอนที่ 9: บันทึกเอกสาร

บันทึกเอกสาร:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable with locked columns created successfully.\nFile saved at " + dataDir);
```

หลังจากทำตามขั้นตอนเหล่านี้ คุณจะสร้างตารางที่มีคอลัมน์ที่ถูกล็อกได้สำเร็จโดยใช้ Aspose.Note สำหรับ .NET

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีสร้างตารางที่มีคอลัมน์ที่ถูกล็อคโดยใช้ Aspose.Note สำหรับ .NET ด้วยการทำตามขั้นตอนเหล่านี้ คุณสามารถจัดการตารางภายในเอกสารของคุณให้ตรงตามความต้องการเฉพาะของคุณได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของตารางเพิ่มเติมได้หรือไม่

ตอบ 1: ได้ คุณสามารถปรับแต่งลักษณะต่างๆ ของตารางได้ เช่น เส้นขอบ การจัดรูปแบบเซลล์ และอื่นๆ โดยใช้คุณสมบัติที่ Aspose.Note สำหรับ .NET มอบให้

### คำถามที่ 2: Aspose.Note สำหรับ .NET เหมาะสำหรับงานประมวลผลเอกสารขนาดใหญ่หรือไม่

A2: แน่นอน! Aspose.Note สำหรับ .NET ได้รับการออกแบบมาเพื่อจัดการกับงานการประมวลผลเอกสารขนาดใหญ่อย่างมีประสิทธิภาพ โดยให้ประสิทธิภาพและความน่าเชื่อถือสูง

### คำถามที่ 3: ฉันสามารถรวม Aspose.Note สำหรับ .NET เข้ากับเฟรมเวิร์ก .NET อื่นๆ ได้หรือไม่

ตอบ 3: ใช่ Aspose.Note สำหรับ .NET ทำงานร่วมกับเฟรมเวิร์ก .NET อื่นๆ ได้อย่างราบรื่น ทำให้ง่ายต่อการรวมความสามารถในการประมวลผลเอกสารเข้ากับแอปพลิเคชันของคุณ

### คำถามที่ 4: มีการสนับสนุนด้านเทคนิคสำหรับ Aspose.Note สำหรับ .NET หรือไม่

A4: ใช่ คุณสามารถเข้าถึงการสนับสนุนทางเทคนิคผ่านทาง[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28) ซึ่งมีผู้เชี่ยวชาญคอยช่วยเหลือคุณในทุกคำถามหรือปัญหาที่คุณอาจพบ

### คำถามที่ 5: ฉันสามารถลองใช้ Aspose.Note สำหรับ .NET ก่อนซื้อได้หรือไม่

 A5: ได้ คุณสามารถดาวน์โหลด Aspose.Note สำหรับ .NET เวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/) เพื่อประเมินคุณสมบัติและความเข้ากันได้กับความต้องการของคุณ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
