---
date: 2026-05-31
description: تعلم كيفية تعديل سجل صفحات OneNote، تغيير عنوان صفحة OneNote، وحذف سجل
  الصفحات باستخدام Aspose.Note للغة Java.
keywords:
- modify onenote page history
- change onenote page title
- Aspose.Note Java
linktitle: تعديل سجل الصفحات في OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-05-31'
  description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  headline: How to modify onenote page history with Aspose.Note
  type: TechArticle
- description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  name: How to modify onenote page history with Aspose.Note
  steps:
  - name: Load the OneNote Document
    text: '`Document` loads a OneNote file into memory and provides access to its
      pages and history.'
  - name: Retrieve the First Page and Its History
    text: '`PageHistory` is the Aspose.Note class that stores a notebook’s revision
      list. It offers methods to query, add, or remove historic pages.'
  - name: Delete a Range of History Items
    text: '`removeRange(int start, int count)` removes a consecutive block of history
      entries starting at the specified index.'
  - name: Replace a History Item
    text: '`set_Item(int index, Page page)` replaces the history entry at the given
      position with a new `Page` object.'
  - name: Change the Title of a History Page
    text: '`setTitle(String title)` updates the title of a historic `Page` instance.'
  - name: Add a New History Entry
    text: '`addItem(Page page)` appends a new page to the end of the history collection.'
  - name: Insert a Page at a Specific Position
    text: '`insertItem(int index, Page page)` inserts a page at the specified index,
      shifting subsequent items forward.'
  - name: Save the Modified Notebook
    text: '`save(String path)` writes the updated notebook to the given file location.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Note for Java integrates seamlessly with Spring, Hibernate,
      Android, and other Java ecosystems.
    question: Can I use Aspose.Note for Java with other Java frameworks?
  - answer: Absolutely—Aspose.Note supports both legacy OneNote 2007 files and the
      modern OneNote 2016/Online formats.
    question: Is Aspose.Note for Java compatible with different versions of OneNote
      files?
  - answer: No, the library is self‑contained; you only need the core JAR and a Java
      runtime.
    question: Does Aspose.Note for Java require any additional dependencies?
  - answer: Yes, you can loop through a directory of `.one` files and apply the same
      history‑editing logic to each notebook.
    question: Can I perform bulk modifications on multiple OneNote files simultaneously?
  - answer: Yes, you can visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28)
      for assistance and to share examples.
    question: Is there a community forum for Aspose.Note for Java where I can ask
      for help?
  type: FAQPage
second_title: Aspose.Note Java API
title: كيفية تعديل سجل صفحات OneNote باستخدام Aspose.Note
url: /ar/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعديل سجل صفحات OneNote باستخدام Aspose.Note

في هذا الدرس ستتعلم **كيفية تعديل سجل صفحات OneNote** خطوة بخطوة باستخدام Aspose.Note for Java API. سواء كنت بحاجة إلى حذف إصدارات قديمة، أو إعادة تسمية صفحة تاريخية، أو إدراج إدخال جديد، فإن الدليل يوضح لك سير عمل جاهز للإنتاج يعمل مع أي دفتر ملاحظات OneNote.

## إجابات سريعة
- **ما معنى “سجل الصفحة” في OneNote؟**  
  إنه مجموعة الإصدارات السابقة للصفحة المخزنة داخل ملف OneNote.
- **هل يمكنني حذف إدخال تاريخ محدد؟**  
  نعم، استخدم طريقتي `removeRange` أو `removeItem` على كائن `PageHistory`.
- **هل تغيير عنوان الصفحة جزء من تعديل السجل؟**  
  بالتأكيد—كل عنصر في السجل له عنوان يمكنك تعديله.
- **هل أحتاج إلى ترخيص لتشغيل هذا الكود؟**  
  ترخيص تقييم مؤقت يكفي للاختبار؛ الترخيص الكامل مطلوب للإنتاج.
- **ما نسخة Java المدعومة؟**  
  يدعم Aspose.Note for Java JDK 8 وما بعده.

## ما هو تعديل سجل صفحات OneNote؟
*تعديل سجل صفحات OneNote* يشير إلى تحرير أو إضافة أو إزالة إدخالات في قائمة المراجعات الداخلية لدفتر ملاحظات OneNote برمجيًا. يتيح لك ذلك الاحتفاظ بالإصدارات ذات الصلة فقط، وإعادة تسمية العناوين التاريخية، وتحسين حجم الدفتر مع تقليل الزيادة العامة للملف.

## لماذا تعديل سجل صفحات OneNote؟
يمكن أن يؤدي تعديل سجل الصفحات إلى تحسين كبير في قابلية إدارة الدفتر وأدائه. من خلال حذف المراجعات غير المستخدمة، تقلل حجم الملف، وتسرع عملية التحميل، وتجعل التنقل أكثر اتساقًا للمستخدمين النهائيين. هذه الفوائد تكون واضحة خاصةً في دفاتر الملاحظات الكبيرة التي تحتوي على مئات الصفحات.

