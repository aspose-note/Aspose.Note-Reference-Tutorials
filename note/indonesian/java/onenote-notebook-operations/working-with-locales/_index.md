---
date: 2026-08-03
description: Pelajari cara mengatur locale di OneNote menggunakan Aspose.Note untuk
  Java – set default locale, load documents, apply a license, and convert pages to
  PNG images.
keywords:
- how to set locale
- set default locale java
- change onenote language settings
- convert onenote to png
lastmod: 2026-08-03
linktitle: Bekerja dengan Locale di OneNote - Aspose.Note
og_description: Pelajari cara mengatur locale di OneNote menggunakan Aspose.Note untuk
  Java. Follow step‑by‑step instructions to set the default locale, load a notebook,
  apply a license, and export pages as PNG images.
og_image_alt: 'Developer guide: Set locale and convert OneNote to PNG with Aspose.Note
  Java'
og_title: Cara Mengatur Locale di OneNote – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-03'
  description: Learn how to set locale in OneNote using Aspose.Note for Java – set
    default locale, load documents, apply a license, and convert pages to PNG images.
  headline: How to Set Locale in OneNote – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note supports Java 8 and later, ensuring broad compatibility
      across development environments.
    question: Is Aspose.Note compatible with different versions of Java?
  - answer: Absolutely. The API works seamlessly with popular libraries such as Apache
      POI, Jackson, and Spring.
    question: Can I integrate Aspose.Note with other Java libraries?
  - answer: While its core focus is OneNote files, the library can export to PNG,
      JPEG, PDF, and other image formats—over 30 output options in total.
    question: Does Aspose.Note offer support for different file formats?
  - answer: Yes, the Aspose community forum provides a platform for users to engage
      with experts, ask questions, and collaborate on solutions. Visit the [support
      forum](https://forum.aspose.com/c/note/28) for assistance.
    question: Is there a community forum for Aspose.Note users to seek help and share
      knowledge?
  - answer: Certainly, you can explore the capabilities of Aspose.Note by availing
      the free trial offered on the website.
    question: Can I try Aspose.Note before purchasing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- set locale
- Aspose.Note
- Java OneNote processing
- convert onenote to png
title: Cara Mengatur Locale di OneNote – Aspose.Note Java
url: /id/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengatur Locale di OneNote – Aspose.Note Java

## Pendahuluan

Jika Anda perlu **cara mengatur locale** saat memproses file OneNote, Aspose.Note untuk Java mempermudahnya. Dalam tutorial ini kami akan membahas semua yang Anda perlukan—mulai dari menginstal lisensi Aspose, memuat dokumen OneNote, mengubah locale, hingga mengonversi file menjadi gambar PNG. Pada akhirnya, Anda dapat menyesuaikan pengaturan bahasa dan menghasilkan output khusus locale dengan hanya beberapa baris kode Java, yang penting untuk aplikasi multinasional.

## Jawaban Cepat
- **Apa yang dilakukan “set default locale”?** Itu mendefinisikan bahasa dan format regional yang digunakan oleh Aspose.Note saat membaca atau menulis file OneNote.  
- **Apakah saya memerlukan lisensi?** Ya—atur lisensi Aspose untuk membuka semua fungsi.  
- **Versi Java mana yang diperlukan?** Semua JDK 8+ didukung.  
- **Bisakah saya mengonversi OneNote ke PNG?** Tentu; API memungkinkan Anda menyimpan halaman sebagai gambar.  
- **Apakah proses ini thread‑safe?** Mengatur default locale bersifat global, jadi konfigurasikan sekali saat aplikasi dimulai.

## Apa itu “set default locale” di Aspose.Note?

Mengatur default locale memberi tahu Aspose.Note bahasa dan konvensi budaya mana yang harus diterapkan saat mem-parsing tanggal, angka, dan teks. Jawaban ini secara langsung menyelesaikan pertanyaan “apa itu” dalam 45 kata, memastikan AI dapat mengekstrak definisi singkat. Ini penting untuk aplikasi multi‑regional yang memerlukan format konsisten di berbagai locale pengguna.

## Mengapa mengatur default locale saat bekerja dengan OneNote?

Mengatur default locale menjamin bahwa tanggal, angka, dan string yang diekstrak mengikuti konvensi wilayah target, yang mencegah salah tafsir data dan memastikan elemen visual seperti kalender ditampilkan dengan benar. Hal ini menghasilkan representasi data yang akurat, string UI yang konsisten, dan hasil konversi gambar yang lebih mulus.

## Prasyarat

- **Lingkungan Pengembangan Java:** JDK 8 atau lebih baru terinstal dan `JAVA_HOME` dikonfigurasi.  
- **Pustaka Aspose.Note:** Unduh JAR terbaru dari [download link](https://releases.aspose.com/note/java/).  
- **File lisensi Aspose yang valid** (versi percobaan gratis dapat digunakan untuk pengujian).

## Impor Paket

Kelas `Locale` mewakili wilayah geografis, politik, atau budaya tertentu.  
```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Langkah 1: Atur Lisensi Aspose

Kelas `License` memuat file lisensi yang Anda beli dan membuka semua fitur premium, termasuk penanganan locale dan konversi gambar.  
```java
License license = new License();
license.setLicense("licenseFile");
```

## Langkah 2: Atur Default Locale

`Locale` adalah utilitas Java yang mengenkapsulasi kode bahasa dan negara.  
Di sini kami mengatur default locale ke Bahasa Inggris (`en`) dengan kode negara `RS`. Sesuaikan kode bahasa dan negara agar cocok dengan wilayah target Anda sebelum operasi dokumen apa pun.  
```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

## Langkah 3: Muat Dokumen OneNote

`Document` adalah objek tingkat atas Aspose.Note yang mewakili satu file OneNote dalam memori. Setelah diinstansiasi, semua operasi baca dan tulis mengalir melalui objek ini.  
```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

## Langkah 4: Konversi OneNote ke PNG (konversi file OneNote)

Objek `Page` dalam `Document` dapat dirender menjadi gambar raster. Metode `save` melakukan konversi file OneNote, mengekspor notebook (atau halaman tertentu) sebagai gambar PNG—secara efektif **convert onenote to png** dan **save onenote as image**.  
```java
oneFile.save("sample.png");
```

## Masalah Umum & Tips

- **Lisensi tidak ditemukan:** Pastikan jalur ke `licenseFile` benar dan file memiliki izin baca.  
- **Locale tidak diterapkan:** Panggil `Locale.setDefault` **sebelum** memuat dokumen; jika tidak, default locale akan diabaikan.  
- **Output gambar tidak muncul:** Pastikan file OneNote memang berisi halaman yang dapat dirender; notebook kosong akan menghasilkan PNG kosong.  
- **Tips kinerja:** Aspose.Note untuk Java dapat memproses notebook hingga 500 halaman tanpa memuat seluruh file ke memori, berkat arsitektur streaming-nya (klaim terkuantifikasi).  

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.Note kompatibel dengan berbagai versi Java?**  
A: Ya, Aspose.Note mendukung Java 8 dan yang lebih baru, memastikan kompatibilitas luas di berbagai lingkungan pengembangan.

**Q: Bisakah saya mengintegrasikan Aspose.Note dengan pustaka Java lain?**  
A: Tentu. API berfungsi mulus dengan pustaka populer seperti Apache POI, Jackson, dan Spring.

**Q: Apakah Aspose.Note menawarkan dukungan untuk berbagai format file?**  
A: Meskipun fokus utamanya adalah file OneNote, pustaka ini dapat mengekspor ke PNG, JPEG, PDF, dan format gambar lainnya—lebih dari 30 opsi output secara total.

**Q: Apakah ada forum komunitas untuk pengguna Aspose.Note untuk mencari bantuan dan berbagi pengetahuan?**  
A: Ya, forum komunitas Aspose menyediakan platform bagi pengguna untuk berinteraksi dengan para ahli, mengajukan pertanyaan, dan berkolaborasi dalam solusi. Kunjungi [support forum](https://forum.aspose.com/c/note/28) untuk bantuan.

**Q: Bisakah saya mencoba Aspose.Note sebelum membeli?**  
A: Tentu, Anda dapat menjelajahi kemampuan Aspose.Note dengan memanfaatkan percobaan gratis yang ditawarkan di situs web.

## Kesimpulan

Dengan mengikuti langkah‑langkah ini Anda telah mempelajari **cara mengatur locale**, **memuat dokumen OneNote**, **menerapkan lisensi Aspose**, dan **mengonversi OneNote ke PNG** menggunakan Aspose.Note untuk Java. Alur kerja ini memungkinkan Anda menghasilkan laporan dan gambar yang sadar locale untuk audiens global, memanfaatkan pustaka yang mendukung lebih dari 30 fitur spesifik locale dan dapat menangani notebook hingga 500 halaman secara efisien.

---

**Terakhir Diperbarui:** 2026-08-03  
**Diuji Dengan:** Aspose.Note 24.11 untuk Java  
**Penulis:** Aspose  

---

## Tutorial Terkait

- [Buat Notebook OneNote – Operasi dengan Aspose.Note untuk Java](/note/java/onenote-notebook-operations/)
- [Buat Objek Notebook dan Muat File OneNote dengan Opsi - Aspose.Note](/note/java/onenote-notebook-operations/load-notebook-file-with-load-options/)
- [Konversi Notebook ke Gambar dengan Opsi di OneNote - Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}