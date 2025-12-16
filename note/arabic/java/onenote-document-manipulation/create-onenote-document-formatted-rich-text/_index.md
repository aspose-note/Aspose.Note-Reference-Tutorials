---
date: 2025-12-09
description: تعلم كيفية حفظ OneNote كملف PDF بنص غني منسق في Java باستخدام Aspose.Note
  for Java. اتبع دليلنا خطوة بخطوة لأتمتة المستندات بسلاسة.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: حفظ OneNote كملف PDF بنص غني منسق في Java
url: /ar/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ OneNote كملف PDF مع نص غني منسق في Java

## مقدمة

إذا كنت بحاجة إلى **حفظ OneNote كملف PDF** مع الحفاظ على تنسيق النص الغني، فأنت في المكان الصحيح. في هذا البرنامج التعليمي سنستعرض إنشاء مستند OneNote، وتطبيق أنماط مخصصة، وتصديره مباشرةً إلى PDF باستخدام Aspose.Note for Java. في النهاية ستحصل على قطعة كود قابلة لإعادة الاستخدام يمكنك إدراجها في أي مشروع Java لأتمتة تحويلات OneNote إلى PDF بشكل احترافي.

## إجابات سريعة
- **ما الذي يدرسه هذا البرنامج التعليمي؟** كيفية إنشاء مستند OneNote بنص منسق وحفظه كملف PDF.  
- **ما المكتبة المطلوبة؟** Aspose.Note for Java (قابلة للتنزيل من الموقع الرسمي).  
- **هل أحتاج إلى ترخيص؟** الترخيص المؤقت يعمل للاختبار؛ الترخيص الكامل مطلوب للإنتاج.  
- **ما بيئة التطوير المتكاملة التي يمكنني استخدامها؟** أي IDE للـ Java — IntelliJ IDEA أو Eclipse أو NetBeans.  
- **هل يمكنني تغيير تنسيق الإخراج؟** نعم، Aspose.Note يدعم PDF وHTML وPNG وغيرها.

## ما هو “حفظ OneNote كملف PDF”؟
حفظ OneNote كملف PDF يعني تحويل بنية صفحة OneNote — بما في ذلك النصوص والصور والتنسيق — إلى ملف PDF ثابت يمكن عرضه على أي منصة دون الحاجة إلى OneNote.

## لماذا تنسيق النص الغني في Java؟
تطبيق تنسيق النص الغني (الخطوط، الألوان، الأنماط) مباشرةً في Java يتيح لك إنشاء مستندات تبدو احترافية وتطابق إرشادات علامتك التجارية دون تعديل يدوي.

## المتطلبات المسبقة

1. **Java Development Kit (JDK)** – أي نسخة حديثة (8 أو أعلى).  
2. **Aspose.Note for Java JAR** – قم بتنزيله من [رابط التحميل](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA أو Eclipse أو أي محرر تفضله.  

## استيراد الحزم

أول، تحتاج إلى استيراد الحزم الضرورية إلى مشروع Java الخاص بك. أضف عبارات الاستيراد التالية في بداية ملف Java الخاص بك:

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

## الخطوة 1: إعداد المستند والصفحة

لنبدأ بتهيئة كائنات `Document` و `Page`:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## الخطوة 2: إنشاء عنوان مع تنسيق

الآن، لنقم بإنشاء عنوان بنص منسق:

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

## الخطوة 3: إنشاء نص غني مع تنسيق

بعد ذلك، لنقم بإنشاء نص غني مع أنماط تنسيق مختلفة:

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

## الخطوة 4: إضافة العناصر إلى الصفحة والمستند

الآن، لنضيف العنوان والنص الغني إلى الصفحة وعناصر المخطط:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## الخطوة 5: حفظ المستند

أخيرًا، احفظ مستند OneNote الذي تم إنشاؤه كملف PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **الملف غير موجود** | تحقق من أن `dataDir` يشير إلى مجلد موجود وأن لديك أذونات كتابة. |
| **الخطوط مفقودة** | تأكد من تثبيت الخطوط التي تشير إليها (مثل *Calibri*) على الجهاز المضيف. |
| **الترخيص غير مُطبق** | حمّل ترخيص Aspose الخاص بك قبل إنشاء `Document` لتجنب علامات مائية للتقييم. |

## الأسئلة المتكررة

**س: هل يمكنني تخصيص أنماط الخط أكثر؟**  
ج: نعم، يمكنك تعديل خصائص إضافية مثل التسطير، والضرب عبر النص، ومحاذاة النص عبر فئات `TextStyle` و `ParagraphStyle`.

**س: هل Aspose.Note for Java متوافق مع جميع بيئات تطوير Java؟**  
ج: بالتأكيد. طالما أن الـ IDE يدعم تطوير Java القياسي، يمكنك إضافة ملف JAR الخاص بـ Aspose.Note إلى مسار الفئة للمشروع.

**س: هل يمكنني دمج هذه الوظيفة في تطبيقات الويب؟**  
ج: نعم، يعمل نفس الكود في تطبيقات تعتمد على الـ servlet أو Spring Boot، مما يتيح توليد OneNote إلى PDF ديناميكي على جانب الخادم.

**س: هل هناك متطلبات ترخيص لاستخدام Aspose.Note for Java؟**  
ج: يلزم الحصول على ترخيص تجاري للاستخدام في الإنتاج. يتوفر ترخيص مؤقت للتقييم والاختبار.

**س: هل يدعم Aspose.Note for Java صيغ مستندات أخرى غير OneNote؟**  
ج: يدعم PDF وHTML وPNG وJPEG والعديد من صيغ التصدير الأخرى، مما يمنحك مرونة تحويل صفحات OneNote إلى الصيغة التي تحتاجها.

## الخلاصة

في هذا الدليل، أظهرنا كيفية **حفظ OneNote كملف PDF** مع تطبيق تنسيق النص الغني باستخدام Aspose.Note for Java. باتباع التعليمات خطوة بخطوة يمكنك أتمتة إنشاء مستندات OneNote مصقولة وتحويلها إلى PDF في أي حل مبني على Java.

---

**آخر تحديث:** 2025-12-09  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}