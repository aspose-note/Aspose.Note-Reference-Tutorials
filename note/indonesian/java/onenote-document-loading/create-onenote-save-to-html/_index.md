---
date: 2025-12-02
description: Pelajari cara mengekspor font saat Anda menyimpan OneNote sebagai HTML
  menggunakan Aspose.Note untuk Java. Panduan ini menunjukkan cara membuat OneNote
  secara programatis dan menyematkan font, CSS, serta gambar.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Cara Mengekspor Font Saat Menyimpan OneNote sebagai HTML – Java
url: /id/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengekspor Font Saat Menyimpan OneNote sebagai HTML – Java

## Introduction

Dalam tutorial ini Anda akan menemukan **cara mengekspor font** ketika Anda **menyimpan OneNote sebagai HTML** menggunakan Aspose.Note untuk Java. Kami akan memandu Anda membuat dokumen OneNote secara programatis, mengonfigurasi opsi penyimpanan HTML, dan menyematkan file font yang diperlukan sehingga HTML yang dihasilkan terlihat persis seperti halaman OneNote asli. Pendekatan ini sempurna ketika Anda perlu mempertahankan kesetiaan visual konten OneNote dalam format yang ramah web.

## Quick Answers
- **What library handles the export?** Aspose.Note for Java  
- **Can fonts be embedded in the HTML?** Yes – set `ExportFonts` to `ExportEmbedded`  
- **Do I need a license for production?** A valid Aspose.Note license is required for commercial use  
- **Which Java version is supported?** Java 8 or higher  
- **Is it possible to save resources to separate files?** Absolutely – configure `ResourceExportType` accordingly  

## What is “how to export fonts” in the context of OneNote HTML conversion?

Ketika Anda mengonversi notebook OneNote ke HTML, tampilan visual tergantung pada CSS, gambar, dan terutama font yang digunakan di halaman asli. **Mengekspor font** berarti menyematkan file font (misalnya TTF) langsung ke dalam paket HTML sehingga browser dapat merender teks persis seperti yang terlihat di OneNote, bahkan jika pengguna akhir tidak memiliki font tersebut terpasang secara lokal.

## Why create OneNote programmatically and save it as HTML?

- **Automation:** Menghasilkan laporan, dokumentasi, atau artikel basis pengetahuan dari OneNote tanpa menyalin‑tempel manual.  
- **Consistency:** Mempertahankan tata letak, gaya, dan font khusus di semua perangkat.  
- **Portability:** HTML dapat dilihat secara universal—tidak memerlukan klien OneNote.  

## Prerequisites

1. Java Development Kit (JDK) 8 atau yang lebih baru terpasang.  
2. Perpustakaan Aspose.Note untuk Java – unduh dari [here](https://releases.aspose.com/note/java/).  
3. File OneNote contoh (`.one`) untuk dimuat, atau Anda dapat membuat file baru secara programatis.  

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

Baris ini memuat file `.one` yang sudah ada. Jika Anda perlu **membuat OneNote secara programatis**, Anda dapat menginstansiasi objek `Document` baru dan menambahkan bagian/halaman melalui API (tidak ditampilkan di sini untuk menjaga fokus pada mengekspor font).

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

- `setExportFonts(ResourceExportType.ExportEmbedded)` memberi tahu Aspose.Note untuk **mengekspor font** langsung ke dalam paket HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` memastikan font TrueType yang digunakan, yang memiliki dukungan luas di browser.

### Step 3: Save as HTML with separate resource files (still exporting fonts)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Meskipun CSS dan gambar disematkan, Anda dapat mengubah `ResourceExportType` menjadi `ExportExternal` jika lebih suka file terpisah untuk caching yang lebih mudah. Bagian penting—**mengekspor font**—tetap tidak berubah.

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

Kelas `UserSavingCallbacks` (Anda perlu mengimplementasikan `ICssSavingCallback`, `IImageSavingCallback`, dan `IFontSavingCallback`) memberi Anda kontrol penuh atas struktur folder, memungkinkan Anda menyimpan font dalam direktori `fonts` khusus sambil tetap **mengekspor font** dengan benar.

## Common Issues & Tips

- **Missing fonts in the output:** Verify that `setExportFonts(ResourceExportType.ExportEmbedded)` is set and that the source OneNote file actually uses embedded fonts.  
- **Large HTML files:** Embedding fonts can increase size. If bandwidth is a concern, switch `ExportFonts` to `ExportExternal` and host the fonts on a CDN.  
- **Callback implementation errors:** Ensure your callback classes correctly write the stream and close resources to avoid file corruption.  

## Frequently Asked Questions

**Q: Can I convert multiple OneNote documents to HTML in one go?**  
A: Yes, loop through each `Document` instance and apply the same `HtmlSaveOptions`.  

**Q: Does Aspose.Note for Java support other output formats besides HTML?**  
A: Absolutely. You can export to PDF, DOCX, PNG, JPEG, and more using the appropriate save options.  

**Q: Is there a trial version available for Aspose.Note for Java?**  
A: Yes, download a free trial from [here](https://releases.aspose.com/).  

**Q: Where can I get support for Aspose.Note for Java?**  
A: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for community and official assistance.  

**Q: How can I purchase a license for Aspose.Note for Java?**  
A: Licenses are available at the [Aspose website](https://purchase.aspose.com/buy).  

## Conclusion

You now know **how to export fonts** while you **save OneNote as HTML** using Aspose.Note for Java. By configuring `HtmlSaveOptions` and optionally using callbacks, you can preserve the exact look of your OneNote pages—including custom fonts—when delivering them on the web. Feel free to experiment with different `ResourceExportType` settings to suit your project’s performance and storage requirements.

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}