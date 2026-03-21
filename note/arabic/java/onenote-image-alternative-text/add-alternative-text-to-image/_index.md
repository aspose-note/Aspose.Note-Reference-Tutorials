---
date: 2026-03-21
description: تعلم كيفية إنشاء مستند OneNote وتعيين النص البديل للصور باستخدام Java
  مع Aspose.Note. يوضح هذا الدليل أيضًا كيفية حفظ ملف OneNote وتحسين إمكانية الوصول.
linktitle: Create OneNote Document & Add Alt Text to Images in Java
second_title: Aspose.Note Java API
title: إنشاء مستند OneNote وإضافة نص بديل للصور في Java
url: /ar/java/onenote-image-alternative-text/add-alternative-text-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء مستند OneNote وإضافة نص بديل للصور في Java

## Introduction

في هذا الدرس ستتعلم **كيفية إنشاء مستند OneNote** برمجيًا و**تعيين نص بديل للصور** باستخدام Java و Aspose.Note API. إضافة النص البديل تجعل صفحات OneNote قابلة للوصول لمستخدمي قارئات الشاشة، تحسن قابلية البحث، وتساعدك على **حفظ ملف OneNote** ببيانات وصفية أغنى. بنهاية الدليل ستكون قادرًا على **إضافة صورة إلى صفحات OneNote**، تعيين كل من العنوان والوصف للصورة، وحفظ الملف على القرص.

## Quick Answers
- **ما المكتبة المطلوبة؟** Aspose.Note for Java  
- **ما الكلمة المفتاحية الأساسية التي يستهدفها هذا الدرس؟** create onenote document  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم، يلزم ترخيص تجاري (يتوفر نسخة تجريبية مجانية).  
- **هل يمكنني إضافة نص بديل لعدة صور؟** بالتأكيد – فقط كرّر الخطوات لكل صورة.  
- **ما نسخة Java المدعومة؟** Java 8 أو أعلى.

## What is “create onenote document” in the context of OneNote?

إنشاء مستند OneNote يعني بناء ملف `.one` برمجيًا يمكن أن يحتوي على صفحات، نص، صور، ومحتوى غني آخر. باستخدام Aspose.Note يمكنك توليد هذا الملف من الصفر، إضافة عناصر، ثم **حفظ ملف OneNote** في أي موقع.

## Why add alt text to images in OneNote?

- **إمكانية الوصول:** يفي بإرشادات WCAG ويساعد المستخدمين ذوي الإعاقات البصرية.  
- **قابلية البحث:** يمكن لمحركات البحث فهرسة الوصف، مما يجعل محتواك أكثر اكتشافًا.  
- **الاحترافية:** يظهر التزامًا بالتصميم الشامل وجودة الوثائق.

## Prerequisites

قبل الغوص في الدرس، تأكد من توفر المتطلبات التالية:

