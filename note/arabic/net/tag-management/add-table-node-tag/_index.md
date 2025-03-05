---
title: أضف عقدة الجدول مع العلامة في Aspose.Note
linktitle: أضف عقدة الجدول مع العلامة في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إضافة الجداول ذات العلامات في Aspose.Note لـ .NET. تعزيز مهارات التعامل مع المستندات الخاصة بك برمجيا.
type: docs
weight: 11
url: /ar/net/tag-management/add-table-node-tag/
---
## مقدمة

في هذا البرنامج التعليمي، سنرشدك خلال عملية إضافة عقدة جدول بعلامة باستخدام Aspose.Note لـ .NET. اتبع الخطوات أدناه لتحقيق ذلك.

## استيراد مساحات الأسماء

قبل البدء، تأكد من استيراد مساحات الأسماء اللازمة للعمل مع Aspose.ملاحظة:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## المتطلبات الأساسية

تأكد من إعداد المتطلبات الأساسية التالية قبل المتابعة:

1.  التثبيت: قم بتنزيل وتثبيت مكتبة Aspose.Note لـ .NET من[هنا](https://releases.aspose.com/note/net/).
2.  الترخيص: الحصول على ترخيص أو استخدام[ترخيص مؤقت](https://purchase.aspose.com/temporary-license/) لاستخدام المكتبة.
3. بيئة التطوير: قم بإعداد بيئة تطوير متوافقة، مثل Visual Studio.

## الخطوة 1: تهيئة كائنات المستند والصفحة

 ابدأ بإنشاء مثيل لـ`Document` فئة وتهيئة أ`Page` هدف:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## الخطوة 2: إنشاء كائنات الجدول والصف والخلية

 تهيئة`Table`, `TableRow` ، و`TableCell` أشياء:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## الخطوة 3: إدراج المحتوى في الخلية

 إضافة محتوى إلى الخلية باستخدام`AppendChildLast` طريقة:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## الخطوة 4: تهيئة عقدة الجدول

 تهيئة`Table` كائن ذو خصائص محددة:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## الخطوة 5: إضافة صف إلى الجدول

أضف عقدة الصف إلى الجدول:

```csharp
table.AppendChildLast(row);
```

## الخطوة 6: إضافة علامة إلى عقدة الجدول

قم بتضمين علامة لعقدة الجدول:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## الخطوة 7: إضافة عقدة الجدول إلى عنصر المخطط التفصيلي

 يخترع`Outline` و`OutlineElement` لإضافة عقدة الجدول:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## الخطوة 8: حفظ المستند

احفظ مستند OneNote:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

بعد اتباع هذه الخطوات، من المفترض أن تكون قد نجحت في إضافة عقدة جدول بعلامة باستخدام Aspose.Note لـ .NET.

## خاتمة

في هذا البرنامج التعليمي، قمنا بتغطية عملية إضافة عقدة جدول بعلامة في Aspose.Note لـ .NET. باتباع هذه الخطوات، يمكنك التعامل بكفاءة مع مستندات OneNote برمجياً، مما يعزز قدرات إدارة المستندات لديك.

## الأسئلة الشائعة

### س1: هل Aspose.Note متوافق مع كافة إصدارات .NET؟

A1: يدعم Aspose.Note for .NET إصدارات .NET Framework 2.0 والإصدارات الأحدث، بما في ذلك .NET Core و.NET Standard.

### س2: هل يمكنني تجربة Aspose.Note قبل شراء الترخيص؟

 ج2: نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Note من[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note؟

 ج3: يمكنك الحصول على ترخيص مؤقت من[هذا الرابط](https://purchase.aspose.com/temporary-license/)، والتي تكون صالحة لمدة 30 يومًا.

### س4: هل يدعم Aspose.Note تشفير المستندات؟

ج4: نعم، يوفر Aspose.Note الدعم لتشفير مستندات OneNote لضمان أمان البيانات.

### س5: هل يتوفر الدعم الفني لمستخدمي Aspose.Note؟

 ج5: نعم، يتم توفير الدعم الفني عبر منتديات Aspose[هنا](https://forum.aspose.com/c/note/28)حيث يمكنك طلب المساعدة من الخبراء.