---
date: 2025-12-17
description: تعلم كيفية تصدير OneNote عن طريق حفظ المستند كصورة PNG بتدرج الرمادي
  باستخدام Aspose.Note للغة Java. يتضمن خطوات تحميل مستند OneNote وإنشاء صورة بتدرج
  الرمادي.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: كيفية تصدير OneNote كصورة بتدرج الرمادي – Aspose.Note
url: /ar/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ صورة بتدرج الرمادي في OneNote - Aspose.Note

## المقدمة

في هذا الدرس، سنوضح لك **كيفية تصدير onenote** عن طريق حفظ المستند كصورة بتدرج الرمادي باستخدام Aspose.Note for Java. صور تدرج الرمادي هي صور أحادية اللون تحتوي فقط على درجات من اللون الرمادي، ويمكن أن تكون مفيدة للطباعة أو الأرشفة أو تقليل حجم الملف. سنستعرض خطوات تحميل مستند OneNote، ضبط خيارات الحفظ لإنشاء **صورة بتدرج الرمادي**، وأخيرًا **حفظ المستند كملف PNG**.

## إجابات سريعة
- **ماذا يعني “كيفية تصدير onenote”؟** يشير إلى تحويل ملف OneNote إلى تنسيق آخر، مثل صورة، برمجياً.  
- **ما هو أفضل تنسيق لإخراج تدرج الرمادي؟** PNG يعمل جيدًا لأنه يحافظ على جودة غير مضغوطة ويدعم وضع اللون الرمادي.  
- **هل أحتاج إلى ترخيص؟** يتطلب الاستخدام في بيئة الإنتاج ترخيصًا صالحًا لـ Aspose.Note؛ يتوفر ترخيص تجريبي مؤقت للاختبار.  
- **ما نسخة Java المطلوبة؟** يوصى باستخدام Java 8 أو أعلى.  
- **هل يمكنني تغيير حجم الصورة؟** نعم، يمكنك تعديل خصائص `ImageSaveOptions` مثل `Resolution` أو `PageSize` قبل الحفظ.

## ما هو “كيفية تصدير onenote”؟
يعني تصدير OneNote تحويل ملف OneNote `.one` برمجياً إلى تمثيل آخر—مثل PDF أو HTML أو صورة. في هذا الدليل نركز على التصدير إلى صورة **PNG بتدرج الرمادي**، وهو طلب شائع لتوثيق أو عمليات طباعة.

## لماذا تصدير OneNote كصورة بتدرج الرمادي؟
- **تقليل حجم الملف** – عادةً ما تكون ملفات PNG بتدرج الرمادي أصغر من الصور الملونة بالكامل.  
- **قراءة أفضل** – للتقارير المطبوعة، يوفر تدرج الرمادي تباينًا أوضح.  
- **التوافق** – PNG مدعوم على نطاق واسع عبر المتصفحات، المحررات، والأجهزة المحمولة.  

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. مجموعة تطوير جافا (JDK) مثبتة على نظامك.  
2. مكتبة Aspose.Note for Java. يمكنك تحميلها من [هنا](https://releases.aspose.com/note/java/).  
3. فهم أساسي لبرمجة Java.  

## استيراد الحزم

لبدء العمل، استورد الحزم الضرورية:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## الخطوة 1: تحميل مستند OneNote

أولاً، **قم بتحميل مستند onenote** إلى Aspose.Note. استبدل `"Your Document Directory"` بمسار المجلد المحلي الخاص بك و`"Aspose.one"` باسم ملف OneNote الخاص بك.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## الخطوة 2: تحديد مسار الإخراج والخيارات

عرّف مسار الإخراج للصورة بتدرج الرمادي وحدد خيارات الحفظ. سنضبط `ColorMode` إلى `GrayScale` ونستخدم صيغة **حفظ المستند كـ png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## الخطوة 3: حفظ المستند

أخيرًا، احفظ المستند كصورة PNG بتدرج الرمادي باستخدام الخيارات التي تم تكوينها.

```java
oneFile.save(dataDir, options);
```

## المشكلات الشائعة والحلول
- **FileNotFoundException** – تحقق من أن `dataDir` يشير إلى المجلد الصحيح وأن ملف `.one` موجود.  
- **LicenseException** – تأكد من تطبيق ترخيص Aspose.Note صالح قبل استدعاء `save`.  
- **إخراج منخفض الدقة** – اضبط `options.setResolution(300)` لزيادة DPI إذا لزم الأمر.

## الأسئلة المتكررة

**س1: هل يمكنني حفظ الصورة بتدرج الرمادي بصيغة مختلفة؟**  
ج1: نعم، ما عليك سوى تغيير معامل `SaveFormat` في مُنشئ `ImageSaveOptions` إلى `Jpeg` أو `Bmp` وغيرها.

**س2: هل Aspose.Note متوافق مع جميع إصدارات مستندات OneNote؟**  
ج2: يدعم Aspose.Note Microsoft OneNote 2010 والإصدارات الأحدث.

**س3: هل يتطلب Aspose.Note ترخيصًا للاستخدام؟**  
ج3: الترخيص الصالح مطلوب للاستخدام في بيئة الإنتاج، لكن يمكن الحصول على ترخيص تجريبي مؤقت للتقييم.

**س4: هل يمكنني تعديل جوانب أخرى من المستند قبل حفظه كصورة؟**  
ج4: بالتأكيد! يوفر Aspose.Note واجهة برمجة تطبيقات شاملة لتحرير الأقسام والصفحات والمحتوى قبل التصدير.

**س5: أين يمكنني العثور على الدعم إذا واجهت مشكلات؟**  
ج5: يمكنك الحصول على الدعم عبر منتدى Aspose.Note [هنا](https://forum.aspose.com/c/note/28).

## الخاتمة

لقد تعلمت الآن **كيفية تصدير onenote** عن طريق تحميل ملف OneNote، ضبط خيارات الحفظ لإنشاء **صورة بتدرج الرمادي**، و**حفظ المستند كملف PNG**. هذه التقنية مفيدة لإنشاء رسومات خفيفة الوزن وجاهزة للطباعة من دفاتر OneNote. لا تتردد في تجربة إعدادات `ColorMode` أخرى أو صيغ صور مختلفة لتناسب احتياجات مشروعك.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-12-17  
**تم الاختبار مع:** Aspose.Note 24.12 for Java  
**المؤلف:** Aspose  

---