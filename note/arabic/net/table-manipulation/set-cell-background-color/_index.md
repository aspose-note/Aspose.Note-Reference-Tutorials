---
title: تعيين لون خلفية الخلية في جداول Aspose.Note
linktitle: تعيين لون خلفية الخلية في جداول Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية تعيين لون خلفية الخلية في جداول Aspose.Note باستخدام دليل خطوة بخطوة. قم بتحسين صور المستندات دون عناء.
weight: 17
url: /ar/net/table-manipulation/set-cell-background-color/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين لون خلفية الخلية في جداول Aspose.Note

## مقدمة

في هذا البرنامج التعليمي، سوف نتعمق في كيفية تعيين لون خلفية الخلية داخل الجداول باستخدام Aspose.Note لـ .NET. يمكن لهذه الميزة أن تعزز بشكل كبير المظهر المرئي وسهولة قراءة مستنداتك. اتبع الخطوات أدناه لمعرفة كيفية تحقيق ذلك.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

1.  تثبيت Aspose.Note لـ .NET: تأكد من أنك قمت بتثبيت Aspose.Note لـ .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/net/).
2. الإلمام بـ C#: الفهم الأساسي للغة البرمجة C# مطلوب لتنفيذ مقتطفات التعليمات البرمجية المتوفرة.

## استيراد مساحات الأسماء

أولاً، لنستورد مساحات الأسماء الضرورية لمشروعنا:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## الخطوة 1: إنشاء كائن مستند

تهيئة كائن المستند:

```csharp
Document doc = new Document();
```

## الخطوة 2: تهيئة TableCell وتعيين محتوى النص

قم بإنشاء كائن TableCell وقم بتعيين محتوى النص الخاص به مع لون الخلفية:

```csharp
TableCell cell11 = new TableCell(doc);
cell11.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Small text"));
cell11.BackgroundColor = Color.Coral;
```

## الخطوة 3: تهيئة TableRow وإلحاق الخلية

تهيئة كائن TableRow وإلحاق الخلية التي تم إنشاؤها مسبقًا:

```csharp
TableRow row = new TableRow(doc);
row.AppendChildLast(cell11);
```

## الخطوة 4: إنشاء جدول بالأعمدة المحددة

قم بإنشاء جدول بأعمدة محددة وجعل حدوده مرئية:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn() { Width = 200 } }
};
table.AppendChildLast(row);
```

## الخطوة 5: إنشاء عنصر المخطط التفصيلي والصفحة

قم بإنشاء عنصر مخطط تفصيلي وصفحة، ثم قم بإلحاق الجدول بالصفحة:

```csharp
OutlineElement oe = new OutlineElement(doc);
oe.AppendChildLast(table);

Outline o = new Outline(doc);
o.AppendChildLast(oe);

Page page = new Page(doc);
page.AppendChildLast(o);

doc.AppendChildLast(page);
```

## الخطوة 6: حفظ المستند

احفظ المستند بالدليل المحدد واسم الملف:

```csharp
doc.Save(Path.Combine("Your Document Directory", "SettingCellBackGroundColor.pdf"));
```

باتباع هذه الخطوات، تكون قد نجحت في تعيين لون خلفية الخلية داخل الجداول باستخدام Aspose.Note لـ .NET.

## خاتمة

في الختام، يوفر Aspose.Note for .NET طريقة ملائمة وفعالة لمعالجة خصائص الجدول، مثل تعيين ألوان خلفية الخلية. بفضل واجهة برمجة التطبيقات البديهية والوثائق الشاملة، يمكنك بسهولة تحسين العرض المرئي لمستنداتك.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص لون الخلفية بشكل أكبر، مثل استخدام التدرجات أو الأنماط؟

A1: يدعم Aspose.Note for .NET الألوان الصلبة لخلفيات الخلايا. ومع ذلك، يمكنك محاكاة التدرجات أو الأنماط باستخدام الصور كخلفيات.

### س2: هل يدعم Aspose.Note for .NET خيارات تنسيق الجدول الأخرى؟

ج2: نعم، يوفر Aspose.Note for .NET خيارات شاملة لتنسيق الجدول، بما في ذلك حدود الخلايا ومحاذاة النص وعرض الأعمدة.

### س3: هل من الممكن تغيير ألوان خلفية الخلية ديناميكيًا بناءً على شروط معينة؟

ج3: بالتأكيد، يمكنك تعديل خصائص الخلية برمجيًا، بما في ذلك ألوان الخلفية، استنادًا إلى أي شروط تحددها في منطق التطبيق الخاص بك.

### س4: هل يمكنني استخدام Aspose.Note لـ .NET للعمل مع الجداول بتنسيقات مستندات أخرى مثل Word أو Excel؟

A4: يستهدف Aspose.Note for .NET تنسيقات ملفات OneNote بشكل خاص. للعمل مع الجداول في مستندات Word أو Excel، يمكنك استخدام Aspose.Words أو Aspose.Cells، على التوالي.

### س5: أين يمكنني العثور على المزيد من الموارد والدعم لـ Aspose.Note لـ .NET؟

 ج5: يمكنك استكشاف[Aspose.Note الوثائق](https://reference.aspose.com/note/net/) للحصول على مراجع وأمثلة تفصيلية لواجهة برمجة التطبيقات. بالإضافة إلى ذلك، يمكنك طلب المساعدة من مجتمع Aspose على[منتدى Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
