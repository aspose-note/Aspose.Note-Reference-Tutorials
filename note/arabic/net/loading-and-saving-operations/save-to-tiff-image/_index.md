---
title: احفظ في صورة TIFF في Aspose.Note
linktitle: احفظ في صورة TIFF في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية حفظ مستندات OneNote كصور TIFF باستخدام طرق ضغط متنوعة باستخدام Aspose.Note لـ .NET.
type: docs
weight: 27
url: /ar/net/loading-and-saving-operations/save-to-tiff-image/
---
## مقدمة

في هذا البرنامج التعليمي، سنستكشف كيفية حفظ المستندات كصور بتنسيق TIFF باستخدام Aspose.Note لـ .NET. Aspose.Note عبارة عن واجهة برمجة تطبيقات قوية تتيح للمطورين العمل مع ملفات Microsoft OneNote برمجيًا. يمكن أن يكون حفظ مستندات OneNote كصور TIFF مفيدًا للعديد من التطبيقات مثل الأرشفة أو المشاركة أو الطباعة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1.  Aspose.Note لـ .NET: تأكد من تثبيت Aspose.Note لـ .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/net/).

2. بيئة التطوير: قم بإعداد بيئة تطوير باستخدام Visual Studio أو أي برنامج .NET IDE آخر.

3. مستند OneNote: قم بإعداد نموذج مستند OneNote الذي تريد تحويله إلى تنسيق TIFF.

## استيراد مساحات الأسماء

أولاً، تحتاج إلى استيراد مساحات الأسماء الضرورية لمشروعك:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;

```

## الخطوة 1: احفظ في TIFF باستخدام ضغط JPEG

يعد ضغط JPEG طريقة مستخدمة على نطاق واسع لتقليل حجم الصور مع الحفاظ على الجودة. إليك كيفية حفظ مستند OneNote كصورة TIFF مع ضغط JPEG:

```csharp
public static void SaveToTiffUsingJpegCompression()
{
    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document("Path_to_your_OneNote_document");

    //قم بتعيين مسار الوجهة لصورة TIFF.
    var dst = "Destination_path_for_TIFF_image";

    // احفظ المستند كصورة TIFF مع ضغط JPEG.
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        TiffCompression = TiffCompression.Jpeg,
        Quality = 93 // ضبط الجودة حسب الحاجة
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using JPEG compression.\nFile saved at " + dst);
}
```

## الخطوة 2: احفظ في TIFF باستخدام ضغط PackBits

يعد ضغط PackBits خوارزمية ضغط بسيطة وفعالة تُستخدم بشكل شائع في صور TIFF. إليك كيفية حفظ مستند OneNote كصورة TIFF باستخدام ضغط PackBits:

```csharp
public static void SaveToTiffUsingPackBitsCompression()
{
    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document("Path_to_your_OneNote_document");

    //قم بتعيين مسار الوجهة لصورة TIFF.
    var dst = "Destination_path_for_TIFF_image";

    // احفظ المستند كصورة TIFF مع ضغط PackBits.
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        TiffCompression = TiffCompression.PackBits
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using PackBits compression.\nFile saved at " + dst);
}
```

## الخطوة 3: احفظ في TIFF باستخدام ضغط CCITT Group 3

يعد ضغط CCITT Group 3، المعروف أيضًا باسم ضغط الفاكس، مناسبًا للصور بالأبيض والأسود. إليك كيفية حفظ مستند OneNote كصورة TIFF باستخدام ضغط CCITT Group 3:

```csharp
public static void SaveToTiffUsingCcitt3Compression()
{
    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document("Path_to_your_OneNote_document");

    //قم بتعيين مسار الوجهة لصورة TIFF.
    var dst = "Destination_path_for_TIFF_image";

    // احفظ المستند كصورة TIFF باستخدام ضغط CCITT Group 3.
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        ColorMode = ColorMode.BlackAndWhite,
        TiffCompression = TiffCompression.Ccitt3
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using CCITT Group 3 fax compression.\nFile saved at " + dst);
}
```

باتباع هذه الخطوات، يمكنك بسهولة حفظ مستندات OneNote الخاصة بك كصور TIFF مع خيارات ضغط مختلفة باستخدام Aspose.Note for .NET.

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية حفظ مستندات OneNote كصور TIFF باستخدام طرق ضغط متنوعة مع Aspose.Note لـ .NET. سواء كنت بحاجة إلى ضغط JPEG أو PackBits أو CCITT Group 3، فإن Aspose.Note يوفر المرونة اللازمة للتعامل مع المتطلبات المختلفة بكفاءة.

## الأسئلة الشائعة

### س1: هل يمكنني ضبط جودة ضغط JPEG؟

A1: نعم، يمكنك ضبط معلمة الجودة عند الحفظ باستخدام ضغط JPEG لتحقيق التوازن بين جودة الصورة وحجم الملف.

### س2: هل Aspose.Note متوافق مع Visual Studio للتطوير؟

ج2: نعم، يمكن دمج Aspose.Note بسلاسة في Visual Studio لتطوير .NET.

### س3: هل توجد أي قيود على حجم مستندات OneNote التي يمكن تحويلها؟

ج3: يمكن لـ Aspose.Note التعامل مع مستندات OneNote الكبيرة دون مشاكل كبيرة في الأداء.

### س4: هل يمكنني أتمتة عملية التحويل لمستندات متعددة؟

ج4: نعم، يمكنك أتمتة عملية التحويل باستخدام المعالجة المجمعة باستخدام Aspose.Note APIs.

### س5: هل هناك نسخة تجريبية متاحة لـ Aspose.Note؟

ج5: نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Note من[هنا](https://releases.aspose.com/).