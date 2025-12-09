---
date: 2025-12-02
description: تعلم كيفية إنشاء صفحة OneNote بعنوان باستخدام Java و Aspose.Note للـ
  Java. يوضح هذا الدليل كيفية تعيين عنوان صفحة OneNote وتخصيص خط العنوان.
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: كيفية إنشاء صفحة OneNote بعنوان - Java
url: /ar/java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء صفحة OneNote بعنوان - Java

## مقدمة

إذا كنت بحاجة إلى **كيفية إنشاء صفحة OneNote** برمجياً، فإن Aspose.Note for Java يجعل ذلك بسيطاً. في هذا البرنامج التعليمي ستتعلم كيفية إنشاء ملف OneNote، وتعيين عنوان الصفحة، وحتى تخصيص خط العنوان—كل ذلك من خلال كود Java. في النهاية، ستحصل على مستند OneNote جاهز للاستخدام يمكنك دمجه في أي تطبيق Java.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.Note for Java.
- **هل يمكنني تعيين خط مخصص للعنوان؟** نعم – استخدم `ParagraphStyle` لتحديد اسم الخط، الحجم، واللون.
- **ما نسخة Java المدعومة؟** أي JDK 8+ (واجهة برمجة التطبيقات متوافقة مع الإصدارات السابقة).
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تعمل للاختبار؛ الترخيص مطلوب للإنتاج.
- **أين يتم حفظ المخرجات؟** تقوم بتحديد المسار في المتغير `dataDir`.

## ما هو عنوان صفحة OneNote؟
عنوان صفحة OneNote هو الرأس المعروض في أعلى كل صفحة. عادةً ما يتضمن اسم الصفحة، تاريخ الإنشاء، والوقت. ضبط هذا العنوان برمجياً يساعدك على إنشاء دفاتر ملاحظات متسقة ومنظمة بشكل جيد.

## لماذا يتم ضبط عنوان صفحة OneNote برمجياً؟
- **الأتمتة:** إنشاء تقارير أو ملاحظات اجتماعات دون تحرير يدوي.  
- **الاتساق:** فرض معيار تسمية عبر جميع الصفحات.  
- **التكامل:** دمج OneNote مع أنظمة أخرى (مثل CRM، أدوات إدارة المشاريع).  

## المتطلبات المسبقة

- **Java Development Kit (JDK)** – الإصدار 8 أو أعلى.  
- **Aspose.Note for Java** – حمّل من الموقع الرسمي **[هنا](https://releases.aspose.com/note/java/)**.  
- **IDE** – IntelliJ IDEA أو Eclipse أو NetBeans (حسب اختيارك).

## استيراد الحزم

أولاً، استورد الفئات التي سنحتاجها من مكتبة Aspose.Note.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### الخطوة 1: إعداد دليل المستند  
حدد المكان الذي سيتم حفظ ملف OneNote المُولد فيه.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### الخطوة 2: إنشاء كائن المستند  
أنشئ كائن `Document` جديد – هذا يمثل ملف OneNote الذي ستقوم بإنشائه.

```java
// Create an object of the Document class
Document doc = new Document();
```

### الخطوة 3: تهيئة كائن الصفحة  
أنشئ كائن `Page` الذي سيحمل العنوان وأي محتوى.

```java
// Initialize Page class object
Page page = new Page();
```

### الخطوة 4: تعيين نمط النص الافتراضي  
حدد `ParagraphStyle` افتراضي سيتم تطبيقه على نص العنوان. هنا نقوم **بتخصيص خط عنوان OneNote**.

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### الخطوة 5: تعيين خصائص عنوان الصفحة  
هنا نقوم **بتعيين عنوان صفحة OneNote** – نص العنوان، التاريخ، والوقت. يمكنك تعديل السلاسل لتتناسب مع حالتك.

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### الخطوة 6: ربط العنوان بالصفحة  
الآن نقوم **بإضافة العنوان إلى OneNote** بربط كائن `Title` مع `Page`.

```java
page.setTitle(title);
```

### الخطوة 7: إلحاق الصفحة بالمستند  
أضف الصفحة المُكوَّنة إلى بنية المستند.

```java
doc.appendChildLast(page);
```

### الخطوة 8: حفظ مستند OneNote  
حدد اسم ملف الإخراج واحفظ الدفتر. هذا يُكمل عملية **إنشاء ملف OneNote باستخدام Java**.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## المشكلات الشائعة والنصائح

| المشكلة | الحل |
|-------|----------|
| **مسار ملف غير صالح** | تأكد من أن `dataDir` ينتهي بفاصل مناسب (`/` أو `\\`) وأن المجلد موجود. |
| **العنوان غير مرئي** | تحقق من أن `ParagraphStyle` تم تطبيقه على كل عنصر `RichText`. |
| **استثناء الترخيص** | استخدم ترخيص تجريبي للاختبار؛ طبق ترخيص كامل قبل النشر. |
| **التاريخ يظهر شهرًا خاطئًا** | الأشهر في Java تبدأ من الصفر؛ `cal.set(2018, 04, 03)` يحدد في الواقع مايو. عدّل وفقًا لذلك. |

## الأسئلة المتكررة

**س: هل Aspose.Note for Java متوافق مع إصدارات Java المختلفة؟**  
ج: نعم، المكتبة تعمل مع Java 8 وما بعده، مما يمنحك مرونة عبر البيئات.

**س: هل يمكنني تخصيص نمط الخط وحجمه لعنوان الصفحة؟**  
ج: بالتأكيد! استخدم `ParagraphStyle` (كما هو موضح في الخطوة 4) لتعيين أي اسم خط، حجم، ولون.

**س: كيف يمكنني إضافة محتوى إضافي (مثل الفقرات أو الصور) إلى الصفحة؟**  
ج: أنشئ كائنات `RichText` أو `Image` إضافية، عيّن أنماطها، وأضفها إلى `Page` باستخدام `page.appendChildLast(yourObject)`.

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.Note for Java؟**  
ج: نعم، يمكنك تحميل نسخة تجريبية مجانية من موقع Aspose لتقييم جميع الميزات.

**س: أين يمكنني الحصول على الدعم إذا واجهت مشاكل؟**  
ج: زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على مساعدة المجتمع أو افتح تذكرة دعم مع Aspose.

---

**آخر تحديث:** 2025-12-02  
**تم الاختبار مع:** Aspose.Note for Java 24.12 (الأحدث وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}