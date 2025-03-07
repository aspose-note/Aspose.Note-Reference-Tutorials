---
title: تغيير نمط الجدول في Aspose.Note
linktitle: تغيير نمط الجدول في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية تخصيص أنماط الجدول في Aspose.Note باستخدام لغة C#. قم بتعديل الألوان والخطوط والمزيد لتحسين عرض المستندات.
weight: 10
url: /ar/net/table-manipulation/change-table-style/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تغيير نمط الجدول في Aspose.Note

## مقدمة

في هذا البرنامج التعليمي، سنستكشف كيفية تغيير نمط الجدول في Aspose.Note باستخدام إطار عمل .NET. Aspose.Note عبارة عن واجهة برمجة تطبيقات قوية تمكن المطورين من العمل مع ملفات Microsoft OneNote برمجيًا. من خلال تخصيص نمط الجداول داخل مستندات OneNote، يمكنك تحسين جاذبيتها المرئية وسهولة قراءتها. سنتناول عملية تعديل أنماط الجدول خطوة بخطوة، مما يضمن الوضوح والفعالية.

## المتطلبات الأساسية

قبل البدء، تأكد من توفر المتطلبات الأساسية التالية:
1. المعرفة الأساسية بلغة البرمجة C#.
2. تم تثبيت Visual Studio على نظامك.
3.  تم تثبيت Aspose.Note لـ .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/net/).
4. الوصول إلى مستند OneNote الذي يحتوي على جداول للتصميم.

## استيراد مساحات الأسماء

للبدء، تأكد من استيراد مساحات الأسماء الضرورية إلى كود C# الخاص بك. توفر مساحات الأسماء هذه إمكانية الوصول إلى الفئات والأساليب المطلوبة لمعالجة الجداول في Aspose.Note.
```csharp
using System;
using System.Collections.Generic;
using System.Drawing;
using System.IO;
using System.Linq;
```

## الخطوة 1: قم بتحميل المستند

أولاً، قم بتحميل مستند OneNote إلى Aspose.Note لبدء العمل بمحتواه.
```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
```

## الخطوة 2: الحصول على عقد الجدول

استرداد قائمة عقد الجدول من المستند الذي تم تحميله. سيسمح لنا ذلك بتكرار كل جدول وتطبيق تغييرات النمط المطلوبة.
```csharp
IList<Table> nodes = document.GetChildNodes<Table>();
```

## الخطوة 3: تخصيص نمط الجدول

قم بالتكرار خلال كل جدول في المستند وقم بتخصيص نمطه وفقًا لمتطلباتك. يوضح المثال أدناه كيفية تمييز الصف الأول وألوان الصف البديل.
```csharp
foreach (Table table in nodes)
{
    SetRowStyle(table.First(), Color.DarkGray, true, true);

    var flag = false;
    foreach (var row in table.Skip(1))
    {
        SetRowStyle(row, flag ? Color.LightGray : Color.Empty, false, false);
        flag = !flag;
    }
}
```

## الخطوة 4: احفظ المستند

بمجرد تعديل أنماط الجدول، قم بحفظ المستند المحدث للحفاظ على التغييرات.
```csharp
document.Save(Path.Combine(dataDir, "ChangeTableStyleOut.one"));
Console.WriteLine("\nTable's style is updated successfully.\nFile saved at " + dataDir);
```

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية تغيير أنماط الجدول في Aspose.Note باستخدام إطار عمل .NET. باتباع هذه الخطوات، يمكنك تخصيص مظهر الجداول داخل مستندات OneNote، مما يؤدي إلى تحسين عرضها المرئي وسهولة قراءتها.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق أنماط مختلفة على صفوف أو أعمدة معينة داخل جدول؟

A1: نعم، يمكنك تخصيص نمط الصفوف أو الأعمدة الفردية عن طريق تعديل التعليمات البرمجية وفقًا لذلك ضمن الأسلوب SetRowStyle.
  
### س2: هل من الممكن تغيير حجم الخط أو محاذاة النص داخل خلايا الجدول؟

ج2: بالتأكيد، يمكنك ضبط خصائص النص المختلفة مثل حجم الخط والمحاذاة واللون عن طريق الوصول إلى الخصائص المناسبة لفئة TextRun.

### س3: هل يدعم Aspose.Note تصدير الجداول إلى تنسيقات أخرى مثل PDF أو HTML؟

ج3: نعم، يوفر Aspose.Note وظيفة لتصدير مستندات OneNote، بما في ذلك الجداول، إلى مجموعة متنوعة من التنسيقات بما في ذلك تنسيقات PDF وHTML وتنسيقات الصور.

### س4: هل يمكنني إنشاء جداول جديدة برمجياً باستخدام Aspose.Note؟

ج4: بالتأكيد، يمكنك إنشاء جداول جديدة ديناميكيًا داخل مستندات OneNote باستخدام واجهة برمجة تطبيقات Aspose.Note، مما يسمح بسيناريوهات إنشاء المستندات تلقائيًا.

### س5: أين يمكنني العثور على المزيد من الموارد والدعم لـ Aspose.Note؟

 ج5: يمكنك استكشاف وثائق Aspose.Note[هنا](https://reference.aspose.com/note/net/) واطلب المساعدة من منتديات مجتمع Aspose.Note[هنا](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
