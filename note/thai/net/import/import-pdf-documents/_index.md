---
title: นำเข้าเอกสาร PDF ลงใน Aspose.Note
linktitle: นำเข้าเอกสาร PDF ลงใน Aspose.Note
second_title: Aspose.Note .NET API
description: เรียนรู้วิธีนำเข้าเอกสาร PDF ไปยัง Aspose.Note สำหรับ .NET ได้อย่างง่ายดายโดยใช้ตัวเลือกการผสานต่างๆ เพื่อการบูรณาการที่ราบรื่น
weight: 10
url: /th/net/import/import-pdf-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# นำเข้าเอกสาร PDF ลงใน Aspose.Note

## การแนะนำ

ด้วยเนื้อหาดิจิทัลที่มีอยู่มากมายในปัจจุบัน การผสานรวมเอกสาร PDF เข้ากับโครงการของคุณอย่างราบรื่นจึงเป็นสิ่งสำคัญ Aspose.Note สำหรับ .NET มีฟังก์ชันที่มีประสิทธิภาพในการนำเข้าเอกสาร PDF ได้อย่างมีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะสำรวจวิธีการนำเข้าเอกสาร PDF ทีละขั้นตอนโดยใช้ Aspose.Note สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1.  Aspose.Note สำหรับ .NET: ดาวน์โหลดและติดตั้งไลบรารีจาก[ที่นี่](https://releases.aspose.com/note/net/).
2. ความรู้พื้นฐานเกี่ยวกับ C# และ .NET Framework: ความเข้าใจในภาษาการเขียนโปรแกรม C# และ .NET Framework จะเป็นประโยชน์

## นำเข้าเนมสเปซ

ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงคลาสและวิธีการที่จำเป็นสำหรับฟังก์ชันการนำเข้า PDF:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;

using Aspose.Note.Importing;

```

## ขั้นตอนที่ 1: นำเข้าเอกสาร PDF โดยใช้ Simple Merge

วิธีการผสานอย่างง่ายช่วยให้สามารถนำเข้าหน้าทั้งหมดจากเอกสาร PDF หลายหน้าทีละหน้า:

```csharp
public static void ImportSetOfFiles_SimpleMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    d.Import(Path.Combine(dataDir, "sampleText.pdf"))
     .Import(Path.Combine(dataDir, "sampleImage.pdf"))
     .Import(Path.Combine(dataDir, "sampleTable.pdf"));

    d.Save(Path.Combine(dataDir, "sample_SimpleMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## ขั้นตอนที่ 2: นำเข้าเอกสาร PDF โดยใช้ Structured Merge

Structured Merge นำเข้าหน้าทั้งหมดจากเอกสาร PDF ในขณะที่แทรกหน้าจากแต่ละเอกสารเป็นลูกของหน้า OneNote ระดับบนสุด:

```csharp
public static void ImportSetOfFiles_StructuredMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    foreach (var file in new[] { "sampleText.pdf", "sampleImage.pdf", "sampleTable.pdf" })
    {
        d.AppendChildLast(new Page()).Title = new Title() { TitleText = new RichText() { ParagraphStyle = ParagraphStyle.Default }.Append(file) };
        d.Import(Path.Combine(dataDir, file), new PdfImportOptions(), new MergeOptions() { InsertAt = int.MaxValue, InsertAsChild = true });
    }

    d.Save(Path.Combine(dataDir, "sample_StructuredMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## ขั้นตอนที่ 3: นำเข้าเอกสาร PDF โดยใช้การผสานหน้าเดียว

Single Page Merge ผสานเนื้อหาจากเอกสาร PDF หลายฉบับลงในหน้า OneNote หน้าเดียว:

```csharp
public static void ImportSetOfFiles_SinglePageMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var importOptions = new PdfImportOptions();
    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    d.Import(Path.Combine(dataDir, "sampleText.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleImage.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleTable.pdf"), importOptions, mergeOptions);

    d.Save(Path.Combine(dataDir, "sample_SinglePageMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## ขั้นตอนที่ 4: นำเข้าเอกสาร PDF โดยใช้ Custom Merge

การผสานแบบกำหนดเองอนุญาตให้จัดกลุ่มหน้าจากเอกสาร PDF ลงในหน้า OneNote หน้าเดียวตามเกณฑ์ที่กำหนดเอง:

```csharp
public static void ImportSetOfFiles_CustomMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    IEnumerable<Page> pages = PdfImporter.Import(Path.Combine(dataDir, "SampleGrouping.pdf"));
    while (pages.Any())
    {
        d.Merge(pages.Take(5), mergeOptions);
        pages = pages.Skip(5);
    }

    d.Save(Path.Combine(dataDir, "sample_CustomMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## บทสรุป

การรวมเอกสาร PDF เข้ากับแอปพลิเคชัน .NET ของคุณกับ Aspose.Note เป็นกระบวนการที่ไม่ซับซ้อน โดยเสนอตัวเลือกการผสานที่หลากหลายที่เหมาะกับความต้องการของโครงการของคุณ ไม่ว่าคุณจะต้องนำเข้าหลายหน้าหรือจัดระเบียบเนื้อหาตามลำดับชั้น Aspose.Note ก็มีเครื่องมือที่จำเป็นสำหรับการผสานรวมที่ราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถนำเข้าเอกสาร PDF ที่เข้ารหัสได้หรือไม่

ตอบ 1: ใช่ Aspose.Note รองรับการนำเข้าเอกสาร PDF ที่เข้ารหัส ตรวจสอบให้แน่ใจว่าคุณระบุข้อมูลรับรองการถอดรหัสที่จำเป็น

### คำถามที่ 2: มีข้อจำกัดเกี่ยวกับขนาดไฟล์ PDF สำหรับการนำเข้าหรือไม่

A2: Aspose.Note ไม่มีข้อจำกัดโดยธรรมชาติเกี่ยวกับขนาดไฟล์ PDF สำหรับการนำเข้า อย่างไรก็ตาม ให้พิจารณาทรัพยากรระบบและผลกระทบด้านประสิทธิภาพสำหรับไฟล์ PDF ขนาดใหญ่

### คำถามที่ 3: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของเนื้อหา PDF ที่นำเข้าได้หรือไม่

A3: ได้ คุณสามารถปรับแต่งลักษณะที่ปรากฏของเนื้อหา PDF ที่นำเข้าได้โดยใช้ตัวเลือกต่างๆ ที่ Aspose.Note มอบให้ เช่น ลักษณะแบบอักษร สี และการปรับเค้าโครง

### คำถามที่ 4: Aspose.Note เข้ากันได้กับ .NET Core หรือไม่

ตอบ 4: ใช่ Aspose.Note เข้ากันได้กับ .NET Core ซึ่งช่วยให้คุณสามารถรวมฟังก์ชันการนำเข้า PDF เข้ากับแอปพลิเคชันข้ามแพลตฟอร์มได้

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือแหล่งข้อมูลเพิ่มเติมได้จากที่ไหน

 A5: สำหรับการสนับสนุนเพิ่มเติม เอกสาร หรือความช่วยเหลือจากชุมชน โปรดไปที่[ฟอรั่ม Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
