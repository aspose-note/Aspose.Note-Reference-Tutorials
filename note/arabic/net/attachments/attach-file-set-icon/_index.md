---
date: 2026-04-03
description: تعلم كيفية تعيين أيقونة مخصصة وإرفاق ملفات في Aspose.Note لـ .NET، بما
  في ذلك حفظ ملفات OneNote واستخدام الصور كأيقونات.
keywords:
- set custom icon
- attach multiple files
- use image as icon
- save onenote file
- embed text file
linktitle: إرفاق ملف وتعيين أيقونة في Aspose.Note
second_title: Aspose.Note .NET API
title: تعيين أيقونة مخصصة وإرفاق ملف في Aspose.Note
url: /ar/net/attachments/attach-file-set-icon/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين أيقونة مخصصة وإرفاق ملف في Aspose.Note

## مقدمة

إذا كنت بحاجة إلى **تعيين أيقونة مخصصة** لمرفق في صفحة OneNote، فإن Aspose.Note لـ .NET يجعل ذلك بسيطًا. من خلال إرفاق ملف وتعيين صورة كأيقونته، يمكنك إنشاء ملاحظات أغنى وأكثر إيضاحًا وتظهر بالضبط كما تريد. في هذا البرنامج التعليمي سنستعرض العملية بالكامل—بدءًا من مستند جديد، إضافة مرفق، تطبيق أيقونة JPEG مخصصة، وأخيرًا حفظ ملف OneNote.

## إجابات سريعة
- **ماذا يعني “set custom icon”?** يتيح لك استبدال صورة المصغرة الافتراضية للمرفق بصورة تقدمها.  
- **هل يمكنني إرفاق ملفات متعددة؟** نعم، كرّر خطوات الإرفاق لكل ملف.  
- **ما صيغ الصور المدعومة للأيقونات؟** أي صيغة متوافقة مع .NET مثل JPEG أو PNG أو BMP أو GIF.  
- **هل أحتاج إلى ترخيص؟** يلزم وجود ترخيص صالح لـ Aspose.Note للاستخدام في الإنتاج؛ نسخة تجريبية مجانية تكفي للتقييم.  
- **كيف أحفظ ملف OneNote؟** استخدم `Document.Save()` وحدد مسار ملف *.one*.

## ما هو “set custom icon” في Aspose.Note؟
يعني تعيين أيقونة مخصصة إرفاق صورة محددة (مثل JPEG) لتمثيل ملف مرفق داخل صفحة OneNote. هذا يحسّن الإشارات البصرية للمستخدمين ويمكن استخدامه لعرض شعارات نوع الملف أو صور العلامة التجارية.

## لماذا تعيين أيقونة مخصصة للمرفقات؟
- **سياق بصري أفضل:** يتعرف المستخدمون فورًا على نوع أو غرض الملف المرفق.  
- **اتساق العلامة التجارية:** استخدم شعار شركتك كأيقونة لجميع المستندات ذات الصلة.  
- **تحسين تجربة المستخدم:** يجعل الملاحظات تبدو مصقولة ومهنية، خاصةً في دفاتر الملاحظات المشتركة.

## المتطلبات المسبقة

- معرفة أساسية ببرمجة C#.
- مكتبة Aspose.Note لـ .NET مثبتة.
- Visual Studio (أو أي بيئة تطوير متوافقة مع .NET) جاهزة للتطوير.

## استيراد مساحات الأسماء

