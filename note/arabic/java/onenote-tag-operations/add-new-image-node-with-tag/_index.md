---
date: 2026-08-13
description: تعلم كيفية إدراج صورة في OneNote، إضافة علامة إلى الصورة، وحفظ OneNote
  كملف PDF باستخدام Aspose.Note للـ Java.
keywords:
- insert image into onenote
- save onenote as pdf
- java add tag to image
lastmod: 2026-08-13
linktitle: إضافة علامة إلى الصورة في OneNote – Aspose.Note
og_description: إدراج صورة في OneNote، إضافة علامة نجمة صفراء إلى الصورة، وتصدير الدفتر
  كملف PDF باستخدام Aspose.Note للـ Java. اتبع الدليل خطوة بخطوة للتنفيذ السريع.
og_image_alt: Guide showing how to insert an image and tag it in OneNote using Aspose.Note
  for Java
og_title: إدراج صورة في OneNote وإضافة علامة – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to insert image into OneNote, add a tag to the image, and
    save OneNote as PDF using Aspose.Note for Java.
  headline: Insert image into OneNote and add tag with Aspose.Note – Java
  type: TechArticle
- description: Learn how to insert image into OneNote, add a tag to the image, and
    save OneNote as PDF using Aspose.Note for Java.
  name: Insert image into OneNote and add tag with Aspose.Note – Java
  steps:
  - name: create document object
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      OneNote notebook in memory. After instantiation, all subsequent operations flow
      through this object.
  - name: initialize page class object
    text: The `Page` class defines a single page inside the notebook. You can set
      page properties such as title and size before adding content.
  - name: initialize outline class object
    text: The `Outline` class groups related content blocks on a page. Outlines are
      containers for `OutlineElement` objects.
  - name: initialize outline element class object
    text: The `OutlineElement` class represents an individual block inside an outline,
      such as a paragraph, image, or table.
  - name: load and insert image
    text: '*(This step demonstrates **insert image into OneNote**)* The `Image` class
      encapsulates image data to be placed on a OneNote page.'
  - name: add note tag to image
    text: '*(Here we answer **how to add image tag**)* The `NoteTag` class defines
      a visual tag that can be attached to page elements.'
  - name: add outline element node
    text: Attach the image (now tagged) to the outline element so it appears in the
      correct order on the page.
  - name: add outline node
    text: Insert the outline into the page’s collection of outlines.
  - name: add page node
    text: Add the fully built page to the document’s page collection.
  type: HowTo
