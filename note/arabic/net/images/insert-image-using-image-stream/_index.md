---
date: 2026-04-13
description: تعلم كيفية إضافة صورة إلى مستندات OneNote باستخدام تدفقات الصور في .NET
  مع Aspose.Note. يغطي هذا الدليل خطوة بخطوة تحميل الصور من التدفق، وإلحاقها بالمخططات،
  وحفظ الملف.
keywords:
- add image to onenote
- how to insert image
- load image from stream
- append image to outline
- image stream .net
linktitle: إضافة صورة إلى OneNote عبر تدفق الصورة باستخدام Aspose.Note
second_title: Aspose.Note .NET API
title: إضافة صورة إلى OneNote عبر تدفق الصورة باستخدام Aspose.Note
url: /ar/net/images/insert-image-using-image-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة صورة إلى OneNote عبر تدفق الصورة باستخدام Aspose.Note

## المقدمة

في هذا البرنامج التعليمي، ستكتشف **كيفية إضافة صورة إلى OneNote** المستندات عن طريق تحميل صورة من تدفق وإلحاقها بمخطط باستخدام Aspose.Note لـ .NET. سواءً كنت تبني أداة تقارير، أو تطبيق لتدوين الملاحظات، أو تقوم بأتمتة الوثائق، فإن إدراج الصور برمجياً يجعل ملفات OneNote أكثر جاذبية وفائدة.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.Note لـ .NET (يتوفر نسخة تجريبية مجانية).  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6+.  
- **هل يمكنني تحميل الصور من تدفق؟** نعم – استخدم `FileStream` أو أي تنفيذ لـ `Stream`.  
- **كيف يمكنني التحكم في محاذاة الصورة؟** عيّن خاصية `Alignment` (مثال: `HorizontalAlignment.Right`).  
- **ما تنسيق الملف الناتج؟** ملف OneNote (`.one`) يمكن فتحه في Microsoft OneNote.

## ما هو “إضافة صورة إلى OneNote”؟

إضافة صورة إلى ملف OneNote تعني تضمين عنصر بصري مباشرة داخل هيكل محتوى الصفحة. مع Aspose.Note، تتعامل مع كائنات مثل `Document` و `Page` و `Outline` و `OutlineElement`. من خلال إدراج كائن `Image` داخل `OutlineElement`، تصبح الصورة جزءًا من تخطيط صفحة OneNote.

## لماذا تستخدم Aspose.Note لإدراج الصور؟

- **لا حاجة لتثبيت Office** – إنشاء أو تعديل ملفات OneNote على الخادم.  
- **تحكم كامل في التخطيط** – محاذاة، تغيير حجم، وتحديد موضع الصور بدقة حيث تحتاجها.  
- **متوافق مع التدفق** – يعمل مع أي `Stream`، مثالي لتخزين السحابة أو السيناريوهات التي تعتمد على الذاكرة فقط.  
- **متعدد المنصات** – متوافق مع بيئات تشغيل .NET على Windows و Linux و macOS.

## المتطلبات المسبقة

