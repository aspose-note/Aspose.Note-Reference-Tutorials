---
title: إنشاء مستند وإدراج صورة باستخدام الدفق في OneNote - Java
linktitle: إنشاء مستند وإدراج صورة باستخدام الدفق في OneNote - Java
second_title: Aspose.Note جافا API
description: تعرف على كيفية دمج الصور بسهولة في مستندات OneNote باستخدام Aspose.Note لـ Java. برنامج تعليمي خطوة بخطوة لمطوري Java.
type: docs
weight: 13
url: /ar/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---
## مقدمة

مرحبًا بك في برنامجنا التعليمي الشامل حول استخدام Aspose.Note لـ Java لإنشاء المستندات وإدراج الصور باستخدام تدفقات الصور في OneNote! في هذا البرنامج التعليمي، سنرشدك خلال العملية خطوة بخطوة، مما يضمن أن لديك فهمًا واضحًا لكل مرحلة. وفي النهاية، ستتمكن من دمج الصور بسهولة في مستندات OneNote الخاصة بك باستخدام Java.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

### مجموعة تطوير جافا (JDK)

تأكد من تثبيت Java Development Kit (JDK) على نظامك. يمكنك تنزيله من موقع أوراكل.

### Aspose.Note لمكتبة جافا

 قم بتنزيل وتثبيت Aspose.Note لمكتبة Java من المتوفرة[وصلة](https://releases.aspose.com/note/java/).

### إعداد إيد

قم بإعداد بيئة التطوير المتكاملة (IDE) الخاصة بك بالتكوينات اللازمة للعمل مع مشاريع Java.

## حزم الاستيراد

للبدء، قم باستيراد الحزم المطلوبة إلى مشروع Java الخاص بك. ستوفر هذه الحزم الوظائف اللازمة للعمل مع مستندات وصور OneNote.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## الخطوة 1: إعداد دليل المستندات

 حدد الدليل الذي توجد به المستندات والصور الخاصة بك. يستبدل`"Your Document Directory"` مع المسار إلى الدليل الخاص بك.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: إنشاء كائن المستند

 تهيئة مثيل لـ`Document` لبدء العمل مع مستند OneNote الخاص بك.

```java
Document doc = new Document();
```

## الخطوة 3: تهيئة كائن الصفحة

 إنشاء`Page` كائن لتمثيل الصفحة داخل المستند.

```java
Page page = new Page();
```

## الخطوة 4: إنشاء المخطط التفصيلي

 تهيئة ان`Outline` كائن لتنظيم المحتوى داخل الصفحة.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## الخطوة 5: إنشاء عنصر المخطط التفصيلي

 يخترع`OutlineElement` للإمساك بالصورة وتحديد موضعها.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## الخطوة 6: تحميل دفق الصور

 قم بتحميل دفق الصورة باستخدام`FileInputStream` للصورة المطلوبة.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## الخطوة 7: إدراج الصورة

 أدخل الصورة في المستند عن طريق إنشاء ملف`Image` الكائن وتحديد محاذاته.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## الخطوة 8: إلحاق الصورة بعنصر المخطط التفصيلي

إلحاق الصورة بعنصر المخطط التفصيلي.

```java
outlineElem1.appendChildLast(image);
```

## الخطوة 9: إلحاق عنصر المخطط التفصيلي بالمخطط التفصيلي

أضف عنصر المخطط التفصيلي إلى المخطط التفصيلي.

```java
outline1.appendChildLast(outlineElem1);
```

## الخطوة 10: إلحاق المخطط التفصيلي بالصفحة

أضف المخطط التفصيلي إلى الصفحة.

```java
page.appendChildLast(outline1);
```

## الخطوة 11: إلحاق الصفحة بالمستند

وأخيرًا، قم بإلحاق الصفحة بالمستند.

```java
doc.appendChildLast(page);
```

## الخطوة 12: حفظ المستند

احفظ المستند المعدل، مع تحديد التنسيق المطلوب (على سبيل المثال، PDF).

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf"، SaveFormat.Pdf)؛
} catch (IOException e) {
    e.printStackTrace();
}
```

باتباع هذه الخطوات، يمكنك إنشاء المستندات وإدراج الصور بسهولة باستخدام تدفقات الصور في OneNote باستخدام Aspose.Note لـ Java.

## خاتمة

في الختام، يمكن أن يؤدي إتقان دمج الصور في مستندات OneNote باستخدام Java إلى تحسين عملية إنشاء المستندات بشكل كبير. مع Aspose.Note for Java، لديك أداة قوية تحت تصرفك لإنجاز هذه المهمة بسلاسة.

## الأسئلة الشائعة

### س1: هل Aspose.Note for Java متوافق مع كافة إصدارات OneNote؟

ج1: يدعم Aspose.Note for Java إصدارات مختلفة من OneNote، مما يضمن التوافق عبر بيئات مختلفة.

### س2: هل يمكنني تخصيص مظهر الصور المدرجة في مستندات OneNote باستخدام Aspose.Note لـ Java؟

ج2: نعم، يمكنك تخصيص جوانب مختلفة من الصور المدرجة، مثل المحاذاة والحجم والاتجاه، لتناسب متطلباتك المحددة.

### س3: هل يوفر Aspose.Note for Java الدعم لتنسيقات المستندات الأخرى إلى جانب PDF؟

ج3: نعم، يدعم Aspose.Note for Java نطاقًا واسعًا من تنسيقات المستندات، بما في ذلك DOCX وHTML والمزيد، مما يمنحك المرونة في مهام إدارة المستندات الخاصة بك.

### س4: أين يمكنني العثور على موارد ودعم إضافيين لـ Aspose.Note لـ Java؟

ج4: يمكنك الوصول إلى الوثائق وروابط التنزيل ومنتديات الدعم والتراخيص المؤقتة لـ Aspose.Note لـ Java من خلال الروابط المتوفرة.

### س5: هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ Java؟

ج5: نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Note لـ Java لاستكشاف ميزاته وإمكانياته قبل اتخاذ قرار الشراء.
