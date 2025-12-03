---
date: 2025-12-03
description: تعلم كيفية تحويل OneNote إلى نص باستخدام Aspose.Note للغة Java. دليل
  خطوة بخطوة يغطي استخراج النص، استخراج الصور، وكيفية قراءة ملفات OneNote.
language: ar
linktitle: Convert OneNote to Text with Document Visitor – Java
second_title: Aspose.Note Java API
title: تحويل OneNote إلى نص باستخدام Document Visitor – Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل OneNote إلى نص باستخدام Document Visitor – Java

## المقدمة

في هذا الدرس ستتعلم **كيفية تحويل OneNote إلى نص** باستخدام Document Visitor الخاص بـ Aspose.Note for Java. سواءً كنت بحاجة إلى قراءة ملفات OneNote برمجياً، استخراج المحتوى النصي العادي، أو سحب الصور المدمجة، فإن Document Visitor يمنحك تحكمًا دقيقًا في كل عقدة داخل مستند .one.

## إجابات سريعة
- **ماذا يعني “convert OneNote to text”?** يعني استخراج التمثيل النصي العادي (وبشكل اختياري الصور) من ملف .one.  
- **أي مكتبة تساعد في ذلك؟** توفر Aspose.Note for Java واجهة برمجة التطبيقات `DocumentVisitor`.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتقييم؛ يلزم الحصول على ترخيص مدفوع للإنتاج.  
- **هل يمكنني أيضًا استخراج الصور؟** نعم – قم بتنفيذ طريقة `VisitImageStart` لسحب الصور.  
- **ما المتطلبات المسبقة؟** Java JDK 8+، ملف JAR الخاص بـ Aspose.Note for Java، وملف .one للمعالجة.

## ما هو “convert OneNote to text”؟
تحويل OneNote إلى نص يعني قراءة ملف OneNote (.one) برمجياً واسترجاع محتواه النصي والعناوين والعناصر الأخرى دون واجهة OneNote الأصلية. هذا مفيد لفهرسة البحث، إعداد التقارير، أو ترحيل المحتوى إلى منصات أخرى.

## لماذا نستخدم Document Visitor ل**كيفية قراءة ملفات OneNote**؟
يتبع Document Visitor نمط التصميم Visitor، مما يتيح لك التجول عبر كل عنصر (صفحات، مخططات، صور، نصوص منسقة، إلخ) في مستند OneNote. مقارنةً بتحميل المستند بالكامل في الذاكرة وتحليلها يدوياً، فإن نهج الزائر هو:

* **كفاءة الذاكرة** – يعالج العقد واحدةً تلو الأخرى.  
* **قابل للتوسيع** – يمكنك إضافة منطق مخصص لأي نوع من العقد (مثل استخراج الصور).  
* **دقة** – يحافظ على الهيكل الأصلي، مما يضمن عدم فقدان المحتوى المخفي.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

1. **Java Development Kit (JDK) 8 أو أحدث** مثبت.  
2. مكتبة **Aspose.Note for Java** تم تحميلها من الموقع الرسمي – [download here](https://releases.aspose.com/note/java/).  
3. **مستند OneNote** (`.one` file) الذي تريد تحويله إلى نص.  

## الخطوة 1: استيراد الحزم

أولاً، استورد الفئات التي ستحتاجها للعمل مع Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## الخطوة 2: إعداد فئة Document Visitor

أنشئ فئة تمتد من `DocumentVisitor`. سيجمع هذا الزائر المخصص النص، يحسب عدد العقد، و(إذا رغبت) يخزن الصور.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## الخطوة 3: تنفيذ طرق الزائر  

هنا نقوم بتنفيذ ردود النداء لأنواع العقد التي نهتم بها. تقوم الطرق بزيادة عداد العقد، ولـ `RichText`، تُضيف النص الفعلي إلى `StringBuilder` الخاص بنا. يمكنك أيضًا إضافة منطق **لاستخراج الصور من OneNote** عبر معالجة `VisitImageStart`.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Pro tip: you can save the image stream here if you need to extract images.
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

## الخطوة 4: طريقة main – تشغيل الزائر

طريقة `main` تقوم بتحميل ملف OneNote، تنشئ مثيلًا من الزائر المخصص الخاص بنا، وتبدأ التجوال. بعد الزيارة، نطبع النص المستخرج وإجمالي عدد العقد.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());
    System.out.println(myConverter.NodeCount());
}
```

## حالات الاستخدام الشائعة – **استخراج الصور من OneNote**

* **فهرسة البحث** – تحويل دفاتر OneNote إلى نص عادي لمحركات البحث النصية الكاملة.  
* **ترحيل المحتوى** – نقل الملاحظات إلى نظام إدارة محتوى (CMS) أو بوابة توثيق.  
* **تحليل البيانات** – استخراج النصوص والصور لمعالجة اللغة الطبيعية أو تحليل الصور.  

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **NullPointerException عند قراءة ملف .one** | تأكد من أن مسار الملف (`dataDir`) ينتهي بفاصل مسار (`/` أو `\\`) وأن الملف موجود. |
| **عدم استخراج الصور** | نفّذ منطقًا داخل `VisitImageStart` لكتابة `image.getImageData()` إلى ملف أو تدفق. |
| **الدفاتر الكبيرة تسبب استهلاكًا عاليًا للذاكرة** | عالج المستند صفحةً بصفحة أو استخدم واجهات برمجة التطبيقات المتدفقة إذا كانت متاحة. |

## الأسئلة المتكررة

**س: هل يمكنني استخراج أنواع محددة من المحتوى من مستند OneNote؟**  
ج: نعم، عبر تنفيذ فقط طرق الزائر التي تحتاجها (مثل `VisitRichTextStart` للنص، `VisitImageStart` للصور).

**س: هل Aspose.Note for Java متوافق مع إصدارات مختلفة من ملفات OneNote؟**  
ج: بالتأكيد. تدعم المكتبة ملفات .one التي تم إنشاؤها بواسطة إصدارات Microsoft OneNote الحديثة.

**س: هل يمكنني دمج عملية الاستخراج هذه في تطبيق Java الخاص بي؟**  
ج: نعم. الشيفرة المعروضة مثال مستقل يمكنك تضمينه مباشرةً في أي مشروع Java.

**س: هل يتعامل Aspose.Note for Java مع هياكل OneNote المعقدة؟**  
ج: نعم. نمط الزائر يتيح لك التنقل عبر المخططات المتداخلة، المجموعات، والكائنات المدمجة دون فقدان الهيكل.

**س: هل هناك حد لحجم مستند OneNote الذي يمكن معالجته؟**  
ج: رغم عدم وجود حد ثابت، قد تتطلب الدفاتر الضخمة جدًا مزيدًا من ذاكرة الـ heap؛ لذا يُفضَّل معالجتها بشكل تدريجي.

**س: كيف يمكنني استخراج الصور من OneNote؟**  
ج: نفّذ طريقة `VisitImageStart` للوصول إلى `image.getImageData()` وكتابة البايتات إلى ملف.

**آخر تحديث:** 2025-12-03  
**تم الاختبار مع:** Aspose.Note for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}