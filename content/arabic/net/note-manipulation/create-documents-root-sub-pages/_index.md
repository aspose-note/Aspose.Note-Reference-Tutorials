---
title: قم بإنشاء المستندات ذات الصفحات الجذرية والفرعية باستخدام Aspose.Note
linktitle: قم بإنشاء المستندات ذات الصفحات الجذرية والفرعية باستخدام Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية استخدام Aspose.Note for .NET لإنشاء مستندات OneNote ديناميكية ذات بنيات هرمية.
type: docs
weight: 11
url: /ar/net/note-manipulation/create-documents-root-sub-pages/
---
## مقدمة

مرحبًا بك في برنامجنا التعليمي حول إنشاء المستندات ذات الصفحات الجذرية والصفحات الفرعية باستخدام Aspose.Note لـ .NET! Aspose.Note هي مكتبة قوية تمكن المطورين من العمل مع ملفات Microsoft OneNote برمجياً، مما يسمح بإنشاء مستندات OneNote ومعالجتها وتحويلها.

في هذا البرنامج التعليمي، سنرشدك خلال عملية إنشاء مستند OneNote بالصفحات الجذرية والصفحات الفرعية خطوة بخطوة. سنقدم شرحًا تفصيليًا ومقتطفات من التعليمات البرمجية باستخدام Aspose.Note لـ .NET، مما يسهل عليك المتابعة والتنفيذ في مشاريعك الخاصة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

1. Visual Studio: ستحتاج إلى تثبيت Visual Studio على نظامك لكتابة وتجميع تعليمات NET البرمجية.
2.  Aspose.Note لـ .NET: قم بتنزيل Aspose.Note لـ .NET وتثبيته من[صفحة التحميل](https://releases.aspose.com/note/net/).
3. المعرفة الأساسية لـ C#: الإلمام بلغة البرمجة C# مطلوب لفهم أمثلة التعليمات البرمجية وتنفيذها.

الآن بعد أن قمت بإعداد كل شيء، دعنا نتعمق في البرنامج التعليمي!

## استيراد مساحات الأسماء

أولاً، لنستورد مساحات الأسماء الضرورية إلى مشروعنا:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## الخطوة 1: تهيئة كائن المستند

```csharp
//قم بإنشاء كائن من فئة المستند
Document doc = new Document();
```

## الخطوة 2: إنشاء الصفحة الجذرية والصفحات الفرعية

```csharp
// تهيئة كائنات فئة الصفحة وتعيين مستوياتها
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### للصفحة 1:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### للصفحة 2:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### للصفحة 3:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## الخطوة 4: إضافة صفحات إلى المستند

```csharp
// إضافة صفحات إلى مستند OneNote
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## الخطوة 5: حفظ المستند

```csharp
// حفظ مستند OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية إنشاء المستندات ذات الصفحات الجذرية والصفحات الفرعية باستخدام Aspose.Note لـ .NET. يمكنك الآن الاستفادة من هذه المعرفة لإنشاء مستندات OneNote المعقدة بشكل ديناميكي في تطبيقاتك.

## الأسئلة الشائعة

### س١: هل يستطيع Aspose.Note التعامل مع مستندات OneNote الكبيرة؟

ج1: نعم، تم تصميم Aspose.Note للتعامل بكفاءة مع مستندات OneNote الكبيرة دون المساس بالأداء.

### س2: هل Aspose.Note متوافق مع .NET Core؟

ج2: نعم، يدعم Aspose.Note .NET Core إلى جانب .NET Framework التقليدي.

### س3: هل يمكنني تحويل مستندات OneNote إلى تنسيقات أخرى باستخدام Aspose.Note؟

ج3: بالتأكيد، يوفر Aspose.Note إمكانات التحويل إلى تنسيقات مختلفة بما في ذلك PDF وDOCX وHTML والمزيد.

### س 4: هل يقدم Aspose.Note التكامل السحابي؟

ج4: يركز Aspose.Note بشكل أساسي على التطوير المحلي، ولكن يمكنك استخدامه داخل البيئات السحابية من خلال الإعداد المناسب.

### س5: هل يتوفر الدعم الفني لـ Aspose.Note؟

ج5: نعم، توفر Aspose دعمًا فنيًا مخصصًا من خلال المنتدى الخاص بها حيث يمكنك طرح الأسئلة والحصول على المساعدة.