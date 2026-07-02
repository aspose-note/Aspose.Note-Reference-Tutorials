---
date: 2026-01-12
description: تعلم كيفية تعديل سجل صفحات OneNote، وتغيير عنوان صفحة OneNote، وحذف سجل
  الصفحات في OneNote باستخدام Aspose.Note للغة Java.
linktitle: Modify Page History in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: كيفية تعديل تاريخ صفحة OneNote باستخدام Aspose.Note
url: /ar/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعديل تاريخ صفحة OneNote باستخدام Aspose.Note

في هذا البرنامج التعليمي ستكتشف **كيفية تعديل مستندات OneNote** برمجياً من خلال العمل مع تاريخ الصفحات. سنستعرض تحميل ملف OneNote، تعديل إدخالات التاريخ الخاصة به، تغيير عنوان الصفحة، وأخيراً حفظ دفتر الملاحظات المحدث—كل ذلك باستخدام Aspose.Note for Java API. سواء كنت بحاجة إلى تنظيف الإصدارات القديمة أو إعادة تسمية الصفحات، فإن الخطوات أدناه تقدم لك حلاً كاملاً وجاهزاً للإنتاج.

## إجابات سريعة
- **ماذا يعني “تاريخ الصفحة” في OneNote؟**  
  هو مجموعة الإصدارات السابقة للصفحة المخزنة داخل ملف OneNote.
- **هل يمكنني حذف إدخال تاريخ معين؟**  
  نعم، استخدم طريقتي `removeRange` أو `removeItem` على كائن `PageHistory`.
- **هل تغيير عنوان الصفحة جزء من تعديل التاريخ؟**  
  بالتأكيد—كل عنصر تاريخ له عنوان يمكنك تعديله.
- **هل أحتاج إلى ترخيص لتشغيل هذا الكود؟**  
  ترخيص تجريبي مؤقت يكفي للاختبار؛ الترخيص الكامل مطلوب للإنتاج.
- **ما نسخة Java المدعومة؟**  
  يدعم Aspose.Note for Java JDK 8 وما بعده.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. **مجموعة تطوير Java (JDK)** – JDK 8 أو أحدث مثبت على جهازك.  
2. **مكتبة Aspose.Note for Java** – حمّلها من [صفحة التحميل](https://releases.aspose.com/note/java/).  
3. **مستند OneNote تجريبي** – مثال: `Sample1.one` يمكنك تعديلّه بأمان.

## استيراد الحزم

أولاً، استورد الفئات التي ستحتاجها. يجب أن يبقى كتلة الشيفرة أدناه كما هي تمامًا.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل مستند OneNote

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### الخطوة 2: استرجاع الصفحة الأولى وتاريخها

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### الخطوة 3: حذف مجموعة من عناصر التاريخ

إذا كنت بحاجة إلى **حذف تاريخ صفحة OneNote**، استدعِ `removeRange`. يزيل المثال الإدخال الأول.

```java
pageHistory.removeRange(0, 1);
```

### الخطوة 4: استبدال عنصر تاريخ

يمكنك استبدال عنصر تاريخ موجود بكائن `Page` جديد.

```java
pageHistory.set_Item(0, new Page());
```

### الخطوة 5: تغيير عنوان صفحة التاريخ

تغيير العنوان هو طلب شائع عندما تريد **تغيير عنوان صفحة OneNote** لإصدار معين.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### الخطوة 6: إضافة إدخال تاريخ جديد

أضف صفحة جديدة إلى مجموعة التاريخ.

```java
pageHistory.addItem(new Page());
```

### الخطوة 7: إدراج صفحة في موضع محدد

أدرج صفحة في الفهرس 1، مما يدفع العناصر الحالية إلى الأمام.

```java
pageHistory.insertItem(1, new Page());
```

### الخطوة 8: حفظ دفتر الملاحظات المعدل

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## لماذا تعديل تاريخ صفحة OneNote؟

- **التحكم في الإصدارات:** احتفظ فقط بالإصدارات ذات الصلة وتخلص من المسودات غير الضرورية.  
- **الاتساق:** مواءمة عناوين الصفحات عبر جميع الإصدارات التاريخية لتحسين التنقل.  
- **الأداء:** مجموعات التاريخ الأصغر تقلل حجم الملف وتسرّع عملية التحميل.

## الأخطاء الشائعة والنصائح

- **فهرس خارج النطاق:** تحقق دائمًا من حجم المجموعة قبل استدعاء `removeRange` أو `insertItem`.  
- **عناوين فارغة:** قد تفتقر بعض الصفحات التاريخية إلى عنوان؛ احرص على معالجة `null` عند استدعاء `getTitle()`.  
- **مكان الحفظ:** تأكد من أن مسار الإخراج (`ModifyPageHistory_out.one`) قابل للكتابة؛ وإلا سيُطرح استثناء `IOException`.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Note for Java مع أطر عمل Java أخرى؟**  
ج: نعم، Aspose.Note for Java متوافق مع أطر عمل Java المختلفة مثل Spring وHibernate وغيرها.

**س: هل Aspose.Note for Java متوافق مع إصدارات مختلفة من ملفات OneNote؟**  
ج: يدعم Aspose.Note for Java العمل مع كل من الإصدارات القديمة والجديدة من ملفات OneNote.

**س: هل يتطلب Aspose.Note for Java أي تبعيات إضافية؟**  
ج: لا، Aspose.Note for Java مكتبة مستقلة ولا تحتاج إلى أي تبعيات إضافية.

**س: هل يمكنني إجراء تعديلات جماعية على عدة ملفات OneNote في آنٍ واحد؟**  
ج: نعم، توفر Aspose.Note for Java واجهات برمجة تطبيقات لمعالجة التعديلات الجماعية بكفاءة.

**س: هل هناك منتدى مجتمع لـ Aspose.Note for Java يمكنني طرح الأسئلة فيه؟**  
ج: نعم، يمكنك زيارة [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على أي مساعدة أو استفسارات تتعلق بالمكتبة.

---

**آخر تحديث:** 2026-01-12  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}