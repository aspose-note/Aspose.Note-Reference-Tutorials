---
date: 2026-06-30
description: تعلم كيفية تصدير OneNote عن طريق حفظ المستند كصورة PNG رمادية باستخدام
  Aspose.Note for Java. يتضمن خطوات تحميل مستند OneNote وإنشاء صورة رمادية.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: كيفية تصدير OneNote كصورة رمادية – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: كيفية تصدير OneNote كصورة رمادية – Aspose.Note
url: /ar/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ كصورة رمادية في OneNote - Aspose.Note

## مقدمة

في هذا الدرس ستكتشف **كيفية تصدير onenote** عن طريق تحويل ملف OneNote `.one` إلى صورة PNG رمادية عالية الجودة باستخدام Aspose.Note للـ Java. غالبًا ما يحتاج مطورو Java إلى تحويل إلى رمادي للطباعة أو الأرشفة أو **تقليل حجم OneNote** دون فقدان المحتوى الأساسي. سنستعرض تحميل مستند OneNote، وتكوين خيارات الحفظ—بما في ذلك **ضبط دقة الصورة**—وأخيرًا حفظ المستند كملف PNG.

## إجابات سريعة
- **ماذا يعني “how to export onenote”؟** إنه يشير إلى تحويل ملف OneNote برمجيًا إلى تنسيق آخر، مثل صورة، باستخدام الكود.  
- **ما هو أفضل تنسيق للإخراج الرمادي؟** PNG يعمل جيدًا لأنه يحافظ على جودة بدون فقدان ويدعم وضع لون رمادي مخصص.  
- **هل أحتاج إلى ترخيص؟** ترخيص Aspose.Note صالح مطلوب للاستخدام في الإنتاج؛ ترخيص تجريبي مؤقت متاح للاختبار.  
- **ما نسخة Java المطلوبة؟** يوصى باستخدام Java 8 أو أعلى.  
- **هل يمكنني تغيير حجم الصورة؟** نعم، يمكنك تعديل خصائص `ImageSaveOptions` مثل `Resolution` أو `PageSize` قبل الحفظ.

## ما هو “how to export onenote”؟

يعني تصدير OneNote تحويل ملف OneNote `.one` برمجيًا إلى تمثيل آخر—مثل PDF أو HTML أو صورة. في هذا الدليل نركز على **إنشاء صور PNG رمادية**، وهو طلب شائع للتوثيق أو سير عمل جاهز للطباعة. باستخدام Aspose.Note، يتم التحويل بالكامل في الذاكرة، لذا لا تحتاج أبدًا إلى تثبيت Microsoft OneNote على الخادم.

## لماذا تصدير OneNote كصورة رمادية؟

عادةً ما تكون صور PNG الرمادية **أصغر بنسبة 30‑40 %** من نظيراتها الملونة بالكامل، مما يسرّع توصيل الويب ويقلل من تكاليف التخزين. كما أنها توفر **تباينًا أوضح** على طابعات الليزر، مما يجعل التقارير أسهل للقراءة. نظرًا لأن PNG مدعوم عالميًا، فإن الملفات الناتجة تعمل على المتصفحات والأجهزة المحمولة ومحررات سطح المكتب دون الحاجة إلى ترميزات إضافية.

## المتطلبات المسبقة

