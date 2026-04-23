---
date: 2026-03-19
description: تعلم كيفية إنشاء مستند OneNote باستخدام Aspose.Note for Java وإدراج الصور
  من تدفق. دليل خطوة بخطوة لمطوري Java.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: كيفية إنشاء مستند OneNote باستخدام Java – بناء المستند وإدراج صورة عبر التدفق
url: /ar/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء مستند OneNote باستخدام Java – بناء المستند وإدراج صورة عبر Stream

## مقدمة

مرحبًا! في هذا الدرس ستقوم **بإنشاء مستند OneNote باستخدام Java** من الصفر وتتعلم كيفية إدراج الصور باستخدام تدفق صورة. سنمرّ بكل خطوة، نشرح لماذا كل جزء مهم، ونقدم لك نصائح عملية لتتمكن من تطبيق التقنية في مشاريع حقيقية. في النهاية، ستكون قادرًا على إنشاء صفحات OneNote برمجيًا وإدراج الصور تمامًا حيث تحتاجها.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.Note for Java  
- **هل يمكنني إدراج صور من تدفق؟** نعم – فقط مرّر `InputStream` إلى مُنشئ `Image`.  
- **ما الصيغة التي يمكنني التصدير إليها؟** أي صيغة يدعمها Aspose.Note، مثل PDF، DOCX، HTML.  
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص مؤقت مجاني يعمل للتقييم؛ الترخيص الكامل مطلوب للإنتاج.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى.

## ما هو “إنشاء مستند OneNote باستخدام Java”؟

إنشاء مستند OneNote باستخدام Java يعني استخدام Aspose.Note API لبناء بنية دفتر ملاحظات برمجيًا — صفحات، مخططات، وعناصر — دون فتح عميل OneNote لسطح المكتب. هذا النهج مثالي لإنشاء تقارير تلقائية، معالجة دفعات من الملاحظات، أو دمج محتوى OneNote في تطبيقات Java الأكبر.

## لماذا تستخدم Aspose.Note for Java لإنشاء مستند OneNote باستخدام Java؟

- **تحكم كامل** في تخطيط الصفحة، موضع المخطط، وتنسيق العناصر.  
- **بدون تفاعل COM** – يعمل على أي نظام تشغيل يدعم Java.  
- **خيارات تصدير غنية** – تحويل نفس المستند إلى PDF، DOCX، HTML، إلخ، باستدعاء واحد.  
- **ملائم للتدفق** – يمكنك تحميل الصور مباشرة من الذاكرة، الشبكة، أو التخزين السحابي.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من إعداد ما يلي:

### مجموعة تطوير Java (JDK)

JDK حديث (8 أو أحدث) مثبت على جهازك.

### مكتبة Aspose.Note for Java

حمّل المكتبة من صفحة الإصدار الرسمية لـ Aspose: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### إعداد بيئة التطوير المتكاملة (IDE)

قم بتكوين بيئة التطوير المتكاملة المفضلة لديك (IntelliJ IDEA، Eclipse، VS Code) لتضمين ملفات JAR الخاصة بـ Aspose.Note في مسار الفئة (classpath) للمشروع.

## استيراد الحزم

لبدء العمل، استورد الفئات المطلوبة من Java و Aspose.Note. هذه الاستيرادات تمنحك الوصول إلى إنشاء المستندات، معالجة الصفحات، إدارة المخططات، وإدراج الصور.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## الخطوة 1: إعداد دليل المستند

حدد المجلد الذي يحتوي على صور المصدر ومكان حفظ ملف الإخراج. استبدل العنصر النائب بالمسار الفعلي على جهازك.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: إنشاء كائن المستند

أنشئ كائنًا جديدًا من نوع `Document`. هذا الكائن يمثل دفتر ملاحظات OneNote الذي تقوم بإنشائه.

```java
Document doc = new Document();
```

## الخطوة 3: تهيئة كائن الصفحة

أنشئ كائن `Page` سيحتوي على جميع المخططات والعناصر لهذه الصفحة من دفتر الملاحظات.

```java
Page page = new Page();
```

## الخطوة 4: إنشاء المخطط

`Outline` يعمل كحاوية للعناصر المموضعّة. هنا نحدد الإزاحات العمودية والأفقية لتحديد موقع المخطط على الصفحة.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## الخطوة 5: إنشاء عنصر المخطط

`OutlineElement` سيستضيف الصورة التي سنقوم بإدراجها.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## الخطوة 6: تحميل تدفق الصورة

