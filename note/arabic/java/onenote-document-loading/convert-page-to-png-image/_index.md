---
date: 2026-02-05
description: تعلم كيفية تصدير صفحات OneNote وحفظ OneNote كصورة. يوضح هذا الدليل كيفية
  تحويل ملفات .one إلى PNG، وتعيين فهرس الصفحة، وتصدير صورة صفحة OneNote باستخدام
  Aspose.Note للغة Java.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: كيفية تصدير صفحة OneNote إلى صورة PNG في Java باستخدام Aspose.Note
url: /ar/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير صفحة OneNote إلى صورة PNG في Java باستخدام Aspose.Note

## المقدمة

في هذا البرنامج التعليمي ستكتشف **كيفية تصدير صفحة OneNote** إلى صورة PNG باستخدام مكتبة Aspose.Note للغة Java. **كيفية تصدير صفحات OneNote** هي حاجة شائعة عندما تريد مشاركة الملاحظات خارج نظام OneNote، أو تضمينها في تقارير، أو معالجتها بأدوات معالجة الصور. سنستعرض كل ما تحتاجه — من إعداد بيئتك إلى تحديد فهرس الصفحة، تحويل الصفحة، وحفظ النتيجة كملف PNG عالي الجودة. في النهاية، ستكون قادرًا على **حفظ OneNote كصورة** في أي تطبيق Java.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.Note للغة Java.  
- **هل يمكن تصدير صفحة واحدة؟** نعم — استخدم `setPageIndex` لاستهداف الصفحة المحددة.  
- **ما صيغ الصور المدعومة؟** PNG، JPEG، GIF، BMP، TIFF (تم عرض PNG هنا).  
- **هل أحتاج إلى ترخيص؟** يتوفر نسخة تجريبية مجانية؛ الترخيص مطلوب للإنتاج.  
- **كم يستغرق تنفيذ العملية؟** عادةً أقل من 10 دقائق للتحويل الأساسي.  
- **كيف أحول .one إلى png؟** حمّل ملف `.one` باستخدام `Document`، حدّد فهرس الصفحة، واحفظ باستخدام `ImageSaveOptions`.  

## ما هو “تصدير صفحة OneNote”؟
تصدير صفحة OneNote يعني تحويل صفحة محددة داخل مستند `.one` إلى ملف صورة مستقل (PNG في هذه الحالة). هذا مفيد عندما تحتاج إلى **تصدير صورة صفحة OneNote** للمشاركة، أو التضمين، أو التحليل المستند إلى الصور.