1. Java Development Kit (JDK) – الإصدار 8 أو أحدث.  
2. مكتبة Aspose.Note for Java – قم بتنزيلها من [here](https://releases.aspose.com/note/java/).  
3. بيئة تطوير متكاملة مثل IntelliJ IDEA أو Eclipse.  
4. معرفة أساسية ببرمجة Java.

## Import Packages

أولًا، استورد الحزم اللازمة في مشروع Java لاستخدام وظائف Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

الآن، دعنا نتبع **الدليل خطوة بخطوة** لإنشاء **مستند OneNote**، إضافة صورة، و**تعيين نص بديل للصورة**.

## How to Create OneNote Document and Set Image Alt Text in Java

### Step 1: Set Up Document Directory

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار المطلق حيث توجد صورة المصدر الخاصة بك وحيث تريد حفظ ملف `.one` الناتج.

### Step 2: Create a Document Object

```java
Document document = new Document();
```

هذا السطر **ينشئ مستند OneNote جديد** ستقوم لاحقًا **بحفظ ملف OneNote** مع المحتوى المضاف.

### Step 3: Create a Page Object

```java
Page page = new Page();
```

الصفحة تعمل كقماش للصورة وأي عناصر أخرى قد ترغب في إضافتها.

### Step 4: Add an Image to the Page

```java
Image image = new Image(null, dataDir + "image.jpg");
```

المُنشئ `Image` يحمل ملف الصورة من المسار المحدد. هذه هي النقطة التي ستقوم فيها **بإضافة صورة إلى OneNote**.

### Step 5: Set Alternative Text Title (Set Image Alt Text)

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

هنا **نحدد نص بديل للعنوان** الذي يعمل كعنوان مختصر للصورة.

### Step 6: Set Alternative Text Description (Set Alt Text Description)

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

الوصف يقدم شرحًا أكثر تفصيلاً—مثالي لقارئات الشاشة.

### Step 7: Append Image to the Page

```java
page.appendChildLast(image);
```

الآن الصورة، الم enriched بنصها البديل، **تمت إضافتها إلى صفحة OneNote**.

### Step 8: Append Page to the Document

```java
document.appendChildLast(page);
```

أرفق الصفحة إلى مستند OneNote الذي أنشأته مسبقًا.

### Step 9: Save the Document (Save OneNote File)

```java
document.save(dataDir + "AlternativeText_out.one");
```

استدعاء `save` **يكتب ملف OneNote** إلى القرص، مع الحفاظ على جميع بيانات النص البديل.

## Common Issues and Solutions

- **FileNotFoundException:** تحقق من أن `dataDir` يشير إلى المجلد الصحيح وأن `image.jpg` موجود.  
- **NullPointerException على الصورة:** تأكد من أن مسار الصورة صالح وأن الملف غير معطوب.  
- **أخطاء الترخيص:** استخدم ملف ترخيص Aspose.Note صالح أو شغّل في وضع التجربة للتقييم.

## Frequently Asked Questions

**س: هل يمكنني إضافة نص بديل لعدة صور داخل مستند واحد؟**  
ج: نعم، فقط كرّر الخطوات 4‑6 لكل صورة تريد توضيحها.

**س: ما صيغ الصور المدعومة لإضافة نص بديل؟**  
ج: يدعم Aspose.Note صيغ JPEG, PNG, GIF, BMP، والعديد من الصيغ الشائعة الأخرى.

**س: هل يمكن تعديل أو إزالة النص البديل بعد تعيينه؟**  
ج: بالتأكيد. استدعِ `setAlternativeTextTitle("")` أو `setAlternativeTextDescription("")` لمسح القيم، أو قدم سلاسل جديدة لتحديثها.

**س: هل توفر Aspose.Note واجهات برمجة تطبيقات للغات أخرى غير Java؟**  
ج: نعم، المكتبة متوفرة أيضًا لـ .NET، C++، وPython.

**س: أين يمكنني تنزيل نسخة تجريبية من Aspose.Note؟**  
ج: يمكنك الحصول على نسخة تجريبية مجانية من [here](https://releases.aspose.com/).

**س: كيف يمكنني برمجيًا **حفظ ملف OneNote** بعد إضافة عدة صفحات؟**  
ج: استدعِ `document.save(<outputPath>)` مرة واحدة بعد إرفاق جميع الصفحات والصور؛ ستتعامل API مع إنشاء الملف بالكامل.

**س: هل يمكنني استخدام نفس الكود **لإضافة صورة إلى OneNote** في مستند موجود؟**  
ج: نعم. حمّل المستند الموجود باستخدام `new Document(<filePath>)`، ثم اتبع الخطوات 3‑7 لإضافة صور جديدة ونص بديل.

## Conclusion

باتباع هذا الدليل، أصبحت الآن تعرف **كيفية إنشاء مستند OneNote**، **إضافة صورة إلى OneNote**، و**تعيين نص بديل للصور** باستخدام Java. تنفيذ هذه الخطوات لا يجعل ملفات OneNote أكثر قابلية للوصول فحسب، بل يحسن أيضًا اكتشافها وجودتها العامة. لا تتردد في تجربة عناوين وأوصاف مختلفة لتوصيل معنى كل صورة بأفضل شكل.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}