---
title: أدخل قائمة الأرقام الصينية في نص Aspose.Note
linktitle: أدخل قائمة الأرقام الصينية في نص Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إدراج قوائم الأرقام الصينية في Aspose.Note لمستندات .NET دون عناء. ارفع مهاراتك في تنسيق المستندات باستخدام هذا الدليل المفصّل خطوة بخطوة.
weight: 20
url: /ar/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# أدخل قائمة الأرقام الصينية في نص Aspose.Note

## مقدمة
هل تتطلع إلى تحسين مهاراتك في Aspose.Note لـ .NET من خلال دمج قوائم الأرقام الصينية في مستنداتك؟ إذا كان الأمر كذلك، فأنت في المكان الصحيح! في هذا البرنامج التعليمي، سنرشدك خلال عملية إدراج قوائم الأرقام الصينية باستخدام Aspose.Note لـ .NET. تتيح لك هذه المكتبة القوية التعامل مع مستندات OneNote بسلاسة.
## المتطلبات الأساسية
قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
- المعرفة الأساسية ببرمجة C#.
-  تم تثبيت Aspose.Note لـ .NET. يمكنك تنزيله[هنا](https://releases.aspose.com/note/net/).
## استيراد مساحات الأسماء
للبدء، قم باستيراد مساحات الأسماء الضرورية إلى مشروعك:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## الخطوة 1: تهيئة مستند OneNote
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## الخطوة 2: تهيئة صفحة OneNote
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## الخطوة 3: تطبيق إعدادات نمط النص
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## الخطوة 4: إنشاء عناصر المخطط التفصيلي
الآن، لنقم بإنشاء ثلاثة عناصر مخطط تفصيلي باستخدام قوائم الأرقام الصينية:
### الخطوة 4.1: العنصر الأول
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### الخطوة 4.2: العنصر الثاني
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### الخطوة 4.3: العنصر الثالث
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## الخطوة 5: إلحاق العناصر بالمخطط التفصيلي
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## الخطوة 6: إلحاق المخطط التفصيلي بالصفحة
```csharp
page.AppendChildLast(outline);
```
## الخطوة 7: إلحاق الصفحة بالمستند
```csharp
doc.AppendChildLast(page);
```
## الخطوة 8: حفظ مستند OneNote
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
تهانينا! لقد قمت بإدراج قوائم الأرقام الصينية بنجاح في مستند Aspose.Note الخاص بك باستخدام مكتبة .NET.
## خاتمة
في هذا البرنامج التعليمي، قمنا بتغطية العملية خطوة بخطوة لدمج قوائم الأرقام الصينية في مستندات Aspose.Note الخاصة بـ .NET. عزز مهارات تنسيق المستندات لديك واجعل المحتوى الخاص بك أكثر تفاعلاً مع هذه التقنيات.
## الأسئلة الشائعة
### س: هل يمكنني تخصيص تنسيق قوائم الأرقام الصينية؟
 ج: نعم، يمكنك تخصيص التنسيق عن طريق ضبط المعلمات في ملف`NumberList` البناء.
### س: هل Aspose.Note متوافق مع أحدث إصدار من .NET؟
ج: نعم، يتم تحديث Aspose.Note بانتظام لدعم أحدث إصدارات .NET.
### س: أين يمكنني العثور على أمثلة ووثائق إضافية؟
ج: استكشاف الشامل[Aspose.Note الوثائق](https://reference.aspose.com/note/net/).
### س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note؟
 ج: الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).
### س: أين يمكنني طلب المساعدة أو مناقشة الاستفسارات المتعلقة بـ Aspose.Note؟
 ج: قم بزيارة[منتدى الدعم Aspose.Note](https://forum.aspose.com/c/note/28) لدعم المجتمع.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
