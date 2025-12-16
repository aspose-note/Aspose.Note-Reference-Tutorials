---
date: 2025-12-16
description: تعلم كيفية حفظ مستندات OneNote كصور BMP باستخدام خيارات حفظ الصور في
  Aspose.Note for Java. كما يمكنك الاطلاع على كيفية حفظ OneNote كملف PDF أو PNG.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: كيفية حفظ OneNote كصورة BMP باستخدام خيارات حفظ الصورة
url: /ar/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية حفظ OneNote كصورة BMP باستخدام خيارات حفظ الصورة

## مقدمة

Aspose.Note for Java هي مكتبة قوية تمكّن مطوري Java من العمل مع ملفات Microsoft OneNote برمجيًا. **في هذا الدرس ستتعلم كيفية حفظ مستندات OneNote كصور BMP** باستخدام ميزة Image Save Options في Aspose.Note for Java. سنستعرض كل خطوة، نشرح لماذا قد تختار BMP بدلاً من الصيغ الأخرى، ونظهر لك كيفية دمج هذه القدرة في تطبيقاتك الخاصة.

## إجابات سريعة
- **ماذا تفعل فئة Image Save Options؟** تتيح لك تحديد صيغة الصورة الناتجة (BMP، PNG، JPEG، إلخ) عند تحويل صفحة OneNote.  
- **هل أحتاج إلى ترخيص لتشغيل العينة؟** النسخة التجريبية المجانية تكفي للتقييم، لكن الترخيص التجاري مطلوب للاستخدام في الإنتاج.  
- **هل يمكنني تحويل صفحة OneNote إلى PDF أو PNG بدلاً من BMP؟** نعم – فقط غيّر قيمة تعداد `SaveFormat` (مثال: `SaveFormat.Pdf` أو `SaveFormat.Png`).  
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها مدعومة بالكامل.  
- **هل هناك معالجة خاصة للمستندات الكبيرة؟** يمكنك بث الإخراج لتجنب استهلاك الذاكرة العالي.

## ما هو “Image Save Options” في Aspose.Note؟
توفر فئة `ImageSaveOptions` تحكمًا دقيقًا في كيفية تحويل صفحات OneNote إلى صور نقطية. يمكنك ضبط صيغة الصورة، الدقة، عمق اللون، وأكثر. هذه المرونة تجعل من السهل إنشاء ملفات BMP للأنظمة القديمة أو ملفات PNG/JPEG للاستخدام على الويب.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. معرفة أساسية بلغة البرمجة Java.  
2. تثبيت JDK (Java Development Kit) على جهازك.  
3. بيئة تطوير متكاملة (IDE) مثل Eclipse أو IntelliJ IDEA.  
4. مكتبة Aspose.Note for Java – حمّلها من [هنا](https://releases.aspose.com/note/java/).

## استيراد الحزم

أولًا، استورد الفئات الضرورية من Aspose.Note وأدوات الإدخال/الإخراج القياسية في Java:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## الخطوة 1: تحميل مستند OneNote

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

هنا نشير إلى المجلد الذي يحتوي على ملف OneNote المصدر (`Aspose.one`) ونحمله في كائن `Document`. يمنحك هذا الكائن وصولًا كاملًا إلى الصفحات، الأقسام، والعناصر الأخرى داخل الدفتر.

## الخطوة 2: حفظ المستند كصورة BMP

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

نقوم بدمج اسم ملف الإخراج، ثم نستدعي `save` مع كائن `ImageSaveOptions` مكوَّن لحفظ **BMP** (`SaveFormat.Bmp`).  
إذا أردت **حفظ صفحة OneNote** كـ PNG، استبدل `SaveFormat.Bmp` بـ `SaveFormat.Png`. بالمثل، يتيح لك `SaveFormat.Pdf` إجراء تحويل **من OneNote إلى PDF**.

## لماذا اختيار BMP؟
- **جودة غير مضغوطة** – BMP يخزن بيانات البكسل الخام، محافظًا على المظهر الدقيق للصفحة الأصلية.  
- **التوافق** – كثير من تطبيقات Windows القديمة تتطلب ملفات BMP.  
- **البساطة** – لا توجد تشوهات ناتجة عن الضغط، مما يجعله مثاليًا لمعالجة الصور الإضافية.

## المشكلات الشائعة والنصائح

- **أخطاء مسار الملف** – تأكد من أن `dataDir` ينتهي بالفاصل المناسب للملفات (`/` أو `\`).  
- **الدفاتر الكبيرة** – بالنسبة لملفات OneNote الضخمة، فكر في حفظ كل صفحة على حدة لتقليل استهلاك الذاكرة.  
- **استثناءات الترخيص** – تشغيل الكود بدون ترخيص صالح سيضيف علامة مائية إلى الصورة المولدة.

## الخلاصة

في هذا الدليل أظهرنا **كيفية حفظ مستندات OneNote** كصور BMP باستخدام `ImageSaveOptions` في Aspose.Note for Java. عبر تبديل تعداد `SaveFormat` يمكنك أيضًا إنشاء PNG أو JPEG أو PDF أو صيغ أخرى مدعومة، مما يمنحك طريقة مرنة لتصدير محتوى OneNote لأي سيناريو لاحق.

## الأسئلة المتكررة

**س1: هل يمكنني حفظ مستندات OneNote بصيغ صور أخرى غير BMP؟**  
ج: نعم، يمكنك استخدام `ImageSaveOptions` مع `SaveFormat.Png` أو `SaveFormat.Jpeg` أو `SaveFormat.Gif` أو `SaveFormat.Tiff` لتصدير إلى تلك الصيغ.

**س2: هل يدعم Aspose.Note for Java التحويل بين صيغ المستندات المختلفة؟**  
ج: بالتأكيد. إلى جانب صيغ الصور، يمكنك تحويل ملفات OneNote إلى PDF أو DOCX أو HTML وغيرها باستخدام `SaveFormat` المناسب.

**س3: هل Aspose.Note for Java متوافق مع أحدث إصدارات OneNote؟**  
ج: نعم، يتم تحديث المكتبة بانتظام لتواكب أحدث إصدارات OneNote.

**س4: هل يمكنني تعديل محتوى مستندات OneNote برمجيًا؟**  
ج: نعم، يمكنك إضافة أو تعديل أو حذف الصفحات، الأقسام، والمحتوى الغني (نص، صور، جداول) عبر الـ API.

**س5: هل يوفر Aspose.Note for Java دعمًا فنيًا؟**  
ج: نعم، تقدم Aspose دعمًا فنيًا ومنتدى مخصص. زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على المساعدة.

---

**آخر تحديث:** 2025-12-16  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