يدعم Aspose.Note **أكثر من 50 تنسيقًا للإدخال والإخراج** ويمكنه معالجة دفاتر ملاحظات تحتوي على **حتى 10,000 صفحة** دون تحميل الملف بالكامل إلى الذاكرة، مما يضمن عمليات عالية الأداء.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. **Java Development Kit (JDK)** – JDK 8 أو أحدث مثبت على جهازك.  
2. **Aspose.Note for Java library** – قم بتنزيله من [صفحة التحميل](https://releases.aspose.com/note/java/).  
3. **مستند OneNote تجريبي** – مثال: `Sample1.one` يمكنك تعديلّه بأمان.

## استيراد الحزم

الفئات التالية مطلوبة: `Document` تمثل دفتر الملاحظات بالكامل، `Page` تمثل صفحة فردية، و`PageHistory` تدير مجموعة الصفحات التاريخية.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## كيفية تعديل سجل صفحات OneNote؟

قم بتحميل دفتر الملاحظات، استرجع مجموعة `PageHistory` الخاصة به، ثم استخدم الطرق المتوفرة لحذف أو استبدال أو إدراج إدخالات. تُجرى جميع العمليات في الذاكرة، وتحتاج فقط إلى استدعاء `save` مرة واحدة في النهاية لحفظ التغييرات.

### الخطوة 1: تحميل مستند OneNote

`Document` يقوم بتحميل ملف OneNote إلى الذاكرة ويوفر الوصول إلى صفحاته وتاريخه.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### الخطوة 2: استرجاع الصفحة الأولى وسجلها

`PageHistory` هو فئة Aspose.Note التي تخزن قائمة مراجعات دفتر الملاحظات. توفر طرقًا للاستعلام، والإضافة، أو إزالة الصفحات التاريخية.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### الخطوة 3: حذف مجموعة من عناصر السجل

`removeRange(int start, int count)` يزيل كتلة متتالية من عناصر السجل بدءًا من الفهرس المحدد.

```java
pageHistory.removeRange(0, 1);
```

### الخطوة 4: استبدال عنصر من السجل

`set_Item(int index, Page page)` يستبدل عنصر السجل في الموضع المحدد بكائن `Page` جديد.

```java
pageHistory.set_Item(0, new Page());
```

### الخطوة 5: تغيير عنوان صفحة السجل

`setTitle(String title)` يحدث عنوان كائن `Page` التاريخي.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### الخطوة 6: إضافة إدخال سجل جديد

`addItem(Page page)` يضيف صفحة جديدة إلى نهاية مجموعة السجل.

```java
pageHistory.addItem(new Page());
```

### الخطوة 7: إدراج صفحة في موضع محدد

`insertItem(int index, Page page)` يدرج صفحة في الفهرس المحدد، مع دفع العناصر اللاحقة إلى الأمام.

```java
pageHistory.insertItem(1, new Page());
```

### الخطوة 8: حفظ دفتر الملاحظات المعدل

`save(String path)` يكتب دفتر الملاحظات المحدث إلى الموقع المحدد.

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## الأخطاء الشائعة والنصائح

- **فهرس خارج النطاق:** تحقق دائمًا من حجم المجموعة قبل استدعاء `removeRange` أو `insertItem`.  
- **عناوين فارغة:** قد تفتقر بعض الصفحات التاريخية إلى عنوان؛ احرص على معالجة `null` عند استدعاء `getTitle()`.  
- **مكان الحفظ:** تأكد من أن مسار الإخراج (`ModifyPageHistory_out.one`) قابل للكتابة؛ وإلا سيُرمى استثناء `IOException`.  
- **نصيحة الأداء:** عند العمل مع دفاتر ملاحظات ضخمة جدًا، استدعِ `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` لتمكين التحميل الكسول وتقليل استهلاك الذاكرة.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Note for Java مع أطر Java أخرى؟**  
ج: نعم، يتكامل Aspose.Note for Java بسلاسة مع Spring وHibernate وAndroid وغيرها من بيئات Java.

**س: هل Aspose.Note for Java متوافق مع إصدارات مختلفة من ملفات OneNote؟**  
ج: بالتأكيد—يدعم Aspose.Note كلًا من ملفات OneNote 2007 القديمة وصيغ OneNote 2016/Online الحديثة.

**س: هل يتطلب Aspose.Note for Java أي تبعيات إضافية؟**  
ج: لا، المكتبة مكتفية ذاتيًا؛ تحتاج فقط إلى ملف JAR الأساسي وبيئة تشغيل Java.

**س: هل يمكنني إجراء تعديلات جماعية على ملفات OneNote متعددة في وقت واحد؟**  
ج: نعم، يمكنك التكرار عبر مجلد يحتوي على ملفات `.one` وتطبيق منطق تعديل السجل على كل دفتر ملاحظات.

**س: هل هناك منتدى مجتمع لـ Aspose.Note for Java يمكنني طرح الأسئلة فيه؟**  
ج: نعم، يمكنك زيارة [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على المساعدة ومشاركة الأمثلة.

---

**آخر تحديث:** 2026-05-31  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [aspose.note page revisions tutorial – Get Page Revisions in OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [How to Save OneNote Page Version – Push Current Page Version in OneNote - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [track changes onenote – Manage Page Revisions with Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}