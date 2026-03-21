---
date: 2026-03-21
description: تعلم كيفية تسطيح الدفتر عن طريق تحويل OneNote إلى PNG باستخدام Aspose.Note
  للغة Java. يغطي هذا الدليل ضبط دقة الصورة، حفظ OneNote كصورة، وتسطية الدفاتر بكفاءة.
linktitle: How to Flatten Notebook – Convert OneNote to PNG
second_title: Aspose.Note Java API
title: كيفية تسطيح الدفتر – تحويل OneNote إلى PNG
url: /ar/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تسطيح دفتر الملاحظات – تحويل OneNote إلى PNG

## المقدمة

في هذا البرنامج التعليمي ستكتشف **كيفية تسطيح دفتر الملاحظات** عن طريق تحويل دفتر OneNote إلى صورة PNG عالية الجودة باستخدام Aspose.Note for Java. سواء كنت بحاجة إلى تضمين لقطة من دفتر الملاحظات في تقرير، أو مشاركة عرض للقراءة فقط مع الزملاء، أو أرشفة صورة متوافقة، فإن هذا الدليل خطوة بخطوة يوضح لك بالضبط كيفية حفظ OneNote كصورة مع التحكم في الدقة.

## إجابات سريعة
- **ماذا يعني “تسطيح دفتر الملاحظات”؟** يدمج جميع عناصر الصفحة في صورة نقطية واحدة.  
- **ما هو التنسيق المستخدم؟** PNG هو الافتراضي، ويعطي جودة بدون فقد.  
- **هل يمكنني تغيير DPI؟** نعم، استخدم `setResolution` على `ImageSaveOptions`.  
- **هل أحتاج إلى ترخيص؟** الإصدار التجريبي المجاني يكفي للتقييم؛ يلزم ترخيص تجاري للإنتاج.  
- **هل هذا مدعوم على جميع أنظمة التشغيل؟** واجهة برمجة تطبيقات Java تعمل في أي بيئة تدعم Java.

## ما هو تحويل OneNote إلى PNG؟

تحويل OneNote إلى PNG يُنشئ تمثيلًا نقطيًا لكل صفحة في دفتر الملاحظات، مع الحفاظ على النصوص والرسومات والكائنات المدمجة في ملف صورة واحد. هذا مفيد بشكل خاص للتوثيق، العروض التقديمية، أو أرشفة الامتثال.

## لماذا تحويل OneNote إلى PNG باستخدام Aspose.Note؟

- **دقة كاملة** – جميع العناصر البصرية تُحافظ عليها.  
- **إخراج بملف واحد** – لا حاجة لإدارة ملفات صفحات متعددة.  
- **دقة قابلة للتخصيص** – ضبط DPI لتلبية متطلبات الجودة.  
- **دون الحاجة لتثبيت Office** – يعمل بشكل مستقل تمامًا عن Microsoft OneNote.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. مجموعة تطوير جافا (JDK) مثبتة على نظامك.  
2. مكتبة Aspose.Note for Java محملة ومُعدّة في مشروع جافا الخاص بك. يمكنك تنزيل المكتبة من [هنا](https://releases.aspose.com/note/java/).  
3. معرفة أساسية ببرمجة جافا.

## استيراد الحزم

لبدء العمل، تحتاج إلى استيراد الحزم الضرورية من Aspose.Note for Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## دليل خطوة بخطوة

### الخطوة 1: إعداد دليل المستند

أولاً، عرّف الدليل الذي يتواجد فيه ملف دفتر الملاحظات:

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار إلى ملف دفتر الملاحظات الخاص بك.

### الخطوة 2: تحميل دفتر الملاحظات

بعد ذلك، حمّل ملف دفتر الملاحظات باستخدام الفئة `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

تأكد من استبدال `"test.onetoc2"` باسم ملف دفتر الملاحظات الخاص بك.

### الخطوة 3: إعداد خيارات حفظ الصورة (set image resolution java)

الآن، قم بإعداد الخيارات لحفظ دفتر الملاحظات كصورة. سنحدد تنسيق الحفظ كـ PNG ونضبط الدقة إلى 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

يمكنك تعديل الدقة وفقًا لمتطلباتك. هنا حيث **تضبط دقة الصورة** للتحكم في جودة الناتج.

### الخطوة 4: تسطيح دفتر الملاحظات (how to flatten notebook)

لضمان أن جميع العناصر تُسطّح في صورة واحدة، اضبط خيار `flatten` إلى `true`:

```java
saveOptions.setFlatten(true);
```

ضبط `flatten` إلى `true` يضمن أن PNG الناتج يحافظ على التخطيط الدقيق لدفتر الملاحظات.

### الخطوة 5: حفظ الصورة (save onenote as image)

أخيرًا، احفظ دفتر الملاحظات كصورة مسطحة:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

استبدل `"ExportImageasFlattenedNotebook_out.png"` باسم ملف الإخراج الذي تريده. هذه الخطوة **تحفظ OneNote كصورة** يمكنك مشاركتها أو تضمينها في أي مكان.

## حالات الاستخدام الشائعة

- **التوثيق:** تضمين صورة دفتر الملاحظات في الأدلة التقنية أو كتيبات المستخدم.  
- **العروض التقديمية:** استخدام شريحة PNG عالية الدقة في PowerPoint دون القلق بشأن توافق الخطوط أو الكائنات.  
- **الأرشفة:** تخزين لقطة للقراءة فقط من دفتر الملاحظات لتدقيق الامتثال.

## نصائح استكشاف الأخطاء وإصلاحها

- **الملف غير موجود:** تحقق مرة أخرى من مسار `dataDir` وتأكد من وجود ملف `.onetoc2`.  
- **صورة منخفضة الجودة:** زد DPI بتغيير `documentSaveOptions.setResolution(600);`.  
- **عناصر مفقودة:** تأكد من تمكين `saveOptions.setFlatten(true);`؛ وإلا قد تظل بعض الطبقات منفصلة.

## الأسئلة المتكررة

**س1: هل يمكنني تعديل دقة الصورة الناتجة؟**  
ج1: نعم، يمكنك تعديل الدقة وفقًا لمتطلباتك عن طريق تعديل معامل طريقة `setResolution`.

**س2: هل يدعم Aspose.Note صيغ صور أخرى للتصدير؟**  
ج2: نعم، يدعم Aspose.Note صيغ صور متعددة مثل PNG، JPEG، BMP، وغيرها لتصدير دفاتر الملاحظات.

**س3: هل يمكنني تخصيص صورة الإخراج أكثر؟**  
ج3: نعم، يوفر Aspose.Note خيارات واسعة لتخصيص صورة الإخراج، بما في ذلك حجم الصفحة، الاتجاه، وإعدادات الجودة.

**س4: هل هناك نسخة تجريبية متاحة لـ Aspose.Note for Java؟**  
ج4: نعم، يمكنك الحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س5: أين يمكنني العثور على الدعم لـ Aspose.Note for Java؟**  
ج5: يمكنك العثور على الدعم والموارد في منتدى Aspose.Note [هنا](https://forum.aspose.com/c/note/28).

---

**آخر تحديث:** 2026-03-21  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}