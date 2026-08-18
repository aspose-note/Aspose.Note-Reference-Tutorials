---
date: 2026-08-18
description: تعرف على كيفية تصدير OneNote إلى PDF، وضبط تنسيق الفقرة في Java، وحفظ
  OneNote كملف PDF باستخدام Aspose.Note for Java.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: تعيين نمط الفقرة أثناء إنشاء مستند OneNote في Java
og_description: تصدير OneNote إلى PDF وضبط نمط الفقرة في Java باستخدام Aspose.Note.
  اتبع هذا الدليل خطوة بخطوة لإنشاء ملفات PDF مصقولة بسهولة.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: تصدير OneNote إلى PDF مع نمط الفقرة في Java (58 حرفًا)
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  headline: How to export OneNote to PDF with paragraph style in Java
  type: TechArticle
- description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  name: How to export OneNote to PDF with paragraph style in Java
  steps:
  - name: set document directory
    text: Define where the generated files will be saved. Replace `"Your Document
      Directory"` with an absolute or relative path on your machine.
  - name: initialize document object
    text: Create the root `Document` that represents the OneNote file. **Definition
      anchor:** `Document` is Aspose.Note’s top‑level object that holds one or more
      pages in memory.
  - name: initialize page object
    text: A OneNote file consists of one or more pages; we start with a single page.
      **Definition anchor:** `Page` represents a single OneNote page, containing outlines,
      images, and other elements.
  - name: initialize outline object
    text: Outlines act as containers for outline elements (think of them as sections).
      **Definition anchor:** `Outline` groups related `OutlineElement` objects and
      defines their visual hierarchy.
  - name: initialize outline element object
    text: Here we **add outline element** that will hold our rich text. **Definition
      anchor:** `OutlineElement` is a leaf node inside an `Outline` that can contain
      text, images, or other media.
  - name: set text style (set paragraph style)
    text: '`ParagraphStyle` defines the font family, size, color, and other typographic
      attributes for a paragraph. The `ParagraphStyle` instance defines the font,
      size, and color—this is where we **set paragraph style** for the upcoming text
      node.'
  - name: initialize rich text object
    text: '`RichText` is the node that stores styled text within an `OutlineElement`.
      We create a `RichText` node, insert a simple string, and attach the previously
      defined style.'
  - name: add rich text node to outline element
    text: Now the styled text lives inside the outline element.
  - name: add outline element node to outline
    text: The outline now contains the element that holds our paragraph.
  - name: add outline node to page
    text: We place the outline onto the page.
  type: HowTo