افتح ملف الصورة كـ stream. استخدام الـ stream يتيح لك قراءة الصورة من أي مصدر (نظام الملفات، الشبكة، قاعدة البيانات) دون الحاجة لحفظها أولاً على القرص.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## الخطوة 7: إدراج الصورة

أنشئ كائن `Image`. يمكن أن يكون الوسيط الأول `null` عندما تقدم تدفقًا لاحقًا، لكن للتبسيط نشير إلى مسار الملف هنا ونضبط محاذاته إلى الجانب الأيمن من الصفحة.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## الخطوة 8: إلحاق الصورة بعنصر المخطط

أضف الصورة إلى عنصر المخطط لتصبح جزءًا من هيكل الصفحة البصري.

```java
outlineElem1.appendChildLast(image);
```

## الخطوة 9: إلحاق عنصر المخطط بالمخطط

الآن قم بإرفاق عنصر المخطط (الذي يحتوي على الصورة) بحاوية المخطط.

```java
outline1.appendChildLast(outlineElem1);
```

## الخطوة 10: إلحاق المخطط بالصفحة

ضع المخطط على الصفحة.

```java
page.appendChildLast(outline1);
```

## الخطوة 11: إلحاق الصفحة بالمستند

أضف الصفحة المكتملة إلى كائن المستند.

```java
doc.appendChildLast(page);
```

## الخطوة 12: حفظ المستند

أخيرًا، احفظ مستند OneNote بالصيغة التي تحتاجها. في هذا المثال نصدر إلى PDF، لكن يمكنك اختيار أي صيغة يدعمها Aspose.Note.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

باتباع هذه الخطوات، لقد نجحت في **إنشاء مستند OneNote باستخدام Java** وإدراج صورة باستخدام تدفق إدخال.

## المشكلات الشائعة والنصائح

- **عدم إغلاق الـ Stream** – في بيئة الإنتاج، يجب دائمًا إغلاق `InputStream` في كتلة `finally` أو استخدام try‑with‑resources.  
- **مسار ملف غير صحيح** – تحقق مرة أخرى أن `dataDir` ينتهي بالفاصل المناسب (`/` أو `\`).  
- **محاذاة الصورة** – إذا ظهرت الصورة خارج الشاشة، عدّل قيم `VerticalOffset`/`HorizontalOffset` للمخطط.  
- **استثناءات الترخيص** – قد تضيف نسخة التقييم علامة مائية إلى الناتج؛ استخدم ترخيصًا صالحًا لإزالتها.

## الأسئلة المتكررة

### س1: هل Aspose.Note for Java متوافق مع جميع إصدارات OneNote؟

A1: يدعم Aspose.Note for Java صيغ ملفات OneNote المتنوعة، مما يضمن التوافق عبر الإصدارات المكتبية، عبر الإنترنت، والهواتف المحمولة.

### س2: هل يمكنني تخصيص مظهر الصور المدخلة في مستندات OneNote باستخدام Aspose.Note for Java؟

A2: نعم، يمكنك تعديل المحاذاة، الحجم، الدوران، وحتى تطبيق القص باستخدام الخصائص المقابلة على كائن `Image`.

### س3: هل يوفر Aspose.Note for Java دعمًا لصيغ مستندات أخرى غير PDF؟

A3: بالتأكيد. يمكن للـ API التصدير إلى DOCX، HTML، XPS، والعديد من الصيغ الأخرى، مما يمنحك مرونة في مشاركة أو أرشفة ملاحظاتك.

### س4: أين يمكنني العثور على موارد إضافية ودعم لـ Aspose.Note for Java؟

A4: يقدم موقع Aspose الرسمي وثائق شاملة، أمثلة على الشيفرة، منتديات، وترخيصات مؤقتة للتقييم.

### س5: هل هناك نسخة تجريبية متاحة لـ Aspose.Note for Java؟

A5: نعم، يمكنك تنزيل نسخة تجريبية مجانية من صفحة إصدارات Aspose لاستكشاف جميع الميزات قبل الشراء.

## الخاتمة

الآن لديك مثال كامل من البداية إلى النهاية حول كيفية **إنشاء مستند OneNote باستخدام Java** وإدراج الصور مباشرةً من `InputStream`. لا تتردد في تجربة عناصر إضافية — نص، جداول، أو أشكال — لإثراء ملاحظاتك. عندما تكون جاهزًا، استكشف خيارات التصدير المتعددة التي يوفرها Aspose.Note لمشاركة محتوى OneNote كـ PDF، DOCX، HTML، وأكثر.

---

**آخر تحديث:** 2026-03-19  
**تم الاختبار باستخدام:** Aspose.Note for Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}