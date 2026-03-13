---
date: 2026-02-07
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

## Pendahuluan

Dalam tutorial ini Anda akan menemukan **cara mengekspor font** ketika Anda **menyimpan OneNote sebagai HTML** menggunakan Aspose.Note untuk Java. Kami akan memandu Anda membuat dokumen OneNote secara programatis, mengonfigurasi opsi penyimpanan HTML, dan menyematkan file font yang diperlukan sehingga HTML yang dihasilkan terlihat persis seperti halaman OneNote asli. Pendekatan ini sempurna ketika Anda perlu mempertahankan kesetiaan visual konten OneNote dalam format yang ramah web.

## Jawaban Cepat
- **Apa perpustakaan yang menangani ekspor?** Aspose.Note untuk Java  
- **Apakah font dapat disematkan dalam HTML?** Ya – atur `ExportFonts` ke `ExportEmbedded`  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi Aspose.Note yang valid diperlukan untuk penggunaan komersial  
- **Versi Java mana yang didukung?** Java 8 atau lebih tinggi  
- **Apakah memungkinkan menyimpan sumber daya ke file terpisah?** Tentu – konfigurasikan `ResourceExportType` sesuai  

## Apa itu “cara mengekspor font” dalam konteks konversi HTML OneNote?

Ketika Anda mengonversi notebook OneNote ke HTML, tampilan visual bergantung pada CSS, gambar, dan terutama font yang digunakan pada halaman asli. **Mengekspor font** berarti menyematkan file font (misalnya, TTF) langsung ke dalam paket HTML sehingga peramban dapat merender teks persis seperti yang terlihat di OneNote, bahkan jika pengguna akhir tidak memiliki font tersebut terpasang secara lokal.

## Mengapa membuat OneNote secara programatis dan menyimpannya sebagai HTML?

- **Otomatisasi:** Menghasilkan laporan, dokumentasi, atau artikel basis pengetahuan dari OneNote tanpa menyalin‑tempel secara manual.  
- **Konsistensi:** Mempertahankan tata letak, gaya, dan font khusus di semua perangkat.  
- **Portabilitas:** HTML dapat dilihat secara universal—tidak memerlukan klien OneNote.  

## Prasyarat

