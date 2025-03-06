---
title: احفظ إلى PDF باستخدام إعدادات الصفحة في OneNote - Aspose.Note
linktitle: احفظ إلى PDF باستخدام إعدادات الصفحة في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرف على كيفية حفظ مستندات OneNote إلى PDF في Java باستخدام مكتبة Aspose.Note. دليل خطوة بخطوة مع أمثلة التعليمات البرمجية لإعدادات الصفحة المختلفة.
weight: 19
url: /ar/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# احفظ إلى PDF باستخدام إعدادات الصفحة في OneNote - Aspose.Note

## مقدمة

في هذا البرنامج التعليمي، سوف نتعلم كيفية حفظ مستندات OneNote بتنسيق PDF باستخدام إعدادات صفحة مختلفة باستخدام Aspose.Note لـ Java. سنغطي طريقتين: الحفظ باستخدام إعدادات صفحة Letter والحفظ باستخدام إعدادات صفحة A4 بدون حد للارتفاع.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

1. تم تثبيت Java Development Kit (JDK) على نظامك.
2. تم تنزيل Aspose.Note لمكتبة Java وإدراجها في مشروع Java الخاص بك.
3. الفهم الأساسي للغة البرمجة جافا.

## حزم الاستيراد

تأكد من أنك قمت باستيراد الحزم اللازمة لاستخدام Aspose.Note لـ Java في مشروعك. إليك بيان الاستيراد:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## احفظ إلى PDF باستخدام إعدادات صفحة الرسالة

### الخطوة 1: قم بتحميل المستند

أولاً، قم بتحميل مستند OneNote إلى Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### الخطوة 2: تحديد مسار الوجهة

حدد مسار الوجهة لملف PDF:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### الخطوة 3: احفظ المستند

احفظ المستند باستخدام إعدادات صفحة Letter:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## احفظ إلى PDF باستخدام إعدادات صفحة A4 بدون حد للارتفاع

### الخطوة 1: قم بتحميل المستند

وبالمثل، قم بتحميل مستند OneNote إلى Aspose.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### الخطوة 2: تحديد مسار الوجهة

حدد مسار الوجهة لملف PDF:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### الخطوة 3: احفظ المستند

احفظ المستند بإعدادات صفحة A4 دون حد الارتفاع:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

بعد اتباع هذه الخطوات، ستكون قد قمت بحفظ مستند OneNote الخاص بك إلى PDF بنجاح باستخدام إعدادات صفحة مختلفة.

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا كيفية حفظ مستندات OneNote بتنسيق PDF باستخدام Aspose.Note لمكتبة Java. باتباع الدليل الموضح خطوة بخطوة، يمكنك بسهولة دمج هذه الوظيفة في تطبيقات Java الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص إعدادات الصفحة بشكل أكبر؟

ج1: نعم، يمكنك تخصيص إعدادات الصفحة وفقًا لمتطلباتك باستخدام Aspose.Note لـ Java.

### س2: هل يدعم Aspose.Note تنسيقات الإخراج الأخرى بخلاف PDF؟

ج2: نعم، يدعم Aspose.Note تنسيقات الإخراج المختلفة بما في ذلك الصور وHTML.

### س3: هل Aspose.Note متوافق مع الإصدارات المختلفة من ملفات OneNote؟

ج3: نعم، يدعم Aspose.Note ملفات OneNote من إصدارات مختلفة بما في ذلك .one و.onetoc2.

### س4: هل يمكنني تحويل عدة ملفات OneNote إلى PDF في عملية تشغيل واحدة؟

ج4: نعم، يمكنك معالجة عدة ملفات OneNote دفعةً واحدة باستخدام Aspose.Note لـ Java.

### س5: هل هناك أي نسخة تجريبية متاحة لأغراض الاختبار؟

ج5: نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Note لـ Java من موقع الويب.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
