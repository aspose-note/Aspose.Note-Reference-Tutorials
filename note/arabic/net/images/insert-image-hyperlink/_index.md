---
title: إدراج الصور باستخدام الارتباطات التشعبية في Aspose.Note
linktitle: إدراج الصور باستخدام الارتباطات التشعبية في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إدراج الصور باستخدام الارتباطات التشعبية في Aspose.Note لـ .NET دون عناء. تعزيز تفاعل المستند مع الصور القابلة للنقر.
weight: 15
url: /ar/net/images/insert-image-hyperlink/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدراج الصور باستخدام الارتباطات التشعبية في Aspose.Note

## مقدمة

يوفر Aspose.Note for .NET مجموعة قوية من الميزات للتعامل مع الصور، بما في ذلك القدرة على إدراج الصور باستخدام الارتباطات التشعبية. في هذا البرنامج التعليمي، سنرشدك خلال عملية إدراج الصور ذات الارتباطات التشعبية باستخدام Aspose.Note لـ .NET.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1.  Aspose.Note لـ .NET: تأكد من تثبيت Aspose.Note لـ .NET. إذا لم يكن الأمر كذلك، يمكنك تنزيله من[هنا](https://releases.aspose.com/note/net/).
2. بيئة التطوير: قم بإعداد بيئة التطوير الخاصة بك باستخدام .NET Framework.
3. الصورة: اجعل الصورة التي تريد إدراجها جاهزة في دليل المستندات.
4. المعرفة الأساسية: الإلمام بـ C# و.NET Framework.

## استيراد مساحات الأسماء

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## الخطوة 1: تهيئة المستند والصفحة

أولاً، نحتاج إلى تهيئة مستند جديد وإنشاء صفحة لإدراج صورتنا.

```csharp
var document = new Document();
var page = new Page(document);
```

## الخطوة 2: إدراج صورة باستخدام الارتباط التشعبي

الآن، دعونا نقوم بإدراج الصورة مع رابط تشعبي. سنقوم بإنشاء`Image` الكائن وتعيينه`HyperlinkUrl` الخاصية إلى عنوان URL المطلوب.

```csharp
string imagePath = "path_to_your_image.jpg";
var image = new Image(document, imagePath) { HyperlinkUrl = "http://example.com" };
```

## الخطوة 3: إلحاق الصورة بالصفحة

بعد ذلك، قم بإلحاق الصورة بالصفحة.

```csharp
page.AppendChildLast(image);
```

## الخطوة 4: إلحاق الصفحة بالمستند

وأخيرًا، قم بإلحاق الصفحة بالمستند وحفظه.

```csharp
document.AppendChildLast(page);
document.Save("path_to_output_file.one");
```

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية إدراج الصور ذات الارتباطات التشعبية باستخدام Aspose.Note لـ .NET. باتباع هذه الخطوات، يمكنك دمج الصور بسلاسة مع الارتباطات التشعبية القابلة للنقر عليها في مستنداتك، مما يعزز تفاعلها ووظائفها.

## الأسئلة الشائعة

### س1: هل يمكنني إدراج صور متعددة تحتوي على ارتباطات تشعبية في مستند واحد؟

ج1: نعم، يمكنك إدراج أي عدد من الصور ذات الارتباطات التشعبية حسب الحاجة في مستند واحد باستخدام Aspose.Note لـ .NET.

### س2: هل يدعم Aspose.Note تنسيقات الصور المختلفة؟

ج2: نعم، يدعم Aspose.Note تنسيقات الصور المختلفة، بما في ذلك JPEG وPNG وGIF وBMP وما إلى ذلك.

### س3: هل يمكنني تخصيص مظهر الارتباطات التشعبية؟

ج3: نعم، يمكنك تخصيص مظهر الارتباطات التشعبية، بما في ذلك تأثيرات اللون والتسطير والتحويم، باستخدام Aspose.Note لـ .NET.

### س4: هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ .NET؟

 ج4: نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.Note لـ .NET من[هنا](https://releases.aspose.com/).

### س5: أين يمكنني الحصول على دعم Aspose.Note لـ .NET؟

 ج5: يمكنك الحصول على دعم Aspose.Note لـ .NET من[منتديات Aspose.Note](https://forum.aspose.com/c/note/28)، حيث يمكنك طرح الأسئلة وطلب التوجيه والتفاعل مع المستخدمين والخبراء الآخرين.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
