---
date: 2026-07-05
description: تعلم كيفية تصدير صفحات OneNote إلى صور باستخدام Java، واكتشف كيفية تحويل
  صورة صفحة OneNote باستخدام Aspose.Note. اتبع دليلنا خطوة بخطوة للتكامل السريع.
keywords:
- export onenote page
- convert .one to image
- onenote image conversion
- batch onenote conversion
linktitle: تصدير صفحة OneNote إلى صورة باستخدام Java
schemas:
- author: Aspose
  dateModified: '2026-07-05'
  description: Learn how to export OneNote pages to images using Java, and discover
    how to convert OneNote page image with Aspose.Note. Follow our step‑by‑step guide
    for quick integration.
  headline: Export OneNote Page to Image Using Java
  type: TechArticle
- questions:
  - answer: Aspose.Note for Java
    question: What library is required?
  - answer: Yes – JPEG, PNG, BMP, GIF, and TIFF via `ImageSaveOptions`
    question: Can I choose the image format?
  - answer: A valid Aspose.Note license is required for commercial deployments.
    question: Do I need a license for production?
  - answer: Any page by setting the zero‑based `PageIndex`.
    question: Which page can I export?
  - answer: Typical pages convert in under a second on a standard JVM.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.Note Java API
title: تصدير صفحة OneNote إلى صورة باستخدام Java
url: /ar/java/onenote-document-loading/convert-page-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير صفحة OneNote إلى صورة باستخدام Java

## مقدمة

في هذا الدرس ستتعلم **كيفية تصدير صفحات OneNote إلى ملفات صور** باستخدام Java ومكتبة Aspose.Note القوية. تحويل صفحة OneNote إلى صورة مفيد عندما تحتاج إلى تضمين محتوى الدفتر في تقارير، مشاركة لقطات مع زملاء لا يملكون OneNote، أو إنشاء صور مصغرة لنظام إدارة المستندات. سنستعرض كل سطر من الشيفرة، نشرح لماذا كل إعداد مهم، ونظهر لك كيفية تعديل النتيجة لسيناريوهات الدفعات.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.Note for Java  
- **هل يمكنني اختيار تنسيق الصورة؟** نعم – JPEG, PNG, BMP, GIF, و TIFF عبر `ImageSaveOptions`  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم وجود ترخيص Aspose.Note صالح للنشر التجاري.  
- **أي صفحة يمكنني تصديرها؟** أي صفحة عن طريق ضبط `PageIndex` الذي يبدأ من الصفر.  
- **ما مدى سرعة التحويل؟** عادةً ما يتم تحويل الصفحات في أقل من ثانية على JVM قياسي.

## ما هو تصدير صفحات OneNote إلى صور؟
تصدير صفحات OneNote إلى صور يحول المحتوى الغني للصفحة—النص، الحبر، الجداول، والوسائط المدمجة—إلى صورة نقطية ثابتة مثل JPEG. هذا يخلق تمثيلًا بصريًا محمولًا يمكن عرضه على أي جهاز، حتى في حال عدم تثبيت عميل OneNote.

## لماذا نستخدم Aspose.Note لتحويل صفحات OneNote؟
تضمن Aspose.Note **دقة تخطيط 100 %**، مع معالجة الخطوط، خطوط الحبر، والكائنات المدمجة دون فقدان. تعمل **بشكل مستقل عن Microsoft Office**، لذا يمكنك تشغيلها على JVM في Windows أو Linux أو macOS. توفر API **تحكمًا دقيقًا** في تنسيق الصورة، الجودة، واختيار الصفحات، وتستطيع **معالجة أكثر من 10,000 صفحة في دفعة واحدة** دون استنزاف الذاكرة.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من توفر المتطلبات التالية:

