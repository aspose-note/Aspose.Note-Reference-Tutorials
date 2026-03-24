---
date: 2026-03-24
description: تعلم كيفية حفظ OneNote كصورة وتحويل OneNote إلى صورة باستخدام Aspose.Note
  للـ Java. دليل خطوة بخطوة لمطوري Java.
linktitle: Save OneNote as Image – Convert Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: حفظ OneNote كصورة – تحويل الدفتر إلى صورة باستخدام Aspose.Note
url: /ar/java/onenote-notebook-operations/convert-notebook-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ OneNote كصورة – تحويل دفتر الملاحظات إلى صورة باستخدام Aspise.Note

## Introduction

في هذا البرنامج التعليمي ستتعلم **كيفية حفظ OneNote كصورة** عن طريق تحويل دفتر ملاحظات OneNote إلى PNG (أو أي تنسيق صورة آخر) باستخدام مكتبة Aspose.Note for Java. تحويل صفحات دفتر الملاحظات إلى صور مفيد عندما تحتاج إلى مشاركة الملاحظات على منصات لا تدعم ملفات OneNote، أو تضمينها في ملفات PDF، أو إدراجها في عروض الشرائح.

## Quick Answers
- **ما المكتبة المطلوبة؟** Aspose.Note for Java.  
- **ما تنسيقات الصور المدعومة؟** PNG, JPEG, BMP, GIF, TIFF, إلخ.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **كم تستغرق عملية التحويل؟** عادةً بضع ثوانٍ لكل دفتر ملاحظات، حسب الحجم.  
- **هل يمكنني معالجة دفاتر الملاحظات دفعةً؟** نعم – فقط قم بالتكرار عبر الملفات وأعد استخدام نفس الكود.

## What is **save OneNote as image**?

حفظ OneNote كصورة يعني تحويل كل صفحة من دفتر ملاحظات `.one` إلى ملف صورة نقطية (مثل PNG). هذا يخلق تمثيلاً محمولاً للعرض فقط يمكن عرضه في أي مكان دون الحاجة إلى OneNote.

## Why convert OneNote to image?

- **مشاركة عبر الأنظمة** – يمكن للمستلمين عرض المحتوى على أي جهاز.  
- **التضمين في المستندات** – إدراج الصورة في Word أو PowerPoint أو ملفات PDF.  
- **الأرشفة** – حفظ لقطة بصرية لا تتغير إذا تم تعديل دفتر الملاحظات الأصلي.  
- **جاهزة للعرض** – استخدم صور PNG عالية الدقة مباشرةً في الشرائح.

## Prerequisites

قبل البدء، تأكد من أنك تمتلك:

1. **Java Development Kit (JDK)** – قم بتنزيل أحدث JDK من [الموقع الإلكتروني](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).  
2. **Aspose.Note for Java library** – احصل على ملف JAR من [موقع Aspose](https://releases.aspose.com/note/java/) وأضفه إلى مسار الفئة (classpath) في مشروعك.

## Import Packages

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

الآن دعنا نستعرض عملية التحويل خطوة بخطوة.

## Step 1: Load the Notebook Document

```java
// Specify the directory where your notebook file is located
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

نقوم بتوجيه الـ API إلى المجلد الذي يحتوي على `Sample1.one` ونحمله في كائن `Document`. من هنا يمكنك الوصول إلى الصفحات والأقسام وعناصر دفتر الملاحظات الأخرى.

## Step 2: Initialize ImageSaveOptions

```java
// Initialize PdfSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` يحدد لـ Aspose.Note كيفية تصيير المخرجات. في هذا المثال نختار PNG، لكن يمكنك استبدال `SaveFormat.Png` بـ `SaveFormat.Jpeg` أو `SaveFormat.Bmp`، إلخ، لت **تحويل OneNote إلى صورة** بتنسيق مختلف.

## Step 3: Save the Document as Image

```java
// Save the document as PNG
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

نداء `save()` يكتب صفحات دفتر الملاحظات المصورة إلى `ConvertToImage_out.png`. إذا كان دفتر الملاحظات يحتوي على عدة صفحات، سيقوم Aspose.Note بإنشاء ملفات صورة منفصلة تلقائيًا (مثال: `ConvertToImage_out_1.png`, `ConvertToImage_out_2.png`).

## Step 4: Print Confirmation

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

رسالة بسيطة في وحدة التحكم تؤكد أن عملية **حفظ OneNote كصورة** نجحت وتخبرك بمكان ملف الإخراج.

## Common Issues & Tips

- **دفاتر ملاحظات كبيرة** – قم بزيادة مساحة الذاكرة المخصصة للـ JVM (`-Xmx`) إذا واجهت `OutOfMemoryError`.  
- **التحكم في الدقة** – استخدم `options.setResolution(300);` لزيادة DPI للحصول على صور بجودة الطباعة.  
- **تحويل دفعة** – ضع الخطوات السابقة داخل حلقة `for` تتكرر عبر قائمة ملفات `.one`.

## FAQ's

### Q1: Can I convert notebooks to other image formats besides PNG?

**س1:** هل يمكنني تحويل دفاتر الملاحظات إلى تنسيقات صورة أخرى غير PNG؟

**ج1:** نعم، يمكنك ذلك. تدعم مكتبة Aspose.Note تنسيقات صور متعددة مثل JPEG، BMP، GIF، TIFF، إلخ. يمكنك تحديد التنسيق المطلوب في كائن `ImageSaveOptions` وفقًا لذلك.

### Q2: Is Aspose.Note compatible with all versions of OneNote?

**س2:** هل Aspose.Note متوافق مع جميع إصدارات OneNote؟

**ج2:** توفر Aspose.Note دعمًا شاملاً لمختلف إصدارات OneNote، مما يضمن التوافق عبر بيئات وصيغ ملفات مختلفة.

### Q3: Can I customize the image output settings during conversion?

**س3:** هل يمكنني تخصيص إعدادات إخراج الصورة أثناء التحويل؟

**ج3:** بالتأكيد. توفر Aspose.Note خيارات واسعة لتخصيص صورة الإخراج، بما في ذلك الدقة، الجودة، عمق اللون، وأكثر. يمكنك تعديل هذه الإعدادات وفقًا لمتطلباتك.

### Q4: Does Aspose.Note support batch conversion of multiple notebooks?

**س4:** هل تدعم Aspose.Note التحويل الدفعي لعدة دفاتر ملاحظات؟

**ج4:** نعم، يمكنك تحويل عدة دفاتر ملاحظات إلى صور دفعةً واحدةً بفعالية باستخدام Aspose.Note. ما عليك سوى التكرار عبر قائمة ملفات دفتر الملاحظات وتطبيق عملية التحويل الموضحة في هذا البرنامج التعليمي.

### Q5: Where can I find additional resources and support for Aspose.Note?

**س5:** أين يمكنني العثور على موارد إضافية ودعم لـ Aspose.Note؟

**ج5:** للحصول على مزيد من الوثائق والأمثلة ودعم المجتمع، زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) وتصفح [الوثائق](https://reference.aspose.com/note/java/).

---

**آخر تحديث:** 2026-03-24  
**تم الاختبار مع:** Aspose.Note for Java 24.8  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}