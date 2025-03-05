---
title: تغيير نمط الجدول في OneNote - Aspose.Note
linktitle: تغيير نمط الجدول في OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: قم بتحسين جداول OneNote الخاصة بك بسهولة باستخدام Aspose.Note لـ Java. اتبع دليلنا خطوة بخطوة لتغيير أنماط الجدول. قم بتنزيل المكتبة الآن!
type: docs
weight: 10
url: /ar/java/onenote-table-manipulation/change-table-style/
---
## مقدمة
Aspose.Note for Java هي مكتبة قوية تسمح للمطورين بمعالجة ملفات OneNote دون عناء. في هذا البرنامج التعليمي، سنركز على تغيير نمط الجدول في مستند OneNote باستخدام Aspose.Note لـ Java. اتبع الدليل الموضح خطوة بخطوة لتحسين المظهر المرئي لجداولك.
## المتطلبات الأساسية
قبل البدء، تأكد من توفر ما يلي:
- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على جهازك.
-  Aspose.Note لمكتبة Java: قم بتنزيل وتثبيت Aspose.Note لمكتبة Java من[صفحة التحميل](https://releases.aspose.com/note/java/).
- دليل المستندات: قم بإعداد دليل لتخزين مستندات OneNote الخاصة بك.
## حزم الاستيراد
في مشروع Java الخاص بك، قم باستيراد الحزم اللازمة للعمل مع Aspose.ملاحظة:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## الخطوة 1: إعداد المستند
قم بتحميل مستند OneNote في Aspose.Note واحصل على قائمة عقد الجدول
```java
// قم بإعداد المستند واحصل على قائمة بعقد الجدول
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## الخطوة 2: تعيين أنماط الصف
قم بالمراجعة خلال كل جدول، وقم بتعيين النمط لكل صف، بما في ذلك تمييز الصف الأول بعد الرأس.

```java
// قم بتعيين أنماط الصفوف لكل جدول في المستند
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // تسليط الضوء على الصف الأول بعد الرأس.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## طريقة setRowStyle
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
## الخطوة 3: احفظ المستند
احفظ المستند المعدل باستخدام أنماط الجدول الجديدة.
باتباع هذه الخطوات، يمكنك بسهولة تغيير نمط الجدول في مستند OneNote باستخدام Aspose.Note لـ Java.

```java
// احفظ المستند المعدل
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## خاتمة
يعمل Aspose.Note for Java على تبسيط عملية معالجة ملفات OneNote. ومن خلال الاستفادة من إمكانيات المكتبة، يمكنك تحسين العرض المرئي لجداولك دون عناء.

## الأسئلة الشائعة
### أين يمكنني العثور على الوثائق الخاصة بـ Aspose.Note لـ Java؟
 قم بزيارة[توثيق](https://reference.aspose.com/note/java/) للحصول على إرشادات شاملة.
### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note لـ Java؟
 اتبع هذا[وصلة](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت.
### هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Note لـ Java؟
 نعم، يمكنك تنزيل نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).
### أين يمكنني الحصول على الدعم لـ Aspose.Note لـ Java؟
 انضم الي[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) لطلب المساعدة من المجتمع.
### كيف يمكنني شراء Aspose.Note لـ Java؟
 يمكنك شراء المكتبة[هنا](https://purchase.aspose.com/buy).