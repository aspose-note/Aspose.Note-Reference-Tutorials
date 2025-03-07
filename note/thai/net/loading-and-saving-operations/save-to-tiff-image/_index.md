---
title: บันทึกเป็นภาพ TIFF ใน Aspose.Note
linktitle: บันทึกเป็นภาพ TIFF ใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีบันทึกเอกสาร OneNote เป็นรูปภาพ TIFF ด้วยวิธีการบีบอัดต่างๆ โดยใช้ Aspose.Note สำหรับ .NET
weight: 27
url: /th/net/loading-and-saving-operations/save-to-tiff-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกเป็นภาพ TIFF ใน Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีบันทึกเอกสารเป็นรูปภาพในรูปแบบ TIFF โดยใช้ Aspose.Note สำหรับ .NET Aspose.Note เป็น API อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft OneNote โดยทางโปรแกรม การบันทึกเอกสาร OneNote เป็นรูปภาพ TIFF จะมีประโยชน์สำหรับแอปพลิเคชันต่างๆ เช่น การเก็บถาวร การแชร์ หรือการพิมพ์

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1.  Aspose.Note สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Note สำหรับ .NET คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/net/).

2. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนาด้วย Visual Studio หรือ .NET IDE อื่น ๆ

3. เอกสาร OneNote: เตรียมเอกสาร OneNote ตัวอย่างที่คุณต้องการแปลงเป็นรูปแบบ TIFF

## นำเข้าเนมสเปซ

ขั้นแรก คุณต้องนำเข้าเนมสเปซที่จำเป็นไปยังโปรเจ็กต์ของคุณ:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;

```

## ขั้นตอนที่ 1: บันทึกเป็น TIFF โดยใช้การบีบอัด JPEG

การบีบอัด JPEG เป็นวิธีที่ใช้กันอย่างแพร่หลายในการลดขนาดรูปภาพโดยยังคงคุณภาพไว้ ต่อไปนี้คือวิธีที่คุณสามารถบันทึกเอกสาร OneNote เป็นรูปภาพ TIFF ด้วยการบีบอัด JPEG:

```csharp
public static void SaveToTiffUsingJpegCompression()
{
    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document("Path_to_your_OneNote_document");

    //กำหนดเส้นทางปลายทางสำหรับภาพ TIFF
    var dst = "Destination_path_for_TIFF_image";

    // บันทึกเอกสารเป็นภาพ TIFF พร้อมการบีบอัด JPEG
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        TiffCompression = TiffCompression.Jpeg,
        Quality = 93 // ปรับคุณภาพได้ตามต้องการ
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using JPEG compression.\nFile saved at " + dst);
}
```

## ขั้นตอนที่ 2: บันทึกเป็น TIFF โดยใช้การบีบอัด PackBits

การบีบอัด PackBits เป็นอัลกอริธึมการบีบอัดที่ง่ายและมีประสิทธิภาพซึ่งมักใช้ในอิมเมจ TIFF ต่อไปนี้คือวิธีที่คุณสามารถบันทึกเอกสาร OneNote เป็นรูปภาพ TIFF ด้วยการบีบอัด PackBits:

```csharp
public static void SaveToTiffUsingPackBitsCompression()
{
    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document("Path_to_your_OneNote_document");

    //กำหนดเส้นทางปลายทางสำหรับภาพ TIFF
    var dst = "Destination_path_for_TIFF_image";

    // บันทึกเอกสารเป็นภาพ TIFF ด้วยการบีบอัด PackBits
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        TiffCompression = TiffCompression.PackBits
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using PackBits compression.\nFile saved at " + dst);
}
```

## ขั้นตอนที่ 3: บันทึกเป็น TIFF โดยใช้การบีบอัด CCITT Group 3

การบีบอัด CCITT Group 3 หรือที่เรียกว่าการบีบอัดแฟกซ์ เหมาะสำหรับภาพขาวดำ ต่อไปนี้คือวิธีที่คุณสามารถบันทึกเอกสาร OneNote เป็นรูปภาพ TIFF ด้วยการบีบอัด CCITT Group 3:

```csharp
public static void SaveToTiffUsingCcitt3Compression()
{
    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document("Path_to_your_OneNote_document");

    //กำหนดเส้นทางปลายทางสำหรับภาพ TIFF
    var dst = "Destination_path_for_TIFF_image";

    // บันทึกเอกสารเป็นภาพ TIFF ด้วยการบีบอัด CCITT Group 3
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        ColorMode = ColorMode.BlackAndWhite,
        TiffCompression = TiffCompression.Ccitt3
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using CCITT Group 3 fax compression.\nFile saved at " + dst);
}
```

เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถบันทึกเอกสาร OneNote ของคุณเป็นรูปภาพ TIFF ได้อย่างง่ายดายด้วยตัวเลือกการบีบอัดต่างๆ โดยใช้ Aspose.Note สำหรับ .NET

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีบันทึกเอกสาร OneNote เป็นรูปภาพ TIFF โดยใช้วิธีการบีบอัดต่างๆ ด้วย Aspose.Note สำหรับ .NET ไม่ว่าคุณจะต้องการการบีบอัด JPEG, PackBits หรือ CCITT Group 3 Aspose.Note มอบความยืดหยุ่นในการจัดการกับความต้องการที่แตกต่างกันได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับคุณภาพของการบีบอัด JPEG ได้หรือไม่

A1: ได้ คุณสามารถปรับพารามิเตอร์คุณภาพได้เมื่อบันทึกด้วยการบีบอัด JPEG เพื่อให้สมดุลระหว่างคุณภาพของภาพและขนาดไฟล์

### คำถามที่ 2: Aspose.Note เข้ากันได้กับ Visual Studio เพื่อการพัฒนาหรือไม่

ตอบ 2: ได้ Aspose.Note สามารถรวมเข้ากับ Visual Studio สำหรับการพัฒนา .NET ได้อย่างราบรื่น

### คำถามที่ 3: มีข้อจำกัดเกี่ยวกับขนาดของเอกสาร OneNote ที่สามารถแปลงได้หรือไม่

A3: Aspose.Note สามารถจัดการเอกสาร OneNote ขนาดใหญ่ได้โดยไม่มีปัญหาด้านประสิทธิภาพที่สำคัญ

### คำถามที่ 4: ฉันสามารถทำให้กระบวนการแปลงเอกสารหลายชุดเป็นแบบอัตโนมัติได้หรือไม่

ตอบ 4: ได้ คุณสามารถทำให้กระบวนการแปลงเป็นอัตโนมัติโดยใช้การประมวลผลเป็นชุดด้วย Aspose.Note API

### คำถามที่ 5: Aspose.Note มีเวอร์ชันทดลองใช้งานหรือไม่

A5: ได้ คุณสามารถทดลองใช้ Aspose.Note ได้ฟรีจาก[ที่นี่](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
