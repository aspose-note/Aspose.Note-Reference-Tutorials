---
date: 2025-12-17
description: Pelajari cara mengekspor OneNote dengan menyimpan dokumen sebagai gambar
  PNG skala abu-abu menggunakan Aspose.Note untuk Java. Termasuk langkah-langkah memuat
  dokumen OneNote dan membuat gambar skala abu-abu.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Cara Mengekspor OneNote sebagai Gambar Grayscale – Aspose.Note
url: /id/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan ke Gambar Grayscale di OneNote - Aspose.Note

## Pendahuluan

Dalam tutorial ini, kami akan menunjukkan **cara mengekspor onenote** dengan menyimpan dokumen sebagai gambar grayscale menggunakan Aspose.Note untuk Java. Gambar grayscale adalah gambar monokrom yang hanya berisi nuansa abu‑abu, yang dapat berguna untuk pencetakan, arsip, atau mengurangi ukuran file. Kami akan memandu Anda memuat dokumen OneNote, mengonfigurasi opsi penyimpanan untuk **membuat gambar grayscale**, dan akhirnya **menyimpan dokumen sebagai PNG**.

## Jawaban Cepat
- **Apa arti “cara mengekspor onenote”?** Ini merujuk pada mengonversi file OneNote ke format lain, seperti gambar, secara programatis.  
- **Format apa yang terbaik untuk output grayscale?** PNG bekerja dengan baik karena mempertahankan kualitas loss‑less dan mendukung mode warna grayscale.  
- **Apakah saya memerlukan lisensi?** Lisensi Aspose.Note yang valid diperlukan untuk penggunaan produksi; lisensi percobaan sementara tersedia untuk pengujian.  
- **Versi Java apa yang diperlukan?** Java 8 atau lebih tinggi disarankan.  
- **Bisakah saya mengubah ukuran gambar?** Ya, Anda dapat menyesuaikan properti `ImageSaveOptions` seperti `Resolution` atau `PageSize` sebelum menyimpan.

## Apa itu “cara mengekspor onenote”?
Mengekspor OneNote berarti secara programatis mengonversi file OneNote `.one` ke representasi lain—seperti PDF, HTML, atau gambar. Dalam panduan ini kami fokus pada mengekspor ke gambar **grayscale PNG**, yang merupakan kebutuhan umum untuk dokumentasi atau alur kerja pencetakan.

## Mengapa mengekspor OneNote sebagai gambar grayscale?
- **Ukuran file lebih kecil** – PNG grayscale biasanya lebih kecil dibandingkan gambar berwarna penuh.  
- **Keterbacaan lebih baik** – Untuk laporan cetak, grayscale sering memberikan kontras yang lebih jelas.  
- **Kompatibilitas** – PNG didukung secara luas di browser, editor, dan perangkat seluler.  

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal‑hal berikut:

1. Java Development Kit (JDK) terpasang di sistem Anda.  
2. Perpustakaan Aspose.Note untuk Java. Anda dapat mengunduhnya dari [sini](https://releases.aspose.com/note/java/).  
3. Pemahaman dasar tentang pemrograman Java.  

## Impor Paket

Untuk memulai, impor paket yang diperlukan:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Langkah 1: Muat Dokumen OneNote

Pertama, **muat dokumen onenote** ke Aspose.Note. Ganti `"Your Document Directory"` dengan jalur ke folder lokal Anda dan `"Aspose.one"` dengan nama file OneNote Anda.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Langkah 2: Tentukan Jalur Output dan Opsi

Tentukan jalur output untuk gambar grayscale dan spesifikasikan opsi penyimpanan. Kami akan mengatur `ColorMode` ke `GrayScale` dan menggunakan format **save document as png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Langkah 3: Simpan Dokumen

Akhirnya, simpan dokumen sebagai gambar PNG grayscale menggunakan opsi yang telah dikonfigurasi.

```java
oneFile.save(dataDir, options);
```

## Masalah Umum dan Solusinya
- **FileNotFoundException** – Pastikan `dataDir` mengarah ke folder yang benar dan file `.one` ada.  
- **LicenseException** – Pastikan Anda telah menerapkan lisensi Aspose.Note yang valid sebelum memanggil `save`.  
- **Output beresolusi rendah** – Sesuaikan `options.setResolution(300)` untuk meningkatkan DPI jika diperlukan.

## Pertanyaan yang Sering Diajukan

**T1: Bisakah saya menyimpan gambar grayscale dalam format lain?**  
J1: Ya, cukup ubah parameter `SaveFormat` pada konstruktor `ImageSaveOptions` menjadi `Jpeg`, `Bmp`, dll.

**T2: Apakah Aspose.Note kompatibel dengan semua versi dokumen OneNote?**  
J2: Aspose.Note mendukung Microsoft OneNote 2010 dan versi selanjutnya.

**T3: Apakah Aspose.Note memerlukan lisensi untuk digunakan?**  
J3: Lisensi yang valid diperlukan untuk penggunaan produksi, tetapi lisensi percobaan sementara dapat diperoleh untuk evaluasi.

**T4: Bisakah saya memanipulasi aspek lain dari dokumen sebelum menyimpannya sebagai gambar?**  
J4: Tentu saja! Aspose.Note menyediakan API komprehensif untuk mengedit bagian, halaman, dan konten sebelum ekspor.

**T5: Di mana saya dapat menemukan dukungan jika mengalami masalah?**  
J5: Anda dapat menemukan dukungan di forum Aspose.Note [sini](https://forum.aspose.com/c/note/28).

## Kesimpulan

Anda kini telah mempelajari **cara mengekspor onenote** dengan memuat file OneNote, mengonfigurasi opsi penyimpanan untuk **membuat gambar grayscale**, dan **menyimpan dokumen sebagai PNG**. Teknik ini berguna untuk menghasilkan visual ringan yang siap cetak dari notebook OneNote. Jangan ragu untuk bereksperimen dengan pengaturan `ColorMode` lain atau format gambar untuk menyesuaikan kebutuhan proyek Anda.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2025-12-17  
**Diuji Dengan:** Aspose.Note 24.12 untuk Java  
**Penulis:** Aspose  

---