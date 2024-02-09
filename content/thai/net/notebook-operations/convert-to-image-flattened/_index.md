---
title: แปลงโน้ตบุ๊กเป็นรูปภาพ (แบน) ใน Aspose Note .NET
linktitle: แปลงโน้ตบุ๊กเป็นรูปภาพ (แบน) ใน Aspose Note .NET
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีแปลงสมุดบันทึก OneNote เป็นรูปภาพที่แบนราบโดยใช้ Aspose.Note สำหรับ .NET คำแนะนำทีละขั้นตอนเพื่อการผสานรวมที่ราบรื่น
type: docs
weight: 12
url: /th/net/notebook-operations/convert-to-image-flattened/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะเรียนรู้วิธีใช้ Aspose.Note สำหรับ .NET เพื่อแปลงสมุดบันทึกเป็นรูปภาพที่แบนราบ เราจะแบ่งกระบวนการออกเป็นขั้นตอนง่ายๆ เพื่อช่วยให้คุณเข้าใจและนำไปปฏิบัติได้อย่างมีประสิทธิภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1.  Aspose.Note สำหรับ .NET: หากคุณยังไม่ได้ดาวน์โหลด ให้ดาวน์โหลดและติดตั้ง Aspose.Note สำหรับ .NET จาก[ที่นี่](https://releases.aspose.com/note/net/).
2. สภาพแวดล้อมการพัฒนา: ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนาที่เหมาะสมสำหรับการพัฒนา .NET
3. สมุดบันทึก OneNote: เตรียมสมุดบันทึก OneNote ที่คุณต้องการแปลงเป็นรูปภาพ

## นำเข้าเนมสเปซ

ก่อนที่จะเริ่มกระบวนการแปลง คุณต้องนำเข้าเนมสเปซที่จำเป็นในโค้ดของคุณ:

```csharp
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

ตอนนี้ มาดูคำแนะนำทีละขั้นตอนในการแปลงสมุดบันทึกให้เป็นรูปภาพที่แบนราบโดยใช้ Aspose.Note สำหรับ .NET

## ขั้นตอนที่ 1: โหลดโน้ตบุ๊ก

ขั้นแรก ให้โหลดสมุดบันทึก OneNote ที่คุณต้องการแปลงเป็นแอปพลิเคชันของคุณ

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";

// โหลดสมุดบันทึก OneNote
var notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการบันทึก

กำหนดตัวเลือกการบันทึกสำหรับโน้ตบุ๊ก รวมถึงรูปแบบรูปภาพและความละเอียด

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
notebookSaveOptions.Flatten = true;
```

## ขั้นตอนที่ 3: บันทึกสมุดบันทึกเป็นรูปภาพ

ตอนนี้ ให้บันทึกสมุดบันทึกเป็นรูปภาพที่แบนราบโดยใช้ตัวเลือกการบันทึกที่กำหนดไว้

```csharp
dataDir = dataDir + "ConvertToImageAsFlattenedNotebook_out.png";

// บันทึกสมุดบันทึก
notebook.Save(dataDir, notebookSaveOptions);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีแปลงสมุดบันทึกให้เป็นรูปภาพที่แบนราบโดยใช้ Aspose.Note สำหรับ .NET ด้วยการทำตามคำแนะนำทีละขั้นตอน คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สำหรับ .NET สามารถจัดการสมุดบันทึกที่ซับซ้อนได้หรือไม่

ตอบ 1: ใช่ Aspose.Note สำหรับ .NET สามารถจัดการโน้ตบุ๊กที่ซับซ้อนได้อย่างมีประสิทธิภาพ

### คำถามที่ 2: Aspose.Note สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A2: ได้ คุณสามารถดาวน์โหลดรุ่นทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: Aspose ให้การสนับสนุนผลิตภัณฑ์ของตนหรือไม่

 A3: ได้ คุณสามารถรับการสนับสนุนจากชุมชน Aspose ได้[ที่นี่](https://forum.aspose.com/c/note/28).

### คำถามที่ 4: ฉันสามารถซื้อใบอนุญาตชั่วคราวสำหรับ Aspose.Note สำหรับ .NET ได้หรือไม่

 A4: ได้ คุณสามารถซื้อใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันจะหาเอกสารสำหรับ Aspose.Note สำหรับ .NET ได้ที่ไหน

 A5: คุณสามารถค้นหาเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/note/net/).