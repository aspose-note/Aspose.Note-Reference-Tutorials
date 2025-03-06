---
title: إدراج الجداول في مستندات Aspose.Note
linktitle: إدراج الجداول في مستندات Aspose.Note
second_title: Aspose.Note .NET API
description: تعلم كيفية إدراج الجداول في مستندات Note باستخدام Aspose.Note لـ .NET. قم بتنظيم البيانات بسلاسة لتحسين إمكانية القراءة والعرض.
weight: 16
url: /ar/net/table-manipulation/insert-tables/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدراج الجداول في مستندات Aspose.Note

## مقدمة

في هذا البرنامج التعليمي، سوف نستكشف كيفية استخدام Aspose.Note لـ .NET لإدراج الجداول في مستندات Note. تعد الجداول ضرورية لتنظيم البيانات بتنسيق منظم داخل المستندات، وتعزيز إمكانية القراءة، وتقديم المعلومات بطريقة واضحة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:
- الفهم الأساسي للغة البرمجة C#.
- تم تثبيت Aspose.Note لـ .NET SDK.
- بيئة التطوير المتكاملة (IDE) مثل Visual Studio.

## استيراد مساحات الأسماء

قبل المتابعة، قم باستيراد مساحات الأسماء الضرورية:
```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## الخطوة 1: تهيئة كائنات المستند والصفحة

للبدء، قم بإنشاء مستند ملاحظة جديد وقم بتهيئة صفحة بداخله.
```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## الخطوة 2: إنشاء صفوف وخلايا الجدول

بعد ذلك، قم بتهيئة صفوف وخلايا الجدول لهيكلة الجدول الخاص بك.
```csharp
TableRow row1 = new TableRow(doc);
TableCell cell11 = new TableCell(doc);
TableCell cell12 = new TableCell(doc);
TableCell cell13 = new TableCell(doc);
```

## الخطوة 3: ملء خلايا الجدول

أضف محتوى إلى كل خلية في الجدول.
```csharp
cell11.AppendChildLast(GetOutlineElementWithText(doc, "cell_1.1"));
cell12.AppendChildLast(GetOutlineElementWithText(doc, "cell_1.2"));
cell13.AppendChildLast(GetOutlineElementWithText(doc, "cell_1.3"));
```

## الخطوة 4: إضافة صفوف إلى الجدول

إلحاق الخلايا بالصفوف الخاصة بها.
```csharp
row1.AppendChildLast(cell11);
row1.AppendChildLast(cell12);
row1.AppendChildLast(cell13);
```

## الخطوة 5: تهيئة الجدول وتكوينه

قم بإنشاء كائن الجدول وقم بتعيين خصائصه، مثل رؤية الحدود وعرض الأعمدة.
```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 200 }, new TableColumn { Width = 200 }, new TableColumn { Width = 200 } }
};
```

## الخطوة 6: إضافة صفوف إلى الجدول

إلحاق الصفوف التي تحتوي على خلايا بالجدول.
```csharp
table.AppendChildLast(row1);
table.AppendChildLast(row2);
```

## الخطوة 7: إضافة جدول إلى بنية الوثيقة

قم بدمج الجدول في بنية المستند عن طريق إضافته إلى المخطط التفصيلي.
```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## الخطوة 8: حفظ المستند

وأخيرًا، احفظ المستند بالجدول المدرج.
```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "InsertTable_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable inserted successfully.\nFile saved at " + dataDir);
```

## خاتمة

في الختام، يوفر استخدام Aspose.Note for .NET طريقة سلسة لإدراج الجداول في مستندات Note، مما يعزز تنظيم المستندات وسهولة قراءتها.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص مظهر الجدول بشكل أكبر؟

A1: نعم، يمكنك ضبط خصائص مختلفة مثل نمط الحدود ومساحة الخلية والمحاذاة لتخصيص الجدول وفقًا لمتطلباتك.

### س2: هل Aspose.Note متوافق مع أطر عمل .NET الأخرى؟

ج2: يدعم Aspose.Note .NET Framework و.NET Core و.NET Standard، مما يضمن التوافق عبر الأنظمة الأساسية المختلفة.

### س3: هل يمكنني إدراج جداول متداخلة باستخدام Aspose.Note؟

ج3: نعم، يمكنك دمج الجداول داخل بعضها البعض لإنشاء تخطيطات وبنيات معقدة داخل مستنداتك.

### س4: كيف يمكنني دمج Aspose.Note في طلبي؟

ج4: التكامل واضح ومباشر؛ ما عليك سوى إضافة مرجع Aspose.Note DLL إلى مشروعك والبدء في الاستفادة من ميزاته.

### س 5: هل يقدم Aspose.Note الدعم لتنسيقات الملفات المختلفة؟

ج5: نعم، يدعم Aspose.Note تنسيقات الملفات المختلفة بما في ذلك تنسيقات OneNote (ONE) وPDF وHTML وتنسيقات الصور لتصدير المستندات واستيرادها.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
