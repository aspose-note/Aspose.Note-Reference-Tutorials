---
date: 2026-03-24
description: Pelajari cara menyimpan OneNote sebagai gambar dan mengonversi OneNote
  menjadi gambar menggunakan Aspose.Note untuk Java. Panduan langkah demi langkah
  untuk pengembang Java.
linktitle: Save OneNote as Image – Convert Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Simpan OneNote sebagai Gambar – Konversi Notebook ke Gambar dengan Aspose.Note
url: /id/java/onenote-notebook-operations/convert-notebook-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan OneNote sebagai Gambar – Konversi Notebook ke Gambar dengan Aspose.Note

## Pendahuluan

Dalam tutorial ini Anda akan belajar **cara menyimpan OneNote sebagai gambar** dengan mengonversi notebook OneNote ke PNG (atau format gambar lainnya) menggunakan pustaka Aspose.Note untuk Java. Mengubah halaman notebook menjadi gambar sangat berguna ketika Anda perlu membagikan catatan di platform yang tidak mendukung file OneNote, menyematkannya dalam PDF, atau memasukkannya ke dalam slide presentasi.

## Jawaban Cepat
- **Library apa yang dibutuhkan?** Aspose.Note for Java.  
- **Format gambar apa yang didukung?** PNG, JPEG, BMP, GIF, TIFF, dll.  
- **Apakah saya membutuhkan lisensi?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Berapa lama proses konversi?** Biasanya beberapa detik per notebook, tergantung ukuran.  
- **Bisakah saya memproses notebook secara batch?** Ya – cukup lakukan loop pada file dan gunakan kembali kode yang sama.

## Apa itu **save OneNote as image**?

Menyimpan OneNote sebagai gambar berarti merender setiap halaman notebook `.one` menjadi file gambar raster (misalnya PNG). Ini menghasilkan representasi portabel yang hanya dapat dilihat dan dapat ditampilkan di mana saja tanpa memerlukan OneNote.

## Mengapa mengonversi OneNote ke gambar?

- **Berbagi lintas platform** – Penerima dapat melihat konten di perangkat apa pun.  
- **Menyisipkan dalam dokumen** – Sisipkan gambar ke Word, PowerPoint, atau PDF.  
- **Pengarsipan** – Simpan snapshot visual yang tidak akan berubah jika notebook asli diedit.  
- **Siap presentasi** – Gunakan PNG beresolusi tinggi langsung dalam slide.

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – Unduh JDK terbaru dari [website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).  
2. **Aspose.Note for Java library** – Dapatkan JAR dari [Aspose website](https://releases.aspose.com/note/java/) dan tambahkan ke classpath proyek Anda.

## Impor Paket

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Sekarang mari kita jalani proses konversi langkah demi langkah.

## Langkah 1: Muat Dokumen Notebook

```java
// Specify the directory where your notebook file is located
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

Kami mengarahkan API ke folder yang berisi `Sample1.one` dan memuatnya ke dalam objek `Document`. Dari sini Anda dapat mengakses halaman, bagian, dan elemen notebook lainnya.

## Langkah 2: Inisialisasi ImageSaveOptions

```java
// Initialize PdfSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` memberi tahu Aspose.Note bagaimana Anda ingin output dirender. Pada contoh ini kami memilih PNG, tetapi Anda dapat mengganti `SaveFormat.Png` dengan `SaveFormat.Jpeg`, `SaveFormat.Bmp`, dll., untuk **mengonversi OneNote ke gambar** dalam format lain.

## Langkah 3: Simpan Dokumen sebagai Gambar

```java
// Save the document as PNG
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Pemanggilan `save()` menulis halaman notebook yang telah dirender ke `ConvertToImage_out.png`. Jika notebook berisi beberapa halaman, Aspose.Note akan secara otomatis menghasilkan file gambar terpisah (misalnya `ConvertToImage_out_1.png`, `ConvertToImage_out_2.png`).

## Langkah 4: Cetak Konfirmasi

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Pesan konsol sederhana mengonfirmasi bahwa operasi **save OneNote as image** berhasil dan memberi tahu Anda di mana menemukan file output.

## Masalah Umum & Tips

- **Notebook besar** – Tingkatkan heap JVM (`-Xmx`) jika Anda mengalami `OutOfMemoryError`.  
- **Kontrol resolusi** – Gunakan `options.setResolution(300);` untuk meningkatkan DPI gambar kualitas cetak.  
- **Konversi batch** – Bungkus langkah-langkah di atas dalam `for` loop yang mengiterasi daftar file `.one`.  

## FAQ

### Q1: Bisakah saya mengonversi notebook ke format gambar lain selain PNG?

A1: Ya, Anda bisa. Pustaka Aspose.Note mendukung berbagai format gambar seperti JPEG, BMP, GIF, TIFF, dll. Anda dapat menentukan format yang diinginkan dalam objek `ImageSaveOptions` sesuai kebutuhan.

### Q2: Apakah Aspose.Note kompatibel dengan semua versi OneNote?

A2: Aspose.Note menyediakan dukungan komprehensif untuk berbagai versi OneNote, memastikan kompatibilitas di berbagai lingkungan dan format file.

### Q3: Bisakah saya menyesuaikan pengaturan output gambar selama konversi?

A3: Tentu saja. Aspose.Note menawarkan opsi luas untuk menyesuaikan gambar output, termasuk resolusi, kualitas, kedalaman warna, dan lainnya. Anda dapat menyesuaikan pengaturan ini sesuai kebutuhan Anda.

### Q4: Apakah Aspose.Note mendukung konversi batch banyak notebook?

A4: Ya, Anda dapat mengonversi batch banyak notebook menjadi gambar secara efisien menggunakan Aspose.Note. Cukup iterasi melalui daftar file notebook Anda dan terapkan proses konversi yang dijelaskan dalam tutorial ini.

### Q5: Di mana saya dapat menemukan sumber daya tambahan dan dukungan untuk Aspose.Note?

A5: Untuk dokumentasi lebih lanjut, contoh, dan dukungan komunitas, kunjungi [Aspose.Note forum](https://forum.aspose.com/c/note/28) dan jelajahi [documentation](https://reference.aspose.com/note/java/).

---

**Last Updated:** 2026-03-24  
**Tested With:** Aspose.Note for Java 24.8  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}