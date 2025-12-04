---
date: 2025-12-04
description: تعلم كيفية استخراج الصور من ملفات OneNote وتحويل OneNote إلى نص في Java
  باستخدام Aspose.Note. دليل خطوة بخطوة مع أمثلة على الشيفرة.
language: ar
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: استخراج الصور من OneNote باستخدام Document Visitor - Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استخراج الصور من OneNote باستخدام Document Visitor - Java

## Introduction

Aspose.Note for Java يجعل من السهل **استخراج الصور من OneNote** دفاتر الملاحظات وكذلك قراءة ملف `.one` الأساسي في Java. في هذا الدرس سنرشدك عبر مثال عملي كامل يوضح كيفية تحميل ملف OneNote، استعراض هيكله باستخدام `DocumentVisitor` مخصص، واستخراج كل من الصور والنص العادي. في النهاية ستعرف أيضًا كيفية **تحويل OneNote إلى نص** إذا كنت تحتاج فقط إلى المحتوى النصي.

## Quick Answers
- **ما المكتبة التي أحتاجها؟** Aspose.Note for Java (رابط التحميل أدناه).  
- **هل يمكن استخراج الصور فقط؟** نعم – نفّذ طريقة `VisitImageStart` في `DocumentVisitor`.  
- **كيف أقرأ ملف .one في Java؟** استخدم `new Document(path, new LoadOptions())`.  
- **هل أحتاج إلى ترخيص للإنتاج؟** الترخيص التجاري مطلوب للاستخدام غير التجريبي.  
- **ما إصدار Java المدعوم؟** JDK 8 أو أعلى.

## Prerequisites

قبل أن تبدأ، تأكد من وجود ما يلي:

1. Java Development Kit (JDK) 8 أو أحدث مثبت.  
2. مكتبة Aspose.Note for Java تم تحميلها. يمكنك تحميلها **[هنا](https://releases.aspose.com/note/java/)**.  
3. مستند OneNote (`.one` file) تريد استخراج الصور منه أو تحويله إلى نص.

## Import Packages

أولاً، استورد الفئات الضرورية من Aspose.Note API.

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

## Step 1: Set Up a Custom Document Visitor

أنشئ فئة تمتد من `DocumentVisitor`. سيتم استدعاء هذه الفئة لكل عقدة في مستند OneNote، مما يتيح لك **استخراج الصور من OneNote** وجمع النص اختياريًا.

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

## Step 2: Implement Visitor Methods

أضف عمليات تجاوز (overrides) لأنواع العقد التي تهتم بها. أدناه نتعامل مع النص الغني، الصور، العناوين، الصفحات، المخططات، وعناصر المخطط. طريقة `VisitImageStart` هي المكان الذي يحدث فيه استخراج الصورة.

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

### Why implement these methods?

- **استخراج الصور من OneNote:** `VisitImageStart` يمنحك وصولًا مباشرًا إلى بايتات الصورة الخام.  
- **تحويل OneNote إلى نص:** `VisitRichTextStart` يجمع المحتوى النصي، مما يتيح عملية **تحويل OneNote إلى نص** بسيطة.  
- **قراءة ملف .one في Java:** نمط الزائر (visitor) يج abstracts بنية ملف `.one` الأساسية، لذا لا تحتاج إلى تحليل الصيغة الثنائية بنفسك.

## Step 3: Run the Visitor from Your Main Method

حمّل ملف `.one`، أنشئ الزائر الخاص بك، وابدأ عملية الاستعراض.

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

## Common Use Cases

- **تقارير آلية:** استخراج الصور والنص من دفتر ملاحظات اجتماع OneNote لتوليد ملخص PDF أو HTML.  
- **ترحيل المحتوى:** تحويل أرشيفات OneNote القديمة إلى ملفات نصية عادية للفهرسة أو استيعاب محركات البحث.  
- **استخراج الأصول الرقمية:** جمع لقطات الشاشة المدمجة، المخططات، أو الصور لإعادة استخدامها في تطبيقات أخرى.

## Troubleshooting & Tips

- **دفاتر ملاحظات كبيرة:** إذا واجهت مشاكل في الذاكرة، عالج الصفحات بشكل فردي عبر فحص `VisitPageStart` وتحميل موارد الصفحة فقط عند الحاجة.  
- **تنسيقات الصور:** كائن `Image` يُعيد بايتات خام؛ قد تحتاج إلى اكتشاف التنسيق (PNG, JPEG) قبل الحفظ.  
- **أخطاء الترخيص:** تأكد من ضبط ترخيص Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) قبل تحميل المستند في بيئة الإنتاج.

## Frequently Asked Questions

**س: هل يمكن استخراج أنواع محددة من المحتوى من مستند OneNote؟**  
ج: نعم – عبر تجاوز فقط طرق الزائر التي تحتاجها (مثل `VisitImageStart` للصور، `VisitRichTextStart` للنص).

**س: هل Aspose.Note for Java متوافق مع إصدارات مختلفة من مستندات OneNote؟**  
ج: بالتأكيد. المكتبة تدعم جميع إصدارات ملفات OneNote الرئيسية، لذا يمكنك بأمان **قراءة ملف .one في Java** بغض النظر عن إصدار OneNote الأصلي.

**س: هل يمكن دمج عملية الاستخراج هذه في تطبيق Java الخاص بي؟**  
ج: نعم. نمط الزائر يعمل بسلاسة داخل أي قاعدة شفرة Java؛ فقط أضف ملف JAR الخاص بالمكتبة واستدعِ المثال المعروض أعلاه.

**س: هل توفر Aspose.Note for Java دعمًا للتعامل مع مستندات OneNote المعقدة؟**  
ج: نعم. المخططات المتداخلة، الوسائط المدمجة، والبيانات المخصصة كلها متاحة عبر API الزائر.

**س: هل هناك حد لحجم مستند OneNote الذي يمكن معالجته؟**  
ج: لا يوجد حد صريح، لكن دفاتر الملاحظات الضخمة قد تتطلب مزيدًا من ذاكرة الـ heap؛ فكر في معالجتها صفحة بصفحة.

**س: كيف أحول النص المستخرج إلى ملف نصي عادي؟**  
ج: بعد أن تُعيد `myConverter.GetText()` سلسلة `String`، اكتبها إلى ملف باستخدام I/O القياسي في Java (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}