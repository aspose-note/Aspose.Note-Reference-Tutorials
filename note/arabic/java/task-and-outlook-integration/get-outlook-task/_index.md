---
date: 2026-04-01
description: تعلم كيفية استخراج المهام من Outlook في OneNote باستخدام Aspose.Note
  للـ Java. اتبع هذا الدليل خطوة بخطوة لاسترجاع تفاصيل المهام بسرعة.
keywords:
- how to extract tasks
- Aspose.Note Java
- Outlook task extraction
linktitle: احصل على مهمة Outlook في OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: كيفية استخراج مهام Outlook في OneNote باستخدام Aspose.Note
url: /ar/java/task-and-outlook-integration/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# الحصول على مهمة Outlook في OneNote - Aspose.Note

## مقدمة
مرحبًا بكم في دليلنا الشامل حول **كيفية استخراج المهام** من Outlook في دفتر ملاحظات OneNote باستخدام Aspose.Note for Java. سواءً كنت تبني أداة ترحيل، أو تولد تقارير، أو تحتاج ببساطة إلى مزامنة بيانات المهام، فإن هذا البرنامج التعليمي يشرح لك كل خطوة — من تحميل ملف OneNote إلى قراءة خصائص كل مهمة Outlook. في النهاية، ستحصل على مقتطف شفرة جاهز للاستخدام يمكنك تعديله لمشاريعك الخاصة.

## إجابات سريعة
- **ما الذي يغطيه هذا البرنامج التعليمي؟** استخراج تفاصيل مهام Outlook من مستند OneNote باستخدام Aspose.Note for Java.  
- **ما الـ API المستخدم؟** مكتبة Aspose.Note Java.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **كم من الوقت تستغرق العملية؟** حوالي 10‑15 دقيقة بمجرد إعداد البيئة.  
- **هل يمكنني معالجة دفاتر ملاحظات متعددة؟** نعم — فقط قم بتكرار الملفات وإعادة استخدام نفس المنطق.

## ما هو استخراج المهام؟
يشير استخراج المهام إلى قراءة معلومات المهام المنظمة (مثل تواريخ الاستحقاق، الحالة، والرموز) التي يخزنها Outlook داخل صفحات OneNote كعلامات `NoteTask`. يتيح ذلك الوصول البرمجي إلى بيانات تعريف المهام دون الحاجة إلى النسخ اليدوي.

## لماذا نستخدم Aspose.Note for Java؟
- **لا يتطلب Microsoft Office** – يعمل على أي منصة تحتوي على بيئة تشغيل Java.  
- **دقة كاملة** – يحافظ على جميع عناصر OneNote مع منحك وصولًا مباشرًا إلى العلامات.  
- **أداء عالي** – مُحسّن للدفاتر الكبيرة والمعالجة الدفعية.  

## المتطلبات المسبقة
قبل أن نبدأ، تأكد من أن لديك ما يلي جاهزًا:

- **بيئة تطوير Java** – JDK 8 أو أحدث مثبتة ومُعَدة.  
- **مكتبة Aspose.Note** – قم بتنزيل أحدث حزمة Java من الموقع الرسمي [هنا](https://releases.aspose.com/note/java/).  
- **ملف OneNote تجريبي** – يستخدم البرنامج التعليمي `Sample1.one`؛ يمكنك استبداله بأي دفتر ملاحظات يحتوي على مهام Outlook.

## استيراد الحزم
أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك. هذه الفئات تمنحك الوصول إلى نموذج المستند وعلامة `NoteTask` الخاصة بـ Outlook.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## دليل خطوة بخطوة

### الخطوة 1: إعداد دليل المستند الخاص بك
حدد المجلد الذي يحتوي على ملف OneNote الخاص بك. استخدام مسار مطلق أو نسبي يعمل، ولكن حافظ على نظافة سلسلة المسار لسهولة القراءة.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تحميل مستند OneNote
أنشئ كائن `Document` بالإشارة إلى ملف `.one`. يقوم Aspose.Note بتحليل الملف إلى بنية شبيهة بـ DOM يمكنك استعراضها.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### الخطوة 3: الحصول على جميع عقد RichText
تُخزن مهام Outlook داخل عناصر `RichText`. استرجع كل عقدة `RichText` لتتمكن من فحص علاماتها.

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

### الخطوة 4: التكرار عبر كل عقدة
قم بالتكرار عبر كل عقدة `RichText`، افحص علاماتها، وتفاعل عندما تصادف `NoteTask`. يطبع الكود أدناه أكثر الخصائص فائدة لكل مهمة.

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Retrieve properties
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```

**نصيحة احترافية:** إذا كنت تحتاج فقط إلى مجموعة فرعية من الخصائص، يمكنك تخطي الأخرى لتحسين الأداء عند معالجة دفاتر ملاحظات كبيرة.

### المشكلات الشائعة والحلول
- **لم يتم العثور على مهام:** تأكد من أن صفحة OneNote تحتوي فعليًا على مهام Outlook. تظهر كصناديق اختيار مع أيقونة Outlook صغيرة.  
- **قيم فارغة:** قد تكون بعض حقول المهمة (مثل `CompletedTime`) `null` إذا لم تُكمل المهمة. احمِ نفسك من `NullPointerException` بالتحقق من `null` قبل الطباعة.  
- **الملف غير موجود:** تحقق من أن `dataDir` ينتهي بفاصل المسار المناسب (`/` أو `\\`) لنظام التشغيل الخاص بك.

## الخلاصة
تهانينا! لقد تعلمت **كيفية استخراج المهام** من Outlook في OneNote باستخدام Aspose.Note Java API. يمنحك هذا النهج تحكمًا برمجيًا كاملاً في بيانات المهام، مما يتيح التكامل مع أدوات التقارير المخصصة، قواعد البيانات، أو سير عمل الأعمال الأخرى.

## الأسئلة المتكررة

**س: هل Aspose.Note متوافق مع جميع إصدارات OneNote؟**  
ج: يدعم Aspose.Note Microsoft OneNote 2010 والإصدارات الأحدث.

**س: هل يمكنني استخدام Aspose.Note للمشاريع الشخصية والتجارية؟**  
ج: نعم، يمكن استخدام Aspose.Note للمشاريع الشخصية والتجارية. زر [هنا](https://purchase.aspose.com/buy) لاستكشاف خيارات الترخيص.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Note؟**  
ج: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.Note؟**  
ج: زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على دعم المجتمع. للحصول على مساعدة إضافية، فكر في شراء [ترخيص مؤقت](https://purchase.aspose.com/temporary-license/).

**س: هل هناك مستندات OneNote تجريبية متاحة للاختبار؟**  
ج: يمكنك العثور على مستندات تجريبية في وثائق Aspose.Note [هنا](https://reference.aspose.com/note/java/).

---

**آخر تحديث:** 2026-04-01  
**تم الاختبار مع:** Aspose.Note for Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}