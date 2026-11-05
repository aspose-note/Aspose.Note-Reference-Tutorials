---
date: 2026-11-05
description: تعلم كيفية تقليل حجم ملف TIFF عند تحويل دفاتر ملاحظات OneNote إلى TIFF
  في Java باستخدام Aspose.Note. يتضمن خيارات JPEG و PackBits و TIFF بالأبيض والأسود.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: كيفية تقليل حجم ملف TIFF عند تحويل OneNote في Java
og_description: تعلم كيفية تقليل حجم ملف TIFF عند تحويل دفاتر ملاحظات OneNote إلى
  TIFF في Java باستخدام Aspose.Note. يتضمن خيارات JPEG و PackBits و TIFF بالأبيض والأسود.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: كيفية تقليل حجم ملف TIFF عند تحويل OneNote في Java
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: كيفية تقليل حجم ملف TIFF عند تحويل OneNote في Java
url: /ar/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تقليل حجم ملف TIFF عند تحويل OneNote في Java

## مقدمة

في هذا الدرس ستكتشف كيفية **تقليل حجم ملف TIFF** أثناء تحويل دفاتر OneNote إلى صور TIFF باستخدام Aspose.Note for Java. سنستعرض ثلاث طرق ضغط — TIFF JPEG، PackBits، و CCITT Group 3 (TIFF أبيض‑أسود) — ونوضح لك كيفية تعديل جودة الصورة، التحكم في وضع اللون، والحفاظ على حجم الملفات مثاليًا للويب أو الأرشفة أو سيناريوهات الفاكس.

## إجابات سريعة
- **ما هو ضغط TIFF JPEG؟** طريقة ضغط فقدانية تقلل حجم ملف TIFF مع الحفاظ على الجودة البصرية.  
- **ما المكتبة التي تتعامل مع التحويل؟** Aspose.Note for Java.  
- **هل أحتاج إلى ترخيص؟** إصدار تجريبي مجاني يعمل للاختبار؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني تغيير جودة الصورة؟** نعم، قم بتعيين خاصية `quality` في `ImageSaveOptions`.  
- **هل التحويل على دفعات ممكن؟** بالتأكيد – قم بالتكرار عبر المستندات وتطبيق نفس الخيارات.

## نظرة عامة على ضغط TIFF JPEG

ضغط TIFF JPEG يخزن بيانات الصورة في حاوية TIFF لكنه يطبق خوارزمية JPEG الفقدانية لتقليل حجم الملف. إنه مثالي عندما تحتاج إلى توازن بين **جودة صورة TIFF** وحجم ملف أصغر، خاصة للويب أو سيناريوهات الأرشفة.

## لماذا استخدام أنواع ضغط TIFF المختلفة؟

تختار نوع الضغط بناءً على المحتوى واحتياجات التخزين: JPEG يعمل بشكل أفضل للصور الفوتوغرافية، PackBits يوفر ضغطًا غير فقداني للرسومات ذات المناطق المتجانسة الكبيرة، و CCITT Group 3 يقدم ضغطًا عالي النسبة للمستندات الأحادية اللون بنمط الفاكس. اختيار الطريقة الصحيحة يتيح لك **تقليل حجم ملف TIFF** دون التضحية بالوضوح البصري المطلوب لتطبيقك.

## اختيار الضغط المناسب

- **JPEG** – جودة قابلة للتعديل (0‑100) تتيح لك الموازنة بين الحجم والتفاصيل، مثالية للصفحات الغنية بالألوان.  
- **PackBits** – ترميز بطول تشغيل غير فقداني؛ مثالي عندما يجب الحفاظ على كل بكسل بدقة.  
- **CCITT Group 3** – أحادي اللون فقط؛ يحقق أقصى ضغط للنص الممسوح ضوئيًا أو مستندات الفاكس.  

## تحويل OneNote إلى TIFF باستخدام Aspose.Note

إذا كان هدفك هو **تحويل OneNote إلى TIFF**، تغطي الطرق الثلاثة أدناه أكثر السيناريوهات شيوعًا. كل طريقة تقوم بتحميل ملف `.one`، وتكوين `ImageSaveOptions`، وحفظ النتيجة كملف `.tiff`.

## المتطلبات المسبقة

- مجموعة تطوير Java (JDK) مثبتة.  
- مكتبة Aspose.Note for Java مضافة إلى مشروعك (Maven/Gradle أو JAR يدوي).  
- إلمام أساسي بصياغة Java.

## استيراد الحزم

الفئات `ImageSaveOptions` و `TiffCompression` و `ColorMode` هي جوهر واجهة برمجة تطبيقات التحويل.  

`ImageSaveOptions` تحدد الخيارات لحفظ الصور، مثل الصيغة والضغط.  
`TiffCompression` تسرد خوارزميات ضغط TIFF المدعومة.  
`ColorMode` يحدد عمق اللون، مثل اللون أو أبيض‑أسود.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## الخطوة 1: حفظ كـ TIFF باستخدام ضغط TIFF JPEG

### حفظ TIFF باستخدام ضغط JPEG في Java

حمّل ملف OneNote، قم بتكوين `ImageSaveOptions` باستخدام ضغط JPEG، واختياريًا عيّن قيمة `quality`، ثم استدعِ طريقة الحفظ. هذا النمط ذو الخطوتين يمنحك التحكم الكامل في حجم الإخراج والوضوح البصري.

