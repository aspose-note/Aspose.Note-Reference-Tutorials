---
date: 2026-04-09
description: تعلم كيفية استخراج بيانات تعريف الصورة والحصول على أبعاد الصورة من ملفات
  OneNote باستخدام Aspose.Note لـ .NET. دليل خطوة بخطوة لمطوري C#.
keywords:
- extract image metadata
- how to extract images
- get image dimensions
- load onenote document
- c# get image properties
linktitle: كيفية استخراج بيانات تعريف الصورة من OneNote باستخدام Aspose.Note
second_title: Aspose.Note .NET API
title: كيفية استخراج بيانات تعريف الصورة من OneNote باستخدام Aspose.Note
url: /ar/net/images/get-info-of-images/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استخراج بيانات تعريف الصورة باستخدام Aspose.Note لـ .NET

في هذا الدرس العملي ستتعلم **كيفية استخراج بيانات تعريف الصورة** — بما في ذلك العرض، الارتفاع، الحجم الأصلي، اسم الملف، ووقت التعديل — من ملفات Microsoft OneNote باستخدام مكتبة Aspose.Note للغة C#. سواء كنت بحاجة إلى عرض صور مصغرة، أو التحقق من أحجام الصور، أو بناء فهرس للأصول المدمجة، فإن استخراج هذه المعلومات برمجياً يوفر عليك خطوات يدوية لا حصر لها.

## إجابات سريعة
- **ماذا يعني “استخراج بيانات تعريف الصورة”?** استرجاع خصائص مثل الأبعاد، اسم الملف، والطوابع الزمنية من الصور المخزنة داخل مستند OneNote.  
- **ما المكتبة التي تتعامل مع ذلك؟** Aspose.Note لـ .NET.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للتطوير؛ الترخيص التجاري مطلوب للإنتاج.  
- **المنصات المدعومة؟** .NET Framework 4.6+، .NET Core 3.1+، .NET 5/6+.  
- **وقت التشغيل النموذجي؟** أقل من ثانية لملف .one قياسي.

## ما هو استخراج بيانات تعريف الصورة؟
استخراج بيانات تعريف الصورة يعني قراءة الخصائص الوصفية (العرض، الارتفاع، الأبعاد الأصلية، اسم الملف، وقت آخر تعديل، إلخ) برمجياً التي تصاحب كل كائن صورة داخل صفحة OneNote. هذه البيانات مفيدة للتحقق، وإعداد التقارير، أو معالجة الصور الإضافية.

## لماذا استخراج بيانات تعريف الصورة من OneNote؟
- **الأتمتة** – بناء أدوات تولد قوائم جرد الصور تلقائيًا.  
- **التحقق** – التأكد من أن الصور تلبي متطلبات الحجم قبل النشر.  
- **التكامل** – دمج محتوى OneNote مع أنظمة أخرى تحتاج إلى تفاصيل الصور (CMS، DAM، إلخ).  
- **الأداء** – تجنب تحميل ملفات الصور الكاملة عندما تكون الأبعاد فقط مطلوبة.

## المتطلبات المسبقة
1. **أساسيات C#** – يجب أن تكون مرتاحًا لكتابة كود C# الأساسي.  
2. **Aspose.Note لـ .NET** – قم بتحميل وتثبيت المكتبة من الموقع الرسمي [هنا](https://releases.aspose.com/note/net/).  
3. **ملف OneNote (.one)** – أي مستند OneNote موجود يحتوي على صور.

## استيراد مساحات الأسماء
قبل أن نبدأ، استورد مساحات الأسماء المطلوبة:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## الخطوة 1: تحميل مستند OneNote
أولاً، قم بتحميل ملف OneNote المستهدف إلى كائن `Aspose.Note.Document`. هذه هي خطوة **load onenote document** التي تُعد الـ API للاستعلامات اللاحقة.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

استبدل `"Your Document Directory"` بالمجلد الفعلي الذي يحتوي على ملف `.one` الخاص بك.

## الخطوة 2: استرجاع جميع عقد الصور
الآن سنقوم **how to extract images** بسحب كل عقدة `Image` من المستند.

```csharp
// Get all Image nodes
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

طريقة `GetChildNodes<T>()` تفحص كامل هيكل الدفتر وتعيد مجموعة من كائنات الصورة.

## الخطوة 3: التكرار عبر كل صورة و **c# get image properties**
سنقوم بالتكرار عبر المجموعة وطباعة بيانات التعريف، بما في ذلك قيم **get image dimensions** و **extract original image size**.

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

يعرض الإخراج العرض/الارتفاع الحالي لكل صورة (كما هو معروض في الصفحة)، الأبعاد الأصلية المخزنة في الملف، اسم الملف، والطابع الزمني لآخر تعديل.

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|-------|--------|-----|
| **NullReferenceException** عندما تكون `images` فارغة | المستند لا يحتوي على صور | تحقق من أن ملف `.one` المصدر يحتوي فعليًا على صور مدمجة. |
| **أبعاد غير صحيحة** | الصور مُقاسة في OneNote | استخدم `OriginalWidth`/`OriginalHeight` للحصول على الحجم الحقيقي. |
| **FileName فارغ** | تم لصق الصورة من الحافظة | قد لا يحتوي الـ API على اسم ملف؛ عالج القيم `null` أو السلاسل الفارغة في الكود. |

## الأسئلة المتكررة

**س: هل Aspose.Note متوافق مع جميع إصدارات Microsoft OneNote؟**  
**ج:** Aspose.Note يدعم صيغ .one، .onepkg، و .onetoc2، ويغطي معظم إصدارات OneNote منذ عام 2007 فصاعدًا.

**س: هل يمكنني تعديل خصائص الصورة بعد استخراجها؟**  
**ج:** نعم، يمكنك تغيير خصائص مثل `Width`، `Height`، أو `FileName` ثم حفظ المستند.

**س: هل يعمل Aspose.Note مع .NET Core؟**  
**ج:** بالتأكيد. المكتبة متوافقة بالكامل مع .NET Core، .NET 5، و .NET 6.

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
**ج:** نعم، يمكنك تنزيل نسخة تجريبية من موقع Aspose لاستكشاف جميع الميزات.

**س: أين يمكنني الحصول على مساعدة إضافية أو دعم المجتمع؟**  
**ج:** زر منتدى Aspose.Note [هنا](https://forum.aspose.com/c/note/28) للحصول على نصائح، أمثلة كود، وإجابات من المجتمع.

---

**آخر تحديث:** 2026-04-09  
**تم الاختبار مع:** Aspose.Note 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}