---
title: تطبيق التعداد النقطي على النص في Aspose.Note
linktitle: تطبيق التعداد النقطي على النص في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية تطبيق التعداد النقطي على النص في Aspose.Note لـ .NET لتحسين مستندات OneNote الخاصة بك. اتبع هذا الدليل خطوة بخطوة للتنسيق الفعال.
type: docs
weight: 10
url: /ar/net/text-manipulation/apply-bullets-on-text/
---
## مقدمة
مرحبًا بك في هذا الدليل المفصّل خطوة بخطوة حول تطبيق التعداد النقطي على النص باستخدام Aspose.Note لـ .NET. Aspose.Note هي مكتبة قوية تتيح للمطورين العمل بسلاسة مع ملفات Microsoft OneNote في تطبيقات .NET الخاصة بهم. في هذا البرنامج التعليمي، سنرشدك خلال عملية تطبيق التعداد النقطي على النص، مما يعزز المظهر المرئي لمستندات OneNote الخاصة بك.
## المتطلبات الأساسية
قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:
- المعرفة الأساسية ببرمجة C# و.NET.
-  تم تثبيت Aspose.Note لمكتبة .NET. يمكنك تنزيله[هنا](https://releases.aspose.com/note/net/).
## استيراد مساحات الأسماء
في كود C# الخاص بك، تأكد من تضمين مساحات الأسماء الضرورية:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## الخطوة 1: قم بإعداد المستند الخاص بك
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
// قم بإنشاء كائن من فئة المستند
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## الخطوة 2: تهيئة الصفحة والمخطط التفصيلي
```csharp
// تهيئة كائن فئة الصفحة
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// تهيئة كائن فئة المخطط التفصيلي
Outline outline = new Outline(doc);
```
## الخطوة 3: تعيين نمط النص الافتراضي
```csharp
// تهيئة كائن فئة TextStyle وتعيين خصائص التنسيق
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## الخطوة 4: إنشاء عناصر المخطط التفصيلي باستخدام الرموز النقطية
```csharp
// تهيئة كائنات فئة OutlineElement وتطبيق الرموز النقطية
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// كرر لعناصر المخطط التفصيلي الأخرى
```
## الخطوة 5: إضافة عناصر المخطط التفصيلي إلى المخطط التفصيلي
```csharp
// إضافة عناصر المخطط التفصيلي
outline.AppendChildLast(outlineElem1);
// كرر لعناصر المخطط التفصيلي الأخرى
```
## الخطوة 6: إضافة مخطط تفصيلي إلى الصفحة
```csharp
// إضافة عقدة المخطط التفصيلي
page.AppendChildLast(outline);
```
## الخطوة 7: إضافة صفحة إلى المستند
```csharp
// إضافة عقدة الصفحة
doc.AppendChildLast(page);
```
## الخطوة 8: احفظ مستند OneNote
```csharp
// حفظ مستند OneNote
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## خاتمة
تهانينا! لقد تعلمت بنجاح كيفية تطبيق التعداد النقطي على النص باستخدام Aspose.Note لـ .NET. يمكن لهذه الميزة تحسين تنسيق مستندات OneNote بشكل كبير، مما يجعلها أكثر جاذبية من الناحية المرئية.
## الأسئلة الشائعة
### هل يمكنني تطبيق أنماط نقطية مختلفة على كل عنصر في القائمة؟
 نعم، يمكنك تخصيص أنماط التعداد النقطي عن طريق تعديل`NumberList` خصائص لكل`OutlineElement`.
### هل Aspose.Note متوافق مع الإصدار الأحدث من Microsoft OneNote؟
يدعم Aspose.Note إصدارات مختلفة من Microsoft OneNote، مما يضمن التوافق مع الإصدارات الأقدم والأحدث.
### هل يمكنني استخدام Aspose.Note لأغراض تجارية؟
 نعم، يمكنك استخدام Aspose.Note for .NET في المشاريع التجارية. للحصول على ترخيص، قم بزيارة[هنا](https://purchase.aspose.com/buy).
### هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ .NET؟
 نعم، يمكنك تنزيل نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).
### أين يمكنني العثور على دعم وموارد إضافية؟
 يمكنك زيارة منتدى مجتمع Aspose.Note[هنا](https://forum.aspose.com/c/note/28) للدعم والمناقشات.