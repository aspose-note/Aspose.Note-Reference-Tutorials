---
date: 2026-01-20
description: تعلم كيفية تعيين نمط الفقرة الافتراضي في OneNote باستخدام Aspise.Note
  للغة Java، وإضافة الخط الافتراضي في OneNote مع تخصيص خط الفقرة.
linktitle: Set Default Paragraph Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: تعيين نمط الفقرة الافتراضي في OneNote - Aspose.Note
url: /ar/java/onenote-styles/set-default-paragraph-style/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين نمط الفقرة الافتراضي في OneNote - Aspose.Note

## المقدمة

في هذا البرنامج التعليمي ستتعلم **كيفية افتراضي يتيح لك إضافة خط افتراضي إلى صفحات OneNote وتخصكمله، مما يوفر عليك تكرار كود التنسيق لكل فقرة.

## إجابات سريعة
- **ما الذي يفعله “set default paragraph style”?** يحدد قالب تنسيق على مستوى الفقرة يتم وراثته من قبل كل فقرة جديدة ما لم تقم بتجاوزها.  
.اطع الفردية.

## ما هو “set default paragraph style”؟
تعيين نمط الفقرة الافتراضي يعني إنشاء كائن `ParagraphStyle` (اسم الخط، الحجم، اللون، إلخ) وتعيينه إلى عنصر، تستخدم كل سطر داخل ذلك الـ `RichText` التنسيق المحدد تلقائيًا ما لم يتجاوزه `TextStyle` معين.

## لماذا تخصيص خط الفقرة في OneNote؟
- **الاتساق:** يضمن مظهرًا موحدًا عبر جميع أقسام الدفتر.  
- **الإنتاجية:** يزيل الحاجة لتنسيق كل فقرة يدويًا.  
- **العلامة التجارية:** يجعل من السهل فرض إرشادات النمط المؤسسية.  

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من وجود ما يلي:

1. مجموعة تطوير جافا (JDK) مثبتة على نظامك.  
2. مكتبة Aspose.Note for Java – قم بتنزيلها من [صفحة التحميل](https://releases.aspose.com/note/java/).  
3. بيئة تطوير متكاملة (IDE) مثل Eclipse أو IntelliJ IDEA لكتابة وتشغيل كود جافا.

## استيراد الحزم

أولاً، استورد الحزم اللازمة لبدء كتابة الكود:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

الآن، دعنا نقسم كود المثال إلى خطوات متعددة:

## الخطوة 1: تهيئة المستند والصفحة والمخطط

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## الخطوة 2: إنشاء عنصر مخطط

```java
OutlineElement outlineElem = new OutlineElement();
```

## الخطوة 3: تعريف نمط الفقرة الافتراضي

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## الخطوة 4: إنشاء نص غني بالنمط الافتراضي

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## الخطوة 5: إلحاق النص الغني بعنصر المخطط

```java
outlineElem.appendChildLast(text);
```

## الخطوة 6: إلحاق عنصر المخطط بالمخطط

```java
outline.appendChildLast(outlineElem);
```

## الخطوة 7: إلحاق المخطط بالصفحة

```java
page.appendChildLast(outline);
```

## الخطوة 8: إلحاق الصفحة بالمستند

```java
document.appendChildLast(page);
```

## الخطوة 9: حفظ المستند

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

سيقوم هذا الكود بتعيين نمط الفقرة الافتراضي في OneNote باستخدام Aspose.Note for Java.

## المشكلات الشائعة والحلول
- **خطأ الخط المفقود على الجهاز الهدف:** يجب تثبيت الخط على النظام الذي يُفتح فيه ملف OneNote؛ وإلا سيعود OneNote إلى الخط الافتراضي.  
- **أخطاء المسار:** تأكد من أن `dataDir` يشير إلى مجلد قابل للكتابة وموجود؛ وإلا سيطلق `document.save` استثناء `IOException`.  
- **الترخيص غير مضبوط:** إذا شغلت هذا بدون ترخيص صالح، سيحتوي الملف المُنشأ على علامة مائية.

## الخلاصة

يمكن تحقيق تعيين نمط الفقرة الافتراضي في OneNote برمجيًا بكفاءة باستخدام Aspose.Note for Java. باتباع الخطوات الموضحة في هذا البرنامج التعليمي، يمكنك دمج هذه الوظيفة بسلاسة في تطبيقات جافا الخاصة بك، إضافة خط افتراضي إلى صفحات OneNote، وتخصيص خط الفقرة ليتوافق مع علامتك التجارية أو معايير الوثائق.

## الأسئلة المتكررة

**س1: هل يمكنني تخصيص نمط الفقرة الافتراضي أكثر؟**  
ج1: نعم، يمكنك تعديل معلمات مثل اسم الخط، الحجم، اللون، المحاذاة، وتباعد الأسطر لتناسب متطلباتك.

**س2: هل يدعم Aspose.Note عمليات تنسيق نصية أخرى؟**  
ج2: بالتأكيد. يوفر Aspose.Note دعمًا واسعًا لمعالجة تنسيق النص، بما في ذلك أنماط الخطوط، النقاط التعداد، المسافات البادئة، وأكثر من ذلك.

**س3: هل Aspose.Note متوافق مع جميع إصدارات OneNote؟**  
ج3: تم تصميم Aspose.Note للعمل مع ملفات Microsoft OneNote عبر إصدارات مختلفة، مما يضمن توافقًا واسعًا.

**س4: هل يمكنني دمج Aspose.Note في مشروع جافا الحالي؟**  
ج4: نعم، يمكنك بسهولة إضافة Aspose.Note إلى مشروعك عن طريق تضمين ملفات JAR أو تبعيات Maven/Gradle واستيراد الحزم المطلوبة.

**س5: هل هناك نسخة تجريبية متاحة لـ Aspose.Note؟**  
ج5: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.Note من خلال [الموقع الإلكتروني](https://releases.aspose.com/).

**س6: كيف أغير النمط الافتراضي بعد إنشاء المستند؟**  
ج6: استخرج `ParagraphStyle` من كائن `RichText` الحالي، عدل خصائصه، وأعد تعيينه، أو أنشئ نمطًا جديدًا وطبقه على فقرات إضافية.

**س7: هل سيؤثر النمط الافتراضي على الفقرات الموجودة في مستند محمل؟**  
ج7: لا. النمط الافتراضي يطبق فقط على الفقرات الجديدة التي تضيفها بعد تعيينه. الفقرات الموجودة تحتفظ بتنسيقها الأصلي ما لم تقم بتعديله صراحةً.

---

**آخر تحديث:** 2026-01-20  
**تم الاختبار مع:** Aspose.Note 24.11 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}