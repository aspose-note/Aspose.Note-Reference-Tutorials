---
date: 2025-12-18
description: تعلم كيفية تصدير صفحات OneNote إلى PDF باستخدام Aspose.Note للغة Java.
  اختر خوارزميات التقسيم، اضبط تقسيم الصفحات، وأنشئ ملفات PDF بسهولة.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: تصدير صفحات OneNote باستخدام طريقة خوارزمية التقسيم – Aspose.Note
url: /ar/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير صفحات OneNote باستخدام طريقة خوارزمية التقسيم – Aspose.Note

## المقدمة

إذا كنت بحاجة إلى **export OneNote pages** إلى مستند PDF برمجياً، فإن Aspose.Note for Java يجعل العملية بسيطة. في هذا البرنامج التعليمي سنستعرض طريقة خوارزمية التقسيم، التي تتيح لك التحكم في كيفية تقسيم المحتوى عبر الصفحات، لضمان مخرجات PDF نظيفة وقابلة للقراءة. ستتعرف على كيفية ضبط خيارات حفظ PDF، اختيار خوارزمية تقسيم الصفحات المناسبة، وأخيراً إنشاء ملف PDF—كل ذلك باستخدام بضع أسطر من كود Java.

## إجابات سريعة
- **What does the Splitting Algorithm do?** يحدد كيفية معالجة الكائنات التي تمتد عبر حدود الصفحات عند تصدير صفحات OneNote إلى PDF.  
- **Which library is required?** Aspose.Note for Java (تحميل من الموقع الرسمي لـ Aspose).  
- **Do I need a license?** يلزم الحصول على ترخيص مؤقت أو كامل للاستخدام في الإنتاج؛ يتوفر نسخة تجريبية مجانية.  
- **Can I export large OneNote notebooks?** نعم – المكتبة تعالج الملفات الكبيرة بكفاءة وتتيح لك ضبط قواعد تقسيم الصفحات.  
- **What output formats are supported?** PDF، JPEG، PNG، XPS، وأكثر؛ يركز هذا الدليل على تصدير PDF.

## ما هو **export onenote pages**؟
يعني تصدير صفحات OneNote تحويل تنسيق الملف الأصلي `.one` إلى تنسيق أكثر قابلية للنقل مثل PDF. هذا مفيد للمشاركة أو الأرشفة أو طباعة المحتوى دون الحاجة إلى تطبيق OneNote.

## لماذا نستخدم خوارزمية التقسيم لـ **export onenote pages**؟
توفر لك الخوارزمية تحكمًا دقيقًا في كيفية معالجة الكائنات المعقدة (الجداول، الصور، الرسومات) عند فواصل الصفحات. باختيار الخوارزمية المناسبة يمكنك:
* الحفاظ على التخطيط البصري لكل صفحة.  
* تجنب المحتوى المقطوع الذي قد يُقص.  
* تقليل عدد الصفحات المُنشأة عندما يمكن نقل الكائنات إلى الصفحة التالية بشكل نظيف.  

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك المتطلبات المسبقة التالية:

1. Java Development Kit (JDK): تأكد من تثبيت JDK على نظامك. يمكنك تحميله من [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.Note for Java Library: قم بتحميل وتثبيت مكتبة Aspose.Note for Java من [download link](https://releases.aspose.com/note/java/).

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

حمّل مستند OneNote باستخدام الفئة `Document` من Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## الخطوة 3: ضبط خيارات حفظ PDF

أنشئ مثيلًا من `PdfSaveOptions` لتحديد الخيارات الخاصة بحفظ المستند كملف PDF. هنا حيث تقوم **set page splitting** السلوك وإعدادات أخرى متعلقة بـ PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## الخطوة 4: ضبط خوارزمية تقسيم الصفحات

اختر خوارزمية التقسيم المناسبة وفقًا لمتطلباتك. هنا نستخدم `KeepPartAndCloneSolidObjectToNextPageAlgorithm`، التي تحتفظ بجزء من الكائن في الصفحة الحالية وتنسخ البقية إلى الصفحة التالية.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## الخطوة 5: حفظ المستند

احفظ المستند باستخدام خيارات حفظ PDF المحددة. هذه الخطوة **generates PDF onenote** مخرجات يمكنك فتحها أو مشاركتها أو طباعتها.

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
| **Objects are cut off at page boundaries** | جرّب خوارزمية مختلفة مثل `AlwaysSplitObjectsAlgorithm` أو زد قيمة العتبة في `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **Output PDF is blank** | تحقق من أن ملف `.one` المصدر غير معطوب وأن مسار `dataDir` صحيح. |
| **Performance is slow with large notebooks** | استخدم `pdfSaveOptions.setCompressImages(true)` لتقليل استهلاك الذاكرة، وفكّر في معالجة الدفتر في أقسام أصغر. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Note for Java مع لغات برمجة أخرى؟**  
ج: نعم، Aspose.Note متوفر أيضًا لـ .NET و C++ و Python.

**س: هل Aspose.Note مناسب لمعالجة ملفات OneNote الكبيرة؟**  
ج: بالتأكيد. المكتبة مُحسّنة للتعامل مع الدفاتر الكبيرة بكفاءة.

**س: أين يمكنني العثور على موارد إضافية ودعم لـ Aspose.Note؟**  
ج: يمكنك الرجوع إلى [documentation](https://reference.aspose.com/note/java/) و[forum](https://forum.aspose.com/c/note/28) للحصول على الدعم والإرشاد.

**س: هل يمكنني تجربة Aspose.Note قبل الشراء؟**  
ج: نعم، يمكنك الاستفادة من [free trial](https://releases.aspose.com/) لاستكشاف الميزات قبل الشراء.

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note؟**  
ج: يمكنك طلب [temporary license](https://purchase.aspose.com/temporary-license/) لتقييم المنتج خلال فترة التجربة.

**آخر تحديث:** 2025-12-18  
**تم الاختبار مع:** Aspose.Note 24.12 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}