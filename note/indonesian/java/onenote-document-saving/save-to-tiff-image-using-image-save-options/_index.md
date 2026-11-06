---
date: 2026-11-05
description: Pelajari cara mengurangi ukuran file TIFF saat mengonversi notebook OneNote
  ke TIFF di Java menggunakan Aspose.Note. Termasuk opsi JPEG, PackBits, dan TIFF
  hitam‑putih.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Cara mengurangi ukuran file TIFF saat mengonversi OneNote di Java
og_description: Pelajari cara mengurangi ukuran file TIFF saat mengonversi notebook
  OneNote ke TIFF di Java menggunakan Aspose.Note. Termasuk opsi JPEG, PackBits, dan
  TIFF hitam‑putih.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Cara mengurangi ukuran file TIFF saat mengonversi OneNote di Java
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Cara mengurangi ukuran file TIFF saat mengonversi OneNote di Java
url: /id/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara mengurangi ukuran file TIFF saat mengonversi OneNote di Java

## Pendahuluan

Dalam tutorial ini Anda akan menemukan cara **mengurangi ukuran file TIFF** saat mengonversi notebook OneNote menjadi gambar TIFF menggunakan Aspose.Note untuk Java. Kami akan membahas tiga metode kompresi—TIFF JPEG, PackBits, dan CCITT Group 3 (TIFF hitam‑putih)—menunjukkan cara menyesuaikan kualitas gambar, mengontrol mode warna, dan menjaga ukuran file tetap optimal untuk web, arsip, atau skenario tipe faks.

## Jawaban cepat

- **Apa itu kompresi TIFF JPEG?** Metode kompresi lossy yang mengurangi ukuran file TIFF sambil mempertahankan kualitas visual.  
- **Perpustakaan mana yang menangani konversi?** Aspose.Note untuk Java.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi diperlukan untuk produksi.  
- **Bisakah saya mengubah kualitas gambar?** Ya, atur properti `quality` pada `ImageSaveOptions`.  
- **Apakah konversi batch memungkinkan?** Tentu – lakukan loop melalui dokumen dan terapkan opsi yang sama.

## Gambaran umum kompresi TIFF JPEG

Kompresi TIFF JPEG menyimpan data gambar dalam kontainer TIFF tetapi menerapkan algoritma lossy JPEG untuk memperkecil file. Ini ideal ketika Anda membutuhkan keseimbangan antara **kualitas gambar tiff** dan ukuran file yang lebih kecil, terutama untuk skenario web atau arsip.

## Mengapa menggunakan tipe kompresi TIFF yang berbeda?

Anda memilih tipe kompresi berdasarkan konten dan kebutuhan penyimpanan: JPEG paling cocok untuk foto, PackBits menyediakan kompresi loss‑less untuk grafik dengan area seragam yang besar, dan CCITT Group 3 memberikan kompresi rasio tinggi untuk dokumen gaya faks monokrom. Memilih metode yang tepat memungkinkan Anda **mengurangi ukuran file TIFF** tanpa mengorbankan kesetiaan visual yang dibutuhkan aplikasi Anda.

## Memilih kompresi yang tepat

- **JPEG** – Kualitas dapat disesuaikan (0‑100) memungkinkan Anda menyeimbangkan ukuran vs. detail, sempurna untuk halaman berwarna kaya.  
- **PackBits** – Enkoding run‑length loss‑less; ideal ketika Anda harus mempertahankan setiap piksel secara tepat.  
- **CCITT Group 3** – Hanya monokrom; memaksimalkan kompresi untuk teks yang dipindai atau dokumen faks.  

## Mengonversi OneNote ke TIFF menggunakan Aspose.Note

Jika tujuan Anda adalah **mengonversi OneNote ke TIFF**, tiga metode di bawah ini mencakup skenario paling umum. Setiap metode memuat file `.one`, mengonfigurasi `ImageSaveOptions`, dan menyimpan hasilnya sebagai file `.tiff`.

## Prasyarat

- Java Development Kit (JDK) terpasang.  
- Perpustakaan Aspose.Note untuk Java ditambahkan ke proyek Anda (Maven/Gradle atau JAR manual).  
- Pemahaman dasar tentang sintaks Java.

## Impor paket

Kelas `ImageSaveOptions`, `TiffCompression`, dan `ColorMode` adalah inti dari API konversi.  

`ImageSaveOptions` mendefinisikan opsi untuk menyimpan gambar, seperti format dan kompresi.  
`TiffCompression` mengenumerasi algoritma kompresi TIFF yang didukung.  
`ColorMode` menentukan kedalaman warna, misalnya warna atau hitam‑putih.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Langkah 1: menyimpan ke TIFF menggunakan kompresi TIFF JPEG

### Menyimpan TIFF dengan kompresi JPEG di Java

Muat file OneNote, konfigurasikan `ImageSaveOptions` dengan kompresi JPEG, secara opsional atur nilai `quality`, dan panggil metode save. Pola dua langkah ini memberi Anda kontrol penuh atas ukuran output dan kesetiaan visual.

