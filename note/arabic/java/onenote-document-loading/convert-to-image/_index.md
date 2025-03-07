---
title: تحويل مستند OneNote إلى صورة - جافا
linktitle: تحويل مستند OneNote إلى صورة - جافا
second_title: Aspose.Note جافا API
description: تعرّف على كيفية تحويل OneNote إلى صورة باستخدام Aspose.Note لـ Java. اتبع الخطوات السهلة، وقم بتحميل المستند، وتهيئة الخيارات، واحفظه بتنسيق PNG.
weight: 14
url: /ar/java/onenote-document-loading/convert-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل مستند OneNote إلى صورة - جافا

## مقدمة

في هذا البرنامج التعليمي، سنرشدك خلال عملية استخدام Aspose.Note لـ Java لتحويل مستند OneNote إلى صورة. سنقوم بتقسيم كل خطوة إلى تعليمات سهلة الاتباع.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1. تم تثبيت Java Development Kit (JDK) على نظامك.
2.  Aspose.Note لمكتبة جافا. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/java/).

## حزم الاستيراد

أولاً، قم باستيراد الحزم الضرورية في كود Java الخاص بك:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

لنقم الآن بتقسيم رمز المثال المقدم إلى خطوات متعددة:

## الخطوة 1: إعداد دليل المستندات

حدد الدليل الذي يوجد به مستند OneNote الخاص بك:

```java
String dataDir = "Your Document Directory";
```

 يستبدل`"Your Document Directory"` مع المسار إلى مستند OneNote الخاص بك.

## الخطوة 2: قم بتحميل المستند

قم بتحميل مستند OneNote في Aspose.Note:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 يضمن`"Sample1.one"` يطابق اسم ملف مستند OneNote الخاص بك.

## الخطوة 3: تهيئة ImageSaveOptions

 تهيئة`ImageSaveOptions` كائن لتحديد تنسيق الحفظ:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

هنا، نقوم بحفظ المستند كصورة PNG. يمكنك اختيار تنسيقات أخرى مثل JPEG أو BMP إذا لزم الأمر.

## الخطوة 4: احفظ المستند كصورة

احفظ المستند الذي تم تحميله كصورة:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

يحفظ هذا السطر المستند كصورة PNG مع الخيارات المحددة.

## الخطوة 5: تأكيد الطباعة

اطبع رسالة لتأكيد حفظ الملف:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

يعلمك هذا السطر بنجاح التحويل وموقع ملف الصورة المحفوظ.

## خاتمة

باتباع الخطوات الموضحة أعلاه، يمكنك بسهولة تحويل مستند OneNote إلى صورة باستخدام Aspose.Note لـ Java. إنها طريقة بسيطة وفعالة للتعامل مع تحويلات المستندات في تطبيقات Java الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني تحويل عدة مستندات OneNote دفعة واحدة؟

A1: نعم، يمكنك التنقل عبر قائمة المستندات وإجراء عملية التحويل لكل مستند.

### س2: هل يدعم Aspose.Note تنسيقات الإخراج الأخرى بخلاف الصور؟

ج2: نعم، يدعم Aspose.Note تنسيقات الإخراج المختلفة مثل تنسيقات PDF وHTML وMicrosoft Word.

### س3: هل Aspose.Note متوافق مع كافة إصدارات ملفات OneNote؟

A3: يوفر Aspose.Note التوافق مع ملفات OneNote التي تم إنشاؤها في إصدارات مختلفة من Microsoft OneNote.

### س 4: هل يمكنني تخصيص دقة الصور الناتجة؟

ج4: نعم، يمكنك ضبط الدقة والمعلمات الأخرى باستخدام الخيارات المتاحة في Aspose.Note.

### س5: هل يتطلب Aspose.Note اتصالاً بالإنترنت لتحويل المستندات؟

ج5: لا، يعمل Aspose.Note محليًا دون الحاجة إلى اتصال بالإنترنت.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
