---
title: استخدم خوارزمية الاحتفاظ بالكائنات الصلبة في OneNote - Aspose.Note
linktitle: استخدم خوارزمية الاحتفاظ بالكائنات الصلبة في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرف على كيفية الحفاظ على الكائنات الصلبة في مستندات Aspose.Note الخاصة بك عند التحويل إلى PDF باستخدام خوارزمية الاحتفاظ بالكائنات الصلبة في Java.
weight: 25
url: /ar/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استخدم خوارزمية الاحتفاظ بالكائنات الصلبة في OneNote - Aspose.Note

## مقدمة

في هذا البرنامج التعليمي، سوف نستكشف كيفية استخدام خوارزمية الاحتفاظ بالكائنات الصلبة في Aspose.Note لـ Java. تعتبر هذه الخوارزمية لا تقدر بثمن للحفاظ على سلامة الكائنات الصلبة داخل مستنداتك عند تحويلها إلى تنسيق PDF. سنقوم بتقسيم العملية خطوة بخطوة، مما يضمن الوضوح والفهم في كل مرحلة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1. تم تثبيت Java Development Kit (JDK) على نظامك.
2.  Aspose.Note لمكتبة جافا. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/java/).

## حزم الاستيراد

أولاً، لنستورد الحزم الضرورية:

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## الخطوة 1: قم بتحميل المستند

قم بتحميل المستند إلى Aspose.Note باستخدام مقتطف التعليمات البرمجية التالي:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## الخطوة 2: تكوين خيارات حفظ PDF

حدد PdfSaveOptions وقم بتعيين PageSplittingAlgorithm على KeepSolidObjectsAlgorithm:

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## الخطوة 3: ضبط حد الارتفاع (اختياري)

يمكنك ضبط حد الارتفاع للأجزاء المستنسخة إذا لزم الأمر:

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## الخطوة 4: احفظ المستند

أخيرًا، احفظ المستند باستخدام خيارات حفظ PDF المحددة:

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية استخدام خوارزمية الاحتفاظ بالكائنات الصلبة في Aspose.Note لـ Java. تضمن هذه الخوارزمية الحفاظ على الكائنات الصلبة الموجودة في مستنداتك عند تحويلها إلى تنسيق PDF، مما يحافظ على سلامة المستند.

## الأسئلة الشائعة

### س1: هل يمكنني ضبط حد الارتفاع للأجزاء المستنسخة؟

 ج1: نعم، يمكنك ضبط حد الارتفاع للأجزاء المستنسخة وفقًا لمتطلباتك باستخدام`heightLimitOfClonedPart` معامل.

### س2: أين يمكنني العثور على المزيد من الوثائق؟

 ج2: يمكنك العثور على وثائق مفصلة حول Aspose.Note لـ Java[هنا](https://reference.aspose.com/note/java/).

### س3: هل هناك نسخة تجريبية مجانية متاحة؟

 ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Note لـ Java[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على الدعم إذا واجهت أية مشكلات؟

 ج4: يمكنك الحصول على الدعم من مجتمع Aspose[هنا](https://forum.aspose.com/c/note/28).

### س5: أين يمكنني شراء الترخيص؟

 ج5: يمكنك شراء ترخيص Aspose.Note لـ Java[هنا](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
