---
date: 2025-12-31
description: تعلم كيفية استخراج مرفقات OneNote باستخدام Java مع Aspose.Note. استرجع
  الملفات من مستندات .one بسرعة وموثوقية.
linktitle: Retrieve Attachment from OneNote using Java
second_title: Aspose.Note Java API
title: كيفية استخراج مرفقات OneNote باستخدام Java
url: /ar/java/onenote-java-integration/retrieve-attachment/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استخراج مرفقات OneNote باستخدام Java

## المقدمة

في عصرنا الرقمي اليوم، **كيفية استخراج OneNote** برمجياً تُعد تحديًا شائعًا للمطورين الذين يبنون تطبيقات تركز على المستندات. تجعل مكتبة Aspose.Note for Java هذه المهمة سهلة من خلال توفير API غني يمكنه قراءة، تعديل، وتصدير المحتوى من ملفات Microsoft OneNote *.one*. في هذا الدرس ستتعلم كيفية استرجاع المرفقات—مثل الصور، ملفات PDF، أو مستندات Word—من دفتر ملاحظات OneNote باستخدام Java.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.Note for Java  
- **هل يمكن استخراج الملفات من .one دون فك الضغط يدويًا؟** نعم، الـ API يقرأ تنسيق .one مباشرة.  
- **هل أحتاج رخصة للتطوير؟** رخصة تقييم مجانية تكفي للاختبار؛ الرخصة الكاملة مطلوبة للإنتاج.  
- **ما نسخة Java المدعومة؟** Java 8 أو أعلى.  
- **هل المعالجة الدفعة ممكنة؟** بالتأكيد—يمكنك تكرار العملية على مستندات متعددة بنفس الكود.

## ما هو “كيفية استخراج OneNote”؟
استخراج محتوى OneNote يعني قراءة دفتر *.one* برمجياً وسحب الموارد المدمجة (المرفقات، الصور، النص). هذا يتيح سيناريوهات مثل أرشفة المستندات تلقائيًا، ترحيل المحتوى، أو إعداد تقارير مخصصة.

## لماذا نستخدم Aspose.Note for Java؟
- **دعم كامل للتنسيق** – يتعامل مع كل عنصر من بنية ملف OneNote.  
- **لا حاجة لتثبيت Office** – يعمل في بيئات بدون واجهة (headless) مثل الخوادم أو خطوط CI.  
- **جاهز للدفعات** – يعالج عشرات دفاتر الملاحظات في تشغيل واحد مع استهلاك ذاكرة منخفض.  

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من جاهزية ما يلي:

### مجموعة تطوير Java (JDK)

1. حمّل أحدث JDK من Oracle أو موزع OpenJDK.  
2. أضف مسار دليل `bin` الخاص بالـ JDK إلى متغير النظام `PATH`.  
3. تحقق باستخدام `java -version` و `javac -version`.

### Aspose.Note for Java

