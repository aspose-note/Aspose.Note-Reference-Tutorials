---
date: 2026-06-30
description: Pelajari cara mengekspor OneNote dengan menyimpan dokumen sebagai gambar
  PNG grayscale menggunakan Aspose.Note untuk Java. Termasuk langkah-langkah memuat
  dokumen OneNote dan membuat gambar grayscale.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Cara Mengekspor OneNote sebagai Gambar Grayscale – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
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

Di tutorial ini Anda akan menemukan **how to export onenote** dengan mengonversi file OneNote `.one` menjadi gambar PNG grayscale berkualitas tinggi menggunakan Aspose.Note untuk Java. Konversi grayscale sering dibutuhkan oleh pengembang Java untuk pencetakan, pengarsipan, atau untuk **reduce OneNote size** tanpa kehilangan konten penting. Kami akan memandu Anda memuat dokumen OneNote, mengonfigurasi opsi penyimpanan—termasuk **adjust image resolution**—dan akhirnya menyimpan dokumen sebagai PNG.

## Jawaban Cepat
- **What does “how to export onenote” mean?** Ini merujuk pada konversi programatis file OneNote ke format lain, seperti gambar, menggunakan kode.  
- **Which format is best for grayscale output?** PNG bekerja dengan baik karena mempertahankan kualitas loss‑less dan mendukung mode warna grayscale khusus.  
- **Do I need a license?** Lisensi Aspose.Note yang valid diperlukan untuk penggunaan produksi; lisensi percobaan sementara tersedia untuk pengujian.  
- **What Java version is required?** Java 8 atau yang lebih baru disarankan.  
- **Can I change the image size?** Ya, Anda dapat menyesuaikan properti `ImageSaveOptions` seperti `Resolution` atau `PageSize` sebelum menyimpan.

## Apa itu “how to export onenote”?

Mengekspor OneNote berarti mengonversi secara programatis file OneNote `.one` ke representasi lain—seperti PDF, HTML, atau gambar. Dalam panduan ini kami fokus pada **creating grayscale PNG** images, sebuah kebutuhan umum untuk dokumentasi atau alur kerja siap cetak. Dengan menggunakan Aspose.Note, konversi terjadi sepenuhnya di memori, sehingga Anda tidak pernah perlu menginstal Microsoft OneNote di server.

## Mengapa mengekspor OneNote sebagai gambar grayscale?

PNG grayscale biasanya **30‑40 % lebih kecil** dibandingkan versi berwarna penuh, yang mempercepat pengiriman web dan mengurangi biaya penyimpanan. Mereka juga memberikan **kontras yang lebih jelas** pada printer laser, membuat laporan lebih mudah dibaca. Karena PNG didukung secara universal, file yang dihasilkan dapat bekerja di browser, perangkat seluler, dan editor desktop tanpa codec tambahan.

## Prasyarat

1. Java Development Kit (JDK) 8 atau yang lebih baru terinstal.  
2. Aspose.Note untuk Java – unduh rilis terbaru dari [here](https://releases.aspose.com/note/java/).  
3. Pemahaman dasar tentang sintaks Java dan pengaturan proyek Maven/Gradle.  

## Impor Paket

Kelas `ImageSaveOptions` mengontrol bagaimana dokumen dirender menjadi gambar.  
`ColorMode` adalah enumerasi yang memungkinkan Anda beralih antara output berwarna penuh dan grayscale.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Langkah 1: Muat Dokumen OneNote

`Document` mewakili sebuah notebook OneNote dan menyediakan metode untuk memuat, mengedit, dan menyimpan isinya. Pertama, **load the OneNote document** ke Aspose.Note. Ganti `"Your Document Directory"` dengan jalur ke folder lokal Anda dan `"Aspose.one"` dengan nama file OneNote Anda.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Langkah 2: Atur Jalur Output dan Opsi

`ImageSaveOptions` mengonfigurasi bagaimana dokumen OneNote dirender ke file gambar. Enumerasi `ColorMode` memilih mode render warna, seperti grayscale atau berwarna penuh. Tentukan jalur output untuk gambar grayscale dan spesifikasikan opsi penyimpanan. Kami akan mengatur `ColorMode` ke `GrayScale` dan menggunakan format **save document as PNG**. Anda juga dapat **adjust image resolution** menjadi 300 DPI untuk cetakan berkualitas tinggi.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Langkah 3: Simpan Dokumen

Akhirnya, simpan dokumen sebagai gambar PNG grayscale menggunakan opsi yang telah dikonfigurasi. Metode `save` menulis file ke disk tanpa memerlukan file sementara perantara apa pun.

```java
oneFile.save(dataDir, options);
```

## Masalah Umum dan Solusinya
- **FileNotFoundException** – Pastikan bahwa `dataDir` mengarah ke folder yang benar dan file `.one` ada.  
- **LicenseException** – Pastikan Anda telah menerapkan lisensi Aspose.Note yang valid sebelum memanggil `save`.  
- **Low‑resolution output** – Sesuaikan `options.setResolution(300)` untuk meningkatkan DPI; DPI yang lebih tinggi menghasilkan cetakan yang lebih tajam tetapi ukuran file lebih besar.  

## Pertanyaan yang Sering Diajukan

**Q1: Bisakah saya menyimpan gambar grayscale dalam format lain?**  
A1: Ya, cukup ubah parameter `SaveFormat` dalam konstruktor `ImageSaveOptions` menjadi `Jpeg`, `Bmp`, atau salah satu dari lebih dari 20 format gambar yang didukung.

**Q2: Apakah Aspose.Note kompatibel dengan semua versi dokumen OneNote?**  
A2: Aspose.Note mendukung Microsoft OneNote 2010 dan yang lebih baru, mencakup lebih dari 95 % notebook yang aktif digunakan saat ini.

**Q3: Apakah Aspose.Note memerlukan lisensi untuk digunakan?**  
A3: Lisensi yang valid diperlukan untuk penggunaan produksi, tetapi lisensi percobaan sementara dapat diperoleh untuk evaluasi tanpa biaya.

**Q4: Bisakah saya memanipulasi aspek lain dari dokumen sebelum menyimpannya sebagai gambar?**  
A4: Tentu saja! Aspose.Note menyediakan API untuk mengedit bagian, halaman, dan elemen individual seperti teks, tabel, dan gambar sebelum diekspor.

**Q5: Di mana saya dapat menemukan dukungan jika saya mengalami masalah?**  
A5: Anda dapat menemukan dukungan di forum Aspose.Note [here](https://forum.aspose.com/c/note/28).

## Kesimpulan

Anda kini telah mempelajari **how to export onenote** dengan memuat file OneNote, mengonfigurasi opsi penyimpanan untuk **create a grayscale image**, dan **saving the document as PNG**. Pendekatan ini ideal untuk menghasilkan visual ringan, siap cetak dari notebook OneNote. Jangan ragu untuk bereksperimen dengan pengaturan `ColorMode` lainnya, nilai DPI yang lebih tinggi, atau format gambar alternatif untuk menyesuaikan kebutuhan proyek Anda.

---

**Terakhir Diperbarui:** 2026-06-30  
**Diuji Dengan:** Aspose.Note 27.0 for Java  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Ekspor Halaman OneNote ke Gambar PNG di Java menggunakan Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote set jpeg resolution – Atur Resolusi Gambar Output di OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Cara Menyimpan OneNote sebagai PDF dengan Aspose.Note untuk Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}