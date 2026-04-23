---
date: 2026-02-15
description: تعلم كيفية تحويل OneNote إلى PDF وحفظ OneNote كملف PDF باستخدام Aspose.Note
  للغة Java. بسط مهام تحويل المستندات الخاصة بك باستخدام PdfSaveOptions.
linktitle: Load OneNote Document into Aspose.Note using PdfSaveOptions
second_title: Aspose.Note Java API
title: تحويل OneNote إلى PDF باستخدام Aspose.Note وخيارات حفظ PDF
url: /ar/java/onenote-document-loading/load-pdf-save-options/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل OneNote إلى PDF باستخدام Aspose.Note و PdfSaveOptions

## المقدمة

في هذا الدليل الشامل، ستتعلم **كيفية تحويل OneNote إلى PDF** باستخدام Aspose.Note للـ Java. سنستعرض خطوات تحميل ملف OneNote، ضبط عملية التحويل، وأخيرًا حفظ النتيجة كملف PDF. في نهاية البرنامج التعليمي ستكون قادرًا على دمج هذه العملية في تطبيقات Java الخاصة بك.

## إجابات سريعة
- **ما المكتبة التي تتولى التحويل؟** Aspose.Note للـ Java مع `PdfSaveOptions`.
- **كم يستغرق تنفيذ الأساسيات؟** حوالي 5‑10 دقائق للحصول على نموذج عمل.
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم، يلزم الحصول على ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.
- **هل يمكنني تخصيص مخرجات PDF؟** بالتأكيد – `PdfSaveOptions` يتيح لك ضبط حجم الصفحة، الهوامش، وأكثر.
- **ما صيغ OneNote المدعومة؟** كلا الملفين `.one` و `.onepkg` مدعومان.

## لماذا تحويل OneNote إلى PDF؟

تحويل دفاتر OneNote إلى PDF يمنحك صيغة يمكن عرضها وطبعها وأرشفتها عالميًا. ملفات PDF مثالية للمشاركة مع أصحاب المصلحة الذين لا يمتلكون OneNote، وللتوافق مع سياسات الاحتفاظ بالوثائق، ولدمج الملاحظات في أنظمة تقارير أكبر.

## المتطلبات المسبقة

قبل البدء، تأكد من توفر ما يلي:

### 1. بيئة تطوير Java
إصدار JDK حديث (يوصى بـ Java 17 أو أحدث). يمكنك تحميله من موقع Oracle أو اعتماد OpenJDK.

### 2. مكتبة Aspose.Note للـ Java
احصل على أحدث حزمة Aspose.Note للـ Java من [صفحة التحميل الرسمية](https://releases.aspose.com/note/java/) وأضف ملف الـ JAR إلى مسار الـ classpath الخاص بمشروعك.

### 3. مستند OneNote تجريبي
ملف `.one` أو `.onepkg` ترغب في تحويله. للاختبار، يستخدم البرنامج التعليمي الملف `Sample1.one`.

## استيراد الحزم

أولًا، استورد الفئات التي ستحتاجها. هذه الاستيرادات تمنحك الوصول إلى نموذج المستند الأساسي وخيارات تحويل PDF.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

## حفظ OneNote كملف PDF باستخدام PdfSaveOptions

نقسم العملية إلى خطوتين واضحين: تحميل الملف المصدر وحفظه كملف PDF. كل خطوة تتضمن شرحًا مختصرًا لتفهّم **سبب** القيام بها.

### الخطوة 1: تحميل مستند OneNote

ننشئ كائن `Document` بالإشارة إلى ملف OneNote الموجود على القرص.

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

*لماذا هذا مهم:* تحميل الملف إلى كائن `Document` يمنحك التحكم الكامل في محتوياته برمجيًا، مما يسمح بإجراء تعديلات إضافية قبل التحويل إذا لزم الأمر.

### الخطوة 2: حفظ المستند كملف PDF

الآن نستدعي طريقة `save`، مع تمرير كائن `PdfSaveOptions` جديد. هذا يخبر Aspose.Note بترجمة صفحات OneNote إلى صفحات PDF.

```java
// Save the document as PDF
oneFile.save(dataDir + "LoadDocIntoAsposeNoteUsingPdfsaveoptions_out.pdf", new PdfSaveOptions());
```

*نصيحة:* إذا رغبت في **حفظ OneNote كملف PDF** بإعدادات مخصصة—مثل **pdf page size java** محدد—قم بضبط كائن `PdfSaveOptions` قبل تمريره إلى `save()`. على سبيل المثال، يمكنك استدعاء `setPageSize(PageSize.A4)` لتطبيق حجم صفحة A4، وهو طلب شائع في توليد PDF باستخدام Java.

*نصيحة احترافية:* يمكنك أيضًا تعيين `setEmbedStandardFonts(true)` لتضمين الخطوط وتجنب ظهور صفحات فارغة على الأنظمة التي لا تتوفر فيها الخطوط المطلوبة.

## حالات الاستخدام الشائعة

- **إنشاء التقارير:** تصدير ملاحظات الاجتماعات أو وثائق المشروع إلى PDF للتوزيع.
- **الأرشفة:** حفظ محتوى OneNote بصيغة غير قابلة للتعديل لتخزين طويل الأمد.
- **الامتثال:** تحويل الملاحظات المنظمة إلى PDFs يمكن توقيعها رقميًا وتدقيقها.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **الملف غير موجود** | مسار `dataDir` غير صحيح | تحقق من مسار الدليل وتأكد من تطابق اسم الملف تمامًا. |
| **إصدار OneNote غير مدعوم** | استخدام ملف `.one` قديم جدًا | قم بفتح الملف في OneNote أولًا واحفظه مرة أخرى، أو استخدم أحدث نسخة من Aspose.Note التي تضيف توافقًا أوسع. |
| **مخرجات PDF تظهر فارغة** | نقص الخطوط على الخادم | ثبّت الخطوط المطلوبة أو قم بتضمينها عبر `PdfSaveOptions.setEmbedStandardFonts(true)`. |

## الأسئلة المتكررة

**س: هل Aspose.Note متوافق مع جميع إصدارات OneNote؟**  
ج: نعم، يدعم Aspose.Note صيغ OneNote الحديثة، بما في ذلك `.one` و `.onepkg`. قد تحتاج الملفات القديمة إلى فتحها وإعادة حفظها في OneNote أولًا.

**س: هل يمكنني تخصيص مخرجات PDF (حجم الصفحة، الهوامش، إلخ)؟**  
ج: بالتأكيد. يوفر `PdfSaveOptions` خصائص مثل `setPageSize()`، `setMarginTop()`، و `setImageCompression()` لضبط النتيجة بدقة.

**س: هل يدعم Aspose.Note التحويل إلى صيغ أخرى غير PDF؟**  
ج: نعم، يمكنك تحويل ملفات OneNote إلى DOCX، HTML، JPEG، PNG، وغيرها باستخدام خيارات الحفظ المقابلة.

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية كاملة الوظائف من [صفحة تحميل Aspose.Note](https://releases.aspose.com/).

**س: أين يمكنني الحصول على المساعدة إذا واجهت مشاكل؟**  
ج: منتدى مجتمع Aspose هو مكان ممتاز لطرح الأسئلة: [منتدى الدعم](https://forum.aspose.com/c/note/28).

---

**آخر تحديث:** 2026-02-15  
**تم الاختبار مع:** Aspose.Note للـ Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}