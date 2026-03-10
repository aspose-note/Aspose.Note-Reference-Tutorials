---
date: 2025-12-18
description: تعلم كيفية **حفظ OneNote كملف PDF** باستخدام نظام الخطوط المحدد في Java
  مع Aspose.Note. يوضح هذا الدليل أيضًا كيفية تحويل OneNote إلى PDF، وتحميل ملفات
  الخطوط المخصصة، وتحديد الخطوط الافتراضية.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: حفظ OneNote كملف PDF باستخدام نظام الخطوط المحدد
url: /ar/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ OneNote كملف PDF باستخدام نظام الخطوط المحدد

## المقدمة

في العديد من سيناريوهات الأعمال تحتاج إلى **حفظ OneNote كملف PDF** مع الحفاظ على المظهر الدقيق للصفحات الأصلية. تجعل مكتبة Aspose.Note for Java ذلك سهلًا من خلال السماح لك بالتحكم في نظام الخطوط أثناء التحويل. في هذا البرنامج التعليمي سنستعرض ثلاث طرق عملية لـ **تحويل OneNote إلى PDF**، تشمل كيفية **تحميل ملفات خطوط مخصصة**، **تحديد خط افتراضي**، وحتى **استخدام تدفق خط** عندما لا يكون الخط متوفرًا على الجهاز الهدف.

## إجابات سريعة
- **ما معنى “save OneNote as PDF”؟** يقوم بتحويل ملف .one إلى PDF مع الحفاظ على التخطيط والتنسيق كما هو.  
- **أي واجهة برمجة تطبيقات تتعامل مع الخطوط؟** `DocumentFontsSubsystem` تتيح لك تحديد خط افتراضي أو تحميل ملف/تدفق خط مخصص.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** نعم، يلزم وجود ترخيص تجاري لـ Aspose.Note للاستخدام غير التجريبي.  
- **هل يمكنني تحويل ملفات متعددة دفعة واحدة؟** بالتأكيد – ما عليك سوى تكرار منطق تحميل وحفظ `Document`.  
- **ما نسخة Java المطلوبة؟** Java 15 أو أحدث (المثال يستخدم JDK 15).

## ما هو “save OneNote as PDF” مع نظام الخطوط؟

يعني حفظ OneNote كملف PDF مع نظام الخطوط أنه أثناء عملية التحويل تقوم Aspose.Note باستبدال أي رموز مفقودة بالخط الذي تزوده به. هذا يضمن أن يظهر ملف PDF متطابقًا على أي جهاز، حتى عندما لا يكون الخط الأصلي مثبتًا.

## لماذا التحكم في نظام الخطوط عند **تحويل OneNote إلى PDF**؟

- **الاتساق في العلامة التجارية** – المستندات المؤسسية تحتفظ بنوع الخط الدقيق.  
- **موثوقية عبر الأنظمة** – ملفات PDF تُظهر نفس الشكل على Windows وmacOS وLinux والهواتف المحمولة.  
- **تقليل الأخطاء** – تختفي تحذيرات الخطوط المفقودة، مما ينتج مخرجات نظيفة.

## المتطلبات المسبقة

### 1. Java Development Kit (JDK)

تأكد من تثبيت Java Development Kit (JDK) على نظامك. يمكنك تنزيله من [هنا](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) إذا لم تقم بذلك بعد.

### 2. Aspose.Note for Java Library