1. Java Development Kit (JDK) 8 atau yang lebih baru terpasang.  
2. Perpustakaan Aspose.Note untuk Java – unduh dari [di sini](https://releases.aspose.com/note/java/).  
3. File OneNote contoh (`.one`) untuk dimuat, atau Anda dapat membuat yang baru secara programatis.  

## Impor Paket

Pertama, impor kelas yang diperlukan ke dalam proyek Java Anda:

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

## Cara Mengekspor Font Saat Menyimpan OneNote sebagai HTML?

Berikut adalah panduan langkah‑demi‑langkah yang menunjukkan **cara mengekspor font** dan sumber daya lainnya.

### Langkah 1: Buat dokumen OneNote secara programatis  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Baris ini memuat file `.one` yang ada. Jika Anda perlu **membuat OneNote secara programatis**, Anda dapat menginstansiasi objek `Document` baru dan menambahkan bagian/halaman melalui API (tidak ditampilkan di sini untuk menjaga fokus pada mengekspor font).

### Langkah 2: Simpan ke aliran memori dengan font yang disematkan  

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
- `setFontFaceTypes(FontFaceType.Ttf)` memastikan font TrueType digunakan, yang memiliki dukungan luas di peramban.

### Langkah 3: Simpan sebagai HTML dengan file sumber daya terpisah (tetap mengekspor font)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Meskipun CSS dan gambar disematkan, Anda dapat mengubah `ResourceExportType` menjadi `ExportExternal` jika lebih suka file terpisah untuk caching yang lebih mudah. Bagian kunci—**mengekspor font**—tetap tidak berubah.

### Langkah 4: Gunakan callback untuk mengontrol tempat penyimpanan setiap sumber daya  

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

Kelas `UserSavingCallbacks` (Anda perlu mengimplementasikan `ICssSavingCallback`, `IImageSavingCallback`, dan `IFontSavingCallback`) memberi Anda kontrol penuh atas struktur folder, memungkinkan Anda menyimpan font di direktori `fonts` khusus sambil tetap **mengekspor font** dengan benar.

## Cara menyematkan font khusus saat mengonversi OneNote ke HTML

Menambahkan font khusus memastikan bahwa rendering HTML cocok dengan tata letak OneNote asli, bahkan pada perangkat yang tidak memiliki font tersebut terpasang. Dengan menggunakan `ExportEmbedded` bersama `FontFaceType.Ttf`, file TrueType di‑encode base‑64 dan disisipkan langsung ke dalam CSS yang dihasilkan, menghilangkan kebutuhan hosting font eksternal.

## Menggunakan ResourceExportType untuk mengontrol ekspor sumber daya

`ResourceExportType` memungkinkan Anda memutuskan apakah CSS, gambar, dan font disimpan **di dalam** file HTML (`ExportEmbedded`) atau disimpan sebagai file **eksternal** (`ExportExternal`). Pilih `ExportEmbedded` untuk solusi satu‑file, atau `ExportExternal` ketika Anda ingin memanfaatkan caching peramban untuk aset berukuran besar.

## Membuat OneNote secara programatis untuk ekspor HTML

Jika Anda memulai dari nol, Anda dapat membangun dokumen OneNote sepenuhnya dalam kode, menambahkan bagian, halaman, dan teks kaya, lalu menerapkan `HtmlSaveOptions` yang sama seperti di atas. Ini memberi Anda otomasi end‑to‑end: dari generasi data hingga output HTML yang sepenuhnya bergaya dengan font khusus yang disematkan.

## Masalah Umum & Tips

- **Font hilang dalam output:** Pastikan `setExportFonts(ResourceExportType.ExportEmbedded)` telah diatur dan file OneNote sumber memang menggunakan font yang disematkan.  
- **File HTML besar:** Menyematkan font dapat meningkatkan ukuran. Jika bandwidth menjadi masalah, ubah `ExportFonts` menjadi `ExportExternal` dan host font di CDN.  
- **Kesalahan implementasi callback:** Pastikan kelas callback Anda menulis aliran dengan benar dan menutup sumber daya untuk menghindari korupsi file.  

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya mengonversi beberapa dokumen OneNote ke HTML sekaligus?**  
J: Ya, iterasi setiap instance `Document` dan terapkan `HtmlSaveOptions` yang sama.  

**T: Apakah Aspose.Note untuk Java mendukung format output lain selain HTML?**  
J: Tentu. Anda dapat mengekspor ke PDF, DOCX, PNG, JPEG, dan lainnya menggunakan opsi penyimpanan yang sesuai.  

**T: Apakah ada versi percobaan yang tersedia untuk Aspose.Note untuk Java?**  
J: Ya, unduh percobaan gratis dari [di sini](https://releases.aspose.com/).  

**T: Di mana saya dapat mendapatkan dukungan untuk Aspose.Note untuk Java?**  
J: Kunjungi [forum Aspose.Note](https://forum.aspose.com/c/note/28) untuk bantuan komunitas dan resmi.  

**T: Bagaimana cara membeli lisensi untuk Aspose.Note untuk Java?**  
J: Lisensi tersedia di [situs Aspose](https://purchase.aspose.com/buy).  

## Kesimpulan

Anda kini mengetahui **cara mengekspor font** saat Anda **menyimpan OneNote sebagai HTML** menggunakan Aspose.Note untuk Java. Dengan mengonfigurasi `HtmlSaveOptions` dan secara opsional menggunakan callback, Anda dapat mempertahankan tampilan persis halaman OneNote Anda—termasuk font khusus—ketika menyajikannya di web. Jangan ragu untuk bereksperimen dengan pengaturan `ResourceExportType` yang berbeda untuk menyesuaikan kebutuhan kinerja dan penyimpanan proyek Anda.

---

**Terakhir Diperbarui:** 2026-02-07  
**Diuji Dengan:** Aspose.Note untuk Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}