أولاً، استورد مساحات الأسماء المطلوبة حتى تتمكن من العمل مع الملفات، الصور، وكائنات OneNote.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing.Imaging;
```

## دليل خطوة بخطوة لإرفاق ملف وتعيين أيقونته

### الخطوة 1: إنشاء كائن Document
مثيل `Document` جديد يمثل ملف OneNote الذي ستبنيه.

```csharp
Document doc = new Document();
```

### الخطوة 2: تهيئة كائن Page
كل ملف OneNote يحتوي على صفحة واحدة أو أكثر. هنا ننشئ الصفحة الأولى.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### الخطوة 3: تهيئة كائن Outline
تعمل الـ Outlines كحاويات لكتل المحتوى على الصفحة.

```csharp
Outline outline = new Outline(doc);
```

### الخطوة 4: تهيئة كائن OutlineElement
هذا العنصر سيحمل الملف المرفق وأيقونته المخصصة.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

### الخطوة 5: قراءة صورة الأيقونة وتهيئة كائن AttachedFile
نفتح تدفق الصورة (الأيقونة المخصصة) ونشير إلى الملف الذي نريد تضمينه.

```csharp
string dataDir = "Your Document Directory";
using (var stream = File.OpenRead(dataDir + "icon.jpg"))
{
    AttachedFile attachedFile = new AttachedFile(doc, dataDir + "attachment.txt", stream, ImageFormat.Jpeg);
}
```

> **نصيحة احترافية:** استبدل `ImageFormat.Jpeg` بـ `ImageFormat.Png` إذا كنت تفضّل أيقونة PNG.

### الخطوة 6: إلحاق الملف المرفق بـ OutlineElement
الآن يصبح الملف (مع أيقونته) عنصرًا فرعيًا لعنصر الـ outline.

```csharp
outlineElem.AppendChildLast(attachedFile);
```

### الخطوة 7: إلحاق OutlineElement بـ Outline
نضع العنصر داخل حاوية الـ outline.

```csharp
outline.AppendChildLast(outlineElem);
```

### الخطوة 8: إلحاق Outline بـ Page
نربط هيكل الـ outline بالكامل بالصفحة.

```csharp
page.AppendChildLast(outline);
```

### الخطوة 9: إلحاق Page بـ Document
نضيف الصفحة المكتملة إلى بنية المستند.

```csharp
doc.AppendChildLast(page);
```

### الخطوة 10: حفظ مستند OneNote
أخيرًا، نكتب المستند إلى القرص كملف *.one*.

```csharp
dataDir = dataDir + "AttachFileAndSetIcon_out.one";
doc.Save(dataDir);
```

## حالات الاستخدام الشائعة
- **إرفاق العقود:** إرفاق ملف PDF واستخدام أيقونة شعار العقد.  
- **مشاركة مقتطفات الشيفرة:** إرفاق ملف `.txt` بأيقونة “كود” مخصصة.  
- **توثيق المشروع:** إرفاق ملفات التصميم وتعيين صورة مصغرة تتطابق مع نوع الملف.

## المشكلات الشائعة والحلول
| المشكلة | الحل |
|-------|----------|
| **الأيقونة لا تظهر** | تحقق من أن صيغة الصورة تتطابق مع `ImageFormat` التي استخدمتها (مثال: JPEG مقابل PNG). |
| **أخطاء مسار الملف** | استخدم `Path.Combine(dataDir, "file.ext")` لتجنب مشاكل الشرط المفقودة. |
| **المرفقات الكبيرة تسبب بطء الأداء** | اضغط الملف مسبقًا أو قسّمه إلى مرفقات أصغر متعددة. |

## الأسئلة المتكررة

**س: هل يمكنني إرفاق ملفات متعددة إلى ملاحظة واحدة باستخدام Aspose.Note لـ .NET؟**  
**ج:** نعم. ما عليك سوى تكرار كتلة “Read the Icon Image and Initialize the AttachedFile Object” لكل ملف وإلحاق كل `AttachedFile` بنفس `OutlineElement` أو إنشاء عناصر منفصلة.

**س: هل من الممكن تعيين أيقونات مخصصة للمرفقات؟**  
**ج:** بالتأكيد. يتيح لك مُنشئ `AttachedFile` تمرير تدفق صورة وتحديد صيغة الصورة، مما يمنحك التحكم الكامل في الأيقونة.

**س: هل يدعم Aspose.Note صيغ صور أخرى لتعيين الأيقونات؟**  
**ج:** نعم. بالإضافة إلى JPEG، يمكنك استخدام PNG أو BMP أو GIF أو أي صيغة يدعمها `System.Drawing.Imaging.ImageFormat`.

**س: هل يمكنني إرفاق ملفات من عناوين URL خارجية؟**  
**ج:** رغم أن Aspose.Note يعمل مع التدفقات المحلية، يمكنك تنزيل ملف عبر `HttpClient`، تخزينه في `MemoryStream`، ثم تمرير هذا التدفق إلى `AttachedFile`.

**س: هل هناك حد لحجم المرفقات؟**  
**ج:** لا يفرض Aspose.Note حدًا ثابتًا، لكن الملفات الكبيرة جدًا قد تؤثر على استهلاك الذاكرة والأداء. يُنصح بضغط المرفقات الكبيرة.

**آخر تحديث:** 2026-04-03  
**تم الاختبار مع:** Aspose.Note 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}