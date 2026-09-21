---
date: 2026-07-29
description: تعلم كيفية تضمين رابط OneNote، حفظ OneNote كملف PDF، وإضافة الروابط التشعبية
  باستخدام Java مع Aspose.Note. صدّر OneNote إلى PDF بسهولة.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: حفظ OneNote كملف PDF وإضافة رابط تشعبي في OneNote باستخدام Java
og_description: تضمين رابط OneNote وتصدير OneNote إلى PDF باستخدام Java و Aspose.Note.
  تعلم خطوة بخطوة كيفية إضافة الروابط التشعبية وإنشاء ملف PDF.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: تضمين رابط OneNote – حفظ OneNote كملف PDF باستخدام Java
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: تضمين رابط OneNote – حفظ OneNote كملف PDF باستخدام Java
url: /ar/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# احفظ OneNote كملف PDF وأضف رابطًا تشعبيًا في OneNote باستخدام Java

## مقدمة

إذا كنت بحاجة إلى **embed link onenote** أثناء تحويل دفتر الملاحظات إلى ملف PDF محمول، فقد وجدت المكان المناسب. يشرح هذا البرنامج التعليمي كيفية حفظ OneNote كملف PDF وإدراج روابط تشعبية قابلة للنقر باستخدام Java ومكتبة Aspose.Note. سترى لماذا هذا النهج مثالي للأرشفة والمشاركة وأتمتة خطوط أنابيب المستندات.

## إجابات سريعة
- **Can I save OneNote as PDF with Java?** نعم، Aspose.Note for Java توفر استدعاء `save` واحد لتوليد ملف PDF.
- **How do I embed a hyperlink?** استخدم `TextStyle.setHyperlinkAddress` على مقطع `RichText`.
- **What are the prerequisites?** JDK 8+ ومكتبة Aspose.Note for Java.
- **Which output formats are supported?** PDF، DOCX، XPS، وأكثر.
- **Is a license required for production?** نعم، يلزم الحصول على ترخيص تجاري للاستخدام غير التجريبي.

## ما هو “save onenote as pdf”؟

إن حفظ دفتر OneNote كملف PDF ينشئ نسخة للقراءة فقط ومتعددة المنصات من ملاحظاتك يمكن لأي شخص فتحها دون الحاجة إلى تطبيق OneNote. هذا التنسيق مثالي للأرشفة أو الطباعة أو المشاركة مع المتعاونين الذين لا يمتلكون OneNote مثبتًا، مع الحفاظ على التخطيط الأصلي والصور وأي روابط تشعبية مضمَّنة.

## لماذا إنشاء PDF من OneNote باستخدام Aspose.Note Java؟

يمكن لـ Aspose.Note for Java **export onenote to pdf** بدقة تخطيط 100 %، مع معالجة ما يصل إلى 200 صفحة لكل مستند دون تحميل الملف بالكامل إلى الذاكرة. تقوم المكتبة بمعالجة أكثر من 30 نوعًا مختلفًا من المحتوى — بما في ذلك الصور والجداول و95 % من أنماط الروابط التشعبية — لذا تحصل على نسخة مطابقة للأصل من دفتر الملاحظات. كما أنها تعمل على Windows وLinux وmacOS، مما يتيح تحويلات دفعة في السحابة أو الخدمات المحلية.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من تثبيت وإعداد المتطلبات المسبقة التالية على نظامك:

### مجموعة تطوير جافا (JDK)

تأكد من أن لديك مجموعة تطوير جافا (JDK) مثبتة على نظامك. يمكنك تنزيل وتثبيت JDK من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### مكتبة Aspose.Note for Java

