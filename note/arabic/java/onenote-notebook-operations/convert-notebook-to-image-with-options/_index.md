---
date: 2025-12-28
description: تعلم كيفية **تحويل OneNote إلى صورة** وتعيين دقة الصورة في Java باستخدام
  Aspose.Note. يوضح هذا الدليل خطوة بخطوة أيضًا كيفية تصدير ملفات PNG من OneNote.
linktitle: Convert OneNote to Image with Options - Aspose.Note
second_title: Aspose.Note Java API
title: تحويل OneNote إلى صورة مع خيارات - Aspose.Note
url: /ar/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل OneNote إلى صورة مع خيارات - Aspose.Note

## المقدمة

في هذا الدرس، ستتعلم كيفية **تحويل OneNote إلى صورة** باستخدام مجموعة متنوعة من الخيارات عبر Aspose.Note للغة Java. سواء كنت تحتاج إلى صورة PNG عالية الدقة للتقارير أو صورة مصغرة JPEG سريعة، فإن الخطوات أدناه توضح لك بالضبط كيفية تحقيق ذلك ودمج العملية في تطبيقات Java الخاصة بك.

## إجابات سريعة
- **ماذا يعني “تحويل OneNote إلى صورة”؟** إنه يحول دفتر OneNote كامل إلى ملفات صورة نقطية (PNG، JPEG، إلخ).
- **ما هو التنسيق الموصى به لجودة غير مضغوطة؟** PNG، لأنه يحافظ على جميع التفاصيل دون تشوهات الضغط.
- **كيف يمكنني ضبط دقة الصورة في Java؟** استخدم `ImageSaveOptions.setResolution(int dpi)` عبر `NotebookImageSaveOptions`.
- **هل يمكنني تصدير دفتر OneNote كملف PNG في خطوة واحدة؟** نعم، يوفر Aspose.Note استدعاء `save` واحد مع الخيارات المناسبة.
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يتطلب الترخيص التجاري للاستخدام في الإنتاج؛ يتوفر نسخة تجريبية مجانية للتقييم.

## ما هو “تحويل OneNote إلى صورة”؟
تحويل دفتر OneNote إلى صورة يعني تحويل كل صفحة من الدفتر إلى ملف bitmap. هذا مفيد لإنشاء معاينات ثابتة، أرشفة المحتوى، أو تضمين صفحات الدفتر في تقارير حيث لا يتم دعم تنسيق OneNote الأصلي.

## لماذا تستخدم Aspose.Note للغة Java؟
- **تحكم كامل** في تنسيق الإخراج، الدقة، وعمق اللون.  
- **بدون اعتماد على Microsoft Office** – يعمل على أي بيئة Java من جانب الخادم.  
- **يدعم دفاتر معقدة** تحتوي على ملفات مدمجة، حبر، ونص غني.

## المتطلبات المسبقة

1. **Java Development Kit (JDK)** – الإصدار 8 أو أعلى.  
2. **Aspose.Note للغة Java ملفات JAR** – قم بتحميل أحدث مكتبة من [هنا](https://releases.aspose.com/note/java/) وأضفها إلى مسار الفئة (classpath) في مشروعك.  

## استيراد الحزم

أولاً، استورد الفئات التي سنحتاجها لتحميل الدفتر وتكوين إخراج الصورة.

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## الخطوة 1: تحميل الدفتر

حمّل دفتر OneNote الذي تريد تحويله. استبدل المسار بموقع ملف `.onetoc2` الخاص بك.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## الخطوة 2: ضبط خيارات الحفظ (كيفية **ضبط دقة الصورة في Java**)

أنشئ مثيلًا من `NotebookImageSaveOptions`، اختر تنسيق الإخراج، وحدد الدقة المطلوبة. في هذا المثال نستخدم PNG بدقة 400 dpi.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

> **نصيحة احترافية:** للحصول على معالجة أسرع للدفاتر الكبيرة، قلل الدقة (مثلاً 150 dpi). زدها للرسومات الجاهزة للطباعة.

## الخطوة 3: حفظ الدفتر كصورة (كيفية **تصدير OneNote PNG**)

حدد اسم ملف الإخراج واستدعِ `save`. تُطبق نفس الخيارات على كل صفحة في الدفتر.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

سيولد الكود أعلاه ملف PNG (أو سلسلة من ملفات PNG، واحدة لكل صفحة) بالدقة التي حددتها.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **OutOfMemoryError** على دفاتر كبيرة | زيادة حجم الذاكرة المخصصة للـ JVM (`-Xmx2g`) أو تقليل الدقة. |
| **صفحات فارغة في الإخراج** | تأكد من أن الدفتر غير محمي بكلمة مرور؛ استخدم `Notebook.load(path, password)` إذا لزم الأمر. |
| **تنسيق صورة غير مدعوم** | استخدم فقط `SaveFormat.Png`، `SaveFormat.Jpeg`، أو `SaveFormat.Bmp` – الصيغ الأخرى غير مدعومة لتصدير الدفتر. |

## الأسئلة المتكررة

**س: هل يمكن لـ Aspose.Note التعامل مع ملفات OneNote المعقدة؟**  
ج: نعم، يعالج الدفاتر التي تحتوي على ملفات مدمجة، تعليقات حبر، وتنسيق غني بكفاءة.

**س: هل Aspose.Note للغة Java سهل التكامل مع المشاريع الحالية؟**  
ج: بالتأكيد. الـ API بسيط، وكل ما عليك هو إضافة ملف JAR إلى مسار الفئة (classpath).

**س: هل يمكنني تخصيص إخراج الصورة عند تحويل دفتر؟**  
ج: نعم. يمكنك ضبط الدقة، التنسيق، وحتى عمق اللون عبر `ImageSaveOptions`.

**س: هل يقدم Aspose.Note دعمًا للمطورين؟**  
ج: نعم. توفر Aspose وثائق شاملة، منتديات، وقنوات دعم سريعة الاستجابة.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Note للغة Java؟**  
ج: نعم، يمكنك تحميل نسخة تجريبية من [هنا](https://releases.aspose.com/).

---

**آخر تحديث:** 2025-12-28  
**تم الاختبار مع:** Aspose.Note 24.11 للغة Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}