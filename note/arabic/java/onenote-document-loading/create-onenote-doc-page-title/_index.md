---
title: إنشاء مستند OneNote بعنوان الصفحة - Java
linktitle: إنشاء مستند OneNote بعنوان الصفحة - Java
second_title: Aspose.Note جافا API
description: تعرف على كيفية إنشاء مستندات OneNote مع عناوين الصفحات في Java باستخدام Aspose.Note لـ Java. برنامج تعليمي شامل مع أمثلة التعليمات البرمجية.
type: docs
weight: 17
url: /ar/java/onenote-document-loading/create-onenote-doc-page-title/
---
## مقدمة

في مجال تطوير Java، أصبحت إدارة مستندات OneNote ومعالجتها بسيطة وفعالة باستخدام Aspose.Note لـ Java. توفر واجهة برمجة تطبيقات Java القوية هذه للمطورين الأدوات اللازمة لإنشاء ملفات OneNote وتعديلها ومعالجتها برمجيًا، مما يوفر تكاملًا سلسًا في تطبيقاتهم. في هذا البرنامج التعليمي، سنتعمق في عملية إنشاء مستند OneNote بعنوان صفحة محدد باستخدام Aspose.Note لـ Java. من خلال اتباع الدليل التفصيلي الموضح أدناه، يمكن للمطورين الاستفادة بسهولة من إمكانات واجهة برمجة التطبيقات (API) هذه لتحسين تطبيقات Java الخاصة بهم من خلال وظائف إدارة مستندات OneNote القوية.

## المتطلبات الأساسية

قبل متابعة هذا البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

### بيئة تطوير جافا

تأكد من تثبيت Java Development Kit (JDK) على نظامك.

### Aspose.Note لمكتبة جافا

 قم بتنزيل وإعداد Aspose.Note لمكتبة Java. يمكنك العثور على رابط التحميل[هنا](https://releases.aspose.com/note/java/).

### بيئة التطوير المتكاملة (IDE)

اختر IDE الذي تفضله لتطوير Java. تشمل الاختيارات الشائعة IntelliJ IDEA أو Eclipse أو NetBeans.

## حزم الاستيراد

أولاً، قم باستيراد الحزم اللازمة من مكتبة Aspose.Note for Java لتسهيل إنشاء مستندات OneNote مع عناوين الصفحات.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

الآن، دعنا نقسم رمز المثال المقدم إلى خطوات متعددة لفهم عملية إنشاء مستند OneNote بعنوان صفحة في Java باستخدام Aspose.Note.

## الخطوة 1: إعداد دليل المستندات

حدد الدليل الذي تريد حفظ مستند OneNote فيه.

```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory";
```

## الخطوة 2: إنشاء كائن المستند

قم بتهيئة كائن من فئة المستند لبدء العمل مع مستند OneNote.

```java
//قم بإنشاء كائن من فئة المستند
Document doc = new Document();
```

## الخطوة 3: تهيئة كائن الصفحة

قم بإنشاء كائن صفحة لتمثيل الصفحة داخل مستند OneNote.

```java
// تهيئة كائن فئة الصفحة
Page page = new Page();
```

## الخطوة 4: تعيين نمط النص الافتراضي

حدد النمط الافتراضي لكل النص في المستند، بما في ذلك لون الخط واسمه وحجمه.

```java
// النمط الافتراضي لكل النص في المستند.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

## الخطوة 5: تعيين خصائص عنوان الصفحة

قم بتكوين خصائص عنوان الصفحة، مثل النص والتاريخ والوقت.

```java
// تعيين خصائص عنوان الصفحة
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

## الخطوة 6: تعيين عنوان الصفحة

قم بتعيين خصائص العنوان للصفحة.

```java
page.setTitle(title);
```

## الخطوة 7: إلحاق الصفحة بالمستند

أضف عقدة الصفحة إلى المستند.

```java
doc.appendChildLast(page);
```

## الخطوة 8: حفظ مستند OneNote

حدد دليل الإخراج واحفظ مستند OneNote الذي تم إنشاؤه.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// حفظ مستند OneNote
doc.save(dataDir);
```

## خاتمة

في الختام، يقدم Aspose.Note for Java حلاً قويًا لمطوري Java الذين يسعون إلى التعامل مع مستندات OneNote برمجيًا. من خلال اتباع الدليل التفصيلي المقدم في هذا البرنامج التعليمي، يمكن للمطورين إنشاء مستندات OneNote بسهولة مع عناوين صفحات محددة، مما يعزز وظائف تطبيقات Java الخاصة بهم.

## الأسئلة الشائعة

### س1: هل يتوافق Aspose.Note for Java مع الإصدارات المختلفة من Java؟

ج1: نعم، Aspose.Note for Java متوافق مع إصدارات مختلفة من Java، مما يضمن المرونة للمطورين.

### س2: هل يمكنني تخصيص نمط الخط وحجم عنوان الصفحة؟

ج2: بالتأكيد! يوفر Aspose.Note for Java خيارات شاملة لتخصيص نمط الخط ولونه وحجمه وفقًا لتفضيلاتك.

### س3: هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ Java؟

ج3: نعم، يمكنك الوصول إلى الإصدار التجريبي المجاني من Aspose.Note لـ Java لاستكشاف ميزاته قبل إجراء عملية شراء.

### س4: كيف يمكنني الحصول على دعم Aspose.Note لـ Java؟

ج4: يمكنك زيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على أي مساعدة فنية أو استفسارات تتعلق بـ Aspose.Note لـ Java.

### س5: هل يمكنني الحصول على ترخيص مؤقت لأغراض الاختبار؟

ج5: نعم، يمكنك الحصول على ترخيص مؤقت من Aspose لأغراض الاختبار والتقييم.