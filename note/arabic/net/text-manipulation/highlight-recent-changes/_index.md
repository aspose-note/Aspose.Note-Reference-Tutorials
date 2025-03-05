---
title: قم بتمييز كافة التغييرات الأخيرة في نص Aspose.Note
linktitle: قم بتمييز كافة التغييرات الأخيرة في نص Aspose.Note
second_title: Aspose.Note .NET API
description: قم بتحسين مستندات الملاحظات الخاصة بك باستخدام Aspose.Note لـ .NET! تعرف على كيفية إبراز التغييرات الأخيرة في النص باستخدام هذا البرنامج التعليمي خطوة بخطوة.
type: docs
weight: 19
url: /ar/net/text-manipulation/highlight-recent-changes/
---
## مقدمة
هل تتطلع إلى إضافة ميزات ديناميكية وجذابة بصريًا إلى مستندات Note الخاصة بك باستخدام .NET؟ يعد Aspose.Note for .NET حلاً قويًا يسمح لك بمعالجة ملفات Note وتحسينها بسلاسة. في هذا البرنامج التعليمي، سوف نتعمق في جانب واحد محدد: تسليط الضوء على جميع التغييرات الأخيرة في نص Aspose.Note.
## المتطلبات الأساسية
قبل أن نبدأ هذه الرحلة، تأكد من توفر المتطلبات الأساسية التالية:
-  Aspose.Note لـ .NET: تأكد من تثبيت مكتبة Aspose.Note. يمكنك تنزيله من[Aspose.Note لوثائق .NET](https://reference.aspose.com/note/net/).
- بيئة التطوير: قم بإعداد بيئة تطوير .NET، بما في ذلك IDE مثل Visual Studio.
- نموذج مستند: قم بإعداد مستند ملاحظة (في هذه الحالة، "Aspose.one") يحتوي على النص الذي تريد تمييزه.
## استيراد مساحات الأسماء
للبدء، قم باستيراد مساحات الأسماء الضرورية في مشروع .NET الخاص بك:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
    using System.Linq;
```
## الخطوة 1: قم بتحميل المستند
ابدأ بتحميل مستند الملاحظة في Aspose.Note:
```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one");
```
## الخطوة 2: تحديد التغييرات الأخيرة
بعد ذلك، حدد عقد RichText التي تم تعديلها خلال الأسبوع الماضي:
```csharp
var richTextNodes = document.GetChildNodes<RichText>().Where(e => e.LastModifiedTime >= DateTime.Today.Subtract(TimeSpan.FromDays(7)));
```
## الخطوة 3: تعيين ألوان التمييز
الآن، قم بتعيين لون التمييز للعقد المحددة وتشغيل النص:
```csharp
foreach (var node in richTextNodes)
{
    // تعيين لون التمييز للفقرة
    node.ParagraphStyle.Highlight = Color.DarkGreen;
    // قم بتعيين لون التمييز لكل تشغيل نص
    foreach (var run in node.TextRuns)
    {
        run.Style.Highlight = Color.DarkSeaGreen;
    }
}
```
## الخطوة 4: احفظ المستند المعدل
احفظ المستند مع التغييرات الأخيرة المميزة:
```csharp
document.Save(Path.Combine(dataDir, "HighlightAllRecentChanges.pdf"));
```
## الخطوة 5: عرض رسالة النجاح
وأخيرًا، قم بعرض رسالة نجاح لإعلام المستخدم:
```csharp
Console.WriteLine("\nText's recent changes are highlighted successfully.");
```
## خاتمة
في هذا البرنامج التعليمي، اكتشفنا كيفية استخدام Aspose.Note لـ .NET لتسليط الضوء على جميع التغييرات الأخيرة في النص داخل مستند Note. تعمل هذه الميزة على تحسين رؤية المستند وتعد إضافة قيمة إلى مجموعة أدواتك للتعامل مع ملفات الملاحظات.
## الأسئلة الشائعة
### هل يمكنني تطبيق ألوان تمييز مختلفة لفترات زمنية مختلفة؟
نعم، يمكنك تخصيص الرمز لتعيين ألوان تمييز مختلفة بناءً على متطلباتك المحددة.
### هل Aspose.Note متوافق مع أحدث أطر عمل .NET؟
يقوم Aspose.Note بتحديث مكتباته بانتظام لضمان التوافق مع أحدث أطر عمل .NET.
### كيف يمكنني معالجة الأخطاء أثناء تنفيذ هذه الميزة؟
يمكنك دمج كتل محاولة الالتقاط للتعامل مع الاستثناءات وتوفير تجربة مستخدم سلسة.
### هل يدعم Aspose.Note ميزات تنسيق النص الأخرى؟
قطعاً! يوفر Aspose.Note مجموعة واسعة من الميزات لتنسيق النص، بما في ذلك أنماط الخطوط وأحجامها والمزيد.
### هل يمكنني دمج هذا الحل في تطبيق ويب؟
نعم، يمكنك دمج Aspose.Note for .NET في تطبيقات الويب لتحسين قدرات معالجة المستندات.