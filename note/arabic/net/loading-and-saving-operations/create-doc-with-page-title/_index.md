---
title: قم بإنشاء مستند بعنوان الصفحة في Aspose.Note
linktitle: قم بإنشاء مستند بعنوان الصفحة في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية إنشاء مستندات تحتوي على صفحات معنونة باستخدام Aspose.Note لـ .NET. اتبع دليلنا خطوة بخطوة للتكامل السلس.
type: docs
weight: 13
url: /ar/net/loading-and-saving-operations/create-doc-with-page-title/
---
## مقدمة

في هذا البرنامج التعليمي، سنرشدك خلال عملية إنشاء مستند بصفحة عنوان باستخدام Aspose.Note لـ .NET. Aspose.Note عبارة عن واجهة برمجة تطبيقات قوية تتيح للمطورين العمل مع ملفات Microsoft OneNote برمجيًا.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من تثبيت المتطلبات الأساسية التالية وإعدادها:

### تثبيت الاستوديو المرئي

1. تنزيل Visual Studio: إذا لم تكن قد قمت بذلك بالفعل، فقم بتنزيل Visual Studio وتثبيته من موقع Microsoft على الويب.

2. تثبيت عبء عمل تطوير .NET: أثناء عملية التثبيت، تأكد من تحديد عبء العمل "تطوير سطح المكتب .NET" للتأكد من أن لديك كافة المكونات الضرورية لتطوير .NET.

3. إنشاء مشروع جديد: افتح Visual Studio وقم بإنشاء مشروع جديد (تطبيق وحدة التحكم أو أي نوع آخر تفضله).

### Aspose.ملاحظة التثبيت

1.  الحصول على Aspose.Note: قم بتنزيل مكتبة Aspose.Note لـ .NET من موقع[موقع إلكتروني](https://releases.aspose.com/note/net/).

2. تثبيت Aspose.Note عبر NuGet: بدلاً من ذلك، يمكنك تثبيت Aspose.Note لـ .NET عبر NuGet Package Manager في Visual Studio. ما عليك سوى البحث عن "Aspose.Note" وتثبيت الإصدار الأحدث.

## استيراد مساحات الأسماء

أولاً، تحتاج إلى استيراد مساحات الأسماء اللازمة لاستخدام Aspose.Note في مشروعك.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

الآن، دعنا نقسم عملية إنشاء مستند بعنوان صفحة إلى خطوات متعددة:

## الخطوة 1: إنشاء كائن مستند

```csharp
//قم بإنشاء كائن من فئة المستند
Document doc = new Aspose.Note.Document();
```

## الخطوة 2: تهيئة كائن فئة الصفحة

```csharp
// تهيئة كائن فئة الصفحة
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## الخطوة 3: تعيين النمط الافتراضي للنص

```csharp
// النمط الافتراضي لكل النص في المستند.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## الخطوة 4: تعيين خصائص عنوان الصفحة

```csharp
// تعيين خصائص عنوان الصفحة
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## الخطوة 5: إلحاق عقدة الصفحة في المستند

```csharp
// إلحاق عقدة الصفحة في المستند
doc.AppendChildLast(page);
```

## الخطوة 6: حفظ مستند OneNote

```csharp
// حفظ مستند OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## خاتمة

تهانينا! لقد نجحت في إنشاء مستند بصفحة عنوان باستخدام Aspose.Note لـ .NET. قدم هذا البرنامج التعليمي دليلاً خطوة بخطوة لمساعدتك على دمج Aspose.Note في تطبيقات .NET الخاصة بك لإدارة ملفات OneNote برمجيًا.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص نمط نص العنوان؟

A1: نعم، يمكنك تخصيص لون الخط واسم الخط وحجم الخط لنص العنوان وفقًا لمتطلباتك.

### س2: هل Aspose.Note متوافق مع .NET Core؟

ج2: نعم، يدعم Aspose.Note .NET Core، مما يسمح لك بتطوير التطبيقات عبر الأنظمة الأساسية.

### س3: هل يمكنني إضافة صور ومرفقات إلى المستند؟

ج3: بالتأكيد! يوفر Aspose.Note واجهات برمجة التطبيقات (APIs) لإضافة الصور والمرفقات والعناصر الأخرى إلى مستندات OneNote الخاصة بك بسلاسة.

### س4: هل يدعم Aspose.Note قراءة ملفات OneNote الموجودة؟

ج4: نعم، يمكنك استخدام Aspose.Note لقراءة ملفات OneNote الموجودة وتعديلها ومعالجتها بسهولة.

### س5: أين يمكنني العثور على الدعم إذا واجهت أية مشكلات؟

 ج5: يمكنك العثور على الدعم والمساعدة على[منتدى Aspose.Note](https://forum.aspose.com/c/note/28)، حيث يمكن للخبراء وأعضاء المجتمع مساعدتك في الرد على استفساراتك.