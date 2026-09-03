---
date: 2026-01-28
description: تعرّف على كيفية إنشاء مخطط في OneNote، وإضافة علامة إلى OneNote، وتوليد
  ملف PDF من OneNote باستخدام Aspose.Note للـ Java.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: إنشاء مخطط في OneNote وإضافة علامة – Aspose.Note
url: /ar/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء مخطط في OneNote وإضافة علامة – Aspose.Note

## مقدمة
هل تبحث عن **إنشاء مخطط في OneNote** وتعزيز التعاون باستخدام العلامات مع Java؟ تجعل Aspose.Note for Java من السهل إضافة العلامات، هيكلة ملاحظاتك، وحتى **إنشاء PDF من ملفات OneNote**. في هذا الدرس سنستعرض كل خطوة، نشرح *لماذا* كل جزء مهم، ونظهر لك كيفية إنتاج ملف PDF مصقول في النهاية.

## إجابات سريعة
- **ماذا يعني “إنشاء مخطط في OneNote”؟** إنه يبني هيكلًا هرميًا (مخططات) ينظم المحتوى مثل العناوين والأقسام الفرعية.  
- **أي مكتبة تضيف علامات إلى OneNote؟** توفر Aspose.Note for Java الفئة `NoteTag` للعلامات البصرية.  
- **هل يمكنني تصدير النتيجة إلى PDF؟** نعم – استخدم `SaveFormat.Pdf` **لإنشاء PDF من OneNote**.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يتوفر ترخيص مؤقت للاختبار؛ يلزم ترخيص كامل للاستخدام التجاري.  
- **ما هي المتطلبات الأساسية؟** تثبيت JDK، مكتبة Aspose.Note for Java، ومعرفة أساسية بـ Java.

## ما هو “إنشاء مخطط في OneNote”؟
إنشاء مخطط في OneNote يعني إضافة كائنات `Outline` و `OutlineElement` التي تُعرّف هيكلًا شجريًا لملاحظاتك. تسمح لك هذه الهرمية بطي وتوسيع وتنظيم المعلومات كما هو الحال مع العناوين في المستند.

## لماذا إضافة علامة إلى OneNote؟
تُعطي العلامات مثل النجوم، العلامات الصح، أو الأيقونات المخصصة للقراء إشارات بصرية، تحسن قابلية البحث، وتساعد الفرق على إعطاء الأولوية للعناصر. باستخدام Aspose.Note يمكنك إرفاق `NoteTag` برمجيًا إلى أي قطعة نصية.

## المتطلبات المسبقة
قبل البدء، تأكد من أنك تمتلك:
- مجموعة تطوير Java (JDK) مثبتة.
- مكتبة Aspose.Note for Java تم تنزيلها. يمكنك الحصول عليها [هنا](https://releases.aspose.com/note/java/).
- فهم أساسي لبرمجة Java.

## استيراد الحزم
تأكد من استيراد الحزم الضرورية لبدء مشروعك:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
دعنا نقسم الشيفرة أعلاه إلى دليل خطوة بخطوة.

## الخطوة 1: إعداد المستند والصفحة
ابدأ بإنشاء كائن `Document` جديد وتهيئة كائن `Page`:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```
هنا، نحدد المسار إلى دليل المستندات، ننشئ `Document` جديدًا، ونهيئ `Page`.

## الخطوة 2: إنشاء مخطط
بعد ذلك، أنشئ كائن `Outline` لتنسيق المحتوى الخاص بك:
```java
Outline outline = new Outline();
```
توفر المخططات هيكلًا هرميًا لمستندك، مما يجعل من السهل **إنشاء مخطط في OneNote** والحفاظ على تنظيم المعلومات.

## الخطوة 3: تهيئة OutlineElement و ParagraphStyle
الآن، قم بتهيئة `OutlineElement` وتعيين `ParagraphStyle` لتنسيق النص:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
`OutlineElement` يمثل عنصرًا داخل المخطط، و`ParagraphStyle` يحدد خصائص تنسيق النص.

## الخطوة 4: إضافة RichText مع NoteTag
أنشئ كائن `RichText`، أضف نص OneNote الخاص بك، وأضف `NoteTag`:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
`RichText` يتيح لك دمج نص منسق، و`NoteTag` **يضيف علامة إلى OneNote** كإشارة بصرية.

## الخطوة 5: بناء هيكل المخطط
أضف عقدة النص، عقدة عنصر المخطط، وعقدة المخطط لبناء هيكل المستند:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
تضمن هذه الخطوة تنظيم محتواك داخل المستند، مكملة عملية **إنشاء مخطط في OneNote**.

## الخطوة 6: حفظ المستند
احفظ المستند بصيغة PDF، والتي **تنشئ PDF من OneNote**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
الآن، تم حفظ مستند OneNote الخاص بك مع العلامات المضافة كملف PDF.

باتباع هذه الخطوات، يمكنك تحسين مستندات OneNote بسهولة باستخدام Aspose.Note for Java.

## الخاتمة
في هذا الدرس استكشفنا كيفية **إنشاء مخطط في OneNote**، إضافة علامة إلى OneNote، ثم **إنشاء PDF من OneNote** باستخدام Aspose.Note for Java. يمنحك استخدام Java تحكمًا كاملاً في هيكل الملاحظة، العلامات البصرية، وخيارات التصدير، مما يجعل ملاحظاتك أكثر تنظيمًا وقابلية للمشاركة.

## الأسئلة المتكررة
### 1. هل يمكنني استخدام Aspose.Note for Java مع لغات برمجة أخرى؟
يدعم Aspose.Note أساسًا Java، ولكن هناك إصدارات متاحة أيضًا لـ .NET.

### 2. هل Aspose.Note for Java مناسب للمبتدئين؟
نعم، يوفر Aspose.Note for Java وثائق شاملة ودعمًا، مما يجعله متاحًا للمبتدئين والمطورين ذوي الخبرة على حد سواء.

### 3. كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note for Java؟
يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### 4. أين يمكنني العثور على دعم إضافي؟
لأي استفسارات أو مساعدة، زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28).

### 5. هل هناك نسخة تجريبية مجانية متاحة؟
نعم، يمكنك تجربة نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

**أسئلة وإجابات إضافية**

**س: هل يمكنني تخصيص أيقونة العلامة؟**  
ج: نعم – يوفر Aspose.Note العديد من الأيقونات المحددة مسبقًا عبر `TagIcon` ويسمح أيضًا بصور مخصصة.

**س: كيف يمكنني تغيير إعدادات إخراج PDF؟**  
ج: استخدم `PdfSaveOptions` للتحكم في جودة الصورة، الضغط، والأمان قبل استدعاء `doc.save`.

**س: هل يمكن إضافة علامات متعددة إلى نفس النص؟**  
ج: بالتأكيد. استدعِ `text.getTags().add()` عدة مرات مع مثيلات `NoteTag` مختلفة.

---

**آخر تحديث:** 2026-01-28  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}