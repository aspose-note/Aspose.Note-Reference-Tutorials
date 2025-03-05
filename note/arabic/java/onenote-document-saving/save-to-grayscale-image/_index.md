---
title: حفظ إلى صورة بتدرج الرمادي في OneNote - Aspose.Note
linktitle: حفظ إلى صورة بتدرج الرمادي في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرف على كيفية حفظ مستند كصورة بتدرج رمادي في OneNote باستخدام Aspose.Note لـ Java. يمكنك التعامل بسهولة مع مستندات Microsoft OneNote برمجياً.
type: docs
weight: 17
url: /ar/java/onenote-document-saving/save-to-grayscale-image/
---
## مقدمة

في هذا البرنامج التعليمي، سنستكشف كيفية حفظ مستند كصورة بتدرج رمادي في OneNote باستخدام Aspose.Note لـ Java. الصور ذات التدرج الرمادي هي صور أحادية اللون حيث يتم تمثيل معلومات الألوان بظلال اللون الرمادي فقط. Aspose.Note عبارة عن واجهة برمجة تطبيقات Java قوية تسمح بمعالجة مستندات Microsoft OneNote برمجيًا.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1. تم تثبيت Java Development Kit (JDK) على نظامك.
2.  Aspose.Note لمكتبة جافا. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/java/).
3. الفهم الأساسي لبرمجة جافا.

## حزم الاستيراد

للبدء، قم باستيراد الحزم الضرورية:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## الخطوة 1: قم بتحميل المستند

 أولاً، قم بتحميل المستند إلى Aspose.Note. يستبدل`"Your Document Directory"` مع المسار إلى دليل المستندات الخاص بك و`"Aspose.one"` باسم مستند OneNote الخاص بك.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## الخطوة 2: تعيين مسار الإخراج والخيارات

حدد مسار الإخراج للصورة ذات التدرج الرمادي وحدد خيارات الحفظ. سنقوم بضبط وضع الألوان على التدرج الرمادي.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## الخطوة 3: احفظ المستند

وأخيرًا، احفظ المستند كصورة ذات تدرج رمادي باستخدام الخيارات المحددة.

```java
oneFile.save(dataDir, options);
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية حفظ مستند كصورة بتدرج رمادي في OneNote باستخدام Aspose.Note لـ Java. يمكن أن يكون هذا مفيدًا بشكل لا يصدق للعديد من التطبيقات التي تتطلب صورًا ذات تدرج رمادي.

## الأسئلة الشائعة

### س1: هل يمكنني حفظ الصورة ذات التدرج الرمادي بتنسيق مختلف؟

 ج1: نعم يمكنك ذلك. ببساطة قم بتغيير`SaveFormat` المعلمة في`ImageSaveOptions` منشئ إلى التنسيق المطلوب.

### س2: هل Aspose.Note متوافق مع كافة إصدارات مستندات OneNote؟

ج2: يدعم Aspose.Note Microsoft OneNote 2010 والإصدارات الأحدث.

### س3: هل يتطلب Aspose.Note ترخيصًا للاستخدام؟

ج3: نعم، أنت بحاجة إلى ترخيص صالح لاستخدام Aspose.Note في بيئات الإنتاج. ومع ذلك، يمكنك الحصول على ترخيص مؤقت لأغراض الاختبار.

### س4: هل يمكنني معالجة جوانب أخرى من المستند قبل حفظه كصورة؟

ج4: بالتأكيد! يوفر Aspose.Note مجموعة واسعة من الميزات لتحرير مستندات OneNote برمجيًا.

### س5: أين يمكنني العثور على الدعم إذا واجهت مشكلات؟

ج5: يمكنك العثور على الدعم في منتدى Aspose.Note[هنا](https://forum.aspose.com/c/note/28).