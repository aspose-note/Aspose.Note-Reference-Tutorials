---
date: 2026-03-29
description: تحويل دفاتر OneNote إلى PDF مع خيارات، حفظ الدفتر كملف PDF، وإضافة رأس
  وتذييل PDF باستخدام Aspose.Note للغة Java.
linktitle: Convert Notebook to PDF with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: تحويل OneNote إلى PDF مع خيارات - Aspose.Note
url: /ar/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل OneNote إلى PDF مع خيارات باستخدام Aspose.Note

## المقدمة

في هذا الدرس ستتعلم كيفية **convert onenote to pdf** مع تحكم كامل في الناتج. تجعل Aspose.Note for Java عملية تصدير دفاتر OneNote إلى PDF سهلة، مما يتيح لك **save notebook as pdf** مع تخصيص رؤوس وتذييلات الصفحات وسلوك تقسيم الصفحات. سواء كنت بحاجة إلى إنشاء تقارير، أرشفة ملاحظات الاجتماعات، أو مشاركة المحتوى مع المستخدمين الذين لا يمتلكون OneNote، فإن هذا الدليل يرافقك في كل خطوة.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع التحويل؟** Aspose.Note for Java.
- **هل يمكنني إضافة رأس أو تذييل إلى PDF؟** نعم – استخدم خيارات حفظ PDF لإدراج رؤوس/تذييلات مخصصة.
- **هل أحتاج إلى ترخيص للإنتاج؟** الترخيص التجاري مطلوب للاستخدام غير التجريبي.
- **ما إصدارات Java المدعومة؟** Java 8 وما بعدها.
- **كم يستغرق التحويل من الوقت؟** عادةً بضع ثوانٍ للدفاتر ذات الحجم المتوسط.

## ما هو “convert onenote to pdf”؟

تحويل OneNote إلى PDF يعني أخذ دفتر OneNote (ملف *.onetoc2*) وتحويل كل صفحة إلى صفحة PDF. يحافظ PDF الناتج على النصوص والصور والتخطيط، مما يجعله قابلاً للعرض على أي جهاز دون الحاجة إلى OneNote.

## لماذا نستخدم Aspose.Note لتصدير دفتر onenote إلى pdf؟

- **لا يتطلب تثبيت Office** – الـ API يعمل بشكل مستقل.
- **تحكم دقيق** – يمكنك ضبط خوارزميات تقسيم الصفحات، تضمين الخطوط، وإضافة رؤوس/تذييلات.
- **دقة عالية** – يتم الحفاظ على المظهر البصري للدفتر الأصلي.
- **متعدد المنصات** – يعمل على Windows وLinux وmacOS مع أي بيئة تشغيل Java.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من توفر المتطلبات التالية:

1. Java Development Kit (JDK) – تم تثبيت JDK 8 أو أحدث.
2. Aspose.Note for Java – قم بتنزيله وتثبيته من [download link](https://releases.aspose.com/note/java/).
3. IDE (بيئة التطوير المتكاملة) – IntelliJ IDEA أو Eclipse أو NetBeans هي خيارات شائعة.

## استيراد الحزم

أولاً، تحتاج إلى استيراد الحزم الضرورية إلى مشروع Java الخاص بك. توفر هذه الحزم الفئات والطرق المطلوبة للعمل مع مستندات OneNote.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## الخطوة 1: تحميل دفتر OneNote

لـ **convert onenote to pdf**، تحتاج أولاً إلى تحميل دفتر OneNote. تأكد من تحديد مسار ملف الدفتر بشكل صحيح.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## الخطوة 2: تحديد خيارات حفظ PDF

توفر Aspose.Note خيارات متعددة لتخصيص مخرجات PDF. يمكنك تحديد خيارات مثل خوارزميات تقسيم الصفحات، إعدادات الرأس/التذييل، وأكثر.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## الخطوة 3: حفظ الدفتر كملف PDF

بعد تحميل الدفتر وتحديد خيارات الحفظ، حان الوقت لـ **save the notebook as pdf**.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|----------|
| PDF يفتقد الصور | الصور مخزنة ككائنات مدمجة ولم يتم تحميلها | تأكد من أن ملف الدفتر وجميع الموارد المرتبطة موجودة في نفس الدليل قبل التحميل. |
| الرأس/التذييل لا يظهر | لم يتم تعيين خيارات الرأس/التذييل في `PdfSaveOptions` | استخدم `documentSaveOptions.setHeaderFooter()` لتحديد المحتوى قبل الحفظ. |
| خطأ الذاكرة في دفاتر كبيرة | تم تحميل الدفتر بالكامل في الذاكرة | قم بمعالجة الدفتر على أقسام أو زد حجم ذاكرة JVM (`-Xmx2g`). |

## الأسئلة المتكررة

### س1: هل يمكنني تخصيص مظهر مخرجات PDF؟

ج1: نعم، توفر Aspose.Note خيارات متعددة لتخصيص مخرجات PDF، بما في ذلك إعدادات الرأس/التذييل، خوارزميات تقسيم الصفحات، وأكثر.

### س2: هل Aspose.Note متوافق مع جميع إصدارات OneNote؟

ج2: يدعم Aspose.Note Microsoft OneNote 2010 والإصدارات الأحدث.

### س3: هل تقدم Aspose.Note نسخة تجريبية مجانية؟

ج3: نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.Note من [here](https://releases.aspose.com/).

### س4: أين يمكنني العثور على وثائق Aspose.Note؟

ج4: يمكنك العثور على وثائق شاملة لـ Aspose.Note [here](https://reference.aspose.com/note/java/).

### س5: كيف يمكنني الحصول على دعم Aspose.Note؟

ج5: لأي مساعدة تقنية أو استفسارات، يمكنك زيارة منتدى دعم Aspose.Note [here](https://forum.aspose.com/c/note/28).

## أسئلة متكررة إضافية

**س: كيف أضيف رأس أو تذييل PDF مخصص؟**  
ج: أنشئ كائن `PdfHeaderFooterOptions`، قم بتكوين النص أو الصور، وعيّنها إلى `documentSaveOptions.setHeaderFooterOptions()` قبل استدعاء `save`.

**س: هل يمكنني تصدير أقسام محددة فقط من الدفتر؟**  
ج: نعم – قم بتحميل الدفتر، استخرج كائنات `Section` المطلوبة، واستدعِ `section.save()` مع نفس خيارات PDF.

**س: هل يمكن تشفير PDF المُولد؟**  
ج: بالتأكيد. استخدم `documentSaveOptions.setEncryptionPassword("yourPassword")` لحماية PDF.

**س: ما هي الاعتبارات المتعلقة بالأداء التي يجب أن أضعها في الاعتبار؟**  
ج: بالنسبة للدفاتر الكبيرة جدًا، فكر في تدفق الإخراج إلى `FileOutputStream` وزيادة حجم ذاكرة JVM إذا واجهت `OutOfMemoryError`.

---

**آخر تحديث:** 2026-03-29  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}