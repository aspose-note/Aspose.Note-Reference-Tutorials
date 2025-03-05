---
title: เขียนตารางด้วย Aspose.Note
linktitle: เขียนตารางด้วย Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีการเขียนตารางที่มีโครงสร้างด้วยเนื้อหา Rich Text โดยใช้ Aspose.Note สำหรับ .NET ปรับปรุงการจัดระเบียบเอกสารและความสามารถในการอ่านได้อย่างง่ายดาย
type: docs
weight: 11
url: /th/net/table-manipulation/compose-tables/
---
## การแนะนำ

ตารางเป็นองค์ประกอบพื้นฐานของเอกสาร ช่วยให้สามารถนำเสนอข้อมูลอย่างมีโครงสร้างได้ Aspose.Note สำหรับ .NET มีเครื่องมือที่มีประสิทธิภาพในการเขียนตารางได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการสร้างตารางที่มีเนื้อหา Rich Text โดยใช้ Aspose.Note

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเจาะลึกการจัดองค์ประกอบตารางด้วย Aspose.Note สำหรับ .NET ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. การตั้งค่าสภาพแวดล้อม: ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนาที่เหมาะสมที่ตั้งค่าด้วย .NET Framework หรือ .NET Core
2.  การติดตั้ง: ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ .NET จาก[เว็บไซต์](https://releases.aspose.com/note/net/).
3. ความรู้พื้นฐาน: ทำความคุ้นเคยกับแนวคิดพื้นฐานของการเขียนโปรแกรม C# และการจัดการเอกสาร

## นำเข้าเนมสเปซ

ก่อนที่คุณจะเริ่มเขียนตาราง ตรวจสอบให้แน่ใจว่าคุณได้นำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

เรามาแยกย่อยตัวอย่างที่ให้ไว้เป็นขั้นตอนที่สามารถจัดการได้:

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

ก่อนที่จะเขียนตาราง ให้กำหนดไดเร็กทอรีที่จะบันทึกเอกสาร

```csharp
string dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: สร้างข้อความส่วนหัว

กำหนดข้อความส่วนหัวด้วยสไตล์เฉพาะ เช่น ขนาดตัวอักษรและตัวหนา

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## ขั้นตอนที่ 3: สร้างหน้าและโครงร่าง

เริ่มต้นหน้าและโครงร่างเพื่อจัดโครงสร้างเนื้อหา

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## ขั้นตอนที่ 4: เพิ่มข้อความสรุป

รวมข้อความสรุปไว้หน้าตาราง

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## ขั้นตอนที่ 5: สร้างตาราง

เริ่มต้นตารางเพื่อจัดระเบียบข้อมูลเป็นแถวและคอลัมน์

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## ขั้นตอนที่ 6: เพิ่มแถวส่วนหัว

เติมตารางด้วยแถวส่วนหัวที่มีชื่อคอลัมน์

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## ขั้นตอนที่ 7: เพิ่มแถวว่าง

แทรกแถวว่างเพื่อเตรียมการแทรกข้อมูล

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## ขั้นตอนที่ 8: เพิ่มข้อมูลการติดต่อ

เติมคอลัมน์ 'ผู้ติดต่อ' ด้วยเนื้อหาเทมเพลต

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## ขั้นตอนที่ 9: บันทึกเอกสาร

บันทึกเอกสารตารางที่เรียบเรียง

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## ขั้นตอนที่ 10: การยืนยัน

ยืนยันการจัดองค์ประกอบเอกสารสำเร็จ

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจวิธีการเขียนตารางที่มีเนื้อหา Rich Text โดยใช้ Aspose.Note สำหรับ .NET ด้วยการทำตามคำแนะนำทีละขั้นตอนเหล่านี้ คุณจะสามารถสร้างตารางที่มีโครงสร้างภายในเอกสารของคุณได้อย่างมีประสิทธิภาพ เพิ่มความสามารถในการอ่านและการจัดระเบียบ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งสไตล์ขององค์ประกอบตารางได้หรือไม่
   
A1: ได้ คุณสามารถปรับแต่งลักษณะต่างๆ เช่น ขนาดตัวอักษร สี และการจัดตำแหน่งให้เหมาะกับความต้องการของคุณได้

### คำถามที่ 2: Aspose.Note เข้ากันได้กับไลบรารี .NET อื่นๆ หรือไม่
   
คำตอบ 2: Aspose.Note ทำงานร่วมกับไลบรารี .NET อื่นๆ ได้อย่างราบรื่น โดยให้ความยืดหยุ่นอย่างมากในการจัดการเอกสาร

### คำถามที่ 3: Aspose.Note รองรับการส่งออกตารางเป็นรูปแบบที่แตกต่างกันหรือไม่
   
ตอบ 3: แน่นอน Aspose.Note ช่วยให้คุณสามารถส่งออกตารางเป็นรูปแบบต่างๆ รวมถึง PDF, DOCX และ HTML

### คำถามที่ 4: ฉันสามารถเติมข้อมูลในตารางแบบไดนามิกด้วยข้อมูลจากแหล่งภายนอกได้หรือไม่
   
A4: ได้ คุณสามารถเติมข้อมูลตารางแบบไดนามิกได้โดยการดึงข้อมูลจากฐานข้อมูล API หรืออินพุตของผู้ใช้

### คำถามที่ 5: มีการสนับสนุนทางเทคนิคสำหรับผู้ใช้ Aspose.Note หรือไม่
   
A5: ใช่ Aspose ให้การสนับสนุนด้านเทคนิคอย่างครอบคลุมผ่านฟอรัมและช่องทางการสนับสนุนเฉพาะ