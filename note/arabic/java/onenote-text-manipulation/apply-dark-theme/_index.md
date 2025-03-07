---
title: تطبيق المظهر الداكن على النص في OneNote - Aspose.Note
linktitle: تطبيق المظهر الداكن على النص في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: استكشف الخطوات السهلة لتطبيق سمة داكنة على نص OneNote الخاص بك باستخدام Aspose.Note لـ Java. ارفع مستوى تجربة التوثيق الرقمي الخاصة بك دون عناء.
weight: 11
url: /ar/java/onenote-text-manipulation/apply-dark-theme/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تطبيق المظهر الداكن على النص في OneNote - Aspose.Note

## مقدمة
في مشهد التوثيق الرقمي دائم التطور، يمكن أن تؤثر جماليات ملاحظاتك بشكل كبير على سهولة القراءة وتجربة المستخدم. أحد الجوانب البارزة هو تنفيذ سمة داكنة، مما يوفر بيئة جذابة بصريًا ومريحة. في هذا البرنامج التعليمي، سنرشدك خلال عملية تطبيق سمة داكنة على النص في OneNote باستخدام Aspose.Note لـ Java.
## المتطلبات الأساسية
قبل الغوص في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:
-  Aspose.Note for Java: قم بتنزيل وتثبيت مكتبة Aspose.Note for Java من[هنا](https://releases.aspose.com/note/java/).
- Java Development Kit (JDK): تأكد من تثبيت Java على جهازك.
- بيئة التطوير المتكاملة (IDE): اختر IDE مثل Eclipse أو IntelliJ للتطوير السلس.
## حزم الاستيراد
للبدء، قم باستيراد الحزم الضرورية إلى مشروع Java الخاص بك:
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
```
## الخطوة 1: تعيين لون خلفية الصفحة
```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory";
// قم بتحميل المستند إلى Aspose.Note.
Document doc = new Document(Paths.get(dataDir, "Aspose.one").toString());
for (Page page: doc)
{
    page.setBackgroundColor(Color.BLACK);
}
```
## الخطوة 2: ضبط لون النص
```java
for (RichText node: doc.getChildNodes(RichText.class))
{
    Color c = node.getParagraphStyle().getFontColor();
    if (c.getAlpha() <= 10 || Math.abs(c.getRed() - Color.BLACK.getRed()) + Math.abs(c.getGreen() - Color.BLACK.getGreen()) + Math.abs(c.getBlue() - Color.BLACK.getBlue()) <= 30)
    {
        node.getParagraphStyle().setFontColor(Color.WHITE);
    }
}
```
## الخطوة 3: حفظ المستند
```java
doc.save(Paths.get(dataDir, "AsposeDarkTheme.pdf").toString());
```
كرر هذه الخطوات لكل مستند، وستكون قد نجحت في تطبيق سمة داكنة على نص OneNote الخاص بك باستخدام Aspose.Note لـ Java.
## خاتمة
في الختام، يعد تحسين المظهر المرئي لملاحظاتك الرقمية أمرًا بسيطًا باستخدام Aspose.Note لـ Java. باتباع هذا الدليل المفصّل خطوة بخطوة، يمكنك بسهولة تطبيق سمة داكنة على النص في OneNote، مما يؤدي إلى الارتقاء بتجربة التوثيق لديك.
## الأسئلة الشائعة
### هل يمكنني تطبيق سمة داكنة على أقسام محددة فقط؟
نعم، يمكنك تعديل التعليمات البرمجية لتطبيق السمة الداكنة بشكل انتقائي على أقسام محددة داخل المستند.
### هل تتوفر سمات داكنة محددة مسبقًا في Aspose.Note لـ Java؟
اعتبارًا من الآن، يتيح لك Aspose.Note for Java تخصيص السمات، ولكن لا توجد سمات داكنة محددة مسبقًا.
### هل يدعم Aspose.Note for Java تنسيقات المستندات الأخرى؟
نعم، يدعم Aspose.Note for Java تنسيقات المستندات المختلفة، بما في ذلك PDF وDOCX وHTML.
### هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ Java؟
 نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).
### كيف يمكنني الحصول على الدعم لـ Aspose.Note لـ Java؟
 قم بزيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على دعم المجتمع أو استكشاف خيارات الدعم المتميزة[هنا](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
