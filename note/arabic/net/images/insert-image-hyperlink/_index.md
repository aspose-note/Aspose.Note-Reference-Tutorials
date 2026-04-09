---
date: 2026-04-09
description: تعلم كيفية إضافة ارتباط تشعبي إلى الصور في Aspose.Note لـ .NET وجعل مستنداتك
  تفاعلية باستخدام رسومات قابلة للنقر.
keywords:
- how to add hyperlink
- insert image hyperlink
- add clickable image
- supported image formats
- append image to page
linktitle: إدراج صور مع ارتباط تشعبي في Aspose.Note
second_title: Aspose.Note .NET API
title: كيفية إضافة ارتباط تشعبي إلى الصور في Aspose.Note
url: /ar/net/images/insert-image-hyperlink/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة ارتباط تشعبي إلى الصور في Aspose.Note

## مقدمة

إذا كنت بحاجة إلى **how to add hyperlink** إلى صورة داخل مستند على نمط OneNote، فإن Aspose.Note for .NET يجعل الأمر بسيطًا. في هذا البرنامج التعليمي ستشاهد بالضبط كيفية إدراج صورة مع رابط قابل للنقر، تحويل الرسومات الثابتة إلى نقاط تنقل تفاعلية. في النهاية، ستكون قادرًا على إضافة صور قابلة للنقر، دعم صيغ صور متعددة، وإضافة **append image to page** إلى الكائنات بثقة.

## إجابات سريعة
- **ما الذي تفعله الميزة؟** يدرج صورة تعمل كارتباط تشعبي داخل مستند Note.  
- **ما المكتبة المطلوبة؟** Aspose.Note for .NET (يتوفر نسخة تجريبية مجانية).  
- **كم يستغرق التنفيذ؟** حوالي 5‑10 دقائق لسيناريو أساسي.  
- **هل يمكنني استخدام أنواع صور مختلفة؟** نعم – JPEG، PNG، GIF، BMP وغيرها من **supported image formats**.  
- **هل يلزم ترخيص للإنتاج؟** نعم، يلزم الحصول على ترخيص تجاري للاستخدام غير التجريبي.

## كيفية إضافة ارتباط تشعبي إلى صورة

ستجد أدناه دليلًا خطوة بخطوة يشرح العملية بالكامل، من إعداد المشروع إلى حفظ المستند النهائي.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. Aspose.Note for .NET: تأكد من تثبيت Aspose.Note for .NET. إذا لم يكن مثبتًا، يمكنك تنزيله من [here](https://releases.aspose.com/note/net/).  
2. بيئة التطوير: قم بإعداد بيئة التطوير الخاصة بك باستخدام إطار عمل .NET.  
3. الصورة: احرص على أن تكون الصورة التي تريد إدراجها جاهزة في دليل المستند الخاص بك.  
4. المعرفة الأساسية: إلمام بلغة C# وإطار عمل .NET.

## استيراد مساحات الأسماء

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## الخطوة 1: تهيئة المستند والصفحة

أولاً، نحتاج إلى إنشاء نسخة جديدة من `Document` وإضافة `Page` حيث ستُوضع الصورة.

```csharp
var document = new Document();
var page = new Page(document);
```

## الخطوة 2: إدراج صورة مع ارتباط تشعبي

الآن، دعنا **insert image hyperlink** بإنشاء كائن `Image` وتعيين خاصية `HyperlinkUrl` له.

```csharp
string imagePath = "path_to_your_image.jpg";
var image = new Image(document, imagePath) { HyperlinkUrl = "http://example.com" };
```

> **نصيحة احترافية:** يمكن أن يشير `HyperlinkUrl` إلى أي عنوان ويب، ملف محلي، أو حتى ارتباط عميق داخل مستند OneNote آخر.

## الخطوة 3: إلحاق الصورة بالصفحة

بعد تجهيز الصورة، نستخدم **append image to page** عبر طريقة `AppendChildLast`.

```csharp
page.AppendChildLast(image);
```

## الخطوة 4: إلحاق الصفحة بالمستند

أخيرًا، أضف الصفحة إلى المستند واحفظ الملف.

```csharp
document.AppendChildLast(page);
document.Save("path_to_output_file.one");
```

## لماذا استخدام الصور القابلة للنقر؟

إضافة ارتباط تشعبي إلى صورة يتيح لك:

* توجيه القراء إلى موارد ذات صلة دون إغراق الصفحة بروابط نصية.  
* إنشاء ملاحظات أكثر ثراءً وتفاعلية تشبه العروض التقديمية التفاعلية.  
* الحفاظ على نظافة التصميم البصري مع توفير كامل إمكانيات التنقل.

## المشكلات الشائعة والنصائح

| المشكلة | الحل |
|-------|----------|
| **Image not displayed** | تحقق من أن `imagePath` يشير إلى ملف صالح وأن الصيغة من ضمن **supported image formats** (JPEG، PNG، GIF، BMP). |
| **Hyperlink not working** | تأكد من أن العنوان URL يتضمن البروتوكول (`http://` أو `https://`). |
| **Multiple images needed** | كرر **Step 2** و**Step 3** لكل صورة، ثم **append** كل واحدة إلى نفس الصفحة أو إلى صفحات مختلفة حسب الحاجة. |
| **Performance concerns** | حمّل الصور الكبيرة مرة واحدة، وأعد استخدام كائن `Image`، أو اضغط الملفات المصدر قبل الإدراج. |

## الأسئلة المتكررة

**س: هل يمكنني إدراج صور متعددة مع روابط تشعبية في مستند واحد؟**  
ج: نعم، يمكنك إدراج عدد غير محدود من الصور مع روابط تشعبية حسب الحاجة في مستند واحد باستخدام Aspose.Note for .NET.

**س: هل يدعم Aspose.Note صيغ صور مختلفة؟**  
ج: نعم، يدعم Aspose.Note صيغًا متعددة من **supported image formats**، بما في ذلك JPEG، PNG، GIF، BMP، وغيرها.

**س: هل يمكنني تخصيص مظهر الروابط التشعبية؟**  
ج: نعم، يمكنك تخصيص مظهر الروابط التشعبية، بما في ذلك اللون، التسطير، وتأثيرات التحويم، باستخدام Aspose.Note for .NET.

**س: هل تتوفر نسخة تجريبية من Aspose.Note for .NET؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.Note for .NET من [here](https://releases.aspose.com/).

**س: أين يمكنني الحصول على الدعم لـ Aspose.Note for .NET؟**  
ج: يمكنك الحصول على الدعم من خلال [Aspose.Note forums](https://forum.aspose.com/c/note/28)، حيث يمكنك طرح الأسئلة، طلب الإرشاد، والتفاعل مع المستخدمين والخبراء الآخرين.

## الخلاصة

في هذا البرنامج التعليمي غطينا **how to add hyperlink** إلى صورة باستخدام Aspose.Note for .NET، وعرضنا الكود المطلوب، وناقشنا أفضل الممارسات لاستخدام **clickable images**. باتباع هذه الخطوات يمكنك إثراء مستنداتك على نمط OneNote، تحسين التنقل، وتقديم تجربة قراءة أكثر جاذبية.

---

**آخر تحديث:** 2026-04-09  
**تم الاختبار مع:** Aspose.Note 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}