---
date: 2026-01-10
description: تعلم دليل مراجعات صفحات Aspose.Note للغة Java – استرجاع مراجعات صفحات
  OneNote برمجياً باستخدام Aspose.Note. اتبع دليلنا خطوةً بخطوة.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: دليل مراجعات الصفحات في aspose.note – الحصول على مراجعات الصفحات في OneNote
url: /ar/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# الحصول على إصدارات الصفحات في OneNote - Aspose.Note

OneNote هو منصة قوية لتدوين الملاحظات، وعندما تحتاج إلى تدقيق التغييرات، يُظهر **aspose.note page revisions tutorial** لك بالضبط كيفية سحب تاريخ الإصدارات ببضع أسطر من كود Java. في هذا الدليل سنستعرض كل ما تحتاجه — من البيئة إلى طباعة تفاصيل كل إصدار — حتى تتمكن من تتبع التعديلات ومساهمات المؤلفين والطوابع الزمنية بسهولة.

## الإجابات السريعة
- **ما الذي يغطيه الدرس؟** استرجاع تاريخ إصدارات الصفحة من ملف OneNote باستخدام Aspose.Note for Java.  
- **ما نسخة المكتبة المطلوبة؟** أي إصدار حديث من Aspose.Note for Java يدعم `LoadOptions.setLoadHistory`.  
- **هل أحتاج إلى ترخيص؟** ترخيص تقييم مؤقت يعمل للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **هل يمكنني تعديل الإصدارات؟** API للقراءة فقط بالنسبة للإصدارات؛ يمكنك فقط استرجاعها.  
- **ما هي المتطلبات الأساسية؟** Java JDK، Aspose.Note for Java، ومستند OneNote يحتوي على بيانات إصدارات.

## ما هو “aspose.note page revisions tutorial”؟
يُظهر الدرس كيفية الوصول برمجياً إلى الإصدارات التاريخية لصف OneNote. كل إصدار يحتوي على بيانات وصفية مثل المؤلف، وقت الإنشاء، ووقت التعديل، مما يتيح لك بناء سجلات تدقيق أو ميزات سجل تغييرات داخل تطبيقاتك.

## لماذا تستخدم Aspose.Note لتتبع إصدارات الصفحات؟
- **No UI dependency** – لا يعتمد على واجهة المستخدم – يعمل بالكامل عبر الكود، مثالي لخدمات الخلفية.  
- **Cross‑platform** – متعدد المنصات – Java يعمل على Windows وLinux وmacOS.  
- **Full control** – تحكم كامل – استرجاع كل خاصية من خصائص الإصدار دون فتح OneNote يدويًا.  
- **Performance** – الأداء – تحميل التاريخ مُحسّن، لذا حتى دفاتر الملاحظات الكبيرة تُعالج بسرعة.

## المتطلبات المسبقة

### 1. Java Development Kit (JDK)
تأكد من تثبيت JDK حديث (8 أو أعلى) وتعيين المتغير `JAVA_HOME`.

### 2. Aspose.Note for Java
قم بتنزيل المكتبة من [رابط التحميل](https://releases.aspose.com/note/java/).

### 3. Sample OneNote Document
أنشئ أو احصل على ملف OneNote (مثال: `Sample1.one`) يحتوي على صفحات مع تاريخ الإصدارات.

## استيراد الحزم
أولاً، استورد الفئات المطلوبة من Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## تنفيذ خطوة بخطوة

### الخطوة 1: إعداد دليل المستند
حدد المجلد الذي يوجد فيه ملف OneNote الخاص بك.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تحميل مستند OneNote مع تمكين التاريخ
فعّل علامة `LoadOptions` لسحب بيانات الإصدارات.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### الخطوة 3: الحصول على الصفحة الأولى
احصل على كائن الصفحة الأولى؛ سيكون هذا هو نقطة المرجع لاسترجاع تاريخها.

```java
Page firstPage = document.getFirstChild();
```

### الخطوة 4: التكرار عبر إصدارات الصفحة
قم بالتكرار عبر كل إصدار واطبع البيانات الوصفية المفيدة مثل الطوابع الزمنية، العنوان، المستوى، والمؤلف.

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

> **Pro tip:** إذا كنت بحاجة لتصفية الإصدارات حسب مؤلف محدد أو نطاق تاريخي، ما عليك سوى إضافة فحوصات شرطية داخل حلقة `for`.

## المشكلات الشائعة والحلول
- **No revisions returned:** تحقق من استدعاء `loadOptions.setLoadHistory(true)` قبل تحميل المستند.  
- **Null author or title:** قد لا تخزن بعض إصدارات OneNote القديمة هذه الحقول؛ تعامل مع القيم `null` بلطف.  
- **Performance lag on large notebooks:** حمّل الأقسام التي تحتاجها فقط أو زد حجم الذاكرة المخصصة لـ JVM.

## الأسئلة المتكررة

**س1: هل يمكنني استخدام Aspose.Note for Java لتعديل إصدارات الصفحات؟**  
A1: لا، API يدعم حاليًا الوصول للقراءة فقط إلى إصدارات الصفحات.

**س2: هل Aspose.Note for Java متوافق مع إصدارات مختلفة من مستندات OneNote؟**  
A2: نعم، يعمل مع صيغ ملفات OneNote المتنوعة، مما يتيح معالجة سلسة عبر الإصدارات.

**س3: هل يتطلب Aspose.Note for Java ترخيصًا للاستخدام؟**  
A3: يلزم ترخيص تجاري للاستخدام في الإنتاج، لكن يتوفر ترخيص تقييم مؤقت للاختبار.

**س4: هل يمكنني طلب الدعم إذا واجهت أي مشكلات أثناء استخدام Aspose.Note for Java؟**  
A4: نعم، يمكنك طرح الأسئلة على منتدى Aspose.Note [هنا](https://forum.aspose.com/c/note/28).

**س5: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Note for Java؟**  
A5: نعم، يمكنك تنزيل نسخة تجريبية مجانية من [الموقع](https://releases.aspose.com/).

---

**آخر تحديث:** 2026-01-10  
**تم الاختبار مع:** Aspose.Note for Java (latest release)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}