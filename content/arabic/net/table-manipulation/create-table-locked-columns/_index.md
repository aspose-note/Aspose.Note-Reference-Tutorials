---
title: إنشاء جدول بالأعمدة المقفلة باستخدام Aspose.Note
linktitle: إنشاء جدول بالأعمدة المقفلة باستخدام Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إنشاء جداول ذات أعمدة مقفلة باستخدام Aspose.Note لـ .NET. دليل خطوة بخطوة لمهام معالجة المستندات بكفاءة.
type: docs
weight: 12
url: /ar/net/table-manipulation/create-table-locked-columns/
---
## مقدمة

يعد إنشاء الجداول ذات الأعمدة المقفلة متطلبًا شائعًا في تطبيقات معالجة المستندات. يوفر Aspose.Note for .NET أدوات قوية لإنجاز هذه المهمة بكفاءة. في هذا البرنامج التعليمي، سنرشدك خلال عملية إنشاء جدول بأعمدة مقفلة خطوة بخطوة باستخدام Aspose.Note لـ .NET.

## المتطلبات الأساسية

قبل البدء، تأكد من توفر المتطلبات الأساسية التالية:

- الفهم الأساسي للغة البرمجة C#.
- تم تثبيت Visual Studio على نظامك.
-  تم تثبيت Aspose.Note لـ .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/net/).
- - الإلمام بمفاهيم التعامل مع المستندات.

## استيراد مساحات الأسماء

أولاً، تحتاج إلى استيراد مساحات الأسماء الضرورية لمشروعك:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## الخطوة 1: تهيئة كائن المستند

ابدأ بإنشاء كائن من فئة المستند:

```csharp
Document doc = new Document();
```

## الخطوة 2: تهيئة كائن الصفحة

تهيئة كائن فئة الصفحة:

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## الخطوة 3: تهيئة كائنات TableRow

إنشاء كائنات TableRow للجدول:

```csharp
TableRow row1 = new TableRow(doc);
TableRow row2 = new TableRow(doc);
```

## الخطوة 4: تهيئة كائنات TableCell

قم بإنشاء كائنات TableCell وقم بتعيين محتوى النص لكل خلية:

```csharp
TableCell cell11 = new TableCell(doc);
cell11.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Small text"));

TableCell cell21 = new TableCell(doc);
cell21.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Long text with several words and spaces."));
```

## الخطوة 5: تهيئة كائن الجدول

قم بتهيئة كائن فئة الجدول وقم بتعيين خصائص مثل عرض العمود والعرض المقفل:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70, LockedWidth = true } }
};
```

## الخطوة 6: إضافة صفوف إلى الجدول

أضف الصفوف التي تمت تهيئتها إلى الجدول:

```csharp
table.AppendChildLast(row1);
table.AppendChildLast(row2);
```

## الخطوة 7: إضافة جدول إلى المخطط التفصيلي

أضف عقدة الجدول إلى OutlineElement:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
```

## الخطوة 8: إضافة مخطط تفصيلي إلى الصفحة

أضف عقدة المخطط التفصيلي إلى الصفحة:

```csharp
page.AppendChildLast(outline);
```

## الخطوة 9: حفظ المستند

احفظ المستند:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable with locked columns created successfully.\nFile saved at " + dataDir);
```

بعد اتباع هذه الخطوات، ستنجح في إنشاء جدول يحتوي على أعمدة مقفلة باستخدام Aspose.Note لـ .NET.

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية إنشاء جدول بأعمدة مقفلة باستخدام Aspose.Note لـ .NET. باتباع هذه الخطوات، يمكنك التعامل بكفاءة مع الجداول الموجودة في مستنداتك لتلبية متطلباتك المحددة.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص مظهر الجدول بشكل أكبر؟

ج1: نعم، يمكنك تخصيص جوانب مختلفة من الجدول مثل الحدود وتنسيق الخلايا والمزيد باستخدام الميزات التي يوفرها Aspose.Note لـ .NET.

### س2: هل Aspose.Note for .NET مناسب لمهام معالجة المستندات واسعة النطاق؟

ج2: بالتأكيد! تم تصميم Aspose.Note for .NET للتعامل مع مهام معالجة المستندات واسعة النطاق بكفاءة، مما يوفر أداءً عاليًا وموثوقية.

### س3: هل يمكنني دمج Aspose.Note لـ .NET مع أطر عمل .NET الأخرى؟

ج3: نعم، يتكامل Aspose.Note for .NET بسلاسة مع أطر عمل .NET الأخرى، مما يجعل من السهل دمج إمكانات معالجة المستندات في تطبيقاتك.

### س4: هل يتوفر الدعم الفني لـ Aspose.Note لـ .NET؟

 ج4: نعم، يمكنك الوصول إلى الدعم الفني من خلال[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) حيث يتوفر الخبراء لمساعدتك في أي أسئلة أو مشكلات قد تواجهها.

### س5: هل يمكنني تجربة Aspose.Note لـ .NET قبل الشراء؟

 ج5: نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.Note لـ .NET من[هنا](https://releases.aspose.com/)لتقييم مميزاته ومدى توافقه مع متطلباتك.