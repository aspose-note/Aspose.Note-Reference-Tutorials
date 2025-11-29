---
date: 2025-11-29
description: تعلم كيفية تصدير صفحة OneNote إلى PNG باستخدام Aspose.Note للغة Java.
  اتبع التعليمات خطوة بخطوة لتحديد فهرس الصفحة، تحويل الصفحة، وحفظ الصورة.
language: ar
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: تصدير صفحة OneNote إلى صورة PNG في Java باستخدام Aspose.Note
url: /java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير صفحة OneNote إلى صورة PNG في Java باستخدام Aspose.Note

## مقدمة

في هذا الدرس ستكتشف **كيفية تصدير صفحة OneNote** إلى صورة PNG باستخدام مكتبة Aspose.Note للغة Java. سنستعرض كل ما تحتاجه — من إعداد بيئتك إلى تعيين فهرس الصفحة وأخيرًا حفظ الصفحة كملف PNG عالي الجودة. في النهاية، ستكون قادرًا على إضافة هذه القدرة إلى أي تطبيق Java يتعامل مع مستندات OneNote.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.Note for Java.  
- **هل يمكنني تصدير صفحة واحدة؟** نعم — استخدم `setPageIndex` لاستهداف الصفحة المحددة.  
- **ما صيغ الصور المدعومة؟** PNG، JPEG، GIF، BMP، TIFF (تم عرض PNG هنا).  
- **هل أحتاج إلى ترخيص؟** يتوفر إصدار تجريبي مجاني؛ الترخيص مطلوب للإنتاج.  
- **كم من الوقت تستغرق العملية؟** عادةً أقل من 10 دقائق للتحويل الأساسي.

## ما هو “تصدير صفحة OneNote”؟
يعني تصدير صفحة OneNote تحويل صفحة محددة داخل مستند `.one` إلى ملف صورة مستقل (PNG في هذه الحالة). يكون ذلك مفيدًا عندما تحتاج إلى مشاركة محتوى OneNote أو تضمينه أو معالجته خارج بيئة OneNote.

## لماذا تستخدم Aspose.Note للغة Java لتحويل OneNote إلى PNG؟
- **بدون اعتماد على Microsoft Office** – يعمل على أي منصة تدعم Java.  
- **تحكم دقيق** – يمكنك اختيار أي صفحة عبر `setPageIndex`.  
- **إخراج عالي الجودة** – يحتفظ PNG بالرسومات المتجهة ووضوح النص.  
- **جاهز للدفعات** – سهل التكرار عبر الصفحات للتحويل الجماعي.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

1. **مجموعة تطوير Java (JDK)** – الإصدار 8 أو أعلى.  
2. **Aspose.Note للغة Java** – حمّل أحدث ملف JAR من [موقع Aspose](https://releases.aspose.com/note/java/).  
3. **مستند OneNote** (`.one`) يحتوي على الصفحة التي تريد تصديرها.

## استيراد الحزم

أولاً، استورد الفئات اللازمة في Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل مستند OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

نستخدم الفئة `Document` لقراءة ملف OneNote من القرص. يتيح لك كائن `LoadOptions` تخصيص سلوك التحميل إذا لزم الأمر.

### الخطوة 2: تهيئة ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` تخبر Aspose.Note أننا نريد الإخراج بصيغة **PNG**. يمكنك التحويل إلى JPEG أو BMP، إلخ، عن طريق تغيير `SaveFormat`.

### الخطوة 3: تعيين فهرس الصفحة (كيفية تحويل صفحة OneNote)

```java
// set page index
opts.setPageIndex(0);
```

طريقة `setPageIndex` تختار الصفحة التي سيتم تصديرها. يبدأ ترقيم الصفحات من **0**، لذا `0` تشير إلى الصفحة الأولى. عدّل هذه القيمة لتصدير صفحة مختلفة.

### الخطوة 4: حفظ المستند كـ PNG (حفظ OneNote كـ PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

استدعاء `save` يكتب الصفحة المحددة إلى ملف PNG على القرص. اسم الملف `ConvertSpecificPageToPngImage_out.png` هو مجرد مثال — يمكنك تسميته بأي اسم تريده.

## المشكلات الشائعة والنصائح

- **فهرس الصفحة غير صحيح** – تذكر أن الفهرسة تبدأ من 0. إذا حصلت على صورة فارغة، تحقق من قيمة الفهرس.  
- **ملف JAR الخاص بـ Aspose.Note مفقود** – تأكد من وجود الـ JAR في مسار الفئات (classpath)؛ وإلا ستظهر لك `ClassNotFoundException`.  
- **صفحات كبيرة** – للصفحات الكبيرة جدًا، فكر في زيادة حجم الذاكرة المخصصة للـ JVM (`-Xmx`) لتجنب `OutOfMemoryError`.

## الأسئلة المتكررة

### س1: هل يمكنني تحويل عدة صفحات إلى صور PNG دفعة واحدة باستخدام Aspose.Note للغة Java؟
ج1: نعم، يمكنك التكرار عبر صفحات المستند، وتحديث `opts.setPageIndex(i)`، واستدعاء `save` لكل تكرار.

### س2: هل يدعم Aspose.Note للغة Java صيغ صور أخرى غير PNG؟
ج2: بالتأكيد. يمكنك تعيين `SaveFormat.Jpeg` أو `SaveFormat.Gif` أو `SaveFormat.Bmp` أو `SaveFormat.Tiff` في `ImageSaveOptions`.

### س3: هل يتوفر نسخة تجريبية مجانية لـ Aspose.Note للغة Java؟
ج3: نعم، يمكنك تنزيل نسخة تجريبية مجانية من [الموقع](https://releases.aspose.com/).

### س4: هل يمكنني الحصول على مساعدة تقنية إذا واجهت أي مشكلات مع Aspose.Note للغة Java؟
ج4: بالتأكيد، يمكنك طلب الدعم من منتدى مجتمع Aspose [هنا](https://forum.aspose.com/c/note/28).

### س5: أين يمكنني شراء ترخيص لـ Aspose.Note للغة Java؟
ج5: يمكنك شراء ترخيص من [صفحة الشراء](https://purchase.aspose.com/buy).

### س6: كيف يمكنني تصدير صفحة تحتوي على صور مدمجة؟
ج6: يتم عرض الصور المدمجة تلقائيًا في مخرجات PNG؛ لا يلزم أي كود إضافي.

### س7: هل يمكنني تعيين DPI أو دقة الصورة؟
ج7: نعم، استخدم `opts.setResolution(int dpi)` قبل استدعاء `save` للتحكم في جودة الإخراج.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-11-29  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

---