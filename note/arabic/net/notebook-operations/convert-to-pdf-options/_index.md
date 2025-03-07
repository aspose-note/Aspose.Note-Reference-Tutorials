---
title: قم بتحويل دفاتر الملاحظات إلى PDF باستخدام الخيارات الموجودة في Aspose Note .NET
linktitle: قم بتحويل دفاتر الملاحظات إلى PDF باستخدام الخيارات الموجودة في Aspose Note .NET
second_title: Aspose.Note .NET API
description: تعرف على كيفية تحويل دفاتر ملاحظات Microsoft OneNote إلى تنسيق PDF باستخدام Aspose.Note لمكتبة .NET مع خيارات قابلة للتخصيص.
weight: 16
url: /ar/net/notebook-operations/convert-to-pdf-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قم بتحويل دفاتر الملاحظات إلى PDF باستخدام الخيارات الموجودة في Aspose Note .NET

## مقدمة

في هذا البرنامج التعليمي، سنتعرف على عملية تحويل دفاتر الملاحظات إلى تنسيق PDF باستخدام Aspose.Note لمكتبة .NET. يوفر Aspose.Note for .NET مجموعة قوية من الميزات للعمل مع ملفات Microsoft OneNote برمجيًا.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

### 1. Aspose.Note لمكتبة .NET
 تأكد من أنك قمت بتنزيل وتثبيت Aspose.Note لمكتبة .NET. يمكنك تنزيله من[موقع إلكتروني](https://releases.aspose.com/note/net/).

### 2. بيئة التطوير
يجب أن يكون لديك بيئة تطوير معدة، مثل Visual Studio، مع تثبيت إطار عمل .NET الضروري.

## استيراد مساحات الأسماء

قبل أن نبدأ في استخدام Aspose.Note لـ .NET في مشروعنا، فلنستورد مساحات الأسماء المطلوبة:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

الآن، دعنا نقسم عملية تحويل دفاتر الملاحظات إلى PDF مع الخيارات إلى خطوات متعددة:

## الخطوة 1: قم بتحميل الكمبيوتر المحمول

أولاً، نحتاج إلى تحميل دفتر OneNote الذي نريد تحويله إلى ملف PDF.

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";

// قم بتحميل دفتر ملاحظات OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## الخطوة 2: حدد خيارات حفظ PDF

بعد ذلك، سنحدد الخيارات لحفظ المفكرة كملف PDF. يمكننا تخصيص إعدادات مختلفة مثل خوارزمية تقسيم الصفحة والهوامش وحجم الصفحة.

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## الخطوة 3: احفظ دفتر الملاحظات بصيغة PDF

الآن، سنقوم بحفظ دفتر الملاحظات كملف PDF باستخدام الخيارات المحددة.

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// احفظ دفتر الملاحظات
notebook.Save(dataDir, notebookSaveOptions);
```

## الخطوة 4: التحقق من التحويل

أخيرًا، دعونا نتحقق من نجاح التحويل ونقوم بطباعة الموقع الذي تم حفظ ملف PDF فيه.

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية تحويل دفاتر ملاحظات OneNote إلى تنسيق PDF باستخدام Aspose.Note لمكتبة .NET. باتباع الخطوات الموضحة أعلاه، يمكنك بسهولة دمج هذه الوظيفة في تطبيقات .NET الخاصة بك.

## الأسئلة الشائعة

### س1: هل يتوافق Aspose.Note for .NET مع كافة إصدارات Microsoft OneNote؟

ج1: نعم، يدعم Aspose.Note for .NET إصدارات مختلفة من Microsoft OneNote، بما في ذلك تنسيقات .one و.onetoc2.

### س2: هل يمكنني تخصيص مظهر مخرجات PDF؟

ج2: نعم، يمكنك تحديد خيارات متنوعة مثل حجم الصفحة والهوامش وخوارزمية تقسيم الصفحة لتخصيص مظهر مخرجات PDF.

### س3: هل يوفر Aspose.Note for .NET الدعم لتنسيقات الملفات الأخرى؟

ج3: نعم، يدعم Aspose.Note for .NET التحويل إلى تنسيقات أخرى متنوعة مثل الصور وHTML ومستندات Microsoft Word.

### س4: هل تتوفر نسخة تجريبية مجانية من Aspose.Note لـ .NET؟

ج4: نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.Note لـ .NET من موقع الويب لتقييم ميزاته قبل إجراء عملية شراء.

### س5: كيف يمكنني الحصول على الدعم الفني لـ Aspose.Note لـ .NET؟

 ج5: يمكنك الحصول على الدعم الفني لـ Aspose.Note لـ .NET من خلال زيارة الموقع[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) أو الاتصال بفريق دعم Aspose مباشرة.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
