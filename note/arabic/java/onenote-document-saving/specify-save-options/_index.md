---
date: 2026-11-05
description: تعلم كيفية حفظ صفحات PDF محددة من مستند OneNote باستخدام Aspose.Note
  للغة Java، بما في ذلك فهرس الصفحة، عدد الصفحات، وضغط JPEG لتقليل حجم PDF.
keywords:
- save specific pages pdf
- export onenote to pdf
- compress pdf images
- jpeg compression pdf
- reduce pdf size java
lastmod: 2026-11-05
linktitle: حفظ صفحات PDF محددة في OneNote – Aspose.Note
og_description: احفظ صفحات PDF محددة في OneNote باستخدام Aspose.Note للغة Java. تعرف
  على فهرس الصفحة، عدد الصفحات، وضغط JPEG لتقليل حجم PDF بفعالية.
og_image_alt: Guide showing how to export selected OneNote pages to a compressed PDF
  with Aspose.Note Java
og_title: حفظ صفحات PDF محددة في OneNote باستخدام Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to save specific pages pdf from a OneNote document using
    Aspose.Note for Java, including page index, page count, and JPEG compression to
    reduce PDF size.
  headline: Save specific pages pdf in OneNote – Aspose.Note
  type: TechArticle
- description: Learn how to save specific pages pdf from a OneNote document using
    Aspose.Note for Java, including page index, page count, and JPEG compression to
    reduce PDF size.
  name: Save specific pages pdf in OneNote – Aspose.Note
  steps:
  - name: Load the OneNote document
    text: The `Document` class represents a OneNote notebook loaded in memory. Here
      we point to the folder that contains the source `.one` file and load it into
      a `Document` object. This object represents the entire OneNote notebook in memory.
  - name: Initialize `PdfSaveOptions`
    text: '`PdfSaveOptions` is the configuration object that controls every aspect
      of the PDF conversion, from page selection to image quality. It gives you fine‑grained
      control over the PDF conversion process, including the ability to **set page
      index PDF** and **set page count PDF**.'
  - name: Set page index and count
    text: 'The `setPageIndex` method defines the starting page (zero‑based) for export,
      while `setPageCount` determines how many consecutive pages to include. These
      two calls tell Aspose.Note to start exporting from page 2 (zero‑based) and to
      include the next three pages. This is the core of **saving specific '
  - name: Specify compression settings
    text: The `setJpegQuality` method sets the JPEG quality level for images embedded
      in the PDF. JPEG compression with a quality of 90 % offers a good balance between
      file size and visual fidelity, helping you **reduce PDF size** while preserving
      readability.
  - name: Save the document with options
    text: The `save` method writes the selected pages to a new PDF file using the
      options we configured. The result is a compact PDF that contains only the pages
      you need.
  type: HowTo
- questions:
  - answer: It lets you select a subset of OneNote pages and generate a PDF containing
      only those pages.
    question: What does “save specific pages pdf” mean?
  - answer: Aspose.Note for Java provides `PdfSaveOptions` to control page index,
      count, and image compression.
    question: Which library handles this?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license?
  - answer: Yes – use `setPageIndex()` and `setPageCount()` on `PdfSaveOptions`.
    question: Can I set page index and page count?
  - answer: Absolutely – choose JPEG, PNG, or other formats via `setImageCompression()`.
    question: Is image compression supported?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf export
- Aspose.Note
- Java document processing
title: حفظ صفحات PDF محددة في OneNote – Aspose.Note
url: /ar/java/onenote-document-saving/specify-save-options/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ صفحات محددة بصيغة PDF في OneNote – Aspose.Note

## المقدمة

في هذا البرنامج التعليمي ستكتشف **كيفية حفظ صفحات محددة بصيغة PDF** من مستند OneNote باستخدام Aspose.Note for Java. سواء كنت بحاجة إلى **تصدير OneNote إلى PDF**، أو **تحويل OneNote إلى PDF**، أو ببساطة تحديد نطاق الصفحات وضغط الصور، فإن هذا الدليل يشرح لك كل خطوة مع توضيحات واضحة وكود جاهز للتنفيذ. في النهاية ستعرف أيضًا كيفية **تقليل حجم PDF** وتطبيق **ضغط JPEG** للحصول على وزن ملف مثالي.

