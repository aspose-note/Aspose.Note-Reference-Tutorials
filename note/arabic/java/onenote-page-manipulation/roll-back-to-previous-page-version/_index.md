---
date: 2026-01-12
description: تعلم كيفية التراجع عن صفحات OneNote واستعادة النسخة السابقة من OneNote
  باستخدام Aspose.Note للغة Java. اتبع هذا الدليل خطوة بخطوة لإدارة مستندات فعّالة.
linktitle: How to Roll Back OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: كيفية التراجع عن OneNote - Aspose.Note
url: /ar/java/onenote-page-manipulation/roll-back-to-previous-page-version/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية التراجع عن OneNote - Aspose.Note

## Introduction

إذا كنت تبحث عن طريقة واضحة برمجية **how to roll back onenote** للصفحات عندما يحدث خطأ، فأنت في المكان الصحيح. في هذا الدرس سنستعرض كيفية استخدام Aspose.Note for Java لإرجاع صفحة OneNote إلى حالة سابقة. سواءً كنت تبني أداة إدارة ملاحظات آلية أو تحتاج إلى شبكة أمان للمفكرات التشاركية، فإن التراجع عن صفحة يساعد في الحفاظ على محتواك دقيقًا وموثوقًا.

## Quick Answers
- **ما معنى “التراجع” في OneNote؟** استعادة الصفحة إلى نسخة سابقة محفوظة في تاريخها.  
- **أي API يتعامل مع التراجع؟** الفئة `PageHistory` في Aspose.Note for Java.  
- **هل أحتاج إلى ترخيص؟** يلزم وجود ترخيص صالح لـ Aspose.Note للاستخدام في بيئة الإنتاج.  
- **هل يمكنني اختيار أي نسخة سابقة؟** نعم – يمكنك اختيار أي إدخال من قائمة تاريخ الصفحة.  
- **هل هذه الطريقة آمنة للملاحظات الكبيرة؟** بالتأكيد؛ العملية تعمل على صفحات فردية دون تحميل الدفتر بالكامل في الذاكرة.

## How to Roll Back OneNote Page Version
فيما يلي دليل مختصر خطوة بخطوة يوضح بالضبط كيفية تنفيذ التراجع. كل خطوة تتضمن شرحًا موجزًا لتفهم *لماذا* نقوم بذلك، وليس فقط *ماذا* نكتب.

## Prerequisites

قبل الغوص في الشيفرة، تأكد من جاهزية ما يلي:

### Java Development Environment Setup
1. **تثبيت مجموعة تطوير جافا (JDK):** احصل على أحدث JDK من موقع Oracle أو من مدير الحزم المفضل لديك.  
2. **تكوين متغيرات البيئة:** عيّن `JAVA_HOME` وقم بتحديث `PATH` بحيث تكون أوامر `java` و `javac` متاحة من سطر الأوامر.  
3. **إضافة Aspose.Note for Java:** حمّل المكتبة من [الموقع](https://purchase.aspose.com/buy) وأضف ملف JAR إلى مسار الفئة (classpath) في مشروعك.

## Import Packages

للتفاعل مع ملفات OneNote، استورد الفئات الأساسية من Aspose.Note:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Step 1: Load OneNote Document
```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
نحدد أولاً المجلد الذي يحتوي على ملف `.one` ونحمّله إلى كائن `Document`.

## Step 2: Get Page History
```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
توفر لك `PageHistory` إمكانية الوصول إلى كل نسخة محفوظة من الصفحة المحددة، مما يتيح قدرة **restore previous onenote version**.

## Step 3: Remove Current Page
```java
document.removeChild(page);
```
بإزالة الصفحة الحالية نُفسح المجال للنسخة التي نريد إعادتها.

## Step 4: Append Previous Page Version
```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
هنا نختار أحدث إدخال تاريخي (يمكنك تعديل الفهرس لاستهداف أي نسخة أقدم) ونضيفه مرة أخرى إلى المستند.

## Step 5: Save Document
```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
أخيرًا، احفظ الدفتر المعدل. الآن يحتوي ملف الإخراج على الصفحة التي تم التراجع عنها.

## Restore Previous OneNote Version
يجمع استخدام `PageHistory` مع `appendChildLast` بينهما لتتمكن من **restore previous onenote version** ببضع أسطر من الشيفرة فقط. هذا مفيد جدًا في سير العمل الآلي حيث لا يكون التراجع اليدوي ممكنًا.

## Common Issues & Tips
- **Empty History:** إذا أعاد `pageHistory.size()` القيمة 0، فهذا يعني أن الصفحة لا تملك نسخًا محفوظة—تأكد من تفعيل النسخ الاحتياطي في OneNote.  
- **Index Out of Bounds:** تذكر أن قائمة التاريخ تبدأ من الصفر. عدّل الفهرس (`size() - 1`) لاستهداف النسخة الدقيقة التي تحتاجها.  
- **Performance:** العمل على صفحة واحدة يتجنب تحميل الدفتر بالكامل في الذاكرة، مما يحافظ على سرعة العملية حتى مع الملفات الكبيرة.

## Conclusion

أصبح لديك الآن طريقة كاملة وجاهزة للإنتاج **how to roll back onenote** باستخدام Aspose.Note for Java. من خلال الاستفادة من `PageHistory`، يمكنك استعادة أي حالة سابقة لصفحة الدفتر بأمان، مما يضمن سلامة البيانات ويمنح المستخدمين الثقة في بيئات التعاون.

## Frequently Asked Questions

**Q1: هل يمكنني التراجع عن عدة نسخ من صفحة؟**  
A: نعم، يمكنك الوصول إلى تاريخ الصفحة بالكامل والتراجع إلى أي نسخة سابقة حسب الحاجة.

**Q2: هل يدعم Aspose.Note لغات برمجة أخرى غير Java؟**  
A: نعم، يوفر Aspose.Note مكتبات لعدة لغات برمجة، بما في ذلك .NET و C++ و Python.

**Q3: هل Aspose.Note متوافق مع جميع إصدارات OneNote؟**  
A: يدعم Aspose.Note صيغ OneNote المتنوعة، مما يضمن التوافق مع معظم إصدارات المستندات.

**Q4: هل يمكنني أتمتة مهام أخرى في OneNote باستخدام Aspose.Note؟**  
A: بالتأكيد، يقدم Aspose.Note إمكانيات واسعة لإضافة وحذف وتعديل المحتوى برمجيًا.

**Q5: هل هناك منتدى مجتمع أو دعم متاح لـ Aspose.Note؟**  
A: نعم، يمكنك زيارة [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على دعم المجتمع أو التواصل مع دعم عملاء Aspose للمساعدة.

---

**Last Updated:** 2026-01-12  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}