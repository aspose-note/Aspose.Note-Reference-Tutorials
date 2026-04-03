---
date: 2026-04-03
description: تعلم كيفية إضافة ارتباط تشعبي في مستندات Aspose.Note باستخدام Aspose.Note
  لـ .NET، وتخصيص مظهر الارتباط التشعبي، وإدراج روابط تشعبية متعددة للحصول على ملفات
  OneNote أغنى.
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: كيفية إضافة ارتباط تشعبي في مستندات Aspose.Note
second_title: Aspose.Note .NET API
title: كيفية إضافة ارتباط تشعبي في مستندات Aspose.Note
url: /ar/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة ارتباط تشعبي في مستندات Aspose.Note

## مقدمة

في هذا البرنامج التعليمي ستكتشف **كيفية إضافة ارتباط تشعبي** إلى النص داخل مستندات Aspose.Note باستخدام واجهة برمجة تطبيقات .NET. تحويل النص إلى ارتباط تشعبي يجعل الملاحظات الثابتة تفاعلية وقابلة للنقر — مثالي لربط موارد الويب أو الأقسام الداخلية أو الملفات الخارجية. سنستعرض كل خطوة، ونظهر لك كيفية **تخصيص مظهر الارتباط التشعبي**، ونشرح كيفية **إدراج روابط تشعبية متعددة** عندما تحتاج إلى صفحات OneNote أكثر غنى.

## إجابات سريعة
- **ما هي الفئة الأساسية لإنشاء ملف OneNote؟** `Document` من Aspose.Note.
- **أي خاصية تجعل النص يتصرف كارتباط تشعبي؟** `IsHyperlink = true` على `TextStyle`.
- **هل يمكنني الربط بمواقع ويب خارجية؟** نعم، قم بتعيين `HyperlinkAddress` إلى عنوان URL مثل `https://www.google.com`.
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يلزم وجود ترخيص Aspose.Note صالح للبُنى غير التجريبية.
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.6+، .NET Core 3.1+، .NET 5/6+.

## ما هو “كيفية إضافة ارتباط تشعبي” في Aspose.Note؟
إضافة ارتباط تشعبي يعني إرفاق عنوان URL بقطعة من النص بحيث عند نقر المستخدم عليها داخل OneNote، يفتح المورد المرتبط في متصفح أو تطبيق آخر. تُظهر Aspose.Note علم `TextStyle.IsHyperlink` وخاصية `HyperlinkAddress` لجعل ذلك ممكنًا برمجيًا.

## لماذا نضيف روابط تشعبية إلى مستندات OneNote؟
- **تحسين التنقل:** الانتقال مباشرة إلى صفحات الويب أو الأقسام ذات الصلة.
- **تحسين الوثائق:** توفير المراجع أو الدروس أو ملفات المصدر دون مغادرة الملاحظة.
- **مظهر احترافي:** الألوان والأنماط القابلة للتخصيص تسمح للروابط التشعبية بالاندماج مع تصميم المستند.

## المتطلبات المسبقة

1. معرفة أساسية بـ C# و Visual Studio.
2. مكتبة Aspose.Note لـ .NET مثبتة – قم بتنزيلها من [هنا](https://releases.aspose.com/note/net/).
3. فهم بنية مستند Aspose.Note (الصفحات، المخططات، النص المنسق).

## استيراد مساحات الأسماء

أولاً، استورد مساحات الأسماء التي تمنحك الوصول إلى الفئات الأساسية في Aspose.Note وأنواع .NET الأساسية.

```csharp
using System;
using System.Drawing;
```

## دليل خطوة بخطوة

### الخطوة 1: إنشاء كائن Document جديد

أنشئ كائن `Document` الذي سيحتوي على جميع الصفحات والمحتوى.

```csharp
Document doc = new Document();
```

### الخطوة 2: تعريف أنماط النص (بما في ذلك نمط الارتباط التشعبي)

أنشئ كائنين `TextStyle` – أحدهما للنص العادي والآخر للارتباط التشعبي.  
هنا نقوم أيضًا **بتخصيص مظهر الارتباط التشعبي** عن طريق ضبط لون الخط.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **نصيحة احترافية:** لإدراج **روابط تشعبية متعددة**، عرّف كائنات `TextStyle` إضافية ذات قيم `HyperlinkAddress` مختلفة واستخدمها لاحقًا في مقاطع `RichText`.

### الخطوة 3: إنشاء كائنات RichText

ابنِ الفقرة التي تمزج بين النص العادي والارتباط التشعبي. تسمح طريقة `Append` بربط أجزاء منسقة معًا.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### الخطوة 4: إنشاء Outline وعنصر Outline

تعمل Outlines كحاويات للعناصر البصرية على الصفحة. اضبط الحجم والموقع حسب الحاجة.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### الخطوة 5: إضافة عناصر إلى صفحة

كل ملف OneNote يتكون من صفحات. نقوم بإنشاء `Title` و `Page`، ثم نرفق الـ outline.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### الخطوة 6: حفظ المستند

اختر مجلدًا، كوّن اسم الملف الكامل، واستدعِ `Save`. سيكون ملف الإخراج ملف OneNote `.one` صالح يحتوي على الارتباط التشعبي الخاص بك.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| الارتباط التشعبي لا يفتح | تأكد من أن `HyperlinkAddress` يتضمن البروتوكول (`http://` أو `https://`). |
| لون النص غير مطبق | قم بتعيين `FontColor` على `TextStyle` المستخدم للارتباط التشعبي. |
| الحاجة إلى عدة روابط في صفحة واحدة | أنشئ عدة كائنات `TextStyle`، كل منها يحمل `HyperlinkAddress` الخاص به، وأضفه إلى نفس أو كائنات `RichText` مختلفة. |
| فشل تحميل المستند في OneNote | تحقق من أنك تستخدم نسخة OneNote مدعومة (2010+). |

## الأسئلة المتكررة

**س: هل يمكنني إضافة روابط تشعبية متعددة داخل نفس المستند باستخدام Aspose.Note؟**  
ج: نعم، ما عليك سوى إنشاء مثيلات `TextStyle` إضافية ذات قيم `HyperlinkAddress` مختلفة وإضافتها إلى كائنات `RichText` الخاصة بك.

**س: كيف يمكنني تخصيص مظهر الروابط التشعبية؟**  
ج: استخدم خصائص مثل `FontColor` و `FontName` و `FontSize` على `TextStyle` التي تحتوي على `IsHyperlink = true`. يتيح لك ذلك مطابقة هوية المستند.

**س: هل يدعم Aspose.Note الروابط التشعبية إلى مواقع ويب خارجية؟**  
ج: بالتأكيد. قم بتعيين `HyperlinkAddress` إلى أي عنوان URL صالح (بما في ذلك `http://` أو `https://`) للربط خارج ملف OneNote.

**س: هل من الممكن إنشاء ملف OneNote واحد يحتوي على العديد من الروابط التشعبية؟**  
ج: نعم. من خلال إلحاق مقاطع `RichText` منسقة متعددة ذات عناوين ارتباط مختلفة، يمكنك **إنشاء مجموعة روابط تشعبية في ملف واحد**.

**س: هل Aspose.Note متوافق مع أحدث إصدارات OneNote؟**  
ج: تعمل المكتبة مع OneNote 2010 وما بعده، بما في ذلك نسخة Windows 10 UWP.

---

**آخر تحديث:** 2026-04-03  
**تم الاختبار مع:** Aspose.Note for .NET 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}