1. **بيئة التطوير** – Visual Studio 2022 أو أي بيئة تطوير متوافقة مع .NET.  
2. **مكتبة Aspose.Note** – قم بتنزيلها من الموقع الرسمي [هنا](https://releases.aspose.com/note/net/).  
3. **ملفات الصور** – على الأقل صورة واحدة (JPG أو PNG أو BMP أو GIF أو TIFF) تريد تضمينها.  
4. **معرفة أساسية بـ C#** – الإلمام بمعالجة الملفات والبرمجة الكائنية.

## استيراد مساحات الأسماء
أولاً، استورد مساحات الأسماء التي تمنحنا الوصول إلى فئات Aspose.Note وأدوات الإدخال/الإخراج القياسية في .NET.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

الآن دعنا نتبع العملية خطوة بخطوة.

### الخطوة 1: تهيئة كائن Document
نبدأ بإنشاء نسخة جديدة من كائن `Document` الذي سيحمل ملف OneNote.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

### الخطوة 2: إنشاء كائن Page
يتكون ملف OneNote من صفحة واحدة أو أكثر. هنا نقوم بإنشاء صفحة جديدة لاستضافة المحتوى.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### الخطوة 3: تهيئة كائنات Outline و OutlineElement
المخططات (Outlines) هي حاويات للمحتوى الغني (نص، صور، جداول). `OutlineElement` هو عنصر فرعي يحمل العناصر فعليًا.

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```

### الخطوة 4: تحميل الصورة من تدفق
باستخدام `FileStream` (أو أي `Stream`) نقوم بقراءة ملف الصورة وإنشاء كائن `Image`. هنا يبرز مفهوم **تحميل الصورة من تدفق**.

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

### الخطوة 5: إلحاق الصورة بـ OutlineElement
الصورة الآن جزء من `OutlineElement`. توضح هذه الخطوة وظيفة **إلحاق الصورة بالمخطط**.

```csharp
outlineElem1.AppendChildLast(image1);
```

### الخطوة 6: إلحاق OutlineElement بالمخطط
نقوم الآن بربط العنصر (مع الصورة) بحاوية المخطط.

```csharp
outline1.AppendChildLast(outlineElem1);
```

### الخطوة 7: إلحاق المخطط بالصفحة
المخطط، الذي يحتوي على الصورة، يُضاف إلى الصفحة.

```csharp
page.AppendChildLast(outline1);
```

### الخطوة 8: إلحاق الصفحة بالوثيقة
مع جاهزية الصفحة، ندرجها في هيكل الوثيقة.

```csharp
doc.AppendChildLast(page);
```

### الخطوة 9: حفظ الوثيقة
أخيرًا، نقوم بحفظ ملف OneNote على القرص. يمكن فتح الملف الناتج في Microsoft OneNote.

```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|----------------|-----|
| **الصورة لا تظهر** | تم إغلاق التدفق قبل إضافة الصورة. | احتفظ بكتلة `using` حول استدعاء `AppendChildLast` (كما هو موضح). |
| **محاذاة غير صحيحة** | خاصية `Alignment` لم تُضبط أو تم استبدالها لاحقًا. | قم بضبط `Alignment` عند إنشاء `Image` أو عدّل `image1.Alignment` قبل الإلحاق. |
| **تنسيق صورة غير مدعوم** | محاولة تحميل تنسيق غير معترف به من قبل Aspose.Note. | حوّل الصورة إلى JPG أو PNG أو BMP أو GIF أو TIFF أولاً. |
| **أخطاء مسار الملف** | `dataDir` يشير إلى مجلد غير موجود. | استخدم `Path.Combine` وتأكد من وجود المجلد قبل التنفيذ. |

## الأسئلة المتكررة

**س: هل يمكنني إدراج صور متعددة في مستند واحد باستخدام هذه الطريقة؟**  
**ج:** نعم. ما عليك سوى تكرار خطوات *تحميل الصورة من تدفق* و *إلحاق الصورة بـ OutlineElement* لكل صورة.

**س: هل تدعم Aspose.Note تنسيقات صور أخرى غير JPG؟**  
**ج:** بالتأكيد. PNG و BMP و GIF و TIFF كلها مدعومة.

**س: هل يمكنني تخصيص محاذاة وحجم الصور المدخلة؟**  
**ج:** نعم. بالإضافة إلى `Alignment`، يمكنك ضبط خصائص `Width` و `Height` و `Scale` على كائن `Image`.

**س: هل Aspose.Note متوافق مع جميع إصدارات .NET؟**  
**ج:** يعمل مع .NET Framework 4.5+، .NET Core 3.1+، .NET 5، و .NET 6+.

**س: أين يمكنني العثور على موارد إضافية ودعم لـ Aspose.Note؟**  
**ج:** يمكنك العثور على وثائق شاملة، منتديات، ودعم على [منتدى Aspose](https://forum.aspose.com/c/note/28).

---

**آخر تحديث:** 2026-04-13  
**تم الاختبار مع:** Aspose.Note 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}