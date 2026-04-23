---
date: 2026-03-16
description: تعلم كيفية تصدير ملفات PDF من OneNote باستخدام Aspose.Note للغة Java
  مع طريقة خوارزمية التقسيم، والتحكم في فواصل الصفحات، وضغط صور PDF بكفاءة.
linktitle: Export OneNote PDF with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: تصدير PDF من OneNote باستخدام طريقة خوارزمية التقسيم – Aspose.Note
url: /ar/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير OneNote PDF باستخدام طريقة خوارزمية التقسيم – Aspose.Note

## المقدمة

إذا كنت بحاجة إلى **تصدير OneNote PDF** برمجياً، فإن Aspose.Note for Java يجعل العملية بسيطة. في هذا الدليل سنستعرض طريقة خوارزمية التقسيم، التي تتيح لك التحكم في كيفية تقسيم المحتوى عبر الصفحات، لضمان مخرجات PDF نظيفة وقابلة للقراءة. ستتعرف على كيفية ضبط خيارات حفظ PDF، اختيار خوارزمية تقسيم الصفحات المناسبة، وأخيراً إنشاء ملف PDF—كل ذلك ببضع أسطر من كود Java.

## الإجابات السريعة
- **ماذا تفعل خوارزمية التقسيم؟** تحدد كيفية معالجة الكائنات التي تمتد عبر حدود الصفحات عند تصدير صفحات OneNote إلى PDF.  
- **ما المكتبة المطلوبة؟** Aspose.Note for Java (قم بتنزيلها من الموقع الرسمي لـ Aspose).  
- **هل أحتاج إلى ترخيص؟** يلزم الحصول على ترخيص مؤقت أو كامل للاستخدام في الإنتاج؛ يتوفر نسخة تجريبية مجانية.  
- **هل يمكنني تصدير دفاتر OneNote الكبيرة؟** نعم – المكتبة تعالج الملفات الكبيرة بكفاءة وتتيح لك ضبط قواعد تقسيم الصفحات.  
- **ما صيغ الإخراج المدعومة؟** PDF، JPEG، PNG، XPS، وأكثر؛ يركز هذا الدليل على تصدير PDF.  
- **كيف يمكنني ضغط صور PDF؟** استخدم `pdfSaveOptions.setCompressImages(true)` لتقليل حجم الصور في ملف PDF المُنشأ.  

## كيفية تصدير OneNote PDF باستخدام خوارزمية التقسيم
هذا القسم يوضح الخطوات الدقيقة اللازمة **لتحويل صفحات OneNote** إلى PDF مع معالجة فواصل الصفحات بذكاء.

## ما هو تصدير OneNote PDF؟
يعني تصدير OneNote PDF تحويل تنسيق الملف الأصلي `.one` إلى مستند PDF محمول. هذا مفيد للمشاركة أو الأرشفة أو طباعة المحتوى دون الحاجة إلى تطبيق OneNote.

## لماذا نستخدم خوارزمية التقسيم لتصدير OneNote PDF؟
تمنحك الخوارزمية تحكمًا دقيقًا في كيفية معالجة الكائنات المعقدة (الجداول، الصور، الرسومات) عند فواصل الصفحات. باختيار الخوارزمية المناسبة يمكنك:

* الحفاظ على التخطيط البصري لكل صفحة.  
* تجنب قطع المحتوى الذي قد يُقصّ إذا لم يُعالج بشكل صحيح.  
* تقليل عدد الصفحات المُولدة عندما يمكن نقل الكائنات إلى الصفحة التالية بشكل نظيف.  

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من توفر المتطلبات التالية:

1. **Java Development Kit (JDK):** تأكد من تثبيت JDK على نظامك. يمكنك تنزيله من [الموقع الإلكتروني](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.Note for Java Library:** قم بتنزيل وتثبيت مكتبة Aspose.Note for Java من [رابط التنزيل](https://releases.aspose.com/note/java/).  

## استيراد الحزم

في مشروع Java الخاص بك، استورد الحزم اللازمة لاستخدام وظائف Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## الخطوة 1: تحديد دليل المستند

قم بإعداد الدليل الذي يقع فيه مستند OneNote الخاص بك.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحميل مستند OneNote

حمّل مستند OneNote باستخدام الفئة `Document` الخاصة بـ Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## الخطوة 3: ضبط خيارات حفظ PDF

أنشئ مثيلًا من `PdfSaveOptions` لتحديد الخيارات الخاصة بحفظ المستند كملف PDF. هنا يمكنك **ضبط سلوك تقسيم الصفحات** وإعدادات أخرى متعلقة بـ PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## الخطوة 4: ضبط خوارزمية تقسيم الصفحات

اختر الخوارزمية المناسبة للتقسيم وفقًا لمتطلباتك. في هذا المثال نستخدم `KeepPartAndCloneSolidObjectToNextPageAlgorithm`، التي تحتفظ بجزء من الكائن في الصفحة الحالية وتستنسخ البقية إلى الصفحة التالية.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## الخطوة 5: حفظ المستند

احفظ المستند باستخدام خيارات حفظ PDF المحددة. هذه الخطوة **تُنتج مخرجات PDF لـ OneNote** التي يمكنك فتحها أو مشاركتها أو طباعتها.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **الكائنات تُقَطَع عند حدود الصفحات** | جرّب خوارزمية مختلفة مثل `AlwaysSplitObjectsAlgorithm` أو زد قيمة العتبة في `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **ملف PDF الناتج فارغ** | تأكد من أن ملف `.one` الأصلي غير تالف وأن مسار `dataDir` صحيح. |
| **الأداء بطيء مع دفاتر ملاحظات كبيرة** | استخدم `pdfSaveOptions.setCompressImages(true)` لتقليل استهلاك الذاكرة، وفكّر في معالجة الدفتر على أقسام أصغر. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Note for Java مع لغات برمجة أخرى؟**  
ج: نعم، تتوفر Aspose.Note أيضًا لـ .NET، C++، وPython.

**س: هل Aspose.Note مناسبة لمعالجة ملفات OneNote الكبيرة؟**  
ج: بالتأكيد. تم تحسين المكتبة للتعامل مع دفاتر ملاحظات كبيرة بكفاءة.

**س: أين يمكنني العثور على موارد إضافية ودعم لـ Aspose.Note؟**  
ج: يمكنك الرجوع إلى [الوثائق](https://reference.aspose.com/note/java/) و[المنتدى](https://forum.aspose.com/c/note/28) للحصول على الدعم والإرشادات.

**س: هل يمكنني تجربة Aspose.Note قبل الشراء؟**  
ج: نعم، يمكنك الاستفادة من [نسخة تجريبية مجانية](https://releases.aspose.com/) لاستكشاف الميزات قبل الشراء.

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note؟**  
ج: يمكنك طلب [ترخيص مؤقت](https://purchase.aspose.com/temporary-license/) لتقييم المنتج خلال فترة التجربة.

---

**آخر تحديث:** 2026-03-16  
**تم الاختبار مع:** Aspose.Note 24.12 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}