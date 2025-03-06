---
title: تحويل المظهر الداكن باستخدام Aspose.Note لـ .NET
linktitle: قم بتطبيق المظهر الداكن على النص في Aspose.Note
second_title: Aspose.Note .NET API
description: قم بتحويل مستندات OneNote الخاصة بك باستخدام Aspose.Note لـ .NET! قم بتطبيق سمة داكنة أنيقة دون عناء. قم بالتنزيل الآن وعزز تجربة تدوين الملاحظات الخاصة بك.
weight: 11
url: /ar/net/text-manipulation/apply-dark-theme-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل المظهر الداكن باستخدام Aspose.Note لـ .NET

## مقدمة
مرحبًا بك في دليلنا خطوة بخطوة حول تطبيق سمة داكنة على النص في Aspose.Note لـ .NET. Aspose.Note عبارة عن واجهة برمجة تطبيقات .NET قوية تتيح للمطورين العمل مع ملفات Microsoft OneNote برمجيًا. في هذا البرنامج التعليمي، سنستكشف كيفية منح مستندات OneNote الخاصة بك مظهرًا أنيقًا وعصريًا من خلال تطبيق سمة داكنة على النص.
## المتطلبات الأساسية
قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
-  Aspose.Note لـ .NET: تأكد من تثبيت Aspose.Note لـ .NET. إذا لم يكن الأمر كذلك، يمكنك تنزيله من[Aspose.Note الوثائق](https://reference.aspose.com/note/net/).
- بيئة التطوير: قم بإعداد بيئة تطوير .NET المفضلة لديك، مثل Visual Studio.
- دليل المستندات: قم بإعداد الدليل الذي يوجد به مستند OneNote الخاص بك.
## استيراد مساحات الأسماء
في مشروع .NET الخاص بك، قم باستيراد مساحات الأسماء الضرورية للعمل مع Aspose.ملاحظة:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## الخطوة 1: قم بتحميل مستند OneNote
قم بتحميل مستند OneNote الخاص بك إلى Aspose.Note باستخدام الكود التالي:
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
// قم بتحميل المستند إلى Aspose.Note.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## الخطوة 2: تعيين لون الخلفية
اضبط لون خلفية كل صفحة على اللون الأسود:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## الخطوة 3: ضبط لون النص
اضبط لون خط النص إلى اللون الأبيض لرؤية أفضل:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## الخطوة 4: احفظ المستند
احفظ مستند OneNote المعدل كملف PDF:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## خاتمة
تهانينا! لقد نجحت في تطبيق سمة داكنة على النص في مستند Aspose.Note الخاص بك. يمكن لهذا التحسين البسيط والفعال أن يمنح ملفات OneNote الخاصة بك مظهرًا أكثر تعقيدًا.
## أسئلة مكررة
### هل يمكنني تطبيق سمة داكنة على أقسام معينة من مستند OneNote الخاص بي؟
نعم، يمكنك تخصيص الكود لاستهداف صفحات أو أقسام معينة داخل وثيقتك.
### هل يدعم Aspose.Note تنسيقات التصدير الأخرى إلى جانب PDF؟
قطعاً! يدعم Aspose.Note تنسيقات التصدير المختلفة، بما في ذلك الصور وMicrosoft Word.
### هل هناك حد لحجم المستند الذي يمكن لـ Aspose.Note التعامل معه؟
يمكن لـ Aspose.Note التعامل مع المستندات ذات الأحجام المختلفة، كما تم تحسين أدائها لتحقيق الكفاءة.
### هل يمكنني العودة إلى المظهر الأصلي بعد تطبيق المظهر الداكن؟
نعم، يمكنك تعديل الكود للتبديل بين السمات بناءً على تفضيلاتك.
### أين يمكنني الحصول على الدعم للاستفسارات المتعلقة بـ Aspose.Note؟
 للحصول على أي مساعدة، قم بزيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) أو استكشاف[توثيق](https://reference.aspose.com/note/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
