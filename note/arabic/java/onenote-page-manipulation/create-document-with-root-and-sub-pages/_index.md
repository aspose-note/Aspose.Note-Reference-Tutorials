---
description: تعرّف على كيفية حفظ PDF من OneNote وإضافة صفحات فرعية في OneNote باستخدام
  Aspose.Note للغة Java. اتبع هذا الدليل خطوة بخطوة لتنظيم ملاحظاتك بكفاءة.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: كيفية حفظ PDF من OneNote وإضافة الصفحات الفرعية
url: /ar/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية حفظ OneNote PDF وإضافة الصفحات الفرعية

## المقدمة

في هذا البرنامج التعليمي، ستكتشف **كيفية حفظ OneNote PDF** أثناء إنشاء مستند يحتوي على كل من الصفحات الجذرية والصفحات الفرعية باستخدام Aspose.Note for Java. تنظيم دفاتر ملاحظات OneNote بهرمية واضحة يجعل التنقل سهلًا، والقدرة على التصدير إلى PDF تضمن إمكانية مشاركة ملاحظاتك بصيغة يمكن قراءتها عالميًا. سنوضح لك أيضًا **كيفية إضافة صفحات فرعية بأسلوب OneNote**، بحيث يمكنك بناء هياكل متعددة المستويات بسهولة.

## إجابات سريعة
- **ماذا يعني الكلمة المفتاحية الأساسية؟** تشير إلى تصدير دفتر OneNote إلى PDF باستخدام Aspose.Note.
- **أي API يُستخدم؟** Aspose.Note for Java.
- **هل يمكنني إنشاء صفحات هرمية؟** نعم – قم بتعيين مستوى الصفحة لبناء صفحات جذرية وفرعية.
- **هل أحتاج إلى ترخيص؟** يتوفر إصدار تجريبي مجاني؛ يلزم وجود ترخيص تجاري للإنتاج.
- **ما صيغ الإخراج المدعومة؟** BMP، PDF، PNG، وأكثر.

## ما هو “كيفية حفظ OneNote PDF”؟
حفظ OneNote كملف PDF يحول صفحات الدفتر إلى مستند ثابت التخطيط يحتفظ بالتنسيق والصور والهرمية. هذا مثالي للمشاركة أو الأرشفة أو طباعة الملاحظات.

## لماذا إضافة صفحات فرعية في OneNote؟
إضافة صفحات فرعية تسمح لك بتجميع المحتوى المتعلق تحت صفحة أصلية، مما يعكس هيكلًا شبيهًا بالمجلدات. يحسن ذلك من تنظيم الملاحظات، ويسرّع البحث، ويعزز تجربة القراءة عندما يتم تصدير الدفتر إلى PDF.

## المتطلبات السابقة

قبل البدء، تأكد من توفر المتطلبات التالية:

