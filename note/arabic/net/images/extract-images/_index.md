---
date: 2026-04-06
description: تعلم كيفية استخراج الصور من مستندات Aspose.Note باستخدام Aspose.Note
  لـ .NET. يوضح هذا الدليل كيفية استخراج الصور بكفاءة.
keywords:
- how to extract images
- Aspose.Note .NET
- extract images from .one
linktitle: كيفية استخراج الصور من مستندات Aspose.Note
second_title: Aspose.Note .NET API
title: كيفية استخراج الصور من مستندات Aspose.Note
url: /ar/net/images/extract-images/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استخراج الصور من مستندات Aspose.Note

## مقدمة

إذا كنت بحاجة إلى **كيفية استخراج الصور** من ملفات Aspose.Note بسرعة وموثوقية، فأنت في المكان الصحيح. تقدم Aspose.Note for .NET واجهة برمجة تطبيقات نظيفة تتيح لك سحب كل صورة من دفتر ملاحظات `.one` ببضع أسطر من كود C#. في هذا الدرس سنستعرض العملية بالكامل — من إعداد البيئة إلى حفظ كل صورة على القرص — حتى تتمكن من دمج استخراج الصور في تطبيقات .NET الخاصة بك بثقة.

## إجابات سريعة
- **ما الذي تُعيده الواجهة البرمجية؟** كائن `Image` يحتوي على البايتات الخام واسم الملف الأصلي.  
- **هل يمكن استخراج جميع الصور مرة واحدة؟** نعم، `GetChildNodes<Image>()` تُعيد كل عقدة صورة في المستند.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم ترخيص تجاري للاستخدام غير التجريبي.  
- **الإصدارات المدعومة من .NET؟** .NET Framework 4.x، .NET Core 3.1+، .NET 5/6+.  
- **أين تُحفظ الملفات المستخرجة؟** في المجلد الذي تحدده في `dataDir` (المجلد نفسه للملف المصدر افتراضيًا).

## ما هو استخراج الصور في Aspose.Note؟

استخراج الصور يعني قراءة البيانات الثنائية للصورة المخزنة داخل ملف OneNote (`.one`) وكتابتها كملفات صورة قياسية (PNG، JPEG، إلخ). هذا مفيد عندما تريد إعادة استخدام الرسومات، إنشاء صور مصغرة، أو نقل المحتوى إلى منصات أخرى.

## لماذا استخراج الصور باستخدام Aspose.Note؟

- **الأتمتة:** لا نسخ‑لصق يدوي؛ التعامل مع مئات دفاتر الملاحظات برمجيًا.  
- **الاتساق:** الحفاظ على الدقة الأصلية والصيغة.  
- **متعدد المنصات:** يعمل على بيئات .NET في Windows، Linux، و macOS.  
- **بدون اعتماد على واجهة المستخدم:** يعمل بدون واجهة رسومية، مثالي للمهام على الخادم أو خطوط أنابيب CI.

## المتطلبات المسبقة

1. **Aspose.Note for .NET Library** – قم بتحميل وتثبيت من [رابط التحميل](https://releases.aspose.com/note/net/).  
2. **.NET Framework / .NET Core** – أي إصدار مدعوم (انظر قسم الإجابات السريعة).

## استيراد المساحات الاسمية

أولاً، استورد المساحات الاسمية المطلوبة حتى يعرف المترجم مكان العثور على الفئات التي سنستخدمها.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل المستند

نبدأ بتحديد المجلد الذي يحتوي على ملف OneNote وتحميله إلى كائن `Document`.

```csharp
string dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

> **نصيحة احترافية:** استخدم `Path.Combine(dataDir, "Aspose.one")` لتحسين معالجة المسارات على أنظمة تشغيل مختلفة.

### الخطوة 2: الحصول على عقد الصور

طريقة `GetChildNodes<T>()` تفحص شجرة المستند بالكامل وتُعيد كل عقدة من النوع المطلوب — في هذه الحالة، `Image`.

```csharp
IList<Aspose.Note.Image> nodes = oneFile.GetChildNodes<Aspose.Note.Image>();
```

### الخطوة 3: استخراج الصور

قم بالتكرار عبر كل عقدة `Image`، وحول مصفوفة البايتات إلى `Bitmap`، واحفظها باسم الملف الأصلي.

```csharp
foreach (Aspose.Note.Image image in nodes)
{
    using (MemoryStream stream = new MemoryStream(image.Bytes))
    {
        using (Bitmap bitMap = new Bitmap(stream))
        {
            // Save image bytes to a file
            bitMap.Save(String.Format(dataDir + "{0}", Path.GetFileName(image.FileName)));
        }
    }
}
```

> **لماذا يعمل هذا:** `image.Bytes` يحتوي على البيانات الخام للصورة، بينما `image.FileName` يحافظ على الاسم الأصلي، مما يجعل الملفات المحفوظة قابلة للتعرف فورًا.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **لم يتم حفظ أي صور** | `dataDir` يشير إلى موقع للقراءة فقط أو مسار غير صحيح. | تحقق من مسار المجلد وتأكد من أن التطبيق لديه أذونات كتابة. |
| **اسم الملف فارغ** | بعض صور OneNote مدمجة بدون اسم ملف. | استخدم اسمًا احتياطيًا، مثل `Guid.NewGuid().ToString() + ".png"`. |
| **استثناء نفاد الذاكرة** | تحميل صور كبيرة جدًا دفعة واحدة. | معالجة الصور واحدةً تلو الأخرى كما هو موضح، أو زيادة حد الذاكرة للعملية. |

## الأسئلة المتكررة

### س1: هل Aspose.Note for .NET متوافق مع جميع إصدارات .NET Framework؟

نعم، Aspose.Note for .NET متوافق مع إصدارات مختلفة من .NET Framework، مما يضمن توافقًا واسعًا عبر بيئات متعددة.

### س2: هل يمكنني استخراج صور متعددة من مستند واحد باستخدام هذه الطريقة؟

بالطبع! يتيح لك المقتطف البرمجي المقدم استخراج جميع الصور الموجودة داخل مستند، بغض النظر عن عددها.

### س3: هل يدعم Aspose.Note for .NET صيغ مستندات أخرى غير .one؟

نعم، يدعم Aspose.Note for .NET صيغ مستندات متنوعة، مما يوفر حلولًا مرنة لمعالجة المستندات.

### س4: هل هناك نسخة تجريبية متاحة لـ Aspose.Note for .NET؟

نعم، يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.Note for .NET من خلال [الموقع](https://releases.aspose.com/)، مما يتيح لك استكشاف ميزاته قبل الشراء.

### س5: أين يمكنني طلب المساعدة أو الدعم لـ Aspose.Note for .NET؟

لأي استفسارات أو مساعدة بخصوص Aspose.Note for .NET، يمكنك زيارة [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للتفاعل مع الخبراء والمطورين الآخرين.

## الخلاصة

باتباع الخطوات أعلاه، أصبحت الآن تعرف **كيفية استخراج الصور** من مستندات Aspose.Note بفعالية. دمج هذا المقتطف في خطوط أنابيب أتمتة أكبر، معالجة دفاتر الملاحظات على دفعات، أو بناء أدوات معرض صور مخصصة — كل ذلك مع موثوقية Aspose.Note for .NET.

---

**آخر تحديث:** 2026-04-06  
**تم الاختبار مع:** Aspose.Note 24.12 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}