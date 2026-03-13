---
date: 2026-02-07
description: Aspose.Note for Java kullanarak OneNote’u HTML olarak kaydederken yazı
  tiplerini nasıl dışa aktaracağınızı öğrenin. Bu kılavuz, OneNote’u programlı olarak
  nasıl oluşturacağınızı ve yazı tiplerini, CSS’i ve görüntüleri nasıl gömeceğinizi
  gösterir.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: OneNote'i HTML Olarak Kaydederken Yazı Tiplerini Nasıl Dışa Aktarılır – Java
url: /tr/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'i HTML Olarak Kaydederken Yazı Tiplerini Nasıl Dışa Aktarılır – Java

## Introduction

Bu öğreticide **OneNote'i HTML olarak kaydederken** **yazı tiplerini nasıl dışa aktaracağınızı** Aspose.Note for Java kullanarak keşfedeceksiniz. Programlı olarak bir OneNote belgesi oluşturmayı, HTML kaydetme seçeneklerini yapılandırmayı ve gerekli yazı tipi dosyalarını gömerek ortaya çıkan HTML'nin orijinal OneNote sayfalarıyla aynı göründüğünden emin olacağız. Bu yaklaşım, OneNote içeriğinin görsel bütünlüğünü web‑dostu bir formatta korumanız gerektiğinde mükemmeldir.

## Quick Answers
- **Dışa aktarmayı hangi kütüphane yönetir?** Aspose.Note for Java  
- **Yazı tipleri HTML'e gömülebilir mi?** Evet – `ExportFonts` özelliğini `ExportEmbedded` olarak ayarlayın  
- **Üretim için lisansa ihtiyacım var mı?** Ticari kullanım için geçerli bir Aspose.Note lisansı gereklidir  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri  
- **Kaynakları ayrı dosyalara kaydetmek mümkün mü?** Kesinlikle – `ResourceExportType`'ı buna göre yapılandırın  

## What is “how to export fonts” in the context of OneNote HTML conversion?

OneNote defterini HTML'e dönüştürdüğünüzde görsel görünüm CSS, görüntüler ve özellikle orijinal sayfalarda kullanılan yazı tiplerine bağlıdır. **Yazı tiplerini dışa aktarmak**, yazı tipi dosyalarını (ör. TTF) doğrudan HTML paketine gömmek anlamına gelir; böylece tarayıcılar, son kullanıcı bu yazı tiplerini yerel olarak yüklü olmasa bile metni OneNote'ta göründüğü gibi render eder.

## Why create OneNote programmatically and save it as HTML?

- **Otomasyon:** OneNote'den raporlar, belgeler veya bilgi‑tabanı makaleleri manuel kopyala‑yapıştırma yapmadan oluşturun.  
- **Tutarlılık:** Düzen, stil ve özel yazı tiplerini cihazlar arasında koruyun.  
- **Taşınabilirlik:** HTML evrensel olarak görüntülenebilir—OneNote istemcisine gerek yok.  

## Prerequisites

1. Java Development Kit (JDK) 8 veya daha yeni bir sürüm kurulu.  
2. Aspose.Note for Java kütüphanesi – [buradan](https://releases.aspose.com/note/java/) indirin.  
3. Yüklemek için bir örnek OneNote dosyası (`.one`) ya da programlı olarak yeni bir dosya oluşturabilirsiniz.  

## Import Packages

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

## How to Export Fonts While Saving OneNote as HTML?

Below is a step‑by‑step guide that shows you **how to export fonts** and other resources.

### Step 1: Create a OneNote document programmatically  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

This line loads an existing `.one` file. If you need to **create OneNote programmatically**, you can instantiate a new `Document` object and add sections/pages via the API (not shown here to keep the focus on exporting fonts).

### Step 2: Save to a memory stream with embedded fonts  

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

### Step 3: Save as HTML with separate resource files (still exporting fonts)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Even though CSS and images are embedded, you can change the `ResourceExportType` to `ExportExternal` if you prefer separate files for easier caching. The key part—**exporting fonts**—remains unchanged.

### Step 4: Use callbacks to control where each resource is stored  

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

## How to embed custom fonts when converting OneNote to HTML

Embedding custom fonts guarantees that the HTML rendering matches the original OneNote layout, even on devices that don’t have those fonts installed. By using `ExportEmbedded` together with `FontFaceType.Ttf`, the TrueType files are base‑64 encoded and inserted directly into the generated CSS, eliminating the need for external font hosting.

## Using ResourceExportType to control resource export

`ResourceExportType` lets you decide whether CSS, images, and fonts are stored **inside** the HTML file (`ExportEmbedded`) or saved as **external** files (`ExportExternal`). Choose `ExportEmbedded` for a single‑file solution, or `ExportExternal` when you want to leverage browser caching for large assets.

## Creating OneNote programmatically for HTML export

If you start from scratch, you can build a OneNote document entirely in code, add sections, pages, and rich text, and then apply the same `HtmlSaveOptions` shown above. This gives you end‑to‑end automation: from data generation to a fully styled HTML output with embedded custom fonts.

## Common Issues & Tips

- **Çıktıda eksik yazı tipleri:** `setExportFonts(ResourceExportType.ExportEmbedded)` ayarlandığını ve kaynak OneNote dosyasının gerçekten gömülü yazı tipleri kullandığını doğrulayın.  
- **Büyük HTML dosyaları:** Yazı tiplerini gömmek dosya boyutunu artırabilir. Bant genişliği bir sorun ise `ExportFonts`'u `ExportExternal` olarak değiştirin ve yazı tiplerini bir CDN'de barındırın.  
- **Geri çağırma (callback) uygulama hataları:** Geri çağırma sınıflarınızın akışı doğru yazdığından ve kaynakları kapattığından emin olun, aksi takdirde dosya bozulabilir.  

## Frequently Asked Questions

**Q: Birden fazla OneNote belgesini tek seferde HTML'e dönüştürebilir miyim?**  
A: Evet, her `Document` örneği üzerinden döngü kurarak aynı `HtmlSaveOptions`'ı uygulayabilirsiniz.  

**Q: Aspose.Note for Java, HTML dışındaki diğer çıktı formatlarını destekliyor mu?**  
A: Kesinlikle. Uygun kaydetme seçeneklerini kullanarak PDF, DOCX, PNG, JPEG ve daha fazlasına dışa aktarabilirsiniz.  

**Q: Aspose.Note for Java için deneme sürümü mevcut mu?**  
A: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.  

**Q: Aspose.Note for Java için destek nereden alınabilir?**  
A: Topluluk ve resmi yardım için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin.  

**Q: Aspose.Note for Java lisansı nasıl satın alınır?**  
A: Lisanslar, [Aspose web sitesinde](https://purchase.aspose.com/buy) mevcuttur.  

## Conclusion

You now know **how to export fonts** while you **save OneNote as HTML** using Aspose.Note for Java. By configuring `HtmlSaveOptions` and optionally using callbacks, you can preserve the exact look of your OneNote pages—including custom fonts—when delivering them on the web. Feel free to experiment with different `ResourceExportType` settings to suit your project’s performance and storage requirements.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}