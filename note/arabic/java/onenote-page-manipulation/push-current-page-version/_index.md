---
title: دفع إصدار الصفحة الحالية في OneNote - Aspose.Note
linktitle: دفع إصدار الصفحة الحالية في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: حافظ على تحديث محتوى OneNote! تعرف على كيفية تحديث سجل الصفحة وإدارة الإصدارات، ويتضمن الدليل خطوة بخطوة والتعليمات البرمجية. #OneNote #Java #Aspose
weight: 18
url: /ar/java/onenote-page-manipulation/push-current-page-version/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دفع إصدار الصفحة الحالية في OneNote - Aspose.Note

## مقدمة

في هذا البرنامج التعليمي، سنستكشف كيفية استخدام Aspose.Note لـ Java لدفع إصدار الصفحة الحالي في OneNote. Aspose.Note هي مكتبة Java قوية تتيح للمطورين العمل مع مستندات Microsoft OneNote برمجيًا، مما يتيح عمليات متنوعة مثل إنشاء ملفات OneNote ومعالجتها وتحويلها.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:
1. المعرفة الأساسية بلغة البرمجة جافا.
2. تم تثبيت Java Development Kit (JDK) على نظامك.
3.  Aspose.Note لمكتبة جافا. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/java/).
4. نموذج مستند OneNote للعمل معه.

## حزم الاستيراد

أولاً، تحتاج إلى استيراد الحزم الضرورية في مشروع Java الخاص بك لاستخدام وظائف Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## الخطوة 1: قم بتحميل مستند OneNote

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 هنا،`dataDir` يجب أن يشير إلى الدليل الذي يوجد به مستند OneNote الخاص بك. يستبدل`"Sample1.one"` باسم ملف OneNote الخاص بك.

## الخطوة 2: احصل على الصفحة الحالية وتاريخها

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 نقوم باسترداد الصفحة الأولى من الوثيقة باستخدام`getFirstChild()` ومن ثم الحصول على تاريخها باستخدام`getPageHistory()`.

## الخطوة 3: ادفع إصدار الصفحة الحالية

```java
pageHistory.addItem(page.deepClone());
```

وهنا، نقوم بإضافة الإصدار الحالي من الصفحة إلى سجلها عن طريق استنساخها وإضافتها كعنصر جديد.

## الخطوة 4: احفظ المستند

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

وأخيرًا، نقوم بحفظ المستند المعدل مع سجل الصفحة المحدث.

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية دفع إصدار الصفحة الحالي في OneNote باستخدام Aspose.Note لـ Java. باتباع هذه الخطوات، يمكنك إدارة إصدار مستندات OneNote برمجياً بشكل فعال.

## الأسئلة الشائعة

### س١: هل يمكنني استخدام Aspose.Note لـ Java للعمل مع ملفات OneNote المشفرة؟

ج1: نعم، يدعم Aspose.Note for Java العمل مع ملفات OneNote المشفرة وغير المشفرة.

### س2: هل يتوافق Aspose.Note for Java مع الإصدار الأحدث من OneNote؟

ج٢: يسعى Aspose.Note for Java إلى الحفاظ على التوافق مع أحدث الإصدارات من مستندات OneNote.

### س3: هل يمكنني معالجة النصوص والصور داخل مستندات OneNote باستخدام Aspose.Note لـ Java؟

ج3: بالتأكيد، يوفر Aspose.Note for Java وظائف واسعة النطاق لمعالجة النصوص والصور والعناصر الأخرى داخل ملفات OneNote.

### س٤: هل يدعم Aspose.Note for Java تحويل ملفات OneNote إلى تنسيقات أخرى؟

ج4: نعم، يدعم Aspose.Note for Java تحويل ملفات OneNote إلى تنسيقات مختلفة مثل PDF وHTML وتنسيقات الصور.

### س5: أين يمكنني الحصول على دعم Aspose.Note لـ Java إذا واجهت أية مشكلات؟

 ج5: يمكنك زيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) لطلب المساعدة من المجتمع أو الاتصال بدعم Aspose مباشرة.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
