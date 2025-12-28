---
date: 2025-12-28
description: Pelajari cara **mengonversi OneNote ke gambar** dan mengatur resolusi
  gambar di Java menggunakan Aspose.Note. Panduan langkah demi langkah ini juga menunjukkan
  cara mengekspor file PNG OneNote.
linktitle: Convert OneNote to Image with Options - Aspose.Note
second_title: Aspose.Note Java API
title: Konversi OneNote ke Gambar dengan Opsi - Aspose.Note
url: /id/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi OneNote ke Gambar dengan Opsi - Aspose.Note

## Pendahuluan

Dalam tutorial ini, Anda akan belajar cara **mengonversi OneNote ke gambar** dengan berbagai opsi menggunakan Aspose.Note untuk Java. Apakah Anda membutuhkan PNG resolusi tinggi untuk pelaporan atau thumbnail JPEG cepat, langkah‑langkah di bawah ini menunjukkan secara tepat cara mencapainya dan mengintegrasikan proses tersebut ke dalam aplikasi Java Anda.

## Jawaban Cepat
- **Apa arti “mengonversi OneNote ke gambar”?** Ini mengubah seluruh notebook OneNote menjadi file gambar raster (PNG, JPEG, dll.).
- **Format apa yang direkomendasikan untuk kualitas tanpa kehilangan?** PNG, karena mempertahankan semua detail tanpa artefak kompresi.
- **Bagaimana cara mengatur resolusi gambar di Java?** Gunakan `ImageSaveOptions.setResolution(int dpi)` melalui `NotebookImageSaveOptions`.
- **Bisakah saya mengekspor notebook OneNote sebagai PNG dalam satu langkah?** Ya, Aspose.Note menyediakan satu panggilan `save` dengan opsi yang sesuai.
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi komersial diperlukan untuk produksi; versi percobaan gratis tersedia untuk evaluasi.

## Apa itu “mengonversi OneNote ke gambar”?
Mengonversi notebook OneNote ke gambar berarti merender setiap halaman notebook sebagai file bitmap. Ini berguna untuk membuat pratinjau statis, mengarsipkan konten, atau menyematkan halaman notebook ke dalam laporan di mana format OneNote asli tidak didukung.

## Mengapa menggunakan Aspose.Note untuk Java?
- **Kontrol penuh** atas format output, resolusi, dan kedalaman warna.  
- **Tanpa ketergantungan Microsoft Office** – bekerja pada lingkungan Java sisi server mana pun.  
- **Mendukung notebook kompleks** dengan file tersemat, tinta, dan teks kaya.

## Prasyarat

1. **Java Development Kit (JDK)** – versi 8 atau lebih tinggi.  
2. **Aspose.Note untuk Java JAR files** – unduh perpustakaan terbaru dari [here](https://releases.aspose.com/note/java/) dan tambahkan ke classpath proyek Anda.  

## Mengimpor Paket

Pertama, impor kelas‑kelas yang diperlukan untuk memuat notebook dan mengonfigurasi output gambar.

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Langkah 1: Memuat Notebook

Muat notebook OneNote yang ingin Anda konversi. Ganti path dengan lokasi file `.onetoc2` Anda.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## Langkah 2: Menetapkan Opsi Penyimpanan (Cara **menetapkan resolusi gambar java**)

Buat instance `NotebookImageSaveOptions`, pilih format output, dan tentukan resolusi yang diinginkan. Pada contoh ini kami menggunakan PNG pada 400 dpi.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

> **Tips pro:** Untuk pemrosesan lebih cepat pada notebook besar, turunkan resolusi (misalnya, 150 dpi). Tingkatkan untuk grafik siap cetak.

## Langkah 3: Menyimpan Notebook sebagai Gambar (Cara **mengekspor OneNote PNG**)

Tentukan nama file output dan panggil `save`. Opsi yang sama diterapkan pada setiap halaman dalam notebook.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

Kode di atas akan menghasilkan file PNG (atau serangkaian file PNG, satu per halaman) dengan resolusi yang Anda tetapkan.

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **OutOfMemoryError** pada notebook besar | Tingkatkan ukuran heap JVM (`-Xmx2g`) atau kurangi resolusi. |
| **Halaman kosong dalam output** | Pastikan notebook tidak dilindungi kata sandi; gunakan `Notebook.load(path, password)` bila diperlukan. |
| **Format gambar tidak didukung** | Gunakan hanya `SaveFormat.Png`, `SaveFormat.Jpeg`, atau `SaveFormat.Bmp` – format lain tidak didukung untuk ekspor notebook. |

## Pertanyaan yang Sering Diajukan

**T: Bisakah Aspose.Note menangani file OneNote yang kompleks?**  
J: Ya, ia memproses notebook dengan file tersemat, anotasi tinta, dan pemformatan kaya secara efisien.

**T: Apakah Aspose.Note untuk Java mudah diintegrasikan ke proyek yang sudah ada?**  
J: Tentu. API-nya sederhana, dan Anda hanya perlu menambahkan JAR ke classpath.

**T: Bisakah saya menyesuaikan output gambar saat mengonversi Notebook?**  
J: Ya. Anda dapat mengatur resolusi, format, bahkan kedalaman warna melalui `ImageSaveOptions`.

**T: Apakah Aspose.Note menyediakan dukungan untuk pengembang?**  
J: Ya. Aspose menyediakan dokumentasi lengkap, forum, dan saluran dukungan yang responsif.

**T: Apakah ada versi percobaan gratis untuk Aspose.Note untuk Java?**  
J: Ya, Anda dapat mengunduh versi percobaan dari [here](https://releases.aspose.com/).

---

**Terakhir Diperbarui:** 2025-12-28  
**Diuji Dengan:** Aspose.Note 24.11 untuk Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}