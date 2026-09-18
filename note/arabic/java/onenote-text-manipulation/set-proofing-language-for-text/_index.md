---
date: 2026-03-29
description: تعلم كيفية تعيين لغة النص في OneNote باستخدام Aspose.Note للغة Java.
  يوضح لك هذا الدليل خطوة بخطوة كيفية إنشاء مستند OneNote، وتغيير لغة النص، وحفظ ملف
  OneNote بكفاءة.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: كيفية تعيين اللغة للنص في OneNote – Aspose.Note
url: /ar/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعيين اللغة للنص في OneNote – Aspose.Note

## مقدمة
إذا كنت بحاجة إلى **كيفية تعيين اللغة** لقطع نص محددة داخل دفتر ملاحظات OneNote، فإن Aspose.Note for Java يجعل ذلك بسيطًا. في هذا البرنامج التعليمي ستتعلم كيفية إنشاء مستند OneNote، وتغيير لغة النص لكلمات أو عبارات فردية، وأخيرًا حفظ ملف OneNote مع تطبيق لغة التدقيق الصحيحة. في النهاية ستفهم لماذا يعتبر تعيين اللغة مهمًا للتدقيق الإملائي والتعريب، وستحصل على عينة كود جاهزة للتنفيذ.

## إجابات سريعة
- **ما الذي يؤثر عليه “set language”؟** إنه يخبر OneNote أي قاموس تدقيق يجب استخدامه للتدقيق الإملائي والنحوي.  
- **هل يمكنني تعيين لغات مختلفة في نفس الملاحظة؟** نعم، يمكنك تعيين لغة لكل مقطع نصي.  
- **هل أحتاج إلى ترخيص لـ Aspose.Note؟** النسخة التجريبية المجانية تعمل للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **ما إصدارات Java المدعومة؟** يدعم Aspose.Note for Java Java 8 والإصدارات الأحدث.  
- **هل الناتج ملف .one؟** نعم، يتم حفظ المستند كملف OneNote *.one*.

## المتطلبات المسبقة
قبل الغوص في الشيفرة، تأكد من أن لديك ما يلي:

1. **Java Development Environment** – تم تثبيت JDK 8 أو أعلى وتكوينه.  
2. **Aspose.Note for Java Library** – قم بتحميل وتثبيت المكتبة من [رابط التحميل](https://releases.aspose.com/note/java/).  
3. **Document Directory** – أنشئ مجلدًا على جهازك حيث سيتم حفظ ملف OneNote المُولد.

## لماذا تعيين اللغة للنص في OneNote؟
تعيين لغة التدقيق يضمن أن يعمل التدقيق الإملائي، واقتراحات القواعد، وفهرسة البحث بشكل صحيح للمحتوى متعدد اللغات. هذا مفيد بشكل خاص لـ:
- **Global teams** تتعاون على دفتر ملاحظات واحد.  
- **Localized documentation** حيث قد يكون كل قسم بلغة مختلفة.  
- **Data‑driven applications** التي تولد ملاحظات برمجيًا للمستخدمين حول العالم.

## استيراد الحزم
ابدأ باستيراد الفئات اللازمة من Aspose.Note وأدوات Java.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## الخطوة 1: إعداد المستند والصفحة
أنشئ مستند OneNote جديدًا وصفحة ستحمل محتواك. تُظهر هذه الخطوة أيضًا **create OneNote document**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## الخطوة 2: إنشاء المخطط والعنصر المخطط
المخطط هو الحاوية لمحتوى الدفتر. هنا نبني الهيكل الذي سيحتوي لاحقًا على النص المتعلق باللغة.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## الخطوة 3: إضافة نص غني مع إعدادات اللغة
الآن نقوم **change text language** عن طريق إرفاق `TextStyle` مع `Locale` محدد لكل مقطع نصي. هذا يوضح **set language for text**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## الخطوة 4: تنظيم العناصر وحفظها
قم بتجميع تسلسل المخطط الهرمي، وأرفقه بالصفحة، وأخيرًا **save OneNote file** مع تطبيق إعدادات اللغة.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## الأخطاء الشائعة والنصائح
- **Locale format** – استخدم وسم IETF BCP‑47 (مثل `en-US`، `de-DE`). سيتسبب وسم غير صحيح في الاعتماد على لغة المستند الافتراضية.  
- **File path** – تأكد من أن `dataDir` يشير إلى مجلد موجود؛ وإلا سيؤدي `document.save` إلى رمي استثناء `IOException`.  
- **Pro tip:** إذا كنت بحاجة لتعيين اللغة لفقرة كاملة، طبّق `TextStyle` على `ParagraphStyle` بدلاً من كل استدعاء `append`.

## الخلاصة
لقد تعلمت الآن **how to set language** لقطع النص الفردية في دفتر ملاحظات OneNote باستخدام Aspose.Note for Java. تتيح لك هذه القدرة **create OneNote document** برمجيًا، **change text language** أثناء التنفيذ، و**save OneNote file** مع بيانات تدقيق دقيقة.

## الأسئلة المتكررة

**س: هل يمكنني تعيين لغة التدقيق للغات أخرى غير المذكورة في المثال؟**  
ج: بالطبع! أضف استدعاءات `append` إضافية مع `Locale.forLanguageTag("xx-XX")` المطلوب.

**س: هل Aspose.Note for Java متوافق مع أحدث إصدارات Java؟**  
ج: نعم، يتم تحديث المكتبة بانتظام لدعم أحدث إصدارات Java.

**س: كيف يمكنني التعامل مع الأخطاء أثناء عملية تعيين اللغة؟**  
ج: قم بلف عملية الحفظ داخل كتلة `try‑catch` لالتقاط `IOException` أو `AsposeException`.

**س: هل يمكنني دمج هذا الكود في تطبيق ويب؟**  
ج: بالتأكيد. فقط أدرج ملف JAR الخاص بـ Aspose.Note في مسار الفئات لمشروع الويب وتأكد من أن الخادم لديه إذن كتابة إلى الدليل المستهدف.

**س: أين يمكنني العثور على أمثلة إضافية ووثائق لـ Aspose.Note for Java؟**  
ج: استكشف [documentation](https://reference.aspose.com/note/java/) للحصول على قائمة كاملة بواجهات برمجة التطبيقات ومشاريع العينة.

---

**آخر تحديث:** 2026-03-29  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}