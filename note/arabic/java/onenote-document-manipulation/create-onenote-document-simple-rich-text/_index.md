---
date: 2025-12-08
description: تعلم كيفية تعيين نمط الفقرة وإضافة عنصر المخطط عند إنشاء مستندات OneNote
  في Java باستخدام Aspose.Note. قم بتصدير OneNote إلى PDF وإنشاء ملفات OneNote بسهولة.
language: ar
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: تعيين نمط الفقرة أثناء إنشاء مستند OneNote في Java
url: /java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين نمط الفقرة أثناء إنشاء مستند OneNote في Java

## المقدمة

في بيئة التطوير السريعة اليوم، القدرة على **تعيين نمط الفقرة** برمجياً أمر أساسي لإنتاج ملفات OneNote مصقولة. يوضح هذا الدرس، خطوة بخطوة، كيفية إنشاء مستند OneNote بنص غني بسيط، وتطبيق تنسيق فقرة مخصص، وأخيراً **تصدير OneNote إلى PDF** باستخدام Aspose.Note for Java. سواءً كنت تبني محرك تقارير، أو حلًا آليًا لتدوين الملاحظات، أو خدمة تحويل مستندات، فإن التقنيات التي ستغطيها هنا ستساعدك على **إنشاء ملفات OneNote** بالمظهر الذي تريده تمامًا.

## إجابات سريعة
- **ماذا يعني “تعيين نمط الفقرة”؟** يطبق الخط، الحجم، اللون، وغيرها من التنسيقات على فقرة من النص.  
- **هل يمكنني تصدير النتيجة إلى PDF؟** نعم – ينتهي الدرس بحفظ ملف OneNote كملف PDF.  
- **هل أحتاج إلى ترخيص لـ Aspose.Note؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **ما هي بيئات التطوير المتكاملة المدعومة؟** أي بيئة Java IDE – Eclipse، IntelliJ IDEA، NetBeans، إلخ.  
- **كم من الوقت يستغرق تنفيذ العملية؟** تقريبًا 10‑15 دقيقة لإنشاء مستند أساسي.

## ما هو “تعيين نمط الفقرة” في Aspose.Note؟
يشير تعيين نمط الفقرة إلى تكوين كائن `ParagraphStyle` (اسم الخط، الحجم، اللون، إلخ) وربطه بعقدة `RichText`. يمنحك هذا التحكم الكامل في مظهر النص داخل صفحة OneNote.

