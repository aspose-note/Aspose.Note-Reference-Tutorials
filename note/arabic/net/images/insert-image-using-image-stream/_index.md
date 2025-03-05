---
title: إدراج الصور باستخدام Image Stream في Aspose.Note
linktitle: إدراج الصور باستخدام Image Stream في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إدراج الصور بسلاسة في مستندات Aspose.Note باستخدام تدفقات الصور في .NET. قم بتحسين ملفات الملاحظات الخاصة بك باستخدام العناصر المرئية دون عناء.
type: docs
weight: 11
url: /ar/net/images/insert-image-using-image-stream/
---
## مقدمة

في هذا البرنامج التعليمي، سوف نستكشف كيفية إدراج الصور في مستند Aspose.Note باستخدام تدفقات الصور في .NET. Aspose.Note عبارة عن واجهة برمجة تطبيقات قوية تتيح للمطورين العمل مع ملفات Microsoft OneNote برمجيًا. باتباع الخطوات الموضحة في هذا الدليل، ستتعلم كيفية دمج الصور بسلاسة في مستندات Note الخاصة بك، مما يعزز جاذبيتها المرئية ووظائفها العامة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:
1. بيئة التطوير: قم بإعداد بيئة تطوير بقدرات .NET.
2.  مكتبة Aspose.Note: قم بتنزيل وتثبيت Aspose.Note لمكتبة .NET. يمكنك العثور على رابط التحميل[هنا](https://releases.aspose.com/note/net/).
3. ملفات الصور: قم بإعداد ملفات الصور التي تنوي إدراجها في مستند الملاحظة الخاص بك.
4. الفهم الأساسي: تعرف على المفاهيم الأساسية للغة البرمجة C# ومعالجة الملفات.

## استيراد مساحات الأسماء
أولاً، لنستورد مساحات الأسماء الضرورية لمشروعنا. ستوفر مساحات الأسماء هذه إمكانية الوصول إلى الفئات والأساليب المطلوبة للعمل مع Aspose.Note والتعامل مع إدراج الصور.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

الآن، دعونا نقسم عملية إدراج الصور باستخدام تدفقات الصور إلى خطوات متعددة.

## الخطوة 1: تهيئة كائن المستند
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
Document doc = new Document();
```
نقوم بتهيئة مثيل جديد لفئة المستند، والذي يمثل مستند OneNote.

## الخطوة 2: إنشاء كائن الصفحة
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```
نقوم بإنشاء كائن صفحة جديد لإضافة محتوى إليه.

## الخطوة 3: تهيئة كائنات المخطط التفصيلي والعنصر التفصيلي
```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```
نقوم بإنشاء مثيلات لفئتي Outline وOutlineElement لتنظيم المحتوى الخاص بنا داخل الصفحة.

## الخطوة 4: تحميل الصورة من الدفق
```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```
نفتح ملف الصورة باستخدام FileStream ونحمله في كائن صورة. يمكننا تحديد خصائص مثل المحاذاة للصورة.

## الخطوة 5: إلحاق الصورة بـ OutlineElement
```csharp
outlineElem1.AppendChildLast(image1);
```
نقوم بإلحاق الصورة بـ OutlineElement، وإضافتها بشكل فعال إلى بنية المستند.

## الخطوة 6: إلحاق OutlineElement بالمخطط التفصيلي
```csharp
outline1.AppendChildLast(outlineElem1);
```
نقوم بإلحاق OutlineElement الذي يحتوي على الصورة بالمخطط التفصيلي.

## الخطوة 7: إلحاق المخطط التفصيلي بالصفحة
```csharp
page.AppendChildLast(outline1);
```
نلحق المخطط التفصيلي بالصفحة، ونضع اللمسات الأخيرة على بنية المحتوى.

## الخطوة 8: إلحاق الصفحة بالمستند
```csharp
doc.AppendChildLast(page);
```
نلحق الصفحة بالمستند، ونكمل تجميع المستند.

## الخطوة 9: حفظ المستند
```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```
وأخيرا، نقوم بحفظ الوثيقة المجمعة مع الصورة المدرجة.

## خاتمة
باتباع هذا البرنامج التعليمي، تعلمت كيفية إدراج الصور في مستندات Aspose.Note باستخدام تدفقات الصور في .NET. من خلال الاستفادة من إمكانيات Aspose.Note، يمكنك الآن دمج العناصر المرئية بسلاسة في ملفات Note الخاصة بك، مما يعزز فائدتها وجاذبيتها المرئية.

## الأسئلة الشائعة

### س1: هل يمكنني إدراج صور متعددة في مستند واحد باستخدام هذه الطريقة؟

A1: نعم، يمكنك إدراج صور متعددة في مستند واحد عن طريق تكرار خطوات إدراج الصورة لكل صورة.

### س2: هل يدعم Aspose.Note تنسيقات الصور الأخرى بخلاف JPG؟

ج2: نعم، يدعم Aspose.Note تنسيقات الصور المختلفة، بما في ذلك PNG وBMP وGIF وTIFF.

### س3: هل يمكنني تخصيص محاذاة وحجم الصور المدرجة؟

ج3: بالتأكيد، يوفر Aspose.Note خيارات شاملة لتخصيص المحاذاة والحجم والخصائص الأخرى للصور المدرجة.

### س 4: هل Aspose.Note متوافق مع كافة إصدارات .NET؟

ج4: يتوافق Aspose.Note for .NET مع إصدارات متعددة من .NET Framework، مما يضمن التوافق الواسع عبر بيئات التطوير المختلفة.

### س5: أين يمكنني العثور على موارد إضافية ودعم لـ Aspose.Note؟

 ج5: يمكنك العثور على وثائق ومنتديات ودعم شامل لـ Aspose.Note على موقع[منتدى أسبوز](https://forum.aspose.com/c/note/28).