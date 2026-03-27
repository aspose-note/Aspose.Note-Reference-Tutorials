---
date: 2026-02-18
description: تعلم كيفية تعيين نمط الفقرة وإضافة عنصر المخطط عند إنشاء مستندات OneNote
  بلغة Java باستخدام Aspose.Note. قم بتصدير OneNote إلى PDF، احفظ OneNote كملف PDF،
  وأنشئ ملفات OneNote بسهولة.
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: تصدير OneNote إلى PDF – تعيين نمط الفقرة أثناء إنشاء مستند OneNote في Java
url: /ar/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين نمط الفقرة أثناء إنشاء مستند OneNote في Java

## مقدمة

في مشهد التطوير السريع اليوم، القدرة على **export OneNote to PDF** برمجياً أمر أساسي لإنتاج مستندات مصقولة وجاهزة للمشاركة. يشرح هذا الدليل كيفية إنشاء ملف OneNote، وتطبيق نمط فقرة مخصص، وأخيراً **exporting OneNote to PDF** باستخدام Aspose.Note for Java. سواءً كنت تبني محرك تقارير، أو حلًا تلقائيًا لتدوين الملاحظات، أو خدمة تحويل مستندات، فإن التقنيات التي يغطيها هذا الدليل ستساعدك على **save OneNote as PDF** مع تحكم دقيق في التنسيق.

## إجابات سريعة
- **What does “set paragraph style” mean?** يطبق الخط، الحجم، اللون، وتنسيقات أخرى على فقرة من النص.  
- **Can I export the result to PDF?** نعم – ينتهي الدليل بحفظ ملف OneNote كملف PDF.  
- **Do I need a license for Aspose.Note?** نسخة تجريبية مجانية تكفي للتقييم؛ يلزم وجود ترخيص للاستخدام في الإنتاج.  
- **Which IDEs are supported?** أي بيئة تطوير Java – Eclipse، IntelliJ IDEA، NetBeans، إلخ.  
- **How long does the implementation take?** تقريباً 10‑15 دقيقة لإنشاء مستند أساسي.

## ما هو “set paragraph style” في Aspose.Note؟
يشير تعيين نمط الفقرة إلى تكوين كائن `ParagraphStyle` (اسم الخط، الحجم، اللون، إلخ) وربطه بعقدة `RichText`. يمنحك هذا تحكمًا كاملاً في كيفية ظهور النص داخل صفحة OneNote.

## كيف يتم تعيين نمط الفقرة في OneNote؟
تطبيق النمط بسيط كإنشاء مثيل `ParagraphStyle`، تخصيص خصائصه، وتعيينه إلى عنصر `RichText`. تجعل الـ API هذا عملية سطر واحد بمجرد أن يصبح كائن النمط جاهزًا.

## لماذا تصدير OneNote إلى PDF؟
- **Consistent branding:** الحفاظ على خطوط الشركة وألوانها عند مشاركة الملاحظات خارجيًا.  
- **Readability:** يحتفظ PDF بالتخطيط الدقيق، مما يجعله مثالياً للطباعة أو الأرشفة.  
- **Cross‑platform access:** يمكن للمستلمين عرض PDF على أي جهاز دون الحاجة إلى OneNote.  

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من وجود ما يلي:

