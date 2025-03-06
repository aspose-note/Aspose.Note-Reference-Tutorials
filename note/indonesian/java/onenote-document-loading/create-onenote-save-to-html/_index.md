---
title: Buat Dokumen OneNote dan Simpan ke HTML - Java
linktitle: Buat Dokumen OneNote dan Simpan ke HTML - Java
second_title: Aspose.Catatan Java API
description: Pelajari cara membuat dan menyimpan dokumen OneNote sebagai HTML menggunakan Aspose.Note untuk Java. Integrasikan ke dalam aplikasi Java untuk penanganan file OneNote terprogram.

weight: 18
url: /id/java/onenote-document-loading/create-onenote-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat Dokumen OneNote dan Simpan ke HTML - Java

## Perkenalan

Aspose.Note untuk Java adalah perpustakaan canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram. Dalam tutorial ini, kita akan mempelajari cara membuat dokumen OneNote dan menyimpannya ke format HTML menggunakan Aspose.Note untuk Java.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1. Java Development Kit (JDK) diinstal pada sistem Anda.
2.  Aspose.Note untuk perpustakaan Java. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/java/).
3. Pengetahuan dasar tentang pemrograman Java.

## Paket Impor

Pertama, impor paket yang diperlukan ke proyek Java Anda:

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

## Langkah 1: Buat Objek Dokumen OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Kode ini menginisialisasi a`Document` objek dengan memuat contoh file OneNote.

## Langkah 2: Simpan sebagai HTML ke Memory Stream

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Di sini, kami menyiapkan opsi penyimpanan HTML dan menyimpan dokumen ke aliran memori.

## Langkah 3: Simpan sebagai HTML dengan Sumber Daya di File Terpisah

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Langkah ini menyimpan dokumen sebagai HTML dengan sumber daya seperti CSS, font, dan gambar dalam file terpisah.

## Langkah 4: Simpan sebagai HTML ke Memory Stream dengan Callback untuk Menghemat Sumber Daya

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

Di sini, kami menyimpan dokumen sebagai HTML ke aliran memori menggunakan callback untuk menangani penghematan sumber daya.

## Kesimpulan

Selamat! Anda telah mempelajari cara membuat dokumen OneNote dan menyimpannya ke format HTML menggunakan Aspose.Note untuk Java. Anda sekarang dapat mengintegrasikan fungsi ini ke dalam aplikasi Java Anda untuk bekerja dengan file OneNote secara terprogram.

## FAQ

### Q1: Bisakah saya mengonversi beberapa dokumen OneNote ke HTML sekaligus?

A1: Ya, Anda dapat mengulang beberapa dokumen dan menerapkan proses penyimpanan secara berulang.

### Q2: Apakah Aspose.Note untuk Java mendukung format output lain selain HTML?

A2: Ya, Aspose.Note untuk Java mendukung berbagai format output termasuk PDF, DOCX, dan format gambar.

### Q3: Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?

A3: Ya, Anda dapat mengunduh versi uji coba gratis dari[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya bisa mendapatkan dukungan untuk Aspose.Note untuk Java?

 A4: Anda bisa mendapatkan dukungan dari[Aspose.Catatan forum](https://forum.aspose.com/c/note/28).

### Q5: Bagaimana cara membeli lisensi Aspose.Note untuk Java?

 A5: Anda dapat membeli lisensi dari[Asumsikan situs web](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
