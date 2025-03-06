---
title: إدراج جدول في OneNote - Aspose.Note
linktitle: إدراج جدول في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرّف على كيفية إدراج الجداول في OneNote باستخدام Aspose.Note لـ Java. دليل خطوة بخطوة لإنشاء المحتوى الديناميكي. تعزيز المستندات الخاصة بك دون عناء.
weight: 16
url: /ar/java/onenote-table-manipulation/insert-table/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدراج جدول في OneNote - Aspose.Note

## مقدمة
إذا كنت تتطلع إلى تحسين مستندات OneNote الخاصة بك عن طريق إدراج الجداول برمجيًا، فإن Aspose.Note for Java هو الحل الأمثل لك. في هذا الدليل التفصيلي، سنرشدك خلال عملية إدراج جدول في مستند OneNote باستخدام مكتبة Java القوية الخاصة بـ Aspose.Note.
## المتطلبات الأساسية
قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
- بيئة تطوير Java: تأكد من تثبيت Java على نظامك.
-  Aspose.Note for Java: قم بتنزيل وتثبيت مكتبة Aspose.Note for Java من[هنا](https://releases.aspose.com/note/java/).
## حزم الاستيراد
ابدأ باستيراد الحزم الضرورية إلى مشروع Java الخاص بك. تعتبر هذه الحزم ضرورية للاستفادة من ميزات Aspose.Note لـ Java.
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException
```

## الخطوة 1: إنشاء مستند OneNote
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory";
Document doc = new Document();
// ... (بيانات الاستيراد الأخرى)
// ...(باقي الكود)
```
## الخطوة 2: تهيئة المستند والصفحة والجدول
```java
// تهيئة كائن فئة الصفحة
Page page = new Page();
// تهيئة كائن فئة TableRow
TableRow row1 = new TableRow();
// تهيئة كائنات فئة TableCell
TableCell cell11 = new TableCell();
TableCell cell12 = new TableCell();
TableCell cell13 = new TableCell();
// ... (رمز لإلحاق عناصر المخطط التفصيلي في خلية الجدول)
// إلحاق خلايا الجدول بالصفوف
row1.appendChildLast(cell11);
row1.appendChildLast(cell12);
row1.appendChildLast(cell13);
// ... (رمز تهيئة وإلحاق صفوف أخرى)
// تهيئة كائن فئة الجدول وتعيين عرض الأعمدة
Table table = new Table();
table.setBordersVisible(true);
// ... (كود إضافة الأعمدة)
// إلحاق صفوف الجدول بالجدول
table.appendChildLast(row1);
table.appendChildLast(row2);
// ... (رمز لإضافة جدول إلى عقدة عنصر المخطط التفصيلي)
```
## الخطوة 3: تهيئة المخطط التفصيلي وOutlineElement
```java
//تهيئة كائن المخطط التفصيلي
Outline outline = new Outline();
// تهيئة كائن OutlineElement
OutlineElement outlineElem = new OutlineElement();
// ... (رمز لإضافة جدول إلى عقدة عنصر المخطط التفصيلي)
// إضافة عنصر المخطط التفصيلي إلى المخطط التفصيلي
outline.appendChildLast(outlineElem);
// إضافة مخطط تفصيلي إلى عقدة الصفحة
page.appendChildLast(outline);
// إضافة صفحة إلى عقدة الوثيقة
doc.appendChildLast(page);
dataDir = dataDir + "InsertTable_out.one";
doc.save(dataDir);
```
## الخطوة 4: احصل على OutlineElement مع النص
```java
public static OutlineElement GetOutlineElementWithText(String text)
{
    OutlineElement outlineElem = new OutlineElement();
    ParagraphStyle textStyle = new ParagraphStyle()
                                        .setFontColor(Color.BLACK)
                                        .setFontName("Arial")
                                        .setFontSize(10);
    RichText richText = new RichText().append(text);
    richText.setParagraphStyle(textStyle);
    outlineElem.appendChildLast(richText);
    return outlineElem;
} 
```
## خاتمة
تهانينا! لقد تعلمت بنجاح كيفية إدراج الجداول في مستندات OneNote باستخدام Aspose.Note لـ Java. توفر هذه المكتبة القوية وظائف واسعة النطاق، مما يسمح لك بإنشاء محتوى ديناميكي وجذاب برمجيًا.
## أسئلة مكررة
### س: هل يمكنني تخصيص مظهر الجدول باستخدام Aspose.Note لـ Java؟
ج: نعم، يمكنك تخصيص جوانب مختلفة، بما في ذلك الحدود وعرض الأعمدة وتصميم الخلايا.
### س: هل Aspose.Note for Java مناسب لكل من المشاريع الشخصية والتجارية؟
ج: نعم، يمكن استخدام Aspose.Note for Java في كل من المشاريع الشخصية والتجارية.
### س: أين يمكنني العثور على دعم إضافي لـ Aspose.Note لـ Java؟
 ج: قم بزيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) لدعم المجتمع والمناقشات.
### س: هل يمكنني تجربة Aspose.Note لـ Java قبل الشراء؟
 ج: نعم، يمكنك استكشاف المكتبة مع أ[تجربة مجانية](https://releases.aspose.com/).
### س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note لـ Java؟
 ج: احصل على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
