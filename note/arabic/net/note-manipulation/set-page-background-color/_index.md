---
title: تعيين لون خلفية الصفحات في Aspose.Note
linktitle: تعيين لون خلفية الصفحات في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية تعيين لون خلفية الصفحات في Aspose.Note المستندات باستخدام لغة البرمجة C# مع دليل خطوة بخطوة.
weight: 19
url: /ar/net/note-manipulation/set-page-background-color/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين لون خلفية الصفحات في Aspose.Note

## مقدمة

يسمح Aspose.Note for .NET للمطورين بمعالجة مستندات OneNote برمجياً. إحدى المهام الشائعة هي تعيين لون خلفية الصفحات داخل هذه المستندات. في هذا البرنامج التعليمي، سنرشدك خلال العملية خطوة بخطوة.

## المتطلبات الأساسية

قبل المتابعة، تأكد من أن لديك ما يلي:

1. المعرفة الأساسية بلغة البرمجة C#.
2. تم تثبيت Visual Studio على نظامك.
3.  تم تثبيت Aspose.Note لمكتبة .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/net/).
4. الوصول إلى محرر النصوص لكتابة كود C#.

## استيراد مساحات الأسماء

أولاً، تأكد من استيراد مساحات الأسماء الضرورية في كود C# الخاص بك. توفر مساحات الأسماء هذه إمكانية الوصول إلى الفئات والأساليب اللازمة لمعالجة مستندات OneNote باستخدام Aspose.Note لـ .NET.

```csharp
using System.Drawing;
using System.IO;

```

الآن، دعونا نقسم رمز المثال المقدم إلى خطوات متعددة:

## الخطوة 1: قم بتحميل مستند OneNote

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(Path.Combine(dataDir, "Aspose.one"));
```

 يستبدل`"Your Document Directory"` بالمسار إلى الدليل الذي يحتوي على مستند OneNote الخاص بك.

## الخطوة 2: التكرار عبر الصفحات

```csharp
foreach (var page in document)
{
    // الخطوة 3 تذهب هنا
}
```

تتكرر هذه الحلقة خلال كل صفحة في المستند.

## الخطوة 3: تعيين لون الخلفية

داخل الحلقة، قم بتعيين لون الخلفية لكل صفحة:

```csharp
page.BackgroundColor = Color.BlueViolet;
```

 يمكنك اختيار أي لون عن طريق الاستبدال`Color.BlueViolet` مع اللون المطلوب.

## الخطوة 4: احفظ المستند

وأخيرا، احفظ الوثيقة المعدلة:

```csharp
document.Save(Path.Combine(dataDir, "SetPageBackgroundColor.one"));
```

 تأكد من الاستبدال`"SetPageBackgroundColor.one"` باسم الملف المطلوب للمستند المعدل.

## خاتمة

باتباع هذه الخطوات، يمكنك بسهولة تعيين لون خلفية الصفحات في مستندات OneNote الخاصة بك باستخدام Aspose.Note for .NET. تعمل هذه الإمكانية على تحسين خيارات التخصيص لمستنداتك، مما يسمح لك بإنشاء محتوى جذاب بصريًا.

## الأسئلة الشائعة

### س1: هل يمكنني تعيين ألوان خلفية مختلفة لصفحات مختلفة داخل نفس المستند؟

A1: نعم، يمكنك تكرار الصفحات بشكل فردي وتعيين ألوان خلفية مختلفة حسب الحاجة.

### س2: هل يدعم Aspose.Note تنسيقات المستندات الأخرى إلى جانب OneNote؟

ج2: يركز Aspose.Note بشكل أساسي على العمل مع مستندات OneNote، ولكنه يوفر أيضًا دعمًا للتصدير إلى تنسيقات أخرى مثل PDF.

### س3: هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ .NET؟

ج3: نعم، يمكنك تنزيل نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).

### س4: هل يمكنني الحصول على تراخيص مؤقتة لأغراض الاختبار؟

 ج4: نعم، التراخيص المؤقتة متاحة للاختبار والتقييم. يمكنك الحصول على واحدة من[هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني العثور على دعم إضافي أو طرح أسئلة حول Aspose.Note؟

 ج5: يمكنك زيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على الدعم والتواصل مع المستخدمين الآخرين.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
