---
title: تطبيق الترقيم على النص في Aspose.Note
linktitle: تطبيق الترقيم على النص في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية تطبيق ترقيم النص في Aspose.Note لـ .NET باستخدام هذا البرنامج التعليمي الشامل. قم بتحسين تنسيق المستندات الخاصة بك دون عناء.
weight: 12
url: /ar/net/text-manipulation/apply-numbering-on-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تطبيق الترقيم على النص في Aspose.Note

## مقدمة
يوفر Aspose.Note for .NET أدوات قوية لمعالجة المستندات في تطبيقات C#. في هذا البرنامج التعليمي، سوف نستكشف عملية تطبيق الترقيم على النص باستخدام Aspose.Note. اتبع هذه الإرشادات خطوة بخطوة لتحسين تنسيق المستند الخاص بك دون عناء.
## المتطلبات الأساسية
قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
- الفهم الأساسي للغة البرمجة C#.
-  تم تثبيت Aspose.Note لـ .NET. يمكنك تنزيله[هنا](https://releases.aspose.com/note/net/).
- بيئة تطوير متكاملة (IDE) مثل Visual Studio.
## استيراد مساحات الأسماء
للبدء، تأكد من استيراد مساحات الأسماء الضرورية في مشروع C# الخاص بك:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## الخطوة 1: قم بإعداد المستند الخاص بك
ابدأ بإنشاء مستند جديد وتهيئة الكائنات المطلوبة:
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
//قم بإنشاء كائن من فئة المستند
Document doc = new Document();
// تهيئة كائن فئة الصفحة
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// تهيئة كائن فئة المخطط التفصيلي
Outline outline = new Outline(doc);
```
## الخطوة 2: تحديد النمط الافتراضي
قم بإعداد النمط الافتراضي للنص الخاص بك باستخدام فئة ParagraphStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## الخطوة 3: تطبيق الترقيم
تهيئة كائنات فئة OutlineElement وتطبيق الترقيم على كل عنصر:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## الخطوة 4: إضافة عناصر المخطط التفصيلي
إلحاق عناصر المخطط التفصيلي بالمخطط التفصيلي:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## الخطوة 5: احفظ المستند
احفظ مستند OneNote بالترقيم المطبق:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## خاتمة
تهانينا! لقد تعلمت بنجاح كيفية تطبيق الترقيم على النص في Aspose.Note لـ .NET. قم بتجربة خيارات التنسيق المختلفة لإنشاء مستندات جذابة بصريًا دون عناء.
## الأسئلة الشائعة
### 1. هل يمكنني تخصيص تنسيق الترقيم؟
نعم، تسمح لك فئة NumberList بتخصيص تنسيق الترقيم وفقًا لتفضيلاتك.
### 2. هل هناك خيارات تنسيق أخرى متاحة؟
يوفر Aspose.Note مجموعة واسعة من خيارات التنسيق، بما في ذلك تصميم الخط واللون والمزيد.
### 3. هل Aspose.Note متوافق مع Visual Studio؟
قطعاً! يتكامل Aspose.Note بسلاسة مع Visual Studio للحصول على تجربة تطوير سلسة.
### 4. هل يمكنني تجربة Aspose.Note قبل الشراء؟
 بالتأكيد! يمكنك استكشاف نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).
### 5. أين يمكنني الحصول على الدعم لـ Aspose.Note؟
 لأي مساعدة أو استفسار قم بزيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
