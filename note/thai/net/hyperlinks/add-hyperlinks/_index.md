---
date: 2026-04-03
description: เรียนรู้วิธีเพิ่มไฮเปอร์ลิงก์ในเอกสาร Aspose.Note ด้วย Aspose.Note for
  .NET ปรับแต่งลักษณะของไฮเปอร์ลิงก์ และแทรกหลายไฮเปอร์ลิงก์เพื่อทำให้ไฟล์ OneNote
  มีความสมบูรณ์ยิ่งขึ้น
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: วิธีเพิ่มไฮเปอร์ลิงก์ในเอกสาร Aspose.Note
second_title: Aspose.Note .NET API
title: วิธีเพิ่มไฮเปอร์ลิงก์ในเอกสาร Aspose.Note
url: /th/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มไฮเปอร์ลิงก์ในเอกสาร Aspose.Note

## บทนำ

ในบทแนะนำนี้คุณจะได้ค้นพบ **วิธีเพิ่มไฮเปอร์ลิงก์** ไปยังข้อความภายในเอกสาร Aspose.Note ด้วย .NET API การเพิ่มไฮเปอร์ลิงก์จะทำให้โน้ตที่คงที่กลายเป็นเนื้อหาแบบโต้ตอบและคลิกได้—เหมาะสำหรับการเชื่อมโยงไปยังแหล่งเว็บ, ส่วนภายใน, หรือไฟล์ภายนอก เราจะเดินผ่านแต่ละขั้นตอน, แสดงให้คุณเห็นวิธี **ปรับแต่งลักษณะของไฮเปอร์ลิงก์**, และอธิบายวิธี **แทรกหลายไฮเปอร์ลิงก์** เมื่อคุณต้องการหน้า OneNote ที่มีความหลากหลายมากขึ้น.

## คำตอบสั้น
- **คลาสหลักสำหรับสร้างไฟล์ OneNote คืออะไร?** `Document` จาก Aspose.Note.
- **คุณสมบัติใดทำให้ข้อความทำงานเป็นไฮเปอร์ลิงก์?** `IsHyperlink = true` บน `TextStyle`.
- **ฉันสามารถเชื่อมโยงไปยังเว็บไซต์ภายนอกได้หรือไม่?** ได้, ตั้งค่า `HyperlinkAddress` เป็น URL เช่น `https://www.google.com`.
- **ต้องการใบอนุญาตสำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีใบอนุญาต Aspose.Note ที่ถูกต้องสำหรับการสร้างที่ไม่ใช่การประเมินผล.
- **เวอร์ชัน .NET ที่รองรับคืออะไร?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.

## “วิธีเพิ่มไฮเปอร์ลิงก์” ใน Aspose.Note คืออะไร?
การเพิ่มไฮเปอร์ลิงก์หมายถึงการแนบ URL ไปยังข้อความบางส่วนเพื่อให้เมื่อผู้ใช้คลิกภายใน OneNote, แหล่งที่เชื่อมโยงจะเปิดในเบราว์เซอร์หรือแอปพลิเคชันอื่น Aspose.Note เปิดเผยแฟล็ก `TextStyle.IsHyperlink` และคุณสมบัติ `HyperlinkAddress` เพื่อทำให้สิ่งนี้เป็นไปได้โดยโปรแกรม.

## ทำไมต้องเพิ่มไฮเปอร์ลิงก์ในเอกสาร OneNote?
- **การนำทางที่ดีขึ้น:** กระโดดตรงไปยังหน้าเว็บหรือส่วนที่เกี่ยวข้อง.
- **เอกสารที่ปรับปรุง:** ให้แหล่งอ้างอิง, บทแนะนำ, หรือไฟล์ต้นฉบับโดยไม่ต้องออกจากโน้ต.
- **รูปลักษณ์มืออาชีพ:** สีและสไตล์ที่ปรับแต่งได้ทำให้ไฮเปอร์ลิงก์ผสมผสานกับการออกแบบเอกสารของคุณ.

## ข้อกำหนดเบื้องต้น

1. ความรู้พื้นฐานของ C# และ Visual Studio.
2. ไลบรารี Aspose.Note สำหรับ .NET ติดตั้งแล้ว – ดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/note/net/).
3. ความเข้าใจโครงสร้างเอกสาร Aspose.Note (หน้า, โครงร่าง, ข้อความที่มีรูปแบบ).

## นำเข้า Namespaces

ก่อนแรก, นำเข้า namespaces ที่ให้คุณเข้าถึงคลาสหลักของ Aspose.Note และประเภทพื้นฐานของ .NET.

