---
date: 2026-04-06
description: تعلم كيفية إنشاء مستند OneNote وإدراج صورة برمجيًا باستخدام Aspose.Note
  لـ .NET. اتبع خطوات سهلة لإضافة الصور، وتعيين المحاذاة، والمزيد.
keywords:
- create onenote document
- how to insert image
- insert image onenote
- set image alignment
- multiple images onenote
linktitle: إنشاء مستند وإدراج صورة في Aspose.Note
second_title: Aspose.Note .NET API
title: إنشاء مستند OneNote وإدراج صورة باستخدام Aspose.Note
url: /ar/net/images/build-doc-insert-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء مستند OneNote وإدراج صورة باستخدام Aspose.Note

## مقدمة

في هذا البرنامج التعليمي، ستقوم **بإنشاء مستند OneNote** وتتعلم **كيفية إدراج صورة** فيه باستخدام Aspose.Note لـ .NET. يمنحك Aspose.Note تحكمًا كاملاً في ملفات OneNote، مما يجعل من السهل إضافة محتوى غني مثل الصور والجداول وتخطيطات مخصصة برمجيًا.

## إجابات سريعة
- **ما هو الهدف الأساسي؟** لإنشاء مستند OneNote وإدراج صورة مع محاذاة مخصصة.  
- **ما المكتبة المطلوبة؟** Aspose.Note for .NET (تحميل [هنا](https://releases.aspose.com/note/net/)).  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تعمل للتطوير؛ يتطلب الترخيص المدفوع للإنتاج.  
- **هل يمكنني إضافة صور متعددة؟** نعم – كرّر خطوات الإدراج لكل صورة (انظر نصيحة “multiple images onenote”).  
- **هل يدعم التحويل إلى PDF؟** بالتأكيد – يمكنك لاحقًا تحويل مستند OneNote إلى PDF باستخدام طريقة `Save` في Aspose.Note مع تنسيق PDF.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من توفر المتطلبات التالية:

1. **Visual Studio** – بيئة تطوير متكاملة كاملة للـ .NET.  
2. **Aspose.Note for .NET** – قم بتحميل وتثبيت المكتبة من الموقع الرسمي.  
3. **فهم أساسي لـ C#** – الإلمام بتركيب C# سيساعدك على متابعة أمثلة الشيفرة.

## استيراد مساحات الأسماء

لنبدأ باستيراد مساحات الأسماء الضرورية إلى مشروع C# الخاص بك. تحتوي هذه المساحات على فئات وأساليب سنستخدمها لتنفيذ مهام تعديل المستند.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

الآن، دعنا نقسم عملية بناء المستند وإدراج صورة إلى خطوات متعددة:

## الخطوة 1: إنشاء كائن Document

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document();
```

هذا السطر من الشيفرة يُنشئ نسخة جديدة من الفئة `Document`، التي تمثل مستند OneNote.

## الخطوة 2: تهيئة كائن Page

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

هنا، نقوم بتهيئة نسخة جديدة من الفئة `Page`، التي تمثل صفحة داخل مستند OneNote.

## الخطوة 3: تهيئة كائن Outline

```csharp
Outline outline = new Outline(doc);
```

الفئة `Outline` تمثل عقدة مخطط في هيكل المستند. نقوم بإنشاء كائن مخطط جديد لتنظيم مستندنا.

## الخطوة 4: تهيئة كائن OutlineElement

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

`OutlineElement` تمثل عنصرًا داخل المخطط. هنا، ننشئ عنصر مخطط جديد لإضافة محتوى إلى مستندنا.

## الخطوة 5: تحميل الصورة

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg");
```

نقوم بتحميل ملف صورة من المسار المحدد باستخدام مُنشئ الفئة `Image`.

## الخطوة 6: تعيين محاذاة الصورة

```csharp
image.Alignment = HorizontalAlignment.Right;
```

هذا السطر يحدد **محاذاة الصورة** إلى الجانب الأيمن من الصفحة. يمكنك أيضًا اختيار `Left` أو `Center` حسب احتياجات التخطيط.

## الخطوة 7: إضافة الصورة إلى عنصر المخطط

```csharp
outlineElem.AppendChildLast(image);
```

هنا، نضيف الصورة إلى عنصر المخطط، موضعها داخل هيكل المستند.

## الخطوة 8: إضافة عنصر المخطط إلى المخطط

```csharp
outline.AppendChildLast(outlineElem);
```

نضيف عنصر المخطط، مع الصورة المُدخلة، إلى هيكل المخطط في المستند.

## الخطوة 9: إضافة المخطط إلى الصفحة

```csharp
page.AppendChildLast(outline);
```

يتم إضافة المخطط، الذي يحتوي على الصورة، إلى هيكل الصفحة في المستند.

## الخطوة 10: إضافة الصفحة إلى المستند

```csharp
doc.AppendChildLast(page);
```

أخيرًا، نضيف الصفحة، مكتملة بمحتواها، إلى المستند.

## الخطوة 11: حفظ المستند

```csharp
dataDir = dataDir + "BuildDocAndInsertImage_out.one";
doc.Save(dataDir);
```

هذا السطر يحفظ مستند OneNote المعدل إلى الموقع المحدد. يمكنك لاحقًا **تحويل OneNote إلى PDF** عن طريق استدعاء `doc.Save("output.pdf")`.

## لماذا هذا مهم

- **الأتمتة** – إنشاء مستندات OneNote برمجيًا يوفر الوقت مقارنةً بالتحرير اليدوي.  
- **الاتساق** – استخدام الشيفرة يضمن أن كل مستند يتبع نفس قواعد التخطيط والتنسيق.  
- **القابلية للتوسع** – يمكن توسيع النهج نفسه لإدراج **multiple images onenote** أو إنشاء تقارير بكميات كبيرة.

## المشكلات الشائعة والنصائح

- **مشكلات المسار** – تأكد دائمًا من أن `dataDir` يشير إلى مجلد صالح؛ وإلا سيفشل تحميل الصورة.  
- **حجم الصورة** – الصور الكبيرة يمكن أن تزيد حجم الملف بشكل كبير؛ فكر في تغيير الحجم قبل الإدراج.  
- **صور متعددة** – لإضافة أكثر من صورة، كرّر الخطوات 5‑7 لكل صورة وأضف كل واحدة إلى نفس أو مختلف `OutlineElement`.

## الأسئلة المتكررة

### س1: هل يمكنني إدراج صور متعددة في مستند واحد باستخدام Aspose.Note for .NET؟

ج1: بالتأكيد! يمكنك إدراج عدد غير محدود من الصور في المستند باتباع نفس خطوات الإدراج لكل صورة.

### س2: هل يدعم Aspose.Note صيغ ملفات أخرى غير OneNote؟

ج2: نعم، يوفر Aspose.Note دعمًا واسعًا لصيغ ملفات متعددة، بما في ذلك PDF، DOCX، HTML، وأكثر.

### س3: هل Aspose.Note مناسب لحلول إدارة المستندات على مستوى المؤسسات؟

ج3: بالتأكيد! يقدم Aspose.Note ميزات قوية وأداء ممتاز، مما يجعله خيارًا مثاليًا لإدارة المستندات على مستوى المؤسسات.

### س4: هل يمكنني تخصيص مظهر الصور المدخلة في المستند؟

ج4: نعم، يوفر Aspose.Note خيارات شاملة لتخصيص مظهر الصورة، بما في ذلك المحاذاة، الحجم، والدوران.

### س5: أين يمكنني العثور على موارد إضافية ودعم لـ Aspose.Note for .NET؟

ج5: يمكنك استكشاف وثائق Aspose.Note [هنا](https://reference.aspose.com/note/net/) وطلب المساعدة من منتدى مجتمع Aspose [هنا](https://forum.aspose.com/c/note/28/).

---

**آخر تحديث:** 2026-04-06  
**تم الاختبار مع:** Aspose.Note 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}