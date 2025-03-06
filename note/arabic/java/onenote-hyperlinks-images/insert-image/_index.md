---
title: إدراج صورة في مستند OneNote باستخدام Java
linktitle: إدراج صورة في مستند OneNote باستخدام Java
second_title: Aspose.Note جافا API
description: تعرف على كيفية إدراج الصور في مستندات OneNote باستخدام Java مع Aspose.Note لمكتبة Java. اتبع دليلنا خطوة بخطوة للتكامل السلس.
weight: 16
url: /ar/java/onenote-hyperlinks-images/insert-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدراج صورة في مستند OneNote باستخدام Java

## مقدمة

في هذا البرنامج التعليمي، سوف نستكشف كيفية إدراج صورة في مستند OneNote باستخدام Java بمساعدة Aspose.Note for Java. Aspose.Note for Java هي مكتبة قوية تتيح للمطورين العمل مع ملفات Microsoft OneNote برمجياً، مما يتيح عمليات متنوعة مثل إنشاء مستندات OneNote وقراءتها ومعالجتها.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من إعداد المتطلبات الأساسية التالية:

### 1. مجموعة تطوير جافا (JDK)
تأكد من تثبيت Java Development Kit (JDK) على نظامك. يمكنك تنزيل JDK وتثبيته من موقع Oracle الإلكتروني.

### 2. Aspose.Note لمكتبة جافا
 قم بتنزيل وإعداد Aspose.Note لمكتبة Java باتباع الخطوات التالية:[توثيق](https://reference.aspose.com/note/java/).

## حزم الاستيراد

ابدأ باستيراد الحزم الضرورية إلى مشروع Java الخاص بك. تتضمن هذه الحزم مكتبة Aspose.Note والتبعيات الأخرى المطلوبة.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

دعنا نقسم عملية إدراج صورة في مستند OneNote إلى خطوات متعددة:

## الخطوة 1: قم بتحميل مستند OneNote

أولاً، قم بتحميل مستند OneNote الذي تريد إدراج الصورة فيه.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## الخطوة 2: احصل على الصفحة

قم باسترجاع الصفحة الموجودة في المستند حيث تريد إدراج الصورة.

```java
Page page = oneFile.getFirstChild();
```

## الخطوة 3: تحميل الصورة

قم بتحميل الصورة التي تريد إدراجها في مستند OneNote.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## الخطوة 4: تخصيص سمات الصورة (اختياري)

اختياريًا، يمكنك تخصيص حجم الصورة وموقعها ومحاذاتها وفقًا لمتطلباتك.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## الخطوة 5: إضافة صورة إلى الصفحة

أضف الصورة إلى الصفحة في مستند OneNote.

```java
page.appendChildLast(image);
```

## الخطوة 6: احفظ المستند

احفظ المستند المعدل، بما في ذلك الصورة المدرجة.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية إدراج صورة في مستند OneNote باستخدام Java بمساعدة Aspose.Note لمكتبة Java. باتباع الدليل الموضح خطوة بخطوة، يمكنك دمج الصور بسهولة في مستندات OneNote برمجيًا.

## الأسئلة الشائعة

### س1: هل يمكنني إدراج صور متعددة في مستند OneNote واحد باستخدام هذه الطريقة؟

ج1: نعم، يمكنك إدراج صور متعددة في مستند OneNote واحد عن طريق تكرار العملية الموضحة في هذا البرنامج التعليمي لكل صورة.

### س2: هل Aspose.Note for Java متوافق مع كافة إصدارات OneNote؟

ج2: يدعم Aspose.Note for Java العمل مع ملفات OneNote التي تم إنشاؤها في Microsoft OneNote 2010 والإصدارات الأحدث.

### س3: هل يمكنني إدراج صور بتنسيقات مختلفة، مثل PNG أو GIF، في مستند OneNote؟

ج3: نعم، يدعم Aspose.Note for Java إدراج الصور بتنسيقات مختلفة، بما في ذلك PNG وJPEG وGIF والمزيد.

### س4: هل هناك إصدار تجريبي من Aspose.Note لـ Java متاح لأغراض الاختبار؟

ج4: نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.Note لـ Java من موقع الويب لأغراض التقييم.

### س5: كيف يمكنني الحصول على الدعم الفني لـ Aspose.Note لـ Java؟

 ج5: يمكنك الحصول على الدعم الفني لـ Aspose.Note لـ Java من خلال زيارة[المنتدى](https://forum.aspose.com/c/note/28) مخصص لمنتجات Aspose.Note.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