```csharp
using System;
using System.Drawing;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: สร้างอ็อบเจ็กต์ Document ใหม่

สร้างอินสแตนซ์ของ `Document` ซึ่งจะเก็บหน้าทั้งหมดและเนื้อหาของคุณ.

```csharp
Document doc = new Document();
```

### ขั้นตอนที่ 2: กำหนดสไตล์ข้อความ (รวมถึงสไตล์ไฮเปอร์ลิงก์)

สร้างอ็อบเจ็กต์ `TextStyle` สองตัว – หนึ่งสำหรับข้อความปกติและหนึ่งสำหรับไฮเปอร์ลิงก์.  
ที่นี่เรายัง **ปรับแต่งลักษณะของไฮเปอร์ลิงก์** โดยตั้งค่าสีฟอนต์.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **เคล็ดลับมืออาชีพ:** เพื่อแทรก **หลายไฮเปอร์ลิงก์**, กำหนดอ็อบเจ็กต์ `TextStyle` เพิ่มเติมโดยมีค่า `HyperlinkAddress` ที่แตกต่างกันและใช้ซ้ำในส่วน `RichText` ต่อไป.

### ขั้นตอนที่ 3: สร้างอ็อบเจ็กต์ RichText

สร้างย่อหน้าที่ผสมข้อความปกติและไฮเปอร์ลิงก์. เมธอด `Append` ช่วยให้คุณต่อส่วนข้อความที่มีสไตล์ต่อกัน.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### ขั้นตอนที่ 4: สร้าง Outline และ Outline Element

Outline ทำหน้าที่เหมือนคอนเทนเนอร์สำหรับองค์ประกอบภาพบนหน้า. ตั้งค่าขนาดและตำแหน่งตามต้องการ.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### ขั้นตอนที่ 5: เพิ่มองค์ประกอบลงในหน้า

ไฟล์ OneNote ทุกไฟล์ประกอบด้วยหลายหน้า. เราจะสร้าง `Title` และ `Page`, จากนั้นแนบ outline.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### ขั้นตอนที่ 6: บันทึกเอกสาร

เลือกโฟลเดอร์, สร้างชื่อไฟล์เต็ม, และเรียก `Save`. ไฟล์ผลลัพธ์จะเป็นไฟล์ OneNote `.one` ที่ถูกต้องซึ่งมีไฮเปอร์ลิงก์ของคุณ.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| ไฮเปอร์ลิงก์ไม่เปิด | ตรวจสอบให้แน่ใจว่า `HyperlinkAddress` มีโปรโตคอล (`http://` หรือ `https://`). |
| สีข้อความไม่ถูกนำไปใช้ | ตั้งค่า `FontColor` บน `TextStyle` ที่ใช้สำหรับไฮเปอร์ลิงก์. |
| ต้องการหลายลิงก์ในหนึ่งหน้า | สร้างอ็อบเจ็กต์ `TextStyle` หลายตัว, แต่ละตัวมี `HyperlinkAddress` ของตนเอง, แล้วต่อเข้ากับอ็อบเจ็กต์ `RichText` เดียวกันหรือแตกต่างกัน. |
| เอกสารไม่สามารถโหลดใน OneNote | ตรวจสอบว่าคุณใช้เวอร์ชัน OneNote ที่รองรับ (2010+). |

## คำถามที่พบบ่อย

**Q: ฉันสามารถเพิ่มหลายไฮเปอร์ลิงก์ภายในเอกสารเดียวกันโดยใช้ Aspose.Note ได้หรือไม่?**  
A: ได้, เพียงสร้างอินสแตนซ์ `TextStyle` เพิ่มเติมที่มีค่า `HyperlinkAddress` ต่างกันและต่อเข้ากับอ็อบเจ็กต์ `RichText` ของคุณ.

**Q: ฉันจะปรับแต่งลักษณะของไฮเปอร์ลิงก์ได้อย่างไร?**  
A: ใช้คุณสมบัติเช่น `FontColor`, `FontName`, และ `FontSize` บน `TextStyle` ที่มี `IsHyperlink = true`. สิ่งนี้ทำให้คุณสามารถปรับให้ตรงกับแบรนด์ของเอกสารของคุณ.

**Q: Aspose.Note รองรับไฮเปอร์ลิงก์ไปยังเว็บไซต์ภายนอกหรือไม่?**  
A: แน่นอน. ตั้งค่า `HyperlinkAddress` เป็น URL ที่ถูกต้องใด ๆ (รวมถึง `http://` หรือ `https://`) เพื่อเชื่อมโยงออกจากไฟล์ OneNote.

**Q: สามารถสร้างไฟล์ OneNote เดียวที่มีหลายไฮเปอร์ลิงก์ได้หรือไม่?**  
A: ได้. โดยการต่อเนื่องการต่อ `RichText` ที่มีสไตล์ต่าง ๆ พร้อมที่อยู่ไฮเปอร์ลิงก์ที่แตกต่างกัน, คุณสามารถ **สร้างคอลเลกชันไฮเปอร์ลิงก์ในไฟล์เดียว**.

**Q: Aspose.Note เข้ากันได้กับเวอร์ชัน OneNote ล่าสุดหรือไม่?**  
A: ไลบรารีทำงานกับ OneNote 2010 ขึ้นไป, รวมถึงเวอร์ชัน Windows 10 UWP.

---

**อัปเดตล่าสุด:** 2026-04-03  
**ทดสอบด้วย:** Aspose.Note for .NET 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}