- questions:
  - answer: Yes, the API supports tables, images, hyperlinks, and advanced layout
      features in addition to plain text.
    question: Can Aspose.Note handle complex formatting such as tables or images?
  - answer: Direct conversion isn’t provided, but you can extract PDF content and
      rebuild a OneNote document using the API.
    question: Is it possible to convert a OneNote PDF back to a OneNote file?
  - answer: Absolutely. Aspose.Note for Java is platform‑independent; just ensure
      a compatible JDK is installed.
    question: Does the library work on Linux/macOS environments?
  - answer: Create additional `Page` and `Outline` objects, then append them to the
      `Document` just like the single‑page example.
    question: How do I add multiple pages or outlines?
  - answer: The official Aspose.Note documentation and the [support forum](https://forum.aspose.com/c/note/28)
      contain many code samples and real‑world scenarios.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- export onenote
- aspose.note
- java document processing
title: كيفية تصدير OneNote إلى PDF مع نمط الفقرة في Java
url: /ar/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ضبط نمط الفقرة أثناء إنشاء مستند OneNote في Java

## مقدمة

تصدير OneNote إلى PDF برمجيًا هو مطلب شائع لمحركات التقارير، وخدمات تدوين الملاحظات الآلية، وأنابيب تحويل المستندات. في هذا البرنامج التعليمي ستتعلم كيفية **تصدير OneNote إلى PDF**، وتطبيق تنسيق فقرة مخصص، وحفظ ملف OneNote — كل ذلك باستخدام Aspose.Note for Java. في النهاية ستحصل على مقتطف Java جاهز للاستخدام ينتج PDF مصقول بالمظهر الدقيق الذي حددته.

## إجابات سريعة

- **ماذا يعني “set paragraph style”?** يطبق الخط، الحجم، اللون، وغيرها من سمات التنسيق على فقرة من النص.  
- **هل يمكنني تصدير النتيجة إلى PDF؟** نعم – ينتهي الدليل بحفظ ملف OneNote كملف PDF.  
- **هل أحتاج إلى ترخيص لـ Aspose.Note؟** الإصدار التجريبي المجاني يكفي للتقييم؛ يلزم ترخيص تجاري للاستخدام في الإنتاج.  
- **ما هي بيئات التطوير المتكاملة (IDEs) المدعومة؟** أي بيئة تطوير Java – Eclipse، IntelliJ IDEA، NetBeans، إلخ.  
- **كم من الوقت يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لمستند أساسي.  

## كيفية تصدير OneNote إلى PDF في Java؟

`Document` يمثل ملف OneNote يحتوي على صفحات، مخططات، وعناصر أخرى. قم بتحميل مستند OneNote الخاص بك باستخدام `new Document()` (أو أنشئ مستندًا جديدًا) واستدعِ `document.save("output.pdf", SaveFormat.Pdf)`. تقوم Aspose.Note بكتابة ملف PDF في خطوة واحدة، مع الحفاظ على الأنماط، الصور، والمخططات دون الحاجة إلى تثبيت Microsoft OneNote. هذا النهج المباشر يعمل على Windows وLinux وmacOS مع أي JDK 1.8+.

## ما هو “set paragraph style” في Aspose.Note؟

`ParagraphStyle` هي الفئة التي تخزن اسم الخط، الحجم، اللون، المحاذاة، وغيرها من إعدادات الطباعة لفقرة. من خلال إرفاق كائن `ParagraphStyle` إلى عقدة `RichText` يمكنك التحكم بدقة في كيفية ظهور تلك الفقرة في صفحة OneNote النهائية والPDF المُصدّر.

## لماذا تصدير OneNote إلى PDF؟

يضمن تصدير OneNote إلى PDF الحفاظ على العلامة التجارية المتسقة عن طريق حفظ الخطوط والألوان المؤسسية، ويحسن قابلية القراءة من خلال الحفاظ على التخطيط الدقيق للطباعة أو الأرشفة، ويوفر وصولًا عبر المنصات بحيث يمكن للمستلمين عرض المستند على أي جهاز دون الحاجة إلى OneNote. كما يقدم فوائد في الأداء، مما يسمح بمعالجة المستندات الكبيرة بسرعة.

## المتطلبات المسبقة

1. **Java Development Kit (JDK) 1.8+** – أي JDK حديث سيعمل.  
2. **Aspose.Note for Java** – قم بتنزيل أحدث JAR من [Aspose.Note download page](https://releases.aspose.com/note/java/).  
3. **An IDE** (Eclipse, IntelliJ IDEA, أو NetBeans) لتجميع وتشغيل العينة.  

> **نصيحة احترافية:** أضف ملف JAR الخاص بـ Aspose.Note إلى مسار الفئة (classpath) في مشروعك عبر Maven (`<dependency>`) أو عن طريق الإشارة يدويًا إلى ملف JAR في بيئة التطوير الخاصة بك.

## استيراد الحزم

أولاً، استورد المساحات الاسمية المطلوبة. يبقى هذا الجزء دون تغيير.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> الفئة `ParagraphStyle` هي المفتاح لـ **set paragraph style** لاحقًا في البرنامج التعليمي.

## دليل خطوة بخطوة

فيما يلي شرح مختصر لكل عملية. كتل الشيفرة هي نفسها تمامًا كما في العينة الأصلية؛ نضيف فقط نصًا توضيحيًا.

### الخطوة 1: تعيين دليل المستند
حدد المكان الذي سيتم حفظ الملفات المُولدة فيه.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بمسار مطلق أو نسبي على جهازك.

### الخطوة 2: تهيئة كائن المستند
أنشئ كائن `Document` الجذري الذي يمثل ملف OneNote.

```java
Document doc = new Document();
```

**مرساة التعريف:** `Document` هو كائن المستوى الأعلى في Aspose.Note الذي يحتفظ بصفحة واحدة أو أكثر في الذاكرة.

### الخطوة 3: تهيئة كائن الصفحة
يتكون ملف OneNote من صفحة واحدة أو أكثر؛ نبدأ بصفحة واحدة.

```java
Page page = new Page();
```

**مرساة التعريف:** `Page` تمثل صفحة OneNote واحدة، تحتوي على مخططات، صور، وعناصر أخرى.

### الخطوة 4: تهيئة كائن المخطط
تعمل المخططات كحاويات لعناصر المخطط (فكر فيها كأقسام).

```java
Outline outline = new Outline();
```

**مرساة التعريف:** `Outline` يجمع كائنات `OutlineElement` ذات الصلة ويحدد التسلسل الهرمي البصري لها.

### الخطوة 5: تهيئة كائن عنصر المخطط
هنا نقوم **بإضافة عنصر مخطط** الذي سيحمل النص المنسق.

```java
OutlineElement outlineElem = new OutlineElement();
```

**مرساة التعريف:** `OutlineElement` هو عقدة نهائية داخل `Outline` يمكنها احتواء نص أو صور أو وسائط أخرى.

### الخطوة 6: تعيين نمط النص (set paragraph style)
`ParagraphStyle` يحدد عائلة الخط، الحجم، اللون، وغيرها من سمات الطباعة لفقرة.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

مثيل `ParagraphStyle` يحدد الخط، الحجم، واللون — هنا نقوم **بتعيين نمط الفقرة** لعقدة النص القادمة.

### الخطوة 7: تهيئة كائن النص المنسق
`RichText` هو العقدة التي تخزن النص المنسق داخل `OutlineElement`.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

ننشئ عقدة `RichText`، ندرج سلسلة بسيطة، ونرفق النمط المحدد مسبقًا.

### الخطوة 8: إضافة عقدة النص المنسق إلى عنصر المخطط
```java
outlineElem.appendChildLast(text);
```

الآن النص المنسق موجود داخل عنصر المخطط.

### الخطوة 9: إضافة عقدة عنصر المخطط إلى المخطط
```java
outline.appendChildLast(outlineElem);
```

المخطط الآن يحتوي على العنصر الذي يحمل فقرتنا.

### الخطوة 10: إضافة عقدة المخطط إلى الصفحة
```java
page.appendChildLast(outline);
```

نضع المخطط على الصفحة.

### الخطوة 11: إضافة عقدة الصفحة إلى المستند
```java
doc.appendChildLast(page);
```

المستند الآن يحتوي على صفحة واحدة مع نصنا المنسق.

### الخطوة 12: حفظ المستند (تصدير OneNote PDF)
```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

طريقة `save` تكتب ملف OneNote و**تصدّر OneNote إلى PDF** في خطوة واحدة. يمكنك أيضًا حفظه كـ `.one` باستخدام `SaveFormat.One` إذا كنت بحاجة إلى الصيغة الأصلية.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **File not found** | `dataDir` يشير إلى مجلد غير موجود. | تأكد من وجود المجلد أو أنشئه برمجيًا (`new File(dataDir).mkdirs();`). |
| **Blank PDF** | لم يتم إضافة أي محتوى قبل الحفظ. | تحقق من أن عقدة `RichText` مضافة وأن النمط محدد. |
| **Unsupported font** | اسم الخط غير مثبت على النظام. | استخدم خطًا شائعًا مثل `"Arial"` أو قم بدمج الخط في المشروع. |

## الأسئلة المتكررة

**Q: هل يمكن لـ Aspose.Note التعامل مع تنسيق معقد مثل الجداول أو الصور؟**  
A: نعم، يدعم API الجداول، الصور، الروابط التشعبية، وميزات التخطيط المتقدمة بالإضافة إلى النص العادي.

**Q: هل من الممكن تحويل PDF الخاص بـ OneNote مرة أخرى إلى ملف OneNote؟**  
A: التحويل المباشر غير متوفر، ولكن يمكنك استخراج محتوى PDF وإعادة بناء مستند OneNote باستخدام الـ API.

**Q: هل تعمل المكتبة على بيئات Linux/macOS؟**  
A: بالتأكيد. Aspose.Note for Java مستقل عن المنصة؛ فقط تأكد من تثبيت JDK متوافق.

**Q: كيف يمكنني إضافة صفحات أو مخططات متعددة؟**  
A: أنشئ كائنات `Page` و `Outline` إضافية، ثم أضفها إلى `Document` كما في مثال الصفحة الواحدة.

**Q: أين يمكنني العثور على المزيد من الأمثلة؟**  
A: توثيق Aspose.Note الرسمي ومنتدى [الدعم](https://forum.aspose.com/c/note/28) يحتويان على العديد من عينات الشيفرة والسيناريوهات الواقعية.

## الخلاصة

لقد رأيت الآن كيفية **set paragraph style**، **add outline element**، و**export OneNote to PDF** باستخدام Aspose.Note for Java. يضمن تطبيق النص المنسق مبكرًا أن يبدو PDF النهائي احترافيًا، وتتعامل عملية `save` ذات الاستدعاء الواحد مع التحويل بكفاءة. يمكنك توسيع هذه القاعدة بإضافة صور، جداول، أو بيانات تعريف مخصصة لتلبية احتياجات تطبيقك المحددة.

---

**آخر تحديث:** 2026-08-18  
**تم الاختبار مع:** Aspose.Note for Java 26.5 (latest release)  
**المؤلف:** Aspose

## الدروس ذات الصلة

- [كيفية حفظ OneNote كملف PDF باستخدام Aspose.Note for Java](/note/java/onenote-document-loading/load-save-format/)
- [تعلم تحويل OneNote إلى PDF باستخدام Aspose.Note مع PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [ضبط نمط الفقرة الافتراضي في OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}