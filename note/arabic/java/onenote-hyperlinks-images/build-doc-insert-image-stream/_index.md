---
date: 2025-12-21
description: تعلم كيفية إنشاء مستند OneNote باستخدام Java وإدراج الصور بسهولة باستخدام
  Aspose.Note for Java. دليل خطوة بخطوة لمطوري Java.
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

## المقدمة

مرحبًا! في هذا الدرس ستقوم **بإنشاء مستند OneNote باستخدام Java** من الصفر وتتعلم كيفية إدراج الصور باستخدام تدفق صورة. سنستعرض كل خطوة، نشرح لماذا كل جزء مهم، ونقدم لك نصائح عملية لتتمكن من تطبيق التقنية في مشاريع حقيقية. في النهاية، ستكون قادرًا على توليد صفحات OneNote برمجيًا وإدراج الصور تمامًا حيث تحتاجها.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.Note for Java  
- **هل يمكنني إدراج صور من Stream؟** نعم – فقط مرّر `InputStream` إلى مُنشئ `Image`.  
- **ما الصيغة التي يمكنني التصدير إليها؟** أي صيغة يدعمها Aspose.Note، مثل PDF, DOCX, HTML.  
- **هل أحتاج إلى رخصة للتطوير؟** رخصة مؤقتة مجانية تعمل للتقييم؛ رخصة كاملة مطلوبة للإنتاج.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى.

## ما هو “create onenote document java”؟

إنشاء مستند OneNote باستخدام Java يعني استخدام واجهة برمجة تطبيقات Aspose.Note لبناء هيكل دفتر ملاحظات برمجيًا — صفحات، مخططات، وعناصر — دون فتح عميل OneNote على سطح المكتب. هذا النهج مثالي لتوليد التقارير تلقائيًا، معالجة دفعات من الملاحظات، أو دمج محتوى OneNote في تطبيقات Java أكبر.

## لماذا تستخدم Aspose.Note for Java لإنشاء مستند onenote باستخدام Java؟

- **تحكم كامل** في تخطيط الصفحة، موضع المخطط، وتنسيق العناصر.  
- **بدون COM interop** – يعمل على أي نظام تشغيل يدعم Java.  
- **خيارات تصدير غنية** – تحويل المستند نفسه إلى PDF, DOCX, HTML، إلخ، باستدعاء واحد.  
- **ملائم للـ Stream** – يمكنك تحميل الصور مباشرة من الذاكرة أو الشبكة أو التخزين السحابي.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من إعداد ما يلي:

### مجموعة تطوير Java (JDK)

JDK حديث (8 أو أحدث) مثبت على جهازك.

### مكتبة Aspose.Note for Java

قم بتنزيل المكتبة من صفحة الإصدار الرسمية لـ Aspose: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### إعداد بيئة التطوير المتكاملة (IDE)

قم بتكوين بيئة التطوير المتكاملة المفضلة لديك (IntelliJ IDEA، Eclipse، VS Code) لتضمين ملفات JAR الخاصة بـ Aspose.Note في مسار الفئة للمشروع.

## استيراد الحزم

لبدء العمل، استورد الفئات المطلوبة من Java و Aspose.Note. هذه الاستيرادات تمنحك الوصول إلى إنشاء المستند، معالجة الصفحات، إدارة المخططات، وإدراج الصور.

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

حدد المجلد الذي يحتوي على صور المصدر وأين سيتم حفظ ملف الإخراج. استبدل العنصر النائب بالمسار الفعلي على جهازك.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: إنشاء كائن المستند

أنشئ كائنًا جديدًا من النوع `Document`. يمثل هذا الكائن دفتر ملاحظات OneNote الذي تقوم ببنائه.

```java
Document doc = new Document();
```

## الخطوة 3: تهيئة كائن الصفحة

أنشئ كائنًا من النوع `Page` سيحمل جميع المخططات والعناصر لهذه الصفحة من دفتر الملاحظات.

```java
Page page = new Page();
```

## الخطوة 4: إنشاء المخطط