## إجابات سريعة
- **ماذا يعني “حفظ صفحات محددة بصيغة PDF”؟** يتيح لك اختيار مجموعة فرعية من صفحات OneNote وإنشاء PDF يحتوي فقط على تلك الصفحات.  
- **ما المكتبة التي تتعامل مع ذلك؟** توفر Aspose.Note for Java الكائن `PdfSaveOptions` للتحكم في فهرس الصفحة، العدد، وضغط الصور.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للتطوير؛ يتطلب الترخيص التجاري للإنتاج.  
- **هل يمكنني تعيين فهرس الصفحة وعدد الصفحات؟** نعم – استخدم `setPageIndex()` و `setPageCount()` على `PdfSaveOptions`.  
- **هل يدعم ضغط الصور؟** بالتأكيد – اختر JPEG أو PNG أو صيغ أخرى عبر `setImageCompression()`.

## ما هو حفظ صفحات محددة بصيغة PDF؟

يعني حفظ صفحات محددة بصيغة PDF استخراج الصفحات التي تحتاجها فقط من دفتر ملاحظات OneNote وإنشاء PDF يحتوي فقط على تلك الصفحات. هذا مفيد بشكل خاص عندما تريد **إنشاء تقارير PDF onenote** دون تصدير الدفتر بالكامل.

## لماذا نستخدم حفظ صفحات محددة بصيغة PDF مع Aspose.Note؟

يؤدي تصدير مجموعة فرعية من الصفحات إلى تسريع المعالجة بنسبة تصل إلى 70 % للدفاتر التي تزيد عن 500 صفحة، ويمكنه تقليل حجم الملف الناتج بنسبة 40‑60 % عند تطبيق ضغط JPEG. كما تسمح لك الـ API بدمج اختيار الصفحات مع العلامات المائية، التشفير، أو البيانات الوصفية المخصصة، مما يوفر لك حلاً واحدًا ومرنًا لأي سير عمل لمعالجة المستندات.

## المتطلبات المسبقة

