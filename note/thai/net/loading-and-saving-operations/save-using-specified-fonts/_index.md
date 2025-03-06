---
title: บันทึกโดยใช้แบบอักษรที่ระบุใน Aspose.Note
linktitle: บันทึกโดยใช้แบบอักษรที่ระบุใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีบันทึกเอกสารด้วยแบบอักษรที่ระบุใน Aspose.Note สำหรับ .NET ปรับแต่งการตั้งค่าแบบอักษรได้อย่างง่ายดายเพื่อการจัดรูปแบบเอกสารที่สอดคล้องกัน
weight: 28
url: /th/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกโดยใช้แบบอักษรที่ระบุใน Aspose.Note

## การแนะนำ

ในบทช่วยสอนนี้ เราจะเรียนรู้วิธีบันทึกเอกสารโดยใช้แบบอักษรที่ระบุใน Aspose.Note สำหรับ .NET เราจะสำรวจวิธีการต่างๆ เพื่อให้บรรลุเป้าหมายนี้ทีละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1.  Aspose.Note สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Note สำหรับ .NET คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/net/).

2. สภาพแวดล้อมการพัฒนา: คุณต้องมีสภาพแวดล้อมการพัฒนาที่ตั้งค่าไว้สำหรับการพัฒนา .NET

## นำเข้าเนมสเปซ

ขั้นแรก เรามานำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## ขั้นตอนที่ 1: บันทึกด้วยชื่อแบบอักษรเริ่มต้น

ในขั้นตอนนี้ เราจะบันทึกเอกสารโดยใช้ชื่อแบบอักษรเริ่มต้นที่ระบุ

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    string dataDir = "Your Document Directory";

    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // บันทึกเอกสารเป็น PDF ด้วยแบบอักษรเริ่มต้นที่ระบุ
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## ขั้นตอนที่ 2: บันทึกด้วยแบบอักษรเริ่มต้นจากไฟล์

ต่อไป มาบันทึกเอกสารโดยใช้แบบอักษรเริ่มต้นที่โหลดจากไฟล์

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // บันทึกเอกสารเป็น PDF พร้อมโหลดแบบอักษรเริ่มต้นจากไฟล์
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## ขั้นตอนที่ 3: บันทึกด้วยแบบอักษรเริ่มต้นจากสตรีม

สุดท้ายนี้ มาบันทึกเอกสารโดยใช้แบบอักษรเริ่มต้นที่โหลดจากสตรีม

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // เส้นทางไปยังไดเร็กทอรีเอกสาร
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // โหลดเอกสารลงใน Aspose.Note
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // บันทึกเอกสารเป็น PDF พร้อมโหลดแบบอักษรเริ่มต้นจากสตรีม
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจวิธีการบันทึกเอกสารโดยใช้แบบอักษรที่ระบุใน Aspose.Note สำหรับ .NET เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถปรับแต่งการตั้งค่าแบบอักษรได้ตามความต้องการของคุณ เพื่อให้มั่นใจว่าเอกสารของคุณได้รับการจัดรูปแบบตามที่ต้องการ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้แบบอักษรใดๆ ในการบันทึกเอกสารใน Aspose.Note ได้หรือไม่

A1: ได้ คุณสามารถระบุแบบอักษรใดก็ได้สำหรับบันทึกเอกสาร เพียงตรวจสอบให้แน่ใจว่าไฟล์ฟอนต์สามารถเข้าถึงได้และโหลดอย่างถูกต้อง

### คำถามที่ 2: Aspose.Note เข้ากันได้กับรูปแบบเอกสารที่แตกต่างกันหรือไม่

คำตอบ 2: Aspose.Note ใช้งานได้กับเอกสาร OneNote เป็นหลัก แต่มีตัวเลือกในการบันทึกในรูปแบบต่างๆ รวมถึง PDF

### คำถามที่ 3: ฉันจะจัดการกับแบบอักษรที่หายไปเมื่อบันทึกเอกสารได้อย่างไร

A3: Aspose.Note มีตัวเลือกให้ใช้แบบอักษรเริ่มต้นในกรณีที่แบบอักษรที่ระบุหายไป เพื่อให้มั่นใจว่ามีการจัดรูปแบบเอกสารที่สอดคล้องกัน

### คำถามที่ 4: Aspose.Note รองรับการฝังแบบอักษรในเอกสารเอาต์พุตหรือไม่

ตอบ 4: ใช่ Aspose.Note อนุญาตให้ฝังแบบอักษรเพื่อให้มั่นใจในการพกพาเอกสารและการแสดงผลที่สอดคล้องกันบนแพลตฟอร์มต่างๆ

### คำถามที่ 5: ฉันจะรับความช่วยเหลือเพิ่มเติมเกี่ยวกับ Aspose.Note ได้ที่ไหน

 A5: สำหรับความช่วยเหลือเพิ่มเติมหรือการสนับสนุนด้านเทคนิค คุณสามารถไปที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
