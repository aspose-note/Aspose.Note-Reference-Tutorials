---
date: 2026-02-05
description: Pelajari cara mengekspor halaman OneNote dan menyimpan OneNote sebagai
  gambar. Panduan ini menunjukkan cara mengonversi .one ke PNG, mengatur indeks halaman,
  dan mengekspor gambar halaman OneNote menggunakan Aspose.Note untuk Java.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Cara Mengekspor Halaman OneNote ke Gambar PNG dalam Java menggunakan Aspose.Note
url: /id/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

 output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor Halaman OneNote ke Gambar PNG di Java menggunakan Aspose.Note

## Pendahuluan

Dalam tutorial ini Anda akan menemukan **how to export OneNote page** ke gambar PNG menggunakan pustaka Aspose.Note untuk Java. **How to export onenote** halaman merupakan kebutuhan umum ketika Anda ingin berbagi catatan di luar ekosistem OneNote, menyematkannya dalam laporan, atau memprosesnya dengan alat pemrosesan gambar. Kami akan membahas semua yang Anda perlukan—dari menyiapkan lingkungan hingga mengatur indeks halaman, mengonversi halaman, dan menyimpan hasilnya sebagai file PNG berkualitas tinggi. Pada akhir tutorial, Anda akan dapat **save onenote as image** di aplikasi Java mana pun.

## Jawaban Cepat
- **Library apa yang dibutuhkan?** Aspose.Note untuk Java.  
- **Bisakah saya mengekspor satu halaman?** Ya—gunakan `setPageIndex` untuk menargetkan halaman yang tepat.  
- **Format gambar yang didukung?** PNG, JPEG, GIF, BMP, TIFF (PNG ditampilkan di sini).  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis tersedia; lisensi diperlukan untuk produksi.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk konversi dasar.  
- **Bagaimana cara mengonversi .one ke png?** Muat file `.one` dengan `Document`, atur indeks halaman, dan simpan dengan `ImageSaveOptions`.  

## Apa itu “export OneNote page”?

Mengekspor halaman OneNote berarti mengonversi halaman tertentu dalam dokumen `.one` menjadi file gambar mandiri (PNG dalam kasus ini). Ini berguna ketika Anda perlu **export onenote page image** untuk berbagi, menyematkan, atau analisis berbasis gambar lebih lanjut.

## Mengapa menggunakan Aspose.Note untuk Java untuk mengonversi OneNote ke PNG?

- **Tanpa ketergantungan Microsoft Office** – berfungsi di platform apa pun yang menjalankan Java.  
- **Kontrol detail** – Anda dapat memilih halaman mana pun melalui `setPageIndex`.  
- **Output berkualitas tinggi** – PNG mempertahankan grafik vektor dan kejernihan teks.  
- **Siap batch** – mudah untuk mengulangi halaman untuk konversi massal, membuat **convert onenote to png** menjadi sederhana untuk banyak halaman sekaligus.  

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – versi 8 atau lebih tinggi.  
2. **Aspose.Note for Java** – unduh JAR terbaru dari [situs Aspose](https://releases.aspose.com/note/java/).  
3. **Dokumen OneNote** (`.one`) yang berisi halaman yang ingin Anda ekspor.

## Impor Paket

Pertama, impor kelas Java yang diperlukan:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

Impor ini memberi Anda akses ke API inti Aspose.Note, termasuk memuat dokumen dan mengonfigurasi opsi penyimpanan gambar.

## Panduan Langkah‑per‑Langkah

### Langkah 1: Muat Dokumen OneNote

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Kami menggunakan kelas `Document` untuk membaca file OneNote dari disk. Objek `LoadOptions` memungkinkan Anda menyesuaikan perilaku pemuatan jika diperlukan. Langkah ini merupakan fondasi untuk **convert .one to png**.

### Langkah 2: Inisialisasi ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` memberi tahu Aspose.Note bahwa kami menginginkan output dalam format **PNG**. Anda dapat beralih ke JPEG, BMP, dll., dengan mengubah `SaveFormat`. Objek ini juga memungkinkan Anda mengontrol DPI, kedalaman warna, dan pengaturan khusus gambar lainnya.

### Langkah 3: Atur Indeks Halaman (Cara mengonversi halaman OneNote)

```java
// set page index
opts.setPageIndex(0);
```

Metode `setPageIndex` memilih halaman mana yang akan diekspor. Penomoran halaman dimulai dari **0**, sehingga `0` merujuk ke halaman pertama. Sesuaikan nilai ini untuk **export a different page** atau untuk mengulangi halaman ketika Anda perlu **save onenote as image** untuk masing‑masing.

### Langkah 4: Simpan Dokumen sebagai PNG (Simpan OneNote sebagai PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Memanggil `save` menulis halaman yang dipilih ke file PNG di disk. Nama file `ConvertSpecificPageToPngImage_out.png` hanya contoh—Anda dapat menamainya sesuka hati. Langkah akhir ini **exports onenote page image** siap digunakan dalam laporan, halaman web, atau pemrosesan lebih lanjut.

## Masalah Umum & Tips

- **Indeks halaman tidak tepat** – Ingat bahwa pengindeksan dimulai dari 0. Jika Anda mendapatkan gambar kosong, periksa nilai indeks.  
- **JAR Aspose.Note tidak ditemukan** – Pastikan JAR berada di classpath Anda; jika tidak, Anda akan melihat `ClassNotFoundException`.  
- **Halaman besar** – Untuk halaman yang sangat besar, pertimbangkan meningkatkan ukuran heap JVM (`-Xmx`) untuk menghindari `OutOfMemoryError`.  
- **Kontrol resolusi** – Gunakan `opts.setResolution(300)` (atau DPI apa pun yang Anda butuhkan) sebelum memanggil `save` untuk meningkatkan kejernihan gambar.  

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya mengonversi beberapa halaman menjadi gambar PNG sekaligus menggunakan Aspose.Note untuk Java?
A1: Ya, Anda dapat mengulangi halaman dokumen, memperbarui `opts.setPageIndex(i)`, dan memanggil `save` untuk setiap iterasi.

### Q2: Apakah Aspose.Note untuk Java mendukung format gambar lain selain PNG?
A2: Tentu saja. Anda dapat mengatur `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp`, atau `SaveFormat.Tiff` dalam `ImageSaveOptions`.

### Q3: Apakah tersedia versi percobaan gratis untuk Aspose.Note untuk Java?
A3: Ya, Anda dapat mengunduh versi percobaan gratis dari [situs web](https://releases.aspose.com/).

### Q4: Bisakah saya mendapatkan bantuan teknis jika mengalami masalah dengan Aspose.Note untuk Java?
A4: Tentu saja, Anda dapat mencari dukungan di forum komunitas Aspose [di sini](https://forum.aspose.com/c/note/28).

### Q5: Di mana saya dapat membeli lisensi untuk Aspose.Note untuk Java?
A5: Anda dapat membeli lisensi dari [halaman pembelian](https://purchase.aspose.com/buy).

### Q6: Bagaimana cara mengekspor halaman yang berisi gambar tersemat?
A6: Gambar tersemat secara otomatis dirender dalam output PNG; tidak diperlukan kode tambahan.

### Q7: Bisakah saya mengatur DPI atau resolusi gambar?
A7: Ya, gunakan `opts.setResolution(int dpi)` sebelum memanggil `save` untuk mengontrol kualitas output.

**Terakhir Diperbarui:** 2026-02-05  
**Diuji Dengan:** Aspose.Note for Java 24.11 (latest)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}