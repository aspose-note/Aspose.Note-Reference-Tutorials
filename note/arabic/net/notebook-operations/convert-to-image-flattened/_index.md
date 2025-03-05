---
title: تحويل دفاتر الملاحظات إلى صورة (مسطحة) في Aspose Note .NET
linktitle: تحويل دفاتر الملاحظات إلى صورة (مسطحة) في Aspose Note .NET
second_title: Aspose.Note .NET API
description: تعرف على كيفية تحويل دفاتر ملاحظات OneNote إلى صور مسطحة باستخدام Aspose.Note لـ .NET. دليل خطوة بخطوة للتكامل السلس.
type: docs
weight: 12
url: /ar/net/notebook-operations/convert-to-image-flattened/
---
## مقدمة

في هذا البرنامج التعليمي، سنتعلم كيفية استخدام Aspose.Note لـ .NET لتحويل دفاتر الملاحظات إلى صور مسطحة. سنقوم بتقسيم العملية إلى خطوات بسيطة لمساعدتك على فهمها وتنفيذها بفعالية.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1.  Aspose.Note for .NET: إذا لم تكن قد قمت بذلك بالفعل، فقم بتنزيل Aspose.Note for .NET وتثبيته من[هنا](https://releases.aspose.com/note/net/).
2. بيئة التطوير: تأكد من أن لديك بيئة تطوير مناسبة تم إعدادها لتطوير .NET.
3. دفتر ملاحظات OneNote: قم بإعداد دفتر ملاحظات OneNote الذي تريد تحويله إلى صورة.

## استيراد مساحات الأسماء

قبل البدء بعملية التحويل، تحتاج إلى استيراد مساحات الأسماء الضرورية في التعليمات البرمجية الخاصة بك:

```csharp
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

الآن، دعنا نتعمق في الدليل خطوة بخطوة لتحويل دفاتر الملاحظات إلى صور مسطحة باستخدام Aspose.Note لـ .NET.

## الخطوة 1: قم بتحميل الكمبيوتر المحمول

أولاً، قم بتحميل دفتر ملاحظات OneNote الذي تريد تحويله إلى التطبيق الخاص بك.

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";

// قم بتحميل دفتر ملاحظات OneNote
var notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## الخطوة 2: قم بتعيين خيارات الحفظ

حدد خيارات الحفظ للكمبيوتر الدفتري، بما في ذلك تنسيق الصورة ودقتها.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
notebookSaveOptions.Flatten = true;
```

## الخطوة 3: احفظ دفتر الملاحظات كصورة

الآن، احفظ دفتر الملاحظات كصورة مسطحة باستخدام خيارات الحفظ المحددة.

```csharp
dataDir = dataDir + "ConvertToImageAsFlattenedNotebook_out.png";

// احفظ دفتر الملاحظات
notebook.Save(dataDir, notebookSaveOptions);
```

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية تحويل دفاتر الملاحظات إلى صور مسطحة باستخدام Aspose.Note لـ .NET. باتباع الدليل الموضح خطوة بخطوة، يمكنك دمج هذه الوظيفة بسلاسة في تطبيقات .NET الخاصة بك.

## الأسئلة الشائعة

### س1: هل يستطيع Aspose.Note لـ .NET التعامل مع دفاتر الملاحظات المعقدة؟

ج1: نعم، Aspose.Note for .NET قادر على التعامل مع دفاتر الملاحظات المعقدة بكفاءة.

### س2: هل تتوفر نسخة تجريبية مجانية من Aspose.Note لـ .NET؟

 ج2: نعم، يمكنك تنزيل نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).

### س3: هل تقدم Aspose الدعم لمنتجاتها؟

 ج3: نعم، يمكنك الحصول على الدعم من مجتمع Aspose[هنا](https://forum.aspose.com/c/note/28).

### س4: هل يمكنني شراء ترخيص مؤقت لـ Aspose.Note لـ .NET؟

 ج4: نعم، يمكنك شراء ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني العثور على وثائق Aspose.Note لـ .NET؟

 ج5: يمكنك العثور على الوثائق[هنا](https://reference.aspose.com/note/net/).