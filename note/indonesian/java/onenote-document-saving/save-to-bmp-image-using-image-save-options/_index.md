---
date: 2026-03-05
description: Pelajari cara mengekspor dokumen OneNote ke gambar BMP menggunakan Image
  Save Options dari Aspose.Note untuk Java. Juga lihat cara mengonversi OneNote ke
  PDF atau menyimpan OneNote sebagai PNG.
linktitle: how to export onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: Cara mengekspor OneNote ke Gambar BMP Menggunakan Opsi Simpan Gambar
url: /id/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# cara mengekspor onenote ke BMP Image Menggunakan Image Save Options

## Cara mengekspor onenote ke BMP Image

Aspose.Note for Java adalah pustaka yang kuat yang memungkinkan pengembang Java untuk bekerja dengan file Microsoft OneNote secara programatis. **Dalam tutorial ini Anda akan belajar cara mengekspor dokumen onenote ke gambar BMP** menggunakan fitur Image Save Options dari Aspose.Note for Java. Kami akan memandu setiap langkah, menjelaskan mengapa Anda mungkin memilih BMP dibandingkan format lain, dan menunjukkan cara mengintegrasikan kemampuan ini ke dalam aplikasi Anda.

## Jawaban Cepat
- **Apa yang dilakukan kelas Image Save Options?** Kelas ini memungkinkan Anda menentukan format gambar output (BMP, PNG, JPEG, dll.) saat mengonversi halaman OneNote.  
- **Apakah saya memerlukan lisensi untuk menjalankan contoh?** Versi percobaan gratis dapat digunakan untuk evaluasi, tetapi lisensi komersial diperlukan untuk penggunaan produksi.  
- **Bisakah saya mengonversi halaman OneNote ke PDF atau PNG alih-alih BMP?** Ya – cukup ubah enum `SaveFormat` (misalnya, `SaveFormat.Pdf` atau `SaveFormat.Png`).  
- **Versi Java mana yang didukung?** Java 8 dan yang lebih baru didukung sepenuhnya.  
- **Apakah ada penanganan khusus untuk dokumen besar?** Anda dapat melakukan streaming output untuk menghindari konsumsi memori yang tinggi.

## Apa itu “Image Save Options” di Aspose.Note?
Kelas `ImageSaveOptions` menyediakan kontrol yang sangat detail tentang bagaimana halaman OneNote dirender sebagai gambar raster. Anda dapat mengatur format gambar, resolusi, kedalaman warna, dan lainnya. Fleksibilitas ini memudahkan **mengekspor gambar halaman onenote** untuk sistem warisan (BMP) atau skenario web modern (PNG/JPEG).  

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

1. Pengetahuan dasar tentang bahasa pemrograman Java.  
2. JDK (Java Development Kit) terinstal di mesin Anda.  
3. IDE seperti Eclipse atau IntelliJ IDEA.  
4. Pustaka Aspose.Note for Java – unduh dari [here](https://releases.aspose.com/note/java/).

## Impor Paket

Pertama, impor kelas Aspose.Note yang diperlukan dan utilitas I/O standar Java:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Langkah 1: Muat Dokumen OneNote

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Di sini kami menunjuk ke folder yang berisi file OneNote sumber (`Aspose.one`) dan memuatnya ke dalam objek `Document`. Objek ini memberi Anda akses penuh ke halaman, bagian, dan elemen lain dalam notebook.

## Langkah 2: Simpan Dokumen sebagai Gambar BMP

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

Kami menggabungkan nama file output, kemudian memanggil `save` dengan instance `ImageSaveOptions` yang dikonfigurasi untuk **BMP** (`SaveFormat.Bmp`).  
Jika Anda ingin **menyimpan halaman onenote** sebagai PNG, cukup ganti `SaveFormat.Bmp` dengan `SaveFormat.Png`. Demikian pula, `SaveFormat.Pdf` memungkinkan Anda melakukan konversi **onenote ke pdf**.

## Mengapa Memilih BMP?
- **Kualitas lossless** – BMP menyimpan data piksel mentah, mempertahankan tampilan asli halaman secara tepat.  
- **Kompatibilitas** – Aplikasi Windows lama sering memerlukan file BMP.  
- **Kesederhanaan** – Tanpa artefak kompresi, menjadikannya ideal untuk pemrosesan gambar lanjutan.

## Masalah Umum & Tips

- **Kesalahan jalur file** – Pastikan `dataDir` diakhiri dengan pemisah file yang sesuai (`/` atau `\`).  
- **Notebook besar** – Untuk file OneNote yang sangat besar, pertimbangkan menyimpan setiap halaman secara terpisah untuk menjaga penggunaan memori tetap rendah.  
- **Pengecualian lisensi** – Menjalankan kode tanpa lisensi yang valid akan menambahkan watermark pada gambar yang dihasilkan.

## Kesimpulan

Dalam panduan ini kami menunjukkan **cara mengekspor onenote** dokumen ke gambar BMP menggunakan `ImageSaveOptions` dari Aspose.Note for Java. Dengan mengganti enum `SaveFormat`, Anda juga dapat menghasilkan PNG, JPEG, PDF, atau format lain yang didukung, memberikan cara fleksibel untuk mengekspor konten OneNote untuk skenario downstream apa pun.

## Pertanyaan yang Sering Diajukan

**Q1: Bisakah saya menyimpan dokumen OneNote ke format gambar lain selain BMP?**  
A: Ya, Anda dapat menggunakan `ImageSaveOptions` dengan `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif`, atau `SaveFormat.Tiff` untuk mengekspor ke format tersebut.

**Q2: Apakah Aspose.Note for Java mendukung konversi antara format dokumen yang berbeda?**  
A: Tentu saja. Selain format gambar, Anda dapat mengonversi file OneNote ke PDF, DOCX, HTML, dan lainnya menggunakan `SaveFormat` yang sesuai.

**Q3: Apakah Aspose.Note for Java kompatibel dengan versi OneNote terbaru?**  
A: Ya, pustaka ini secara rutin diperbarui agar tetap selaras dengan rilis OneNote terbaru.

**Q4: Bisakah saya memanipulasi konten dokumen OneNote secara programatis?**  
A: Ya, Anda dapat menambah, mengedit, atau menghapus halaman, bagian, dan konten kaya (teks, gambar, tabel) melalui API.

**Q5: Apakah Aspose.Note for Java menyediakan dukungan teknis?**  
A: Ya, Aspose menyediakan dukungan teknis dan forum khusus. Kunjungi [Aspose.Note forum](https://forum.aspose.com/c/note/28) untuk bantuan.

---

**Terakhir Diperbarui:** 2026-03-05  
**Diuji Dengan:** Aspose.Note for Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}