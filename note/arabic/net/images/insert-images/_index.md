---
title: إدراج الصور في مستندات Aspose.Note
linktitle: إدراج الصور في مستندات Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إدراج الصور بسلاسة في مستندات Aspose.Note باستخدام .NET للمحتوى المرئي المحسن. اتبع دليلنا خطوة بخطوة لسهولة التكامل.
weight: 16
url: /ar/net/images/insert-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدراج الصور في مستندات Aspose.Note

## مقدمة

يمكن أن تؤدي إضافة الصور إلى مستندات Aspose.Note الخاصة بك إلى تحسين جاذبيتها وفائدتها البصرية بشكل كبير. سواء كنت تقوم بإنشاء ملاحظات أو عروض تقديمية أو أي مستند آخر، فإن دمج الصور يمكن أن يوفر السياق والوضوح للمحتوى الخاص بك. في هذا البرنامج التعليمي، سنرشدك خلال عملية إدراج الصور في مستندات Aspose.Note الخاصة بك باستخدام .NET.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

1.  Aspose.Note لـ .NET: قم بتنزيل Aspose.Note لـ .NET وتثبيته من[هنا](https://releases.aspose.com/note/net/).
   
2. ملفات الصور: قم بإعداد ملفات الصور التي تنوي إدراجها في مستندات Aspose.Note الخاصة بك.

## استيراد مساحات الأسماء

أولاً، تحتاج إلى استيراد مساحات الأسماء الضرورية للعمل مع Aspose.Note في مشروع .NET الخاص بك. وإليك كيف يمكنك القيام بذلك:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## الخطوة 1: تحميل المستند والحصول على الصفحة

ابدأ بتحميل مستند Aspose.Note الموجود لديك والوصول إلى الصفحة المطلوبة حيث تريد إدراج الصورة.

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## الخطوة 2: تحميل الصورة وتعيين الخصائص

بعد ذلك، قم بتحميل الصورة التي تريد إدراجها وحدد خصائصها مثل العرض والارتفاع والإزاحات والمحاذاة وفقًا لمتطلباتك.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // ضبط عرض الصورة
    Height = 100,               // ضبط ارتفاع الصورة
    HorizontalOffset = 100,     // تعيين الإزاحة الأفقية
    VerticalOffset = 400,       // تعيين الإزاحة العمودية
    Alignment = HorizontalAlignment.Right  // ضبط محاذاة الصورة
};
```

## الخطوة 3: إضافة صورة إلى الصفحة

بمجرد قيامك بتكوين خصائص الصورة، قم بإضافة الصورة إلى الصفحة المطلوبة في مستند Aspose.Note الخاص بك.

```csharp
page.AppendChildLast(image);
```

## خاتمة

تهانينا! لقد نجحت في إدراج صورة في مستند Aspose.Note الخاص بك باستخدام .NET. يمكن للصور تحسين التمثيل المرئي لمستنداتك بشكل كبير، مما يجعلها أكثر جاذبية وغنية بالمعلومات.

## الأسئلة الشائعة

### س1: هل يمكنني إدراج صور بأي تنسيق في مستندات Aspose.Note؟

ج1: نعم، يدعم Aspose.Note تنسيقات الصور المختلفة بما في ذلك JPG وPNG وBMP وGIF وما إلى ذلك.

### س2: هل يمكن تغيير حجم الصور المدرجة برمجياً؟

ج2: بالتأكيد! يمكنك ضبط عرض الصور وارتفاعها وفقًا لتفضيلاتك أثناء الإدراج.

### س3: هل يوفر Aspose.Note خيارات لتعديل محاذاة الصورة؟

ج3: نعم، يمكنك محاذاة الصور إلى اليسار أو اليمين أو المركز داخل صفحات المستند.

### س 4: هل يمكنني إدراج صور متعددة في صفحة واحدة من المستند؟

ج4: بالتأكيد! يمكنك إدراج أي عدد تريده من الصور في صفحة واحدة باستخدام Aspose.Note.

### س5: هل هناك حد لحجم ملف الصور الذي يمكن إدراجه؟

ج5: لا يفرض Aspose.Note قيودًا صارمة على أحجام ملفات الصور، ولكن يوصى بتحسين الصور للحصول على أداء أفضل.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
