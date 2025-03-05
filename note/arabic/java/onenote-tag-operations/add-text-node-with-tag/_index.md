---
title: إضافة عقدة نصية مع علامة في OneNote - Aspose.Note
linktitle: إضافة عقدة نصية مع علامة في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: اكتشف كيفية إضافة عقد نصية ذات علامات في OneNote باستخدام Aspose.Note لـ Java. سهلة وفعالة وصديقة للمطورين. قم بتنزيل المكتبة الآن!
type: docs
weight: 13
url: /ar/java/onenote-tag-operations/add-text-node-with-tag/
---
## مقدمة
في هذا البرنامج التعليمي، سنستكشف كيفية إضافة عقدة نصية بعلامة في OneNote باستخدام Aspose.Note لـ Java. Aspose.Note هي مكتبة Java قوية تتيح للمطورين العمل مع ملفات Microsoft OneNote برمجياً. تعد إضافة العقد النصية مع العلامات مطلبًا شائعًا في معالجة المستندات، ويعمل Aspose.Note على تبسيط هذه المهمة.
## المتطلبات الأساسية
قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:
- المعرفة الأساسية ببرمجة جافا.
-  تم تثبيت Aspose.Note لمكتبة Java. يمكنك تنزيله[هنا](https://releases.aspose.com/note/java/).
- بيئة تطوير متكاملة (IDE) تم إعدادها لتطوير Java.
## حزم الاستيراد
ابدأ باستيراد الحزم اللازمة لمشروع Java الخاص بك. في التعليمات البرمجية الخاصة بك، قم بتضمين الواردات التالية:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## الخطوة 1: إنشاء كائن المستند
تهيئة كائن فئة المستند لتمثيل مستند OneNote:
```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory";
//قم بإنشاء كائن من فئة المستند
Document doc = new Document();
```
## الخطوة 2: تهيئة كائن فئة الصفحة
قم بتهيئة كائن فئة الصفحة لتمثيل الصفحة داخل المستند:
```java
// تهيئة كائن فئة الصفحة
Page page = new Page();
```
## الخطوة 3: تهيئة كائن فئة المخطط التفصيلي
قم بتهيئة كائن فئة المخطط التفصيلي لتنظيم المحتوى داخل الصفحة:
```java
// تهيئة كائن فئة المخطط التفصيلي
Outline outline = new Outline();
```
## الخطوة 4: تهيئة كائن فئة OutlineElement
تهيئة كائن فئة OutlineElement لتمثيل عنصر داخل المخطط التفصيلي:
```java
// تهيئة كائن فئة OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## الخطوة 5: تخصيص نمط النص
قم بإعداد نمط عقدة النص، مثل لون الخط والاسم والحجم:
```java
// تخصيص نمط النص
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## الخطوة 6: إنشاء كائن RichText
قم بإنشاء كائن RichText وألحق النص المطلوب به:
```java
// إنشاء كائن RichText
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## الخطوة 7: إضافة علامة الملاحظة
أضف علامة ملاحظة، مثل النجمة الصفراء، إلى النص:
```java
// إضافة علامة ملاحظة
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## الخطوة 8: إضافة عقدة نصية
أضف عقدة النص إلى عنصر المخطط التفصيلي:
```java
// إضافة عقدة نصية
outlineElem.appendChildLast(text);
```
## الخطوة 9: إضافة عنصر المخطط التفصيلي إلى المخطط التفصيلي
أضف عنصر المخطط التفصيلي إلى المخطط التفصيلي:
```java
// إضافة عقدة عنصر المخطط التفصيلي
outline.appendChildLast(outlineElem);
```
## الخطوة 10: إضافة مخطط تفصيلي إلى الصفحة
أضف المخطط التفصيلي إلى الصفحة:
```java
// إضافة عقدة المخطط التفصيلي
page.appendChildLast(outline);
```
## الخطوة 11: إضافة صفحة إلى المستند
إضافة الصفحة إلى المستند:
```java
// إضافة عقدة الصفحة
doc.appendChildLast(page);
```
## الخطوة 12: حفظ مستند OneNote
احفظ مستند OneNote في الدليل المحدد:
```java
// حفظ مستند OneNote
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
تهانينا! لقد نجحت في إضافة عقدة نصية بعلامة في OneNote باستخدام Aspose.Note لـ Java.
## خاتمة
في هذا البرنامج التعليمي، قمنا بتغطية العملية خطوة بخطوة لإضافة عقدة نصية بعلامة في OneNote باستخدام مكتبة Aspose.Note for Java. تعمل هذه المكتبة القوية على تبسيط مهام معالجة المستندات، مما يسهل على المطورين التعامل مع ملفات OneNote برمجيًا.
## أسئلة مكررة
### س: هل يمكنني استخدام Aspose.Note لـ Java مع مكتبات Java الأخرى؟
ج: نعم، يمكن دمج Aspose.Note for Java بسلاسة مع مكتبات Java الأخرى لتحسين قدرات معالجة المستندات.
### س: هل تتوفر نسخة تجريبية مجانية من Aspose.Note لـ Java؟
 ج: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).
### س: كيف يمكنني الحصول على دعم Aspose.Note لـ Java؟
ج: يمكنك طلب الدعم من مجتمع Aspose.Note[المنتدى](https://forum.aspose.com/c/note/28).
### س: هل التراخيص المؤقتة متاحة لـ Aspose.Note لـ Java؟
 ج: نعم، يمكنك الحصول على تراخيص مؤقتة[هنا](https://purchase.aspose.com/temporary-license/).
### س: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.Note لـ Java؟
 ج: الوثائق متاحة[هنا](https://reference.aspose.com/note/java/).