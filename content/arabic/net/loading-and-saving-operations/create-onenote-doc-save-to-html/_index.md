---
title: أنشئ مستند OneNote واحفظه إلى HTML في Aspose.Note
linktitle: أنشئ مستند OneNote واحفظه إلى HTML في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إنشاء مستندات Microsoft OneNote وحفظها بتنسيق HTML في تطبيقات .NET باستخدام Aspose.Note API. اتبع برنامجنا التعليمي الشامل مع أمثلة خطوة بخطوة.
type: docs
weight: 14
url: /ar/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## مقدمة

Aspose.Note for .NET عبارة عن واجهة برمجة تطبيقات قوية تتيح للمطورين العمل مع مستندات Microsoft OneNote برمجيًا في تطبيقات .NET الخاصة بهم. باستخدام Aspose.Note، يمكنك إنشاء ملفات OneNote ومعالجتها وتحويلها بسهولة. في هذا البرنامج التعليمي، سوف نستكشف كيفية إنشاء مستند OneNote وحفظه بتنسيق HTML باستخدام الخيارات المتنوعة التي توفرها Aspose.Note for .NET API.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

- المعرفة الأساسية بلغة البرمجة C#.
- تم تثبيت Visual Studio على نظامك.
-  Aspose.Note لـ .NET API المثبت في مشروعك. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/net/).
- الإلمام ببنية مستندات Microsoft OneNote.

## استيراد مساحات الأسماء

قبل أن نتعمق في جزء البرمجة، فلنستورد مساحات الأسماء الضرورية:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

الآن، دعنا نقسم كل مثال إلى خطوات متعددة ونرى كيفية إنشاء مستند OneNote وحفظه بتنسيق HTML باستخدام Aspose.Note لـ .NET.

## الخطوة 1: إنشاء مستند OneNote بالخيارات الافتراضية

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // تهيئة مستند OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // النمط الافتراضي لكل النص في المستند.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // حفظ في تنسيق HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

في هذه الخطوة، نقوم بتهيئة مستند OneNote جديد، وإضافة صفحة بعنوان، وحفظها بتنسيق HTML باستخدام الخيارات الافتراضية.

## الخطوة 2: إنشاء وحفظ نطاق صفحات محدد في HTML

```csharp
public static void CreateAndSavePageRange()
{
    // تهيئة مستند OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // النمط الافتراضي لكل النص في المستند.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // حفظ في تنسيق HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

نوضح هنا كيفية إنشاء مستند وحفظ نطاق صفحات معين بتنسيق HTML.

## الخطوة 3: احفظ بتنسيق HTML في Memory Stream باستخدام الموارد المضمنة

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // قم بتحميل مستند OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // تحديد خيارات حفظ HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // احفظ المستند في دفق الذاكرة
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

توضح هذه الخطوة كيفية حفظ مستند OneNote بتنسيق HTML باستخدام الموارد المضمنة (CSS والخطوط والصور) في تدفق الذاكرة.

## الخطوة 4: حفظ كملف HTML إلى ملف مع الموارد في ملفات منفصلة

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // قم بتحميل مستند OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // تحديد خيارات حفظ HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //احفظ المستند في ملف HTML مع الموارد المخزنة في ملفات منفصلة
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

في هذه الخطوة، نقوم بحفظ مستند OneNote بتنسيق HTML مع تخزين جميع الموارد (CSS والخطوط والصور) في ملفات منفصلة.

## الخطوة 5: احفظ بتنسيق HTML في Memory Stream مع عمليات الاسترجاعات لحفظ الموارد

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // حدد تكوين عمليات الاسترجاعات المحفوظة
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // تحديد خيارات حفظ HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // قم بتحميل مستند OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // احفظ المستند بتنسيق HTML مع الموارد التي تتم إدارتها بواسطة عمليات الاسترجاعات المحددة من قبل المستخدم
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // إلحاق البيانات يدويًا بتدفق CSS
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

نوضح هنا كيفية حفظ مستند OneNote بتنسيق HTML باستخدام الموارد التي تتم إدارتها من خلال عمليات الاسترجاعات المحددة من قبل المستخدم.

## خاتمة

في هذه المقالة، اكتشفنا كيفية العمل مع مستندات OneNote وحفظها بتنسيق HTML باستخدام Aspose.Note لـ .NET. باتباع الدليل خطوة بخطوة، يمكنك ذلك بسهولة

 قم بدمج هذه الوظيفة في تطبيقات .NET الخاصة بك، مما يسمح لك بمعالجة ملفات OneNote بكفاءة.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص مظهر ملف HTML المحفوظ؟

ج1: نعم، يمكنك تخصيص المظهر عن طريق تعديل أوراق أنماط CSS التي تم إنشاؤها أثناء عملية التحويل.

### س2: هل يدعم Aspose.Note التحويل إلى تنسيقات أخرى إلى جانب HTML؟

ج2: نعم، يدعم Aspose.Note التحويل إلى تنسيقات مختلفة مثل PDF والصور ومستندات Microsoft Word.

### س3: هل Aspose.Note متوافق مع تطبيقات .NET Core؟

ج3: نعم، Aspose.Note متوافق مع كل من تطبيقات .NET Framework و.NET Core.

### س4: هل يمكنني استخراج النصوص والصور من مستندات OneNote باستخدام Aspose.Note؟

ج4: نعم، يمكنك استخراج النصوص والصور بالإضافة إلى إجراء العديد من المعالجات الأخرى باستخدام Aspose.Note API.

### س5: هل هناك إصدار تجريبي متاح لاختبار ميزات Aspose.Note؟

 ج5: نعم، يمكنك تنزيل نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).