1. **Java Development Kit (JDK)** – ثبّت JDK 11 أو أحدث. يمكنك تنزيله من [الموقع الرسمي لأوراكل](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) إذا لم تقم بذلك بعد.  
2. **Aspose.Note for Java** – احصل على أحدث مكتبة من [صفحة تنزيل Aspose.Note](https://releases.aspose.com/note/java/). أضف ملف JAR إلى مسار الـ classpath في مشروعك.

## استيراد الحزم

`Document`، `ImageSaveOptions`، والفئات المرتبطة هي جزء من API الخاصة بـ Aspose.Note، وتوفر وظائف لتحميل، تعديل، وحفظ ملفات OneNote.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## الخطوة 1: تحميل مستند OneNote

الفئة `Document` تمثّل دفتر OneNote واحد في الذاكرة. تحميل ملف `.one` يمنحك إمكانية الوصول إلى صفحاته، أقسامه، وموارده.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **نصيحة احترافية:** استخدم مسارًا مطلقًا أو تدفق مورد إذا كان ملفك داخل JAR؛ فهذا يتجنّب `FileNotFoundException` أثناء التشغيل.

## الخطوة 2: تهيئة خيارات حفظ الصورة

`ImageSaveOptions` تحدد كيفية تحويل الصفحة إلى صورة. ضبط `SaveFormat` إلى `Jpeg` ينتج ملفًا مدعومًا على نطاق واسع، بينما `Png` يحافظ على الشفافية.

```java
// Initialize ImageSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
```

## الخطوة 3: تحديد فهرس الصفحة

الفهارس تبدأ من الصفر، لذا `1` يختار **الصفحة الثانية**. عدّل هذه القيمة لتصدير أي صفحة تحتاجها، أو كرّر العملية عبر جميع الصفحات للتحويل الدفعي.

```java
// Specify second page for conversion
options.setPageIndex(1);
```

## الخطوة 4: حفظ المستند كصورة

استدعاء `save` على كائن `Document` يكتب الصفحة المرسومة إلى نظام الملفات باستخدام الخيارات التي ضبطتها.

```java
// Save the document
oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);
```

## الخطوة 5: طباعة التأكيد

رسالة بسيطة في وحدة التحكم تؤكد أن الصورة تم إنشاؤها بنجاح، وهو مفيد لتسجيل الأحداث في خطوط الأنابيب الآلية.

```java
// Print confirmation message
System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
```

## حالات الاستخدام الشائعة

- **إنشاء تقارير:** دمج لقطات OneNote مباشرةً في تقارير PDF أو HTML دون الحاجة إلى لقطات يدوية.  
- **إنشاء صور مصغرة:** توليد معاينات منخفضة الدقة لمجموعة كبيرة من صفحات OneNote، مما يتيح بحثًا بصريًا سريعًا.  
- **المشاركة عبر المنصات:** مشاركة صورة JPEG لصفحة OneNote مع مستخدمين على macOS أو Linux أو الأجهزة المحمولة التي لا تملك عميل OneNote.

## كيفية تحويل صفحات OneNote إلى صور (سيناريوهات بديلة)

إذا كنت بحاجة إلى **تحويل صور صفحات OneNote بالجملة**، ضع الشيفرة أعلاه داخل حلقة تتكرر على `document.getPages()`. حدّث `options.setPageIndex(i)` لكل تكرار، ويمكنك تعديل `options.setQuality(90)` للتحكم في ضغط JPEG. يتيح لك هذا النهج معالجة دفاتر كاملة باستدعاء طريقة واحدة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **الصورة فارغة** | فهرس الصفحة خارج النطاق أو المستند لم يُحمّل بشكل صحيح. | تأكد أن `options.setPageIndex` يقع ضمن `0 .. document.getPages().size() - 1`. |
| **تنسيق غير مدعوم** | استخدام نسخة قديمة من Aspose.Note لا تدعم بعض الصيغ. | حدّث إلى أحدث إصدار من Aspose.Note for Java. |
| **OutOfMemoryError** | تحويل صفحات كبيرة جدًا على JVM بذاكرة منخفضة. | زد حجم الـ heap (`-Xmx2g`) أو عالج الصفحات واحدةً تلو الأخرى. |

## الأسئلة المتكررة

**س1: هل يمكنني تحويل عدة صفحات إلى صور باستخدام هذه الطريقة؟**  
ج: نعم. ضع منطق الحفظ داخل حلقة وغيّر `options.setPageIndex(i)` لكل صفحة تريد تصديرها.

**س2: هل Aspose.Note متوافق مع إصدارات مختلفة من ملفات OneNote؟**  
ج: بالتأكيد. تدعم Aspose.Note ملفات `.one` من OneNote 2007، 2010، 2013، 2016، والإصدارات الأحدث.

**س3: هل يمكنني تخصيص تنسيق الصورة والجودة أثناء التحويل؟**  
ج: نعم. اختر `SaveFormat.Png`، `SaveFormat.Bmp`، أو `SaveFormat.Tiff`، واضبط `options.setQuality(int)` لضغط JPEG (0‑100).

**س4: هل تقدم Aspose.Note دعمًا للغات برمجة أخرى؟**  
ج: نعم. تتوفر مكتبات لـ .NET، Python، C++، وأكثر، جميعها تقدم وظائف مماثلة.

**س5: أين يمكنني العثور على دعم إضافي أو مساعدة؟**  
ج: زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) أو راجع الوثائق الرسمية [هنا](https://reference.aspose.com/note/java/).

---

**آخر تحديث:** 2026-07-05  
**تم الاختبار مع:** Aspose.Note for Java 26.4  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [Export OneNote Pages – Convert Specific Page Range to PDF with Java](/note/java/onenote-document-loading/convert-page-range-to-pdf/)
- [Convert Notebook to Image in OneNote - Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-image/)
- [Aspose Java Tutorial - Get Information about Pages in OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}