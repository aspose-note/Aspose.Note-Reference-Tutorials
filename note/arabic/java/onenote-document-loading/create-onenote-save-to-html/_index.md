---
date: 2026-02-07
description: تعلم كيفية تصدير الخطوط أثناء حفظ OneNote كملف HTML باستخدام Aspose.Note
  للغة Java. يوضح لك هذا الدليل كيفية إنشاء OneNote برمجيًا وإدراج الخطوط وCSS والصور.
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

## المقدمة

في هذا الدرس ستكتشف **كيفية تصدير الخطوط** عندما **تحفظ OneNote كملف HTML** باستخدام Aspose.Note for Java. سنستعرض إنشاء مستند OneNote برمجياً، وتكوين خيارات حفظ HTML، وتضمين ملفات الخطوط المطلوبة بحيث يبدو ملف HTML الناتج مطابقاً تماماً للصفحات الأصلية في OneNote. هذا النهج مثالي عندما تحتاج إلى الحفاظ على الدقة البصرية لمحتوى OneNote في تنسيق صديق للويب.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع التصدير؟** Aspose.Note for Java  
- **هل يمكن تضمين الخطوط في ملف HTML؟** Yes – set `ExportFonts` to `ExportEmbedded`  
- **هل أحتاج إلى ترخيص للإنتاج؟** A valid Aspose.Note license is required for commercial use  
- **ما نسخة Java المدعومة؟** Java 8 or higher  
- **هل من الممكن حفظ الموارد في ملفات منفصلة؟** Absolutely – configure `ResourceExportType` accordingly  

## ما معنى “كيفية تصدير الخطوط” في سياق تحويل OneNote إلى HTML؟

عند تحويل دفتر ملاحظات OneNote إلى HTML، يعتمد المظهر البصري على CSS، الصور، وخاصة الخطوط المستخدمة في الصفحات الأصلية. **تصدير الخطوط** يعني تضمين ملفات الخط (مثل TTF) مباشرةً في حزمة HTML حتى يتمكن المتصفح من عرض النص بنفس الشكل الذي يظهر في OneNote، حتى إذا لم يكن لدى المستخدم النهائي تلك الخطوط مثبتة محليًا.

## لماذا إنشاء OneNote برمجياً وحفظه كملف HTML؟

- **الأتمتة:** توليد تقارير، وثائق، أو مقالات قاعدة معرفة من OneNote دون النسخ واللصق اليدوي.  
- **الاتساق:** الحفاظ على التخطيط، التنسيق، والخطوط المخصصة عبر الأجهزة.  
- **القابلية للنقل:** HTML يمكن عرضه عالمياً—لا حاجة لعميل OneNote.  

## المتطلبات المسبقة

1. Java Development Kit (JDK) 8 أو أحدث مثبت.  
2. مكتبة Aspose.Note for Java – قم بتنزيلها من [هنا](https://releases.aspose.com/note/java/).  
3. ملف OneNote تجريبي (`.one`) للتحميل، أو يمكنك إنشاء ملف جديد برمجياً.  

## استيراد الحزم

First, import the required classes into your Java project:

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

Below is a step‑by‑step guide that shows you **how to export fonts** and other resources.

### الخطوة 1: إنشاء مستند OneNote برمجياً  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

This line loads an existing `.one` file. If you need to **create OneNote programmatically**, you can instantiate a new `Document` object and add sections/pages via the API (not shown here to keep the focus on exporting fonts).

### الخطوة 2: حفظ إلى تدفق الذاكرة مع تضمين الخطوط  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` tells Aspose.Note to **export fonts** directly into the HTML package.  
- `setFontFaceTypes(FontFaceType.Ttf)` ensures TrueType fonts are used, which have broad browser support.

### الخطوة 3: حفظ كملف HTML مع ملفات موارد منفصلة (مع الاستمرار في تصدير الخطوط)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Even though CSS and images are embedded, you can change the `ResourceExportType` to `ExportExternal` if you prefer separate files for easier caching. The key part—**exporting fonts**—remains unchanged.

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

The `UserSavingCallbacks` class (you’ll need to implement `ICssSavingCallback`, `IImageSavingCallback`, and `IFontSavingCallback`) gives you full control over folder structure, allowing you to keep fonts in a dedicated `fonts` directory while still **exporting fonts** correctly.

## كيفية تضمين الخطوط المخصصة عند تحويل OneNote إلى HTML

Embedding custom fonts guarantees that the HTML rendering matches the original OneNote layout, even on devices that don’t have those fonts installed. By using `ExportEmbedded` together with `FontFaceType.Ttf`, the TrueType files are base‑64 encoded and inserted directly into the generated CSS, eliminating the need for external font hosting.

## استخدام ResourceExportType للتحكم في تصدير الموارد

`ResourceExportType` lets you decide whether CSS, images, and fonts are stored **inside** the HTML file (`ExportEmbedded`) or saved as **external** files (`ExportExternal`). Choose `ExportEmbedded` for a single‑file solution, or `ExportExternal` when you want to leverage browser caching for large assets.

## إنشاء OneNote برمجياً لتصدير HTML

If you start from scratch, you can build a OneNote document entirely in code, add sections, pages, and rich text, and then apply the same `HtmlSaveOptions` shown above. This gives you end‑to‑end automation: from data generation to a fully styled HTML output with embedded custom fonts.

## المشكلات الشائعة والنصائح

- **الخطوط المفقودة في الناتج:** Verify that `setExportFonts(ResourceExportType.ExportEmbedded)` is set and that the source OneNote file actually uses embedded fonts.  
- **ملفات HTML الكبيرة:** Embedding fonts can increase size. If bandwidth is a concern, switch `ExportFonts` to `ExportExternal` and host the fonts on a CDN.  
- **أخطاء تنفيذ ردود النداء:** Ensure your callback classes correctly write the stream and close resources to avoid file corruption.  

## الأسئلة المتكررة

**س: هل يمكنني تحويل عدة مستندات OneNote إلى HTML دفعة واحدة؟**  
ج: Yes, loop through each `Document` instance and apply the same `HtmlSaveOptions`.  

**س: هل يدعم Aspose.Note for Java صيغ إخراج أخرى غير HTML؟**  
ج: Absolutely. You can export to PDF, DOCX, PNG, JPEG, and more using the appropriate save options.  

**س: هل تتوفر نسخة تجريبية من Aspose.Note for Java؟**  
ج: Yes, download a free trial from [هنا](https://releases.aspose.com/).  

**س: أين يمكنني الحصول على دعم Aspose.Note for Java؟**  
ج: Visit the [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) for community and official assistance.  

**س: كيف يمكنني شراء ترخيص لـ Aspose.Note for Java؟**  
ج: Licenses are available at the [موقع Aspose](https://purchase.aspose.com/buy).  

## الخلاصة

You now know **how to export fonts** while you **save OneNote as HTML** using Aspose.Note for Java. By configuring `HtmlSaveOptions` and optionally using callbacks, you can preserve the exact look of your OneNote pages—including custom fonts—when delivering them on the web. Feel free to experiment with different `ResourceExportType` settings to suit your project’s performance and storage requirements.

---

**آخر تحديث:** 2026-02-07  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}