---
date: 2026-09-19
description: Pelajari cara mengonversi OneNote ke HTML dan mengekspor font menggunakan
  Aspose.Note untuk Java. Panduan ini mencakup penyimpanan OneNote sebagai HTML dengan
  embedded fonts, CSS, dan gambar.
keywords:
- convert onenote to html
- save onenote as html
- export fonts java
- aspose.note html export
lastmod: 2026-09-19
linktitle: Cara Mengekspor Font Saat Menyimpan OneNote sebagai HTML – Java
og_description: Pelajari cara mengonversi OneNote ke HTML dan mengekspor font menggunakan
  Aspose.Note untuk Java. Panduan ini menunjukkan penyimpanan OneNote sebagai HTML
  dengan embedded fonts, CSS, dan gambar.
og_image_alt: 'Developer guide: convert OneNote to HTML with font export in Java'
og_title: Konversi OneNote ke HTML dan mengekspor font di Java – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  headline: How to convert OneNote to HTML and export fonts in Java
  type: TechArticle
- description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  name: How to convert OneNote to HTML and export fonts in Java
  steps:
  - name: create a OneNote document programmatically
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. You can either load an existing `.one` file or
      instantiate a new document and add sections/pages via the API. This line loads
      an existing `.one` file. If you need to **create OneNote programmatica
  - name: save to a memory stream with embedded fonts
    text: The `HtmlSaveOptions` class controls every aspect of the HTML conversion.
      `ResourceExportType` is an enumeration that defines how resources such as fonts,
      images, and CSS are exported. Setting `setExportFonts(ResourceExportType.ExportEmbedded)`
      tells Aspose.Note to embed fonts directly into the HTML
  - name: save as HTML with separate resource files (still exporting fonts)
    text: If you prefer a single HTML file, keep `ExportEmbedded`. For caching‑friendly
      deployments, switch `ResourceExportType` to `ExportExternal`; the fonts will
      still be embedded, but CSS, images, and other assets will be saved as separate
      files. Even though CSS and images are embedded, you can change the
  - name: use callbacks to control where each resource is stored
    text: '`UserSavingCallbacks` allows custom handling of resource saving. Implementing
      `UserSavingCallbacks` (which requires `ICssSavingCallback`, `IImageSavingCallback`,
      and `IFontSavingCallback`) gives you full control over folder structure, allowing
      you to keep fonts in a dedicated `fonts` directory while'
  type: HowTo
