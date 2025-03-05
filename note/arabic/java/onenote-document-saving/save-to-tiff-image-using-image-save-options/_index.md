---
title: حفظ إلى صورة TIFF باستخدام خيارات حفظ الصورة في OneNote
linktitle: حفظ إلى صورة TIFF باستخدام خيارات حفظ الصورة في OneNote
second_title: Aspose.Note جافا API
description: تحويل مستندات OneNote إلى TIFF والتحكم في حجم الملف وجودته! اختر ضغط Jpeg أو PackBits أو Fax في Java. احصل على أمثلة التعليمات البرمجية وتعلم كيف! #OneNote #Java #Aspose
type: docs
weight: 21
url: /ar/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---
## مقدمة

ستتعلم في هذا البرنامج التعليمي كيفية حفظ مستند بتنسيق صورة TIFF باستخدام طرق ضغط مختلفة في Aspose.Note لـ Java. سنقوم بتغطية المتطلبات الأساسية واستيراد الحزم وتوفير دليل خطوة بخطوة لكل طريقة ضغط.

## المتطلبات الأساسية

قبل أن تبدأ، تأكد من أن لديك ما يلي:

- تم تثبيت Java Development Kit (JDK) على نظامك.
- تم تنزيل Aspose.Note لمكتبة Java وتكوينها.
- الفهم الأساسي للغة البرمجة جافا.

## حزم الاستيراد

أولاً، تحتاج إلى استيراد الحزم الضرورية إلى ملف Java الخاص بك:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## الخطوة 1: الحفظ في TIFF باستخدام ضغط JPEG

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // المسار إلى دليل المستندات.
    String dataDir = "Your Document Directory";

    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  قم بتحميل المستند باستخدام`Document` فصل.
-  إنشاء مثيل ل`ImageSaveOptions` وحدد نوع ضغط TIFF كـ JPEG.
- اضبط الجودة المطلوبة (اختياري).
- احفظ المستند بتنسيق TIFF باستخدام الخيارات المحددة.

## الخطوة 2: الحفظ في TIFF باستخدام ضغط PackBits

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // المسار إلى دليل المستندات.
    String dataDir = "Your Document Directory";

    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  قم بتحميل المستند باستخدام`Document` فصل.
-  إنشاء مثيل ل`ImageSaveOptions` وحدد نوع ضغط TIFF كـ PackBits.
- احفظ المستند بتنسيق TIFF باستخدام الخيارات المحددة.

## الخطوة 3: الحفظ في TIFF باستخدام ضغط الفاكس CCITT Group 3

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // المسار إلى دليل المستندات.
    String dataDir = "Your Document Directory";

    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  قم بتحميل المستند باستخدام`Document` فصل.
-  إنشاء مثيل ل`ImageSaveOptions` وحدد نوع ضغط TIFF كفاكس CCITT Group 3.
- اضبط وضع الألوان على الأسود والأبيض.
- احفظ المستند بتنسيق TIFF باستخدام الخيارات المحددة.

## خاتمة

في هذا البرنامج التعليمي، تعلمت كيفية حفظ مستند بتنسيق صورة TIFF باستخدام طرق ضغط مختلفة في Aspose.Note لـ Java. باتباع الدليل الموضح خطوة بخطوة، يمكنك الاستفادة بكفاءة من إمكانيات Aspose.Note لتلبية متطلباتك.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.Note لـ Java لتحويل تنسيقات المستندات الأخرى إلى TIFF؟

ج1: نعم، يدعم Aspose.Note for Java التحويل من تنسيقات المستندات المختلفة إلى TIFF، بما في ذلك مستندات OneNote.

### س2: ما أهمية تحديد نوع الضغط عند الحفظ في TIFF؟

ج2: يتيح لك تحديد نوع الضغط التحكم في جودة الصورة وحجم الملف. توفر طرق الضغط المختلفة مقايضات بين الجودة ونسبة الضغط.

### س3: هل Aspose.Note for Java مناسب للمعالجة المجمعة للمستندات؟

ج3: نعم، يوفر Aspose.Note for Java واجهات برمجة التطبيقات للمعالجة المجمعة، مما يتيح لك أتمتة مهام تحويل المستندات بكفاءة.

### س4: هل يمكنني تخصيص إعدادات الضغط بشكل أكبر؟

ج4: نعم، يمكنك ضبط المعلمات مثل الجودة والدقة وطريقة الضغط لتخصيص الإخراج وفقًا لمتطلباتك.

### س5: هل يقدم Aspose.Note for Java الدعم الفني؟

ج5: نعم، توفر Aspose دعمًا فنيًا شاملاً من خلال المنتديات والأنظمة القائمة على التذاكر.