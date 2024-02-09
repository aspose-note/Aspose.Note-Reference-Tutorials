---
title: إنشاء الجداول باستخدام Aspose.Note
linktitle: إنشاء الجداول باستخدام Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إنشاء جداول منظمة بمحتوى نصي منسق باستخدام Aspose.Note لـ .NET. تعزيز تنظيم المستندات وسهولة قراءتها دون عناء.
type: docs
weight: 11
url: /ar/net/table-manipulation/compose-tables/
---
## مقدمة

الجداول هي مكونات أساسية للوثائق، مما يتيح العرض المنظم للمعلومات. يوفر Aspose.Note for .NET أدوات قوية لإنشاء الجداول بسهولة. في هذا البرنامج التعليمي، سنرشدك خلال عملية إنشاء الجداول ذات المحتوى النصي المنسق باستخدام Aspose.Note.

## المتطلبات الأساسية

قبل الغوص في تكوين الجدول باستخدام Aspose.Note for .NET، تأكد من توفر المتطلبات الأساسية التالية:

1. إعداد البيئة: تأكد من أن لديك بيئة تطوير مناسبة تم إعدادها باستخدام .NET Framework أو .NET Core.
2.  التثبيت: قم بتنزيل وتثبيت Aspose.Note لـ .NET من[موقع إلكتروني](https://releases.aspose.com/note/net/).
3. المعرفة الأساسية: تعرف على المفاهيم الأساسية لبرمجة C# ومعالجة المستندات.

## استيراد مساحات الأسماء

قبل البدء في إنشاء الجداول، تأكد من استيراد مساحات الأسماء الضرورية:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

دعونا نقسم المثال المقدم إلى خطوات يمكن التحكم فيها:

## الخطوة 1: إعداد دليل المستندات

قبل إنشاء الجدول، حدد الدليل الذي سيتم حفظ المستند فيه.

```csharp
string dataDir = "Your Document Directory";
```

## الخطوة 2: إنشاء نص الرأس

حدد نص الرأس باستخدام أنماط محددة مثل حجم الخط والخط الغامق.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## الخطوة 3: إنشاء الصفحة والمخطط التفصيلي

قم بتهيئة صفحة ومخطط تفصيلي لتنظيم المحتوى.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## الخطوة 4: إضافة نص ملخص

قم بتضمين نص ملخص قبل الجدول.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## الخطوة 5: إنشاء الجدول

تهيئة جدول لتنظيم البيانات في صفوف وأعمدة.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## الخطوة 6: إضافة صف الرأس

قم بملء الجدول بصف رأس يحتوي على عناوين الأعمدة.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## الخطوة 7: إضافة صفوف فارغة

قم بإدراج صفوف فارغة للتحضير لإدراج البيانات.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## الخطوة 8: إضافة معلومات الاتصال

قم بملء عمود "جهات الاتصال" بمحتوى القالب.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## الخطوة 9: احفظ المستند

احفظ مستند الجدول المكون.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## الخطوة 10: التأكيد

تأكيد تكوين المستند بنجاح.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا كيفية إنشاء جداول تحتوي على محتوى نصي منسق باستخدام Aspose.Note لـ .NET. باتباع هذه الإرشادات خطوة بخطوة، يمكنك إنشاء جداول منظمة بكفاءة داخل مستنداتك، مما يعزز سهولة القراءة والتنظيم.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص نمط عناصر الجدول؟
   
ج1: نعم، يمكنك تخصيص جوانب مختلفة مثل حجم الخط واللون والمحاذاة لتناسب متطلباتك.

### س2: هل Aspose.Note متوافق مع مكتبات .NET الأخرى؟
   
ج2: يتكامل Aspose.Note بسلاسة مع مكتبات .NET الأخرى، مما يوفر مرونة واسعة النطاق في معالجة المستندات.

### س3: هل يدعم Aspose.Note تصدير الجداول إلى تنسيقات مختلفة؟
   
ج3: بالتأكيد، يتيح لك Aspose.Note تصدير الجداول إلى تنسيقات مختلفة بما في ذلك PDF وDOCX وHTML.

### س4: هل يمكنني تعبئة الجداول ببيانات من مصادر خارجية بشكل حيوي؟
   
ج4: نعم، يمكنك تعبئة الجداول ديناميكيًا عن طريق جلب البيانات من قواعد البيانات أو واجهات برمجة التطبيقات أو مدخلات المستخدم.

### س5: هل يتوفر الدعم الفني لمستخدمي Aspose.Note؟
   
ج5: نعم، توفر Aspose دعمًا فنيًا شاملاً من خلال منتدياتها وقنوات الدعم المخصصة لها.