---
title: قم بتعيين نمط الفقرة الافتراضي في Aspose.Note
linktitle: قم بتعيين نمط الفقرة الافتراضي في Aspose.Note
second_title: Aspose.Note .NET API
description: اكتشف قوة Aspose.Note لـ .NET من خلال دليلنا خطوة بخطوة حول تعيين أنماط الفقرة الافتراضية. ارفع مهاراتك في التعامل مع المستندات دون عناء.
weight: 24
url: /ar/net/text-manipulation/set-default-paragraph-style/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قم بتعيين نمط الفقرة الافتراضي في Aspose.Note

## مقدمة
في مجال تطوير .NET، يبرز Aspose.Note كأداة قوية للعمل مع ملفات OneNote. إحدى الميزات الأساسية التي تقدمها هي القدرة على تعيين أنماط الفقرة الافتراضية، مما يوفر للمطورين المرونة للتحكم في مظهر النص في مستنداتهم. في هذا البرنامج التعليمي، سوف نتعمق في عملية تعيين أنماط الفقرة الافتراضية باستخدام Aspose.Note لـ .NET. تابع معنا بينما نقوم بتفصيل كل خطوة لمساعدتك على إتقان هذا الجانب الحاسم من معالجة المستندات.
## المتطلبات الأساسية
قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
- Aspose.Note لـ .NET: تأكد من تثبيت مكتبة Aspose.Note لـ .NET. يمكنك تنزيله من[Aspose.Note وثائق .NET](https://reference.aspose.com/note/net/).
- بيئة التطوير المتكاملة (IDE): احصل على بيئة تطوير متكاملة فعالة لتطوير .NET، مثل Visual Studio، مثبتة على جهازك.
والآن بعد أن أصبحت لديك الأدوات اللازمة، دعنا ننتقل إلى الخطوات التالية.
## استيراد مساحات الأسماء
قبل كتابة التعليمات البرمجية، من الضروري استيراد مساحات الأسماء الضرورية للاستفادة من الوظائف التي يوفرها Aspose.Note لـ .NET. اتبع الخطوات التالية:
## الخطوة 1: افتح مشروعك في IDE
افتح مشروعك الحالي أو قم بإنشاء مشروع جديد في IDE المفضل لديك.
## الخطوة 2: إضافة مساحة الاسم Aspose.Note
قم بتضمين مساحة الاسم Aspose.Note في ملف التعليمات البرمجية الخاص بك عن طريق إضافة السطر التالي في الأعلى:
```csharp
    using System;
    using System.IO;
```
الآن بعد أن قمنا بإعداد الأساس، دعونا ننتقل إلى جوهر البرنامج التعليمي لدينا.
## دليل خطوة بخطوة لتعيين نمط الفقرة الافتراضي
## الخطوة 1: تهيئة المستند والصفحة
```csharp
var document = new Document();
var page = new Page();
```
## الخطوة 2: إنشاء مخطط تفصيلي
```csharp
var outline = new Outline();
```
## الخطوة 3: إضافة عنصر المخطط التفصيلي
```csharp
var outlineElem = new OutlineElement();
```
## الخطوة 4: إنشاء نص منسق بنمط الفقرة
```csharp
var text = new RichText() { ParagraphStyle = new ParagraphStyle() { FontName = "Courier New", FontSize = 20 } }
    .Append($"DefaultParagraphFontAndSize{Environment.NewLine}")
    .Append($"OnlyDefaultParagraphFont{Environment.NewLine}", new TextStyle() { FontSize = 14 })
    .Append("OnlyDefaultParagraphFontSize", new TextStyle() { FontName = "Verdana" });
```
## الخطوة 5: إلحاق نص بعنصر المخطط التفصيلي
```csharp
outlineElem.AppendChildLast(text);
```
## الخطوة 6: إلحاق عنصر المخطط التفصيلي بالمخطط التفصيلي
```csharp
outline.AppendChildLast(outlineElem);
```
## الخطوة 7: إلحاق المخطط التفصيلي بالصفحة
```csharp
page.AppendChildLast(outline);
```
## الخطوة 8: إلحاق الصفحة بالمستند
```csharp
document.AppendChildLast(page);
```
## الخطوة 9: حفظ المستند
```csharp
document.Save(Path.Combine("Your Document Directory", "SetDefaultParagraphStyle.one"));
```
لقد قمت الآن بتعيين نمط الفقرة الافتراضي في مستند Aspose.Note الخاص بك بنجاح. لا تتردد في استكشاف أنماط وأحجام الخطوط المختلفة لتخصيص النص وفقًا لمتطلباتك.
## خاتمة
إن إتقان فن إعداد أنماط الفقرات الافتراضية باستخدام Aspose.Note for .NET يفتح عالمًا من الإمكانيات في معالجة المستندات. من خلال هذه الخطوات البسيطة والقوية، يمكنك تحسين المظهر المرئي لمستنداتك وتقديم تجربة مستخدم أكثر صقلًا.
## أسئلة مكررة
### هل يمكنني تغيير نمط الفقرة الافتراضي بعد حفظ المستند؟
لا، يتم تعيين نمط الفقرة الافتراضي أثناء إنشاء المستند ولا يمكن تغييره بعد الحفظ.
### هل يدعم Aspose.Note أنماط الخطوط الأخرى بخلاف الأمثلة المقدمة؟
قطعاً! يقدم Aspose.Note مجموعة واسعة من أنماط الخطوط وأحجامها لتتمكن من استكشافها وتنفيذها في مستنداتك.
### هل يمكنني تطبيق أنماط افتراضية مختلفة على أقسام مختلفة من المستند؟
نعم، يمكنك إنشاء مخططات تفصيلية أو صفحات متعددة بأنماط فقرات افتراضية متميزة داخل نفس المستند.
### هل Aspose.Note متوافق مع أحدث أطر عمل .NET؟
نعم، يتم تحديث Aspose.Note بانتظام لضمان التوافق مع أحدث أطر عمل .NET.
### هل التراخيص المؤقتة متاحة لـ Aspose.Note؟
 نعم، يمكنك الحصول على ترخيص مؤقت لـ Aspose.Note من[هنا](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