1. انتقل إلى [صفحة التحميل](https://releases.aspose.com/note/java/) الخاصة بـ Aspose.Note for Java.  
2. حمّل أحدث أرشيف إصدار.  
3. استخرج ملفات JAR إلى مجلد يمكن لمشروعك الإشارة إليه.

## استيراد الحزم

لبدء العمل، استورد الفئات التي ستحتاجها. الكتلة أدناه لم تتغير عن الدرس الأصلي:

```java
import java.io.ByteArrayInputStream;
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.StandardCopyOption;
import java.util.List;
import com.aspose.note.AttachedFile;
import com.aspose.note.Document;
```

> **نصيحة احترافية:** احتفظ بهذه الاستيرادات معًا في أعلى ملف المصدر لتسهيل الصيانة المستقبلية.

## دليل خطوة بخطوة

### الخطوة 1: تحديد دليل المستند

حدد مكان وجود ملف *.one* المصدر على جهازك.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار المطلق أو النسبي الذي يحتوي على ملف OneNote الخاص بك.

### الخطوة 2: تحميل المستند

أنشئ كائن `Document` يمثل دفتر ملاحظات OneNote.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

> هذا السطر **يسترجع** ملف OneNote ويجهزه للمعالجة اللاحقة.

### الخطوة 3: الحصول على قائمة المرفقات

اطلب من المستند جميع الملفات المرفقة (صور، PDF، إلخ).

```java
List<AttachedFile> attachments = doc.getChildNodes(AttachedFile.class);
```

القائمة المرجعة `List` تحتوي على كائنات `AttachedFile`، كل منها يمثل موردًا مدمجًا واحدًا.

### الخطوة 4: استرجاع المرفقات وحفظها

كرر عبر المجموعة، استخرج البيانات الثنائية، واكتب كل ملف إلى القرص.

```java
for (AttachedFile a : attachments) {
    byte[] buffer = a.getBytes();
    ByteArrayInputStream stream = new ByteArrayInputStream(buffer);
    String outputFile = "Output_" + a.getFileName();
    Path outputPath = Utils.getPath(RetrieveAttachment.class, outputFile);
    Files.copy(stream, outputPath, StandardCopyOption.REPLACE_EXISTING);
    System.out.println("File saved: " + outputPath);
}
```

- `a.getBytes()` يُعيد البايتات الخام للمرفق.  
- `Utils.getPath(...)` يبني مسار إخراج آمن (يمكنك استبداله بأي `Path` تفضله).  
- الحلقة تطبع المسار الكامل لكل ملف محفوظ، لتمنحك تغذية راجعة فورية.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|----------------|-----|
| **عدم إرجاع أي مرفقات** | قد لا يحتوي الدفتر على ملفات مرفقة أو تُخزن في صفحة مختلفة. | تحقق يدويًا من ملف *.one* في OneNote، أو كرر عبر الصفحات (`doc.getChildNodes(Page.class)`) لتحديد المرفقات. |
| **`AccessDeniedException` على Windows** | المجلد الهدف للكتابة قد يكون للقراءة فقط أو يتطلب صلاحيات مرتفعة. | اختر دليلًا قابلًا للكتابة (مثل مجلد `Documents` للمستخدم) أو شغّل JVM بصلاحيات مناسبة. |
| **ملفات كبيرة تسبب OutOfMemoryError** | تحميل مرفقات ضخمة إلى الذاكرة دفعة واحدة. | قم ببث البايتات مباشرة إلى ملف باستخدام `Files.newOutputStream` بدلاً من تحميل المصفوفة بالكامل. |

## الأسئلة المتكررة

**س1: هل يمكنني استرجاع مرفقات من مستندات OneNote محمية بكلمة مرور؟**  
ج: تدعم Aspose.Note for Java فتح دفاتر ملاحظات محمية عندما تزود الاعتمادات الصحيحة أثناء تحميل المستند.

**س2: هل تدعم Aspose.Note for Java المعالجة الدفعة لعدة ملفات OneNote؟**  
ج: نعم، يمكنك وضع الكود داخل حلقة تتكرر على قائمة ملفات *.one*، وتستخرج المرفقات من كل منها.

**س3: هل هناك حد لحجم أو عدد المرفقات التي يمكن استرجاعها؟**  
ج: صُممت الـ API للتعامل مع دفاتر ملاحظات كبيرة، لكن الحدود العملية تعتمد على حجم heap للـ JVM والمساحة المتاحة على القرص.

**س4: هل يمكنني تخصيص موقع الإخراج وتسمية الملفات للمرفقات المستخرجة؟**  
ج: بالتأكيد—عدّل المتغيرات `outputFile` و `outputPath` داخل الحلقة لتتناسب مع نظام التسمية والبنية التي تريدها.

**س5: هل توفر Aspose.Note for Java دعمًا ومساعدة للمشكلات التقنية؟**  
ج: نعم، يمكن للمطورين الوصول إلى دعم شامل عبر منتدى Aspose.Note على الرابط [https://forum.aspose.com/c/note/28](https://forum.aspose.com/c/note/28).

---

**آخر تحديث:** 2025-12-31  
**تم الاختبار مع:** Aspose.Note for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}