---
date: 2026-04-06
description: เรียนรู้วิธีสร้างเอกสาร OneNote และแทรกรูปภาพโดยใช้โค้ดด้วย Aspose.Note
  สำหรับ .NET ทำตามขั้นตอนง่ายๆ เพื่อเพิ่มรูปภาพ ตั้งค่าการจัดแนวและอื่นๆ อีกมากมาย
keywords:
- create onenote document
- how to insert image
- insert image onenote
- set image alignment
- multiple images onenote
linktitle: สร้างเอกสารและแทรกรูปภาพใน Aspose.Note
second_title: Aspose.Note .NET API
title: สร้างเอกสาร OneNote และแทรกรูปภาพโดยใช้ Aspose.Note
url: /th/net/images/build-doc-insert-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างเอกสาร OneNote และแทรกรูปภาพโดยใช้ Aspose.Note

## บทนำ

ในบทเรียนนี้ คุณจะ **สร้างเอกสาร OneNote** และเรียนรู้ **วิธีแทรกรูปภาพ** ลงในเอกสารโดยใช้ Aspose.Note สำหรับ .NET Aspose.Note ให้คุณควบคุมไฟล์ OneNote ได้อย่างเต็มที่ ทำให้การเพิ่มเนื้อหาที่หลากหลาย เช่น รูปภาพ ตาราง และการจัดวางแบบกำหนดเอง ผ่านโปรแกรมเป็นเรื่องง่าย