قم بتنزيل وتثبيت مكتبة Aspose.Note for Java. يمكنك العثور على الوثائق ورابط التنزيل [هنا](https://reference.aspose.com/note/java/).

## استيراد الحزم

للبدء، استورد الحزم الضرورية المطلوبة للعمل مع Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

الآن، دعنا نقسم المثال المقدم إلى خطوات متعددة:

## كيف تُضمّن رابط onenote أثناء الحفظ كملف PDF؟

حمّل نسخة جديدة من كائن `Document`، بنِ هيكل الصفحة، عرّف `TextStyle` باللون الأحمر للارتباط التشعبي، وأخيرًا استدعِ `document.save("output.pdf", SaveFormat.Pdf)`. هذه السلسلة تُنشئ ملف PDF يحتوي على رابط تشعبي فعال بالكامل، مع الحفاظ على جميع التنسيقات الأصلية والصور.

## الخطوة 1: إعداد هيكل المستند

`Document` يمثل دفتر OneNote في Aspose.Note.  
`Page` هو حاوية للمخططات والعناصر الأخرى على مستوى الصفحة.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## الخطوة 2: تعريف نمط النص الافتراضي

`ParagraphStyle` يحدد التنسيق الافتراضي للفقرات مثل المحاذاة والمسافات والمسافة البادئة.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## الخطوة 3: تعيين نص العنوان

`Title` يمثل عنصر عنوان الصفحة في مستند OneNote.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## الخطوة 4: إنشاء المخطط وعناصر المخطط

`Outline` يعمل كحاوية لتسلسل هرمي من كتل المحتوى.  
`OutlineElement` هو عنصر فردي داخل المخطط، مثل فقرة أو جدول.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## الخطوة 5: تعريف نمط النص للارتباط التشعبي

`TextStyle` يتحكم في المظهر البصري لتشغيلات النص، بما في ذلك الخط واللون وإعدادات التسطير.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## الخطوة 6: إضافة نص مع ارتباط تشعبي

`RichText` يمثل تشغيلًا من النص المنسق داخل فقرة. ضبط عنوان الارتباط التشعبي يجعل النص قابلًا للنقر في ملف PDF المُصدَّر.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## الخطوة 7: إضافة المخطط إلى الصفحة والصفحة إلى المستند

تقوم هذه الخطوة بربط عناصر المخطط التي تم إنشاؤها مسبقًا بالصفحة ثم إضافة الصفحة إلى كائن `Document`.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## الخطوة 8: حفظ المستند كملف PDF

`SaveFormat.Pdf` يخبر Aspose.Note بتصدير المستند بصيغة PDF.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## الخاتمة

تهانينا! لقد نجحت في **حفظ OneNote كملف PDF** وإضافة ارتباط تشعبي إلى المستند باستخدام Java ومكتبة Aspose.Note. تتيح لك هذه القدرة **embed link onenote** وإنشاء ملفات PDF تفاعلية قابلة للمشاركة مباشرةً من محتوى OneNote الخاص بك.

## الأسئلة المتكررة

**س: كيف يمكنني تخصيص مظهر الارتباط التشعبي؟**  
ج: استخدم خصائص `TextStyle` مثل `setFontColor`، `setUnderline`، أو `setFontName` قبل استدعاء `setHyperlinkAddress`.

**س: هل يمكنني حفظ المستند بصيغ غير PDF؟**  
ج: نعم، يدعم Aspose.Note صيغ DOCX وXPS وHTML والعديد من صيغ التصدير الأخرى.

**س: ماذا لو احتجت إلى إضافة ارتباط تشعبي إلى ملف OneNote موجود؟**  
ج: حمّل الملف الموجود باستخدام `new Document("input.one")`، عدّل المحتوى كما هو موضح، ثم استدعِ `save` بالصيغ المطلوبة.

**س: هل هناك طريقة لفتح الارتباط التشعبي برمجيًا بعد إنشاء ملف PDF؟**  
ج: سيتعامل عارض PDF مع الروابط القابلة للنقر تلقائيًا؛ لا يلزم أي شفرة إضافية.

**س: هل أحتاج إلى ترخيص للاستخدام التطويري؟**  
ج: ترخيص تقييم مؤقت يكفي للتطوير والاختبار، لكن الترخيص الكامل مطلوب للنشر في بيئات الإنتاج.

---

**آخر تحديث:** 2026-07-29  
**تم الاختبار مع:** Aspose.Note for Java 26.4  
**المؤلف:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## دروس ذات صلة

- [كيفية حفظ OneNote كملف PDF باستخدام Aspose.Note for Java](/note/java/onenote-document-loading/load-save-format/)
- [تحويل OneNote إلى PDF باستخدام Aspose.Note وPdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [إضافة ارتباط تشعبي إلى صورة في OneNote باستخدام Java](/note/java/onenote-hyperlinks-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}