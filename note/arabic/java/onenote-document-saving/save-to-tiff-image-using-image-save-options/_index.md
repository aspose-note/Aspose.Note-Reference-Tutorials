---
date: 2025-12-17
description: تعلم كيفية حفظ مستندات OneNote كملفات TIFF باستخدام ضغط TIFF JPEG أو
  PackBits أو CCITT Group 3 Fax في Java. تحكم في جودة الصورة وحجم الملف ووضع اللون
  باستخدام Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: حفظ إلى صورة TIFF باستخدام ضغط TIFF JPEG في OneNote
url: /ar/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ صورة TIFF باستخدام ضغط TIFF JPEG في OneNote

## المقدمة

في هذا الدرس ستكتشف **كيفية حفظ مستند OneNote كملف TIFF باستخدام ضغط TIFF JPEG** بالإضافة إلى طريقتين شائعتين آخرين للضغط. سنستعرض الإعدادات المطلوبة، نستورد الحزم اللازمة لجافا، ونوفر كودًا واضحًا خطوة بخطوة لكل خيار ضغط. في النهاية ستتمكن من التحكم في **جودة صورة TIFF**، تقليل حجم الملف، وحتى إنتاج ملفات TIFF بالأبيض والأسود لإخراج على نمط الفاكس.

## إجابات سريعة
- **ما هو ضغط TIFF JPEG؟** طريقة ضغط فقدانية تقلل حجم ملف TIFF مع الحفاظ على الجودة البصرية.  
- **أي مكتبة تتولى التحويل؟** Aspose.Note for Java.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للاختبار؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني تغيير جودة الصورة؟** نعم، عيّن خاصية `quality` في `ImageSaveOptions`.  
- **هل التحويل الجماعي ممكن؟** بالتأكيد – يمكنك حلق عبر المستندات وتطبيق نفس الخيارات.

## ما هو ضغط TIFF JPEG؟
يخزن ضغط TIFF JPEG بيانات الصورة داخل حاوية TIFF لكنه يطبق خوارزمية JPEG الفقدانية لتقليل حجم الملف. إنه مثالي عندما تحتاج إلى توازن بين **جودة صورة TIFF** وحجم أصغر، خاصةً للويب أو الأرشفة.

## لماذا نستخدم أنواع ضغط TIFF المختلفة؟
- **JPEG** – مناسب للصور الفوتوغرافية؛ يتيح ضبط الجودة.  
- **PackBits** – ترميز بسيط بدون فقد (run‑length)؛ مفيد للرسومات ذات المناطق المتجانسة الكبيرة.  
- **CCITT Group 3 Fax** – أبيض وأسود فقط؛ مثالي للمستندات الممسوحة وإرسال الفاكس.  

اختيار الضغط المناسب يتيح لك تلبية قيود التخزين دون التضحية بالوضوح البصري المطلوب لتطبيقك.

## المتطلبات المسبقة

- تثبيت مجموعة تطوير جافا (JDK).  
- إضافة مكتبة Aspose.Note for Java إلى مشروعك (Maven/Gradle أو JAR يدوي).  
- معرفة أساسية بصياغة جافا.

## استيراد الحزم

أولاً، استورد الفئات الضرورية من Aspose.Note إلى ملف جافا الخاص بك:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## الخطوة 1: حفظ كـ TIFF باستخدام ضغط TIFF JPEG

فيما يلي الطريقة الكاملة التي تُحمّل ملف OneNote وتُحفظه كـ TIFF باستخدام ضغط JPEG. عدّل قيمة `quality` (0‑100) للتحكم في **جودة صورة TIFF**.

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

