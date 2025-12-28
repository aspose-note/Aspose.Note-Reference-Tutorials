---
date: 2025-12-28
description: تعرّف على كيفية تسطيح ملف PDF من دفتر ملاحظات OneNote باستخدام Aspose.Note
  للغة Java. يوضح هذا الدليل كيفية تحويل OneNote إلى PDF، وتخصيص خيارات التصدير، واستخدام
  خيارات حفظ Aspose PDF.
linktitle: Convert Notebook to Flattened PDF in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: كيفية تسطيح PDF من دفتر OneNote – دليل Aspose.Note
url: /ar/java/onenote-notebook-operations/convert-notebook-to-flattened-pdf/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تسطيح PDF من دفتر ملاحظات OneNote – Aspose.Note

## المقدمة

إذا كنت بحاجة إلى **تسطيح ملفات PDF** التي تم إنشاؤها من دفاتر OneNote، سيوضح لك هذا الدليل الخطوات الدقيقة باستخدام Aspose.Note for Java. تحويل دفتر ملاحظات OneNote إلى PDF مسطح هو طلب شائع عندما تريد مستندًا ثابتًا جاهزًا للطباعة يحافظ على التخطيط الأصلي دون عناصر تفاعلية. سنغطي كل شيء من إعداد البيئة إلى تكوين `NotebookPdfSaveOptions` بحيث يكون PDF الناتج مسطحًا بالكامل.

## إجابات سريعة
- **ما هو “تسطيح PDF”؟** ينشئ PDF يتم فيه دمج جميع العناصر التفاعلية (التعليقات، الطبقات) في صفحة ثابتة واحدة.
- **أي مكتبة تتعامل مع التحويل؟** Aspose.Note for Java، باستخدام خيارات حفظ PDF المدمجة.
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتقييم؛ الترخيص التجاري مطلوب للإنتاج.
- **هل يمكنني تحويل دفاتر متعددة دفعة واحدة؟** نعم – يمكنك تكرار العملية عبر ملفات `.onetoc2` متعددة باستخدام نفس الشيفرة.
- **هل الناتج مسطح فعلاً؟** ضبط `flatten` على `true` يضمن PDF غير تفاعلي.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من توفر ما يلي:

1. **Java Development Kit (JDK)** – أي نسخة حديثة (8 أو أعلى) مثبتة ومُعَدَّة.
2. **Aspose.Note for Java library** – حمّله من [here](https://releases.aspose.com/note/java/).
3. **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA، Eclipse، أو أي محرر تفضله.
4. **دفتر ملاحظات OneNote** (`.onetoc2` file) تريد تصديره.

## استيراد الحزم

أولاً، استورد الفئات المطلوبة لمعالجة الدفتر وتصدير PDF.

```java
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import java.io.IOException;
```

## الخطوة 1: تحميل دفتر OneNote

حمّل الدفتر الذي ترغب في تحويله. استبدل مسار العنصر النائب بالموقع الفعلي لملف `.onetoc2` الخاص بك.

```java
String dataDir = "Your Document Directory";
Notebook notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## الخطوة 2: ضبط خيارات التحويل

قم بتكوين خيارات حفظ PDF. ضبط `flatten` على `true` يضمن أن يكون PDF الناتج مسطحًا. هنا يأتي دور **aspose pdf save options**.

```java
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
notebookSaveOptions.setFlatten(true);
```

## الخطوة 3: حفظ الدفتر كملف PDF مسطح

حدد اسم ملف الإخراج واستدعِ طريقة `save` مع الخيارات التي قمنا بضبطها.

```java
dataDir = dataDir + "ExportNotebookToPDFAsFlattened_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## لماذا هذا مهم

تسطيح PDF ضروري عندما يتم مشاركة المستند مع مستخدمين قد لا يمتلكون تطبيق OneNote الأصلي أو عندما تحتاج إلى تخطيط ثابت للطباعة، الأرشفة، أو الامتثال القانوني. باستخدام `NotebookPdfSaveOptions` من Aspose.Note تحصل على تحكم دقيق في عملية التصدير، مما يجعل تحويل OneNote إلى PDF بسيطًا مع الحفاظ على الدقة البصرية.

## المشكلات الشائعة & استكشاف الأخطاء وإصلاحها

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| صفحات فارغة في PDF | لم يتم تحميل دفتر الملاحظات بشكل صحيح | تحقق من مسار ملف `.onetoc2` وتأكد من عدم تلفه. |
| PDF غير مسطح | `setFlatten(true)` لم يتم استدعاؤه | تحقق مرة أخرى من تمرير كائن `NotebookPdfSaveOptions` إلى `save`. |
| خطأ نفاد الذاكرة للدفاتر الكبيرة | ذاكرة JVM غير كافية | قم بزيادة حجم الذاكرة (`-Xmx2g` أو أعلى) عند تشغيل التطبيق. |

## الأسئلة المتكررة

**س: هل Aspose.Note for Java متوافق مع إصدارات مختلفة من OneNote؟**  
ج: نعم، يدعم Aspose.Note for Java إصدارات OneNote المختلفة، مما يضمن تحويلًا سلسًا عبر البيئات.

**س: هل يمكنني تخصيص مخرجات PDF باستخدام Aspose.Note for Java؟**  
ج: بالطبع. يمكنك تعديل حجم الصفحة، الهوامش، الخطوط، والخصائص الأخرى عبر `NotebookPdfSaveOptions`.

**س: هل يدعم Aspose.Note for Java التحويل الجماعي للدفاتر؟**  
ج: نعم، يمكنك المرور عبر ملفات دفاتر متعددة وتطبيق نفس خيارات الحفظ على كل منها.

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.Note for Java؟**  
ج: نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Note for Java من [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على الدعم لـ Aspose.Note for Java؟**  
ج: يمكنك العثور على الدعم والمساعدة لـ Aspose.Note for Java على [منتدى Aspose.Note](https://forum.aspose.com/c/note/28).

---

**آخر تحديث:** 2025-12-28  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}