1. Arahkan `dataDir` ke folder yang berisi file `.one` Anda.  
2. Panggil `SaveToTiffUsingJpegCompression()` dari metode utama atau layanan Anda.  
3. File `.tiff` yang dihasilkan akan muncul di direktori yang sama.

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Penjelasan**

- `ImageSaveOptions` memberi tahu Aspose.Note untuk menghasilkan file TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` memilih kompresi JPEG.  
- `setQuality(93)` (opsional) menyesuaikan kualitas gambar; nilai yang lebih rendah menghasilkan file yang lebih kecil.

## Gambaran umum kompresi TIFF PackBits

PackBits adalah algoritma kompresi lossless yang paling cocok untuk gambar dengan area warna solid yang besar. Ini sering disebut **tiff packbits compression** dalam dokumentasi.

## Menyimpan TIFF dengan kompresi PackBits di Java

Jika Anda membutuhkan opsi loss‑less, PackBits adalah algoritma run‑length sederhana yang bekerja baik untuk grafik dengan warna solid. Konfigurasikan `ImageSaveOptions` dengan `TiffCompression.PackBits` dan simpan dokumen.

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Penjelasan**

- `setTiffCompression(TiffCompression.PackBits)` mengubah metode kompresi.  
- Tidak diperlukan pengaturan kualitas karena PackBits bersifat loss‑less.

## Menyimpan TIFF dengan kompresi CCITT Group 3 di Java

Untuk dokumen gaya faks, Anda sering menginginkan **TIFF hitam putih**. CCITT Group 3 memberikan kompresi tinggi untuk gambar monokrom. Atur mode warna ke hitam‑putih dan pilih enum kompresi CCITT 3.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Penjelasan**

- `setColorMode(ColorMode.BlackAndWhite)` memaksa output monokrom.  
- `setTiffCompression(TiffCompression.Ccitt3)` menerapkan kompresi yang berorientasi faks.

## Masalah umum & tips

| Issue | Solution |
|-------|----------|
| **File output lebih besar dari yang diharapkan** | Coba kurangi nilai `quality` JPEG atau beralih ke PackBits jika lossless dapat diterima. |
| **Warna tampak pudar** | Pastikan Anda tidak secara tidak sengaja mengatur `ColorMode.BlackAndWhite` ketika Anda membutuhkan warna penuh. |
| **Kesalahan format gambar tidak didukung** | Verifikasi bahwa Anda menggunakan versi terbaru Aspose.Note; build lama mungkin tidak memiliki beberapa enum kompresi. |
| **LicenseException saat runtime** | Instal lisensi Aspose.Note yang valid (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Pertanyaan yang sering diajukan

**Q: Bisakah saya mengonversi tipe dokumen lain (mis., PDF, DOCX) ke TIFF dengan opsi ini?**  
A: Ya. Meskipun Aspose.Note berfokus pada file OneNote, Aspose.PDF, Aspose.Words, dan perpustakaan lain menyediakan `ImageSaveOptions` serupa untuk format mereka.

**Q: Bagaimana kompresi TIFF JPEG berbeda dari file JPEG standar?**  
A: Algoritma JPEG sama, tetapi data gambar berada di dalam kontainer TIFF, yang dapat menampung banyak halaman dan metadata yang lebih kaya.

**Q: Apakah memungkinkan memproses batch banyak file `.one`?**  
A: Tentu. Iterasi melalui direktori, panggil salah satu dari tiga metode untuk setiap file, dan kumpulkan TIFF yang dihasilkan.

**Q: Bisakah saya mengontrol DPI/resolusi TIFF output?**  
A: Ya. Gunakan `options.setResolution(int dpi)` sebelum menyimpan.

**Q: Apakah Aspose.Note mendukung pemrosesan asynchronous?**  
A: API itu sendiri bersifat sinkron, tetapi Anda dapat membungkus panggilan dalam `CompletableFuture` Java atau pool thread untuk eksekusi paralel.

## Kesimpulan

Anda kini memiliki toolkit **konversi TIFF Java** lengkap yang memungkinkan Anda **mengurangi ukuran file TIFF** saat menyimpan dokumen OneNote sebagai file TIFF menggunakan kompresi JPEG, PackBits, atau CCITT Group 3 Fax. Sesuaikan kualitas, mode warna, dan resolusi untuk memenuhi kebutuhan spesifik Anda, dan integrasikan metode ini ke dalam alur kerja batch untuk produktivitas maksimal.

---

**Terakhir diperbarui:** 2026-11-05  
**Diuji dengan:** Aspose.Note for Java 26.4 (latest at time of writing)  
**Penulis:** Aspose

## Tutorial Terkait

- [Cara Merender Gambar Halaman OneNote (JPEG) Menggunakan Save Format dengan Aspose.Note untuk Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Gunakan Aspose.Note untuk Java untuk Menyimpan OneNote sebagai PNG dengan Opsi – Mengonversi Notebook ke Gambar](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [Cara Mengekspor OneNote sebagai Gambar Grayscale – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}