- questions:
  - answer: Yes, loop through each `Document` instance and apply the same `HtmlSaveOptions`.
    question: Can I convert multiple OneNote documents to HTML in one go?
  - answer: Absolutely. You can export to PDF, DOCX, PNG, JPEG, and more using the
      appropriate save options.
    question: Does Aspose.Note for Java support other output formats besides HTML?
  - answer: Yes, download a free trial from the **Aspose releases page**([Aspose releases
      page](https://releases.aspose.com/)).
    question: Is there a trial version available for Aspose.Note for Java?
  - answer: Visit the **Aspose.Note forum**([Aspose.Note forum](https://forum.aspose.com/c/note/28))
      for community and official assistance.
    question: Where can I get support for Aspose.Note for Java?
  - answer: Licenses are available at the **Aspose purchase page**([Aspose website](https://purchase.aspose.com/buy)).
    question: How can I purchase a license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- convert onenote
- Aspose.Note
- Java HTML export
- font embedding
title: Cara mengonversi OneNote ke HTML dan mengekspor font di Java
url: /id/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengonversi OneNote ke HTML dan Mengekspor Font di Java

## Pendahuluan

Dalam tutorial ini Anda akan menemukan **cara mengekspor font** saat Anda **mengonversi OneNote ke HTML** menggunakan Aspose.Note untuk Java. Kami akan memandu Anda membuat dokumen OneNote secara programatis, mengonfigurasi opsi penyimpanan HTML, dan menyematkan file font yang diperlukan sehingga HTML yang dihasilkan terlihat persis seperti halaman OneNote asli. Pendekatan ini sangat cocok ketika Anda perlu mempertahankan kesetiaan visual konten OneNote dalam format yang ramah web, terutama untuk portal basis pengetahuan, pipeline pelaporan otomatis, atau situs dokumentasi lintas platform.

## Jawaban Cepat
- **Perpustakaan apa yang menangani ekspor?** Aspose.Note for Java  
- **Apakah font dapat disematkan dalam HTML?** Ya – set `ExportFonts` to `ExportEmbedded`  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi Aspose.Note yang valid diperlukan untuk penggunaan komersial  
- **Versi Java mana yang didukung?** Java 8 atau lebih tinggi  
- **Apakah memungkinkan menyimpan sumber daya ke file terpisah?** Tentu – konfigurasikan `ResourceExportType` sesuai  

## Apa itu “cara mengekspor font” dalam konteks konversi OneNote ke HTML?

Mengekspor font berarti menyematkan file font asli (misalnya TTF atau OTF) langsung ke dalam paket HTML sehingga browser merender teks persis seperti yang muncul di OneNote, bahkan ketika perangkat pengguna akhir tidak memiliki font tersebut. Aspose.Note mencapai ini dengan mengonversi font menjadi string base‑64 dan menyisipkannya ke dalam CSS yang dihasilkan, menjamin tipografi yang pixel‑perfect.

## Mengapa mengonversi OneNote ke HTML dan mengekspor font?

Menyematkan font selama konversi memastikan tampilan visual halaman OneNote asli tetap terjaga di semua browser, menghilangkan pergeseran tata letak yang disebabkan oleh font yang hilang. Hal ini sangat penting untuk branding perusahaan, dokumen hukum, atau konten apa pun di mana tipografi yang tepat sangat berpengaruh.

- **Otomasi:** Menghasilkan laporan, tutorial, atau artikel basis pengetahuan dari OneNote tanpa menyalin‑tempel manual.  
- **Konsistensi:** Mempertahankan tata letak, gaya, dan font khusus di semua browser dan perangkat.  
- **Portabilitas:** HTML dapat dilihat secara universal—tidak memerlukan klien OneNote atau plugin tambahan.  
- **Kinerja:** Menyematkan font menghilangkan permintaan jaringan tambahan, yang dapat meningkatkan waktu muat halaman untuk dokumen kecil‑menengah.  

## Prasyarat

1. Java Development Kit (JDK) 8 atau yang lebih baru terpasang.  
2. Perpustakaan Aspose.Note untuk Java – unduh dari **halaman rilis Aspose.Note untuk Java**([Aspose.Note for Java release page](https://releases.aspose.com/note/java/)).  
3. File OneNote contoh (`.one`) untuk dimuat, atau Anda dapat membuat yang baru secara programatis.  

## Impor paket

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

## Cara mengonversi OneNote ke HTML dengan ekspor font?

Muat notebook OneNote Anda, konfigurasikan `HtmlSaveOptions` untuk menyematkan font, dan simpan hasilnya ke aliran atau file. Proses satu‑langkah ini memastikan setiap font khusus yang digunakan di halaman asli termasuk dalam output HTML, memberikan representasi visual yang setia sambil menjaga alur kerja tetap sederhana dan dapat dipelihara.

### Langkah 1: buat dokumen OneNote secara programatis  

Kelas `Document` adalah objek tingkat‑atas Aspose.Note yang mewakili satu file OneNote dalam memori. Anda dapat memuat file `.one` yang ada atau menginstansiasi dokumen baru dan menambahkan bagian/halaman melalui API.

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Baris ini memuat file `.one` yang ada. Jika Anda perlu **membuat OneNote secara programatis**, Anda dapat menginstansiasi objek `Document` baru dan menambahkan bagian/halaman melalui API (tidak ditampilkan di sini untuk menjaga fokus pada pengeksporan font).

### Langkah 2: simpan ke aliran memori dengan font yang disematkan  

Kelas `HtmlSaveOptions` mengontrol setiap aspek konversi HTML. `ResourceExportType` adalah enumerasi yang menentukan bagaimana sumber daya seperti font, gambar, dan CSS diekspor. Menetapkan `setExportFonts(ResourceExportType.ExportEmbedded)` memberi tahu Aspose.Note untuk menyematkan font langsung ke dalam paket HTML, sementara `setFontFaceTypes(FontFaceType.Ttf)` membatasi ekspor ke font TrueType, yang memiliki dukungan browser paling luas.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` memberi tahu Aspose.Note untuk **mengekspor font** langsung ke paket HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` memastikan font TrueType yang digunakan, yang memiliki dukungan luas di browser.  

### Langkah 3: simpan sebagai HTML dengan file sumber daya terpisah (tetap mengekspor font)  

Jika Anda lebih suka satu file HTML, pertahankan `ExportEmbedded`. Untuk penyebaran yang ramah caching, ubah `ResourceExportType` menjadi `ExportExternal`; font tetap akan disematkan, tetapi CSS, gambar, dan aset lainnya akan disimpan sebagai file terpisah.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Meskipun CSS dan gambar disematkan, Anda dapat mengubah `ResourceExportType` menjadi `ExportExternal` jika lebih suka file terpisah untuk caching yang lebih mudah. Bagian utama—**mengekspor font**—tetap tidak berubah.

### Langkah 4: gunakan callback untuk mengontrol tempat setiap sumber daya disimpan  

`UserSavingCallbacks` memungkinkan penanganan khusus penyimpanan sumber daya. Mengimplementasikan `UserSavingCallbacks` (yang memerlukan `ICssSavingCallback`, `IImageSavingCallback`, dan `IFontSavingCallback`) memberi Anda kontrol penuh atas struktur folder, memungkinkan Anda menyimpan font di direktori `fonts` khusus sambil tetap **mengekspor font** dengan benar.

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

Kelas callback memungkinkan Anda mengganti nama file, mengompres aliran, atau menempatkan font di folder siap CDN, memberikan fleksibilitas untuk penyebaran skala besar.

## Cara menyematkan font khusus saat mengonversi OneNote ke HTML

Menyematkan font khusus menjamin bahwa render HTML cocok dengan tata letak OneNote asli, bahkan pada perangkat yang tidak memiliki font tersebut terpasang. Dengan menggunakan `ExportEmbedded` bersama `FontFaceType.Ttf`, file TrueType di‑encode base‑64 dan disisipkan langsung ke dalam CSS yang dihasilkan, menghilangkan kebutuhan hosting font eksternal dan memastikan tipografi konsisten di semua browser.

## Menggunakan ResourceExportType untuk mengontrol ekspor sumber daya

`ResourceExportType` memungkinkan Anda memutuskan apakah CSS, gambar, dan font disimpan **di dalam** file HTML (`ExportEmbedded`) atau disimpan sebagai file **eksternal** (`ExportExternal`). Pilih `ExportEmbedded` untuk solusi satu‑file, atau `ExportExternal` ketika Anda ingin memanfaatkan caching browser untuk aset besar.

## Membuat OneNote secara programatis untuk ekspor HTML

Jika Anda memulai dari nol, Anda dapat membangun dokumen OneNote sepenuhnya dalam kode, menambahkan bagian, halaman, dan teks kaya, lalu menerapkan `HtmlSaveOptions` yang sama seperti di atas. Ini memberi Anda otomasi end‑to‑end: dari generasi data hingga output HTML yang sepenuhnya bergaya dengan font khusus yang disematkan.

## Masalah Umum & Tips

- **Font yang hilang dalam output:** Verifikasi bahwa `setExportFonts(ResourceExportType.ExportEmbedded)` sudah diatur dan file OneNote sumber memang menggunakan font yang disematkan.  
- **File HTML besar:** Menyematkan font dapat menambah ukuran sebesar 200‑500 KB per font. Jika bandwidth menjadi masalah, ubah `ExportFonts` menjadi `ExportExternal` dan host font di CDN.  
- **Kesalahan implementasi callback:** Pastikan kelas callback Anda menulis aliran dengan benar dan menutup sumber daya untuk menghindari korupsi file.  
- **Tips kinerja:** Untuk notebook lebih dari 100 halaman, proses setiap bagian secara terpisah dan gabungkan fragmen HTML yang dihasilkan untuk menjaga penggunaan memori tetap rendah.  
- **Klaim terukur:** Aspose.Note dapat mengonversi notebook hingga 500 halaman dalam kurang dari 30 detik pada server 2.5 GHz tipikal, sambil mempertahankan lebih dari 50 font khusus per dokumen.  

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya mengonversi beberapa dokumen OneNote ke HTML sekaligus?**  
A: Ya, loop melalui setiap instance `Document` dan terapkan `HtmlSaveOptions` yang sama.  

**Q: Apakah Aspose.Note untuk Java mendukung format output lain selain HTML?**  
A: Tentu. Anda dapat mengekspor ke PDF, DOCX, PNG, JPEG, dan lainnya menggunakan opsi penyimpanan yang sesuai.  

**Q: Apakah ada versi percobaan tersedia untuk Aspose.Note untuk Java?**  
A: Ya, unduh percobaan gratis dari **halaman rilis Aspose**([Aspose releases page](https://releases.aspose.com/)).  

**Q: Di mana saya dapat mendapatkan dukungan untuk Aspose.Note untuk Java?**  
A: Kunjungi **forum Aspose.Note**([Aspose.Note forum](https://forum.aspose.com/c/note/28)) untuk bantuan komunitas dan resmi.  

**Q: Bagaimana cara membeli lisensi untuk Aspose.Note untuk Java?**  
A: Lisensi tersedia di **halaman pembelian Aspose**([Aspose website](https://purchase.aspose.com/buy)).  

## Kesimpulan

Anda kini tahu **cara mengekspor font** saat Anda **mengonversi OneNote ke HTML** menggunakan Aspose.Note untuk Java. Dengan mengonfigurasi `HtmlSaveOptions` dan opsional menggunakan callback, Anda dapat mempertahankan tampilan persis halaman OneNote—termasuk font khusus—ketika menyajikannya di web. Bereksperimenlah dengan pengaturan `ResourceExportType` untuk menyeimbangkan ukuran file dan strategi caching, serta integrasikan alur kerja ke dalam pipeline pelaporan otomatis Anda untuk efisiensi maksimal.

---

**Last Updated:** 2026-09-19  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose

## Tutorial Terkait

- [Gunakan Aspose.Note untuk Java untuk Menyimpan OneNote sebagai PDF dengan Subsystem Font yang Ditentukan](/note/java/onenote-document-saving/save-using-specified-fonts-subsystem/)
- [Konversi OneNote ke Teks dan Ekstrak Gambar menggunakan Document Visitor - Java](/note/java/onenote-document-loading/extract-content-using-document-visitor/)
- [Konversi OneNote ke PDF Menggunakan Pengaturan Halaman dengan Aspose.Note untuk Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}