- questions:
  - answer: You can find the documentation at the **[Aspose.Note Java API reference](https://reference.aspose.com/note/java/)**.
    question: Where can I find Aspose.Note documentation?
  - answer: You can download it from the releases page **[Aspose.Note Java release
      page](https://releases.aspose.com/note/java/)**.
    question: How do I download Aspose.Note for Java?
  - answer: Yes, you can access the free trial at the **[Aspose free trial page](https://releases.aspose.com/)**.
    question: Is there a free trial available?
  - answer: Visit the community forum **[Aspose.Note community forum](https://forum.aspose.com/c/note/28)**
      for support.
    question: Where can I get support for Aspose.Note?
  - answer: If required, you can obtain a temporary license from the **[temporary
      license request page](https://purchase.aspose.com/temporary-license/)**.
    question: Do I need a temporary license?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote automation
- aspose.note java
- insert image into onenote
- add tag to image
- export onenote pdf
title: إدراج صورة في OneNote وإضافة علامة باستخدام Aspose.Note – Java
url: /ar/java/onenote-tag-operations/add-new-image-node-with-tag/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدراج صورة في OneNote وإضافة علامة باستخدام Aspose.Note – Java

## مقدمة
إذا كنت بحاجة إلى **إدراج صورة في OneNote** أثناء العمل بـ Java، فإن Aspose.Note يجعل العملية بأكملها بسيطة. في هذا البرنامج التعليمي سنستعرض كيفية إدراج صورة في صفحة OneNote، وتطبيق علامة نجمة صفراء على تلك الصورة، وأخيرًا **حفظ OneNote كملف PDF**. في النهاية ستعرف بالضبط كيفية إضافة علامة إلى الصورة، وإدراج صورة في OneNote، وتحويل OneNote إلى PDF — كل ذلك ببضع أسطر من الشيفرة.

## إجابات سريعة
- **ماذا يعني “إضافة علامة إلى صورة”?** إنه يرفق علامة ملاحظة بصرية (مثل نجمة صفراء) بعقدة صورة في صفحة OneNote.  
- **ما المكتبة التي تتعامل مع ذلك؟** Aspose.Note for Java.  
- **هل أحتاج إلى ترخيص للاختبار؟** إصدار تجريبي مجاني يعمل للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **هل يمكنني تصدير النتيجة كملف PDF؟** نعم – استخدم `doc.save(..., SaveFormat.Pdf)` لـ **حفظ OneNote كملف PDF**.  
- **كم من الوقت تستغرق العملية؟** عادةً أقل من 10 دقائق لسيناريو أساسي.

## ما هو “إضافة علامة إلى صورة” في OneNote؟
عنصر `NoteTag` هو كائن بيانات وصفية يضع علامة بصرية على صورة بأيقونة مثل نجمة أو علم. يظهر في واجهة OneNote ويمكن البحث عنه أو تصفيته، مما يسمح للمستخدمين بتحديد المواقع بسرعة للمرئيات الموسومة داخل دفاتر ملاحظات كبيرة.

## لماذا نضيف علامة إلى صورة في OneNote؟
توفر علامات الصور طريقة خفيفة لإضافة سياق دون تعديل الصورة نفسها. تُخزن العلامات كجزء من بنية الصفحة، مما يتيح عمليات بحث سريعة، وإشارات بصرية، وتصنيفًا، وهو مفيد بشكل خاص في الأبحاث، وتتبع المشاريع، أو دفاتر الملاحظات التعليمية.

- تنظيم المحتوى البصري دون تعديل الصورة نفسها.  
- تحديد الرسومات المهمة بسرعة باستخدام بحث العلامات في OneNote.  
- توفير سياق (مثل “مراجعة لاحقًا”، “مرجع مهم”) مباشرة على الصفحة.  

## المتطلبات المسبقة
قبل أن نبدأ، تأكد من وجود ما يلي:

1. Aspose.Note for Java: تأكد من تثبيت مكتبة Aspose.Note. إذا لم تكن مثبتة، يمكنك تنزيلها من **[صفحة تنزيل Aspose.Note for Java](https://releases.aspose.com/note/java/)**.  
2. بيئة تطوير Java: JDK (الإصدار 8 أو أحدث) يعمل، وIDE أو أداة بناء من اختيارك.  

الآن بعد أن تم استيفاء المتطلبات المسبقة، لننتقل إلى الخطوات التالية.

## استيراد الحزم
في مشروع Java الخاص بك، ابدأ باستيراد الحزم اللازمة:
الفئة `Document` تمثل دفتر OneNote في الذاكرة.  
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```

## كيف تقوم بإدراج صورة في OneNote؟
حمّل ملف الصورة المستهدف، أنشئ عقدة `Image`، وأضفها إلى مخطط الصفحة. يتطلب الإدراج ثلاث نداءات API فقط ويحافظ على دقة الصورة الأصلية. يعمل هذا النهج مع صيغ PNG، JPEG، BMP، وGIF دون تحويل إضافي.

### الخطوة 1: إنشاء كائن المستند
الفئة `Document` هي كائن المستوى الأعلى في Aspose.Note الذي يمثل دفتر OneNote في الذاكرة. بعد الإنشاء، تتدفق جميع العمليات اللاحقة عبر هذا الكائن.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```

### الخطوة 2: تهيئة كائن الفئة Page
الفئة `Page` تعرف صفحة واحدة داخل الدفتر. يمكنك ضبط خصائص الصفحة مثل العنوان والحجم قبل إضافة المحتوى.

```java
// initialize Page class object
Page page = new Page();
```

### الخطوة 3: تهيئة كائن الفئة Outline
الفئة `Outline` تجمع كتل المحتوى المرتبطة على صفحة. المخططات هي حاويات لكائنات `OutlineElement`.

```java
// initialize Outline class object
Outline outline = new Outline();
```

### الخطوة 4: تهيئة كائن الفئة OutlineElement
الفئة `OutlineElement` تمثل كتلة فردية داخل المخطط، مثل فقرة أو صورة أو جدول.

```java
// initialize OutlineElement class object
OutlineElement outlineElem = new OutlineElement();
```

## كيف تضيف علامة إلى صورة في OneNote؟
أنشئ كائن `NoteTag`، اضبط نوعه (مثلاً نجمة صفراء)، وأرفقه بعقدة `Image` التي تم إنشاؤها مسبقًا. تصبح العلامة جزءًا من بيانات تعريف الصورة وتُعرض تلقائيًا بواسطة OneNote.

لإرفاق علامة، أنشئ كائن `NoteTag`، اضبط خاصية `TagIcon` إلى الرمز المطلوب (على سبيل المثال `TagIcon.YellowStar`)، واربطه بعقدة `Image` باستخدام طريقة `addTag`. تصبح العلامة جزءًا من بيانات تعريف الصورة وتُعرض تلقائيًا بواسطة OneNote.

### الخطوة 5: تحميل وإدراج الصورة  
*(توضح هذه الخطوة **إدراج صورة في OneNote**)*  
الفئة `Image` تحيط ببيانات الصورة لتوضع على صفحة OneNote.  
```java
// load an image
Image image = new Image(dataDir + "Input.jpg");
// insert image in the document node
outlineElem.appendChildLast(image);
```

### الخطوة 6: إضافة علامة ملاحظة إلى الصورة  
*(هنا نجيب على **كيفية إضافة علامة إلى الصورة**)*  
الفئة `NoteTag` تعرف علامة بصرية يمكن إرفاقها بعناصر الصفحة.  
```java
// add a yellow star note tag to the image
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```

### الخطوة 7: إضافة عقدة عنصر المخطط
أرفق الصورة (الموسومة الآن) بعنصر المخطط بحيث تظهر بالترتيب الصحيح على الصفحة.

```java
// add outline element node
outline.appendChildLast(outlineElem);
```

### الخطوة 8: إضافة عقدة المخطط
أدرج المخطط في مجموعة المخططات الخاصة بالصفحة.

```java
// add outline node
page.appendChildLast(outline);
```

### الخطوة 9: إضافة عقدة الصفحة
أضف الصفحة المكتملة إلى مجموعة صفحات المستند.

```java
// add page node
doc.appendChildLast(page);
```

## كيف تحفظ OneNote كملف PDF؟
استدعِ طريقة `save` على كائن `Document`، مع تحديد `SaveFormat.Pdf`. يقوم Aspose.Note بتحويل جميع عناصر الصفحة — بما في ذلك الصور، العلامات، والمخططات — إلى تمثيل PDF دقيق دون الحاجة إلى تثبيت Microsoft OneNote.

تحدد تعداد `SaveFormat` صيغة الإخراج لحفظ المستند.  
```java
// save OneNote document as a PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```

تهانينا! لقد نجحت في **إضافة علامة إلى صورة**، وإدراج صورة في OneNote، وتصدير الدفتر إلى PDF باستخدام Aspose.Note for Java.

## المشكلات الشائعة والحلول
| المشكلة | الحل |
|-------|----------|
| **الصورة غير معروضة** | تحقق من أن المسار في `dataDir + "Input.jpg"` صحيح وأن الملف قابل للوصول. |
| **العلامة غير مرئية** | تأكد من أنك تستخدم نسخة OneNote تدعم علامات الملاحظات (معظم الإصدارات الحديثة تدعم ذلك). |
| **إخراج PDF فارغ** | تحقق من أن المستند يحتوي على صفحة/مخطط واحد على الأقل قبل استدعاء `save`. |

## الأسئلة المتكررة

**س: أين يمكنني العثور على وثائق Aspose.Note؟**  
ج: يمكنك العثور على الوثائق في **[مرجع Aspose.Note Java API](https://reference.aspose.com/note/java/)**.

**س: كيف يمكنني تنزيل Aspose.Note لـ Java؟**  
ج: يمكنك تنزيله من صفحة الإصدارات **[صفحة إصدار Aspose.Note Java](https://releases.aspose.com/note/java/)**.

**س: هل يتوفر نسخة تجريبية مجانية؟**  
ج: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية عبر **[صفحة التجربة المجانية من Aspose](https://releases.aspose.com/)**.

**س: أين يمكنني الحصول على الدعم لـ Aspose.Note؟**  
ج: قم بزيارة منتدى المجتمع **[منتدى Aspose.Note](https://forum.aspose.com/c/note/28)** للحصول على الدعم.

**س: هل أحتاج إلى ترخيص مؤقت؟**  
ج: إذا لزم الأمر، يمكنك الحصول على ترخيص مؤقت من **[صفحة طلب الترخيص المؤقت](https://purchase.aspose.com/temporary-license/)**.

## الخلاصة
إتقان Aspose.Note for Java يفتح إمكانيات مثيرة في معالجة مستندات OneNote. باتباعك لهذا البرنامج التعليمي، تعلمت **كيفية إضافة علامة إلى صورة**، **إدراج صورة في OneNote**، و**حفظ OneNote كملف PDF** — مهارات يمكنك تطبيقها على مجموعة واسعة من مشاريع الأتمتة. استمر في استكشاف وثائق Aspose.Note على **[وثائق Aspose.Note Java](https://reference.aspose.com/note/java/)** للحصول على ميزات وإمكانات متقدمة أكثر.

---

**آخر تحديث:** 2026-08-13  
**تم الاختبار مع:** Aspose.Note 24.11 for Java  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية إضافة صورة إلى OneNote باستخدام Java – إنشاء مستند وإدراج صورة](/note/java/onenote-hyperlinks-images/build-doc-insert-image/)
- [كيفية حفظ OneNote كملف PDF باستخدام Aspose.Note لـ Java](/note/java/onenote-document-loading/load-save-format/)
- [إدراج صف جدول Java - إضافة عقدة جدول مع علامة في OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}