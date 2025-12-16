---
date: 2025-12-16
description: Pelajari cara menyimpan dokumen OneNote ke gambar BMP menggunakan opsi
  penyimpanan gambar Aspose.Note untuk Java. Juga lihat cara menyimpan OneNote ke
  PDF atau PNG.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: Cara Menyimpan OneNote ke Gambar BMP Menggunakan Opsi Simpan Gambar
url: /id/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# cara menyimpan onenote ke Gambar BMP Menggunakan Opsi Penyimpanan Gambar

## Introduction

Aspose.Note for Java adalah perpustakaan kuat yang memungkinkan pengembang Java bekerja dengan file Microsoft OneNote secara programatis. **Dalam tutorial ini Anda akan belajar cara menyimpan dokumen onenote ke gambar BMP** menggunakan fitur Image Save Options dari Aspose.Note for Java. Kami akan membimbing Anda melalui setiap langkah, menjelaskan mengapa Anda mungkin memilih BMP dibandingkan format lain, dan menunjukkan cara mengintegrasikan kemampuan ini ke dalam aplikasi Anda.

## Quick Answers
- **Apa yang dilakukan kelas Image Save Options?** Kelas ini memungkinkan Anda menentukan format gambar output (BMP, PNG, JPEG, dll.) saat mengonversi halaman OneNote.  
- **Apakah saya memerlukan lisensi untuk menjalankan contoh?** Versi percobaan gratis dapat digunakan untuk evaluasi, tetapi lisensi komersial diperlukan untuk penggunaan produksi.  
- **Bisakah saya mengonversi halaman OneNote ke PDF atau PNG alih-alih BMP?** Ya – cukup ubah enum `SaveFormat` (misalnya `SaveFormat.Pdf` atau `SaveFormat.Png`).  
- **Versi Java mana yang didukung?** Java 8 dan versi selanjutnya sepenuhnya didukung.  
- **Apakah ada penanganan khusus untuk dokumen besar?** Anda dapat melakukan streaming output untuk menghindari konsumsi memori yang tinggi.

## What is “Image Save Options” in Aspose.Note?
Kelas `ImageSaveOptions` menyediakan kontrol detail tentang bagaimana halaman OneNote dirender sebagai gambar raster. Anda dapat mengatur format gambar, resolusi, kedalaman warna, dan lainnya. Fleksibilitas ini memudahkan pembuatan file BMP untuk sistem legacy atau file PNG/JPEG untuk penggunaan web.

## Prerequisites

Sebelum Anda memulai, pastikan Anda memiliki:

1. Pengetahuan dasar tentang bahasa pemrograman Java.  
2. JDK (Java Development Kit) terinstal di mesin Anda.  
3. IDE seperti Eclipse atau IntelliJ IDEA.  
4. Perpustakaan Aspose.Note for Java – unduh dari [here](https://releases.aspose.com/note/java/).

## Import Packages

Pertama, impor kelas Aspose.Note yang diperlukan dan utilitas I/O standar Java:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Step 1: Load the OneNote Document

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Di sini kami menunjuk ke folder yang berisi file OneNote sumber (`Aspose.one`) dan memuatnya ke dalam objek `Document`. Objek ini memberi Anda akses penuh ke halaman, bagian, dan elemen lain dalam notebook.

## Step 2: Save the Document as a BMP Image

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

Kami menggabungkan nama file output, lalu memanggil `save` dengan instance `ImageSaveOptions` yang dikonfigurasi untuk **BMP** (`SaveFormat.Bmp`).  
Jika Anda ingin **menyimpan halaman onenote** sebagai PNG, cukup ganti `SaveFormat.Bmp` dengan `SaveFormat.Png`. Demikian pula, `SaveFormat.Pdf` memungkinkan Anda melakukan konversi **onenote ke pdf**.

## Why Choose BMP?
- **Kualitas lossless** – BMP menyimpan data piksel mentah, mempertahankan tampilan asli halaman secara tepat.  
- **Kompatibilitas** – Aplikasi Windows lama sering memerlukan file BMP.  
- **Kesederhanaan** – Tanpa artefak kompresi, menjadikannya ideal untuk pemrosesan gambar lanjutan.

## Common Issues & Tips

- **Kesalahan jalur file** – Pastikan `dataDir` diakhiri dengan pemisah file yang tepat (`/` atau `\`).  
- **Notebook besar** – Untuk file OneNote yang sangat besar, pertimbangkan menyimpan setiap halaman secara terpisah untuk menjaga penggunaan memori tetap rendah.  
- **Pengecualian lisensi** – Menjalankan kode tanpa lisensi yang valid akan menambahkan watermark pada gambar yang dihasilkan.

## Conclusion

Dalam panduan ini kami menunjukkan **cara menyimpan onenote** dokumen ke gambar BMP menggunakan `ImageSaveOptions` dari Aspose.Note for Java. Dengan mengganti enum `SaveFormat` Anda juga dapat menghasilkan PNG, JPEG, PDF, atau format lain yang didukung, memberikan cara fleksibel untuk mengekspor konten OneNote untuk skenario downstream apa pun.

## Frequently Asked Questions

**Q1: Bisakah saya menyimpan dokumen OneNote ke format gambar lain selain BMP?**  
A: Ya, Anda dapat menggunakan `ImageSaveOptions` dengan `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif`, atau `SaveFormat.Tiff` untuk mengekspor ke format tersebut.

**Q2: Apakah Aspose.Note for Java mendukung konversi antar format dokumen yang berbeda?**  
A: Tentu saja. Selain format gambar, Anda dapat mengonversi file OneNote ke PDF, DOCX, HTML, dan lainnya menggunakan `SaveFormat` yang sesuai.

**Q3: Apakah Aspose.Note for Java kompatibel dengan versi OneNote terbaru?**  
A: Ya, perpustakaan ini secara rutin diperbarui agar tetap selaras dengan rilis OneNote terbaru.

**Q4: Bisakah saya memanipulasi konten dokumen OneNote secara programatis?**  
A: Ya, Anda dapat menambah, mengedit, atau menghapus halaman, bagian, dan konten kaya (teks, gambar, tabel) melalui API.

**Q5: Apakah Aspose.Note for Java menyediakan dukungan teknis?**  
A: Ya, Aspose menawarkan dukungan teknis dan forum khusus. Kunjungi [Aspose.Note forum](https://forum.aspose.com/c/note/28) untuk bantuan.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2025-12-16  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose