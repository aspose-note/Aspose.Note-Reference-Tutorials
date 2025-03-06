---
title: บันทึกเป็น PDF ใน Aspose.Note
linktitle: บันทึกเป็น PDF ใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีบันทึกเอกสาร Microsoft OneNote เป็นรูปแบบ PDF โดยใช้ Aspose.Note สำหรับ .NET บทช่วยสอนทีละขั้นตอนพร้อมตัวอย่างโค้ดสำหรับเค้าโครงหน้า Letter และ A4
weight: 26
url: /th/net/loading-and-saving-operations/save-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกเป็น PDF ใน Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีบันทึกเอกสารเป็นรูปแบบ PDF โดยใช้ Aspose.Note สำหรับ .NET Aspose.Note เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม เราจะครอบคลุมข้อกำหนดเบื้องต้น นำเข้าเนมสเปซ และให้คำแนะนำทีละขั้นตอนสำหรับการบันทึกเอกสารเป็น PDF ในเค้าโครงหน้าต่างๆ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ติดตั้ง Visual Studio บนระบบของคุณแล้ว
-  Aspose.Note สำหรับไลบรารี .NET ที่ดาวน์โหลดและติดตั้ง คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/net/).
- ความรู้พื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C#

## นำเข้าเนมสเปซ

ขั้นแรก เรามานำเข้าเนมสเปซที่จำเป็นไปยังโค้ด C# ของเรา:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

ตอนนี้เราได้ครอบคลุมข้อกำหนดเบื้องต้นและนำเข้าเนมสเปซแล้ว เรามาดำเนินการบันทึกเอกสารเป็น PDF ในเค้าโครงหน้าต่างๆ กัน

## ขั้นตอนที่ 1: บันทึกเป็น PDF โดยใช้การตั้งค่าหน้าจดหมาย


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    string dataDir = "Your Document Directory";

    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // บันทึกเอกสาร
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### คำอธิบาย:

- เราโหลดเอกสาร OneNote ลงใน Aspose.Note
- กำหนดเส้นทางปลายทางสำหรับไฟล์ PDF ที่บันทึกไว้
-  บันทึกเอกสารเป็น PDF โดยใช้`PdfSaveOptions` กับ`PageSettings` ตั้งค่าให้`Letter`.

## ขั้นตอนที่ 2: บันทึกเป็น PDF โดยใช้การตั้งค่าหน้า A4 โดยไม่มีขีดจำกัดความสูง

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    string dataDir = "Your Document Directory";

    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // บันทึกเอกสาร
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### คำอธิบาย:

- เช่นเดียวกับขั้นตอนก่อนหน้า เราโหลดเอกสาร OneNote ลงใน Aspose.Note
- กำหนดเส้นทางปลายทางสำหรับไฟล์ PDF ที่บันทึกไว้
-  บันทึกเอกสารเป็น PDF โดยใช้`PdfSaveOptions` กับ`PageSettings` ตั้งค่าให้`A4NoHeightLimit`.

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีบันทึกเอกสารเป็นรูปแบบ PDF โดยใช้ Aspose.Note สำหรับ .NET เราครอบคลุมเค้าโครงหน้าที่แตกต่างกันสองแบบ: Letter และ A4 โดยไม่จำกัดความสูง ด้วย Aspose.Note นักพัฒนาสามารถจัดการไฟล์ OneNote ด้วยการเขียนโปรแกรมได้อย่างง่ายดาย โดยให้ความยืดหยุ่นและประสิทธิภาพในงานการจัดการเอกสาร

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Note สามารถจัดการไฟล์ OneNote ที่ซับซ้อนได้หรือไม่

A1: ใช่ Aspose.Note รองรับฟีเจอร์และฟังก์ชันต่างๆ เพื่อจัดการไฟล์ OneNote ที่ซับซ้อนได้อย่างมีประสิทธิภาพ

### คำถามที่ 2: Aspose.Note เหมาะสำหรับโครงการเชิงพาณิชย์หรือไม่

 ตอบ 2: แน่นอน Aspose.Note สามารถใช้ในโครงการเชิงพาณิชย์ได้อย่างง่ายดาย คุณสามารถซื้อใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 3: Aspose.Note ให้ทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถสำรวจ Aspose.Note ได้ด้วยรุ่นทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะหาเอกสารสำหรับ Aspose.Note ได้ที่ไหน

 A4: คุณสามารถค้นหาเอกสารโดยละเอียดได้[ที่นี่](https://reference.aspose.com/note/net/).

### Q5: ต้องการความช่วยเหลือเพิ่มเติมหรือไม่?

 A5: อย่าลังเลที่จะถามคำถามหรือขอการสนับสนุนในฟอรัม Aspose.Note[ที่นี่](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
