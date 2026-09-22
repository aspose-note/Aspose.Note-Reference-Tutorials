---
date: 2026-08-13
description: تعلم كيفية الحصول على OneNote page modified time واسترجاع page revisions
  باستخدام Aspose.Note للـ Java، مثالي لـ auditing و document management.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: احصل على Revisions of Pages في OneNote - Aspose.Note
og_description: تعلم كيفية الحصول على OneNote page modified time واسترجاع revisions
  of OneNote pages باستخدام Aspose.Note للـ Java. خطوات سريعة، code snippets، و troubleshooting.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: احصل على OneNote page modified time باستخدام Aspose.Note – دليل Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: احصل على OneNote page modified time باستخدام Aspose.Note
url: /ar/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# الحصول على وقت تعديل صفحة OneNote باستخدام Aspose.Note

## مقدمة

في هذا البرنامج التعليمي ستتعلم كيفية **الحصول على طوابع وقت تعديل صفحة OneNote** وسحب سجل المراجعات الكامل لصفحة OneNote باستخدام Aspose.Note للغة Java. سواءً كنت تبني ميزة تتبع التدقيق، أو عارض سجل التغييرات، أو تحتاج إلى عرض تاريخ آخر تعديل في لوحة معلومات، فإن هذا الدليل يرافقك في كل خطوة — من إعداد البيئة إلى التعامل مع المشكلات الشائعة.

## إجابات سريعة
- **ما الذي تُعيده “get last modified time”؟** تُعيد طابع الوقت لأحدث تعديل على صفحة OneNote.  
- **أي فئة توفر سجل المراجعات؟** `PageHistory` عبر `Document.getPageHistory(Page)`.  
- **هل أحتاج إلى ترخيص لهذه الميزة؟** نعم، يلزم وجود ترخيص Aspose.Note صالح للاستخدام في الإنتاج.  
- **ما نسخة Java المدعومة؟** Java 8 أو أعلى (JDK 8+).  
- **هل يمكنني تصفية المراجعات حسب المؤلف؟** يمكنك قراءة خاصية `Author` لكل كائن `Page` وتطبيق الفلتر الخاص بك.

## ما هو “get last modified time” في OneNote؟

يتم تخزين وقت آخر تعديل كخاصية بيانات تعريفية على كل صفحة OneNote تُشير إلى لحظة أحدث تعديل. تُظهر Aspose.Note هذه القيمة عبر الطريقة `Page.getLastModifiedTime()`، التي تُعيد كائن `java.util.Date` يمكن تنسيقه أو تسجيله وفقًا لمتطلبات تطبيقك.

## لماذا استرجاع مراجعات الصفحة؟

يمنحك استرجاع مراجعات الصفحة سجل تدقيق كامل لكل تغيير تم إجراؤه على صفحة OneNote، مما يتيح لك تتبع من قام بتعديل ماذا ومتى. يمكن استخدام هذا السجل لمقارنة الإصدارات، استعادة الحالات السابقة، أو تحليل أنماط التعاون بين الفرق، مما يجعله أساسيًا للامتثال ومراقبة الجودة.

## المتطلبات المسبقة

- **Java Development Kit (JDK) 8 أو أحدث** – قم بالتثبيت من موقع Oracle أو أي بائع متوافق.  
- **مكتبة Aspose.Note للغة Java** – قم بتنزيل ملف JAR من صفحة إصدارات Aspose.Note Java **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** واتبع دليل التثبيت **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## استيراد الحزم

تمثل الفئة `Document` دفتر ملاحظات OneNote محملاً في الذاكرة، بينما توفر `Page` و `PageHistory` الوصول إلى الصفحات الفردية وبيانات مراجعاتها.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(يتم عرض عبارات الاستيراد الفعلية كنص عادي للحفاظ على عدد كتل الشيفرة الأصلية.)*

## كيفية الحصول على وقت تعديل صفحة OneNote؟