1. مجموعة تطوير جافا (JDK): تأكد من تثبيت JDK على نظامك.  
2. Aspose.Note for Java: قم بتنزيل وتثبيت Aspose.Note for Java من [الموقع](https://purchase.aspose.com/buy).  
3. بيئة تطوير متكاملة (IDE): اختر IDE لجافا مثل IntelliJ IDEA أو Eclipse أو NetBeans.

## استيراد الحزم

ابدأ باستيراد الحزم اللازمة في مشروع جافا الخاص بك:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## الخطوة 1: إعداد دليل المستند

حدد الدليل الذي تريد حفظ مستند OneNote فيه:

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: إنشاء كائن المستند

أنشئ كائن `Document`:

```java
Document doc = new Document();
```

## الخطوة 3: إنشاء الصفحات

قم بتهيئة كائنات الصفحات وتعيين مستوياتها. يحدد تعيين المستوى ما إذا كانت الصفحة جذرية أو فرعية:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## الخطوة 4: إضافة العقد إلى الصفحات

### إضافة العقد إلى الصفحة الأولى

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### إضافة العقد إلى الصفحة الثانية

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### إضافة العقد إلى الصفحة الثالثة

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## الخطوة 5: إضافة الصفحات إلى المستند

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## الخطوة 6: حفظ المستند

احفظ مستند OneNote كملف PDF (أو BMP في هذا المثال). يتيح تغيير `SaveFormat` التصدير إلى PDF، مما يحقق متطلب “كيفية حفظ OneNote PDF”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **نصيحة احترافية:** لتصدير مباشرة إلى PDF، استبدل `SaveFormat.Bmp` بـ `SaveFormat.Pdf`.

تهانينا! لقد نجحت في إنشاء مستند OneNote يحتوي على صفحات جذرية وفرعية وتعلمت **كيفية حفظ OneNote PDF** باستخدام Aspose.Note for Java.

## لماذا هذا مهم

- **تنظيم هرمي:** تسمح الصفحات الجذرية والفرعية بمحاكاة هياكل المجلدات داخل OneNote.  
- **تصدير PDF سلس:** بمجرد التنظيم، يحافظ التصدير إلى PDF على الهرمية، مما يجعل المستند النهائي سهل القراءة والمشاركة.  
- **الأتمتة:** يمكن دمج الكود في تطبيقات جافا أكبر، مما يتيح إنشاء دفاتر ملاحظات منظمة دفعة واحدة.

## الأخطاء الشائعة وكيفية تجنبها

| المشكلة | السبب | الحل |
|-------|-------|----------|
| الصفحات تظهر على نفس المستوى | قيمة `setLevel` غير صحيحة | استخدم `setLevel((byte) 1)` للصفحات الجذرية و`setLevel((byte) 2)` (أو أعلى) للصفحات الفرعية. |
| مخرجات PDF تظهر فارغة | عدم استخدام `SaveFormat.Pdf` أو مسار ملف غير صحيح | تحقق من وجود الدليل واستخدم `SaveFormat.Pdf`. |
| الخط غير مطبق | اسم الخط غير صحيح أو الخط غير موجود على النظام | تأكد من تثبيت الخط (مثال: “David Transparent”) على الجهاز الذي يشغل الكود. |

## الأسئلة المتكررة

**س: هل يمكنني إنشاء مستويات متعددة من الصفحات الفرعية باستخدام Aspose.Note for Java؟**  
ج: نعم، يمكنك إنشاء هرميات أعمق عن طريق تعيين أرقام مستويات أعلى (مثال: `setLevel((byte) 3)` للصفحة الفرعية من المستوى الثالث).

**س: هل Aspose.Note for Java متوافق مع بيئات تطوير جافا المختلفة؟**  
ج: بالتأكيد. يعمل مع IntelliJ IDEA و Eclipse و NetBeans وأي IDE يدعم تطوير جافا.

**س: هل يمكنني تخصيص تنسيق النص في مستند OneNote الخاص بي؟**  
ج: نعم. استخدم `ParagraphStyle` لتعيين اسم الخط، الحجم، اللون، وغيرها من الخصائص لكل عنصر `RichText`.

**س: هل يدعم Aspose.Note for Java حفظ المستندات بصيغ غير BMP؟**  
ج: نعم. تشمل الصيغ المدعومة PDF، PNG، JPEG، DOCX، وأكثر. غيّر قيمة تعداد `SaveFormat` وفقًا لذلك.

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.Note for Java؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية من موقع Aspose.

## الخلاصة

إن تنظيم دفاتر ملاحظات OneNote بهرمية واضحة وتصديرها كملفات PDF يجعل ملاحظاتك أكثر قابلية للوصول والمشاركة. باتباع الخطوات أعلاه، أصبحت الآن تعرف **كيفية حفظ OneNote PDF** و**إضافة صفحات فرعية بأسلوب OneNote** برمجيًا باستخدام Aspose.Note for Java.

---

**آخر تحديث:** 2026-01-07  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (الأحدث)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}