---
date: 2026-10-26
description: تعلم كيفية إضافة checkboxes OneNote أثناء إنشاء meeting notes template
  باستخدام Aspose.Note for Java، وتخصيص font style في OneNote بسهولة.
keywords:
- add checkboxes onenote
- generate meeting notes template
- customize font style onenote
- create outline onenote
lastmod: 2026-10-26
linktitle: إنشاء meeting notes template باستخدام Aspose.Note for Java – إنشاء مخطط
  في OneNote
og_description: تعلم كيفية إضافة checkboxes OneNote أثناء إنشاء meeting notes template
  باستخدام Aspose.Note for Java، وتخصيص font style في OneNote بسهولة.
og_image_alt: 'Developer guide: add checkboxes onenote and generate meeting notes
  template using Aspose.Note for Java'
og_title: إضافة checkboxes OneNote وإنشاء notes template في Java
schemas:
- author: Aspose
  dateModified: '2026-10-26'
  description: Learn how to add checkboxes onenote while generating a meeting notes
    template with Aspose.Note for Java, and customize font style onenote easily.
  headline: Add checkboxes onenote and create notes template in Java
  type: TechArticle
- questions:
  - answer: You can create a bulleted list and manually mark items, but using `NoteCheckBox`
      provides interactive checkboxes that sync with OneNote’s UI.
    question: How do I add a checklist to OneNote without using checkboxes?
  - answer: Absolutely. Just change the date formatting or pass a custom title string
      to reuse the same structure for each week.
    question: Can I use this template to create a meeting agenda template for weekly
      repeats?
  - answer: Define `ParagraphStyle` objects with your corporate font name, size, and
      color, then apply them to each `RichText` element as shown in Step 1.
    question: What is the best way to customize font style onenote for branding?
  - answer: Yes. After saving the OneNote file, you can load it with Aspose.Note and
      export to PDF using `Document.save("output.pdf", SaveFormat.Pdf)`.
    question: Does Aspose.Note support exporting the outline to PDF?
  - answer: You can set the checkbox state by adding a `NoteCheckBox` tag with the
      `Checked` property set to `true`.
    question: Is there a way to programmatically mark a checkbox as completed?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote
- Aspose.Note
- Java
- meeting notes template
- checkboxes
title: إضافة checkboxes OneNote وإنشاء notes template في Java
url: /ar/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة مربعات اختيار OneNote وإنشاء قالب ملاحظات في Java

## مقدمة
في بيئات التعاون الحديثة، **add checkboxes onenote** بسرعة وتوليد قالب ملاحظات اجتماع مصقول دون تنسيق يدوي. تمنحك Aspose.Note for Java تحكمًا كاملاً في عناوين الصفحات، المخططات الهرمية، تنسيق الخطوط، ومربعات الاختيار التفاعلية، مما يتيح لك إنتاج جدول أعمال قابل لإعادة الاستخدام في ثوانٍ. يوجهك هذا الدليل خلال كل خطوة — من استيراد الفئات المطلوبة إلى حفظ ملف OneNote النهائي — حتى تتمكن من التركيز على محتوى الاجتماع، وليس على العمل المرهق للواجهة.

## إجابات سريعة
- **ما معنى “add checkboxes onenote”?** يعني ذلك إدراج مربعات اختيار تفاعلية برمجيًا في مخطط OneNote، تمامًا كما تفعل الواجهة.  
- **أي مكتبة تساعد في ذلك؟** توفر Aspose.Note for Java الـ API الكامل.  
- **هل يمكنني إضافة مربعات اختيار إلى المخطط؟** نعم — استخدم `NoteCheckBox.createBlueCheckBox()` أو ألوان أخرى.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للاستخدام في الإنتاج.  
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها.

## ما هو add checkboxes onenote؟
إضافة مربعات اختيار onenote تُدرج علامة `NoteCheckBox` داخل عنصر `RichText`، محوّلة سطر نص عادي إلى مربع اختيار تفاعلي يمكن للمستخدمين تحديده أو إلغاء تحديده مباشرة داخل واجهة OneNote، مع الحفاظ على حالة المربع عبر الأجهزة وضمان التناسق.

## لماذا تستخدم Aspose.Note لإنشاء قالب ملاحظات اجتماع؟
تعالج Aspose.Note **أكثر من 50 تنسيقًا للإدخال والإخراج** ويمكنها التعامل مع صفحات تحتوي على **حتى 500 سطر** دون تحميل المستند بالكامل في الذاكرة، مما يوفّر توليدًا سريعًا وفعّالًا للذاكرة لأجندات كبيرة. كما توفر API سلسًا لتنسيق الخطوط، وتدعم أحرف Unicode، وتتكامل بسلاسة مع مكتبات Aspose الأخرى، مما يجعلها مثالية لتدفقات عمل توثيق الاجتماعات على مستوى المؤسسة.

