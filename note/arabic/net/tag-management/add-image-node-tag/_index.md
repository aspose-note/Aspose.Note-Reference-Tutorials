---
title: أضف عقدة صورة مع علامة في Aspose.Note
linktitle: أضف عقدة صورة مع علامة في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية تحسين مستندات OneNote الخاصة بك عن طريق إضافة صور ذات علامات مخصصة باستخدام Aspose.Note لـ .NET.
type: docs
weight: 10
url: /ar/net/tag-management/add-image-node-tag/
---
## مقدمة

في هذا البرنامج التعليمي، سنستكشف كيفية إضافة عقدة صورة بعلامة باستخدام Aspose.Note لـ .NET. تتيح لك هذه الميزة تحسين مستندات OneNote الخاصة بك عن طريق إضافة صور ذات علامات مخصصة.

## المتطلبات الأساسية

قبل أن تبدأ، تأكد من أن لديك ما يلي:

1. Visual Studio: قم بتثبيت Visual Studio IDE على نظامك.
2.  Aspose.Note for .NET: قم بتنزيل وتثبيت مكتبة Aspose.Note for .NET من[رابط التحميل](https://releases.aspose.com/note/net/).
3. المعرفة الأساسية: تعرف على لغة البرمجة C# وإطار عمل .NET.

## استيراد مساحات الأسماء

أولاً، تأكد من تضمين مساحات الأسماء الضرورية في كود C# الخاص بك:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## الخطوة 1: تهيئة كائنات المستند والصفحة

 ابدأ بإنشاء مثيل لـ`Document` فئة و أ`Page` هدف:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## الخطوة 2: تهيئة كائنات المخطط التفصيلي والعنصر التفصيلي

 بعد ذلك، قم بالتهيئة`Outline` و`OutlineElement` أشياء:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## الخطوة 3: تحميل وإدراج الصورة

قم بتحميل الصورة المطلوبة وأدخلها في عقدة المستند:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## الخطوة 4: إضافة علامة إلى الصورة

أضف علامة مخصصة للصورة:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## الخطوة 5: إلحاق عنصر المخطط التفصيلي وعقد الصفحة

إلحاق عنصر المخطط التفصيلي وعقد المخطط التفصيلي بالصفحة:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## الخطوة 6: احفظ المستند

احفظ مستند OneNote المعدل:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## خاتمة

باتباع هذه الخطوات، يمكنك بسهولة إضافة عقدة صورة بعلامة مخصصة باستخدام Aspose.Note لـ .NET، مما يؤدي إلى إثراء مستندات OneNote الخاصة بك بمرئيات مخصصة.

## الأسئلة الشائعة

### س1: هل يمكنني إضافة صور متعددة بعلامات مختلفة في مستند واحد باستخدام Aspose.Note؟

ج1: نعم، يمكنك إضافة صور متعددة بعلامات مختلفة عن طريق اتباع خطوات مماثلة لكل صورة.

### س2: هل Aspose.Note متوافق مع كافة إصدارات OneNote؟

ج2: يدعم Aspose.Note إصدارات مختلفة من OneNote، مما يضمن التوافق عبر بيئات مختلفة.

### س3: هل يمكنني تخصيص مظهر العلامة المضافة إلى الصورة؟

ج3: نعم، يوفر Aspose.Note المرونة في تخصيص مظهر العلامة ليناسب تفضيلاتك.

### س4: هل يقدم Aspose.Note دعمًا لإضافة الصور من عناوين URL؟

ج4: يدعم Aspose.Note بشكل أساسي إضافة الصور من الدلائل المحلية، ولكن يمكنك دمج الصور الخارجية عن طريق تنزيلها محليًا أولاً.

### س5: هل هناك أي قيود على حجم أو تنسيق الصور التي يمكن إضافتها؟

ج5: يدعم Aspose.Note نطاقًا واسعًا من تنسيقات الصور ولا يفرض أي قيود صارمة على حجم الصورة، مما يسمح لك بدمج عناصر مرئية متنوعة في مستنداتك.