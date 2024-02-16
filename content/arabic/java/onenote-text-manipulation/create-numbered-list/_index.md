---
title: إنشاء قائمة مرقمة في OneNote - Aspose.Note
linktitle: إنشاء قائمة مرقمة في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرف على كيفية إنشاء قائمة مرقمة بسهولة في OneNote باستخدام Aspose.Note لـ Java. قم بتنزيل نسخة تجريبية مجانية وانغمس في عالم تطوير Java!
type: docs
weight: 14
url: /ar/java/onenote-text-manipulation/create-numbered-list/
---
## مقدمة
يعمل Aspose.Note for Java على تمكين مطوري Java من العمل بسلاسة مع ملفات Microsoft OneNote. في هذا البرنامج التعليمي، سنرشدك خلال عملية إنشاء قائمة مرقمة في OneNote باستخدام مكتبة Aspose.Note القوية لـ Java.
## المتطلبات الأساسية
قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
- تم تثبيت Java Development Kit (JDK) على جهازك.
-  تم تنزيل Aspose.Note لمكتبة Java من[هنا](https://releases.aspose.com/note/java/).
## استيراد الحزم
أولاً، لنستورد الحزم الضرورية في مشروع Java الخاص بك لتحقيق أقصى استفادة من وظائف Aspose.Note. قم بتضمين الكود التالي في مشروعك:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## الخطوة 1: تهيئة كائنات المستند والصفحة والمخطط التفصيلي
```java
// دليل المستندات الخاص بك
String dataDir = "Your Document Directory";
// إنشاء كائنات المستند والصفحة والمخطط التفصيلي
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// ضبط نمط النص الافتراضي
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## الخطوة 2: تحديد نمط النص الافتراضي
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## الخطوة 3: إنشاء عناصر المخطط التفصيلي
الآن، لنقم بإنشاء العناصر لقائمتك المرقمة.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// كرر ذلك مع العناصر الأخرى (outlineElem2 وoutlineElem3)
```
## الخطوة 4: إضافة عناصر المخطط التفصيلي إلى المخطط التفصيلي
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## الخطوة 5: إضافة المخطط التفصيلي إلى الصفحة
```java
page.appendChildLast(outline);
```
## الخطوة 6: حفظ المستند
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
اتبع هذه الخطوات بدقة، وستتمكن بسهولة من إنشاء قائمة مرقمة في OneNote باستخدام Aspose.Note لـ Java.
## خاتمة
في هذا البرنامج التعليمي، استكشفنا العملية السلسة لإنشاء قائمة مرقمة في OneNote باستخدام Aspose.Note لـ Java. إن الميزات القوية للمكتبة تجعلها أداة لا تقدر بثمن لمطوري Java الذين يعملون مع ملفات Microsoft OneNote.
## أسئلة مكررة
### س: هل يمكنني تخصيص تنسيق الترقيم في قائمة OneNote الخاصة بي؟
ج: بالتأكيد! يمكنك تخصيص تنسيق الترقيم باستخدام فئة NumberList التي توفرها Aspose.Note لـ Java.
### س: هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ Java؟
 ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).
### س: كيف يمكنني الحصول على دعم Aspose.Note لـ Java؟
 ج: قم بزيارة[Aspose.Note لمنتدى جافا](https://forum.aspose.com/c/note/28) لدعم المجتمع.
### س: أين يمكنني العثور على الوثائق التفصيلية لـ Aspose.Note لـ Java؟
 ج: راجع[توثيق](https://reference.aspose.com/note/java/) للحصول على معلومات شاملة.
### س: كيف يمكنني شراء ترخيص Aspose.Note لـ Java؟
 ج: يمكنك شراء ترخيص[هنا](https://purchase.aspose.com/buy).