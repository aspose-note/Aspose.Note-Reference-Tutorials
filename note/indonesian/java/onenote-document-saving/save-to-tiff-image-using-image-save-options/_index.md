---
date: 2025-12-17
description: Pelajari cara menyimpan dokumen OneNote sebagai file TIFF menggunakan
  kompresi TIFF JPEG, PackBits, atau CCITT Group 3 Fax di Java. Kendalikan kualitas
  gambar, ukuran file, dan mode warna dengan Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Simpan ke Gambar TIFF Menggunakan Kompresi JPEG TIFF di OneNote
url: /id/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan ke Gambar TIFF Menggunakan Kompresi TIFF JPEG di OneNote

## Pendahuluan

Dalam tutorial ini Anda akan menemukan **cara menyimpan dokumen OneNote ke file TIFF menggunakan kompresi TIFF JPEG** dan dua metode kompresi populer lainnya. Kami akan menjelaskan langkah‑langkah pengaturan yang diperlukan, mengimpor paket Java yang diperlukan, dan menyediakan kode langkah‑demi‑langkah yang jelas untuk setiap opsi kompresi. Pada akhir tutorial Anda akan dapat mengontrol **kualitas gambar TIFF**, mengurangi ukuran file, dan bahkan menghasilkan TIFF hitam‑putih untuk output bergaya faks.

## Jawaban Cepat
- **Apa itu kompresi TIFF JPEG?** Metode kompresi lossy yang mengurangi ukuran file TIFF sambil mempertahankan kualitas visual.  
- **Perpustakaan mana yang menangani konversi?** Aspose.Note untuk Java.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi diperlukan untuk produksi.  
- **Bisakah saya mengubah kualitas gambar?** Ya, atur properti `quality` pada `ImageSaveOptions`.  
- **Apakah konversi batch memungkinkan?** Tentu – lakukan perulangan pada dokumen dan terapkan opsi yang sama.

## Apa itu Kompresi TIFF JPEG?

Kompresi TIFF JPEG menyimpan data gambar dalam kontainer TIFF tetapi menerapkan algoritma lossy JPEG untuk memperkecil file. Ini ideal ketika Anda membutuhkan keseimbangan antara **kualitas gambar tiff** dan ukuran file yang lebih kecil, terutama untuk skenario web atau arsip.

## Mengapa Menggunakan Berbagai Jenis Kompresi TIFF?

- **JPEG** – Baik untuk foto; menawarkan kualitas yang dapat disesuaikan.  
- **PackBits** – Pengkodean run‑length sederhana dan loss‑less; berguna untuk grafik dengan area seragam yang besar.  
- **CCITT Group 3 Fax** – Hanya hitam‑putih; sempurna untuk dokumen yang dipindai dan transmisi faks.  

Memilih kompresi yang tepat memungkinkan Anda memenuhi batasan penyimpanan tanpa mengorbankan kesetiaan visual yang diperlukan untuk aplikasi Anda.

## Prasyarat

- Java Development Kit (JDK) terpasang.  
- Perpustakaan Aspose.Note untuk Java ditambahkan ke proyek Anda (Maven/Gradle atau JAR manual).  
- Pemahaman dasar tentang sintaks Java.

## Impor Paket

Pertama, masukkan kelas Aspose.Note yang diperlukan ke dalam file Java Anda:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Langkah 1: Simpan ke TIFF Menggunakan Kompresi TIFF JPEG

Berikut adalah metode lengkap yang memuat file OneNote dan menyimpannya sebagai TIFF dengan kompresi JPEG. Sesuaikan nilai `quality` (0‑100) untuk mengontrol **kualitas gambar tiff**.

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

### Cara Menyimpan TIFF dengan Kompresi JPEG di Java
1. Arahkan `dataDir` ke folder yang berisi file `.one` Anda.  
2. Panggil `SaveToTiffUsingJpegCompression()` dari metode utama atau layanan Anda.  
3. File `.tiff` yang dihasilkan akan muncul di direktori yang sama.

## Langkah 2: Simpan ke TIFF Menggunakan Kompresi PackBits

Jika Anda memerlukan opsi loss‑less, PackBits adalah algoritma run‑length sederhana yang bekerja baik untuk grafik dengan warna solid.

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

## Langkah 3: Simpan ke TIFF Menggunakan Kompresi CCITT Group 3 Fax (TIFF Hitam‑Putih)

Untuk dokumen bergaya faks, Anda sering menginginkan **TIFF hitam‑putih**. CCITT Group 3 memberikan kompresi tinggi untuk gambar monokrom.

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

## Masalah Umum & Tips

| Masalah | Solusi |
|-------|----------|
| **File output lebih besar dari yang diharapkan** | Coba kurangi nilai `quality` JPEG atau beralih ke PackBits jika lossless dapat diterima. |
| **Warna tampak pudar** | Pastikan Anda tidak secara tidak sengaja mengatur `ColorMode.BlackAndWhite` ketika Anda membutuhkan warna penuh. |
| **Kesalahan format gambar tidak didukung** | Pastikan Anda menggunakan versi terbaru Aspose.Note; build lama mungkin tidak memiliki beberapa enum kompresi. |
| **LicenseException saat runtime** | Instal lisensi Aspose.Note yang valid (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya mengonversi tipe dokumen lain (mis., PDF, DOCX) ke TIFF dengan opsi ini?**  
A: Ya. Aspose.Note berfokus pada file OneNote, tetapi perpustakaan Aspose lainnya (PDF, Words) menyediakan `ImageSaveOptions` serupa untuk format masing‑masing.

**Q: Bagaimana kompresi TIFF JPEG berbeda dari file JPEG standar?**  
A: Data gambar disimpan di dalam kontainer TIFF, mempertahankan metadata dan memungkinkan banyak halaman, sementara algoritma kompresi tetap JPEG.

**Q: Apakah memungkinkan memproses batch banyak file `.one`?**  
A: Tentu. Lakukan perulangan pada folder, panggil salah satu dari tiga metode per file, dan kumpulkan TIFF yang dihasilkan.

**Q: Bisakah saya mengontrol DPI/resolusi output TIFF?**  
A: Ya. Gunakan `options.setResolution(int dpi)` sebelum menyimpan.

**Q: Apakah Aspose.Note mendukung pemrosesan asynchronous?**  
A: API itu sendiri bersifat sinkron, tetapi Anda dapat membungkus panggilan dalam `CompletableFuture` Java atau thread pool untuk eksekusi paralel.

## Kesimpulan

Anda kini memiliki toolkit **konversi tiff java** lengkap yang memungkinkan Anda menyimpan dokumen OneNote sebagai file TIFF menggunakan kompresi JPEG, PackBits, atau CCITT Group 3 Fax. Sesuaikan kualitas, mode warna, dan resolusi untuk memenuhi persyaratan **kualitas gambar tiff** spesifik Anda, dan integrasikan metode ini ke dalam alur kerja batch untuk produktivitas maksimal.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}