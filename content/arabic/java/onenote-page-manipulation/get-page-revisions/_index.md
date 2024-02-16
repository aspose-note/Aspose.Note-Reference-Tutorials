---
title: احصل على مراجعات الصفحة في OneNote - Aspose.Note
linktitle: احصل على مراجعات الصفحة في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرف على كيفية استرداد مراجعات الصفحة في OneNote باستخدام Aspose.Note لـ Java. اتبع دليلنا خطوة بخطوة لتتبع التغييرات بشكل فعال.
type: docs
weight: 14
url: /ar/java/onenote-page-manipulation/get-page-revisions/
---
## مقدمة

يعد OneNote أداة قوية لتنظيم ملاحظاتك وإدارتها، ولكن في بعض الأحيان تحتاج إلى تتبع التغييرات والمراجعات التي تم إجراؤها على صفحاتك. باستخدام Aspose.Note لـ Java، يمكنك بسهولة استرداد مراجعات الصفحة برمجيًا. في هذا البرنامج التعليمي، سنرشدك خلال عملية الحصول على مراجعات الصفحة في OneNote باستخدام Aspose.Note لـ Java.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

### 1. مجموعة تطوير جافا (JDK)

تأكد من تثبيت Java Development Kit (JDK) على نظامك. يمكنك تنزيل JDK وتثبيته من موقع Oracle الإلكتروني.

### 2. Aspose.Note لجافا

قم بتنزيل وتثبيت Aspose.Note لـ Java من[رابط التحميل](https://releases.aspose.com/note/java/).

### 3. نموذج مستند OneNote

إعداد نموذج مستند OneNote (`Sample1.one`) الذي يحتوي على الصفحات التي تريد استرداد المراجعات منها.

## حزم الاستيراد

أولاً، تحتاج إلى استيراد الحزم الضرورية من Aspose.Note لـ Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

الآن، دعونا نقسم المثال المقدم إلى خطوات متعددة:

## الخطوة 1: إعداد دليل المستندات

حدد مسار الدليل حيث يوجد مستند OneNote الخاص بك.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: قم بتحميل مستند OneNote

 قم بتحميل مستند OneNote باستخدام`LoadOptions` لتمكين سجل التحميل.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## الخطوة 3: احصل على الصفحة الأولى

استرداد الصفحة الأولى من المستند الذي تم تحميله.

```java
Page firstPage = document.getFirstChild();
```

## الخطوة 4: التكرار من خلال مراجعات الصفحة

قم بالتكرار من خلال كل مراجعة للصفحة واسترجاع المعلومات ذات الصلة مثل وقت التعديل الأخير ووقت الإنشاء والعنوان والمستوى والمؤلف.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية استرداد مراجعات الصفحة في OneNote باستخدام Aspose.Note لـ Java. باتباع هذه الخطوات، يمكنك تتبع التغييرات التي تم إجراؤها على صفحات OneNote الخاصة بك برمجياً بكفاءة.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.Note لـ Java لتعديل مراجعات الصفحة؟

ج1: لا، يدعم Aspose.Note for Java حاليًا استرداد مراجعات الصفحة ولكن لا يدعم تعديلها.

### س2: هل يتوافق Aspose.Note for Java مع الإصدارات المختلفة من مستندات OneNote؟

ج2: نعم، يدعم Aspose.Note for Java إصدارات مختلفة من مستندات OneNote، مما يسمح لك بالعمل مع تنسيقات ملفات مختلفة بسلاسة.

### س3: هل يتطلب Aspose.Note for Java ترخيصًا للاستخدام؟

ج3: نعم، أنت بحاجة إلى شراء ترخيص لاستخدام Aspose.Note لـ Java في المشاريع التجارية. ومع ذلك، يمكنك أيضًا الحصول على ترخيص مؤقت لأغراض التقييم.

### س4: هل يمكنني طلب الدعم إذا واجهت أية مشكلات أثناء استخدام Aspose.Note لـ Java؟

 ج4: نعم، يمكنك طلب الدعم من منتدى Aspose.Note[هنا](https://forum.aspose.com/c/note/28).

### س5: هل تتوفر نسخة تجريبية مجانية من Aspose.Note لـ Java؟

 ج5: نعم، يمكنك الوصول إلى الإصدار التجريبي المجاني من Aspose.Note لـ Java من[موقع إلكتروني](https://releases.aspose.com/).