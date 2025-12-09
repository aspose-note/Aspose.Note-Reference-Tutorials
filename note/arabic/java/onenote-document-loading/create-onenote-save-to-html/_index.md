---
date: 2025-12-02
description: تعلم كيفية تصدير الخطوط أثناء حفظ OneNote كملف HTML باستخدام Aspose.Note
  للغة Java. يوضح لك هذا الدليل كيفية إنشاء OneNote برمجيًا وتضمين الخطوط وCSS والصور.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: كيفية تصدير الخطوط عند حفظ OneNote كملف HTML – Java
url: /ar/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تصدير الخطوط عند حفظ OneNote كملف HTML – Java

## مقدمة

في هذا الدرس ستكتشف **كيفية تصدير الخطوط** عندما **تحفظ OneNote كملف HTML** باستخدام Aspose.Note for Java. سنستعرض إنشاء مستند OneNote برمجياً، تكوين خيارات حفظ HTML، وتضمين ملفات الخطوط المطلوبة بحيث يبدو ملف HTML الناتج مطابقاً تماماً للصفحات الأصلية في OneNote. هذا النهج مثالي عندما تحتاج إلى الحفاظ على الدقة البصرية لمحتوى OneNote في صيغة صديقة للويب.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع التصدير؟** Aspose.Note for Java  
- **هل يمكن تضمين الخطوط في ملف HTML؟** نعم – اضبط `ExportFonts` إلى `ExportEmbedded`  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يلزم وجود ترخيص Aspose.Note صالح للاستخدام التجاري  
- **ما نسخة Java المدعومة؟** Java 8 أو أعلى  
- **هل من الممكن حفظ الموارد في ملفات منفصلة؟** بالتأكيد – اضبط `ResourceExportType` وفقاً لذلك  

## ما هو “كيفية تصدير الخطوط” في سياق تحويل OneNote إلى HTML؟

عند تحويل دفتر ملاحظات OneNote إلى HTML، يعتمد المظهر البصري على CSS، الصور، وخاصة الخطوط المستخدمة في الصفحات الأصلية. **تصدير الخطوط** يعني تضمين ملفات الخط (مثل TTF) مباشرةً في حزمة HTML حتى يتمكن المتصفح من عرض النص كما هو في OneNote، حتى إذا لم يكن لدى المستخدم النهائي تلك الخطوط مثبتة محلياً.

## لماذا إنشاء OneNote برمجياً وحفظه كملف HTML؟

- **الأتمتة:** إنشاء تقارير، وثائق، أو مقالات قاعدة معرفة من OneNote دون الحاجة إلى النسخ واللصق اليدوي.  
- **الاتساق:** الحفاظ على التخطيط، الأنماط، والخطوط المخصصة عبر الأجهزة.  
- **القابلية للنقل:** HTML يمكن عرضه على أي جهاز—لا حاجة إلى عميل OneNote.  

## المتطلبات المسبقة

1. مجموعة تطوير جافا (JDK) 8 أو أحدث مثبتة.  
2. مكتبة Aspose.Note for Java – حمّلها من [هنا](https://releases.aspose.com/note/java/).  
3. ملف OneNote تجريبي (`.one`) للتحميل، أو يمكنك إنشاء ملف جديد برمجياً.  

## استيراد الحزم

أولاً، استورد الفئات المطلوبة في مشروع Java الخاص بك:

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

## كيفية تصدير الخطوط أثناء حفظ OneNote كملف HTML؟

فيما يلي دليل خطوة بخطوة يوضح لك **كيفية تصدير الخطوط** وغيرها من الموارد.

### الخطوة 1: إنشاء مستند OneNote برمجياً  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

هذا السطر يحمل ملف `.one` موجود. إذا كنت بحاجة إلى **إنشاء OneNote برمجياً**، يمكنك إنشاء كائن `Document` جديد وإضافة أقسام/صفحات عبر الـ API (لم يتم عرض ذلك هنا لتبسيط التركيز على تصدير الخطوط).

### الخطوة 2: حفظ إلى تدفق الذاكرة مع الخطوط المدمجة  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` يخبر Aspose.Note بـ **تصدير الخطوط** مباشرةً إلى حزمة HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` يضمن استخدام خطوط TrueType، التي تحظى بدعم واسع في المتصفحات.

### الخطوة 3: حفظ كملف HTML مع ملفات موارد منفصلة (مع الاستمرار في تصدير الخطوط)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

على الرغم من أن CSS والصور مدمجة، يمكنك تغيير `ResourceExportType` إلى `ExportExternal` إذا فضلت ملفات منفصلة لتسهيل التخزين المؤقت. الجزء الأساسي—**تصدير الخطوط**—يبقى دون تغيير.

### الخطوة 4: استخدام ردود النداء للتحكم في مكان تخزين كل مورد  

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

فئة `UserSavingCallbacks` (ستحتاج إلى تنفيذ `ICssSavingCallback`، `IImageSavingCallback`، و `IFontSavingCallback`) تمنحك التحكم الكامل في بنية المجلدات، مما يسمح لك بوضع الخطوط في دليل `fonts` مخصص مع **تصدير الخطوط** بشكل صحيح.

## مشكلات شائعة ونصائح

- **الخطوط مفقودة في الناتج:** تأكد من ضبط `setExportFonts(ResourceExportType.ExportEmbedded)` وأن ملف OneNote المصدر يستخدم خطوطاً مدمجة فعلياً.  
- **ملفات HTML كبيرة:** تضمين الخطوط قد يزيد الحجم. إذا كانت النطاق الترددي مصدر قلق، غيّر `ExportFonts` إلى `ExportExternal` واستضيف الخطوط على CDN.  
- **أخطاء تنفيذ ردود النداء:** تأكد من أن فئات رد النداء تكتب التيار وتغلق الموارد بشكل صحيح لتجنب فساد الملفات.  

## الأسئلة المتكررة

**س: هل يمكنني تحويل عدة مستندات OneNote إلى HTML دفعة واحدة؟**  
ج: نعم، قم بالتكرار عبر كل كائن `Document` وطبق نفس `HtmlSaveOptions`.  

**س: هل تدعم Aspose.Note for Java صيغ إخراج أخرى غير HTML؟**  
ج: بالتأكيد. يمكنك التصدير إلى PDF، DOCX، PNG، JPEG، والمزيد باستخدام خيارات الحفظ المناسبة.  

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.Note for Java؟**  
ج: نعم، حمّل نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).  

**س: أين يمكنني الحصول على الدعم لـ Aspose.Note for Java؟**  
ج: زر [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على مساعدة المجتمع والرسمية.  

**س: كيف يمكنني شراء ترخيص لـ Aspose.Note for Java؟**  
ج: الترخيص متاح عبر [موقع Aspose](https://purchase.aspose.com/buy).  

## الخلاصة

أنت الآن تعرف **كيفية تصدير الخطوط** أثناء **حفظ OneNote كملف HTML** باستخدام Aspose.Note for Java. من خلال تكوين `HtmlSaveOptions` واستخدام ردود النداء إذا لزم الأمر، يمكنك الحفاظ على المظهر الدقيق لصفحات OneNote—including الخطوط المخصصة—عند تقديمها على الويب. لا تتردد في تجربة إعدادات `ResourceExportType` المختلفة لتناسب متطلبات الأداء والتخزين في مشروعك.

---

**آخر تحديث:** 2025-12-02  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}