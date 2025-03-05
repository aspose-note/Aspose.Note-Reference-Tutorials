---
title: إنشاء مستند OneNote وحفظه في HTML - Java
linktitle: إنشاء مستند OneNote وحفظه في HTML - Java
second_title: Aspose.Note جافا API
description: تعرّف على كيفية إنشاء مستندات OneNote وحفظها بتنسيق HTML باستخدام Aspose.Note لـ Java. التكامل مع تطبيقات Java للتعامل البرمجي مع ملفات OneNote.

type: docs
weight: 18
url: /ar/java/onenote-document-loading/create-onenote-save-to-html/
---
## مقدمة

Aspose.Note for Java هي مكتبة قوية تتيح للمطورين العمل مع ملفات Microsoft OneNote برمجياً. في هذا البرنامج التعليمي، سنستكشف كيفية إنشاء مستند OneNote وحفظه بتنسيق HTML باستخدام Aspose.Note لـ Java.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1. تم تثبيت Java Development Kit (JDK) على نظامك.
2.  Aspose.Note لمكتبة جافا. يمكنك تنزيله من[هنا](https://releases.aspose.com/note/java/).
3. المعرفة الأساسية ببرمجة جافا.

## حزم الاستيراد

أولاً، قم باستيراد الحزم اللازمة لمشروع Java الخاص بك:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## الخطوة 1: إنشاء كائن مستند OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 يقوم هذا الرمز بتهيئة أ`Document` الكائن عن طريق تحميل نموذج ملف OneNote.

## الخطوة 2: احفظ بتنسيق HTML في Memory Stream

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

هنا، نقوم بإعداد خيارات حفظ HTML وحفظ المستند في دفق الذاكرة.

## الخطوة 3: احفظ بتنسيق HTML مع الموارد في ملفات منفصلة

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

تقوم هذه الخطوة بحفظ المستند بتنسيق HTML مع موارد مثل CSS والخطوط والصور في ملفات منفصلة.

## الخطوة 4: احفظ بتنسيق HTML في Memory Stream مع عمليات الاسترجاعات لحفظ الموارد

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

هنا، نقوم بحفظ المستند بتنسيق HTML في دفق الذاكرة باستخدام عمليات الاسترجاعات للتعامل مع توفير الموارد.

## خاتمة

تهانينا! لقد تعلمت كيفية إنشاء مستند OneNote وحفظه بتنسيق HTML باستخدام Aspose.Note لـ Java. يمكنك الآن دمج هذه الوظيفة في تطبيقات Java الخاصة بك للعمل مع ملفات OneNote برمجياً.

## الأسئلة الشائعة

### س1: هل يمكنني تحويل عدة مستندات OneNote إلى HTML دفعة واحدة؟

A1: نعم، يمكنك تنفيذ حلقات عبر مستندات متعددة وتطبيق عملية الحفظ بشكل متكرر.

### س2: هل يدعم Aspose.Note for Java تنسيقات الإخراج الأخرى إلى جانب HTML؟

ج2: نعم، يدعم Aspose.Note for Java تنسيقات الإخراج المختلفة بما في ذلك تنسيقات PDF وDOCX وتنسيقات الصور.

### س3: هل هناك إصدار تجريبي متاح لـ Aspose.Note لـ Java؟

ج3: نعم، يمكنك تنزيل نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).

### س4: أين يمكنني الحصول على الدعم لـ Aspose.Note لـ Java؟

 ج4: يمكنك الحصول على الدعم من[منتدى Aspose.Note](https://forum.aspose.com/c/note/28).

### س5: كيف يمكنني شراء ترخيص Aspose.Note لـ Java؟

 ج5: يمكنك شراء ترخيص من[موقع أسبوز](https://purchase.aspose.com/buy).