---
date: 2025-12-21
description: تعلم كيفية إضافة صورة إلى مستندات OneNote باستخدام Java مع Aspose.Note
  for Java. اتبع دليلنا خطوة بخطوة لإدراج الصور وحفظ OneNote كملف PDF إذا رغبت.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: كيفية إضافة صورة إلى OneNote باستخدام Java
url: /ar/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدراج صورة في مستند OneNote باستخدام Java

## مقدمة

في هذا الدرس، سوف نستكشف كيفية إدراج صورة في مستند OneNote باستخدام Java بمساعدة Aspose.Note for Java. Aspose.Note for Java هي مكتبة قوية تتيح للمطورين العمل مع ملفات Microsoft OneNote برمجياً، مما يمكنهم من تنفيذ عمليات مختلفة مثل إنشاء، قراءة، وتعديل مستندات OneNote.

## إجابات سريعة
- **ما هي أسهل طريقة لإضافة صورة إلى OneNote باستخدام Java؟**  
  استخدم فئة `Image` في Aspose.Note for Java وأضفها إلى صفحة.
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟**  
  نعم، يلزم ترخيص تجاري للنشر في بيئات الإنتاج.
- **هل يمكنني تعيين أبعاد مخصصة للصورة؟**  
  بالطبع – استدعِ `setWidth()` و `setHeight()` على كائن `Image`.
- **هل يمكن حفظ ملف OneNote كملف PDF بعد إضافة الصورة؟**  
  نعم، استدعِ `save(..., SaveFormat.Pdf)` **لحفظ OneNote كملف PDF**.
- **ما نسخة Java المدعومة؟**  
  Aspose.Note for Java يعمل مع JDK 8 وما بعده.

## كيفية إضافة صورة إلى OneNote باستخدام Java؟

قبل الغوص في الكود، دعنا نناقش بإيجاز لماذا قد ترغب في تضمين الصور برمجياً في OneNote. سواءً كنت تولد محاضر اجتماعات، تنشئ تقارير آلية، أو تبني خط أنابيب لتوثيق، فإن إدراج الصور يمنح ملاحظاتك سياقًا بصريًا لا يمكن للنص العادي توفيره. مع Aspose.Note for Java يمكنك القيام بذلك بالكامل عبر الكود، دون الحاجة لفتح واجهة OneNote.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك المتطلبات التالية مُعدة:

### 1. مجموعة تطوير Java (JDK)
تأكد من أن لديك مجموعة تطوير Java (JDK) مثبتة على نظامك. يمكنك تنزيل وتثبيت JDK من موقع Oracle.

### 2. مكتبة Aspose.Note for Java
قم بتنزيل وإعداد مكتبة Aspose.Note for Java باتباع [الوثائق](https://reference.aspose.com/note/java/).

## استيراد الحزم

ابدأ باستيراد الحزم الضرورية إلى مشروع Java الخاص بك. تشمل هذه الحزم مكتبة Aspose.Note وغيرها من الاعتمادات المطلوبة.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

دعنا نفصل عملية إدراج صورة في مستند OneNote إلى عدة خطوات:

## الخطوة 1: تحميل مستند OneNote

أولاً، قم بتحميل مستند OneNote الذي تريد إدراج الصورة فيه.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## الخطوة 2: الحصول على الصفحة

استرجع الصفحة في المستند حيث تريد إدراج الصورة.

```java
Page page = oneFile.getFirstChild();
```

## الخطوة 3: تحميل الصورة

حمّل الصورة التي تريد إدراجها في مستند OneNote.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## الخطوة 4: تخصيص خصائص الصورة (اختياري)

اختياريًا، يمكنك تخصيص حجم الصورة، موقعها، ومحاذاتها وفقًا لمتطلباتك. هذا هو المكان الذي تقوم فيه **تعيين أبعاد الصورة Java** النمط.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## الخطوة 5: إضافة الصورة إلى الصفحة

أضف الصورة إلى الصفحة في مستند OneNote.

```java
page.appendChildLast(image);
```

## الخطوة 6: حفظ المستند

احفظ المستند المعدل، بما في ذلك الصورة المُدخلة. يمكنك أيضًا **حفظ OneNote كملف PDF** في هذه المرحلة.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## الخاتمة

في هذا الدرس، تعلمنا كيفية إدراج صورة في مستند OneNote باستخدام Java بمساعدة مكتبة Aspose.Note for Java. باتباع الدليل خطوة بخطوة، يمكنك دمج الصور بسهولة في مستندات OneNote برمجياً.

## الأسئلة المتكررة

### س1: هل يمكنني إدراج صور متعددة في مستند OneNote واحد باستخدام هذه الطريقة؟

نعم، يمكنك إدراج صور متعددة في مستند OneNote واحد عن طريق تكرار العملية الموضحة في هذا الدرس لكل صورة.

### س2: هل Aspose.Note for Java متوافق مع جميع إصدارات OneNote؟

Aspose.Note for Java يدعم العمل مع ملفات OneNote التي تم إنشاؤها في Microsoft OneNote 2010 والإصدارات الأحدث.

### س3: هل يمكنني إدراج صور بصيغ مختلفة، مثل PNG أو GIF، في مستند OneNote؟

نعم، Aspose.Note for Java يدعم إدراج الصور بمختلف الصيغ، بما في ذلك PNG و JPEG و GIF وغيرها.

### س4: هل هناك نسخة تجريبية من Aspose.Note for Java متاحة لأغراض الاختبار؟

نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.Note for Java من الموقع لأغراض التقييم.

### س5: كيف يمكنني الحصول على الدعم الفني لـ Aspose.Note for Java؟

يمكنك الحصول على الدعم الفني لـ Aspose.Note for Java بزيارة [المنتدى](https://forum.aspose.com/c/note/28) المخصص لمنتجات Aspose.Note.

---

**آخر تحديث:** 2025-12-21  
**تم الاختبار مع:** Aspose.Note for Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}