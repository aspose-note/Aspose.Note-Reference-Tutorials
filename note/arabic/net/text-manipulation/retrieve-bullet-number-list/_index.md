---
title: استرداد قائمة التعداد النقطي أو الرقمي في نص Aspose.Note
linktitle: استرداد قائمة التعداد النقطي أو الرقمي في نص Aspose.Note
second_title: Aspose.Note .NET API
description: أطلق العنان لإمكانات Aspose.Note لـ .NET من خلال دليلنا خطوة بخطوة حول استرداد قوائم التعداد النقطي أو الرقمي. ارفع مهاراتك في التعامل مع مستندات OneNote!
weight: 23
url: /ar/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استرداد قائمة التعداد النقطي أو الرقمي في نص Aspose.Note

## مقدمة
مرحبًا بك في عالم Aspose.Note for .NET، وهي مكتبة قوية ومتعددة الاستخدامات تمكن المطورين من التعامل مع مستندات OneNote دون عناء. في هذا البرنامج التعليمي، سوف نتعمق في عملية استرداد قوائم التعداد النقطي أو الرقمي باستخدام Aspose.Note لـ .NET. سواء كنت مطورًا متمرسًا أو متحمسًا للبرمجة، سيزودك هذا الدليل بالمعرفة اللازمة للتنقل عبر تعقيدات العمل باستخدام القوائم في Aspose.Note.
## المتطلبات الأساسية
قبل أن نبدأ رحلة البرمجة هذه، تأكد من توفر المتطلبات الأساسية التالية:
-  Aspose.Note لـ .NET: تأكد من تثبيت مكتبة Aspose.Note. إذا لم يكن الأمر كذلك، يمكنك تنزيله من[Aspose.Note لوثائق .NET](https://reference.aspose.com/note/net/).
- بيئة التطوير: لديك بيئة تطوير عمل، ويفضل أن تكون Microsoft Visual Studio، تم إعدادها على جهازك.
- المعرفة الأساسية بـ C#: تعرف على C# لأن هذا البرنامج التعليمي مكتوب بهذه اللغة.
## استيراد مساحات الأسماء
لكي تتمكن من التفاعل مع Aspose.Note for .NET، تحتاج إلى استيراد مساحات الأسماء الضرورية إلى مشروعك. قم بتضمين مساحات الأسماء التالية في بداية التعليمات البرمجية الخاصة بك:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
الآن، دعونا نقسم عملية استرجاع القوائم النقطية أو الرقمية خطوة بخطوة:
## الخطوة 1: قم بتعيين دليل المستندات الخاص بك
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
```
 يستبدل`"Your Document Directory"` بالمسار الفعلي حيث يوجد مستند Aspose.Note الخاص بك.
## الخطوة 2: قم بتحميل المستند
```csharp
// قم بتحميل المستند إلى Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 تأكد من استبدال`"ApplyNumberingOnText.one"` باسم مستند OneNote المحدد.
## الخطوة 3: استرداد مجموعة العقد
```csharp
// استرداد مجموعة من العقد لعنصر المخطط التفصيلي.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
تقوم هذه الخطوة باسترداد مجموعة من عقد المخطط التفصيلي من المستند الذي تم تحميله.
## الخطوة 4: التكرار من خلال كل عقدة
```csharp
// التكرار من خلال كل عقدة.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // تابع إلى الخطوات التالية...
    }
}
```
تضمن هذه الحلقة أننا نتعامل فقط مع العقد التي تحتوي على قائمة أرقام.
## الخطوة 5: استرداد معلومات الخط
```csharp
// استرجاع اسم الخط
Console.WriteLine("Font Name: " + list.Font);
// استرداد طول الخط
Console.WriteLine("Font Length: " + list.Font.Length);
// استرداد حجم الخط
Console.WriteLine("Font Size: " + list.FontSize);
// استرداد لون الخط
Console.WriteLine("Font Color: " + list.FontColor);
// استرداد التنسيق
Console.WriteLine("Font format: " + list.Format);
// تحقق بالخط العريض
Console.WriteLine("Is bold: " + list.IsBold);
// تحقق مائل
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
تستخرج سطور التعليمات البرمجية هذه معلومات متنوعة متعلقة بالخط من قائمة الأرقام.
## خاتمة
 تهانينا! لقد تعلمت بنجاح كيفية استرداد قوائم التعداد النقطي أو الرقمي باستخدام Aspose.Note لـ .NET. أثناء مواصلة الاستكشاف، راجع[توثيق](https://reference.aspose.com/note/net/) لمزيد من الرؤى والوظائف المتعمقة.
## الأسئلة الشائعة
### هل يمكنني استخدام Aspose.Note لـ .NET مع لغات البرمجة الأخرى؟
يدعم Aspose.Note بشكل أساسي .NET، ولكن هناك إصدارات أخرى من المكتبة مصممة خصيصًا لمنصات ولغات مختلفة.
### هل Aspose.Note متوافق مع أحدث تنسيقات OneNote؟
نعم، يدعم Aspose.Note مجموعة واسعة من تنسيقات OneNote، مما يضمن التوافق مع أحدث الإصدارات.
### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note؟
 يزور[هذا الرابط](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت لأغراض التقييم.
### ما هي خيارات الدعم المتاحة لمستخدمي Aspose.Note؟
يمكنك الاستكشاف وطلب المساعدة في[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) لأية استفسارات أو مشاكل قد تواجهها.
### هل هناك نسخة تجريبية مجانية من Aspose.Note لـ .NET؟
 نعم، يمكنك الوصول إلى الإصدار التجريبي المجاني من Aspose.Note لـ .NET[هنا](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
