---
date: 2026-03-19
description: تعلم كيفية إضافة صورة إلى OneNote باستخدام Java مع Aspose.Note for Java،
  بما في ذلك كيفية ضبط أبعاد الصورة في Java وحفظ OneNote كملف PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: إضافة صورة إلى OneNote باستخدام Java
url: /ar/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدراج صورة في مستند OneNote باستخدام Java

## المقدمة

في هذا الدرس ستتعلم **كيفية إضافة صورة إلى OneNote** برمجيًا باستخدام Java ومكتبة Aspose.Note for Java. تضمين الصور في صفحات OneNote مفيد عندما تحتاج إلى إنشاء محاضر اجتماعات، تقارير آلية، أو وثائق تجمع بين النص والبيانات المرئية. بنهاية الدليل ستكون قادرًا على تحميل ملف OneNote موجود، إدراج صورة، تعديل حجمها وموقعها اختياريًا، وحتى **حفظ OneNote كملف PDF** – كل ذلك دون فتح واجهة OneNote.

## إجابات سريعة
- **ما هي أسهل طريقة لإضافة صورة إلى OneNote باستخدام Java؟**  
  استخدم فئة `Image` في Aspose.Note for Java وأضفها إلى صفحة.
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟**  
  نعم، يلزم الحصول على ترخيص تجاري للنشر في بيئة الإنتاج.
- **هل يمكنني تعيين أبعاد مخصصة للصورة؟**  
  بالطبع – استدعِ `setWidth()` و `setHeight()` على كائن `Image`.
- **هل يمكن حفظ ملف OneNote كملف PDF بعد إضافة الصورة؟**  
  نعم، استدعِ `save(..., SaveFormat.Pdf)` **لحفظ OneNote كملف PDF**.
- **ما إصدار Java المدعوم؟**  
  Aspose.Note for Java يعمل مع JDK 8 وما بعده.

## لماذا إضافة صورة إلى OneNote؟

إضافة عناصر بصرية تجعل الملاحظات أسهل للفهم وأكثر جاذبية. يمكن للصور توضيح المخططات، لقطات الشاشة، أو الرسوم البيانية التي قد تتطلب أوصافًا نصية مطولة. أتمتة هذه الخطوة توفر الوقت، خاصةً عند إنشاء دفعات كبيرة من الملاحظات من مصادر البيانات.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من توفر ما يلي:

### 1. مجموعة تطوير Java (JDK)
قم بتثبيت JDK 8 أو أحدث. يمكنك تنزيله من موقع Oracle أو استخدام توزيعة OpenJDK.

### 2. مكتبة Aspose.Note for Java
حمّل أحدث نسخة من مكتبة Aspose.Note for Java وأضفها إلى مسار الفئات (classpath) في مشروعك. تعليمات الإعداد التفصيلية متوفرة في [الوثائق الرسمية](https://reference.aspose.com/note/java/).

## استيراد الحزم

ابدأ باستيراد الفئات الضرورية. هذه الاستيرادات تمنحك الوصول إلى وظائف Aspose.Note الأساسية بالإضافة إلى الأدوات الأساسية في Java.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## دليل خطوة بخطوة

فيما يلي دليل مختصر مرقم. كل خطوة تتضمن شرحًا قصيرًا يليه الكود الدقيق الذي تحتاج إلى نسخه.

### الخطوة 1: تحميل مستند OneNote

ننشئ كائن `LoadOptions` (مفيد للتخصيصات المستقبلية) ونفتح ملف `.one` الموجود.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### الخطوة 2: الحصول على الصفحة المستهدفة

للتبسيط نعمل مع الصفحة الأولى في المستند، لكن يمكنك الانتقال إلى أي صفحة تحتاجها.

```java
Page page = oneFile.getFirstChild();
```

### الخطوة 3: تحميل الصورة التي تريد تضمينها

أنشئ كائن `Image` بتمرير مرجع المستند ومسار ملف الصورة.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### الخطوة 4: تعيين أبعاد الصورة Java (اختياري)

إذا كنت بحاجة إلى أن تتناسب الصورة مع مساحة محددة، اضبط العرض، الارتفاع، والإزاحات. هنا يبرز المفتاح الثانوي **set image dimensions java**.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### الخطوة 5: إلحاق الصورة بالصفحة

طريقة `appendChildLast` تضيف الصورة كآخر عنصر في الصفحة المختارة.

```java
page.appendChildLast(image);
```

### الخطوة 6: حفظ المستند – يمكنك أيضًا حفظ OneNote كملف PDF

أخيرًا، احفظ التغييرات. يوضح المثال حفظ الملف كملف PDF، مستوفياً المفتاح الثانوي **save onenote as pdf**.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## المشكلات الشائعة والحلول

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| `FileNotFoundException` عند تحميل الصورة | مسار الصورة غير صحيح | تحقق من أن `dataDir` واسم ملف الصورة صحيحان. |
| الصورة تظهر مشوهة | تم ضبط العرض/الارتفاع بشكل غير صحيح | استخدم أبعاد الصورة الأصلية أو احسب نسبة أبعاد مناسبة قبل استدعاء `setWidth`/`setHeight`. |
| ملف PDF الناتج فارغ | غياب ترخيص لـ Aspose.Note | طبق ترخيصًا صالحًا قبل استدعاء `save`. |

## الأسئلة المتكررة

### س1: هل يمكنني إدراج صور متعددة في مستند OneNote واحد باستخدام هذه الطريقة؟

**ج:** نعم. ما عليك سوى تكرار الخطوات 3‑5 لكل صورة تريد إضافتها، مع استهداف نفس الصفحة أو صفحات مختلفة.

### س2: هل Aspose.Note for Java متوافق مع جميع إصدارات OneNote؟

**ج:** Aspose.Note for Java يدعم ملفات OneNote التي تم إنشاؤها باستخدام Microsoft OneNote 2010 والإصدارات الأحدث.

### س3: هل يمكنني إدراج صور بصيغ مختلفة، مثل PNG أو GIF، في مستند OneNote؟

**ج:** بالطبع. المكتبة تدعم PNG، JPEG، GIF، BMP، والعديد من الصيغ الشائعة الأخرى.

### س4: هل هناك نسخة تجريبية من Aspose.Note for Java متاحة لأغراض الاختبار؟

**ج:** نعم، يمكنك تنزيل نسخة تجريبية مجانية من موقع Aspose لتقييم الـ API قبل الشراء.

### س5: كيف يمكنني الحصول على الدعم الفني لـ Aspose.Note for Java؟

**ج:** يمكنك الحصول على المساعدة بزيارة [المنتدى](https://forum.aspose.com/c/note/28) المخصص لمنتجات Aspose.Note.

## الخاتمة

أصبح لديك الآن مثال كامل وجاهز للإنتاج يوضح **كيفية إضافة صورة إلى OneNote** باستخدام Java، تخصيص مظهرها، وإمكانية **حفظ OneNote كملف PDF**. لا تتردد في تعديل الكود ليتناسب مع سير عملك الخاص—سواءً كنت تبني محرك تقارير، نظام توثيق آلي، أو تطبيق ملاحظات مخصص.

---

**آخر تحديث:** 2026-03-19  
**تم الاختبار مع:** Aspose.Note for Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}