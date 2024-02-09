---
title: أضف الارتباطات التشعبية في مستندات Aspose.Note
linktitle: أضف الارتباطات التشعبية في مستندات Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إضافة ارتباطات تشعبية إلى مستندات Aspose.Note باستخدام Aspose.Note لـ .NET. قم بتحسين تفاعل المستند من خلال هذا البرنامج التعليمي خطوة بخطوة.
type: docs
weight: 10
url: /ar/net/hyperlinks/add-hyperlinks/
---
## مقدمة

ستتعلم في هذا البرنامج التعليمي كيفية إضافة ارتباطات تشعبية إلى النص داخل مستندات Aspose.Note باستخدام إطار عمل .NET. يوفر Aspose.Note ميزات قوية لمعالجة مستندات OneNote برمجيًا. يمكن أن تؤدي إضافة الارتباطات التشعبية إلى تحسين التفاعل وسهولة استخدام مستنداتك، مما يجعلها أكثر جاذبية للمستخدمين.

## المتطلبات الأساسية:

قبل البدء، تأكد من توفر المتطلبات الأساسية التالية:

1. الفهم الأساسي للغة البرمجة C#.
2. تم تثبيت Visual Studio على نظامك.
3.  تم تثبيت Aspose.Note لمكتبة .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/net/).
4. الإلمام بهيكل ومكونات مستندات Aspose.Note.

## استيراد مساحات الأسماء:

أولاً، تحتاج إلى استيراد مساحات الأسماء الضرورية إلى مشروع C# الخاص بك. توفر مساحات الأسماء هذه إمكانية الوصول إلى الفئات والأساليب المطلوبة للعمل مع مستندات Aspose.Note.

```csharp
using System;
using System.Drawing;
```

## الخطوة 1: إنشاء كائن مستند جديد:

ابدأ بإنشاء مثيل جديد لفئة المستند. سيمثل هذا الكائن مستند Aspose.Note الخاص بك، والذي ستضيف إليه الارتباط التشعبي.

```csharp
Document doc = new Document();
```

## الخطوة 2: تحديد أنماط النص:

تحديد أنماط النص للنص العادي ونص الارتباط التشعبي. يمكنك تخصيص سمات مختلفة مثل لون الخط واسم الخط وحجم الخط وفقًا لتفضيلاتك.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

## الخطوة 3: إنشاء كائنات RichText:

قم بإنشاء كائنات RichText لمقاطع النص التي تريد تضمينها في المستند الخاص بك. قم بإلحاق النص المناسب وتطبيق أنماط النص المطلوبة على كل مقطع.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

## الخطوة 4: إنشاء المخطط التفصيلي وعنصر المخطط التفصيلي:

قم بإنشاء كائن مخطط تفصيلي وكائن OutlineElement لتنظيم محتوى المستند الخاص بك. قم بإلحاق كائن RichText الذي يحتوي على الارتباط التشعبي بـ OutlineElement.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

## الخطوة 5: إضافة عناصر إلى الصفحة:

قم بإنشاء كائن عنوان وكائن صفحة. إلحاق كائن المخطط التفصيلي بالصفحة. وأخيرًا، قم بإلحاق الصفحة بالمستند.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## الخطوة 6: حفظ المستند:

حدد مسار الملف حيث تريد حفظ مستند Aspose.Note واستدعاء طريقة Save لحفظه.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## خاتمة:

تعلمت في هذا البرنامج التعليمي كيفية إضافة ارتباطات تشعبية إلى مستندات Aspose.Note باستخدام Aspose.Note لـ .NET. باتباع هذه الخطوات، يمكنك تحسين تفاعل مستنداتك وتزويد المستخدمين بتجربة أكثر ديناميكية.

## الأسئلة الشائعة

### س1: هل يمكنني إضافة ارتباطات تشعبية متعددة داخل نفس المستند باستخدام Aspose.Note؟

ج1: نعم، يمكنك إضافة ارتباطات تشعبية متعددة إلى مقاطع نصية مختلفة داخل مستند Aspose.Note واحد.

### س2: هل يمكنني تخصيص مظهر الارتباطات التشعبية في مستندات Aspose.Note؟

ج2: نعم، يمكنك تخصيص سمات مختلفة مثل لون الخط وحجم الخط ونمط الخط للارتباطات التشعبية في مستندات Aspose.Note.

### س3: هل يدعم Aspose.Note الارتباطات التشعبية لمواقع الويب الخارجية؟

ج3: نعم، يتيح لك Aspose.Note إنشاء ارتباطات تشعبية توجه المستخدمين إلى مواقع الويب أو صفحات الويب الخارجية.

### س4: هل Aspose.Note متوافق مع كافة إصدارات Microsoft OneNote؟

ج4: تم تصميم Aspose.Note للعمل مع Microsoft OneNote 2010 والإصدارات الأحدث.

### س5: هل يمكنني إضافة ارتباطات تشعبية برمجيًا باستخدام Aspose.Note APIs؟

ج5: نعم، يوفر Aspose.Note واجهات برمجة التطبيقات التي تسمح لك بإضافة ارتباطات تشعبية إلى النص برمجيًا داخل تطبيقات .NET الخاصة بك.