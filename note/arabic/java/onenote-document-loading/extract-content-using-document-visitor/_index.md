---
date: 2026-02-10
description: تعلم كيفية تحويل OneNote إلى نص واستخراج الصور باستخدام Aspose.Note للغة
  Java. يوضح الدليل كيفية قراءة ملف .one باستخدام Java وإجراء استخراج نص OneNote.
linktitle: Convert OneNote to Text and Extract Images using Document Visitor - Java
second_title: Aspose.Note Java API
title: تحويل OneNote إلى نص واستخراج الصور باستخدام Document Visitor - Java
url: /ar/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل OneNote إلى نص واستخراج الصور باستخدام Document Visitor - Java

## مقدمة

يسهل Aspose.Note for Java **تحويل OneNote إلى نص** بينما يقوم أيضًا **باستخراج الصور من دفاتر OneNote**. سنرشدك في هذا الدرس بمثال توضيحي يوضح كيفية تحميل ملف OneNote، واستعراض هيكله باستخدام `DocumentVisitor` المخصص، واستخراج كل الصور والنص العادي. في النهاية ستعرف أيضًا كيف **تقرأ ملف .one java** ولماذا هذا مثالي للهجرة برنامج للمحتوى أو إعداد التقارير.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.Note for Java (رابط التحميل أدناه).
- **هل يمكنني الحصول على الصور فقط؟** نعم – نفّذ طريقة `VisitImageStart` في `DocumentVisitor`.
- **كيف أقرأ ملف .one في Java؟** استخدم `new Document(path, new LoadOptions())`.
- **هل أحتاج إلى ترخيص للإنتاج؟** مطلوب ترخيص تجاري غير تجريبي.
- **ما نسخة Java المدعومة؟** JDK8أو أعلى.

## ما هو تحويل OneNote إلى نص؟

تحويل OneNote إلى نص يعني النسخة النصية الخام من دفتر `.one` حفظه كنص Unicode عادي. هذا مفيد عندما تحتاج إلى أرشيفات للبحث، تدفق بيانات جديدة، أو ملخصات بسيطة دون تنسيق OneNote الأصلي.

## لماذا نستخدم Document Visitor في Aspose.Note لاستخراج نص Onenote؟

- **تحكم دقيق:** نمط الزائر يتيح لك تحديد أي حفل بالضبط (الصفحات، اللقطات، الصور، الصورة الغني) تريد وحدها.
- **الأداء:** تجنب تحميل المستند بالكامل في الذاكرة ككتلة واحدة؛ كل عقدة تُزار عند الطلب.
- **المرونة:** يمكن في نهاية المطاف نفس الزائر لاستخراج الصور أو البيانات أو البيانات الوصفية المخصصة، مما يجعل حلاً شاملاً لكل من **تحويل onenote إلى نص** و **كيفية استخراج الصور**.

## المتطلبات الأساسية

قبل أن تبدأ، تأكد من أن لديك:

