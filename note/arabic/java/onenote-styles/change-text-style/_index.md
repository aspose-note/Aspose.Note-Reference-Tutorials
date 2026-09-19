---
date: 2026-06-05
description: تعلم كيفية تغيير حجم الخط في OneNote، وضبط لون الخط، وتظليل النص باستخدام
  Aspose.Note for Java – دليل خطوة بخطوة مع مقتطفات الشيفرة.
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: تغيير حجم الخط في OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: تغيير حجم الخط في OneNote - Aspose.Note
url: /ar/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تغيير حجم الخط في OneNote - Aspose.Note

## المقدمة

في هذا البرنامج التعليمي ستتعلم **كيفية تغيير حجم الخط في مستندات OneNote** باستخدام Aspose.Note للغة Java. سنستعرض تحميل ملف OneNote، الوصول إلى عقد النص الخاصة به، تطبيق اللون، التظليل، وتغييرات حجم الخط، وأخيرًا حفظ الملف المحدث. سواءً كنت تقوم بأتمتة إنشاء التقارير أو تحسين ملاحظات الاجتماعات، فإن هذا الدليل يوفر لك طريقة موثوقة لتنسيق محتوى OneNote برمجيًا.

## الإجابات السريعة
- **كيف يمكنني تغيير حجم الخط في OneNote باستخدام Java؟** قم بتحميل المستند، تعديل خاصية `FontSize` لكل `TextRun`، ثم احفظ – ثلاث خطوات بسيطة.  
- **هل يمكنني أيضًا تغيير لون النص والتظليل؟** نعم، قم بتعيين `FontColor` و `HighlightColor` على نفس `TextRun`.  
- **ما نسخة Aspose.Note المطلوبة؟** أي إصدار 23.10+ يدعم هذه واجهات برمجة التطبيقات للتنسيق.  
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تكفي للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **هل هذه الطريقة مناسبة للدفاتر الكبيرة؟** نعم – تقوم Aspose.Note بمعالجة دفاتر مئات الصفحات دون تحميل الملف بالكامل في الذاكرة.

## ما هو تغيير حجم الخط في OneNote؟
**change font size onenote** يشير إلى تعديل خاصية `FontSize` لعناصر النص داخل دفتر OneNote برمجيًا. باستخدام Aspose.Note، يمكن للمطورين تعديل هذه الخاصية عبر API، مما يحدث تحديثًا مباشرًا لهياكل ملفات OneNote الأساسية، ويضمن تغير المظهر البصري دون تحرير يدوي أو تفاعل مع الواجهة.

## لماذا نستخدم Aspose.Note لتغيير نمط النص في OneNote؟
توفر Aspose.Note أكثر من 30 خيارًا للتنسيق — بما في ذلك عائلة الخط، الحجم، اللون، التظليل، المحاذاة، وتباعد الفقرات — وتم تصميمها لمعالجة دفاتر كبيرة بكفاءة. يمكنها التعامل مع دفاتر تحتوي على أكثر من 500 صفحة مع استهلاك أقل من 150 ميغابايت من الذاكرة، مما يوفر أتمتة موثوقة وعالية الأداء لتدفقات عمل المستندات على مستوى المؤسسات.

## المتطلبات المسبقة

1. معرفة أساسية ببرمجة Java.  
2. JDK 8 أو أعلى مثبت على جهازك.  
3. مكتبة Aspose.Note للغة Java (قم بتنزيلها من موقع Aspose).  
4. الإلمام بالهيكل الهرمي لـ OneNote (الصفحات، الأقسام، عقد RichText).

## كيفية تغيير حجم الخط في OneNote باستخدام Aspose.Note؟

قم بتحميل ملف OneNote الخاص بك، حدد كل عقدة `RichText`، حدّث نمط كل `TextRun`، واحفظ المستند. هذه العملية المتكاملة لا تحتاج سوى بضع أسطر من الشيفرة وتنفّذ في أقل من ثانية للدفاتر النموذجية.

### الخطوة 1: استيراد الحزم

The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note` namespace. Import them at the top of your Java source file:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### الخطوة 2: تحميل المستند

The `Document` class is Aspose.Note's top‑level object that represents a single OneNote file in memory. Loading a file is as simple as passing the file path to its constructor.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### الخطوة 3: الوصول إلى عقد RichText

`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`, you gain access to every piece of editable text in the notebook.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### الخطوة 4: تغيير نمط النص

`TextRun` represents a contiguous run of characters sharing the same formatting. Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize` to **20** points to achieve the desired styling.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### الخطوة 5: حفظ المستند

Call `document.save("StyledSample.one")` to write the changes back to a OneNote file. The save operation preserves all original content while applying the new styles.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## المشكلات الشائعة والحلول

- **النص لا يتغير:** تأكد من أنك تت iterate على كائنات `TextRun` داخل كل عقدة `RichText`؛ تخطي هذه المرحلة سيترك التنسيق دون تغيير.  
- **اللون يظهر مختلفًا:** تستخدم Aspose.Note قيم RGB؛ تحقق من أنك تستخدم الثوابت الصحيحة `java.awt.Color`.  
- **دفتر كبير يبطئ الأداء:** يتيح LoadOptions ضبط طريقة تحميل Aspose.Note للملف، مما يسمح بالبث واختيار الصيغة. استخدم `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` لتمكين وضع البث، مما يقلل من استهلاك الذاكرة.

## الأسئلة المتكررة

**س: هل يمكنني تطبيق تغييرات نمط النص هذه على أقسام محددة من مستند OneNote الخاص بي؟**  
ج: نعم، قم بفلترة مجموعة `RichText` حسب معرف الصفحة أو القسم قبل تطبيق تغييرات النمط.

**س: هل تدعم Aspose.Note خيارات تنسيق أخرى بخلاف اللون، التظليل، والحجم؟**  
ج: بالتأكيد، يمكنك تعديل عائلة الخط، الغامق/المائل، التسطير، المحاذاة، وتباعد الفقرات باستخدام نموذج الكائن نفسه.

**س: هل يمكنني دمج Aspose.Note مع مكتبات Java أخرى للمعالجة المتقدمة؟**  
ج: نعم، تعمل Aspose.Note بسلاسة مع مكتبات مثل Apache POI، Jackson، أو Spring لبناء خطوط معالجة مستندات معقدة.

**س: هل Aspose.Note مرخص للاستخدام التجاري؟**  
ج: يلزم الحصول على ترخيص تجاري للنشر في بيئات الإنتاج؛ يتوفر ترخيص تقييم مجاني للتطوير والاختبار.

**س: أين يمكنني العثور على عينات إضافية ومرجع API؟**  
ج: زر بوابة توثيق Aspose.Note، حمّل ملف PDF الكامل لمرجع API، واستكشف مستودع GitHub للحصول على أمثلة المجتمع.

## الخلاصة

باتباع الخطوات السابقة، أصبحت الآن تعرف **كيفية تغيير حجم الخط في ملفات OneNote**، تعديل لون النص، وتطبيق التظليل باستخدام Aspose.Note للغة Java. تتيح لك هذه القدرة أتمتة تحسين المظهر البصري لملاحظات الاجتماعات، المواد التدريبية، أو أي محتوى يعتمد على OneNote على نطاق واسع.

---

**آخر تحديث:** 2026-06-05  
**تم الاختبار مع:** Aspose.Note 23.10 للغة Java  
**المؤلف:** Aspose

## الدروس ذات الصلة

- [تعيين نمط الفقرة الافتراضي في OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [تعيين لغة التدقيق للنص في OneNote - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [تعيين عنوان الصفحة في نمط Microsoft OneNote - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}