قم بتنزيل وإعداد مكتبة Aspose.Note for Java. يمكنك تنزيلها من [الموقع الإلكتروني](https://releases.aspose.com/note/java/).

## استيراد الحزم

تأكد من استيراد الحزم الضرورية في مشروع Java الخاص بك:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

الآن لنقسام كل مثال إلى خطوات متعددة لفهم العملية بشكل أفضل.

## كيفية **حفظ OneNote كملف PDF** باستخدام نظام خطوط المستند مع خط افتراضي

### الخطوة 1: الحفظ باستخدام نظام خطوط المستند مع اسم الخط الافتراضي

توضح هذه الخطوة كيفية **حفظ OneNote كملف PDF** بطريقة بسيطة عن طريق تحديد اسم الخط الافتراضي.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

في هذه الخطوة:
- يتم تحميل مستند OneNote باستخدام Aspose.Note.  
- يتم تحديد **الخط الافتراضي** كـ **"Times New Roman"**.  
- يتم حفظ المستند بتنسيق PDF باستخدام الخط المختار.

### الخطوة 2: الحفظ باستخدام نظام خطوط المستند مع خط افتراضي من ملف

هنا **نحمّل ملف خط مخصص** ونستخدمه كبديل عند التحويل إلى PDF.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

النقاط الرئيسية:
- يتم **تحميل ملف الخط المخصص** `geo_1.ttf` **من القرص**.  
- `usingDefaultFontFromFile` **يحدد الخط الافتراضي من ملف**، مما يضمن أن يستخدم PDF هذا الخط عندما يكون الخط الأصلي مفقودًا.  
- يحافظ ملف PDF الناتج على المظهر المقصود.

### الخطوة 3: الحفظ باستخدام نظام خطوط المستند مع خط افتراضي من تدفق

أحيانًا قد يكون الخط مخزنًا في قاعدة بيانات أو يُستقبل عبر الشبكة. يوضح هذا المثال كيفية **استخدام تدفق خط**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

ما يحدث هنا:
- يتم فتح ملف الخط كـ **InputStream**، وهو مفيد عندما يكون الخط موجودًا في مصدر غير ملف.  
- `usingDefaultFontFromStream` **يستخدم تدفق خط** لتحديد الخط الاحتياطي.  
- يتم حفظ ملف OneNote كـ PDF باستخدام الخط المستند إلى التدفق.

## المشكلات الشائعة والحلول

| المشكلة | لماذا يحدث | كيفية الإصلاح |
|-------|----------------|------------|
| **تحذيرات الخط المفقود** | ملف .one الأصلي يشير إلى خط غير موجود على الجهاز. | قدم خطًا افتراضيًا عبر `usingDefaultFont` أو `usingDefaultFontFromFile` أو `usingDefaultFontFromStream`. |
| **الملف غير موجود للخط المخصص** | مسار ملف `.ttf` غير صحيح. | استخدم مسارات مطلقة أو تحقق من المسار النسبي من دليل العمل. |
| **لم يتم إغلاق التدفق** | يحدث استثناء قبل استدعاء `close()`. | استخدم try‑with‑resources (`try (InputStream stream = ...) { ... }`) للإغلاق التلقائي. |

## الأسئلة المتكررة

**س: هل يمكنني تحديد خطوط مختلفة لأجزاء مختلفة من المستند؟**  
ج: نعم، يمكنك تطبيق إعدادات خط مخصصة على عناصر النص الغنية الفردية باستخدام فئة `Font` في Aspose.Note.

**س: هل Aspose.Note متوافق مع جميع إصدارات OneNote؟**  
ج: تدعم Aspose.Note ملفات OneNote من الإصدارات الحديثة لسطح المكتب والهواتف المحمولة، مما يضمن توافقًا واسعًا.

**س: كيف يمكنني التعامل مع الخطوط المفقودة عند حفظ المستندات؟**  
ج: استخدم طرق نظام الخطوط الموضحة أعلاه (`usingDefaultFont`، `usingDefaultFontFromFile`، `usingDefaultFontFromStream`) لتوفير بديل.

**س: هل يمكنني تخصيص خصائص الخط مثل الحجم والنمط؟**  
ج: بالتأكيد – تتيح لك الواجهة برمجة التطبيقات ضبط الحجم والنمط واللون وغيرها من السمات على أساس كل تشغيل.

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.Note for Java؟**  
ج: نعم، يمكن تنزيل نسخة تجريبية مجانية من موقع Aspose.

## الخلاصة

في هذا البرنامج التعليمي تعلمنا كيفية **حفظ OneNote كملف PDF** مع التحكم في نظام الخطوط في Java باستخدام Aspose.Note. باتباع النهج الثلاثة — تحديد اسم الخط الافتراضي، تحميل ملف خط مخصص، أو استخدام تدفق خط — يمكنك ضمان تمثيل ثابت للخطوط عبر المنصات عند تصدير أو حفظ مستندات OneNote الخاصة بك.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}