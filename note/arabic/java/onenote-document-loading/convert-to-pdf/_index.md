---
date: 2025-11-30
description: تعلم كيفية تحويل مستندات OneNote إلى PDF باستخدام Aspose.Note للـ Java.
  يوضح لك هذا الدليل خطوة بخطوة كيفية حفظ OneNote كملف PDF، وتحويل صفحات محددة، ودمج
  الحل في مشاريع Java الخاصة بك.
language: ar
linktitle: Convert OneNote to PDF - Java
second_title: Aspose.Note Java API
title: تحويل OneNote إلى PDF - Java
url: /java/onenote-document-loading/convert-to-pdf/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل OneNote إلى PDF - Java

## المقدمة

في هذا الدرس، سنستكشف كيفية **تحويل OneNote إلى PDF** باستخدام Aspose.Note for Java. Aspose.Note هي مكتبة Java قوية تتيح لك التعامل مع ملفات OneNote وحفظ OneNote كـ **PDF** بسهولة. سواء كنت بحاجة إلى إنشاء ملف PDF واحد للدفتر بأكمله أو فقط **تحويل صفحات محددة إلى PDF**، فإن هذا الدليل يمرّ بك عبر العملية بالكامل مع أمثلة واضحة وعملية.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.Note for Java  
- **هل يمكنني تحويل الصفحات المحددة فقط؟** نعم – استخدم `PdfSaveOptions.setPageIndex` و `setPageCount`  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** الترخيص التجاري مطلوب للاستخدام غير التجريبي  
- **ما نسخة Java المدعومة؟** JDK 8 أو أحدث (يوصى بـ JDK 15)  
- **هل ملف PDF الناتج قابل للبحث؟** نعم، PDF المُولد يحتفظ بالنص القابل للبحث بشكل افتراضي  

## ما هو “تحويل OneNote إلى PDF”؟
تحويل دفتر OneNote إلى PDF يعني أخذ ملف OneNote الغني متعدد الصفحات (`.one`) وتحويله إلى مستند PDF مسطح يمكن عرضه على أي منصة. هذا مفيد للمشاركة، الأرشفة، أو طباعة الملاحظات دون الحاجة إلى تطبيق OneNote.

## لماذا تحويل OneNote إلى PDF باستخدام Aspose.Note؟
- **بدون اعتماد على Microsoft Office** – يعمل على أي منصة تدعم Java.  
- **تحكم دقيق** – يمكنك اختيار صفحات فردية، ضبط جودة الصور، وتضمين الخطوط.  
- **دقة عالية** – يتم الحفاظ على التخطيط والجداول والصور تمامًا كما تظهر في OneNote.  
- **تكامل سهل** – بضع أسطر من الشيفرة تتكامل طبيعيًا مع تطبيقات Java الحالية.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

1. **Java Development Kit (JDK)** – JDK 8+ مثبت. يمكنك تنزيله من [هنا](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).  
2. **Aspose.Note for Java** – حمّل أحدث JAR من [هنا](https://releases.aspose.com/note/java/).  

## استيراد الحزم

للبدء، استورد الفئات الضرورية إلى مشروع Java الخاص بك. هذه الفئات تتيح لك تحميل ملف OneNote وتعريف خيارات تصدير PDF.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

### الخطوة 1: تحميل مستند OneNote

أولاً، حمّل ملف OneNote الذي تريد تحويله.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

استبدل `"Your Document Directory"` بالمسار المطلق أو النسبي إلى ملف `.one` الخاص بك.

### الخطوة 2: تهيئة `PdfSaveOptions`

أنشئ كائن `PdfSaveOptions` الذي سيحمل جميع إعدادات PDF.

```java
PdfSaveOptions options = new PdfSaveOptions();
```

### الخطوة 3: حفظ OneNote كـ PDF (أو تحويل صفحات محددة إلى PDF)

يمكنك تحويل الدفتر بالكامل، أو تحديد نطاق من الصفحات للتحويل.

```java
// Set page index (zero‑based). Uncomment to start from page 2.
// options.setPageIndex(2);

// Set page count. Uncomment to export only 3 pages starting from the index above.
// options.setPageCount(3);
```

*إذا تركت السطرين معلقين، سيقوم Aspose.Note بتحويل المستند بالكامل.*

### الخطوة 4: حفظ المستند كـ PDF

الآن اكتب ملف PDF إلى القرص باستخدام الخيارات التي عرّفتها.

```java
oneFile.save(dataDir + "ConvertToPdf_out.pdf", options);
```

### الخطوة 5: عرض رسالة النجاح

رسالة في وحدة التحكم تؤكد أن التحويل نجح.

```java
System.out.println("File saved: " + dataDir + "ConvertToPdf_out.pdf");
```

## المشكلات الشائعة والنصائح

- **الملف غير موجود** – تحقق مرة أخرى من مسار `dataDir` وتأكد من وجود ملف `.one`.  
- **صفحات PDF فارغة** – تأكد من أن ملف OneNote المصدر يحتوي فعلاً على محتوى في الصفحات التي تصدرها.  
- **دفاتر كبيرة** – فكر في التحويل على دفعات (استخدم `setPageIndex`/`setPageCount`) لتقليل استهلاك الذاكرة.  
- **أخطاء الترخيص** – النسخة التجريبية تضيف علامة مائية؛ قم بتطبيق ترخيص صالح للإصدارات الإنتاجية.

## الأسئلة المتكررة

**س: هل Aspose.Note متوافق مع جميع إصدارات OneNote؟**  
ج: يدعم Aspose.Note الملفات التي أنشأتها إصدارات OneNote 2007، 2010، 2013، 2016، وأحدث نسخة Windows 10.

**س: هل يمكنني تخصيص إعدادات تحويل PDF؟**  
ج: نعم. استخدم فئة `PdfSaveOptions` لضبط جودة الصورة، تضمين الخطوط، تحديد حجم الصفحة، وأكثر.

**س: هل Aspose.Note يتطلب ترخيصًا للاستخدام التجاري؟**  
ج: نعم، الترخيص التجاري مطلوب للإنتاج. يمكنك الحصول عليه [هنا](https://purchase.aspose.com/buy).

**س: هل الدعم الفني متاح لمستخدمي Aspose.Note؟**  
ج: بالطبع. يمكنك الوصول إلى منتدى الدعم [هنا](https://forum.aspose.com/c/note/28).

**س: هل يمكن تجربة Aspose.Note قبل الشراء؟**  
ج: نسخة تجريبية مجانية متاحة للتحميل [هنا](https://releases.aspose.com/).

---

**آخر تحديث:** 2025-11-30  
**تم الاختبار مع:** Aspose.Note for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}