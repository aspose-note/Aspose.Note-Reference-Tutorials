---
date: 2026-03-19
description: تعلم كيفية إضافة صورة إلى OneNote باستخدام Aspose.Note للغة Java. يوضح
  هذا الدليل خطوة بخطوة كيفية إنشاء مستندات OneNote، وإدراج صورة في OneNote، وحفظ
  OneNote كملف PDF.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: كيفية إضافة صورة إلى OneNote باستخدام Java – بناء المستند وإدراج الصورة
url: /ar/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة صورة إلى OneNote باستخدام Java – إنشاء مستند وإدراج صورة

## المقدمة

في هذا البرنامج التعليمي، ستتعلم **كيفية إضافة صورة إلى OneNote** باستخدام Aspose.Note Java API. سنستعرض إنشاء مستند OneNote من الصفر، وإدراج صورة، وحفظ النتيجة كملف PDF. سواءً كنت تبني أداة تقارير، أو تقوم بأتمتة تدوين الملاحظات، أو تحتاج ببساطة إلى تضمين رسومات برمجيًا، فإن هذا الدليل يقدم لك مسارًا واضحًا وتطبيقيًا.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.Note for Java.  
- **هل يمكنني إدراج أي صيغة صورة؟** JPEG, PNG, BMP, GIF and more are supported.  
- **ما صيغ الإخراج المتاحة؟** You can save as OneNote, PDF, XPS, HTML, etc.  
- **هل أحتاج إلى ترخيص للإنتاج؟** Yes, a commercial license is required for non‑trial use.  
- **هل الكود متعدد المنصات؟** Absolutely – Java runs on Windows, Linux, and macOS.

## كيفية إضافة صورة إلى OneNote باستخدام Java

إضافة صورة إلى OneNote تعني تضمين ملف صورة برمجيًا في صفحة OneNote بحيث يظهر بجانب النص أو المخططات أو العناصر الأخرى. تقوم Aspose.Note API بتجريد تنسيق ملف OneNote، مما يتيح لك التركيز على المحتوى بدلاً من بنية XML الأساسية.

### لماذا يتم تضمين صورة في OneNote؟

- **الأتمتة:** Generate meeting minutes with screenshots automatically.  
- **الاتساق:** Ensure every page follows the same layout and branding.  
- **التكامل:** Combine data from other systems (e.g., charts) directly into OneNote notebooks.  
- **متعدد المنصات:** Java lets you run the same code on any server or desktop environment.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1. **Java Development Kit (JDK)** – أي نسخة حديثة (8 أو أحدث).  
2. **Aspose.Note for Java library** – قم بتنزيله من [الموقع الإلكتروني](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA أو Eclipse أو أي محرر متوافق مع Java تفضله.  

## استيراد الحزم

ابدأ باستيراد الفئات الضرورية في ملف Java المصدر الخاص بك:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## دليل خطوة بخطوة

### الخطوة 1: إعداد المستند

أنشئ مستند OneNote جديدًا وحاوية صفحة حيث سيعيش المحتوى.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### الخطوة 2: تهيئة المخطط

يعمل *المخطط* كحاوية للعناصر مثل النص والصور. نضبط إزاحاته إلى الصفر بحيث يبدأ المحتوى من الزاوية العليا اليسرى.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### الخطوة 3: تحميل ومحاذاة الصورة

حمّل الصورة التي تريد تضمينها وقم بمحاذاتها إلى الجانب الأيمن من الصفحة. هنا نضيف فعليًا **صورة إلى OneNote**. يوضح مُنشئ `Image` كيفية **تحميل ملف صورة java** برمجيًا.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### الخطوة 4: إرفاق الصورة بعنصر المخطط

غلف الصورة داخل `OutlineElement`. هذه الخطوة تربط الكائن البصري بهرمية مخطط المستند وتقوم فعليًا **إدراج صورة في OneNote**.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### الخطوة 5: تجميع بنية المستند

أضف عنصر المخطط إلى المخطط، ثم أرفق المخطط بالصفحة، وأخيرًا أضف الصفحة إلى المستند.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### الخطوة 6: حفظ مستند OneNote

احفظ المستند على القرص. في هذا المثال نصدر إلى PDF، مما يوضح كيفية **حفظ OneNote كملف PDF** أو **تحويل OneNote إلى PDF**. يمكنك أيضًا حفظه كملف OneNote أصلي (`.one`) عن طريق تغيير `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## المشكلات الشائعة والحلول

| المشكلة | سبب حدوثها | الحل |
|-------|----------------|-----|
| **الصورة غير ظاهرة** | مسار ملف غير صحيح أو صيغة غير مدعومة. | تحقق من أن `dataDir` يشير إلى المجلد الصحيح واستخدم نوع صورة مدعوم (JPEG، PNG، إلخ). |
| **المستند محفوظ كملف PDF فارغ** | تم ضبط إزاحات المخطط بشكل غير صحيح. | تأكد من استدعاء `setVerticalOffset(0)` و `setHorizontalOffset(0)`، أو عدّل الإزاحات لتضع المحتوى داخل حدود الصفحة. |
| **IOException عند الحفظ** | المجلد الوجهة غير موجود أو يفتقر إلى صلاحية الكتابة. | أنشئ المجلد مسبقًا أو شغّل البرنامج بصلاحيات مناسبة. |

## الأسئلة المتكررة

**س1: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.Note for Java؟**  
A1: يمكنك الوصول إلى الوثائق [هنا](https://reference.aspose.com/note/java/).

**س2: كيف يمكنني تنزيل Aspose.Note for Java؟**  
A2: يمكنك تنزيل Aspose.Note for Java من [صفحة التنزيل](https://releases.aspose.com/note/java/).

**س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Note for Java؟**  
A3: نعم، يمكنك الحصول على نسخة تجريبية مجانية من [الموقع الإلكتروني](https://releases.aspose.com/).

**س4: أين يمكنني الحصول على الدعم لـ Aspose.Note for Java؟**  
A4: للحصول على الدعم، زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28).

**س5: هل يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note for Java؟**  
A5: نعم، يمكنك طلب ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

**س6: هل يمكنني استخدام هذا الكود **لحفظ OneNote كملف PDF** على خادم Linux؟**  
A6: بالطبع. مكتبة Aspose.Note مستقلة عن المنصة، لذا يعمل نفس الكود على Windows وLinux وmacOS.

**س7: هل يدعم الـ API **تضمين صورة في OneNote** بصيغة PNG شفافة؟**  
A7: نعم، ملفات PNG ذات القنوات ألفا مدعومة بالكامل وتحتفظ بالشفافية عند إدراجها.

---

**آخر تحديث:** 2026-03-19  
**تم الاختبار مع:** Aspose.Note for Java 24.12 (latest)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}