## لماذا نعين نمط الفقرة عند إنشاء ملفات OneNote؟
- **الهوية البصرية المتسقة:** تطبيق خطوط وألوان الشركة تلقائيًا.  
- **سهولة القراءة:** الخطوط الأكبر أو الألوان المحددة تحسن إمكانية الوصول.  
- **دقة التصدير:** يتم الحفاظ على النص المنسق عند **تحويل OneNote إلى PDF** لاحقًا.  

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. **مجموعة تطوير جافا (JDK) 1.8+** – أي نسخة حديثة من JDK ستعمل.  
2. **Aspose.Note for Java** – حمّل أحدث ملف JAR من [صفحة تنزيل Aspose.Note](https://releases.aspose.com/note/java/).  
3. **بيئة تطوير متكاملة** (Eclipse، IntelliJ IDEA، أو NetBeans) لتجميع وتشغيل المثال.  

> **نصيحة محترف:** أضف ملف JAR الخاص بـ Aspose.Note إلى مسار الفئة (classpath) في مشروعك عبر Maven أو عن طريق الإشارة إلى الملف يدويًا في IDE.

## استيراد الحزم

أولاً، استورد الفئات التي سنحتاجها. يبقى هذا الجزء دون تغيير.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> فئة `ParagraphStyle` هي المفتاح لـ **تعيين نمط الفقرة** لاحقًا في الدرس.

## دليل خطوة بخطوة

فيما يلي شرح مختصر لكل عملية. كتل الشيفرة هي نفسها تمامًا كما في العينة الأصلية؛ نضيف فقط النص التوضيحي.

### الخطوة 1: تعيين دليل المستند
حدد مكان حفظ الملفات التي سيتم إنشاؤها.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بمسار مطلق أو نسبي على جهازك.

### الخطوة 2: تهيئة كائن المستند
أنشئ كائن `Document` الجذري الذي يمثل ملف OneNote.

```java
Document doc = new Document();
```

### الخطوة 3: تهيئة كائن الصفحة
يتكون ملف OneNote من صفحة أو أكثر؛ نبدأ بصفحة واحدة.

```java
Page page = new Page();
```

### الخطوة 4: تهيئة كائن المخطط (Outline)
تعمل المخططات كحاويات لعناصر المخطط (فكر فيها كأقسام).

```java
Outline outline = new Outline();
```

### الخطوة 5: تهيئة كائن عنصر المخطط (OutlineElement)
هنا نضيف **عنصر مخطط** سيحمل النص الغني الخاص بنا.

```java
OutlineElement outlineElem = new OutlineElement();
```

### الخطوة 6: تعيين نمط النص (تعيين نمط الفقرة)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

مثيل `ParagraphStyle` يحدد الخط، الحجم، واللون—وهنا نُـ **نعيّن نمط الفقرة** للعقدة النصية القادمة.

### الخطوة 7: تهيئة كائن RichText

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

ننشئ عقدة `RichText`، ندرج سلسلة نصية بسيطة، ونرفق النمط المحدد مسبقًا.

### الخطوة 8: إضافة عقدة RichText إلى OutlineElement

```java
outlineElem.appendChildLast(text);
```

الآن النص المنسق يعيش داخل عنصر المخطط.

### الخطوة 9: إضافة عقدة OutlineElement إلى Outline

```java
outline.appendChildLast(outlineElem);
```

المخطط الآن يحتوي على العنصر الذي يحمل فقرتنا.

### الخطوة 10: إضافة عقدة Outline إلى الصفحة

```java
page.appendChildLast(outline);
```

نضع المخطط على الصفحة.

### الخطوة 11: إضافة عقدة الصفحة إلى المستند

```java
doc.appendChildLast(page);
```

المستند الآن يحتوي على صفحة واحدة بنصنا المنسق.

### الخطوة 12: حفظ المستند (تصدير OneNote إلى PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

طريقة `save` تكتب ملف OneNote وتقوم **بتصدير OneNote إلى PDF** في خطوة واحدة. يمكنك أيضًا حفظه كملف `.one` باستخدام `SaveFormat.One` إذا احتجت الصيغة الأصلية.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|---------|-------|------|
| **الملف غير موجود** | `dataDir` يشير إلى مجلد غير موجود. | تأكد من وجود الدليل أو أنشئه برمجيًا (`new File(dataDir).mkdirs();`). |
| **PDF فارغ** | لم يتم إضافة محتوى قبل الحفظ. | تحقق من إلحاق عقدة `RichText` وتعيين النمط. |
| **خط غير مدعوم** | اسم الخط غير مثبت على النظام. | استخدم خطًا شائعًا مثل `"Arial"` أو قم بدمج الخط في المشروع. |

## الأسئلة المتكررة

**س: هل يمكن لـ Aspose.Note التعامل مع تنسيقات معقدة مثل الجداول أو الصور؟**  
ج: نعم، تدعم الـ API الجداول، الصور، الروابط التشعبية، والمزيد من ميزات التخطيط المتقدمة.

**س: هل يمكن **تحويل OneNote PDF** مرة أخرى إلى ملف OneNote؟**  
ج: التحويل المباشر غير متوفر، لكن يمكنك استخراج محتوى PDF وإعادة بناء مستند OneNote باستخدام الـ API.

**س: هل تعمل المكتبة على بيئات Linux/macOS؟**  
ج: بالتأكيد. Aspose.Note for Java مستقل عن النظام؛ ما عليك سوى تثبيت JDK.

**س: كيف أضيف صفحات أو مخططات متعددة؟**  
ج: أنشئ كائنات `Page` و `Outline` إضافية، ثم ألحقها بـ `Document` كما في مثال الصفحة الواحدة.

**س: أين يمكنني العثور على مزيد من الأمثلة؟**  
ج: توثيق Aspose.Note الرسمي ومنتدى [الدعم](https://forum.aspose.com/c/note/28) يحتويان على العديد من عينات الشيفرة.

## الخلاصة

لقد رأيت الآن كيف **تعيّن نمط الفقرة**، **تضيف عنصر مخطط**، وتُنشئ ملف OneNote يمكن **تصديره إلى PDF** باستخدام Aspose.Note for Java. يضمن إدراج النص المنسق في مرحلة الإنشاء أن يبدو المستند النهائي احترافيًا، وأن أي عملية **تحويل OneNote إلى PDF** لاحقة تحتفظ بالتنسيق. لا تتردد في توسيع هذه الأساسيات بإضافة صور، جداول، أو بيانات تعريف مخصصة لتلبية احتياجات مشروعك.

---

**آخر تحديث:** 2025-12-08  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (أحدث إصدار)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}