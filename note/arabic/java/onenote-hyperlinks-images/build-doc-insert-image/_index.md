---
date: 2025-12-20
description: تعلم كيفية إضافة صورة إلى OneNote باستخدام Aspose.Note للغة Java. دليل
  خطوة بخطوة لإنشاء مستندات OneNote وإدراج الصور برمجيًا.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: كيفية إضافة صورة إلى OneNote باستخدام Java – إنشاء المستند وإدراج الصورة
url: /ar/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة صورة إلى OneNote باستخدام Java – إنشاء مستند وإدراج صورة

## المقدمة

في هذا الدرس، ستتعلم **كيفية إضافة صورة إلى OneNote** باستخدام Aspose.Note Java API. سنستعرض إنشاء مستند OneNote من الصفر، إدراج صورة، وحفظ النتيجة كملف PDF. سواءً كنت تبني أداة تقارير، أو تقوم بأتمتة تدوين الملاحظات، أو تحتاج ببساطة إلى تضمين رسومات برمجياً، فإن هذا الدليل يقدم لك مسارًا واضحًا وتطبيقيًا.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.Note for Java.  
- **هل يمكنني إدراج أي تنسيق صورة؟** تدعم JPEG، PNG، BMP، GIF وغيرها.  
- **ما هي صيغ الإخراج المتاحة؟** يمكنك الحفظ كـ OneNote، PDF، XPS، HTML، إلخ.  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم، يلزم الحصول على ترخيص تجاري للاستخدام غير التجريبي.  
- **هل الشيفرة متعددة المنصات؟** بالتأكيد – Java تعمل على Windows، Linux، و macOS.

## ما هو “إضافة صورة إلى OneNote”؟
إضافة صورة إلى OneNote تعني تضمين ملف صورة داخل صفحة OneNote برمجيًا بحيث تظهر جنبًا إلى جنب مع النص أو المخططات أو العناصر الأخرى. تقوم Aspose.Note API بتجريد تنسيق ملف OneNote، مما يتيح لك التركيز على المحتوى بدلاً من بنية XML الداخلية.

## لماذا نضيف صورة إلى OneNote باستخدام Java؟
- **الأتمتة:** إنشاء محاضر الاجتماعات مع لقطات الشاشة تلقائيًا.  
- **الاتساق:** ضمان أن كل صفحة تتبع نفس التخطيط والعلامة التجارية.  
- **التكامل:** دمج البيانات من أنظمة أخرى (مثل المخططات) مباشرةً في دفاتر OneNote.  
- **متعددة المنصات:** تسمح لك Java بتشغيل نفس الشيفرة على أي خادم أو بيئة سطح مكتب.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من توفر ما يلي:

1. **Java Development Kit (JDK)** – أي نسخة حديثة (8 أو أعلى).  
2. **Aspose.Note for Java library** – حمّلها من [الموقع الإلكتروني](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA، Eclipse، أو أي محرر يدعم Java تفضله.  

## استيراد الحزم

ابدأ باستيراد الفئات الضرورية في ملف المصدر Java الخاص بك:

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

إنشاء مستند OneNote جديد وحاوية صفحة حيث سيُوضع المحتوى.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### الخطوة 2: تهيئة المخطط (Outline)

المخطط *outline* يعمل كحاوية للعناصر مثل النصوص والصور. نضبط إزاحاته إلى الصفر لتبدأ المحتويات من الزاوية العليا اليسرى.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### الخطوة 3: تحميل الصورة ومحاذاتها

حمّل الصورة التي تريد تضمينها وحاذها إلى الجانب الأيمن من الصفحة. هنا يتم **إضافة صورة إلى OneNote** فعليًا.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### الخطوة 4: ربط الصورة بعنصر المخطط

لف الصورة داخل `OutlineElement`. هذه الخطوة تربط الكائن البصري بهيكل المخطط في المستند.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### الخطوة 5: تجميع بنية المستند

أضف عنصر المخطط إلى المخطط، ثم اربط المخطط بالصفحة، وأخيرًا أضف الصفحة إلى المستند.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### الخطوة 6: حفظ مستند OneNote

احفظ المستند على القرص. في هذا المثال نصدر إلى PDF، لكن يمكنك أيضًا حفظه كملف OneNote أصلي (`.one`) بتغيير قيمة `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|--------|-------|------|
| **الصورة لا تظهر** | مسار الملف غير صحيح أو تنسيق غير مدعوم. | تحقق من أن `dataDir` يشير إلى المجلد الصحيح واستخدم تنسيق صورة مدعوم (JPEG، PNG، إلخ). |
| **المستند يُحفظ كملف PDF فارغ** | إزاحات المخطط مضبوطة بشكل غير صحيح. | تأكد من استدعاء `setVerticalOffset(0)` و `setHorizontalOffset(0)`، أو عدّل الإزاحات لتضع المحتوى داخل حدود الصفحة. |
| **IOException عند الحفظ** | المجلد الوجهة غير موجود أو لا يملك صلاحية كتابة. | أنشئ المجلد مسبقًا أو شغّل البرنامج بصلاحيات مناسبة. |

## الأسئلة المتكررة

**س1: أين يمكنني العثور على وثائق Aspose.Note for Java؟**  
ج1: يمكنك الوصول إلى الوثائق [من هنا](https://reference.aspose.com/note/java/).

**س2: كيف يمكنني تحميل Aspose.Note for Java؟**  
ج2: يمكنك تحميل Aspose.Note for Java من [صفحة التحميل](https://releases.aspose.com/note/java/).

**س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Note for Java؟**  
ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية من [الموقع الإلكتروني](https://releases.aspose.com/).

**س4: أين يمكنني الحصول على دعم لـ Aspose.Note for Java؟**  
ج4: للحصول على الدعم، زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28).

**س5: هل يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note for Java؟**  
ج5: نعم، يمكنك طلب ترخيص مؤقت [من هنا](https://purchase.aspose.com/temporary-license/).

---

**آخر تحديث:** 2025-12-20  
**تم الاختبار باستخدام:** Aspose.Note for Java 24.12 (latest)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}