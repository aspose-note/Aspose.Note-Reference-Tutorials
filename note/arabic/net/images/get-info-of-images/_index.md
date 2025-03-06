---
title: احصل على معلومات الصور في Aspose.Note
linktitle: احصل على معلومات الصور في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية استخراج معلومات الصورة من ملفات Microsoft OneNote باستخدام Aspose.Note لـ .NET. اتبع دليلنا خطوة بخطوة للتطوير الفعال.
weight: 13
url: /ar/net/images/get-info-of-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# احصل على معلومات الصور في Aspose.Note

## مقدمة

في عالم تطوير .NET، يوفر Aspose.Note مجموعة قوية من الأدوات للعمل مع ملفات Microsoft OneNote. إحدى المهام الشائعة التي يواجهها مطورو البرامج غالبًا هي استخراج المعلومات من الصور المضمنة في هذه الملاحظات. سواء كان الأمر يتعلق بالحصول على الأبعاد أو أسماء الملفات أو أوقات التعديل، فإن Aspose.Note يبسط هذه العملية.

## المتطلبات الأساسية

قبل أن نتعمق في استخراج معلومات الصورة باستخدام Aspose.Note، تأكد من أن لديك ما يلي:

1. المعرفة الأساسية بـ C#: الإلمام بلغة برمجة C# أمر ضروري لفهم أمثلة التعليمات البرمجية.
2.  تثبيت Aspose.Note لـ .NET: تأكد من تثبيت مكتبة Aspose.Note في بيئة التطوير لديك. يمكنك تنزيله[هنا](https://releases.aspose.com/note/net/).

## استيراد مساحات الأسماء

قبل أن نبدأ، دعونا نستورد مساحات الأسماء الضرورية:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## الخطوة 1: قم بتحميل المستند

أولاً، قم بتحميل مستند OneNote المستهدف في Aspose.Note:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";

// قم بتحميل المستند إلى Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

 يستبدل`"Your Document Directory"` مع المسار إلى ملف OneNote الخاص بك.

## الخطوة 2: استرداد معلومات الصورة

بعد ذلك، قم باسترداد جميع عقد الصورة من المستند:

```csharp
// الحصول على كافة العقد الصورة
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

يقوم مقتطف التعليمات البرمجية هذا بجلب جميع عقد الصور الموجودة في مستند OneNote الذي تم تحميله.

## الخطوة 3: التكرار من خلال الصور

الآن، دعونا نمر عبر كل عقدة صورة لاستخراج البيانات الوصفية الخاصة بها:

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

تطبع هذه الحلقة سمات مختلفة لكل صورة، مثل العرض والارتفاع والأبعاد الأصلية واسم الملف ووقت آخر تعديل.

## خاتمة

باستخدام Aspose.Note for .NET، يصبح استخراج معلومات الصورة من مستندات OneNote عملية سلسة. باتباع الخطوات الموضحة في هذا البرنامج التعليمي، يمكن للمطورين استرداد البيانات التعريفية بكفاءة من الصور المضمنة، وتمكينهم من إنشاء تطبيقات قوية.

## الأسئلة الشائعة

### س1: هل Aspose.Note متوافق مع كافة إصدارات Microsoft OneNote؟

ج1: يدعم Aspose.Note تنسيقات مختلفة لملفات OneNote، بما في ذلك .one، و.onepkg، و.onetoc2، مما يضمن التوافق عبر الإصدارات المختلفة.

### س2: هل يمكنني تعديل خصائص الصورة باستخدام Aspose.Note؟

ج2: نعم، يسمح لك Aspose.Note بمعالجة خصائص الصورة مثل الأبعاد وأسماء الملفات وأوقات التعديل برمجيًا.

### س3: هل يقدم Aspose.Note الدعم لـ .NET Core؟

ج3: نعم، يوفر Aspose.Note الدعم لـ .NET Core، مما يتيح التطوير عبر الأنظمة الأساسية لتطبيقاتك.

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Note؟

ج4: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية من Aspose.Note لاستكشاف ميزاته قبل إجراء عملية شراء.

### س5: أين يمكنني العثور على دعم أو مساعدة إضافية فيما يتعلق بـ Aspose.Note؟

ج5: لأية استفسارات أو مساعدة يمكنك زيارة منتدى Aspose.Note[هنا](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
