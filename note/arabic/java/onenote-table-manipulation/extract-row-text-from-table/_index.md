---
title: استخراج نص الصف من الجدول في مستند OneNote - Aspose.Note
linktitle: استخراج نص الصف من الجدول في مستند OneNote - Aspose.Note
second_title: Aspose.Note جافا API
description: تعرّف على كيفية استخراج نص الصف من جداول OneNote بسهولة باستخدام Aspose.Note لـ Java. اتبع دليلنا خطوة بخطوة للتكامل السلس.
weight: 13
url: /ar/java/onenote-table-manipulation/extract-row-text-from-table/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استخراج نص الصف من الجدول في مستند OneNote - Aspose.Note

## مقدمة
مرحبًا بك في هذا البرنامج التعليمي الشامل حول استخراج نص الصف من الجداول في مستندات OneNote باستخدام Aspose.Note لـ Java. Aspose.Note هي مكتبة Java قوية تمكن المطورين من العمل مع ملفات Microsoft OneNote بسلاسة. في هذا البرنامج التعليمي، سنرشدك خلال العملية خطوة بخطوة، ونوضح لك كيفية استخراج نص الصف بكفاءة من الجداول الموجودة في مستندات OneNote الخاصة بك.
## المتطلبات الأساسية
قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
-  Aspose.Note لمكتبة Java: تأكد من تثبيت Aspose.Note لمكتبة Java. يمكنك تنزيله من[رابط التحميل](https://releases.aspose.com/note/java/).
- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على جهازك.
- مستند OneNote: قم بإعداد نموذج مستند OneNote (على سبيل المثال، "Sample1.one") يحتوي على الجداول التي تريد استخراج نص الصف منها.
## حزم الاستيراد
في مشروع Java الخاص بك، قم باستيراد حزم Aspose.Note الضرورية. وهذا يضمن أن لديك حق الوصول إلى الفئات والأساليب المطلوبة للعمل مع مستندات OneNote.
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableRow;
```
## الخطوة 1: قم بتعيين دليل المستندات
```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory";
```
## الخطوة 2: قم بتحميل مستند OneNote
```java
// قم بتحميل المستند إلى Aspose.Note.
Document document = new Document(dataDir + "Sample1.one", new LoadOptions());
```
## الخطوة 3: الحصول على عقد الجدول
```java
// الحصول على قائمة العقد الجدول
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```
## الخطوة 4: التكرار من خلال الجداول والصفوف
```java
// ضبط عدد الصفوف
int rowCount = 0;
for (Table table : nodes) {
    // التكرار من خلال صفوف الجدول
    for (TableRow row : table) {
        rowCount++;
        // استرداد النص
        List<RichText> textNodes = (List<RichText>) row.getChildNodes(RichText.class);
        StringBuilder text = new StringBuilder();
        for (RichText richText : textNodes) {
            text = text.append(richText.getText().toString());
        }
        // طباعة النص على شاشة الإخراج
        System.out.println(text);
    }
}
```
كرر هذه الخطوات لكل جدول في مستند OneNote، وستتمكن من استخراج نص الصف بنجاح.
## خاتمة
تهانينا! لقد تعلمت كيفية استخراج نص الصف من الجداول في مستندات OneNote باستخدام Aspose.Note لـ Java. يوفر هذا البرنامج التعليمي أساسًا للاستفادة من الإمكانات القوية لـ Aspose.Note في تطبيقات Java الخاصة بك.
## أسئلة مكررة
### هل Aspose.Note متوافق مع الإصدار الأحدث من Microsoft OneNote؟
 يدعم Aspose.Note إصدارات OneNote المختلفة، بما في ذلك الإصدار الأحدث. الرجوع إلى[توثيق](https://reference.aspose.com/note/java/) للحصول على تفاصيل التوافق.
### هل يمكنني تجربة Aspose.Note لـ Java قبل الشراء؟
نعم، يمكنك استكشاف النسخة التجريبية المجانية من Aspose.Note على[هذا الرابط](https://releases.aspose.com/).
### أين يمكنني العثور على دعم ومساعدة إضافيين؟
 قم بزيارة[منتدى Aspose.Note](https://forum.aspose.com/c/note/28) لدعم المجتمع والمناقشات.
### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note؟
 احصل على ترخيص مؤقت من[هذا الرابط](https://purchase.aspose.com/temporary-license/).
### هل هناك أي متطلبات نظام محددة لاستخدام Aspose.Note لـ Java؟
راجع الوثائق لمعرفة متطلبات النظام التفصيلية.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
