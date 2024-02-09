---
title: الحفظ باستخدام الخطوط المحددة في Aspose.Note
linktitle: الحفظ باستخدام الخطوط المحددة في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية حفظ المستندات بخطوط محددة في Aspose.Note لـ .NET. قم بتخصيص إعدادات الخط بسهولة للحصول على تنسيق ثابت للمستندات.
type: docs
weight: 28
url: /ar/net/loading-and-saving-operations/save-using-specified-fonts/
---
## مقدمة

في هذا البرنامج التعليمي، سوف نتعلم كيفية حفظ المستندات باستخدام خطوط محددة في Aspose.Note لـ .NET. سنستكشف طرقًا مختلفة لتحقيق ذلك، خطوة بخطوة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1.  Aspose.Note لـ .NET: تأكد من تثبيت Aspose.Note لـ .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/net/).

2. بيئة التطوير: أنت بحاجة إلى إعداد بيئة تطوير لتطوير .NET.

## استيراد مساحات الأسماء

أولاً، لنستورد مساحات الأسماء الضرورية:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## الخطوة 1: الحفظ باسم الخط الافتراضي

في هذه الخطوة، سنقوم بحفظ مستند باستخدام اسم خط افتراضي محدد.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // المسار إلى دليل المستندات.
    string dataDir = "Your Document Directory";

    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // احفظ المستند بصيغة PDF بالخط الافتراضي المحدد.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## الخطوة 2: الحفظ بالخط الافتراضي من الملف

بعد ذلك، دعونا نحفظ مستندًا باستخدام الخط الافتراضي الذي تم تحميله من ملف.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // المسار إلى دليل المستندات.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // احفظ المستند بصيغة PDF مع تحميل الخط الافتراضي من الملف.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## الخطوة 3: الحفظ باستخدام الخط الافتراضي من الدفق

وأخيرًا، دعونا نحفظ مستندًا باستخدام الخط الافتراضي الذي تم تحميله من الدفق.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // المسار إلى دليل المستندات.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // احفظ المستند بصيغة PDF مع تحميل الخط الافتراضي من الدفق.
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

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا كيفية حفظ المستندات باستخدام خطوط محددة في Aspose.Note لـ .NET. باتباع هذه الخطوات، يمكنك تخصيص إعدادات الخط وفقًا لمتطلباتك، مما يضمن تنسيق مستنداتك حسب الرغبة.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام أي خط لحفظ المستندات في Aspose.Note؟

A1: نعم، يمكنك تحديد أي خط لحفظ المستندات. فقط تأكد من إمكانية الوصول إلى ملف الخط وتحميله بشكل صحيح.

### س2: هل Aspose.Note متوافق مع تنسيقات المستندات المختلفة؟

ج2: يعمل Aspose.Note بشكل أساسي مع مستندات OneNote ولكنه يوفر خيارات للحفظ بتنسيقات مختلفة بما في ذلك PDF.

### س3: كيف يمكنني التعامل مع الخطوط المفقودة عند حفظ المستندات؟

ج3: يوفر Aspose.Note خيارات لاستخدام الخطوط الافتراضية في حالة فقدان الخط المحدد، مما يضمن تنسيقًا متسقًا للمستند.

### س4: هل يدعم Aspose.Note تضمين الخط في مستندات الإخراج؟

ج4: نعم، يسمح Aspose.Note بتضمين الخطوط لضمان إمكانية نقل المستندات والعرض المتسق عبر الأنظمة الأساسية المختلفة.

### س5: أين يمكنني الحصول على المزيد من المساعدة فيما يتعلق بـ Aspose.Note؟

 ج5: لمزيد من المساعدة أو الدعم الفني، يمكنك زيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28).