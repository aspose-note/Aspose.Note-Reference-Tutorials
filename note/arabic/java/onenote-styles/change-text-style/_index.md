---
date: 2026-01-18
description: تعلم كيفية تعيين لون الخط في Java في OneNote باستخدام Aspose.Note، وتظليل
  النص، وتعديل حجم الخط، وحفظ OneNote كملف PDF. دليل خطوة بخطوة مع الشيفرة.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: تعيين لون الخط في OneNote باستخدام Java – Aspose.Note
url: /ar/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين لون الخط Java في OneNote – Aspose.Note

## المقدمة

في هذا البرنامج التعليمي ستكتشف كيفية **set font color Java** للنص داخل مستند OneNote باستخدام Aspose.Note for Java API. سنستعرض تحميل ملف `.one`، الوصول إلى عقد RichText الخاصة به، تطبيق اللون، التظليل، وتغييرات حجم الخط، وأخيرًا **saving OneNote as PDF**. سواء كنت بحاجة إلى **highlight text onenote**، أو **modify font size onenote**، أو ببساطة تغيير نمط النص العام، فإن الخطوات أدناه توفر لك حلًا كاملًا وجاهزًا للإنتاج.

## إجابات سريعة
- **هل يمكنني تغيير لون الخط لكلمات معينة؟** نعم – قم بالتكرار عبر كائنات `TextRun` واستخدم `setFontColor`.
- **هل يتيح لي Aspose.Note حفظ OneNote كملف PDF؟** بالطبع؛ استخدم `document.save("output.pdf")`.
- **ما إصدار Java المطلوب؟** Java 8 أو أعلى.
- **هل يدعم التظليل؟** استخدم `setHighlight(Color)` على `TextStyle`.
- **هل يمكنني تحويل OneNote إلى PDF بسطر واحد؟** ليس مباشرةً، لكن طريقة `save` تتعامل مع التحويل.

## ما هو “set font color java”؟

تشير العبارة إلى تعيين لون خط جديد للعنصر النصي في ملف OneNote برمجيًا باستخدام كود Java. مع Aspose.Note، تحصل على تحكم كامل في سمات النمط مثل لون الخط، التظليل، والحجم دون فتح واجهة OneNote.

## لماذا تغيير نمط النص في OneNote؟

- **تحسين قابلية القراءة** – النص الملون أو المظلل يجذب الانتباه إلى النقاط الرئيسية.
- **اتساق العلامة التجارية** – فرض ألوان الشركة عبر ملاحظات الاجتماعات.
- **جودة التصدير** – الملاحظات المنسقة تبدو احترافية عندما **convert onenote to pdf** للمشاركة.

## المتطلبات المسبقة

1. معرفة أساسية ببرمجة Java.  
2. JDK 8 أو أحدث مثبت.  
3. مكتبة Aspose.Note for Java مضافة إلى مشروعك (Maven/Gradle أو JAR يدوي).  
4. ملف OneNote تجريبي (`Sample1.one`) للتجربة.  

## استيراد الحزم

أولاً، استورد الفئات التي سنحتاجها:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل المستند

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

نقوم بتحميل ملف OneNote (`Sample1.one`) حتى يتمكن Aspose.Note من العمل مع هيكله الداخلي.

### الخطوة 2: الوصول إلى عقد RichText

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

كائنات `RichText` تحتوي على الفقرات الفعلية. من خلال استرجاع العقدة الأولى نحصل على مقبض للنص الذي نريد تنسيقه.

### الخطوة 3: تغيير نمط النص (set font color java)

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

داخل الحلقة نقوم **set font color Java** إلى اللون الأصفر، نطبق تظليلًا أزرق (مظهرًا **highlight text onenote**)، ونزيد الحجم إلى 20 نقطة، موضحين **modify font size onenote**.

### الخطوة 4: حفظ المستند (save onenote as pdf)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

استدعاء `save` بامتداد `.pdf` يقوم تلقائيًا **convert onenote to pdf**، مما يمنحك ملفًا جاهزًا للمشاركة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|---------|-------|------|
| لا يظهر تغيير اللون | تم فتح المستند في OneNote قبل الحفظ | أغلق OneNote أو أعد تحميل الملف بعد انتهاء عملية Java |
| لم يتم تطبيق التظليل | استخدام لون يتطابق مع الخلفية | اختر `Color` متباين (مثال: `Color.yellow`) |
| `document.save` يرمي `IOException` | مسار الإخراج غير صالح | تأكد من وجود الدليل ولديك أذونات كتابة |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق هذه التغييرات النمطية على أقسام معينة فقط من ملف OneNote الخاص بي؟**  
**ج:** نعم – قم بتصفية عقد `RichText` حسب الـ `Section` أو `Page` الأب قبل التكرار على `TextRun`s.

**س: بخلاف اللون، التظليل، والحجم، ما التنسيقات الأخرى التي يمكن لـ Aspose.Note التعامل معها؟**  
**ج:** يمكنك تغيير عائلة الخط، الغامق/المائل/التسطير، المحاذاة، وحتى تباعد الفقرات.

**س: هل من الممكن معالجة عدة ملفات OneNote دفعة واحدة؟**  
**ج:** بالتأكيد. ضع منطق التحميل والتنسيق داخل حلقة تعالج كل ملف `.one` في مجلد.

**س: هل تدعم المكتبة الحفظ مباشرةً إلى صيغ أخرى مثل DOCX؟**  
**ج:** نعم – يمكن لـ Aspose.Note تصدير إلى PDF، DOCX، HTML، والعديد من صيغ الصور.

**س: أين يمكنني العثور على مزيد من الأمثلة ومرجع API؟**  
**ج:** زر موقع توثيق Aspose.Note الرسمي، استكشف مرجع API، وحمّل النسخة التجريبية المجانية للتجربة العملية.

## الخلاصة

أصبح لديك الآن مثال كامل من البداية إلى النهاية حول كيفية **set font color Java**، تظليل النص، تعديل حجم الخط، و**save OneNote as PDF** باستخدام Aspose.Note. لا تتردد في تعديل الكود لاستهداف صفحات محددة، تطبيق تنسيق شرطي، أو دمجه في خطوط معالجة مستندات أكبر.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-01-18  
**تم الاختبار مع:** Aspose.Note 24.11 for Java  
**المؤلف:** Aspose