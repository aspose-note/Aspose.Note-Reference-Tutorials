---
date: 2026-04-30
description: تعرّف على كيفية **حفظ OneNote كملف PDF** وإضافة صفحات فرعية في OneNote
  باستخدام Aspose.Note للغة Java. اتبع هذا الدليل خطوة بخطوة لتنظيم ملاحظاتك بكفاءة.
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: كيفية حفظ OneNote كملف PDF وإضافة الصفحات الفرعية
second_title: Aspose.Note Java API
title: كيفية حفظ OneNote كملف PDF وإضافة الصفحات الفرعية
url: /ar/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية حفظ OneNote كملف PDF وإضافة الصفحات الفرعية

## مقدمة

في هذا البرنامج التعليمي، ستكتشف **كيفية حفظ OneNote كملف PDF** أثناء إنشاء مستند يحتوي على كل من الصفحات الجذرية والصفحات الفرعية باستخدام Aspose.Note for Java. تنظيم دفاتر OneNote الخاصة بك بهرمية واضحة يجعل التنقل سهلًا، وتصديرها إلى PDF يضمن إمكانية مشاركة ملاحظاتك بصيغة قابلة للقراءة عالميًا. سنظهر لك أيضًا كيفية **إضافة صفحات فرعية بأسلوب OneNote**، بحيث يمكنك بناء هياكل متعددة المستويات بسهولة.

## إجابات سريعة
- **ماذا يعني “save onenote as pdf”؟** يشير إلى تصدير دفتر OneNote إلى ملف PDF باستخدام Aspose.Note for Java.  
- **ما هو الـ API المطلوب؟** توفر Aspose.Note for Java الفئات والطرق اللازمة.  
- **هل يمكنني إنشاء صفحات هرمية؟** نعم – قم بتعيين مستوى الصفحة لبناء الصفحات الجذرية والصفحات الفرعية.  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** يتوفر نسخة تجريبية مجانية، لكن الترخيص التجاري مطلوب للاستخدام الإنتاجي.  
- **ما هي الصيغ التي يمكنني التصدير إليها؟** بالإضافة إلى PDF يمكنك التصدير إلى BMP و PNG و JPEG و DOCX وغيرها.

## كيفية حفظ OneNote كملف PDF

تحويل OneNote إلى PDF يحول كل صفحة من دفتر الملاحظات إلى مستند ثابت التخطيط يحافظ على التنسيق والصور والهرمية الصفحية. هذا مثالي للمشاركة أو الأرشفة أو طباعة الملاحظات مع الحفاظ على الهيكل الأصلي.

## لماذا إضافة صفحات فرعية في OneNote؟

إضافة صفحات فرعية تتيح لك تجميع المحتوى المتعلق تحت صفحة أصلية، مما يحاكي هيكلًا شبيهًا بالمجلدات. هذا يحسن تنظيم الملاحظات، ويسرّع عملية البحث، ويعزز تجربة القراءة عندما يتم تصدير دفتر الملاحظات إلى PDF.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من توفر المتطلبات التالية:

1. **Java Development Kit (JDK)** – تأكد من تثبيت JDK على نظامك.  
2. **Aspose.Note for Java** – قم بتنزيل وتثبيت Aspose.Note for Java من [الموقع الإلكتروني](https://purchase.aspose.com/buy).  
3. **Integrated Development Environment (IDE)** – اختر بيئة تطوير Java مثل IntelliJ IDEA أو Eclipse أو NetBeans.

## استيراد الحزم

ابدأ باستيراد الحزم اللازمة في مشروع Java الخاص بك:

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

إنشاء كائن `Document`:

```java
Document doc = new Document();
```

## الخطوة 3: إنشاء الصفحات

تهيئة كائنات الصفحات وتعيين مستوياتها. تحديد المستوى يحدد ما إذا كانت الصفحة جذرية أم صفحة فرعية:

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

احفظ مستند OneNote كملف PDF (أو BMP في هذا المثال). تغيير `SaveFormat` يتيح لك التصدير إلى PDF، مما يحقق متطلب “save onenote as pdf”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **نصيحة احترافية:** لتصدير مباشرة إلى PDF، استبدل `SaveFormat.Bmp` بـ `SaveFormat.Pdf`.

تهانينا! لقد نجحت في إنشاء مستند OneNote يحتوي على صفحات جذرية وفرعية وتعلمت **كيفية حفظ OneNote كملف PDF** باستخدام Aspose.Note for Java.

## لماذا هذا مهم

- **تنظيم هرمي:** تسمح الصفحات الجذرية والفرعية بمحاكاة هياكل المجلدات داخل OneNote.  
- **تصدير PDF سلس:** بمجرد التنظيم، يحافظ التصدير إلى PDF على الهرمية، مما يجعل المستند النهائي سهل القراءة والمشاركة.  
- **الأتمتة:** يمكن دمج الكود في تطبيقات Java الأكبر، مما يتيح إنشاء دفاتر ملاحظات منظمة دفعة واحدة.

## المشكلات الشائعة وكيفية تجنبها

| المشكلة | السبب | الحل |
|-------|-------|----------|
| الصفحات تظهر على نفس المستوى | قيمة `setLevel` غير صحيحة | استخدم `setLevel((byte) 1)` للصفحات الجذرية و `setLevel((byte) 2)` (أو أعلى) للصفحات الفرعية. |
| مخرجات PDF تظهر فارغة | عدم وجود `SaveFormat.Pdf` أو مسار ملف غير صحيح | تحقق من وجود الدليل واستخدم `SaveFormat.Pdf`. |
| الخط غير مطبق | اسم الخط غير صحيح أو الخط غير موجود على النظام | تأكد من تثبيت الخط (مثال: “David Transparent”) على الجهاز الذي يشغل الكود. |

## الأسئلة المتكررة

**س: هل يمكنني إنشاء مستويات متعددة من الصفحات الفرعية باستخدام Aspose.Note for Java؟**  
ج: نعم، يمكنك إنشاء هياكل أعمق بتعيين أرقام مستويات أعلى (مثال: `setLevel((byte) 3)` لصفحة فرعية من المستوى الثالث).

**س: هل Aspose.Note for Java متوافق مع بيئات تطوير Java المختلفة؟**  
ج: بالتأكيد. يعمل مع IntelliJ IDEA و Eclipse و NetBeans وأي بيئة تدعم تطوير Java.

**س: هل يمكنني تخصيص تنسيق النص في مستند OneNote الخاص بي؟**  
ج: نعم. استخدم `ParagraphStyle` لتعيين اسم الخط، الحجم، اللون، وغيرها من الخصائص لكل عنصر `RichText`.

**س: هل يدعم Aspose.Note for Java حفظ المستندات بصيغ غير BMP؟**  
ج: نعم. تشمل الصيغ المدعومة PDF و PNG و JPEG و DOCX وغيرها. غيّر تعداد `SaveFormat` وفقًا لذلك.

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.Note for Java؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية من موقع Aspose.

## الخلاصة

تنظيم دفاتر OneNote الخاصة بك بهيكل هرمي واضح وتصديرها كملفات PDF يجعل ملاحظاتك أكثر قابلية للوصول والمشاركة. باتباع الخطوات السابقة، أنت الآن تعرف **كيفية حفظ OneNote كملف PDF** و **إضافة صفحات فرعية بأسلوب OneNote** برمجيًا باستخدام Aspose.Note for Java.

---

**آخر تحديث:** 2026-04-30  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (latest)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}