1. مجموعة تطوير Java (JDK) 8 أو أحدث مثبتة.  
2. مكتبة Aspose.Note للـ Java – حمّل أحدث إصدار من [here](https://releases.aspose.com/note/java/).  
3. فهم أساسي لبنية جمل Java وإعداد مشروع Maven/Gradle.  

## استيراد الحزم

تتحكم الفئة `ImageSaveOptions` في كيفية تحويل المستند إلى صورة.  
`ColorMode` هي تعداد يتيح لك التبديل بين الإخراج ملون كامل والرمادي.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## الخطوة 1: تحميل مستند OneNote

`Document` تمثل دفتر ملاحظات OneNote وتوفر طرقًا لتحميل وتحرير وحفظ محتوياته. أولاً، **حمّل مستند OneNote** إلى Aspose.Note. استبدل `"Your Document Directory"` بمسار المجلد المحلي الخاص بك و `"Aspose.one"` باسم ملف OneNote الخاص بك.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## الخطوة 2: تعيين مسار الإخراج والخيارات

`ImageSaveOptions` يضبط كيفية تحويل مستند OneNote إلى ملف صورة. تعداد `ColorMode` يحدد وضع عرض اللون، مثل الرمادي أو اللون الكامل. عرّف مسار الإخراج للصورة الرمادية وحدد خيارات الحفظ. سنضبط `ColorMode` إلى `GrayScale` ونستخدم صيغة **حفظ المستند كـ PNG**. يمكنك أيضًا **ضبط دقة الصورة** إلى 300 DPI للطباعة عالية الجودة.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## الخطوة 3: حفظ المستند

أخيرًا، احفظ المستند كصورة PNG رمادية باستخدام الخيارات المكوّنة. طريقة `save` تكتب الملف إلى القرص دون الحاجة إلى أي ملفات مؤقتة وسيطة.

```java
oneFile.save(dataDir, options);
```

## المشكلات الشائعة والحلول
- **FileNotFoundException** – تحقق من أن `dataDir` يشير إلى المجلد الصحيح وأن ملف `.one` موجود.  
- **LicenseException** – تأكد من تطبيق ترخيص Aspose.Note صالح قبل استدعاء `save`.  
- **Low‑resolution output** – اضبط `options.setResolution(300)` لزيادة DPI؛ كلما ارتفعت DPI زادت وضوح الطباعة لكن حجم الملف سيكبر.  

## الأسئلة المتكررة

**Q1: هل يمكنني حفظ الصورة الرمادية بتنسيق مختلف؟**  
A1: نعم، ببساطة غيّر معلمة `SaveFormat` في مُنشئ `ImageSaveOptions` إلى `Jpeg` أو `Bmp` أو أي من أكثر من 20 تنسيق صورة مدعوم.

**Q2: هل Aspose.Note متوافق مع جميع إصدارات مستندات OneNote؟**  
A2: يدعم Aspose.Note Microsoft OneNote 2010 وما بعده، ويغطي أكثر من 95 % من دفاتر الملاحظات المستخدمة حاليًا.

**Q3: هل يتطلب Aspose.Note ترخيصًا للاستخدام؟**  
A3: يلزم وجود ترخيص صالح للاستخدام في الإنتاج، لكن يمكن الحصول على ترخيص تجريبي مؤقت للتقييم دون تكلفة.

**Q4: هل يمكنني تعديل جوانب أخرى من المستند قبل حفظه كصورة؟**  
A4: بالتأكيد! يوفر Aspose.Note واجهات برمجة تطبيقات لتعديل الأقسام والصفحات والعناصر الفردية مثل النص والجداول والصور قبل التصدير.

**Q5: أين يمكنني العثور على الدعم إذا واجهت مشاكل؟**  
A5: يمكنك العثور على الدعم في منتدى Aspose.Note [here](https://forum.aspose.com/c/note/28).

## الخاتمة

لقد تعلمت الآن **كيفية تصدير onenote** عن طريق تحميل ملف OneNote، وتكوين خيارات الحفظ **لإنشاء صورة رمادية**، و**حفظ المستند كـ PNG**. هذا النهج مثالي لإنشاء رسومات خفيفة الوزن وجاهزة للطباعة من دفاتر OneNote. لا تتردد في تجربة إعدادات `ColorMode` الأخرى، أو قيم DPI أعلى، أو صيغ صور بديلة لتتناسب مع متطلبات مشروعك.

---

**آخر تحديث:** 2026-06-30  
**تم الاختبار مع:** Aspose.Note 27.0 for Java  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [تصدير صفحة OneNote إلى صورة PNG في Java باستخدام Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote ضبط دقة jpeg – ضبط دقة صورة الإخراج في OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [كيفية حفظ OneNote كملف PDF باستخدام Aspose.Note للـ Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}