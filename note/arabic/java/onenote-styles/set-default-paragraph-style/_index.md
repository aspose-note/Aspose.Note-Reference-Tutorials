---
title: تعيين نمط الفقرة الافتراضي في OneNote - Aspose.Note
linktitle: تعيين نمط الفقرة الافتراضي في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرف على كيفية تعيين أنماط الفقرة الافتراضية في OneNote باستخدام Aspose.Note لـ Java. اتبع دليلنا خطوة بخطوة لتنسيق النص بكفاءة في تطبيقات Java الخاصة بك.
weight: 11
url: /ar/java/onenote-styles/set-default-paragraph-style/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين نمط الفقرة الافتراضي في OneNote - Aspose.Note

## مقدمة

يوفر Aspose.Note for Java إمكانات قوية لمعالجة تنسيق النص، بما في ذلك تعيين أنماط الفقرة الافتراضية. سيرشدك هذا البرنامج التعليمي خلال عملية تعيين أنماط الفقرة الافتراضية في OneNote باستخدام Aspose.Note.

## المتطلبات الأساسية

قبل أن تبدأ، تأكد من أن لديك ما يلي:

1. Java Development Kit (JDK): تأكد من تثبيت JDK على نظامك.
2.  Aspose.Note لمكتبة Java: قم بتنزيل Aspose.Note لـ Java وتثبيته من[صفحة التحميل](https://releases.aspose.com/note/java/).
3. بيئة التطوير المتكاملة (IDE): يجب أن يكون لديك IDE مثبتًا، مثل Eclipse أو IntelliJ IDEA، لتسهيل عملية البرمجة.

## حزم الاستيراد

أولاً، قم باستيراد الحزم اللازمة لبدء البرمجة:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

الآن، دعونا نقسم رمز المثال إلى خطوات متعددة:

## الخطوة 1: تهيئة المستند والصفحة والمخطط التفصيلي

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## الخطوة 2: إنشاء عنصر المخطط التفصيلي

```java
OutlineElement outlineElem = new OutlineElement();
```

## الخطوة 3: تحديد نمط الفقرة الافتراضي

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## الخطوة 4: إنشاء نص منسق بالنمط الافتراضي

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## الخطوة 5: إلحاق نص منسق بعنصر المخطط التفصيلي

```java
outlineElem.appendChildLast(text);
```

## الخطوة 6: إلحاق عنصر المخطط التفصيلي بالمخطط التفصيلي

```java
outline.appendChildLast(outlineElem);
```

## الخطوة 7: إلحاق المخطط التفصيلي بالصفحة

```java
page.appendChildLast(outline);
```

## الخطوة 8: إلحاق الصفحة بالمستند

```java
document.appendChildLast(page);
```

## الخطوة 9: حفظ المستند

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

سيقوم هذا الرمز بتعيين نمط الفقرة الافتراضي في OneNote باستخدام Aspose.Note لـ Java.

## خاتمة

يمكن تحقيق تعيين أنماط الفقرة الافتراضية في OneNote برمجيًا بكفاءة باستخدام Aspose.Note لـ Java. باتباع الخطوات الموضحة في هذا البرنامج التعليمي، يمكنك دمج هذه الوظيفة بسلاسة في تطبيقات Java الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص نمط الفقرة الافتراضي بشكل أكبر؟

A1: نعم، يمكنك ضبط معلمات مختلفة مثل اسم الخط والحجم واللون والمحاذاة لتناسب متطلباتك.

### س2: هل يدعم Aspose.Note عمليات تنسيق النص الأخرى؟

ج2: بالتأكيد، يوفر Aspose.Note دعمًا شاملاً لمعالجة تنسيق النص، بما في ذلك أنماط الخطوط والنقاط النقطية والمسافات البادئة.

### س3: هل Aspose.Note متوافق مع كافة إصدارات OneNote؟

ج3: تم تصميم Aspose.Note للعمل مع ملفات Microsoft OneNote عبر إصدارات مختلفة، مما يضمن التوافق الواسع.

### س4: هل يمكنني دمج Aspose.Note في مشروع Java الحالي الخاص بي؟

ج4: نعم، يمكنك بسهولة دمج Aspose.Note في مشاريع Java الخاصة بك عن طريق إضافة التبعيات الضرورية واستيراد الحزم المطلوبة.

### س5: هل هناك نسخة تجريبية متاحة لـ Aspose.Note؟

 ج5: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية من Aspose.Note من[موقع إلكتروني](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
