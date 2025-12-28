---
date: 2025-12-28
description: تعلم كيفية تصدير OneNote إلى PDF مع تحكم كامل باستخدام Aspose.Note للغة
  Java. يتضمن خيارات تصدير دفتر ملاحظات OneNote إلى PDF ودليل تحويل دفتر الملاحظات
  إلى PDF باستخدام Java.
linktitle: How to Export OneNote to PDF with Options – Convert Notebook to PDF using
  Aspose.Note
second_title: Aspose.Note Java API
title: كيفية تصدير OneNote إلى PDF مع خيارات – تحويل دفتر الملاحظات إلى PDF باستخدام
  Aspose.Note
url: /ar/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تصدير OneNote إلى PDF مع خيارات – Aspose.Note Java API

## المقدمة

في هذا البرنامج التعليمي، ستتعلم **كيفية تصدير OneNote إلى PDF** مع خيارات قابلة للتخصيص باستخدام Aspose.Note للـ Java. تحويل دفتر ملاحظات OneNote إلى PDF هو طلب شائع—سواء كنت بحاجة لمشاركة ملاحظات الاجتماعات، أرشفة الوثائق، أو إنشاء تقارير قابلة للطباعة. مع Aspose.Note، العملية بسيطة، قابلة للبرمجة بالكامل، وتمنحك تحكمًا دقيقًا في ملف PDF الناتج.

## إجابات سريعة
- **ماذا يفعل الـ API؟** يقوم بتحميل دفتر ملاحظات OneNote ويحفظه كملف PDF مع إعدادات اختيارية.  
- **ما اللغة المستخدمة؟** Java – مثالية لتطبيقات الخادم أو سطح المكتب.  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **هل يمكنني التحكم في تخطيط الصفحة؟** نعم، يمكنك ضبط خوارزميات تقسيم الصفحات، الرؤوس، التذييلات، وأكثر.  
- **هل عينة الشيفرة قابلة للتنفيذ؟** بالتأكيد – فقط استبدل مسار العنصر النائب بموقع دفتر الملاحظات الخاص بك.

## ما هو “كيفية تصدير OneNote إلى PDF”؟

تصدير OneNote إلى PDF يعني تحويل دفتر ملاحظات OneNote الأصلي (`*.onetoc2` والملفات المرتبطة بالأقسام) إلى مستند PDF ثابت ومحمول. يحافظ هذا التحويل على التنسيق، الصور، والكائنات المدمجة مع جعل المحتوى قابلًا للعرض على أي جهاز دون الحاجة إلى OneNote.

## لماذا نستخدم Aspose.Note للـ Java؟

- **بدون اعتماد على Microsoft Office** – يعمل على أي منصة تدعم Java.  
- **خيارات PDF غنية** – التحكم في تقسيم الصفحات، الرؤوس/التذييلات، ومعالجة الكائنات.  
- **دقة عالية** – مخرجات PDF تتطابق إلى حد كبير مع مظهر OneNote الأصلي.  
- **قابلية التوسع** – مناسب لمعالجة دفاتر ملاحظات بالآلاف دفعة واحدة.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

