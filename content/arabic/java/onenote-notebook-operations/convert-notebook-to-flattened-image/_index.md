---
title: تحويل دفتر الملاحظات إلى صورة مسطحة في OneNote - Aspose.Note
linktitle: تحويل دفتر الملاحظات إلى صورة مسطحة في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرف على كيفية تحويل دفتر ملاحظات إلى صورة مسطحة في OneNote باستخدام Aspose.Note لـ Java. الحفاظ على جميع العناصر في ملف صورة واحد دون عناء.
type: docs
weight: 13
url: /ar/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---
## مقدمة

في هذا البرنامج التعليمي، سنرشدك خلال عملية تحويل دفتر ملاحظات إلى صورة مسطحة في OneNote باستخدام Aspose.Note لـ Java. يتيح لك ذلك حفظ دفتر الملاحظات الخاص بك كملف صورة، مما يضمن الحفاظ على جميع العناصر بتنسيق صورة واحدة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1. تم تثبيت Java Development Kit (JDK) على نظامك.
2.  تم تنزيل Aspose.Note لمكتبة Java وإعدادها في مشروع Java الخاص بك. يمكنك تحميل المكتبة من[هنا](https://releases.aspose.com/note/java/).
3. المعرفة الأساسية ببرمجة جافا.

## حزم الاستيراد

للبدء، تحتاج إلى استيراد الحزم الضرورية من Aspose.Note لـ Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## الخطوة 1: إعداد دليل المستندات

أولاً، حدد الدليل الذي يوجد به ملف دفتر الملاحظات الخاص بك:

```java
String dataDir = "Your Document Directory";
```

 يستبدل`"Your Document Directory"` مع المسار إلى ملف دفتر الملاحظات الخاص بك.

## الخطوة 2: تحميل دفتر الملاحظات

 بعد ذلك، قم بتحميل ملف دفتر الملاحظات باستخدام ملف`Notebook` فصل:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 تأكد من الاستبدال`"test.onetoc2"` مع اسم ملف دفتر الملاحظات الخاص بك.

## الخطوة 3: ضبط خيارات حفظ الصورة

الآن، قم بإعداد الخيارات لحفظ دفتر الملاحظات كصورة. سنحدد تنسيق الحفظ كـ PNG ونضبط الدقة على 400 نقطة في البوصة:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

يمكنك ضبط الدقة وفقًا لمتطلباتك.

## الخطوة 4: تسوية دفتر الملاحظات

للتأكد من أن كافة العناصر قد تم تسويتها في صورة واحدة، قم بتعيين`flatten` خيار ل`true`:

```java
saveOptions.setFlatten(true);
```

وهذا يضمن أن الصورة الناتجة تحافظ على تخطيط دفتر الملاحظات الخاص بك.

## الخطوة 5: حفظ الصورة

أخيرًا، احفظ دفتر الملاحظات كصورة مسطحة:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 يستبدل`"ExportImageasFlattenedNotebook_out.png"` مع اسم ملف الإخراج المطلوب.

## خاتمة

في الختام، باستخدام Aspose.Note for Java، يمكنك بسهولة تحويل دفتر ملاحظاتك إلى صورة مسطحة في OneNote. تضمن هذه العملية الحفاظ على جميع العناصر في تنسيق صورة واحدة، مما يسهل المشاركة والعرض بسهولة.

## الأسئلة الشائعة

### س1: هل يمكنني ضبط دقة الصورة الناتجة؟

 ج1: نعم، يمكنك ضبط الدقة وفقًا لمتطلباتك عن طريق تعديل`setResolution` معلمة الطريقة.

### س2: هل يدعم Aspose.Note تنسيقات الصور الأخرى للتصدير؟

ج2: نعم، يدعم Aspose.Note تنسيقات صور متنوعة مثل PNG، وJPEG، وBMP، وما إلى ذلك، لتصدير دفاتر الملاحظات.

### س3: هل يمكنني تخصيص الصورة الناتجة بشكل أكبر؟

ج3: نعم، يوفر Aspose.Note خيارات شاملة لتخصيص الصورة الناتجة، بما في ذلك حجم الصفحة والاتجاه وإعدادات الجودة.

### س4: هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ Java؟

 ج4: نعم، يمكنك الحصول على نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).

### س5: أين يمكنني العثور على دعم لـ Aspose.Note لـ Java؟

 ج5: يمكنك العثور على الدعم والموارد في منتدى Aspose.Note[هنا](https://forum.aspose.com/c/note/28).