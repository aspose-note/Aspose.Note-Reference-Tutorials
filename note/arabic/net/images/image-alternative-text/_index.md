---
date: 2026-04-09
description: تعلم كيفية إضافة نص بديل للصور في Aspose.Note لـ .NET بسهولة. عزّز إمكانية
  الوصول وحسّن تجربة المستخدم من خلال هذا الدليل خطوة بخطوة.
keywords:
- how to add alt text
- add alternative text image
- append image to page
linktitle: إضافة نص بديل للصور في Aspose.Note
second_title: Aspose.Note .NET API
title: كيفية إضافة نص بديل للصور في Aspose.Note
url: /ar/net/images/image-alternative-text/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة نص بديل للصور في Aspose.Note

## مقدمة

إذا كنت بحاجة إلى **كيفية إضافة نص بديل** للصور في مستنداتك على نمط OneNote، فأنت في المكان الصحيح. يشرح هذا البرنامج التعليمي الخطوات الدقيقة لإضافة نص بديل (العنوان والوصف) إلى صورة باستخدام Aspose.Note for .NET. إضافة النص البديل لا تعزز فقط إمكانية الوصول لمستخدمي قارئات الشاشة بل تحسن أيضًا تحسين محركات البحث لأي محتوى منشور على الويب يضم هذه الصور لاحقًا.

## إجابات سريعة
- **ما معنى “alt text”؟** وصف نصي يمثل الصورة عندما لا يمكن عرضها.  
- **لماذا نستخدم Aspose.Note للنص البديل؟** يوفر API بسيط لتعيين كل من العنوان والوصف برمجيًا.  
- **ما هي المتطلبات المسبقة؟** بيئة تطوير .NET، Visual Studio، وAspose.Note for .NET مثبتة.  
- **هل يمكنني إضافة نص بديل إلى الصور الموجودة؟** نعم – يمكنك تحميل كائن صورة، ضبط خصائصه، وحفظ المستند.  
- **أين يتم حفظ الناتج؟** في المسار الذي تحدده باستخدام `document.Save(...)`.

## ما هو “how to add alt text” في Aspose.Note؟

إضافة النص البديل يعني تعيين خصائص `AlternativeTextTitle` و `AlternativeTextDescription` لكائن `Image`. يتم قراءة هذه الخصائص بواسطة قارئات الشاشة وغيرها من تقنيات المساعدة لنقل معنى الصورة.

## لماذا نضيف نصًا بديلًا للصورة في مستندك؟

- **الامتثال لإمكانية الوصول** – يفي بإرشادات WCAG وSection 508.  
- **تحسين SEO** – تقوم محركات البحث بفهرسة النص الوصفي.  
- **تحسين تجربة المستخدم** – المستخدمون الذين عطلوا الصور لا يزالون يفهمون المحتوى.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

- معرفة أساسية بـ C# وتطوير .NET.  
- Visual Studio مثبتًا على جهازك.  
- Aspose.Note for .NET تم تنزيله وإضافته كمرجع في مشروعك – يمكنك الحصول عليه [هنا](https://releases.aspose.com/note/net/).  
- ملف صورة (مثال: `image.jpg`) تريد تضمينه.

## استيراد مساحات الأسماء

أولاً، قم بتضمين مساحات الأسماء المطلوبة للتعامل مع الملفات وكائنات Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## الخطوة 1: تهيئة المستند والصفحة

أنشئ كائن `Document` جديدًا وأضف `Page` حيث ستُوضع الصورة.

```csharp
var document = new Document();
var page = new Page(document);
```

## الخطوة 2: تحميل الصورة

حدد المجلد الذي يحتوي على صورتك وأنشئ كائن `Image`.

```csharp
string dataDir = "Your Document Directory";
var image = new Image(document, dataDir + "image.jpg");
```

## الخطوة 3: تعيين النص البديل

هنا نقوم **بإضافة نص بديل للصورة** عن طريق ملء حقلي العنوان والوصف.

```csharp
image.AlternativeTextTitle = "This is an image's title!";
image.AlternativeTextDescription = "And this is an image's description!";
```

## الخطوة 4: إلحاق الصورة بالصفحة

الآن نقوم **بإلحاق الصورة بالصفحة** باستخدام طريقة `AppendChildLast`.

```csharp
page.AppendChildLast(image);
```

## الخطوة 5: حفظ المستند

حدد اسم ملف الإخراج واحفظ مستند OneNote.

```csharp
dataDir = dataDir + "ImageAlternativeText_out.one";
document.Save(dataDir);
```

## الخطوة 6: عرض رسالة النجاح

رسالة بسيطة في وحدة التحكم تؤكد نجاح العملية.

```csharp
Console.WriteLine("\nImage alternative text setup successfully.\nFile saved at " + dataDir); 
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **النص البديل غير ظاهر** | ترك `AlternativeTextTitle` أو `AlternativeTextDescription` فارغًا | تأكد من تعيين كلا الخصائص قبل الحفظ. |
| **الملف غير موجود** | مسار `dataDir` غير صحيح | استخدم مسارًا مطلقًا أو تحقق من وجود المجلد النسبي. |
| **استثناء عند الحفظ** | أذونات كتابة غير كافية | شغّل Visual Studio كمسؤول أو اختر مجلدًا قابلًا للكتابة. |

## الأسئلة المتكررة

### س1: لماذا النص البديل مهم للصور؟

A1: يوفر النص البديل وصفًا نصيًا للصور، مما يجعلها متاحة للمستخدمين الذين يعتمدون على قارئات الشاشة أو الذين عطلوا الصور.

### س2: هل يمكنني إضافة نص بديل إلى الصور الموجودة في مستند؟

A2: نعم، يمكنك بسهولة إضافة نص بديل إلى الصور الموجودة بالفعل في مستند باستخدام Aspose.Note for .NET.

### س3: هل Aspose.Note متوافق مع مكتبات .NET الأخرى؟

A3: يتكامل Aspose.Note بسلاسة مع مكتبات .NET الأخرى، موفرًا وظائف شاملة لمعالجة المستندات.

### س4: كيف يمكنني الحصول على الدعم لـ Aspose.Note؟

A4: يمكنك الحصول على الدعم لـ Aspose.Note بزيارة [منتدى Aspose.Note](https://forum.aspose.com/c/note/28)، حيث يمكنك طرح الأسئلة وإيجاد الحلول.

### س5: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Note؟

A5: نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Note بزيارة [هنا](https://releases.aspose.com/).

## الخلاصة

إضافة النص البديل للصور هي خطوة صغيرة تحدث فرقًا كبيرًا في إمكانية الوصول، تحسين محركات البحث، وتجربة المستخدم العامة. باستخدام Aspose.Note for .NET، العملية بسيطة — فقط قم بتعيين خصائص `AlternativeTextTitle` و `AlternativeTextDescription`، ألحق الصورة، واحفظ المستند.

---

**آخر تحديث:** 2026-04-09  
**تم الاختبار مع:** Aspose.Note 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}