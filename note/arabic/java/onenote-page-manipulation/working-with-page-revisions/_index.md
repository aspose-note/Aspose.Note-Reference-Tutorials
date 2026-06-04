---
date: 2026-01-15
description: تعلم كيفية تتبع التغييرات في OneNote وإدارة مراجعات الصفحات في مستندات
  OneNote باستخدام Aspose.Note للغة Java. يتضمن مثالًا على ملخص المراجعة وكيفية تعديل
  تاريخ المراجعة.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: تتبع التغييرات في أوننوت – إدارة مراجعات الصفحات باستخدام Aspose.Note
url: /ar/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# العمل مع مراجعات الصفحات في OneNote - Aspose.Note

## مقدمة

OneNote أداة قوية لتنظيم الملاحظات، وعندما تحتاج إلى **track changes onenote**، يصبح إدارة مراجعات الصفحات أمرًا أساسيًا للتعاون الفعّال. باستخدام Aspose.Note for Java، يمكنك التعامل مع المراجعات برمجيًا، وعرض من قام بتحرير الصفحة، وحتى تعديل الطوابع الزمنية. يرشّحك هذا الدليل خلال كل خطوة، من تحميل المستند إلى تحديث ملخص المراجعة.

## إجابات سريعة
- **What does “track changes onenote” mean?** يشير إلى مراقبة من قام بتحرير صفحة OneNote ومتى.
- **Which library is required?** Aspose.Note for Java.
- **Can I change the author or date of a revision?** نعم، باستخدام RevisionSummary API (`modify revision date`).
- **Do I need a OneNote file beforehand?** نعم، يلزم وجود ملف `.one` تجريبي.
- **Is a license needed for production?** يتطلب ترخيص Aspose.Note صالح للاستخدام التجاري.

## ما هو مثال ملخص المراجعة؟
*revision summary* يوفر بيانات تعريفية حول أحدث التغييرات في الصفحة—اسم المؤلف، وقت التعديل الأخير، وتفاصيل أخرى. في هذا الدليل سنسترجع ونعرض هذه المعلومات، ثم نوضح كيفية **modify revision date**.

## لماذا تتبع التغييرات onenote باستخدام Aspose.Note؟
- **Collaboration:** التعاون: رؤية سريعة لمن قام بأحدث التعديلات.
- **Auditing:** التدقيق: الحفاظ على سجل موثوق للتغييرات للامتثال.
- **Automation:** الأتمتة: دمج معالجة المراجعات في خدمات الخلفية أو أدوات الترحيل.

## المتطلبات المسبقة

### بيئة تطوير Java
تأكد من تثبيت مجموعة تطوير جافا (JDK) على نظامك.

### مكتبة Aspose.Note for Java
قم بتنزيل وتثبيت مكتبة Aspose.Note for Java من [here](https://releases.aspose.com/note/java/).

### مستند OneNote
احرص على وجود مستند OneNote تجريبي جاهز لأغراض الاختبار.

## استيراد الحزم

في مشروع Java الخاص بك، استورد الحزم الضرورية للعمل مع Aspose.Note for Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

دعنا نقسم المثال المقدم إلى خطوات متعددة لفهم واضح.

## الخطوة 1: تحميل مستند OneNote

أولاً، قم بتحميل مستند OneNote واحصل على الصفحة الفرعية الأولى.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## الخطوة 2: قراءة ملخص مراجعة الصفحة

اقرأ ملخص مراجعة المحتوى للصفحة. هذا هو **revision summary example** الذي يُظهر من قام بتحرير الصفحة آخر مرة.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## الخطوة 3: تحديث ملخص مراجعة الصفحة

قم بتحديث ملخص مراجعة الصفحة بمؤلف جديد وتاريخ تعديل جديد. يوضح هذا كيفية **modify revision date** برمجيًا.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## الخلاصة

يمكن تبسيط إدارة مراجعات الصفحات في مستندات OneNote برمجيًا باستخدام Aspose.Note for Java. باتباع الخطوات الموضحة في هذا الدليل، يمكنك بفعالية **track changes onenote**، عرض تفاصيل المراجعة، وحتى **modify revision date** لتناسب سير عملك.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.Note for Java مع مكتبات Java أخرى؟
نعم، يمكن دمج Aspose.Note for Java مع مكتبات Java أخرى لتعزيز الوظائف.

### س2: هل يدعم Aspose.Note for Java جميع إصدارات مستندات OneNote؟
يدعم Aspose.Note for Java إصدارات مختلفة من مستندات OneNote، بما في ذلك الإصدارات القديمة.

### س3: هل Aspose.Note for Java مناسب لتطبيقات المستوى المؤسسي؟
بالطبع، تم تصميم Aspose.Note for Java لتلبية احتياجات التطبيقات على مستوى المؤسسات مع ميزات قوية وقابلية التوسع.

### س4: هل يمكنني تخصيص مراجعات الصفحات باستخدام Aspose.Note for Java؟
نعم، يمكنك تخصيص مراجعات الصفحات وفقًا لمتطلباتك باستخدام Aspose.Note for Java.

### س5: أين يمكنني الحصول على الدعم لـ Aspose.Note for Java؟
يمكنك الحصول على الدعم لـ Aspose.Note for Java من [Aspose.Note forum](https://forum.aspose.com/c/note/28).

---

**Last Updated:** 2026-01-15  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}