## لماذا نستخدم Aspose.Note للغة Java لتحويل OneNote إلى PNG؟
- **بدون اعتماد على Microsoft Office** – يعمل على أي منصة تدعم Java.  
- **تحكم دقيق** – يمكنك اختيار أي صفحة عبر `setPageIndex`.  
- **إخراج عالي الجودة** – PNG يحافظ على الرسومات المتجهة ووضوح النص.  
- **جاهز للمعالجة الجماعية** – سهل التكرار عبر الصفحات للتحويل الضخم، مما يجعل من السهل **تحويل OneNote إلى png** للعديد من الصفحات دفعة واحدة.  

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. **مجموعة تطوير جافا (JDK)** – الإصدار 8 أو أعلى.  
2. **Aspose.Note للغة Java** – حمّل أحدث ملف JAR من [موقع Aspose](https://releases.aspose.com/note/java/).  
3. **مستند OneNote** (`.one`) يحتوي على الصفحة التي تريد تصديرها.

## استيراد الحزم

أولاً، استورد الفئات اللازمة في Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

هذه الاستيرادات تمنحك الوصول إلى واجهة برمجة التطبيقات الأساسية لـ Aspose.Note، بما في ذلك تحميل المستندات وتكوين خيارات حفظ الصورة.

## دليل خطوة بخطوة

### الخطوة 1: تحميل مستند OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

نستخدم فئة `Document` لقراءة ملف OneNote من القرص. كائن `LoadOptions` يتيح لك تخصيص سلوك التحميل إذا لزم الأمر. هذه الخطوة هي الأساس لـ **تحويل .one إلى png**.

### الخطوة 2: تهيئة ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` يخبر Aspose.Note أننا نريد الإخراج بصيغة **PNG**. يمكنك التبديل إلى JPEG أو BMP، إلخ، عن طريق تغيير `SaveFormat`. هذا الكائن يتيح لك أيضًا التحكم في DPI، عمق اللون، وإعدادات الصورة الأخرى.

### الخطوة 3: تحديد فهرس الصفحة (كيفية تحويل صفحة OneNote)

```java
// set page index
opts.setPageIndex(0);
```

طريقة `setPageIndex` تحدد أي صفحة سيتم تصديرها. يبدأ ترقيم الصفحات من **0**، لذا فإن `0` يشير إلى الصفحة الأولى. عدّل هذه القيمة **لتصدير صفحة مختلفة** أو لتكرار عبر الصفحات عندما تحتاج إلى **حفظ OneNote كصورة** لكل منها.

### الخطوة 4: حفظ المستند كملف PNG (حفظ OneNote كـ PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

استدعاء `save` يكتب الصفحة المحددة إلى ملف PNG على القرص. اسم الملف `ConvertSpecificPageToPngImage_out.png` هو مجرد مثال — يمكنك تسميته كما تشاء. هذه الخطوة النهائية **تُصدر صورة صفحة OneNote** جاهزة للاستخدام في تقارير، صفحات ويب، أو معالجة إضافية.

## المشكلات الشائعة والنصائح

- **فهرس الصفحة غير صحيح** – تذكر أن الفهرسة تبدأ من 0. إذا حصلت على صورة فارغة، تحقق من قيمة الفهرس.  
- **عدم وجود ملف JAR الخاص بـ Aspose.Note** – تأكد من أن الـ JAR موجود في مسار الـ classpath؛ وإلا ستظهر لك `ClassNotFoundException`.  
- **صفحات كبيرة** – للصفحات الكبيرة جدًا، فكر في زيادة حجم ذاكرة JVM (`-Xmx`) لتجنب `OutOfMemoryError`.  
- **التحكم في الدقة** – استخدم `opts.setResolution(300)` (أو أي DPI تحتاجه) قبل استدعاء `save` لتحسين وضوح الصورة.  

## الأسئلة المتكررة

### س1: هل يمكنني تحويل عدة صفحات إلى صور PNG دفعة واحدة باستخدام Aspose.Note للغة Java؟
ج1: نعم، يمكنك التكرار عبر صفحات المستند، وتحديث `opts.setPageIndex(i)`، ثم استدعاء `save` لكل تكرار.

### س2: هل يدعم Aspose.Note للغة Java صيغ صور أخرى غير PNG؟
ج2: بالتأكيد. يمكنك ضبط `SaveFormat.Jpeg`، `SaveFormat.Gif`، `SaveFormat.Bmp` أو `SaveFormat.Tiff` في `ImageSaveOptions`.

### س3: هل تتوفر نسخة تجريبية مجانية لـ Aspose.Note للغة Java؟
ج3: نعم، يمكنك تنزيل نسخة تجريبية مجانية من [الموقع](https://releases.aspose.com/).

### س4: هل يمكنني الحصول على مساعدة تقنية إذا واجهت أي مشاكل مع Aspose.Note للغة Java؟
ج4: بالتأكيد، يمكنك طلب الدعم من منتدى مجتمع Aspose [هنا](https://forum.aspose.com/c/note/28).

### س5: أين يمكنني شراء ترخيص لـ Aspose.Note للغة Java؟
ج5: يمكنك شراء الترخيص من [صفحة الشراء](https://purchase.aspose.com/buy).

### س6: كيف أقوم بتصدير صفحة تحتوي على صور مدمجة؟
ج6: يتم تلقائيًا عرض الصور المدمجة في ناتج PNG؛ لا تحتاج إلى كود إضافي.

### س7: هل يمكنني ضبط DPI أو دقة الصورة؟
ج7: نعم، استخدم `opts.setResolution(int dpi)` قبل استدعاء `save` للتحكم في جودة الإخراج.

---

**آخر تحديث:** 2026-02-05  
**تم الاختبار مع:** Aspose.Note للغة Java 24.11 (الأحدث)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}