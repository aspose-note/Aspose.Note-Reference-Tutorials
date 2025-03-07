---
title: استيراد مستندات PDF إلى Aspose.Note
linktitle: استيراد مستندات PDF إلى Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية استيراد مستندات PDF إلى Aspose.Note لـ .NET دون عناء باستخدام خيارات الدمج المتنوعة لتحقيق التكامل السلس.
weight: 10
url: /ar/net/import/import-pdf-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استيراد مستندات PDF إلى Aspose.Note

## مقدمة

مع الكم الهائل من المحتوى الرقمي المتاح اليوم، يعد دمج مستندات PDF في مشاريعك بسلاسة أمرًا بالغ الأهمية. يوفر Aspose.Note for .NET وظائف قوية لاستيراد مستندات PDF بكفاءة. في هذا البرنامج التعليمي، سنستكشف كيفية استيراد مستندات PDF خطوة بخطوة باستخدام Aspose.Note لـ .NET.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك ما يلي:

1.  Aspose.Note لـ .NET: قم بتنزيل المكتبة وتثبيتها من[هنا](https://releases.aspose.com/note/net/).
2. المعرفة الأساسية بـ C# و.NET Framework: سيكون فهم لغة البرمجة C# و.NET Framework مفيدًا.

## استيراد مساحات الأسماء

تأكد من استيراد مساحات الأسماء الضرورية للوصول إلى الفئات والأساليب المطلوبة لوظيفة استيراد PDF:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;

using Aspose.Note.Importing;

```

## الخطوة 1: استيراد مستندات PDF باستخدام Simple Merge

يسمح أسلوب الدمج البسيط باستيراد جميع الصفحات من مستندات PDF المتعددة صفحة تلو الأخرى:

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

## الخطوة 2: استيراد مستندات PDF باستخدام الدمج الهيكلي

يقوم الدمج الهيكلي باستيراد جميع الصفحات من مستندات PDF أثناء إدراج صفحات من كل مستند كعناصر فرعية لصفحة OneNote ذات المستوى الأعلى:

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

## الخطوة 3: استيراد مستندات PDF باستخدام دمج الصفحات الواحدة

تقوم ميزة Single Page Merge بدمج المحتوى من مستندات PDF متعددة في صفحة OneNote واحدة:

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

## الخطوة 4: استيراد مستندات PDF باستخدام الدمج المخصص

يسمح الدمج المخصص بتجميع الصفحات من مستندات PDF في صفحات OneNote واحدة بناءً على معايير مخصصة:

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

## خاتمة

يعد دمج مستندات PDF في تطبيقات .NET الخاصة بك باستخدام Aspose.Note عملية مباشرة، حيث تقدم خيارات دمج متنوعة مصممة خصيصًا لمتطلبات مشروعك. سواء كنت بحاجة إلى استيراد صفحات متعددة أو تنظيم المحتوى بشكل هرمي، فإن Aspose.Note يوفر الأدوات اللازمة للتكامل السلس.

## الأسئلة الشائعة

### س1: هل يمكنني استيراد مستندات PDF المشفرة؟

ج1: نعم، يدعم Aspose.Note استيراد مستندات PDF المشفرة. تأكد من توفير بيانات اعتماد فك التشفير المطلوبة.

### س2: هل هناك أي قيود على حجم ملف PDF للاستيراد؟

ج2: ليس لدى Aspose.Note أي قيود متأصلة على حجم ملف PDF للاستيراد. ومع ذلك، ضع في اعتبارك موارد النظام وتأثيرات الأداء بالنسبة لملفات PDF الكبيرة.

### س3: هل يمكنني تخصيص مظهر محتوى PDF المستورد؟

ج3: نعم، يمكنك تخصيص مظهر محتوى PDF المستورد باستخدام الخيارات المتنوعة التي يوفرها Aspose.Note، مثل أنماط الخطوط والألوان وتعديلات التخطيط.

### س4: هل Aspose.Note متوافق مع .NET Core؟

ج4: نعم، Aspose.Note متوافق مع .NET Core، مما يسمح لك بدمج وظيفة استيراد PDF في التطبيقات عبر الأنظمة الأساسية.

### س5: أين يمكنني العثور على دعم أو موارد إضافية؟

 ج5: للحصول على دعم إضافي أو وثائق أو مساعدة مجتمعية، قم بزيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