## المتطلبات المسبقة
- فهم أساسي لبرمجة Java.  
- مكتبة Aspose.Note for Java مثبتة. يمكنك **download Aspose.Note for Java** من صفحة الإصدار الرسمية: [Aspose.Note for Java release page](https://releases.aspose.com/note/java/).  
- بيئة تطوير متكاملة (IDE) مثل Eclipse أو IntelliJ IDEA.  

## استيراد الحزم
الفئات `Document`، `Outline`، `ParagraphStyle`، `RichText`، و`NoteCheckBox` هي اللبنات الأساسية.  

`Document` يمثل ملف OneNote بالكامل في الذاكرة، مما يسمح بإضافة أو تعديل الصفحات والمحتوى.  
`Outline` يُنمذج هيكل القائمة الهرمية المعروض في OneNote، مما يتيح نقاطًا نقطية متداخلة وترقيمًا.  
`ParagraphStyle` يعرّف سمات الخط والفقرة القابلة لإعادة الاستخدام التي يمكن تطبيقها على عناصر `RichText` متعددة.  
`RichText` يحمل محتوى النص الفعلي للفقرة ويمكن أن يحتوي على علامات مثل `NoteCheckBox`.  
`NoteCheckBox` ينشئ علامة مربع اختيار تفاعلية يمكن إرفاقها بفقرة `RichText`.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## الخطوة 1: إنشاء بنية المستند
أولاً، أنشئ كائن `Document`، عيّن عنوان صفحة، وعرّف كائنين `ParagraphStyle` قابلين لإعادة الاستخدام — أحدهما للعناوين والآخر للنص الأساسي.  

تسمح لك كائنات `ParagraphStyle` بتطبيق نفس عائلة الخط، الحجم، واللون على فقرات متعددة دون تكرار الشيفرة.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*ما فعلنا:*  
- تم تعريف `headerStyle` للعناوين و`bodyStyle` للنص العادي.  
- تم إنشاء `Document` وإضافة `Title` يتضمن تاريخ اليوم، مما يمنح الصفحة عنوانًا واضحًا.

## الخطوة 2: تحديد النقاط المهمة
بعد ذلك، أضف كائن `Outline` إلى الصفحة واملأه بأقسام مثل “Agenda”، “Discussion Items”، و“Action Items”.  

كائن `Outline` يمثل القائمة الهرمية التي تراها في OneNote. باستخدام `createListNumberingStyle` نولد قائمة مرقمة يمكن إعادة تشغيلها لكل قسم جديد.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*لماذا هذا مهم:*  
- تعكس هيكلية المخطط البنية اليدوية التي كنت ستكتبها في OneNote، مما يضمن التناسق عبر جميع الصفحات المُولدة.  
- تحافظ أنماط الترقيم على ترتيب كل قسم من جدول الأعمال بشكل أنيق وسهل المتابعة.

## الخطوة 3: تمييز عناصر الإجراء (كيفية إضافة مربعات الاختيار)
تحتاج عناصر الإجراء إلى إشارة بصرية. من خلال إرفاق علامة `NoteCheckBox` بكل عنصر `RichText`، يمكنك تمكين **add checkboxes onenote** مباشرة داخل المخطط.  

`NoteCheckBox.createBlueCheckBox()` ينشئ مربع اختيار أزرق؛ تتوفر ألوان أخرى للعلامة التجارية.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*نصيحة احترافية:* استخدم `NoteCheckBox.createBlueCheckBox()` لمربع اختيار أزرق؛ تتوفر ألوان أخرى إذا كنت تحتاج إلى نمط بصري مختلف.

## الخطوة 4: تخصيص نمط الخط في OneNote
للحفاظ على ملاحظات الاجتماع متوافقة مع هوية العلامة التجارية، طبّق كائنات `ParagraphStyle` التي عرّفتها مسبقًا على كل عنصر `RichText`.  

ضبط خصائص `FontName`، `FontSize`، و`FontColor` يضمن أن الصفحة المُولدة تتطابق مع دليل أسلوب شركتك.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## الخطوة 5: حفظ المستند
أخيرًا، اكتب ملف OneNote إلى القرص. يمكن فتح الملف مباشرة في تطبيق OneNote لسطح المكتب، ويمكنك أيضًا تحويله إلى PDF لاحقًا إذا لزم الأمر.

*الإجابة المباشرة:* استدعِ `document.save("MeetingTemplate.one")` — يكتب الـ API ملف OneNote متوافق بالكامل يفتح فورًا في عميل OneNote.

## المشكلات الشائعة والحلول
| المشكلة | الحل |
|-------|----------|
| **عدم ظهور مربعات الاختيار** | تأكد من أنك استدعيت `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` بعد ضبط نمط الفقرة. |
| **خطوط مختلفة في OneNote** | تحقق من أن اسم الخط (مثل “Calibri”) مثبت على الجهاز الذي يفتح OneNote الملف. |
| **عدم إزاحة المخطط** | اضبط `setVerticalOffset` و`setHorizontalOffset` على كائن `Outline`. |
| **إعادة ترقيم غير متوقعة** | استخدم `restartFlag` بشكل صحيح؛ عيّنه إلى `true` فقط للقائمة الأولى في قسم جديد. |

## الأسئلة المتكررة
### كيف أضيف مربعات اختيار OneNote؟
حمّل عنصر `RichText`، ثم استدعِ `richText.getTags().add(NoteCheckBox.createBlueCheckBox())`. تحول العلامة السطر إلى مربع اختيار تفاعلي يمكن للمستخدمين تحديده داخل OneNote.

### هل يمكنني تخصيص أنماط الخط في ملاحظات الاجتماع؟
نعم. أنشئ كائنات `ParagraphStyle` بالخط، الحجم، واللون المطلوبين، ثم عيّنها لكل عنصر `RichText` كما هو موضح في الخطوة 1.

### هل Aspose.Note متوافق مع مكتبات Java الأخرى؟
يعمل Aspose.Note جنبًا إلى جنب مع منتجات Aspose الأخرى (PDF, Cells, Slides) ومكتبات Java القياسية، مما يتيح لك ربط العمليات مثل تحويل ملف OneNote المُولد إلى PDF.

### كيف يمكنني إضافة أقسام إضافية إلى ملاحظات الاجتماع؟
استخدم النمط نفسه: أنشئ عقدة `Outline` جديدة، طبّق `ParagraphStyle`، وأضف مربعات اختيار إذا لزم الأمر. الـ API قابل للتكرار لأي عدد من الأقسام.

### هل هناك اعتبارات ترخيص لـ Aspose.Note؟
راجع [Aspose.Note documentation](https://reference.aspose.com/note/java/) للحصول على تفاصيل الترخيص الكاملة. النسخة التجريبية مجانية للتطوير؛ يلزم ترخيص تجاري للنشر في بيئات الإنتاج.

### هل هناك نسخة تجريبية متاحة لـ Aspose.Note؟
نعم، يمكنك الوصول إلى **صفحة تحميل التجربة المجانية لـ Aspose.Note**: [Aspose.Note trial download page](https://releases.aspose.com/).

## الأسئلة الشائعة
**س: كيف أضيف قائمة مراجعة إلى OneNote دون استخدام مربعات الاختيار؟**  
ج: يمكنك إنشاء قائمة نقطية وتحديد العناصر يدويًا، لكن استخدام `NoteCheckBox` يوفر مربعات اختيار تفاعلية تتزامن مع واجهة OneNote.

**س: هل يمكنني استخدام هذا القالب لإنشاء قالب جدول أعمال للاجتماعات المتكررة أسبوعيًا؟**  
ج: بالتأكيد. فقط غيّر تنسيق التاريخ أو مرّر سلسلة عنوان مخصصة لإعادة استخدام نفس البنية كل أسبوع.

**س: ما هي أفضل طريقة لتخصيص نمط الخط في OneNote للعلامة التجارية؟**  
ج: عرّف كائنات `ParagraphStyle` باسم الخط، الحجم، واللون الخاصين بشركتك، ثم طبّقها على كل عنصر `RichText` كما هو موضح في الخطوة 1.

**س: هل يدعم Aspose.Note تصدير المخطط إلى PDF؟**  
ج: نعم. بعد حفظ ملف OneNote، يمكنك تحميله باستخدام Aspose.Note وتصديره إلى PDF عبر `Document.save("output.pdf", SaveFormat.Pdf)`.

**س: هل هناك طريقة لتمييز مربع الاختيار كمكتمل برمجيًا؟**  
ج: يمكنك ضبط حالة المربع بإضافة علامة `NoteCheckBox` مع الخاصية `Checked` مضبوطة على `true`.

---

**Last Updated:** 2026-10-26  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (latest at time of writing)  
**المؤلف:** Aspose

## دروس ذات صلة

- [إضافة علامات إلى OneNote – إنشاء مستند OneNote مع علامات باستخدام Aspose.Note](/note/java/onenote-tag-operations/)
- [كيفية تخصيص أنماط OneNote باستخدام Aspose.Note for Java](/note/java/onenote-styles/)
- [إنشاء مستند OneNote Java – درس Aspose Note Java](/note/java/onenote-document-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}