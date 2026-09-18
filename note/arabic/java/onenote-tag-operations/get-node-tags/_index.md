---
date: 2026-02-28
description: تعلم كيفية استخراج العلامات من ملفات OneNote باستخدام Aspose.Note للغة
  Java. يوضح هذا البرنامج التعليمي كيفية تحميل ملف OneNote، والحصول على علامات OneNote،
  وتعديل علامات OneNote بفعالية.
linktitle: How to Extract Tags from OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: كيفية استخراج العلامات من OneNote باستخدام Aspose.Note
url: /ar/java/onenote-tag-operations/get-node-tags/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استخراج العلامات من OneNote باستخدام Aspose.Note

## المقدمة
إذا كنت تحتاج إلى **كيفية استخراج العلامات** من مستند OneNote، فقد وجدت المكان المناسب. في هذا الدليل سنستعرض العملية الكاملة لتحميل ملف OneNote، الحصول على علامات OneNote، وحتى تعديل تلك العلامات باستخدام Aspose.Note للـ Java. بنهاية الشرح ستكون قادرًا على دمج استخراج العلامات في أي تطبيق Java بثقة.

## إجابات سريعة
- **ما هو الصنف الأساسي لفتح ملف OneNote؟** `Document`
- **أي طريقة تُرجع جميع عقد RichText؟** `doc.getChildNodes(RichText.class)`
- **هل يمكنك قراءة وقت إنشاء NoteTag؟** نعم، عبر `noteTag.getCreationTime()`
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** نعم، يلزم وجود ترخيص Aspose.Note صالح
- **هل الـ API متوافق مع Java 8 وما بعده؟** بالتأكيد، يدعم إصدارات Java الحديثة

## ما هو “كيفية استخراج العلامات” في OneNote؟
استخراج العلامات يعني قراءة البيانات الوصفية (مثل الحالة، التسمية، الأيقونة، والطوابع الزمنية) التي يضيفها OneNote إلى الفقرات، مربعات الاختيار، أو عناصر المحتوى الأخرى. تُخزن هذه العلامات ككائنات `NoteTag` داخل عقد `RichText`.

## لماذا نستخدم Aspose.Note لاستخراج العلامات؟
- **لا حاجة لتثبيت OneNote** – العمل مباشرةً مع ملفات .one.
- **تحكم كامل** – استرجاع، قراءة، وتعديل خصائص العلامات برمجيًا.
- **متعدد المنصات** – يعمل على أي نظام تشغيل يدعم Java.

## المتطلبات المسبقة
- بيئة تطوير Java (JDK 8+).
- مكتبة Aspose.Note تم تحميلها من [هنا](https://releases.aspose.com/note/java/).
- مستند OneNote تجريبي (مثال: `Sample1.one`) موجود في دليل معروف.

## استيراد الحزم
ابدأ باستيراد الفئات التي ستحتاجها. هذه الاستيرادات تمنحك الوصول إلى معالجة المستندات، واجهات العلامات، وعقد النص الغني.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTag;
import com.aspose.note.RichText;
```

## كيفية تحميل ملف OneNote
الخطوة الأولى هي تحميل ملف OneNote إلى كائن `Document`.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
```

> **نصيحة احترافية:** احرص على أن يكون مسار `dataDir` مطلقًا أو استخدم `Paths.get(...)` لتجنب الأخطاء المتعلقة بالمسارات.

## كيفية الحصول على علامات OneNote
بعد تحميل المستند، استرجع جميع عقد `RichText`. قد يحتوي كل عقدة على علامة أو أكثر.

```java
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
```

## التكرار عبر كل عقدة
قم بالتكرار عبر كل عقدة `RichText` لفحص علاماتها.

```java
// Iterate through each node
for (RichText richText : nodes) {
    // Process each node here
}
```

## استرجاع علامات NoteTag (كيفية تعديل علامات OneNote)
داخل الحلقة، تحقق مما إذا كانت العلامة هي `NoteTag`. إذا كانت كذلك، يمكنك قراءة خصائصها — أو تعديلها إذا لزم الأمر.

```java
for (ITag tag : richText.getTags()) {
    if (tag.getClass() == NoteTag.class) {
        NoteTag noteTag = (NoteTag) tag;
        // Retrieve properties
        System.out.println("Completed Time: " + noteTag.getCompletedTime());
        System.out.println("Create Time: " + noteTag.getCreationTime());
        System.out.println("Font Color: " + noteTag.getFontColor());
        System.out.println("Status: " + noteTag.getStatus());
        System.out.println("Label: " + noteTag.getLabel());
        System.out.println("Icon: " + noteTag.getIcon());
        System.out.println("High Light: " + noteTag.getHighlight());
        // Example of modifying a property
        // noteTag.setLabel("Updated Label");
    }
}
```

> **تحذير:** تعديل علامة يغيّر المستند الأساسي. تذكر حفظ المستند بعد إجراء التغييرات.

## الخلاصة
أنت الآن تعرف **كيفية استخراج العلامات**، وكيفية **تحميل ملف OneNote**، وكيفية **الحصول على علامات OneNote**، وحتى **تعديل علامات OneNote** باستخدام Aspose.Note للـ Java. دمج هذه المقاطع في مشاريعك الخاصة لأتمتة تحليل الملاحظات، وإعداد التقارير، أو مهام النقل.

## الأسئلة المتكررة
### هل Aspose.Note متوافق مع جميع إصدارات OneNote؟
Aspose.Note يدعم صيغ ملفات OneNote المختلفة، مما يضمن التوافق عبر الإصدارات المتعددة.

### هل يمكنني تعديل خصائص NoteTag المسترجعة؟
نعم، Aspose.Note يسمح لك بتعديل وتحديث خصائص NoteTag برمجيًا.

### هل هناك نسخة تجريبية متاحة لـ Aspose.Note؟
بالطبع! يمكنك الوصول إلى النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

### أين يمكنني العثور على وثائق شاملة لـ Aspose.Note للـ Java؟
استكشف الوثائق التفصيلية [هنا](https://reference.aspose.com/note/java/).

### كيف يمكنني الحصول على دعم لأي مشكلات أو استفسارات؟
توجه إلى منتدى الدعم [هنا](https://forum.aspose.com/c/note/28) للحصول على مساعدة من مجتمع Aspose.

## أسئلة شائعة
**س:** *هل يمكنني استخراج العلامات من ملفات OneNote المحمية بكلمة مرور؟*  
**ج:** نعم، قدم كلمة المرور عند إنشاء كائن `Document`.

**س:** *هل أحتاج إلى استدعاء طريقة حفظ بعد تعديل العلامات؟*  
**ج:** بالتأكيد. استخدم `doc.save("UpdatedSample.one");` لحفظ التغييرات.

**س:** *هل يمكن تصفية العلامات حسب الحالة؟*  
**ج:** يمكنك فحص `noteTag.getStatus()` داخل الحلقة ومعالجة الحالات المطلوبة فقط.

**س:** *ماذا يحدث إذا لم تحتوي عقدة RichText على أي علامات؟*  
**ج:** `richText.getTags()` تُعيد مجموعة فارغة؛ الحلقة تتخطاها ببساطة.

**س:** *هل يمكنني معالجة عدة ملفات OneNote دفعة واحدة؟*  
**ج:** غلف المنطق أعلاه في روتين تكرار للملفات وتعامل مع كل مستند على حدة.

---

**آخر تحديث:** 2026-02-28  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}