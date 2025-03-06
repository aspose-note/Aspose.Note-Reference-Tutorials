---
title: استخراج الصور من مستند OneNote باستخدام Java
linktitle: استخراج الصور من مستند OneNote باستخدام Java
second_title: Aspose.Note جافا API
description: تعرف على كيفية استخراج الصور من مستندات OneNote باستخدام Java مع مكتبة Aspose.Note. اتبع دليلنا خطوة بخطوة لاستخراج الصور بسلاسة.
weight: 14
url: /ar/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استخراج الصور من مستند OneNote باستخدام Java

## مقدمة

في هذا البرنامج التعليمي، سنرشدك خلال عملية استخراج الصور من مستند OneNote باستخدام Java بمساعدة مكتبة Aspose.Note.

## المتطلبات الأساسية

قبل أن تبدأ، تأكد من أن لديك ما يلي:

1.  Java Development Kit (JDK): تأكد من تثبيت Java على نظامك. يمكنك تنزيله وتثبيته من[موقع إلكتروني](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  مكتبة Aspose.Note: قم بتنزيل مكتبة Aspose.Note وتضمينها في مشروع Java الخاص بك. يمكنك الحصول عليه من[رابط التحميل](https://releases.aspose.com/note/java/).

## حزم الاستيراد

للبدء، قم باستيراد الحزم الضرورية:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## الخطوة 1: قم بتحميل المستند

أولاً، قم بتحميل مستند OneNote باستخدام Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## الخطوة 2: الحصول على جميع الصور

بعد ذلك، قم باسترداد جميع الصور من المستند:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## الخطوة 3: استخراج الصور

كرر قائمة الصور واحفظ كل صورة في ملف:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## خاتمة

يمكن استخراج الصور من مستند OneNote باستخدام Java بسهولة باستخدام مكتبة Aspose.Note. باتباع الخطوات الموضحة في هذا البرنامج التعليمي، يمكنك استرداد الصور من مستنداتك بسهولة لمزيد من المعالجة أو التحليل.

## الأسئلة الشائعة

### س1: هل يمكنني استخراج الصور من مستندات OneNote المحمية بكلمة مرور؟

ج1: نعم، يدعم Aspose.Note استخراج الصور من المستندات المحمية بكلمة مرور أيضًا.

### س2: هل Aspose.Note متوافق مع الإصدارات المختلفة من Java؟

ج2: Aspose.Note متوافق مع إصدارات مختلفة من Java، مما يضمن المرونة للمطورين.

### س3: هل يمكنني استخراج الصور من مستندات OneNote المتعددة في عملية تنفيذ واحدة؟

ج3: بالتأكيد، يمكنك التكرار عبر مستندات متعددة واستخراج الصور من كل منها باستخدام Aspose.Note.

### س4: هل توجد أي قيود على حجم مستندات OneNote؟

ج4: يتعامل Aspose.Note مع المستندات ذات الأحجام المختلفة بكفاءة، مما يضمن عدم وجود قيود على حجم المستند لاستخراج الصور.

### س5: هل يدعم Aspose.Note استخراج أنواع أخرى من المحتوى بخلاف الصور؟

ج5: نعم، إلى جانب الصور، يسمح Aspose.Note باستخراج النص والمرفقات وأنواع المحتوى الأخرى من مستندات OneNote.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
