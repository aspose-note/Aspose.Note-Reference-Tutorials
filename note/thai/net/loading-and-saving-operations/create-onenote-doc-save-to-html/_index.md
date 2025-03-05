---
title: สร้างเอกสาร OneNote และบันทึกเป็น HTML ใน Aspose.Note
linktitle: สร้างเอกสาร OneNote และบันทึกเป็น HTML ใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีสร้างและบันทึกเอกสาร Microsoft OneNote เป็นรูปแบบ HTML ในแอปพลิเคชัน .NET โดยใช้ Aspose.Note API ปฏิบัติตามบทช่วยสอนที่ครอบคลุมของเราพร้อมตัวอย่างทีละขั้นตอน
type: docs
weight: 14
url: /th/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## การแนะนำ

Aspose.Note สำหรับ .NET เป็น API อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับเอกสาร Microsoft OneNote โดยทางโปรแกรมในแอปพลิเคชัน .NET ของตน ด้วย Aspose.Note คุณสามารถสร้าง จัดการ และแปลงไฟล์ OneNote ได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะสำรวจวิธีสร้างเอกสาร OneNote และบันทึกเป็นรูปแบบ HTML โดยใช้ตัวเลือกต่างๆ ที่ได้รับจาก Aspose.Note สำหรับ .NET API

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

- ความรู้พื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C#
- ติดตั้ง Visual Studio บนระบบของคุณแล้ว
-  ติดตั้ง Aspose.Note สำหรับ .NET API ในโปรเจ็กต์ของคุณ คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/note/net/).
- ความคุ้นเคยกับโครงสร้างของเอกสาร Microsoft OneNote

## นำเข้าเนมสเปซ

ก่อนที่เราจะเจาะลึกในส่วนของการเขียนโค้ด เรามานำเข้าเนมสเปซที่จำเป็นก่อน:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

ตอนนี้ เราจะแบ่งแต่ละตัวอย่างออกเป็นหลายขั้นตอน และดูวิธีสร้างเอกสาร OneNote และบันทึกเป็นรูปแบบ HTML โดยใช้ Aspose.Note สำหรับ .NET

## ขั้นตอนที่ 1: สร้างเอกสาร OneNote ด้วยตัวเลือกเริ่มต้น

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // เตรียมใช้งานเอกสาร OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // สไตล์เริ่มต้นสำหรับข้อความทั้งหมดในเอกสาร
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // บันทึกเป็นรูปแบบ HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

ในขั้นตอนนี้ เราจะเริ่มต้นเอกสาร OneNote ใหม่ เพิ่มหน้าที่มีชื่อเรื่อง และบันทึกเป็นรูปแบบ HTML โดยใช้ตัวเลือกเริ่มต้น

## ขั้นตอนที่ 2: สร้างและบันทึกช่วงหน้าเฉพาะเป็น HTML

```csharp
public static void CreateAndSavePageRange()
{
    // เตรียมใช้งานเอกสาร OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // สไตล์เริ่มต้นสำหรับข้อความทั้งหมดในเอกสาร
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // บันทึกเป็นรูปแบบ HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

ที่นี่ เราจะสาธิตวิธีการสร้างเอกสารและบันทึกช่วงหน้าเฉพาะเป็นรูปแบบ HTML

## ขั้นตอนที่ 3: บันทึกเป็น HTML ไปยังสตรีมหน่วยความจำด้วยทรัพยากรที่ฝังตัว

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // โหลดเอกสาร OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // ระบุตัวเลือกการบันทึก HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // บันทึกเอกสารลงในสตรีมหน่วยความจำ
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

ขั้นตอนนี้แสดงวิธีการบันทึกเอกสาร OneNote เป็นรูปแบบ HTML พร้อมทรัพยากรที่ฝังตัว (CSS แบบอักษร และรูปภาพ) ลงในสตรีมหน่วยความจำ

## ขั้นตอนที่ 4: บันทึกเป็น HTML เป็นไฟล์พร้อมทรัพยากรในไฟล์แยก

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // โหลดเอกสาร OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // ระบุตัวเลือกการบันทึก HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    // บันทึกเอกสารเป็นไฟล์ HTML พร้อมทรัพยากรที่จัดเก็บไว้ในไฟล์แยกกัน
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

ในขั้นตอนนี้ เราจะบันทึกเอกสาร OneNote เป็นรูปแบบ HTML พร้อมทรัพยากรทั้งหมด (CSS แบบอักษร และรูปภาพ) เก็บไว้ในไฟล์แยกกัน

## ขั้นตอนที่ 5: บันทึกเป็น HTML ไปยังสตรีมหน่วยความจำพร้อมการโทรกลับเพื่อบันทึกทรัพยากร

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // ระบุการกำหนดค่าการโทรกลับที่บันทึก
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // ระบุตัวเลือกการบันทึก HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // โหลดเอกสาร OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // บันทึกเอกสารในรูปแบบ HTML ด้วยทรัพยากรที่จัดการโดยการโทรกลับที่ผู้ใช้กำหนด
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // ผนวกข้อมูลเข้ากับสตรีม CSS ด้วยตนเอง
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

ที่นี่ เราจะสาธิตวิธีการบันทึกเอกสาร OneNote เป็นรูปแบบ HTML ด้วยทรัพยากรที่จัดการโดยการโทรกลับที่ผู้ใช้กำหนด

## บทสรุป

ในบทความนี้ เราได้สำรวจวิธีการทำงานกับเอกสาร OneNote และบันทึกเป็นรูปแบบ HTML โดยใช้ Aspose.Note สำหรับ .NET โดยทำตามคำแนะนำทีละขั้นตอนคุณสามารถได้อย่างง่ายดาย

 รวมฟังก์ชันนี้เข้ากับแอปพลิเคชัน .NET ของคุณ ทำให้คุณสามารถจัดการไฟล์ OneNote ได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของไฟล์ HTML ที่บันทึกไว้ได้หรือไม่

A1: ได้ คุณสามารถปรับแต่งลักษณะที่ปรากฏได้โดยการแก้ไขสไตล์ชีต CSS ที่สร้างขึ้นระหว่างกระบวนการแปลง

### คำถามที่ 2: Aspose.Note รองรับการแปลงเป็นรูปแบบอื่นนอกเหนือจาก HTML หรือไม่

ตอบ 2: ใช่ Aspose.Note รองรับการแปลงเป็นรูปแบบต่างๆ เช่น PDF รูปภาพ และเอกสาร Microsoft Word

### คำถามที่ 3: Aspose.Note เข้ากันได้กับแอปพลิเคชัน .NET Core หรือไม่

A3: ใช่ Aspose.Note เข้ากันได้กับทั้งแอปพลิเคชัน .NET Framework และ .NET Core

### คำถามที่ 4: ฉันสามารถแยกข้อความและรูปภาพจากเอกสาร OneNote โดยใช้ Aspose.Note ได้หรือไม่

ตอบ 4: ได้ คุณสามารถแยกข้อความและรูปภาพ รวมทั้งดำเนินการจัดการอื่นๆ ได้โดยใช้ Aspose.Note API

### คำถามที่ 5: มีเวอร์ชันทดลองใช้สำหรับการทดสอบฟีเจอร์ Aspose.Note หรือไม่

 A5: ได้ คุณสามารถดาวน์โหลดเวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).