1. حدد `dataDir` إلى المجلد الذي يحتوي على ملف `.one` الخاص بك.  
2. استدعِ `SaveToTiffUsingJpegCompression()` من الدالة الرئيسية أو الخدمة.  
3. سيظهر ملف `.tiff` الناتج في نفس الدليل.

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**شرح**

- `ImageSaveOptions` يخبر Aspose.Note بإخراج ملف TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` يختار ضغط JPEG.  
- `setQuality(93)` (اختياري) يضبط جودة الصورة بدقة؛ القيم الأقل تنتج ملفات أصغر.

## نظرة عامة على ضغط TIFF PackBits

PackBits هو خوارزمية ضغط غير فقدانية تعمل بشكل أفضل للصور التي تحتوي على مساحات كبيرة من اللون الصلب. غالبًا ما يُشار إليه كـ **ضغط tiff packbits** في الوثائق.

## حفظ TIFF باستخدام ضغط PackBits في Java

إذا كنت بحاجة إلى خيار غير فقداني، فإن PackBits هو خوارزمية تشغيل بطول بسيطة تعمل جيدًا للرسومات ذات الألوان الصلبة. قم بتكوين `ImageSaveOptions` باستخدام `TiffCompression.PackBits` واحفظ المستند.

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**شرح**

- `setTiffCompression(TiffCompression.PackBits)` يبدل طريقة الضغط.  
- لا حاجة لتعيين جودة لأن PackBits غير فقداني.

## حفظ TIFF باستخدام ضغط CCITT Group 3 في Java

للمستندات بنمط الفاكس غالبًا ما تحتاج إلى **TIFF أبيض وأسود**. يوفر CCITT Group 3 ضغطًا عاليًا للصور أحادية اللون. اضبط وضع اللون إلى أبيض‑أسود واختر تعداد ضغط CCITT 3.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**شرح**

- `setColorMode(ColorMode.BlackAndWhite)` يفرض إخراجًا أحادي اللون.  
- `setTiffCompression(TiffCompression.Ccitt3)` يطبق ضغطًا مخصصًا للفاكس.

## المشكلات الشائعة والنصائح

| المشكلة | الحل |
|-------|----------|
| **ملف الإخراج أكبر من المتوقع** | حاول تقليل قيمة JPEG `quality` أو التحويل إلى PackBits إذا كان الضغط غير الفاقد مقبولًا. |
| **الألوان تبدو باهتة** | تأكد من أنك لم تقم بتعيين `ColorMode.BlackAndWhite` عن غير قصد عندما تحتاج إلى ألوان كاملة. |
| **خطأ تنسيق صورة غير مدعوم** | تحقق من أنك تستخدم نسخة حديثة من Aspose.Note؛ الإصدارات القديمة قد تفتقر إلى بعض تعدادات الضغط. |
| **LicenseException أثناء التشغيل** | قم بتثبيت ترخيص Aspose.Note صالح (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## الأسئلة المتكررة

**س: هل يمكنني تحويل أنواع مستندات أخرى (مثل PDF، DOCX) إلى TIFF باستخدام هذه الخيارات؟**  
ج: نعم. بينما يركز Aspose.Note على ملفات OneNote، توفر مكتبات Aspose.PDF و Aspose.Words وغيرها خيارات `ImageSaveOptions` مماثلة لتنسيقاتها.

**س: كيف يختلف ضغط TIFF JPEG عن ملف JPEG عادي؟**  
ج: خوارزمية JPEG هي نفسها، لكن بيانات الصورة توجد داخل حاوية TIFF، التي يمكنها احتواء صفحات متعددة وبيانات وصفية أغنى.

**س: هل من الممكن معالجة دفعة من ملفات `.one` متعددة؟**  
ج: بالتأكيد. قم بالتكرار عبر دليل، استدعِ أي من الطرق الثلاث لكل ملف، واجمع ملفات TIFF الناتجة.

**س: هل يمكنني التحكم في DPI/الدقة لملف TIFF الناتج؟**  
ج: نعم. استخدم `options.setResolution(int dpi)` قبل الحفظ.

**س: هل يدعم Aspose.Note المعالجة غير المتزامنة؟**  
ج: الواجهة البرمجية نفسها متزامنة، لكن يمكنك تغليف الاستدعاءات في `CompletableFuture` الخاصة بـ Java أو مجموعة من الخيوط للتنفيذ المتوازي.

## الخلاصة

أصبحت الآن تمتلك مجموعة أدوات **تحويل TIFF في Java** كاملة تتيح لك **تقليل حجم ملف TIFF** عند حفظ مستندات OneNote كملفات TIFF باستخدام ضغط JPEG أو PackBits أو CCITT Group 3 Fax. اضبط الجودة، وضع اللون، والدقة لتلبية متطلباتك الخاصة، ودمج هذه الطرق في سير عمل دفعي لتحقيق أقصى إنتاجية.

---

**آخر تحديث:** 2026-11-05  
**تم الاختبار مع:** Aspose.Note for Java 26.4 (latest at time of writing)  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية عرض صورة صفحة OneNote (JPEG) باستخدام تنسيق الحفظ مع Aspose.Note for Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [استخدام Aspose.Note for Java لحفظ OneNote كـ PNG مع الخيارات – تحويل الدفتر إلى صورة](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [كيفية تصدير OneNote كصورة تدرج رمادي – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}