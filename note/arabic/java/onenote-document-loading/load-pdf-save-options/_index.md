---
date: 2025-12-05
description: تعلم كيفية تحويل OneNote إلى PDF وحفظ OneNote كملف PDF باستخدام Aspose.Note
  للغة Java. بسط مهام تحويل المستندات الخاصة بك باستخدام PdfSaveOptions.
linktitle: Load OneNote Document into Aspose.Note using PdfSaveOptions
second_title: Aspose.Note Java API
title: تحويل OneNote إلى PDF باستخدام Aspose.Note و PdfSaveOptions
url: /ar/java/onenote-document-loading/load-pdf-save-options/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل OneNote إلى PDF باستخدام Aspose.Note و PdfSaveOptions

## المقدمة

في هذا الدليل الشامل، ستتعلم **كيفية تحويل OneNote إلى PDF** باستخدام Aspose.Note للغة Java. سنستعرض خطوات تحميل ملف OneNote، ضبط إعدادات التحويل، وأخيرًا حفظ النتيجة كملف PDF. بنهاية هذا الشرح ستكون قادرًا على دمج هذه العملية في تطبيقات Java الخاصة بك بسهولة.

## إجابات سريعة
- **ما المكتبة التي تتولى التحويل؟** Aspose.Note للغة Java مع `PdfSaveOptions`.
- **كم من الوقت تستغرق التنفيذ الأساسي؟** حوالي 5‑10 دقائق للحصول على نموذج عمل.
- **هل أحتاج إلى رخصة للإنتاج؟** نعم، يلزم الحصول على رخصة تجارية؛ يتوفر إصدار تجريبي مجاني.
- **هل يمكنني تخصيص مخرجات PDF؟** بالتأكيد – `PdfSaveOptions` يتيح لك ضبط حجم الصفحة، الهوامش، والمزيد.
- **ما صيغ OneNote المدعومة؟** كل من ملفات `.one` و `.onepkg` مدعومة.

## تحويل OneNote إلى PDF – مقدمة

Aspose.Note يبسط التعامل مع ملفات Microsoft OneNote في Java. سواء كنت تحتاج إلى إنشاء تقارير، أرشفة ملاحظات، أو دمج محتوى OneNote في سير عمل أكبر، فإن تحويل هذه الملفات إلى PDF غالبًا ما يكون الخطوة الأولى.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من توفر ما يلي:

### 1. بيئة تطوير Java
إصدار حديث من JDK (يوصى بـ Java 17 أو أحدث). يمكنك تحميله من موقع Oracle أو اعتماد OpenJDK.

### 2. مكتبة Aspose.Note للغة Java
احصل على أحدث حزمة Aspose.Note للغة Java من [صفحة التحميل الرسمية](https://releases.aspose.com/note/java/) وأضف ملف الـ JAR إلى مسار الـ classpath في مشروعك.

### 3. مستند OneNote تجريبي
ملف `.one` أو `.onepkg` ترغب في تحويله. للاختبار، يستخدم الدليل `Sample1.one`.

## استيراد الحزم

أولاً، استورد الفئات التي ستحتاجها. هذه الاستيرادات تمنحك الوصول إلى نموذج المستند الأساسي وخيارات تحويل PDF.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

## حفظ OneNote كملف PDF باستخدام PdfSaveOptions

فيما يلي نقسم العملية إلى خطوتين واضحين: تحميل الملف المصدر وحفظه كملف PDF. كل خطوة تتضمن شرحًا مختصرًا لتفهم **سبب** تنفيذها.

### الخطوة 1: تحميل مستند OneNote

ننشئ كائن `Document` بالإشارة إلى ملف OneNote الموجود على القرص.

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

*لماذا هذا مهم:* تحميل الملف إلى كائن `Document` يمنحك تحكمًا برمجيًا كاملاً في محتوياته، مما يسمح بإجراء تعديلات إضافية قبل التحويل إذا لزم الأمر.

### الخطوة 2: حفظ المستند كملف PDF

الآن نستدعي طريقة `save`، مع تمرير كائن `PdfSaveOptions` جديد. هذا يخبر Aspose.Note بترجمة صفحات OneNote إلى صفحات PDF.

```java
// Save the document as PDF
oneFile.save(dataDir + "LoadDocIntoAsposeNoteUsingPdfsaveoptions_out.pdf", new PdfSaveOptions());
```

*نصيحة:* إذا رغبت في **حفظ OneNote كملف PDF** بإعدادات مخصصة (مثل حجم صفحة محدد أو ضغط الصور)، قم بضبط كائن `PdfSaveOptions` قبل تمريره إلى `save()`.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **الملف غير موجود** | مسار `dataDir` غير صحيح | تحقق من مسار الدليل وتأكد من تطابق اسم الملف تمامًا. |
| **إصدار OneNote غير مدعوم** | استخدام ملف `.one` قديم جدًا | قم بفتح الملف في OneNote وحفظه مرة أخرى، أو استخدم أحدث نسخة من Aspose.Note التي تضيف توافقًا أوسع. |
| **مخرجات PDF تظهر فارغة** | نقص الخطوط على الخادم | ثبّت الخطوط المطلوبة أو قم بدمجها عبر `PdfSaveOptions.setEmbedStandardFonts(true)`. |

## الأسئلة المتكررة

**س: هل Aspose.Note متوافق مع جميع إصدارات OneNote؟**  
ج: نعم، يدعم Aspose.Note صيغ OneNote الحديثة، بما في ذلك `.one` و `.onepkg`. قد تحتاج الملفات القديمة إلى فتحها وإعادة حفظها في OneNote أولًا.

**س: هل يمكنني تخصيص مخرجات PDF (حجم الصفحة، الهوامش، إلخ)؟**  
ج: بالتأكيد. توفر `PdfSaveOptions` خصائص مثل `setPageSize()`، `setMarginTop()`، و `setImageCompression()` لضبط النتيجة بدقة.

**س: هل يدعم Aspose.Note التحويل إلى صيغ غير PDF؟**  
ج: نعم، يمكنك تحويل ملفات OneNote إلى DOCX، HTML، JPEG، PNG، وغيرها باستخدام خيارات الحفظ المناسبة.

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
ج: نعم، يمكنك تحميل نسخة تجريبية كاملة الوظائف من [صفحة تحميل Aspose.Note](https://releases.aspose.com/).

**س: أين يمكنني الحصول على المساعدة إذا واجهت مشاكل؟**  
ج: منتدى مجتمع Aspose هو مكان رائع لطرح الأسئلة: [منتدى الدعم](https://forum.aspose.com/c/note/28).

---

**آخر تحديث:** 2025-12-05  
**تم الاختبار مع:** Aspose.Note للغة Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}