---
date: 2026-03-27
description: تعرّف على كيفية استخراج تفاصيل المهام من مهام OneNote Outlook باستخدام
  Aspose.Note للغة Java – حل سريع وموثوق لمطوري Java.
linktitle: Get Outlook Task in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: كيفية استخراج مهمة من مهام OneNote Outlook – Aspose.Note
url: /ar/java/onenote-text-manipulation/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استخراج المهمة من مهام OneNote Outlook

## المقدمة
إذا كنت بحاجة إلى **كيفية استخراج مهمة** موجودة داخل صفحة OneNote — خاصةً مهام Outlook — فإن Aspose.Note for Java يجعل العملية سهلة. في هذا الدرس العملي سنستعرض الخطوات الدقيقة لسحب خصائص المهمة (الحالة، تاريخ الاستحقاق، وقت الإنشاء، إلخ) من مستند OneNote، ثم طباعتها على وحدة التحكم. في النهاية ستحصل على مقتطف قابل لإعادة الاستخدام يمكنك دمجه في أي مشروع Java يعمل مع ملفات OneNote.

## إجابات سريعة
- **ماذا يغطي هذا الدرس؟** استخراج تفاصيل مهمة Outlook من ملف OneNote باستخدام Aspose.Note for Java.  
- **كم يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لإعداد أساسي.  
- **المتطلبات المسبقة؟** Java JDK، مكتبة Aspose.Note for Java، وملف OneNote يحتوي على مهام.  
- **هل أحتاج إلى ترخيص؟** يلزم وجود ترخيص مؤقت أو كامل لـ Aspose.Note للاستخدام في بيئة الإنتاج.  
- **هل يمكن تشغيله على أي نظام تشغيل؟** نعم — المكتبة مستقلة عن النظام طالما أن Java تعمل.

## ما هو استخراج المهمة من OneNote؟
استخراج المهمة يعني قراءة الوسم `NoteTask` الذي يخزّنه OneNote لكل مهمة مرتبطة بـ Outlook. يحمل الوسم بيانات وصفية مثل وقت الإكمال، تاريخ الاستحقاق، والحالة، والتي يمكنك الوصول إليها برمجياً عبر نموذج كائنات Aspose.Note.

## لماذا نحتاج إلى استخراج معلومات المهمة؟
- **الأتمتة:** مزامنة المهام مع نظام إدارة المهام الخاص بك.  
- **التقارير:** إنشاء تقارير مخصصة عن تقدم المهام عبر دفاتر ملاحظات متعددة.  
- **الهجرة:** نقل المهام من OneNote إلى منصات أخرى (مثل Microsoft Planner أو Jira).  

## المتطلبات المسبقة
قبل أن تبدأ، تأكد من وجود ما يلي:

- **Java Development Kit (JDK)** — أي نسخة حديثة (8 أو أعلى).  
- **Aspose.Note for Java** — قم بتحميله من [صفحة التحميل](https://releases.aspose.com/note/java/).  

## استيراد الحزم
ابدأ باستيراد الفئات الضرورية إلى ملف مصدر Java الخاص بك:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## الخطوة 1: إعداد المشروع
أنشئ مشروع Java جديد (Maven، Gradle، أو IDE عادي) وأضف ملف JAR الخاص بـ Aspose.Note إلى مسار الفئة (classpath). احتفظ بملفات OneNote في مجلد مخصص، على سبيل المثال `data/`.

## الخطوة 2: تحميل مستند OneNote
حمّل ملف `.one` الذي تريد فحصه:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

> **نصيحة احترافية:** استخدم مسارًا مطلقًا أو خاصية تكوين إذا كان تطبيقك يعمل في بيئات مختلفة.

## الخطوة 3: استرجاع عقد RichText
جميع العناصر النصية ممثلة بعقد `RichText`. احصل عليها جميعًا:

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

## الخطوة 4: التكرار عبر كل عقدة
ابحث في كل عقدة `RichText` عن وسم `NoteTask`:

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            // Your code to handle NoteTask
        }
    }
}
```

## الخطوة 5: استرجاع خصائص المهمة
بمجرد حصولك على كائن `NoteTask`، يمكنك قراءة خصائصه:

```java
NoteTask noteTask = (NoteTask) tag;
System.out.println("Completed Time: " + noteTask.getCompletedTime());
System.out.println("Create Time: " + noteTask.getCreationTime());
System.out.println("Due Date: " + noteTask.getDueDate());
System.out.println("Status: " + noteTask.getStatus());
System.out.println("Icon: " + noteTask.getIcon());
```

> **ملاحظة:** نفّذ الحلقة لكل عقدة `NoteTask` لاستخراج المعلومات من جميع المهام في المستند.

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|-------|--------|-----|
| `NullPointerException` على `noteTask` | الوسم ليس من نوع `NoteTask`. | أضف فحصًا للـ null أو تحقق من `tag instanceof NoteTask`. |
| لا توجد مخرجات للتواريخ | المهمة في OneNote لا تحتوي على تاريخ استحقاق. | تحقق من `noteTask.getDueDate()` إذا كان `null` قبل الطباعة. |
| المكتبة غير موجودة وقت التشغيل | ملف JAR غير موجود في مسار الفئة. | تأكد من تضمين ملف Aspose.Note JAR في إعدادات البناء. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Note for Java مع أطر عمل Java أخرى؟**  
ج: نعم، يتكامل Aspose.Note for Java بسلاسة مع Spring، Jakarta EE، Android، وأي بيئة Java قياسية.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Note for Java؟**  
ج: نعم، يمكنك تجربة نسخة تجريبية مجانية من Aspose.Note for Java [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.Note for Java؟**  
ج: زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على مساعدة المجتمع أو اشترِ خطة دعم متميزة.

**س: أين يمكنني العثور على وثائق مفصلة لـ Aspose.Note for Java؟**  
ج: راجع [وثائق Aspose.Note for Java](https://reference.aspose.com/note/java/) للحصول على مراجع API متعمقة وأمثلة.

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.Note for Java؟**  
ج: احصل على ترخيصك المؤقت [هنا](https://purchase.aspose.com/temporary-license/).

## الخلاصة
لقد أصبحت الآن متمكنًا من **كيفية استخراج مهمة** من OneNote باستخدام Aspose.Note for Java. تفتح هذه القدرة الباب أمام سيناريوهات الأتمتة، وإعداد التقارير، والهجرة التي كانت سابقةً يدوية ومعرضة للأخطاء. لا تتردد في توسيع العينة — احفظ البيانات المستخرجة في قاعدة بيانات، ادفعها إلى خدمة خارجية، أو اجمعها مع محتوى OneNote آخر.

---

**آخر تحديث:** 2026-03-27  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}