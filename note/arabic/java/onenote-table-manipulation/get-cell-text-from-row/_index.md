---
date: 2026-01-25
description: تعلم كيفية تحويل الجدول إلى نص في OneNote باستخدام Aspose.Note للغة Java.
  اتبع هذا الدليل خطوة بخطوة لسرد صفوف الجدول في Java واستخراج محتويات الخلايا بكفاءة.
linktitle: Convert Table to Text in OneNote with Aspose.Note (Java)
second_title: Aspose.Note Java API
title: تحويل الجدول إلى نص في OneNote باستخدام Aspose.Note (Java)
url: /ar/java/onenote-table-manipulation/get-cell-text-from-row/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل الجدول إلى نص في OneNote باستخدام Aspose.Note (Java)

## مقدمة
في هذا البرنامج التعليمي ستكتشف كيفية **تحويل الجدول إلى نص** من مستند OneNote باستخدام مكتبة Aspose.Note للغة Java. سنستعرض خطوات تحميل ملف OneNote، سرد صفوف الجدول في Java، واستخراج النص من كل خلية حتى تتمكن من إعادة استخدامه في تطبيقاتك الخاصة. في النهاية، ستحصل على مقطع شفرة قابل لإعادة الاستخدام يحول بيانات الجدول إلى نص عادي ببضع أسطر من Java فقط.

## إجابات سريعة
- **ماذا يعني “تحويل الجدول إلى نص”؟** استخراج المحتوى النصي من كل خلية في الجدول وربطه في سلسلة قابلة للقراءة.  
- **أي مكتبة تتولى ذلك؟** Aspose.Note للغة Java.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **هل يمكنني معالجة جداول كبيرة؟** نعم – قم بالتكرار صفًا بصف لتقليل استهلاك الذاكرة.  
- **هل هذا متوافق مع Java 17؟** بالتأكيد؛ Aspose.Note يدعم أحدث إصدارات Java.

## المتطلبات السابقة
قبل أن نبدأ، تأكد من أن لديك ما يلي جاهزًا:

- **بيئة تطوير Java** – JDK 8 أو أحدث مثبتة ومُعَّدة.  
- **Aspose.Note للغة Java** – قم بتحميله وتثبيته من [هذا الرابط](https://releases.aspose.com/note/java/).  
- **مستند OneNote تجريبي** – ملف مثل `Sample1.one` موجود في دليل العمل الخاص بك.

## استيراد الحزم
أولاً، استورد فئات Aspose.Note التي سنحتاجها للعمل مع الجداول والنص المنسق.

```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableCell;
import com.aspose.note.TableRow;
```

## الخطوة 1: تحميل مستند OneNote
بعد ذلك، وجه الـ API إلى ملف `.one` الخاص بك واستخرج جميع عقد الجداول.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note.
Document document = new Document(dataDir + "Sample1.one");
// Get a list of table nodes
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```

## كيفية سرد صفوف الجدول في Java باستخدام Aspose.Note
الآن بعد أن حصلنا على الجداول، نحتاج إلى **سرد صفوف الجدول في Java** – أي التكرار عبر كل كائن `TableRow`.

## الخطوة 2: التكرار عبر الجداول واستخراج النص
الحلقات المتداخلة التالية تمر عبر كل جدول، صف، وخلية، وتستخرج عناصر `RichText` وتبني تمثيل نص عادي.

```java
for (Table table : nodes) {
    // Iterate through table rows
    for (TableRow row : table) {
        // Get list of TableCell nodes
        List<TableCell> cellNodes = (List<TableCell>) row.getChildNodes(TableCell.class);
        
        // Iterate through table cells
        for (TableCell cell : cellNodes) {
            // Retrieve text
            List<RichText> textNodes = (List<RichText>) cell.getChildNodes(RichText.class);
            StringBuilder text = new StringBuilder();
            
            // Step 2: Retrieve Text from RichText Nodes
            for (RichText richText : textNodes) {
                text = text.append(richText.getText().toString());
            }
            
            // Step 3: Print Text
            System.out.println(text);
        }
    }
}
```

### لماذا يحقق هذا النهج تحويل الجدول إلى نص
- **المعالجة صفًا بصف** تحافظ على استهلاك منخفض للذاكرة، حتى للجداول الكبيرة.  
- **استخراج RichText** يضمن أنك تلتقط المحتوى المنسق مثل العلامات الغامقة أو المائلة إذا احتجت إليها لاحقًا.  
- **دمج باستخدام `StringBuilder`** يمنحك مخرجات نظيفة وقابلة للقراءة جاهزة للتسجيل أو التخزين أو التحليل الإضافي.

## المشكلات الشائعة والحلول
| المشكلة | الحل |
|-------|----------|
| **NullPointerException عند `getChildNodes`** | تحقق من أن المستند يحتوي فعليًا على جداول؛ استخدم `if (nodes.isEmpty())` لتجنب النتائج الفارغة. |
| **غياب النص في المخرجات** | قد تحتوي بعض الخلايا على عناصر متداخلة (مثل الصور). تأكد من معالجة عقد `RichText` فقط، أو وسّع الحلقة لتتعامل مع أنواع العقد الأخرى. |
| **تباطؤ الأداء مع جداول ضخمة** | عالج الصفوف على دفعات أو قم ببث المخرجات إلى ملف بدلاً من طباعتها على الشاشة. |

## الأسئلة المتكررة

**س: هل Aspose.Note متوافق مع أحدث إصدارات Java؟**  
ج: التحديثات الدورية تضمن توافق Aspose.Note مع أحدث إصدارات Java. راجع [الوثائق](https://reference.aspose.com/note/java/) للحصول على تفاصيل النسخة المحددة.

**س: هل يمكن تجربة Aspose.Note للغة Java قبل الشراء؟**  
ج: بالتأكيد! نسخة تجريبية مجانية متاحة لك [هنا](https://releases.aspose.com/).

**س: كيف يمكن الحصول على ترخيص مؤقت لـ Aspose.Note للغة Java؟**  
ج: احصل على ترخيص مؤقت بزيارة [هذا الرابط](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني العثور على دعم المجتمع لـ Aspose.Note للغة Java؟**  
ج: انضم إلى مجتمع Aspose.Note النشط على [المنتدى](https://forum.aspose.com/c/note/28) للمناقشات والمساعدة.

**س: هل تتوفر مستندات عينة لأغراض الاختبار؟**  
ج: استكشف وثائق Aspose.Note للحصول على مجموعة غنية من المستندات العينة ومقاطع الشفرة.

---

**آخر تحديث:** 2026-01-25  
**تم الاختبار مع:** Aspose.Note للغة Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}