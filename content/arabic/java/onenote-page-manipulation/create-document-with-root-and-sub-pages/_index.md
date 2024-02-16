---
title: قم بإنشاء مستند بالصفحات الجذرية والفرعية في OneNote
linktitle: قم بإنشاء مستند بالصفحات الجذرية والفرعية في OneNote
second_title: Aspose.Note جافا API
description: قم بإنشاء مستند يحتوي على صفحات جذرية وفرعية في OneNote باستخدام Aspose.Note لـ Java. اتبع الدليل الموضح خطوة بخطوة لتنظيم ملاحظاتك بكفاءة.
type: docs
weight: 11
url: /ar/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## مقدمة

في هذا البرنامج التعليمي، سنرشدك خلال عملية إنشاء مستند يحتوي على صفحات جذرية وفرعية في OneNote باستخدام Aspose.Note لـ Java. باتباع هذه الخطوات، ستتمكن من تنظيم مستندات OneNote بكفاءة باستخدام بنية هرمية.

## المتطلبات الأساسية

قبل البدء، تأكد من توفر المتطلبات الأساسية التالية:

1. Java Development Kit (JDK): تأكد من تثبيت JDK على نظامك.
2. Aspose.Note لـ Java: قم بتنزيل Aspose.Note لـ Java وتثبيته من[موقع إلكتروني](https://purchase.aspose.com/buy).
3. بيئة التطوير المتكاملة (IDE): اختر Java IDE مثل IntelliJ IDEA أو Eclipse أو NetBeans.

## حزم الاستيراد

ابدأ باستيراد الحزم الضرورية في مشروع Java الخاص بك:

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

## الخطوة 1: إعداد دليل المستندات

حدد الدليل الذي تريد حفظ مستند OneNote فيه:

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: إنشاء كائن المستند

 إنشاء مثيل أ`Document` هدف:

```java
Document doc = new Document();
```

## الخطوة 3: إنشاء الصفحات

تهيئة كائنات الصفحة وتعيين مستوياتها:

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

## الخطوة 5: إضافة صفحات إلى المستند

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## الخطوة 6: احفظ المستند

احفظ مستند OneNote:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // التعامل مع الاستثناء
}
```

تهانينا! لقد نجحت في إنشاء مستند يحتوي على صفحات جذرية وفرعية في OneNote باستخدام Aspose.Note لـ Java.

## خاتمة

يعد تنظيم مستندات OneNote الخاصة بك ببنية هرمية أمرًا ضروريًا لتحسين الإدارة والتنقل. باستخدام Aspose.Note لـ Java، يمكنك إنشاء مستندات ذات صفحات جذرية وفرعية بكفاءة، مما يوفر تخطيطًا واضحًا ومنظمًا لملاحظاتك.

## الأسئلة الشائعة

### س1: هل يمكنني إنشاء مستويات متعددة من الصفحات الفرعية باستخدام Aspose.Note لـ Java؟

ج1: نعم، يمكنك إنشاء مستويات متعددة للصفحات الفرعية عن طريق تعيين المستوى المناسب لكل صفحة.

### س2: هل Aspose.Note for Java متوافق مع بيئة Java IDEs المختلفة؟

ج2: نعم، Aspose.Note for Java متوافق مع Java IDEs الشائعة مثل IntelliJ IDEA وEclipse وNetBeans.

### س3: هل يمكنني تخصيص تنسيق النص في مستند OneNote الخاص بي؟

ج3: نعم، يمكنك تخصيص الخط واللون والحجم وخيارات التنسيق الأخرى باستخدام Aspose.Note لميزات النص المنسق في Java.

### س4: هل يدعم Aspose.Note for Java حفظ المستندات بتنسيقات مختلفة؟

ج4: نعم، يدعم Aspose.Note for Java حفظ المستندات بتنسيقات مختلفة بما في ذلك BMP وPDF وPNG والمزيد.

### س5: هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ Java؟

ج5: نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.Note لـ Java من موقع الويب.