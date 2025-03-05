---
title: أضف عقدة نصية مع علامة في Aspose.Note
linktitle: أضف عقدة نصية مع علامة في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إضافة العقد النصية ذات العلامات إلى مستندات OneNote باستخدام Aspose.Note لـ .NET.
type: docs
weight: 12
url: /ar/net/tag-management/add-text-node-tag/
---
## مقدمة

تعد Aspose.Note for .NET مكتبة قوية تمكن المطورين من إنشاء ملفات Microsoft OneNote ومعالجتها وتحويلها برمجيًا باستخدام إطار عمل .NET. في هذا البرنامج التعليمي، سوف نستكشف كيفية إضافة عقدة نصية بعلامة إلى مستند OneNote باستخدام Aspose.Note لـ .NET.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

1. Visual Studio: تأكد من تثبيت Visual Studio على نظامك.
2.  Aspose.Note لـ .NET: قم بتنزيل Aspose.Note لـ .NET وتثبيته من[موقع إلكتروني](https://releases.aspose.com/note/net/).
3. المعرفة الأساسية بـ C#: تعرف على أساسيات لغة البرمجة C#.

## استيراد مساحات الأسماء

أولاً، تحتاج إلى استيراد مساحات الأسماء الضرورية للوصول إلى الفئات والأساليب المطلوبة للعمل مع Aspose.Note لـ .NET.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## الخطوة 1: إنشاء كائن مستند

قم بتهيئة كائن مستند لبدء العمل باستخدام مستند OneNote.

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## الخطوة 2: تهيئة كائنات الصفحة والمخطط التفصيلي

قم بإنشاء كائنات الصفحة والمخطط التفصيلي لتنظيم محتوى مستند OneNote.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## الخطوة 3: إضافة عقدة نصية مع العلامة

قم بإنشاء كائن RichText بالنص والنمط المطلوب، ثم قم بإضافته إلى OutlineElement.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## الخطوة 4: إلحاق عنصر المخطط التفصيلي وعقد الصفحة

قم بإلحاق OutlineElement بالمخطط التفصيلي، ثم قم بإلحاق المخطط التفصيلي بالصفحة. وأخيرًا، قم بإلحاق الصفحة بالمستند.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## الخطوة 5: احفظ المستند

احفظ مستند OneNote المعدل في موقع محدد.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية إضافة عقدة نصية بعلامة إلى مستند OneNote باستخدام Aspose.Note لـ .NET. بفضل هذه المعرفة، يمكنك الآن تخصيص ملفات OneNote وتحسينها برمجيًا.

## الأسئلة الشائعة

### س1: هل يمكنني إضافة عقد نصية متعددة بعلامات مختلفة في نفس المستند؟

A1: نعم، يمكنك إضافة عقد نصية متعددة بعلامات مختلفة باتباع نفس العملية لكل عقدة.

### س2: هل يتوافق Aspose.Note for .NET مع كافة إصدارات OneNote؟

ج2: يدعم Aspose.Note for .NET إصدارات مختلفة من OneNote، بما في ذلك الإصدارات 2010 و2013 و2016 وما فوق.

### Q3: هل يمكنني تخصيص ألوان وأنماط العلامة؟

ج3: نعم، يمكنك تخصيص ألوان وأنماط العلامة وفقًا لمتطلباتك.

### س4: هل يدعم Aspose.Note for .NET تشفير المستندات؟

ج4: نعم، يدعم Aspose.Note for .NET تشفير المستندات لضمان أمان البيانات.

### س5: أين يمكنني العثور على المزيد من الموارد والدعم لـ Aspose.Note لـ .NET؟

 ج5: يمكنك استكشاف[Aspose.Note لوثائق .NET](https://reference.aspose.com/note/net/)وطلب المساعدة من[منتدى Aspose.Note](https://forum.aspose.com/c/note/28).