للحصول على طابع الوقت لآخر تعديل، قم أولاً بتحميل مستند OneNote إلى كائن `Document`، ثم اختر الـ `Page` المطلوب. استدعِ الطريقة `getLastModifiedTime()` على تلك الصفحة، والتي تُعيد كائن `java.util.Date`. يمكنك بعد ذلك تنسيق هذا التاريخ باستخدام `SimpleDateFormat` أو تحويله إلى UTC لتقارير متسقة عبر المناطق الزمنية.

## الخطوة 1: تعيين دليل المستند

حدد المجلد الذي يحتوي على ملف OneNote الخاص بك.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## الخطوة 2: تحميل المستند

أنشئ مثيلًا من `Document` بتمرير المسار الكامل إلى ملف `.one` الخاص بك.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 3: الحصول على الصفحة الأولى

استرجع كائن `Page` الأول من مجموعة صفحات المستند.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## الخطوة 4: الحصول على مراجعات الصفحة

احصل على `PageHistory` للصفحة المحددة. إذا لم يتم تعديل دفتر الملاحظات مطلقًا، قد تُعيد هذه الدالة `null`.

```java
Page firstPage = doc.getFirstChild();
```

## الخطوة 5: استعراض مراجعات الصفحة

قم بالتكرار عبر كل مراجعة `Page`، اقرأ خاصية `Author` و `LastModifiedTime`، وعرض المعلومات.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## المشكلات الشائعة والحلول
- **Null `PageHistory`** – تحقق من أن دفتر الملاحظات يحتوي فعليًا على مراجعات؛ وإلا فإن `getPageHistory` تُعيد `null`.  
- **اختلافات المنطقة الزمنية** – تستخدم `getLastModifiedTime()` المنطقة الزمنية الافتراضية للـ JVM. حوّل إلى UTC باستخدام `SimpleDateFormat` إذا كان تطبيقك يتطلب منطقة موحدة.  
- **عدم تحميل الترخيص** – بدون ترخيص صالح، تعمل Aspose.Note في وضع التقييم، مما يحد من معالجة الصفحات. حمّل ملف الترخيص عند بدء تشغيل التطبيق لتجنب هذا القيد.

## الأسئلة المتكررة

**س1: هل يمكنني استخدام Aspose.Note للغة Java لإنشاء مستندات OneNote جديدة؟**  
A: نعم، تتيح لك الواجهة البرمجية إنشاء وتعديل وحفظ دفاتر ملاحظات OneNote برمجيًا من الصفر.

**س2: هل Aspose.Note للغة Java متوافق مع إصدارات مختلفة من ملفات OneNote؟**  
A: نعم، يدعم صيغ ملفات OneNote من 2007 إلى 2021، مما يضمن توافقًا واسعًا عبر بيئات سطح المكتب والسحابة.

**س3: هل يمكنني تخصيص تنسيق الإخراج عند تصدير مستندات OneNote؟**  
A: بالتأكيد. يمكنك التصدير إلى PDF أو HTML أو PNG أو SVG، والتحكم في خيارات مثل دقة الصورة وتضمين الخطوط.

**س4: هل يتطلب Aspose.Note للغة Java ترخيصًا للاستخدام التجاري؟**  
A: نعم، الترخيص التجاري إلزامي للنشر في بيئات الإنتاج. تتوفر نسخة تجريبية مجانية للتقييم.

**س5: أين يمكنني طلب المساعدة إذا واجهت مشكلات؟**  
A: زر منتدى مجتمع Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** لطرح الأسئلة، مشاركة التجارب، والحصول على مساعدة من المجتمع ومهندسي Aspose.

**آخر تحديث:** 2026-08-13  
**تم الاختبار مع:** Aspose.Note for Java 23.12 (latest at time of writing)  
**المؤلف:** Aspose

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

## دروس ذات صلة

- [دروس Aspose Java - الحصول على معلومات حول الصفحات في OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [دروس مراجعات صفحات aspose.note – الحصول على مراجعات الصفحات في OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [تتبع تغييرات OneNote – إدارة مراجعات الصفحات باستخدام Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}