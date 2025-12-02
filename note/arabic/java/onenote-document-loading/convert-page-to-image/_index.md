---
date: 2025-11-29
description: تعلم كيفية تصدير صفحات OneNote إلى صور باستخدام Java، واكتشف كيفية تحويل
  صورة صفحة OneNote باستخدام Aspose.Note. اتبع دليلنا خطوة بخطوة للتكامل السريع.
language: ar
linktitle: How to Export OneNote Page to Image Using Java
second_title: Aspose.Note Java API
title: كيفية تصدير صفحة OneNote إلى صورة باستخدام Java
url: /java/onenote-document-loading/convert-page-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تصدير صفحة OneNote إلى صورة باستخدام Java

## المقدمة

في هذا الدرس، ستتعلم **كيفية تصدير OneNote** الصفحات إلى ملفات صور باستخدام Java مع Aspose.Note. تحويل صفحة OneNote إلى صورة مفيد عندما تحتاج إلى تضمين محتوى الدفتر في تقارير، مشاركة لقطات مع مستخدمين لا يستخدمون OneNote، أو إنشاء صور مصغرة لأنظمة إدارة المستندات. سنستعرض كل خطوة، نشرح لماذا كل سطر مهم، ونظهر لك كيفية تخصيص الناتج.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.Note for Java  
- **هل يمكنني اختيار تنسيق الصورة؟** نعم – JPEG، PNG، BMP، إلخ عبر `ImageSaveOptions`  
- **هل أحتاج إلى ترخيص للإنتاج؟** ترخيص Aspose.Note صالح مطلوب للاستخدام التجاري.  
- **أي صفحة يمكنني تصديرها؟** أي صفحة عن طريق تعيين `PageIndex` (بدءًا من الصفر).  
- **كم يستغرق التحويل من وقت؟** عادةً أقل من ثانية لصفحة قياسية.

## ما هو تصدير صفحات OneNote إلى صور؟
تصدير صفحات OneNote يعني تحويل المحتوى الغني للصفحة—النص، الرسومات، الجداول—إلى ملف صورة ثابت (مثل JPEG). هذه العملية تُنشئ تمثيلًا بصريًا محمولًا يمكن عرضه في أي مكان، حتى حيث لا يكون عميل OneNote مثبتًا.

## لماذا نستخدم Aspose.Note لتحويل صفحات OneNote؟
- **دقة كاملة** – يحافظ على التخطيط، الخطوط، وضربات الحبر.  
- **بدون اعتماد على Microsoft Office** – يعمل على أي منصة تدعم Java.  
- **تحكم دقيق** – اختيار تنسيق الصورة، الجودة، ورقم الصفحة المحدد.  
- **قابل للتوسع** – مناسب لمعالجة دفعات من الصفحات المتعددة.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من توفر المتطلبات التالية:

1. **Java Development Kit (JDK)** – قم بتثبيت JDK 11 أو أحدث. يمكنك تنزيله من [Oracle's official site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) إذا لم تقم بذلك بعد.  
2. **Aspose.Note for Java** – احصل على أحدث مكتبة من [Aspose.Note download page](https://releases.aspose.com/note/java/). أضف ملف JAR إلى مسار الفئة (classpath) في مشروعك.

## استيراد الحزم

أولاً، لنستورد الحزم الضرورية التي تمنحنا الوصول إلى معالجة المستندات وخيارات حفظ الصور.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## الخطوة 1: تحميل مستند OneNote

نبدأ بتحميل ملف `.one` إلى كائن `Aspose.Note` من نوع `Document`.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **نصيحة احترافية:** استخدم مسارًا مطلقًا أو تدفق موارد إذا كان ملفك داخل JAR.

## الخطوة 2: تهيئة خيارات حفظ الصورة

أنشئ مثيلًا من `ImageSaveOptions` لتحديد تنسيق الإخراج (JPEG في هذا المثال). يمكنك التبديل إلى PNG أو BMP أو GIF بتغيير `SaveFormat`.

```java
// Initialize ImageSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
```

## الخطوة 3: تحديد فهرس الصفحة

الصفحات تبدأ من الصفر، لذا `1` يختار **الصفحة الثانية**. عدّل هذه القيمة لتصدير أي صفحة تحتاجها.

```java
// Specify second page for conversion
options.setPageIndex(1);
```

## الخطوة 4: حفظ المستند كصورة

الآن نستدعي `save` على كائن `Document`، مع تمرير اسم الملف الهدف والخيارات التي قمنا بتكوينها.

```java
// Save the document
oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);
```

## الخطوة 5: طباعة التأكيد

رسالة بسيطة في وحدة التحكم تؤكد أن الصورة تم إنشاؤها بنجاح.

```java
// Print confirmation message
System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
```

## كيفية تحويل صفحات OneNote إلى صور (سيناريوهات بديلة)

إذا كنت بحاجة إلى **تحويل ملفات صورة صفحة OneNote** بالجملة، ضع الشيفرة أعلاه داخل حلقة تتكرر على `Document.getPages()`. غيّر `options.setPageIndex(i)` لكل تكرار، ويمكنك تعديل `options.setQuality(90)` للتحكم في ضغط JPEG.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|---------|-------|------|
| **الصورة فارغة** | فهرس الصفحة خارج النطاق أو المستند لم يتم تحميله بشكل صحيح. | تحقق من أن `options.setPageIndex` يقع ضمن `0 .. document.getPages().size() - 1`. |
| **تنسيق غير مدعوم** | استخدام نسخة أقدم من Aspose.Note لا تدعم بعض التنسيقات. | قم بالتحديث إلى أحدث إصدار من Aspose.Note for Java. |
| **OutOfMemoryError** | تحويل صفحات كبيرة جدًا على JVM بذاكرة منخفضة. | زيادة حجم الذاكرة (`-Xmx2g`) أو معالجة الصفحات واحدةً تلو الأخرى. |

## الأسئلة المتكررة

**س1: هل يمكنني تحويل صفحات متعددة إلى صور باستخدام هذه الطريقة؟**  
ج:. ضع منطق الحفظ داخل حلقة وعدّل `options.setPageIndex(i)` لكل صفحة تريد تصديرها.

**س2: هل Aspose.Note متوافق مع إصدارات مختلفة من ملفات OneNote؟**  
ج: بالطبع. يدعم Aspose.Note ملفات .one من OneNote 2007، 2010، 2013، والإصدارات الأحدث.

**س3: هل يمكنني تخصيص تنسيق الصورة والجودة أثناء التحويل؟**  
ج: نعم. اختر `SaveFormat.Png`، `SaveFormat.Bmp`، إلخ، واضبط `options.setQuality(int)` لجودة JPEG (0‑100).

**س4: هل يقدم Aspose.Note دعمًا للغات برمجة أخرى؟**  
ج: نعم. تتوفر مكتبات لـ .NET، Python، C++، وأكثر.

**س5: أين يمكنني العثور على دعم أو مساعدة إضافية؟**  
ج: قم بزيارة [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) أو راجع الوثائق الرسمية [هنا](https://reference.aspose.com/note/java/).

**آخر تحديث:** 2025-11-29  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}