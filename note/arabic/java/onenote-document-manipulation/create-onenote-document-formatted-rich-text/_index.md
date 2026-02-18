---
date: 2026-02-18
description: تعلم كيفية إنشاء مستند OneNote، تنسيق النص الغني، وحفظه كملف PDF في Java
  باستخدام Aspose.Note. دليل خطوة بخطوة لأتمتة سلسة.
linktitle: Create OneNote document and save as PDF in Java
second_title: Aspose.Note Java API
title: إنشاء مستند OneNote وحفظه كملف PDF في Java
url: /ar/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

.

Translate.

Now "Last Updated:" keep date.

"Tested With:" keep version.

"Author:" keep Aspose.

Now close shortcodes.

Make sure to keep all markdown formatting.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء مستند OneNote وحفظه كملف PDF في Java

## المقدمة

إذا كنت بحاجة إلى **إنشاء مستند OneNote** و**حفظ OneNote كملف PDF** مع الحفاظ على تنسيق النص الغني، فأنت في المكان الصحيح. في هذا الدليل سنستعرض خطوات إنشاء مستند OneNote، وتطبيق الأنماط المخصصة، وتصديره مباشرةً إلى PDF باستخدام Aspose.Note for Java. في النهاية ستحصل على مقتطف قابل لإعادة الاستخدام يمكنك إدراجه في أي مشروع Java لأتمتة تحويلات OneNote إلى PDF بشكل احترافي.

## إجابات سريعة
- **ماذا يعلّمك هذا الدليل؟** كيفية إنشاء مستند OneNote بنص منسق وحفظه كملف PDF.  
- **ما المكتبة المطلوبة؟** Aspose.Note for Java (يمكن تحميلها من الموقع الرسمي).  
- **هل أحتاج إلى ترخيص؟** ترخيص مؤقت يعمل للاختبار؛ الترخيص الكامل مطلوب للإنتاج.  
- **ما بيئة التطوير المتكاملة (IDE) التي يمكنني استخدامها؟** أي بيئة Java—IntelliJ IDEA، Eclipse، أو NetBeans.  
- **هل يمكنني تغيير تنسيق الإخراج؟** نعم، يدعم Aspose.Note صيغ PDF، HTML، PNG، وأكثر.

## ما هو “حفظ OneNote كملف PDF”؟
يعني حفظ OneNote كملف PDF تحويل بنية صفحة OneNote—بما فيها النصوص، الصور، والتنسيق—إلى ملف PDF ثابت يمكن عرضه على أي منصة دون الحاجة إلى OneNote.

## لماذا تنسيق النص الغني في Java؟
يسمح تطبيق **تنسيق النص الغني** مباشرةً في Java بإنشاء مستندات تبدو احترافية وتطابق إرشادات العلامة التجارية الخاصة بك دون الحاجة إلى تحرير يدوي.

## المتطلبات المسبقة

1. **Java Development Kit (JDK)** – أي نسخة حديثة (8 أو أعلى).  
2. **Aspose.Note for Java JAR** – حمّله من [رابط التحميل](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA، Eclipse، أو أي محرر تفضله.  

## استيراد الحزم

قبل أن نبدأ، استورد الفئات الضرورية إلى ملف Java الخاص بك:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## كيفية إنشاء مستند OneNote – دليل خطوة بخطوة

### الخطوة 1: إعداد المستند والصفحة

تهيئة كائنات `Document` و `Page` التي ستحمل جميع المحتويات:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### الخطوة 2: إنشاء العنوان مع التنسيق

أضف عنصر عنوان وطبق **set paragraph style** للتحكم في مظهره:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

### الخطوة 3: إنشاء نص غني مع التنسيق

هنا نبني محتوى نص غني باستخدام عدة كائنات `TextStyle` لتوضيح **تنسيق النص الغني**:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

### الخطوة 4: إضافة العناصر إلى الصفحة والمستند

اجمع العنوان والنص الغني في هيكل الصفحة:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### الخطوة 5: حفظ المستند – تصدير OneNote إلى PDF

أخيرًا، صدّر مستند OneNote كملف PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|---------|------|
| **الملف غير موجود** | تحقق من أن `dataDir` يشير إلى مجلد موجود وأن لديك أذونات كتابة. |
| **الخطوط مفقودة** | تأكد من تثبيت الخطوط التي تشير إليها (مثل *Calibri*) على الجهاز المضيف. |
| **الترخيص غير مفعّل** | حمّل ترخيص Aspose قبل إنشاء الـ `Document` لتجنب علامات مائية التقييم. |

## الأسئلة المتكررة

**س: هل يمكنني تخصيص أنماط الخط أكثر؟**  
ج: نعم، يمكنك تعديل خصائص إضافية مثل التسطير، الخط المشطوب، ومحاذاة النص عبر فئات `TextStyle` و `ParagraphStyle`.

**س: هل Aspose.Note for Java متوافق مع جميع بيئات تطوير Java؟**  
ج: بالطبع. طالما أن بيئة التطوير تدعم تطوير Java القياسي، يمكنك إضافة ملف Aspose.Note JAR إلى مسار الفئة (classpath) الخاص بالمشروع.

**س: هل يمكنني دمج هذه الوظيفة في تطبيقات الويب؟**  
ج: نعم، يعمل نفس الكود في تطبيقات تعتمد على الـ servlet أو Spring Boot، مما يتيح إنشاء OneNote إلى PDF بشكل ديناميكي على جانب الخادم.

**س: هل هناك متطلبات ترخيص لاستخدام Aspose.Note for Java؟**  
ج: يتطلب الترخيص التجاري للاستخدام في الإنتاج. يتوفر ترخيص مؤقت للتقييم والاختبار.

**س: هل يدعم Aspose.Note for Java صيغ مستندات أخرى غير OneNote؟**  
ج: يدعم صيغ PDF، HTML، PNG، JPEG، والعديد من صيغ التصدير الأخرى، مما يمنحك مرونة تحويل صفحات OneNote إلى الصيغة التي تحتاجها.

## الخلاصة

في هذا الدليل أظهرنا كيفية **إنشاء مستند OneNote**، وتطبيق **تنسيق النص الغني**، و**حفظ OneNote كملف PDF** باستخدام Aspose.Note for Java. باتباع التعليمات خطوة بخطوة يمكنك أتمتة إنشاء مستندات OneNote مصقولة وتحويلها إلى PDF في أي حل مبني على Java.

---

**آخر تحديث:** 2026-02-18  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}