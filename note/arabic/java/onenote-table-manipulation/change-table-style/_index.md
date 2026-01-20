---
date: 2026-01-20
description: تعلم كيفية تغيير نمط الجدول في OneNote باستخدام Aspose.Note للغة Java
  وتعيين ألوان خلفية صفوف الجدول. اتبع الدليل خطوة بخطوة لتطبيق لون الخلفية، وتنسيق
  النص بالخط العريض، وحفظ مستند OneNote.
linktitle: Change Table Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: كيفية تغيير نمط الجدول في OneNote باستخدام Aspose.Note
url: /ar/java/onenote-table-manipulation/change-table-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تغيير نمط الجدول في OneNote باستخدام Aspose.Note

## المقدمة
إذا كنت بحاجة إلى **كيفية تغيير نمط الجدول** في دفتر ملاحظات OneNote، فإن Aspose.Note for Java يجعل العملية سهلة للغاية. في هذا البرنامج التعليمي سنستعرض العملية بالكامل — من تحميل ملف OneNote، تعيين ألوان خلفية لصفوف الجدول، تطبيق تنسيق غامق ومائل، إلى حفظ المستند المحدث في النهاية. بنهاية هذا الدليل ستكون مرتاحًا مع تنسيق جداول OneNote، وتعرف كيفية تطبيق لون الخلفية على الصفوف، وتفهم كيفية حفظ مستند OneNote بالأنماط الجديدة.

## إجابات سريعة
- **ما هي المكتبة الأفضل لتنسيق جداول OneNote؟** Aspose.Note for Java.  
- **هل يمكنني تعيين ألوان خلفية لصفوف الجدول؟** نعم، باستخدام طريقة المساعدة `setRowStyle`.  
- **كيف أجعل النص غامقًا في جدول OneNote؟** اضبط علامة `bold` في `setRowStyle`.  
- **ما المطلوب لحفظ الملف المعدل؟** استدعِ `document.save(...)` مع مسار صالح.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** نعم، يلزم ترخيص تجاري.  

## ما هو “كيفية تغيير نمط الجدول” في OneNote؟
تغيير نمط الجدول يعني تعديل ألوان الصفوف، تنسيق النص، والمظهر العام بحيث يصبح البيانات أسهل للقراءة وأكثر جاذبية بصريًا. توفر Aspose.Note واجهة برمجة تطبيقات سلسة للتعامل مع هذه الخصائص برمجيًا.

## لماذا تستخدم Aspose.Note for Java؟
- **تحكم كامل** في هياكل OneNote دون الحاجة إلى العمل اليدوي عبر الواجهة.  
- **دعم متعدد المنصات**؛ يعمل على أي نظام تشغيل يدعم Java.  
- **خيارات تنسيق غنية** مثل ألوان الخلفية، النص الغامق والمائل.  

## المتطلبات المسبقة
قبل أن تبدأ، تأكد من وجود ما يلي:
- **بيئة تطوير Java** – JDK 8 أو أعلى مثبت.  
- **مكتبة Aspose.Note for Java** – حمّلها من [صفحة التحميل](https://releases.aspose.com/note/java/).  
- **دليل المستندات** – مجلد سيحتوي على ملفات `.one` الخاصة بك.  

## استيراد الحزم
في مشروع Java الخاص بك، استورد الحزم اللازمة للعمل مع Aspose.Note:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

## الخطوة 1: إعداد المستند
حمّل مستند OneNote إلى Aspose.Note واسترجع قائمة عقد الجداول.
```java
// Set up the document and get the list of table nodes
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```

## الخطوة 2: تعيين أنماط الصفوف
تجول عبر كل جدول، عيّن النمط لكل صف، بما في ذلك تمييز الصف الأول بعد العنوان. هذا يوضح **تعيين خلفية صف الجدول** و**كيفية تطبيق لون الخلفية**.
```java
// Set row styles for each table in the document
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Highlight first row after the head.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```

## طريقة setRowStyle
طريقة المساعدة تطبق لون الخلفية، والنص الغامق والمائل على كل خلية في الصف. هنا يتم تنفيذ **كيفية جعل النص غامقًا في onenote**.
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```

## الخطوة 3: حفظ المستند
بعد تنسيق الجداول، احفظ المستند المعدل. هذا يوضح **كيفية حفظ مستند onenote** مع تطبيق التنسيق الجديد.
```java
// Save the modified document
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```

## الخلاصة
Aspose.Note for Java يبسط عملية التعامل مع ملفات OneNote. من خلال الاستفادة من قدرات المكتبة، يمكنك بسهولة تغيير أنماط الجداول، تعيين ألوان خلفية لصفوف الجداول، جعل النص غامقًا، وحفظ مستند OneNote — كل ذلك ببضع أسطر من الشيفرة.

## الأسئلة المتكررة
### أين يمكنني العثور على وثائق Aspose.Note for Java؟
قم بزيارة [الوثائق](https://reference.aspose.com/note/java/) للحصول على إرشادات شاملة.

### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note for Java؟
اتبع هذا [الرابط](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت.

### هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Note for Java؟
نعم، يمكنك تنزيل نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

### أين يمكنني الحصول على الدعم لـ Aspose.Note for Java؟
انضم إلى [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على مساعدة من المجتمع.

### كيف يمكنني شراء Aspose.Note for Java؟
يمكنك شراء المكتبة من [هنا](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-20  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

---