1. مجموعة تطوير Java (JDK)8 أو أحدث.
2. مكتبة Aspose.Note for Java تم تحميلها. يمكنك تنزيلها **[هنا](https://releases.aspose.com/note/Java/)**.
3. مستند OneNote (ملف .one) الذي تريد نسخ الصور منه أو تحويله إلى نص.

## استيراد الحزم

First, import the necessary classes from the Aspose.Note API.

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

## الخطوة 1: إعداد زائر مستند مخصص

أنشئ فئةً ترث من `DocumentVisitor`. سيتم استدعاء هذه الفئة لكل عقدة في مستند OneNote، مما يسمح لك باستخراج صور OneNote، وجمع النصوص اختياريًا.

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

## الخطوة 2: تنفيذ دوال الزائر

أضف تعديلات لأنواع العقد التي تهمك. فيما يلي، نتعامل مع النصوص المنسقة، والصور، والعناوين، والصفحات، والمخططات التفصيلية، وعناصر المخطط التفصيلي. يتم استخراج الصور من خلال دالة `VisitImageStart`.

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
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
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

### لماذا تطبيق هذه الأساليب؟

- **استخراج الصور من OneNote:** `VisitImageStart` يتيح لك الوصول المباشر إلى بايتات الصورة الخام.
- **تحويل OneNote إلى نص:** `VisitRichTextStart` يجمع المحتوى النصي، مما يتيح عملية **تحويل OneNote إلى نص** بسيط.
- **قراءة ملف .one في Java:** نمط الزائر (نمط الزائر) إي الملخصات بنية ملف داخلي `.one`، لذا لا تحتاج إلى تحليل الصيغة الثنائية DIY.

## الخطوة 3: قم بتشغيل الزائر من طريقتك الرئيسية

قم بتحميل الملف ".one"، وقم بإنشاء مثيل للزائر، وابدأ عملية الاجتياز.

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
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## حالات الاستخدام الشائعة

- **إعداد تقارير واقعية:** سحب الصور والنص من دفتر ملاحظات OneNote للاجتماعات لإنشاء ملخص بتنسيق PDF أو HTML.
- **ترحيل المحتوى:** تحويل أرشيف OneNote القديم إلى ملفات نصية للفهرسة أو استيعاب محركات البحث.
- **استخراج الأصول الرقمية:** جمع لقطات الشاشة المدمجة أو اللقطات أو الصور التي يمكن استخدامها في تطبيقات أخرى.

## استكشاف الأخطاء وإصلاحها ونصائح

- **دفاتر ملاحظات كبيرة:** إذا واجهت مشكلات في الذاكرة، تناولت الصفحات بشكل فردي عن طريق فحص `VisitPageStart` وتحميل المسائل المستوى الصفحي فقط عند الحاجة.
- **تنسيقات الصور:** كائن `Image` يُعيد بايتات خام؛ قد تحتاج إلى الابتكار (PNG, JPEG) قبل الحفظ.
- **أخطاء قضائية:** تأكد من ضبط ترخيص Aspose (`License License = new License(); License.setLicense("Aspose.Note.Java.lic");`) قبل تحميل السوق في عالم الإنتاج.
- **كيفية النسخ الصور الجديدة:** صَفِّ عقد داخل `VisitImageStart` حسب الحجم أو مطلوب إذا كنت تحتاج فقط إلى أنواع خاصة من الصور.

## الأسئلة المتداولة

**س: هل يمكنني استخراج أنواع محددة من المحتوى من مستند OneNote؟**  
ج: نعم – عن طريق تجاوز فقط طرق الزائر التي تحتاجها (مثل `VisitImageStart` للصور، `VisitRichTextStart` للنص).

**س: هل Aspose.Note for Java متوافق مع إصدارات مختلفة من مستندات OneNote؟**  
ج: بالتأكيد. المكتبة تدعم جميع إصدارات ملفات OneNote الرئيسية، لذا يمكنك بأمان **read .one file java** بغض النظر عن نسخة OneNote الأصلية.

**س: هل يمكنني دمج عملية الاستخراج هذه في تطبيق Java الخاص بي؟**  
ج: نعم. نمط الزائر يعمل بسلاسة داخل أي قاعدة شفرة Java؛ فقط أضف ملف JAR الخاص بالمكتبة واستدعِ المثال الموضح أعلاه.

**س: هل توفر Aspose.Note for Java دعمًا لمعالجة مستندات OneNote المعقدة؟**  
ج: نعم. المخططات المتداخلة، الوسائط المدمجة، والبيانات المخصصة كلها متاحة عبر واجهة برمجة تطبيقات الزائر.

**س: هل هناك أي حد لحجم مستند OneNote الذي يمكن معالجته؟**  
ج: لا يوجد حد ثابت، لكن دفاتر الملاحظات الكبيرة جدًا قد تتطلب المزيد من ذاكرة الـ heap؛ فكر في معالجتها صفحة بصفحة.

**س: كيف أحول النص المستخرج إلى ملف نصي عادي؟**  
ج: بعد أن تُعيد `myConverter.GetText()` قيمة `String`، اكتبها إلى ملف باستخدام I/O القياسي في Java (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---
**Last Updated:** 2026-02-10  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}