1. **Java Development Kit (JDK) 1.8+** – أي نسخة حديثة من JDK ستعمل.  
2. **Aspose.Note for Java** – قم بتحميل أحدث ملف JAR من [Aspose.Note download page](https://releases.aspose.com/note/java/).  
3. **An IDE** (Eclipse, IntelliJ IDEA, أو NetBeans) لتجميع وتشغيل العينة.  

> **نصيحة احترافية:** أضف ملف JAR الخاص بـ Aspose.Note إلى مسار الفئة (classpath) في مشروعك عبر Maven أو عن طريق الإشارة يدويًا إلى ملف JAR في IDE الخاص بك.

## استيراد الحزم

أولاً، استورد الفئات التي سنحتاجها. هذه الكتلة تبقى دون تغيير.

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

> فئة `ParagraphStyle` هي المفتاح لـ **set paragraph style** لاحقًا في الدليل.

## دليل خطوة بخطوة

فيما يلي شرح مختصر لكل عملية. كتل الشيفرة هي نفسها تمامًا كما في العينة الأصلية؛ نضيف فقط نصًا توضيحيًا.

### الخطوة 1: تعيين دليل المستند
حدد المكان الذي سيتم حفظ الملفات المولدة فيه.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بمسار مطلق أو نسبي على جهازك.

### الخطوة 2: تهيئة كائن Document
إنشاء كائن `Document` الجذر الذي يمثل ملف OneNote.

```java
Document doc = new Document();
```

### الخطوة 3: تهيئة كائن Page
يتكون ملف OneNote من صفحة واحدة أو أكثر؛ نبدأ بصفحة واحدة.

```java
Page page = new Page();
```

### الخطوة 4: تهيئة كائن Outline
تعمل الـ Outlines كحاويات لعناصر المخطط (فكر فيها كأقسام).

```java
Outline outline = new Outline();
```

### الخطوة 5: تهيئة كائن OutlineElement
هنا نـ**add outline element** التي ستحمل النص المنسق لدينا.

```java
OutlineElement outlineElem = new OutlineElement();
```

### الخطوة 6: تعيين نمط النص (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

مثيل `ParagraphStyle` يحدد الخط، الحجم، واللون—هنا نـ**set paragraph style** للنود النصية القادمة.

### الخطوة 7: تهيئة كائن RichText

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

ننشئ عقدة `RichText`، ندرج سلسلة بسيطة، ونرفق النمط المحدد مسبقًا.

### الخطوة 8: إضافة عقدة RichText إلى OutlineElement

```java
outlineElem.appendChildLast(text);
```

الآن النص المنسق موجود داخل عنصر المخطط.

### الخطوة 9: إضافة عقدة OutlineElement إلى Outline

```java
outline.appendChildLast(outlineElem);
```

المخطط الآن يحتوي على العنصر الذي يحمل فقرتنا.

### الخطوة 10: إضافة عقدة Outline إلى Page

```java
page.appendChildLast(outline);
```

نضع المخطط على الصفحة.

### الخطوة 11: إضافة عقدة Page إلى Document

```java
doc.appendChildLast(page);
```

المستند الآن يحتوي على صفحة واحدة مع النص المنسق.

### الخطوة 12: حفظ المستند (Export OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

طريقة `save` تكتب ملف OneNote وتـ**exports OneNote PDF** في خطوة واحدة. يمكنك أيضًا حفظه كـ `.one` باستخدام `SaveFormat.One` إذا كنت تحتاج الصيغة الأصلية.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **File not found** | `dataDir` يشير إلى مجلد غير موجود. | تأكد من وجود الدليل أو أنشئه برمجياً (`new File(dataDir).mkdirs();`). |
| **Blank PDF** | لم يتم إضافة أي محتوى قبل الحفظ. | تحقق من إلحاق عقدة `RichText` وتعيين النمط. |
| **Unsupported font** | اسم الخط غير مثبت على النظام. | استخدم خطًا شائعًا مثل `"Arial"` أو قم بدمج الخط في المشروع. |

## الأسئلة المتكررة

**س: هل يمكن لـ Aspose.Note التعامل مع تنسيقات معقدة مثل الجداول أو الصور؟**  
ج: نعم، تدعم الـ API الجداول، الصور، الروابط التشعبية، ومزيدًا من ميزات التخطيط المتقدمة.

**س: هل من الممكن **convert OneNote PDF** مرة أخرى إلى ملف OneNote؟**  
ج: لا يتوفر تحويل مباشر، لكن يمكنك استخراج محتوى PDF وإعادة بناء مستند OneNote باستخدام الـ API.

**س: هل تعمل المكتبة على بيئات Linux/macOS؟**  
ج: بالتأكيد. Aspose.Note for Java مستقل عن المنصة؛ فقط تأكد من تثبيت JDK.

**س: كيف يمكنني إضافة صفحات أو مخططات متعددة؟**  
ج: أنشئ كائنات `Page` و `Outline` إضافية، ثم ألحقها بـ `Document` كما في مثال الصفحة الواحدة.

**س: أين يمكنني العثور على المزيد من الأمثلة؟**  
ج: توثيق Aspose.Note الرسمي ومنتدى [support forum](https://forum.aspose.com/c/note/28) يحتويان على العديد من عينات الشيفرة.

## الخاتمة

لقد رأيت الآن كيفية **set paragraph style**، **add outline element**، وإنشاء ملف OneNote يمكن **export to PDF** باستخدام Aspose.Note for Java. يضمن إدراج النص المنسق في مرحلة الإنشاء أن يبدو المستند النهائي احترافيًا وأن أي عملية **convert OneNote PDF** لاحقة تحتفظ بالتنسيق. لا تتردد في توسيع هذا الأساس بإضافة صور، جداول، أو بيانات تعريف مخصصة لتلبية احتياجات مشروعك.

---

**آخر تحديث:** 2026-02-18  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (أحدث إصدار)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}