## คำตอบสั้น
- **วัตถุประสงค์หลักคืออะไร?** เพื่อสร้างเอกสาร OneNote และแทรกรูปภาพพร้อมการจัดแนวที่กำหนดเอง  
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.Note สำหรับ .NET (ดาวน์โหลด [ที่นี่](https://releases.aspose.com/note/net/))  
- **ฉันต้องการไลเซนส์หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีไลเซนส์แบบชำระเงินสำหรับการใช้งานในผลิตภัณฑ์  
- **ฉันสามารถเพิ่มหลายรูปภาพได้หรือไม่?** ได้ – ทำซ้ำขั้นตอนการแทรกสำหรับแต่ละรูปภาพ (ดูเคล็ดลับ “multiple images onenote”)  
- **การแปลงเป็น PDF รองรับหรือไม่?** แน่นอน – คุณสามารถแปลงเอกสาร OneNote เป็น PDF ภายหลังโดยใช้เมธอด `Save` ของ Aspose.Note พร้อมรูปแบบ PDF

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้ครบถ้วน:

1. **Visual Studio** – IDE ที่ครบคุณสมบัติสำหรับการพัฒนา .NET  
2. **Aspose.Note for .NET** – ดาวน์โหลดและติดตั้งไลบรารีจากเว็บไซต์อย่างเป็นทางการ  
3. **ความเข้าใจพื้นฐานของ C#** – ความคุ้นเคยกับไวยากรณ์ C# จะช่วยให้คุณตามตัวอย่างโค้ดได้ง่ายขึ้น

## นำเข้า Namespaces

เราจะเริ่มโดยนำเข้า Namespaces ที่จำเป็นเข้าสู่โปรเจกต์ C# ของคุณ Namespaces เหล่านี้ประกอบด้วยคลาสและเมธอดที่เราจะใช้ในการจัดการเอกสาร

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

ต่อไปนี้เป็นการแบ่งกระบวนการสร้างเอกสารและแทรกรูปภาพเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: สร้าง Document Object

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document();
```

บรรทัดนี้เป็นการสร้างอินสแตนซ์ใหม่ของคลาส `Document` ซึ่งเป็นตัวแทนของเอกสาร OneNote

## ขั้นตอนที่ 2: เริ่มต้น Page Object

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

ที่นี่เราจะสร้างอินสแตนซ์ใหม่ของคลาส `Page` ซึ่งเป็นหน้าหนึ่งในเอกสาร OneNote

## ขั้นตอนที่ 3: เริ่มต้น Outline Object

```csharp
Outline outline = new Outline(doc);
```

คลาส `Outline` แสดงถึงโหนดโครงร่างในลำดับชั้นของเอกสาร เราจะสร้างออบเจ็กต์ Outline ใหม่เพื่อจัดโครงสร้างเอกสาร

## ขั้นตอนที่ 4: เริ่มต้น OutlineElement Object

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

`OutlineElement` คือองค์ประกอบภายในโครงร่าง ที่นี่เราจะสร้าง OutlineElement ใหม่เพื่อเพิ่มเนื้อหาในเอกสาร

## ขั้นตอนที่ 5: โหลดรูปภาพ

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg");
```

เราจะโหลดไฟล์รูปภาพจากพาธที่ระบุโดยใช้คอนสตรัคเตอร์ของคลาส `Image`

## ขั้นตอนที่ 6: ตั้งค่าการจัดแนวรูปภาพ

```csharp
image.Alignment = HorizontalAlignment.Right;
```

บรรทัดนี้ตั้งค่า **การจัดแนวรูปภาพ** ไปทางด้านขวาของหน้า คุณสามารถเลือก `Left` หรือ `Center` ตามความต้องการของการจัดวางได้เช่นกัน

## ขั้นตอนที่ 7: เพิ่มรูปภาพไปยัง Outline Element

```csharp
outlineElem.AppendChildLast(image);
```

ที่นี่เราจะเพิ่มรูปภาพลงใน Outline Element เพื่อวางไว้ในโครงสร้างของเอกสาร

## ขั้นตอนที่ 8: เพิ่ม Outline Element ไปยัง Outline

```csharp
outline.AppendChildLast(outlineElem);
```

เราจะเพิ่ม Outline Element พร้อมรูปภาพที่แทรกเข้าไปในโครงสร้าง Outline ของเอกสาร

## ขั้นตอนที่ 9: เพิ่ม Outline ไปยัง Page

```csharp
page.AppendChildLast(outline);
```

Outline ที่มีรูปภาพจะถูกเพิ่มเข้าไปในโครงสร้างของหน้า (Page)

## ขั้นตอนที่ 10: เพิ่ม Page ไปยัง Document

```csharp
doc.AppendChildLast(page);
```

สุดท้าย เราจะเพิ่มหน้า (Page) ที่มีเนื้อหาครบถ้วนเข้าไปในเอกสาร (Document)

## ขั้นตอนที่ 11: บันทึก Document

```csharp
dataDir = dataDir + "BuildDocAndInsertImage_out.one";
doc.Save(dataDir);
```

บรรทัดนี้บันทึกเอกสาร OneNote ที่แก้ไขแล้วไปยังตำแหน่งที่ระบุ คุณสามารถต่อไป **แปลง OneNote เป็น PDF** ได้โดยเรียก `doc.Save("output.pdf")`

## ทำไมเรื่องนี้ถึงสำคัญ

- **Automation** – การสร้างเอกสาร OneNote ด้วยโปรแกรมช่วยประหยัดเวลาเมื่อเทียบกับการแก้ไขด้วยมือ  
- **Consistency** – การใช้โค้ดทำให้เอกสารแต่ละไฟล์มีรูปแบบและกฎการจัดสไตล์เดียวกัน  
- **Scalability** – วิธีเดียวกันสามารถขยายเพื่อแทรก **multiple images onenote** เอกสารหรือสร้างรายงานเป็นจำนวนมาก

## ข้อผิดพลาดทั่วไปและเคล็ดลับ

- **ปัญหาเส้นทาง** – ตรวจสอบให้แน่ใจว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้อง; หากไม่เช่นนั้นการโหลดรูปภาพจะล้มเหลว  
- **ขนาดรูปภาพ** – รูปภาพขนาดใหญ่สามารถเพิ่มขนาดไฟล์อย่างมาก; ควรปรับขนาดก่อนแทรก  
- **หลายรูปภาพ** – เพื่อเพิ่มรูปภาพมากกว่าหนึ่งภาพ ให้ทำซ้ำขั้นตอน 5‑7 สำหรับแต่ละรูปและเพิ่มแต่ละรูปไปยัง `OutlineElement` เดียวกันหรือแตกต่างกัน

## คำถามที่พบบ่อย

### Q1: ฉันสามารถแทรกหลายรูปภาพลงในเอกสารเดียวโดยใช้ Aspose.Note for .NET ได้หรือไม่?

A1: แน่นอน! คุณสามารถแทรกรูปภาพได้ตามจำนวนที่ต้องการโดยทำตามขั้นตอนการแทรกเดียวกันสำหรับแต่ละรูป

### Q2: Aspose.Note รองรับรูปแบบไฟล์อื่นนอกจาก OneNote หรือไม่?

A2: ใช่, Aspose.Note มีการสนับสนุนรูปแบบไฟล์หลายประเภทอย่างกว้างขวาง รวมถึง PDF, DOCX, HTML และอื่น ๆ

### Q3: Aspose.Note เหมาะสำหรับโซลูชันการจัดการเอกสารระดับองค์กรหรือไม่?

A3: แน่นอน! Aspose.Note มีคุณลักษณะที่แข็งแกร่งและประสิทธิภาพยอดเยี่ยม ทำให้เป็นตัวเลือกที่เหมาะสำหรับการจัดการเอกสารระดับองค์กร

### Q4: ฉันสามารถปรับแต่งลักษณะของรูปภาพที่แทรกในเอกสารได้หรือไม่?

A4: ใช่, Aspose.Note มีตัวเลือกครบถ้วนสำหรับการปรับแต่งลักษณะของรูปภาพ รวมถึงการจัดแนว, ขนาด, และการหมุน

### Q5: ฉันจะหาแหล่งข้อมูลและการสนับสนุนเพิ่มเติมสำหรับ Aspose.Note for .NET ได้จากที่ไหน?

A5: คุณสามารถสำรวจเอกสาร Aspose.Note ได้ [ที่นี่](https://reference.aspose.com/note/net/) และขอความช่วยเหลือจากฟอรั่มชุมชน Aspose [ที่นี่](https://forum.aspose.com/c/note/28/)

---

**Last Updated:** 2026-04-06  
**Tested With:** Aspose.Note 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}