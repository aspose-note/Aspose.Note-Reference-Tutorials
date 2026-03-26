---
date: 2026-01-05
description: Pelajari cara mengatur locale default, memuat dokumen OneNote, mengatur
  lisensi Aspose, mengonversi OneNote ke PNG, dan menyimpan OneNote sebagai gambar
  menggunakan Aspose.Note untuk Java.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Atur Locale Default di OneNote – Aspose.Note Java
url: /id/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengatur Locale Default di OneNote – Aspose.Note Java

## Pendahuluan

Jika Anda perlu **set default locale** saat memproses file OneNote, Aspose.Note untuk Java mempermudahnya. Pada tutorial ini kami akan membahas semua yang Anda perlukan—mulai dari melisensikan produk, memuat dokumen OneNote, mengubah locale, hingga akhirnya mengonversi file menjadi gambar PNG. Pada akhir tutorial, Anda akan dapat menyesuaikan pengaturan bahasa dan menghasilkan output yang spesifik locale dengan hanya beberapa baris kode.

## Jawaban Cepat
- **Apa yang dilakukan “set default locale”?** Itu mendefinisikan bahasa dan format regional yang digunakan oleh Aspose.Note saat membaca atau menulis file OneNote.  
- **Apakah saya memerlukan lisensi?** Ya—atur lisensi Aspose untuk membuka semua fungsi.  
- **Versi Java mana yang diperlukan?** Semua JDK 8+ didukung.  
- **Bisakah saya mengonversi OneNote ke PNG?** Tentu saja; API memungkinkan Anda menyimpan halaman sebagai gambar.  
- **Apakah proses ini thread‑safe?** Mengatur locale default bersifat global, jadi konfigurasikan sekali saat aplikasi mulai.

## Apa itu “set default locale” di Aspose.Note?
Mengatur locale default memberi tahu Aspose.Note bahasa dan konvensi budaya apa yang harus diterapkan saat mem-parsing tanggal, angka, dan teks. Ini penting untuk aplikasi multi‑regional yang memerlukan format konsisten di berbagai locale pengguna.

## Mengapa mengatur locale default saat bekerja dengan OneNote?
- **Representasi data yang akurat:** Tanggal dan angka muncul dengan benar untuk audiens target.  
- **String UI yang konsisten:** Teks yang diekstrak dari OneNote menghormati pengaturan bahasa.  
- **Konversi yang disederhanakan:** Ketika Anda kemudian mengonversi file OneNote ke PNG atau format lain, tata letak visual sesuai dengan locale yang diharapkan.

## Prasyarat

- **Lingkungan Pengembangan Java:** JDK terpasang dan `JAVA_HOME` dikonfigurasi.  
- **Pustaka Aspose.Note:** Unduh JAR terbaru dari [download link](https://releases.aspose.com/note/java/).  
- **File lisensi Aspose yang valid** (versi percobaan gratis dapat digunakan untuk pengujian).

## Impor Paket

Sebelum menulis kode apa pun, impor kelas‑kelas yang menyediakan fungsionalitas yang diperlukan.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Langkah 1: Atur Lisensi Aspose

```java
License license = new License();
license.setLicense("licenseFile");
```

Mengatur lisensi Aspose membuka semua fitur, termasuk penanganan locale dan konversi gambar.

## Langkah 2: Atur Locale Default

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Di sini kami **set default locale** ke Bahasa Inggris (`en`) dengan kode negara `rs`. Sesuaikan kode bahasa dan negara agar cocok dengan wilayah target Anda.

## Langkah 3: Muat Dokumen OneNote

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Langkah ini **load(s) OneNote document** ke dalam objek `Document` sehingga Anda dapat bekerja dengan isinya.

## Langkah 4: Konversi OneNote ke PNG (konversi file OneNote)

```java
oneFile.save("sample.png");
```

Metode `save` melakukan **onenote file conversion**, mengekspor notebook (atau halaman tertentu) sebagai gambar PNG—secara efektif **convert onenote to png** dan **save onenote as image**.

## Masalah Umum & Tips

- **Lisensi tidak ditemukan:** Pastikan jalur ke `licenseFile` benar dan file memiliki izin baca.  
- **Locale tidak diterapkan:** Panggil `Locale.setDefault` **sebelum** memuat dokumen.  
- **Output gambar tidak muncul:** Pastikan file OneNote memang berisi halaman yang dapat dirender; notebook kosong akan menghasilkan PNG kosong.

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.Note kompatibel dengan berbagai versi Java?**  
J: Ya, Aspose.Note mendukung Java 8 dan yang lebih baru, memastikan kompatibilitas luas di berbagai lingkungan pengembangan.

**T: Bisakah saya mengintegrasikan Aspose.Note dengan pustaka Java lain?**  
J: Tentu saja. API bekerja mulus dengan pustaka populer seperti Apache POI, Jackson, dan Spring.

**T: Apakah Aspose.Note menawarkan dukungan untuk berbagai format file?**  
J: Meskipun fokus utamanya adalah file OneNote, pustaka ini dapat mengekspor ke PNG, JPEG, PDF, dan format gambar lainnya.

**T: Apakah ada forum komunitas untuk pengguna Aspose.Note untuk mencari bantuan dan berbagi pengetahuan?**  
J: Ya, forum komunitas Aspose menyediakan platform bagi pengguna untuk berinteraksi dengan para ahli, mengajukan pertanyaan, dan berkolaborasi dalam solusi. Kunjungi [support forum](https://forum.aspose.com/c/note/28) untuk bantuan.

**T: Bisakah saya mencoba Aspose.Note sebelum membeli?**  
J: Tentu saja, Anda dapat menjelajahi kemampuan Aspose.Note dengan memanfaatkan percobaan gratis yang ditawarkan di situs web.

## Kesimpulan

Dengan mengikuti langkah‑langkah ini Anda telah belajar cara **set default locale**, **load OneNote document**, **set Aspose license**, dan **convert OneNote to PNG** menggunakan Aspose.Note untuk Java. Alur kerja ini memberi Anda kemampuan menghasilkan laporan dan gambar yang sadar locale untuk audiens global.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2026-01-05  
**Diuji Dengan:** Aspose.Note 24.11 for Java  
**Penulis:** Aspose