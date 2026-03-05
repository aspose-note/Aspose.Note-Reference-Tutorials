---
date: 2026-03-05
description: تعلم كيفية تصدير مستندات OneNote إلى صور BMP باستخدام خيارات حفظ الصورة
  في Aspose.Note for Java. كما يمكنك الاطلاع على كيفية تحويل OneNote إلى PDF أو حفظ
  OneNote كملف PNG.
linktitle: how to export onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: كيفية تصدير OneNote إلى صورة BMP باستخدام خيارات حفظ الصورة
url: /ar/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تصدير OneNote إلى صورة BMP باستخدام خيارات حفظ الصورة

## كيفية تصدير OneNote إلى صورة BMP

Aspose.Note for Java هي مكتبة قوية تمكّن مطوري Java من العمل مع ملفات Microsoft OneNote برمجيًا. **في هذا البرنامج التعليمي ستتعلم كيفية تصدير مستندات OneNote إلى صور BMP** باستخدام ميزة خيارات حفظ الصورة في Aspose.Note for Java. سنستعرض كل خطوة، ونوضح لماذا قد تختار BMP على غيرها من الصيغ، ونظهر لك كيفية دمج هذه القدرة في تطبيقاتك الخاصة.

## إجابات سريعة
- **ماذا يفعل صف Image Save Options؟** يتيح لك تحديد صيغة الصورة الناتجة (BMP، PNG، JPEG، إلخ) عند تحويل صفحة OneNote.  
- **هل أحتاج إلى ترخيص لتشغيل العينة؟** النسخة التجريبية المجانية تكفي للتقييم، لكن الترخيص التجاري مطلوب للاستخدام في الإنتاج.  
- **هل يمكنني تحويل صفحة OneNote إلى PDF أو PNG بدلاً من BMP؟** نعم – فقط غيّر تعداد `SaveFormat` (مثال: `SaveFormat.Pdf` أو `SaveFormat.Png`).  
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها مدعومة بالكامل.  
- **هل هناك معالجة خاصة للمستندات الكبيرة؟** يمكنك بث الإخراج لتجنب استهلاك الذاكرة العالي.

## ما هو “Image Save Options” في Aspose.Note؟
يوفر الصف `ImageSaveOptions` تحكمًا دقيقًا في كيفية تحويل صفحات OneNote إلى صور نقطية. يمكنك ضبط صيغة الصورة، الدقة، عمق اللون، وأكثر. هذه المرونة تجعل من السهل **تصدير صورة صفحة OneNote** للأنظمة القديمة (BMP) أو سيناريوهات الويب الحديثة (PNG/JPEG).  

## المتطلبات المسبقة

1. معرفة أساسية بلغة برمجة Java.  
2. JDK (Java Development Kit) مثبت على جهازك.  
3. بيئة تطوير متكاملة (IDE) مثل Eclipse أو IntelliJ IDEA.  
4. مكتبة Aspose.Note for Java – قم بتنزيلها من [here](https://releases.aspose.com/note/java/).

## استيراد الحزم

أولاً، استورد الفئات الضرورية من Aspose.Note وأدوات الإدخال/الإخراج القياسية في Java:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## الخطوة 1: تحميل مستند OneNote

هنا نشير إلى المجلد الذي يحتوي على ملف OneNote المصدر (`Aspose.one`) ونحمله في كائن `Document`. هذا الكائن يمنحك وصولًا كاملًا إلى الصفحات، الأقسام، والعناصر الأخرى داخل الدفتر.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## الخطوة 2: حفظ المستند كصورة BMP

نقوم بدمج اسم ملف الإخراج، ثم نستدعي `save` مع كائن `ImageSaveOptions` مُعد لتنسيق **BMP** (`SaveFormat.Bmp`).  
إذا أردت **حفظ صفحة OneNote** كـ PNG، استبدل ببساطة `SaveFormat.Bmp` بـ `SaveFormat.Png`. وبالمثل، يتيح لك `SaveFormat.Pdf` إجراء تحويل **OneNote إلى PDF**.

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

## لماذا اختيار BMP؟
- **جودة غير مضغوطة** – BMP يخزن بيانات البكسل الخام، محافظًا على المظهر الدقيق للصفحة الأصلية.  
- **التوافق** – غالبًا ما تتطلب التطبيقات القديمة على Windows ملفات BMP.  
- **البساطة** – لا توجد عيوب ضغط، مما يجعلها مثالية لمعالجة الصور الإضافية.

## المشكلات الشائعة والنصائح

- **أخطاء مسار الملف** – تأكد من أن `dataDir` ينتهي بالفاصل المناسب للملفات (`/` أو `\`).  
- **دفاتر ملاحظات كبيرة** – بالنسبة لملفات OneNote الكبيرة جدًا، فكر في حفظ كل صفحة على حدة لتقليل استهلاك الذاكرة.  
- **استثناءات الترخيص** – تشغيل الكود بدون ترخيص صالح سيضيف علامة مائية إلى الصورة المُنشأة.

## الخلاصة

في هذا الدليل، عرضنا **كيفية تصدير مستندات OneNote** إلى صور BMP باستخدام `ImageSaveOptions` في Aspose.Note for Java. من خلال تبديل تعداد `SaveFormat` يمكنك أيضًا إنشاء PNG أو JPEG أو PDF أو صيغ أخرى مدعومة، مما يمنحك طريقة مرنة لتصدير محتوى OneNote لأي سيناريو لاحق.

## الأسئلة المتكررة

**س1: هل يمكنني حفظ مستندات OneNote إلى صيغ صور أخرى غير BMP؟**  
ج: نعم، يمكنك استخدام `ImageSaveOptions` مع `SaveFormat.Png` أو `SaveFormat.Jpeg` أو `SaveFormat.Gif` أو `SaveFormat.Tiff` لتصدير إلى تلك الصيغ.

**س2: هل يدعم Aspose.Note for Java التحويل بين صيغ المستندات المختلفة؟**  
ج: بالتأكيد. بالإضافة إلى صيغ الصور، يمكنك تحويل ملفات OneNote إلى PDF أو DOCX أو HTML وغيرها باستخدام `SaveFormat` المناسب.

**س3: هل Aspose.Note for Java متوافق مع أحدث إصدارات OneNote؟**  
ج: نعم، يتم تحديث المكتبة بانتظام لتواكب أحدث إصدارات OneNote.

**س4: هل يمكنني تعديل محتوى مستندات OneNote برمجيًا؟**  
ج: نعم، يمكنك إضافة أو تعديل أو حذف الصفحات، الأقسام، والمحتوى الغني (نص، صور، جداول) عبر الـ API.

**س5: هل يقدم Aspose.Note for Java دعمًا فنيًا؟**  
ج: نعم، تقدم Aspose دعمًا فنيًا ومنتدى مخصص. زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على المساعدة.

**آخر تحديث:** 2026-03-05  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}