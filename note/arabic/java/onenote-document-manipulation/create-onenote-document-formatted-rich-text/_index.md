---
title: إنشاء مستند OneNote بنص منسق منسق في Java
linktitle: إنشاء مستند OneNote بنص منسق منسق في Java
second_title: Aspose.Note جافا API
description: تعرف على كيفية إنشاء مستندات OneNote منسقة بشكل غني برمجياً في Java باستخدام Aspose.Note لـ Java. اتبع دليلنا خطوة بخطوة لأتمتة المستندات بسلاسة.
weight: 11
url: /ar/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء مستند OneNote بنص منسق منسق في Java

## مقدمة

يمكن أن يكون إنشاء مستندات OneNote منسقة بشكل غني برمجياً أداة قوية للمطورين الذين يتطلعون إلى أتمتة مهام إنشاء المستندات في تطبيقات Java. يوفر Aspose.Note for Java مجموعة شاملة من الميزات والوظائف لتحقيق ذلك بسلاسة. في هذا البرنامج التعليمي، سنرشدك خلال عملية إنشاء مستند OneNote بنص منسق منسق باستخدام Aspose.Note لـ Java.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من إعداد المتطلبات الأساسية التالية:

1. Java Development Kit (JDK): تأكد من تثبيت JDK على نظامك.
2.  Aspose.Note لـ Java JAR: قم بتنزيل ملف Aspose.Note لـ Java JAR وتضمينه في مشروعك. يمكنك الحصول عليه من[رابط التحميل](https://releases.aspose.com/note/java/).
3. بيئة التطوير المتكاملة (IDE): استخدم IDE المفضل لديك مثل IntelliJ IDEA أو Eclipse.

## حزم الاستيراد

أولاً، تحتاج إلى استيراد الحزم اللازمة لمشروع Java الخاص بك. أضف عبارات الاستيراد التالية إلى بداية ملف Java الخاص بك:

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

لنبدأ بتهيئة كائنات المستند والصفحة:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## الخطوة 2: إنشاء عنوان بالتنسيق

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

## الخطوة 3: إنشاء نص منسق بالتنسيق

بعد ذلك، لنقم بإنشاء نص منسق باستخدام أنماط تنسيق مختلفة:

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

## الخطوة 4: إضافة عناصر إلى الصفحة والمستند

الآن، دعونا نضيف العنوان والنص المنسق إلى عناصر الصفحة والمخطط التفصيلي:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## الخطوة 5: حفظ المستند

وأخيرًا، احفظ مستند OneNote الذي تم إنشاؤه:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية إنشاء مستند OneNote بنص منسق منسق في Java باستخدام Aspose.Note لـ Java. باتباع هذه الإرشادات خطوة بخطوة، يمكنك بسهولة إنشاء مستندات OneNote مخصصة برمجيًا، مما يعزز قدرات أتمتة المستندات لديك.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص أنماط الخطوط بشكل أكبر؟

ج1: نعم، يمكنك ضبط خصائص مختلفة مثل لون الخط وحجمه ونمطه وما إلى ذلك، لتناسب متطلباتك.

### س2: هل Aspose.Note for Java متوافق مع كافة بيئات Java IDE؟

ج2: نعم، يمكنك استخدام Aspose.Note لـ Java مع أي Java IDE يدعم تطوير Java.

### س3: هل يمكنني دمج هذه الوظيفة في تطبيقات الويب؟

ج3: بالتأكيد، يمكن دمج Aspose.Note for Java بسلاسة في تطبيقات الويب لإنشاء مستندات ديناميكية.

### س4: هل هناك أي متطلبات ترخيص لاستخدام Aspose.Note لـ Java؟

ج4: نعم، أنت بحاجة إلى الحصول على ترخيص لاستخدام Aspose.Note لـ Java في المشاريع التجارية. ومع ذلك، يمكنك أيضًا استخدام ترخيص مؤقت لأغراض الاختبار.

### س5: هل يدعم Aspose.Note for Java تنسيقات المستندات الأخرى إلى جانب OneNote؟

ج5: نعم، يدعم Aspose.Note for Java مجموعة متنوعة من تنسيقات المستندات، بما في ذلك تنسيقات PDF وHTML وتنسيقات الصور.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
