---
date: 2026-01-10
description: تعلم كيفية الحصول على وقت التعديل الأخير واسترجاع إصدارات صفحات OneNote
  باستخدام Aspose.Note للغة Java. دمج ذلك في تطبيقات Java الخاصة بك لإدارة مستندات
  فعّالة.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: كيفية الحصول على وقت التعديل الأخير لصفحات OneNote – Aspose.Note
url: /ar/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# الحصول على مراجعات الصفحات في OneNote - Aspose.Note

## المقدمة

في هذا البرنامج التعليمي، ستحصل على **وقت آخر تعديل** للصفحات داخل مستند OneNote وتستكشف كيفية استرجاع تاريخ المراجعات الكامل باستخدام Aspose.Note for Java. سواءً كنت تبني نظام إدارة مستندات، أو تدقق التغييرات، أو تحتاج ببساطة إلى عرض متى تم تعديل الصفحة آخر مرة، يوضح لك هذا الدليل بالضبط كيفية استخراج هذه المعلومات برمجيًا.

## إجابات سريعة
- **ماذا تُعيد الدالة “get last modified time”؟** طابع زمني لآخر تعديل تم على صفحة OneNote.  
- **أي فئة توفر تاريخ المراجعات؟** `PageHistory` عبر `Document.getPageHistory(Page)`.  
- **هل أحتاج إلى ترخيص لهذه الميزة؟** نعم، يلزم وجود ترخيص Aspose.Note صالح للاستخدام في الإنتاج.  
- **ما نسخة Java المدعومة؟** Java 8 أو أعلى (JDK 8+).  
- **هل يمكنني تصفية المراجعات حسب المؤلف؟** يمكنك قراءة خاصية `Author` لكل كائن `Page` وتطبيق الفلتر الخاص بك.

## ما هو “get last modified time” في OneNote؟

إن **وقت آخر تعديل** هو حقل بيانات وصفية يُخزن مع كل صفحة ويسجل متى تم تعديل الصفحة آخر مرة. تُظهر Aspose.Note هذه القيمة عبر طريقة `Page.getLastModifiedTime()`، مما يجعل من السهل عرض أو تسجيل تواريخ التغييرات.

## لماذا استرجاع مراجعات الصفحات؟

- **سجلات التدقيق:** الحفاظ على سجل لمن قام بتغيير ماذا ومتى.  
- **مقارنة الإصدارات:** بناء ميزات تقارن بين مراجعتين جنبًا إلى جنب.  
- **رؤى التعاون بين المستخدمين:** فهم أنماط التحرير في دفاتر الملاحظات المشتركة.  

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك ما يلي:

### تثبيت مجموعة تطوير Java (JDK)

قم بتثبيت JDK 8 أو أحدث من موقع Oracle أو من مدير الحزم المفضل لديك.

### مكتبة Aspose.Note for Java

حمّل المكتبة من الموقع الرسمي. يمكنك العثور على رابط التحميل **[هنا](https://releases.aspose.com/note/java/)**. اتبع تعليمات التثبيت في الوثائق **[هنا](https://reference.aspose.com/note/java/)**.

## استيراد الحزم

للبدء، استورد الحزم الضرورية إلى مشروع Java الخاص بك. ستمكنك هذه الحزم من الاستفادة من الوظائف التي توفرها Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

الآن، دعنا نقسم شفرة المثال المقدمة إلى خطوات متعددة لفهم كل مكوّن ووظيفته.

## كيفية الحصول على وقت آخر تعديل لصفحة OneNote

### الخطوة 1: تعيين دليل المستند
حدد الدليل الذي يقع فيه مستند OneNote الخاص بك.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تحميل المستند
حمّل مستند OneNote إلى Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### الخطوة 3: الحصول على الصفحة الأولى
استرجع الصفحة الأولى من المستند.

```java
Page firstPage = doc.getFirstChild();
```

### الخطوة 4: الحصول على مراجعات الصفحة
احصل على تاريخ مراجعات الصفحة.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### الخطوة 5: استعراض مراجعات الصفحة
تجول في قائمة مراجعات الصفحة واستخرج المعلومات ذات الصلة، بما في ذلك **وقت آخر تعديل**.

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

## المشكلات الشائعة والحلول
- **`PageHistory` فارغ:** تأكد من أن المستند يحتوي فعليًا على مراجعات؛ وإلا قد تُعيد `getPageHistory` القيمة `null`.  
- **اختلافات المنطقة الزمنية:** تُعيد `getLastModifiedTime()` كائن `java.util.Date` في المنطقة الزمنية الافتراضية للنظام. حوّل إلى UTC إذا لزم الأمر.  
- **الترخيص غير محمّل:** بدون ترخيص صالح، قد تعمل Aspose.Note في وضع التقييم، مما يحد من عدد الصفحات المعالجة.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.Note for Java لإنشاء مستندات OneNote جديدة؟
ج1: نعم، توفر Aspose.Note for Java دعمًا شاملاً لإنشاء وقراءة وتعديل مستندات OneNote برمجيًا.

### س2: هل Aspose.Note for Java متوافق مع إصدارات مختلفة من ملفات OneNote؟
ج2: نعم، تدعم Aspose.Note for Java إصدارات مختلفة من ملفات Microsoft OneNote، مما يضمن التوافق عبر بيئات مختلفة.

### س3: هل يمكنني تخصيص تنسيق الإخراج عند تصدير مستندات OneNote؟
ج3: بالتأكيد، توفر Aspose.Note for Java مرونة في تصدير مستندات OneNote إلى صيغ مختلفة مثل PDF وHTML والصور، مع خيارات للتخصيص.

### س4: هل يتطلب Aspose.Note for Java ترخيصًا للاستخدام التجاري؟
ج4: نعم، يلزم وجود ترخيص صالح للاستخدام التجاري لـ Aspose.Note for Java. يمكنك الحصول على الترخيص من موقع Aspose.

### س5: أين يمكنني طلب المساعدة إذا واجهت مشكلات أو كان لدي أسئلة حول Aspose.Note for Java؟
ج5: للحصول على الدعم والمساعدة، يمكنك زيارة منتدى Aspose.Note **[هنا](https://forum.aspose.com/c/note/28)**، حيث يمكنك طرح الأسئلة ومشاركة التجارب والتفاعل مع المستخدمين الآخرين والخبراء.

**آخر تحديث:** 2026-01-10  
**تم الاختبار مع:** Aspose.Note for Java 23.12 (الأحدث وقت كتابة هذا المقال)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}