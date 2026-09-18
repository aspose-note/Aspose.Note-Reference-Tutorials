---
date: 2026-03-05
description: تعلم كيفية حفظ OneNote كملف PDF أثناء إنشاء قائمة مرقمة باستخدام Aspose.Note
  للغة Java. يتضمن الخطوات لتعيين نمط النص الافتراضي وتخصيص الترقيم.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: حفظ OneNote كملف PDF – إنشاء قائمة مرقمة باستخدام Aspose.Note
url: /ar/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ OneNote كملف PDF – إنشاء قائمة مرقمة باستخدام Aspose.Note

## المقدمة
Aspose.Note for Java تمكّن مطوري Java من **حفظ OneNote كملف PDF** وإثراء المستند بتنسيقات متقدمة، مثل القوائم المرقمة. في هذا البرنامج التعليمي، سنرشدك خلال العملية الكاملة — من تعيين نمط النص الافتراضي إلى تخصيص تنسيق الترقيم — حتى تتمكن من تصدير OneNote إلى PDF بمظهر احترافي.

## إجابات سريعة
- **ما الذي يغطيه هذا البرنامج التعليمي؟** إنشاء قائمة مرقمة في OneNote وحفظ الملف كـ PDF باستخدام Aspose.Note for Java.  
- **ما هي الكلمة المفتاحية الأساسية المستهدفة؟** *save onenote as pdf*  
- **هل أحتاج إلى ترخيص؟** يتوفر إصدار تجريبي مجاني؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **ما نسخة Java المطلوبة؟** JDK 8 أو أحدث.  
- **كم من الوقت تستغرق عملية التنفيذ؟** حوالي 10–15 دقيقة لقائمة أساسية.

## ما هو “حفظ OneNote كملف PDF”؟
حفظ OneNote كملف PDF يحوّل صفحة OneNote ذات النص الغني إلى مستند ثابت قابل للنقل يمكن مشاركته عبر المنصات دون الحاجة إلى OneNote. هذا مفيد بشكل خاص للأرشفة، والتقارير، أو توزيع المحتوى على المستخدمين الذين لا يمتلكون OneNote مثبتًا.

## لماذا إنشاء قائمة مرقمة قبل التصدير؟
القائمة المرقمة تضيف هيكلًا وقابلية قراءة، مما يجعل ملف PDF المُصدّر يبدو كأنه تقرير مصقول. مع Aspose.Note يمكنك **تخصيص تنسيق الترقيم**، وتعيين الخطوط، والتحكم في التباعد — كل ذلك مع الحفاظ على تخطيط OneNote الأصلي.

## المتطلبات المسبقة
قبل البدء، تأكد من وجود:

- Java Development Kit (JDK) مثبت على جهازك.  
- مكتبة Aspose.Note for Java تم تحميلها من [here](https://releases.aspose.com/note/java/).  

## استيراد الحزم
أولاً، استورد الفئات المطلوبة حتى تتمكن من العمل مع كائنات OneNote وتحويلها إلى PDF.

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

## كيفية حفظ OneNote كملف PDF مع قائمة مرقمة؟
فيما يلي دليل خطوة بخطوة يوضح **كيفية إنشاء عناصر القائمة**، **تعيين نمط النص الافتراضي**، وأخيرًا **تصدير OneNote إلى PDF**.

### الخطوة 1: تهيئة كائنات Document و Page و Outline
نبدأ بإنشاء هياكل OneNote الأساسية. هذا يوضح أيضًا استخدام **add outline element java**.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **نصيحة احترافية:** احتفظ بمسار `dataDir` مطلقًا أو استخدم `System.getProperty("user.dir")` لتجنب مشاكل المسار.

### الخطوة 2: تعيين نمط النص الافتراضي
نمط موحد يضمن أن القائمة تبدو متناسقة عبر جميع العناصر.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### الخطوة 3: إنشاء عناصر Outline (قائمة مرقمة)
هنا **نخصص تنسيق الترقيم** باستخدام `NumberList`. النمط `"{0})"` ينتج “1)”، “2)”، إلخ.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **لماذا هذا مهم:** من خلال إرفاق `NumberList` بكل `OutlineElement`، تحصل على تحكم كامل في نمط الترقيم، الخط، والحجم.

### الخطوة 4: إضافة عناصر Outline إلى الـ Outline
الآن نجمع عناصر القائمة الفردية في مخطط واحد.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### الخطوة 5: إرفاق Outline بالصفحة
يصبح الـ Outline جزءًا من هيكل صفحة OneNote.

```java
page.appendChildLast(outline);
```

### الخطوة 6: حفظ المستند كملف PDF
أخيرًا، **نحفظ OneNote كملف PDF**. سيحتوي ملف الإخراج على القائمة المرقمة كما تم تعريفها.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

تشغيل الكود أعلاه يولد ملف PDF باسم `CreateNumberedList_out.pdf` في الدليل المحدد، مع الحفاظ على تنسيق القائمة المرقمة.

## المشكلات الشائعة والحلول
| المشكلة | الحل |
|-------|----------|
| **ملف PDF فارغ** | تأكد من استدعاء `doc.appendChildLast(page);` قبل `doc.save()`. |
| **عدم ظهور الترقيم** | تحقق من أن نمط `NumberList` و `NumberFormat` تم تعيينهما بشكل صحيح. |
| **خطأ ملف غير موجود** | استخدم مسارًا مطلقًا لـ `dataDir` أو أنشئ الدليل مسبقًا. |
| **عدم تطابق الخط** | قم بتثبيت الخط (مثل Arial) على الجهاز الذي يشغل الكود. |

## الأسئلة المتكررة
### س: هل يمكنني تخصيص تنسيق الترقيم في قائمة OneNote الخاصة بي؟
ج: بالطبع! يمكنك تخصيص تنسيق الترقيم باستخدام الفئة `NumberList` المقدمة من Aspose.Note for Java.

### س: هل تتوفر نسخة تجريبية من Aspose.Note for Java؟
ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س: كيف يمكنني الحصول على الدعم لـ Aspose.Note for Java؟
ج: قم بزيارة [منتدى Aspose.Note for Java](https://forum.aspose.com/c/note/28) للحصول على دعم المجتمع.

### س: أين يمكنني العثور على الوثائق التفصيلية لـ Aspose.Note for Java؟
ج: ارجع إلى [الوثائق](https://reference.aspose.com/note/java/) للحصول على معلومات شاملة.

### س: كيف أشتري ترخيصًا لـ Aspose.Note for Java؟
ج: يمكنك شراء ترخيص [هنا](https://purchase.aspose.com/buy).

## الخلاصة
في هذا البرنامج التعليمي أظهرنا كيفية **حفظ OneNote كملف PDF** مع إنشاء قائمة مرقمة نظيفة باستخدام Aspose.Note for Java. من خلال تعيين نمط النص الافتراضي، تخصيص تنسيق الترقيم، واتباع الدليل خطوة بخطوة، يمكنك توليد ملفات PDF احترافية من صفحات OneNote بسرعة وموثوقية.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-03-05  
**تم الاختبار مع:** Aspose.Note for Java 24.11  
**المؤلف:** Aspose  

---