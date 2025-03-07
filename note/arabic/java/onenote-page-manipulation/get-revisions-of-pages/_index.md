---
title: احصل على مراجعات الصفحات في OneNote - Aspose.Note
linktitle: احصل على مراجعات الصفحات في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرف على كيفية استرداد مراجعات الصفحات داخل مستندات OneNote باستخدام Aspose.Note Java. قم بدمج هذا في تطبيقات Java الخاصة بك لإدارة المستندات بكفاءة.
weight: 15
url: /ar/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# احصل على مراجعات الصفحات في OneNote - Aspose.Note

## مقدمة

في هذا البرنامج التعليمي، سوف نتعمق في إمكانيات Aspose.Note for Java، وهي مكتبة قوية تمكنك من العمل مع ملفات Microsoft OneNote بسلاسة في تطبيقات Java الخاصة بك. وعلى وجه التحديد، سنركز على كيفية استرداد مراجعات الصفحات داخل مستند OneNote. بحلول نهاية هذا الدليل، ستكون مجهزًا بالمعرفة اللازمة لاستخراج مراجعات الصفحة بكفاءة، بما في ذلك تفاصيل مثل وقت آخر تعديل، ووقت الإنشاء، والعنوان، والمستوى، والمؤلف.

## المتطلبات الأساسية

قبل الغوص في هذا البرنامج التعليمي، تأكد من إعداد المتطلبات الأساسية التالية:

### تم تثبيت مجموعة أدوات تطوير Java (JDK).

تأكد من تثبيت Java Development Kit على نظامك. يمكنك تنزيله وتثبيته من موقع Oracle على الويب أو استخدام مدير الحزم إذا كنت تستخدم نظامًا يستند إلى Unix.

### Aspose.Note لمكتبة جافا

 قم بتنزيل وتثبيت Aspose.Note لمكتبة Java من موقع الويب. يمكنك العثور على رابط التحميل[هنا](https://releases.aspose.com/note/java/) . اتبع تعليمات التثبيت المتوفرة في الوثائق[هنا](https://reference.aspose.com/note/java/).

## حزم الاستيراد

للبدء، قم باستيراد الحزم الضرورية إلى مشروع Java الخاص بك. ستسمح لك هذه الحزم بالاستفادة من الوظائف التي يوفرها Aspose.Note لـ Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

الآن، دعونا نقسم رمز المثال المقدم إلى خطوات متعددة لفهم كل مكون ووظائفه.

## الخطوة 1: قم بتعيين دليل المستندات

حدد الدليل الذي يوجد به مستند OneNote الخاص بك.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: قم بتحميل المستند

قم بتحميل مستند OneNote إلى Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## الخطوة 3: احصل على الصفحة الأولى

استرداد الصفحة الأولى من الوثيقة.

```java
Page firstPage = doc.getFirstChild();
```

## الخطوة 4: احصل على مراجعات الصفحة

الحصول على تاريخ المراجعات للصفحة.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## الخطوة 5: اجتياز مراجعات الصفحة

قم بالتكرار من خلال قائمة مراجعات الصفحة واسترجاع المعلومات ذات الصلة.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا كيفية استرداد مراجعات الصفحات داخل مستند OneNote باستخدام Aspose.Note لـ Java. باتباع الدليل الموضح خطوة بخطوة والاستفادة من رمز المثال المقدم، يمكنك بسهولة دمج هذه الوظيفة في تطبيقات Java الخاصة بك، مما يتيح الإدارة الفعالة لملفات OneNote.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.Note لـ Java لإنشاء مستندات OneNote جديدة؟

ج1: نعم، يوفر Aspose.Note for Java دعمًا شاملاً لإنشاء مستندات OneNote وقراءتها ومعالجتها برمجياً.

### س2: هل يتوافق Aspose.Note for Java مع الإصدارات المختلفة من ملفات OneNote؟

ج2: نعم، يدعم Aspose.Note for Java إصدارات مختلفة من ملفات Microsoft OneNote، مما يضمن التوافق عبر بيئات مختلفة.

### س3: هل يمكنني تخصيص تنسيق الإخراج عند تصدير مستندات OneNote؟

ج3: بالتأكيد، يوفر Aspose.Note for Java المرونة في تصدير مستندات OneNote إلى تنسيقات مختلفة مثل PDF وHTML والصور، مع خيارات للتخصيص.

### س4: هل يتطلب Aspose.Note for Java ترخيصًا للاستخدام التجاري؟

ج4: نعم، يلزم وجود ترخيص صالح للاستخدام التجاري لـ Aspose.Note لـ Java. يمكنك الحصول على ترخيص من موقع Aspose.

### س5: أين يمكنني طلب المساعدة إذا واجهت مشكلات أو كانت لدي أسئلة حول Aspose.Note for Java؟

 ج5: للحصول على الدعم والمساعدة، يمكنك زيارة منتدى Aspose.Note[هنا](https://forum.aspose.com/c/note/28)حيث يمكنك طرح الأسئلة ومشاركة الخبرات والتفاعل مع المستخدمين والخبراء الآخرين.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
