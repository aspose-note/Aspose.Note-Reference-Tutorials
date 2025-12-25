---
date: 2025-12-25
description: تعلم كيفية تحويل OneNote إلى PNG باستخدام Aspose.Note للغة Java. يوضح
  هذا الدليل كيفية ضبط دقة الصورة، وتسطح دفتر الملاحظات، وحفظ OneNote كصورة بكفاءة.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: كيفية تحويل OneNote إلى PNG – تحويل دفتر الملاحظات إلى صورة باستخدام Aspose.Note
url: /ar/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل دفتر الملاحظات إلى صورة مسطحة في OneNote - Aspose.Note

## المقدمة

في هذا البرنامج التعليمي ستكتشف كيفية **تحويل OneNote إلى PNG** عن طريق تحويل دفتر ملاحظات كامل إلى صورة مسطحة واحدة باستخدام Aspose.Note للغة Java. هذه الطريقة مثالية عندما تحتاج إلى مشاركة دفتر الملاحظات كصورة ثابتة، أو تضمينه في تقارير، أو أرشفته دون فقدان أي تفاصيل بصرية.

## إجابات سريعة
- **ماذا يعني “flatten notebook”؟** يدمج جميع عناصر الصفحة في صورة نقطية واحدة.  
- **ما هو التنسيق المستخدم؟** PNG هو الافتراضي، ويعطي جودة غير مضغوطة.  
- **هل يمكنني تغيير DPI؟** نعم، استخدم `setResolution` على `ImageSaveOptions`.  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتقييم؛ يتطلب الترخيص التجاري للإنتاج.  
- **هل هذا مدعوم على جميع أنظمة التشغيل؟** API جافا يعمل في أي بيئة تدعم جافا.

## ما هو تحويل OneNote إلى PNG؟

تحويل OneNote إلى PNG ينشئ تمثيلًا نقطيًا لكل صفحة في دفتر الملاحظات، مع الحفاظ على النصوص والرسومات والكائنات المدمجة في ملف صورة واحد. هذا مفيد بشكل خاص للتوثيق، العروض التقديمية، أو أرشفة الامتثال.

## لماذا تحويل OneNote إلى PNG باستخدام Aspose.Note؟

- **دقة كاملة** – جميع العناصر البصرية تُحفظ.  
- **إخراج ملف واحد** – لا حاجة لإدارة ملفات صفحات متعددة.  
- **دقة قابلة للتخصيص** – ضبط DPI لتلبية متطلبات الجودة.  
- **بدون تثبيت Office** – يعمل بشكل مستقل تمامًا عن Microsoft OneNote.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

1. مجموعة تطوير جافا (JDK) مثبتة على نظامك.  
2. مكتبة Aspose.Note للغة Java تم تحميلها وإعدادها في مشروع جافا الخاص بك. يمكنك تحميل المكتبة من [هنا](https://releases.aspose.com/note/java/).  
3. معرفة أساسية ببرمجة جافا.

## استيراد الحزم

لبدء العمل، تحتاج إلى استيراد الحزم الضرورية من Aspose.Note للغة Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## الخطوة 1: إعداد دليل المستند

أولاً، عرّف الدليل الذي يوجد فيه ملف دفتر الملاحظات الخاص بك:

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار إلى ملف دفتر الملاحظات.

## الخطوة 2: تحميل دفتر الملاحظات

بعد ذلك، حمّل ملف دفتر الملاحظات باستخدام الفئة `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

تأكد من استبدال `"test.onetoc2"` باسم ملف دفتر الملاحظات الخاص بك.

## الخطوة 3: إعداد خيارات حفظ الصورة

الآن، قم بإعداد الخيارات لحفظ دفتر الملاحظات كصورة. سنحدد تنسيق الحفظ كـ PNG ونضبط الدقة إلى 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

يمكنك تعديل الدقة وفقًا لمتطلباتك. هنا حيث **تضبط دقة الصورة** للتحكم في جودة الإخراج.

## الخطوة 4: تسطيح دفتر الملاحظات

للتأكد من أن جميع العناصر تُسطّح في صورة واحدة، اضبط خيار `flatten` إلى `true`:

```java
saveOptions.setFlatten(true);
```

ضبط `flatten` إلى `true` يضمن أن PNG الناتج يحافظ على التخطيط الدقيق لدفتر الملاحظات الخاص بك.

## الخطوة 5: حفظ الصورة

أخيرًا، احفظ دفتر الملاحظات كصورة مسطحة:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

استبدل `"ExportImageasFlattenedNotebook_out.png"` باسم ملف الإخراج الذي تريده. هذه الخطوة **تحفظ OneNote كصورة** يمكنك مشاركتها أو تضمينها في أي مكان.

## حالات الاستخدام الشائعة

- **التوثيق:** تضمين صورة دفتر الملاحظات في الأدلة التقنية أو كتيبات المستخدم.  
- **العروض التقديمية:** استخدام شريحة PNG عالية الدقة في PowerPoint دون القلق بشأن توافق الخطوط أو الكائنات.  
- **الأرشفة:** تخزين لقطة قراءة‑فقط لدفتر الملاحظات لأغراض تدقيق الامتثال.

## نصائح استكشاف الأخطاء وإصلاحها

- **الملف غير موجود:** تحقق مرة أخرى من مسار `dataDir` وتأكد من وجود ملف `.onetoc2`.  
- **صورة ذات جودة منخفضة:** زد DPI بتغيير `documentSaveOptions.setResolution(600);`.  
- **عناصر مفقودة:** تأكد من تمكين `saveOptions.setFlatten(true);`؛ وإلا قد تظل بعض الطبقات منفصلة.

## الأسئلة المتكررة

**س1: هل يمكنني تعديل دقة الصورة الناتجة؟**  
ج1: نعم، يمكنك تعديل الدقة وفقًا لمتطلباتك عن طريق تعديل معلمة طريقة `setResolution`.

**س2: هل يدعم Aspose.Note صيغ صور أخرى للتصدير؟**  
ج2: نعم، يدعم Aspose.Note صيغ صور متعددة مثل PNG، JPEG، BMP، وغيرها لتصدير دفاتر الملاحظات.

**س3: هل يمكنني تخصيص صورة الإخراج أكثر؟**  
ج3: نعم، يوفر Aspose.Note خيارات واسعة لتخصيص صورة الإخراج، بما في ذلك حجم الصفحة، الاتجاه، وإعدادات الجودة.

**س4: هل هناك نسخة تجريبية متاحة لـ Aspose.Note للغة Java؟**  
ج4: نعم، يمكنك الحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س5: أين يمكنني العثور على الدعم لـ Aspose.Note للغة Java؟**  
ج5: يمكنك العثور على الدعم والموارد في منتدى Aspose.Note [هنا](https://forum.aspose.com/c/note/28).

---

**آخر تحديث:** 2025-12-25  
**تم الاختبار مع:** Aspose.Note للغة Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}