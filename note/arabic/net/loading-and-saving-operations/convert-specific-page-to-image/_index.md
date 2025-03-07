---
title: تحويل صفحة معينة إلى صورة في Aspose.Note
linktitle: تحويل صفحة معينة إلى صورة في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية تحويل صفحات معينة من مستندات Microsoft OneNote إلى صور برمجياً باستخدام Aspose.Note لـ .NET.
weight: 11
url: /ar/net/loading-and-saving-operations/convert-specific-page-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل صفحة معينة إلى صورة في Aspose.Note

## مقدمة

Aspose.Note for .NET عبارة عن واجهة برمجة تطبيقات قوية تمكن المطورين من العمل مع مستندات Microsoft OneNote برمجيًا. سواء كنت بحاجة إلى استخراج المحتوى، أو تحويل المستندات إلى تنسيقات أخرى، أو معالجة العناصر داخل ملف OneNote، فإن Aspose.Note for .NET يوفر وظائف شاملة لتبسيط مهامك. في هذا البرنامج التعليمي، سنستكشف كيفية استخدام Aspose.Note لـ .NET لتحويل صفحات معينة من مستند OneNote إلى صور. سنقوم بتغطية المتطلبات الأساسية، واستيراد مساحات الأسماء، وتقديم إرشادات خطوة بخطوة حول تنفيذ عملية التحويل.

## المتطلبات الأساسية

قبل أن نتعمق في استخدام Aspose.Note for .NET لتحويل صفحات OneNote إلى صور، تأكد من أن لديك ما يلي:

- Visual Studio: تأكد من تثبيت Visual Studio على نظامك.
-  Aspose.Note لـ .NET: قم بتنزيل Aspose.Note لـ .NET وتثبيته من[هنا](https://releases.aspose.com/note/net/).
- Microsoft OneNote: ستحتاج إلى تثبيت OneNote على نظامك لإنشاء مستندات OneNote أو الحصول عليها.

## استيراد مساحات الأسماء

في مشروع C# الخاص بك، قم باستيراد مساحات الأسماء الضرورية للوصول إلى Aspose.Note لفئات وأساليب .NET.

```csharp
using System;
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
```

## تحويل صفحة معينة إلى صورة

لننتقل الآن خلال عملية تحويل صفحة معينة من مستند OneNote إلى صورة باستخدام Aspose.Note لـ .NET.

### الخطوة 1: قم بتحميل المستند

```csharp
string dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

### الخطوة 2: تهيئة ImageSaveOptions

```csharp
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png)
{
    PageIndex = 1 // قم بتعيين فهرس الصفحة للتحويل
};
```

### الخطوة 3: احفظ المستند بصيغة PNG

```csharp
dataDir = dataDir + "ConvertSpecificPageToImage_out.png";
oneFile.Save(dataDir, opts);
```

## ضبط دقة صورة الإخراج

يمكنك أيضًا ضبط دقة الصورة الناتجة عند حفظ المستند كصورة.

### الخطوة 1: قم بتحميل المستند

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

### الخطوة 2: ضبط دقة صورة الإخراج

```csharp
dataDir = dataDir + "SetOutputImageResolution_out.jpg";
doc.Save(dataDir, new ImageSaveOptions(SaveFormat.Jpeg) { Resolution = 220 });
```

## خاتمة

يعمل Aspose.Note for .NET على تبسيط مهمة تحويل صفحات محددة من مستندات OneNote إلى صور برمجيًا. باتباع الخطوات الموضحة في هذا البرنامج التعليمي، يمكنك دمج هذه الوظيفة بكفاءة في تطبيقات .NET الخاصة بك، مما يعزز الإنتاجية ويوسع قدراتك باستخدام ملفات OneNote.

## الأسئلة الشائعة

### س1: هل يمكنني تحويل صفحات متعددة مرة واحدة باستخدام Aspose.Note لـ .NET؟

A1: نعم، يمكنك تكرار الصفحات وتحويلها بشكل فردي أو جماعي.

### س2: هل يدعم Aspose.Note for .NET تنسيقات الإخراج الأخرى إلى جانب PNG وJPEG؟

ج2: نعم، يدعم Aspose.Note for .NET تنسيقات الإخراج المختلفة لتحويل الصور.

### س3: هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ .NET؟

 ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).

### س4: هل يمكنني ضبط جودة الصورة عند التحويل إلى JPEG؟

ج4: نعم، يمكنك ضبط جودة الصورة وفقًا لمتطلباتك.

### س5: أين يمكنني الحصول على دعم Aspose.Note لـ .NET؟

 ج5: يمكنك الحصول على الدعم من مجتمع Aspose.Note لـ .NET[المنتدى](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
