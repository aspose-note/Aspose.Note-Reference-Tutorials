---
title: إنشاء جدول بأعمدة مقفلة في OneNote - Aspose.Note
linktitle: إنشاء جدول بأعمدة مقفلة في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: عزز تجربة OneNote الخاصة بك مع Aspose.Note لـ Java. تعرف على كيفية إنشاء جداول ذات أعمدة مقفلة باستخدام دليل خطوة بخطوة. تحميل النسخة التجريبية المجانية من الآن!
weight: 12
url: /ar/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء جدول بأعمدة مقفلة في OneNote - Aspose.Note

## مقدمة
يعد OneNote أداة قوية لتنظيم المعلومات، كما يعمل Aspose.Note for Java على تحسين قدراته من خلال توفير طريقة سلسة لإنشاء جداول ذات أعمدة مقفلة. في هذا البرنامج التعليمي، سنرشدك خلال عملية استخدام Aspose.Note لـ Java لإنشاء جدول بأعمدة مقفلة في OneNote.
## المتطلبات الأساسية
قبل البدء، تأكد من توفر المتطلبات الأساسية التالية:
- [مجموعة تطوير جافا (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)المثبتة على جهازك.
- [Aspose.Note لجافا](https://downloads.aspose.com/note/java) المكتبة التي تم تنزيلها وإضافتها إلى مشروعك.
## حزم الاستيراد
في مشروع Java الخاص بك، قم باستيراد الحزم اللازمة للعمل مع Aspose.ملاحظة:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## الخطوة 1: قم بإعداد مشروعك
ابدأ بإنشاء مشروع Java جديد وإضافة مكتبة Aspose.Note إلى مسار الفصل الدراسي الخاص بك. تأكد من تكوين مشروعك لاستخدام JDK.
## الخطوة 2: تهيئة كائنات المستند والصفحة
```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory";
//قم بإنشاء كائن من فئة المستند
Document doc = new Document();
// تهيئة كائن فئة الصفحة
Page page = new Page();
```
## الخطوة 3: إنشاء صفوف وخلايا الجدول
```java
// تهيئة كائن فئة TableRow
TableRow row1 = new TableRow();
// تهيئة كائن فئة TableCell وتعيين محتوى النص
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// تهيئة كائن فئة TableRow
TableRow row2 = new TableRow();
// تهيئة كائن فئة TableCell وتعيين محتوى النص
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## الخطوة 4: إنشاء الجدول وتخصيصه
```java
// تهيئة كائن فئة الجدول
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// إضافة صفوف
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## الخطوة 5: إضافة جدول إلى المخطط التفصيلي والصفحة
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// إضافة عقدة الجدول
outlineElem.appendChildLast(table);
// إضافة عقدة عنصر المخطط التفصيلي
outline.appendChildLast(outlineElem);
// إضافة عقدة المخطط التفصيلي
page.appendChildLast(outline);
// إضافة عقدة الصفحة
doc.appendChildLast(page);
```
## الخطوة 6: احفظ المستند
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
تهانينا! لقد نجحت في إنشاء جدول يحتوي على أعمدة مقفلة في OneNote باستخدام Aspose.Note لـ Java.
## خاتمة
في هذا البرنامج التعليمي، استكشفنا عملية استخدام Aspose.Note لـ Java لتحسين تجربة OneNote الخاصة بك عن طريق إنشاء جداول ذات أعمدة مقفلة. تضيف هذه الوظيفة طبقة جديدة من التنظيم والبنية إلى ملاحظاتك.
## الأسئلة الشائعة
### هل Aspose.Note for Java متوافق مع جميع إصدارات Java؟
نعم، Aspose.Note for Java متوافق مع Java 6 والإصدارات الأحدث.
### هل يمكنني تخصيص مظهر الجدول بشكل أكبر؟
قطعاً! يوفر Aspose.Note for Java خيارات شاملة لتخصيص الجداول، مثل ضبط الحدود وتباعد الخلايا والمزيد.
### هل هناك نسخة تجريبية متاحة قبل الشراء؟
 نعم يمكنك ذلك[تنزيل نسخة تجريبية مجانية](https://releases.aspose.com/) لاستكشاف إمكانيات Aspose.Note لـ Java.
### أين يمكنني العثور على دعم إضافي أو مناقشات مجتمعية؟
 قم بزيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على الدعم والمناقشات المجتمعية.
### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note لـ Java؟
 يزور[هذا الرابط](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت لأغراض الاختبار.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