1. **مجموعة تطوير جافا (JDK)** – الإصدار 8 أو أعلى.  
2. **Aspose.Note للـ Java** – حمّله من [رابط التحميل](https://releases.aspose.com/note/java/).  
3. **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA، Eclipse، أو NetBeans (حسب اختيارك).  
4. **دفتر ملاحظات OneNote** تريد تحويله (مثال: `Notizbuch öffnen.onetoc2`).

## استيراد الحزم

أولاً، استورد الفئات التي توفر معالجة الدفتر وحفظ PDF.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## الخطوة 1: تحميل دفتر ملاحظات OneNote

حمّل ملف دفتر الملاحظات من القرص. استبدل `Your Document Directory` بالمجلد الفعلي الذي يحتوي على ملف `.onetoc2` الخاص بك.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## الخطوة 2: تحديد خيارات حفظ PDF

هنا تقوم بتعريف كيفية إنشاء ملف PDF. المثال يحدد خوارزمية تقسيم الصفحات التي تحافظ على الكائنات الصلبة معًا، وهو مفيد عندما تكون لديك مخططات أو جداول يجب أن تبقى في نفس الصفحة.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## الخطوة 3: حفظ دفتر الملاحظات كملف PDF

أخيرًا، اكتب دفتر الملاحظات كملف PDF. يمكن أن يكون مسار الإخراج أي موقع تفضله.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|---------|-------|------|
| **الملف غير موجود** | مسار `dataDir` أو اسم الملف غير صحيح. | تحقق من المسار وتأكد من وجود ملف دفتر الملاحظات. |
| **الخطوط مفقودة** | يحتاج عرض PDF إلى نفس الخطوط المستخدمة في OneNote. | ثبّت الخطوط المطلوبة على الخادم أو دمجها عبر خيارات Aspose الإضافية. |
| **دفاتر ملاحظات كبيرة تسبب OutOfMemoryError** | يتم تحميل دفتر الملاحظات بالكامل في الذاكرة. | عالج الأقسام بشكل منفصل أو زد حجم ذاكرة JVM (`-Xmx`). |

## الخلاصة

استعرضنا **كيفية تصدير OneNote إلى PDF** باستخدام Aspose.Note للـ Java، بدءًا من تحميل دفتر الملاحظات، ضبط خيارات PDF، وحفظ النتيجة. باتباع هذه الخطوات، يمكنك دمج تحويل دفتر الملاحظات إلى PDF في أي تطبيق Java، سواء كان أداة سطح مكتب، خدمة ويب، أو خلفية معالجة دفعات.

## الأسئلة المتكررة

### س1: هل يمكنني تخصيص مظهر ملف PDF الناتج؟

ج1: نعم، يوفر Aspose.Note خيارات متعددة لتخصيص مخرجات PDF، بما في ذلك إعدادات الرأس/التذييل، خوارزميات تقسيم الصفحات، وأكثر.

### س2: هل Aspose.Note متوافق مع جميع إصدارات OneNote؟

ج2: يدعم Aspose.Note Microsoft OneNote 2010 والإصدارات الأحدث.

### س3: هل يقدم Aspose.Note نسخة تجريبية مجانية؟

ج3: نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.Note من [هنا](https://releases.aspose.com/).

### س4: أين يمكنني العثور على وثائق Aspose.Note؟

ج4: يمكنك العثور على وثائق شاملة لـ Aspose.Note [هنا](https://reference.aspose.com/note/java/).

### س5: كيف يمكنني الحصول على دعم لـ Aspose.Note؟

ج5: لأي مساعدة تقنية أو استفسارات، يمكنك زيارة منتدى دعم Aspose.Note [هنا](https://forum.aspose.com/c/note/28).

## أسئلة متكررة إضافية

**س: كيف أصدر دفتر ملاحظات OneNote إلى PDF دون فقدان الصور؟**  
ج: تأكد من ضبط `KeepSolidObjectsAlgorithm` كما هو موضح، وتأكد من أن ملفات الصور الخاصة بدفتر الملاحظات متاحة في نفس الدليل.

**س: هل يمكنني تحويل عدة دفاتر ملاحظات دفعة واحدة؟**  
ج: نعم. قم بتكرار قائمة مسارات دفاتر الملاحظات، أنشئ كائن `Notebook` لكل منها، طبّق نفس `NotebookPdfSaveOptions`، ثم استدعِ `save()`.

**س: هل يمكن تعيين بيانات تعريف PDF (المؤلف، العنوان) أثناء التحويل؟**  
ج: استخدم `PdfSaveOptions.setMetadata()` لتحديد المؤلف، العنوان، الموضوع، والكلمات المفتاحية قبل الحفظ.

**س: هل يدعم الـ API ملفات PDF محمية بكلمة مرور؟**  
ج: يمكنك تعيين كلمة مرور على `PdfSaveOptions` عبر `setEncryptionPassword()` بعد تكوين الخيارات الأخرى.

**س: ما نسخة Aspose.Note المستخدمة في هذا البرنامج التعليمي؟**  
ج: تم اختبار الشيفرة مع Aspose.Note للـ Java الإصدار 23.12.

---

**آخر تحديث:** 2025-12-28  
**تم الاختبار مع:** Aspose.Note للـ Java 23.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}