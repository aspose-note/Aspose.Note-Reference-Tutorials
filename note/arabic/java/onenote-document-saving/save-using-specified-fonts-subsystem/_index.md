---
title: حفظ باستخدام النظام الفرعي للخطوط المحددة في OneNote
linktitle: حفظ باستخدام النظام الفرعي للخطوط المحددة في OneNote
second_title: Aspose.Note جافا API
description: تعرف على كيفية حفظ مستندات OneNote باستخدام النظام الفرعي للخطوط المحددة في Java باستخدام Aspose.Note. ضمان تمثيل الخطوط المتسق عبر الأنظمة الأساسية دون عناء.
type: docs
weight: 22
url: /ar/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---
## مقدمة

يوفر Aspose.Note for Java إمكانات قوية للعمل مع مستندات OneNote. أحد المتطلبات الشائعة عند العمل مع مثل هذه المستندات هو التأكد من الحفاظ على الخطوط بشكل صحيح، خاصة إذا كان المستند سيتم تصديره أو حفظه بتنسيقات مختلفة مثل PDF. سيرشدك هذا البرنامج التعليمي خلال عملية حفظ مستندات OneNote مع تحديد النظام الفرعي للخطوط، مما يضمن تمثيلًا متسقًا ودقيقًا للنص عبر الأنظمة الأساسية المختلفة.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من إعداد المتطلبات الأساسية التالية:

### 1. مجموعة تطوير جافا (JDK)

 تأكد من تثبيت Java Development Kit (JDK) على نظامك. يمكنك تنزيله من[هنا](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) إذا لم تكن قد فعلت ذلك بالفعل.

### 2. Aspose.Note لمكتبة جافا

 قم بتنزيل وإعداد Aspose.Note لمكتبة Java. يمكنك تنزيله من[موقع إلكتروني](https://releases.aspose.com/note/java/).

## حزم الاستيراد

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

الآن دعونا نقسم كل مثال إلى خطوات متعددة لفهم العملية بشكل أفضل.

## الخطوة 1: الحفظ باستخدام النظام الفرعي لخطوط المستندات مع اسم الخط الافتراضي

توضح هذه الخطوة كيفية حفظ مستند بتنسيق PDF باستخدام اسم خط افتراضي محدد.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // تحديد الخط الافتراضي.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // احفظ المستند بصيغة PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

في هذه الخطوة:
- يتم تحميل مستند OneNote باستخدام Aspose.Note.
- يتم تحديد الخط الافتراضي كـ "Times New Roman".
- يتم حفظ المستند بتنسيق PDF بالخط المحدد.

## الخطوة 2: الحفظ باستخدام النظام الفرعي لخطوط المستندات مع الخط الافتراضي من الملف

توضح هذه الخطوة كيفية حفظ مستند بتنسيق PDF باستخدام الخط الافتراضي الذي تم تحميله من الملف.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // حدد المسار إلى ملف الخط.
    String fontFile = "geo_1.ttf";

    // حدد الخط الافتراضي من الملف.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // احفظ المستند بصيغة PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

في هذه الخطوة:
- تم تحميل ملف الخط "geo_1.ttf".
- يتم تحديد الخط الافتراضي من ملف الخط الذي تم تحميله.
- يتم حفظ المستند بتنسيق PDF بالخط المحدد.

## الخطوة 3: الحفظ باستخدام النظام الفرعي لخطوط المستندات مع الخط الافتراضي من الدفق

توضح هذه الخطوة كيفية حفظ مستند بتنسيق PDF باستخدام خط افتراضي تم تحميله من الدفق.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // قم بتحميل المستند إلى Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // حدد المسار إلى ملف الخط.
    String fontFile = "geo_1.ttf";

    // قم بتحميل ملف الخط كدفق.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // حدد الخط الافتراضي من الدفق.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // احفظ المستند بصيغة PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

في هذه الخطوة:
- يتم تحميل ملف الخط "geo_1.ttf" كدفق.
- يتم تحديد الخط الافتراضي من الدفق المحمل.
- يتم حفظ المستند بتنسيق PDF بالخط المحدد.

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية حفظ مستندات OneNote باستخدام النظام الفرعي للخطوط المحددة في Java باستخدام Aspose.Note. باتباع هذه الخطوات، يمكنك ضمان تمثيل الخط بشكل متسق عبر الأنظمة الأساسية المختلفة عند تصدير مستنداتك أو حفظها.

## الأسئلة الشائعة

### س1: هل يمكنني تحديد خطوط مختلفة لأجزاء مختلفة من المستند؟

ج1: نعم، يمكنك تحديد خطوط مختلفة لأجزاء مختلفة من المستند باستخدام Aspose.Note لـ Java.

### س2: هل Aspose.Note متوافق مع كافة إصدارات OneNote؟

ج2: يدعم Aspose.Note إصدارات مختلفة من OneNote، مما يضمن التوافق عبر بيئات مختلفة.

### س3: كيف يمكنني التعامل مع الخطوط المفقودة عند حفظ المستندات؟

A3: يوفر Aspose.Note خيارات لتحديد الخطوط الافتراضية للتعامل مع الخطوط المفقودة بشكل فعال أثناء حفظ المستند.

### س 4: هل يمكنني تخصيص خصائص الخط مثل الحجم والنمط؟

ج4: نعم، يمكنك تخصيص خصائص الخط مثل الحجم والنمط واللون باستخدام Aspose.Note لـ Java.

### س5: هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ Java؟

ج5: نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Note لـ Java من موقع الويب.