---
title: إضافة عقدة صورة جديدة مع علامة في OneNote - Aspose.Note
linktitle: إضافة عقدة صورة جديدة مع علامة في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرف على كيفية إضافة عقدة صورة جديدة بعلامة في OneNote باستخدام Aspose.Note لـ Java. ارفع مهاراتك في برمجة Java دون عناء.
weight: 10
url: /ar/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة عقدة صورة جديدة مع علامة في OneNote - Aspose.Note

## مقدمة
في عالم برمجة Java، يبرز Aspose.Note كأداة قوية للتعامل مع مستندات OneNote بسهولة. إذا كنت تتطلع إلى تحسين مهاراتك ومعرفة كيفية إضافة عقدة صورة جديدة بعلامة في OneNote باستخدام Aspose.Note، فقد وصلت إلى المكان الصحيح. سيرشدك هذا الدليل خطوة بخطوة خلال العملية، مما يضمن أنك تفهم كل مفهوم بدقة.
## المتطلبات الأساسية
قبل أن نتعمق في البرنامج التعليمي، دعونا نتأكد من أن لديك كل ما تحتاجه:
1.  Aspose.Note لـ Java: تأكد من تثبيت مكتبة Aspose.Note. إذا لم يكن الأمر كذلك، يمكنك تنزيله[هنا](https://releases.aspose.com/note/java/).
2. بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java عاملة على جهازك.
والآن بعد أن توفرت لدينا المتطلبات الأساسية، فلننتقل إلى الخطوات التالية.
## حزم الاستيراد
في مشروع Java الخاص بك، ابدأ باستيراد الحزم الضرورية:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## الخطوة 1: إنشاء كائن المستند
```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory";
// إنشاء كائن من فئة المستند
Document doc = new Document();
```
## الخطوة 2: تهيئة كائن فئة الصفحة
```java
// تهيئة كائن فئة الصفحة
Page page = new Page();
```
## الخطوة 3: تهيئة كائن فئة المخطط التفصيلي
```java
// تهيئة كائن فئة المخطط التفصيلي
Outline outline = new Outline();
```
## الخطوة 4: تهيئة كائن فئة OutlineElement
```java
// تهيئة كائن فئة OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## الخطوة 5: تحميل وإدراج الصورة
```java
// تحميل صورة
Image image = new Image(null, dataDir + "Input.jpg");
// إدراج صورة في عقدة الوثيقة
outlineElem.appendChildLast(image);
```
## الخطوة 6: إضافة علامة ملاحظة إلى الصورة
```java
// أضف علامة ملاحظة بنجمة صفراء إلى الصورة
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## الخطوة 7: إضافة عقدة عنصر المخطط التفصيلي
```java
// إضافة عقدة عنصر المخطط التفصيلي
outline.appendChildLast(outlineElem);
```
## الخطوة 8: إضافة عقدة المخطط التفصيلي
```java
// إضافة عقدة المخطط التفصيلي
page.appendChildLast(outline);
```
## الخطوة 9: إضافة عقدة الصفحة
```java
// إضافة عقدة الصفحة
doc.appendChildLast(page);
```
## الخطوة 10: حفظ مستند OneNote
```java
// حفظ مستند OneNote كملف PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
تهانينا! لقد نجحت في إضافة عقدة صورة جديدة بعلامة في OneNote باستخدام Aspose.Note لـ Java.
## خاتمة
 يفتح إتقان Aspose.Note لـ Java إمكانيات مثيرة في معالجة مستندات OneNote. باتباع هذا البرنامج التعليمي، اكتسبت مهارة عملية يمكن تطبيقها على مشاريع مختلفة. استمر في استكشاف وثائق Aspose.Note[هنا](https://reference.aspose.com/note/java/)لمزيد من الميزات والإمكانيات المتقدمة.
## الأسئلة الشائعة
### أين يمكنني العثور على وثائق Aspose.Note؟
 يمكنك العثور على الوثائق[هنا](https://reference.aspose.com/note/java/).
### كيف أقوم بتنزيل Aspose.Note لجافا؟
 يمكنك تنزيله من صفحة الإصدارات[هنا](https://releases.aspose.com/note/java/).
### هل هناك نسخة تجريبية مجانية متاحة؟
 نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).
### أين يمكنني الحصول على الدعم لـ Aspose.Note؟
 قم بزيارة منتدى المجتمع[هنا](https://forum.aspose.com/c/note/28) للدعم.
### هل أحتاج إلى ترخيص مؤقت؟
 إذا لزم الأمر، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