- `ImageSaveOptions` تُخبر Aspose.Note بإنتاج ملف TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` يحدد ضغط JPEG.  
- `setQuality(93)` (اختياري) يضبط جودة الصورة؛ القيم الأقل تُنتج ملفات أصغر.

### كيفية حفظ TIFF باستخدام ضغط JPEG في Java
1. عيّن `dataDir` إلى المجلد الذي يحتوي على ملف `.one` الخاص بك.  
2. استدعِ `SaveToTiffUsingJpegCompression()` من الدالة `main` أو الخدمة الخاصة بك.  
3. سيظهر ملف `.tiff` الناتج في نفس الدليل.

## الخطوة 2: حفظ كـ TIFF باستخدام ضغط PackBits

إذا كنت تحتاج إلى خيار بدون فقد، فإن PackBits هو خوارزمية تشغيل‑طول بسيطة تعمل جيدًا للرسومات ذات الألوان الصلبة.

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

- `setTiffCompression(TiffCompression.PackBits)` يغيّر طريقة الضغط.  
- لا حاجة لتعيين جودة لأن PackBits هو ضغط بدون فقد.

## الخطوة 3: حفظ كـ TIFF باستخدام ضغط CCITT Group 3 Fax (TIFF أبيض وأسود)

للمستندات على نمط الفاكس غالبًا ما تحتاج إلى **TIFF أبيض وأسود**. يوفر CCITT Group 3 ضغطًا عاليًا للصور أحادية اللون.

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
- `setTiffCompression(TiffCompression.Ccitt3)` يطبق الضغط المخصص للفاكس.

## المشكلات الشائعة والنصائح

| المشكلة | الحل |
|-------|----------|
| **حجم الملف الناتج أكبر من المتوقع** | حاول تقليل قيمة جودة JPEG أو التحول إلى PackBits إذا كان الفقدان مقبولًا. |
| **الألوان تبدو باهتة** | تأكد من أنك لا تقوم بتعيين `ColorMode.BlackAndWhite` عن غير قصد عندما تحتاج إلى ألوان كاملة. |
| **خطأ تنسيق صورة غير مدعوم** | تحقق من أنك تستخدم نسخة حديثة من Aspose.Note؛ الإصدارات القديمة قد تفتقر إلى بعض تعداد الضغط. |
| **LicenseException أثناء التشغيل** | ثبت ترخيص Aspose.Note صالح (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## الأسئلة المتكررة

**س: هل يمكنني تحويل أنواع مستندات أخرى (مثل PDF, DOCX) إلى TIFF باستخدام هذه الخيارات؟**  
ج: نعم. يركز Aspose.Note على ملفات OneNote، لكن مكتبات Aspose الأخرى (PDF, Words) توفر `ImageSaveOptions` مماثلة لتنسيقاتهم الخاصة.

**س: كيف يختلف ضغط TIFF JPEG عن ملفات JPEG العادية؟**  
ج: تُخزن بيانات الصورة داخل حاوية TIFF، مما يحافظ على البيانات الوصفية ويسمح بوجود صفحات متعددة، بينما يبقى خوارزمية الضغط هي JPEG.

**س: هل يمكن معالجة مجموعة كبيرة من ملفات `.one` دفعيًا؟**  
ج: بالتأكيد. يمكنك حلقة عبر مجلد، استدعاء أي من الطرق الثلاثة لكل ملف، وجمع ملفات TIFF الناتجة.

**س: هل يمكنني التحكم في DPI/دقة TIFF الناتج؟**  
ج: نعم. استخدم `options.setResolution(int dpi)` قبل الحفظ.

**س: هل يدعم Aspose.Note المعالجة غير المتزامنة؟**  
ج: الواجهة البرمجية نفسها متزامنة، لكن يمكنك تغليف الاستدعاءات في `CompletableFuture` أو مجموعات خيوط Java للتنفيذ المتوازي.

## الخاتمة

الآن لديك مجموعة أدوات **تحويل TIFF بجافا** كاملة تتيح لك حفظ مستندات OneNote كملفات TIFF باستخدام ضغط JPEG أو PackBits أو CCITT Group 3 Fax. عدّل الجودة، وضع اللون، والدقة لتلبية متطلبات **جودة صورة TIFF** الخاصة بك، ودمج هذه الطرق في سير عمل دفعي لتحقيق أقصى إنتاجية.

---

**آخر تحديث:** 2025-12-17  
**تم الاختبار مع:** Aspose.Note for Java 23.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}