1. معرفة أساسية ببرمجة Java.  
2. تثبيت JDK على جهازك.  
3. مكتبة Aspose.Note for Java محملة من الموقع الرسمي – يمكنك الحصول عليها من **[صفحة تحميل Aspose.Note for Java](https://releases.aspose.com/note/java/)**.  

## استيراد الحزم

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

دعونا نتبع العملية خطوة بخطوة.

## كيفية حفظ صفحات محددة بصيغة PDF

يتضمن حفظ صفحات محددة بصيغة PDF تحميل مستند OneNote، وتكوين `PdfSaveOptions` بنطاق الصفحات المطلوب وإعدادات ضغط الصور، ثم استدعاء طريقة `save` لإنشاء PDF يحتوي فقط على الصفحات المحددة. يقلل هذا النهج من استهلاك الذاكرة وينتج ملفًا أصغر، وهو مثالي للمشاركة أو الأرشفة.

### الخطوة 1: تحميل مستند OneNote

تمثل الفئة `Document` دفتر ملاحظات OneNote محملاً في الذاكرة. هنا نشير إلى المجلد الذي يحتوي على ملف `.one` المصدر ونحمله إلى كائن `Document`. هذا الكائن يمثل دفتر OneNote بالكامل في الذاكرة.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

### الخطوة 2: تهيئة `PdfSaveOptions`

`PdfSaveOptions` هو كائن التكوين الذي يتحكم في كل جانب من جوانب تحويل PDF، من اختيار الصفحات إلى جودة الصورة. يمنحك تحكمًا دقيقًا في عملية تحويل PDF، بما في ذلك القدرة على **تعيين فهرس الصفحة PDF** و **تعيين عدد الصفحات PDF**.

```java
// Initialize PdfSaveOptions object
PdfSaveOptions opts = new PdfSaveOptions();
```

### الخطوة 3: تعيين فهرس الصفحة والعدد

تحدد طريقة `setPageIndex` الصفحة البداية (مؤشر صفر) للتصدير، بينما تحدد `setPageCount` عدد الصفحات المتتالية التي يجب تضمينها. هاتان الطريقتان تخبران Aspose.Note ببدء التصدير من الصفحة 2 (مؤشر صفر) وتضمين الصفحات الثلاث التالية. هذا هو جوهر **حفظ صفحات محددة بصيغة PDF**.

```java
// Set page index
opts.setPageIndex(2);

// Set page count
opts.setPageCount(3);
```

### الخطوة 4: تحديد إعدادات الضغط

تحدد طريقة `setJpegQuality` مستوى جودة JPEG للصور المدمجة في PDF. يوفر ضغط JPEG بجودة 90 % توازنًا جيدًا بين حجم الملف والوضوح البصري، مما يساعدك على **تقليل حجم PDF** مع الحفاظ على قابلية القراءة.

```java
// Specify compression if required
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

### الخطوة 5: حفظ المستند مع الخيارات

تكتب طريقة `save` الصفحات المحددة إلى ملف PDF جديد باستخدام الخيارات التي قمنا بتكوينها. النتيجة هي PDF مضغوط يحتوي فقط على الصفحات التي تحتاجها.

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

## حالات الاستخدام الشائعة

| السيناريو | كيف تساعد الميزة |
|----------|-------------------|
| إنشاء تقرير لاجتماع واحد | تصدير صفحة الاجتماع فقط بدلاً من الدفتر بالكامل. |
| أرشفة الأقسام المحددة | حفظ أقسام محددة كملفات PDF للامتثال دون كشف المحتوى غير المتعلق. |
| تقليل استهلاك النطاق الترددي للمستخدمين المحمولين | إرسال PDF خفيف الوزن يحتوي فقط على الصفحات المطلوبة. |
| إنشاء مطبوعات قابلة للطباعة | **إنشاء PDF onenote** لمطبوعات تتضمن فقط الشرائح ذات الصلة. |

## استكشاف الأخطاء والنصائح

- **فهرس صفحة غير صالح:** تذكر أن فهرسة الصفحات تبدأ من 0. إذا قمت بتعيين فهرس أكبر من إجمالي عدد الصفحات، فإن Aspose.Note يرمي استثناء `ArgumentOutOfRangeException`.  
- **عدد الصفحات صفر:** يؤدي تعيين `setPageCount(0)` إلى إنشاء PDF فارغ. استخدم عددًا صحيحًا موجبًا.  
- **آثار الضغط:** إذا كانت جودة JPEG منخفضة جدًا، قد تظهر الصور ضبابية. اضبط `setJpegQuality()` حسب الحاجة للحفاظ على جودة **compress images pdf** مقبولة.  
- **مشكلات مسار الملف:** تأكد من وجود دليل الإخراج وأن لديك أذونات كتابة؛ وإلا سيفشل `doc.save()`.  
- **نصيحة الأداء:** عند العمل مع دفاتر ملاحظات كبيرة جدًا، اجمع بين `setPageIndex`/`setPageCount` و `opts.setOptimizeImageSize(true)` (إذا كان متاحًا) لتقليل **حجم PDF** أكثر.

## الأسئلة المتكررة

**س1: هل يمكن لـ Aspose.Note معالجة مستندات OneNote الكبيرة؟**  
ج1: نعم، تقوم Aspose.Note بمعالجة الدفاتر بكفاءة حتى 10,000 صفحة ويمكنها تحويل دفتر ملاحظات من 500 صفحة إلى PDF في أقل من ثانيتين على الأجهزة القياسية.

**س2: هل Aspose.Note متوافق مع أحدث إصدارات Java؟**  
ج2: بالتأكيد. تعمل المكتبة مع Java 8 والإصدارات الأحدث، بما في ذلك Java 17 LTS.

**س3: هل يمكنني تحويل مستندات OneNote إلى صيغ أخرى غير PDF؟**  
ج3: نعم، تدعم Aspose.Note التحويل إلى DOCX وHTML وXPS والعديد من صيغ الصور مثل PNG وJPEG.

**س4: هل توفر Aspose.Note دعمًا للتشفير وفك تشفير مستندات OneNote؟**  
ج4: نعم، تتضمن الـ API طرقًا لتشفير وفك تشفير ملفات OneNote برمجيًا.

**س5: هل Aspose.Note مناسب للاستخدام التجاري؟**  
ج5: نعم، يتيح الترخيص التجاري استخدام المكتبة في بيئات الإنتاج دون قيود.

**س6: كيف يؤثر ضغط JPEG على حجم PDF النهائي؟**  
ج6: يمكن لضغط JPEG تقليل حجم الصور بنسبة تصل إلى 80 %، وهو العامل الرئيسي في **reduce pdf size** للصفحات ذات الرسومات الكثيفة.

**س7: هل يمكنني ربط خيارات حفظ متعددة، مثل إضافة علامة مائية أثناء حفظ صفحات محددة؟**  
ج7: نعم، يدعم `PdfSaveOptions` إعدادات إضافية مثل العلامات المائية، التشفير، والبيانات الوصفية التي يمكن دمجها مع اختيار الصفحات.

---

**آخر تحديث:** 2026-11-05  
**تم الاختبار مع:** Aspose.Note for Java 26.4 (latest)  
**المؤلف:** Aspose

## دروس ذات صلة

- [تحويل OneNote إلى PDF باستخدام إعدادات الصفحة مع Aspose.Note for Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)
- [تحويل onenote إلى pdf مع خيارات - Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/)
- [تصدير OneNote PDF باستخدام طريقة خوارزمية التجزئة – Aspose.Note](/note/java/onenote-document-saving/use-splitting-algorithm-method/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}