يعمل `Outline` كحاوية للعناصر المتموضعه. هنا نحدد الإزاحات العمودية والأفقية لتحديد موقع المخطط على الصفحة.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## الخطوة 5: إنشاء عنصر المخطط

سيستضيف `OutlineElement` الصورة التي سنقوم بإدراجها قريبًا.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## الخطوة 6: تحميل تدفق الصورة

افتح ملف الصورة كـ stream. يتيح لك استخدام الـ stream قراءة الصورة من أي مصدر (نظام ملفات، شبكة، قاعدة بيانات) دون الحاجة لحفظها أولًا على القرص.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## الخطوة 7: إدراج الصورة

أنشئ كائنًا من النوع `Image`. يمكن أن يكون الوسيط الأول `null` عندما تزود الـ stream لاحقًا، لكن للتبسيط نُشير إلى مسار الملف هنا ونحدد محاذاته إلى الجانب الأيمن من الصفحة.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## الخطوة 8: إلحاق الصورة بعنصر المخطط

أضف الصورة إلى عنصر المخطط لتصبح جزءًا من التسلسل الهرمي البصري للصفحة.

```java
outlineElem1.appendChildLast(image);
```

## الخطوة 9: إلحاق عنصر المخطط بالمخطط

الآن قم بربط عنصر المخطط (الذي يحتوي على الصورة) بحاوية المخطط.

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

أخيرًا، احفظ مستند OneNote بالصيغ التي تحتاجها. في هذا المثال نصدر إلى PDF، لكن يمكنك اختيار أي صيغة يدعمها Aspose.Note.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

باتباع هذه الخطوات تكون قد نجحت في **إنشاء مستند OneNote باستخدام Java** وأدرجت صورة باستخدام تدفق إدخال.

## المشكلات الشائعة والنصائح

- **عدم إغلاق الـ Stream** – في بيئة الإنتاج، احرص دائمًا على إغلاق `InputStream` في كتلة `finally` أو استخدم try‑with‑resources.  
- **مسار ملف غير صحيح** – تحقق مرة أخرى من أن `dataDir` ينتهي بالفاصل المناسب (`/` أو `\`).  
- **محاذاة الصورة** – إذا ظهرت الصورة خارج الشاشة، عدل قيم `VerticalOffset`/`HorizontalOffset` للمخطط.  
- **استثناءات الرخصة** – قد تضيف نسخة التقييم علامة مائية إلى الناتج؛ استخدم رخصة صالحة لإزالتها.

## الأسئلة المتكررة

### س1: هل Aspose.Note for Java متوافق مع جميع إصدارات OneNote؟

ج1: يدعم Aspose.Note for Java صيغ ملفات OneNote المتنوعة، مما يضمن التوافق عبر الإصدارات المكتبية، عبر الإنترنت، والهواتف المحمولة.

### س2: هل يمكنني تخصيص مظهر الصور المدخلة في مستندات OneNote باستخدام Aspose.Note for Java؟

ج2: نعم، يمكنك تعديل المحاذاة، الحجم، الدوران، وحتى تطبيق القص باستخدام الخصائص المناسبة لكائن `Image`.

### س3: هل يوفر Aspose.Note for Java دعمًا لصيغ مستندات أخرى غير PDF؟

ج3: بالتأكيد. يمكن للواجهة تصدير إلى DOCX، HTML، XPS، والعديد من الصيغ الأخرى، مما يمنحك مرونة في مشاركة أو أرشفة ملاحظاتك.

### س4: أين يمكنني العثور على موارد إضافية ودعم لـ Aspose.Note for Java؟

ج4: يقدم موقع Aspose الرسمي وثائق شاملة، أمثلة على الشيفرة، منتديات، ورخص مؤقتة للتقييم.

### س5: هل هناك نسخة تجريبية متاحة لـ Aspose.Note for Java؟

ج5: نعم، يمكنك تنزيل نسخة تجريبية مجانية من صفحة الإصدارات الخاصة بـ Aspose لاستكشاف جميع الميزات قبل الشراء.

---

**آخر تحديث:** 2025-12-21  
**تم الاختبار مع:** Aspose.Note for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}