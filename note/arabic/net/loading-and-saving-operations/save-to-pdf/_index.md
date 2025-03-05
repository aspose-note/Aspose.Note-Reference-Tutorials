---
title: احفظه في ملف PDF في Aspose.Note
linktitle: احفظه في ملف PDF في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية حفظ مستندات Microsoft OneNote بتنسيق PDF باستخدام Aspose.Note لـ .NET. برنامج تعليمي خطوة بخطوة مع أمثلة التعليمات البرمجية لتخطيطات الصفحات بحجم Letter وA4.
type: docs
weight: 26
url: /ar/net/loading-and-saving-operations/save-to-pdf/
---
## مقدمة

في هذا البرنامج التعليمي، سنستكشف كيفية حفظ المستندات بتنسيق PDF باستخدام Aspose.Note لـ .NET. Aspose.Note هي مكتبة قوية تمكن المطورين من العمل مع ملفات Microsoft OneNote برمجياً. سنقوم بتغطية المتطلبات الأساسية، واستيراد مساحات الأسماء، وتوفير أدلة خطوة بخطوة لحفظ المستندات في ملف PDF في تخطيطات الصفحات المختلفة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

- تم تثبيت Visual Studio على نظامك.
-  تم تنزيل وتثبيت Aspose.Note لمكتبة .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/net/).
- المعرفة الأساسية بلغة البرمجة C#.

## استيراد مساحات الأسماء

أولاً، لنستورد مساحات الأسماء الضرورية إلى كود C# الخاص بنا:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

الآن بعد أن قمنا بتغطية المتطلبات الأساسية واستيراد مساحات الأسماء، فلنتابع حفظ المستندات إلى PDF في تخطيطات صفحات مختلفة.

## الخطوة 1: احفظ إلى PDF باستخدام إعدادات صفحة الرسالة


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // المسار إلى دليل المستندات.
    string dataDir = "Your Document Directory";

    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // احفظ المستند.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### توضيح:

- نقوم بتحميل مستند OneNote في Aspose.Note.
- حدد مسار الوجهة لملف PDF المحفوظ.
-  احفظ المستند إلى PDF باستخدام`PdfSaveOptions` مع`PageSettings` ضبط ل`Letter`.

## الخطوة 2: احفظ إلى PDF باستخدام إعدادات صفحة A4 بدون حد للارتفاع

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // المسار إلى دليل المستندات.
    string dataDir = "Your Document Directory";

    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // احفظ المستند.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### توضيح:

- كما هو الحال في الخطوة السابقة، نقوم بتحميل مستند OneNote إلى Aspose.Note.
- حدد مسار الوجهة لملف PDF المحفوظ.
-  احفظ المستند إلى PDF باستخدام`PdfSaveOptions` مع`PageSettings` ضبط ل`A4NoHeightLimit`.

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية حفظ المستندات بتنسيق PDF باستخدام Aspose.Note لـ .NET. قمنا بتغطية تخطيطين مختلفين للصفحة: Letter وA4 بدون حد للارتفاع. باستخدام Aspose.Note، يمكن للمطورين التعامل بسهولة مع ملفات OneNote برمجيًا، مما يوفر المرونة والكفاءة في مهام إدارة المستندات.

## الأسئلة الشائعة

### س١: هل يستطيع Aspose.Note التعامل مع ملفات OneNote المعقدة؟

ج1: نعم، يدعم Aspose.Note العديد من الميزات والوظائف للتعامل مع ملفات OneNote المعقدة بشكل فعال.

### س2: هل Aspose.Note مناسب للمشاريع التجارية؟

 ج2: بالتأكيد، يمكن استخدام Aspose.Note في المشاريع التجارية بسهولة. يمكنك شراء ترخيص[هنا](https://purchase.aspose.com/buy).

### س3: هل يقدم Aspose.Note نسخة تجريبية مجانية؟

 ج3: نعم، يمكنك استكشاف Aspose.Note من خلال الإصدار التجريبي المجاني المتاح[هنا](https://releases.aspose.com/).

### س4: أين يمكنني العثور على وثائق Aspose.Note؟

 ج4: يمكنك العثور على وثائق مفصلة[هنا](https://reference.aspose.com/note/net/).

### س5: هل تحتاج إلى مزيد من المساعدة؟

 ج5: لا تتردد في طرح أية أسئلة أو طلب الدعم في منتدى Aspose.Note[هنا](https://forum.aspose.com/c/note/28).