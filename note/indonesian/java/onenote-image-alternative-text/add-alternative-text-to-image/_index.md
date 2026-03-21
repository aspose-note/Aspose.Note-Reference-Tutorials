---
date: 2026-03-21
description: Pelajari cara membuat dokumen OneNote dan mengatur teks alt gambar menggunakan
  Java dengan Aspose.Note. Panduan ini juga menunjukkan cara menyimpan file OneNote
  dan meningkatkan aksesibilitas.
linktitle: Create OneNote Document & Add Alt Text to Images in Java
second_title: Aspose.Note Java API
title: Buat Dokumen OneNote & Tambahkan Teks Alt pada Gambar di Java
url: /id/java/onenote-image-alternative-text/add-alternative-text-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat Dokumen OneNote & Tambahkan Teks Alternatif ke Gambar dalam Java

## Pendahuluan

Dalam tutorial ini Anda akan belajar **cara membuat dokumen OneNote** secara programatik dan **menetapkan teks alternatif gambar** menggunakan Java dan API Aspose.Note. Menambahkan teks alternatif membuat halaman OneNote Anda dapat diakses oleh pengguna pembaca layar, meningkatkan kemampuan pencarian, dan membantu Anda **menyimpan file OneNote** dengan metadata yang lebih kaya. Pada akhir panduan Anda akan dapat **menambahkan gambar onenote** ke halaman, menetapkan baik judul maupun deskripsi untuk gambar, dan menyimpan file ke disk.

## Jawaban Cepat

- **Perpustakaan apa yang diperlukan?** Aspose.Note for Java  
- **Kata kunci utama apa yang ditargetkan tutorial ini?** create onenote document  
- **Apakah saya memerlukan lisensi untuk produksi?** Yes, a commercial license is required (a free trial is available).  
- **Bisakah saya menambahkan teks alternatif ke beberapa gambar?** Absolutely – just repeat the steps for each image.  
- **Versi Java apa yang didukung?** Java 8 or higher.

## Apa itu “create onenote document” dalam konteks OneNote?

Membuat dokumen OneNote berarti secara programatik membangun file `.one` yang dapat berisi halaman, teks, gambar, dan konten kaya lainnya. Dengan Aspose.Note Anda dapat menghasilkan file ini dari awal, menambahkan elemen, dan kemudian **menyimpan file OneNote** ke lokasi mana pun.

## Mengapa menambahkan teks alternatif ke gambar di OneNote?

- **Aksesibilitas:** Memenuhi pedoman WCAG dan membantu pengguna dengan gangguan penglihatan.  
- **Kemampuan Pencarian:** Mesin pencari dapat mengindeks deskripsi, membuat konten Anda lebih mudah ditemukan.  
- **Profesionalisme:** Menunjukkan komitmen terhadap desain inklusif dan kualitas dokumentasi.

## Prasyarat

Sebelum memulai tutorial, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK) – versi 8 atau lebih baru.  
2. Aspose.Note for Java Library – download it from [here](https://releases.aspose.com/note/java/).  
3. Sebuah IDE seperti IntelliJ IDEA atau Eclipse.  
4. Pengetahuan dasar tentang pemrograman Java.

## Impor Paket

Pertama, impor paket yang diperlukan ke dalam proyek Java Anda untuk memanfaatkan fungsionalitas Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

Sekarang, mari kita jalani **panduan langkah‑demi‑langkah** untuk **membuat dokumen OneNote**, menambahkan gambar, dan **menetapkan teks alternatif gambar**.

## Cara Membuat Dokumen OneNote dan Menetapkan Teks Alternatif Gambar dalam Java

### Langkah 1: Siapkan Direktori Dokumen

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur absolut tempat gambar sumber Anda berada dan tempat Anda ingin file output `.one` disimpan.

### Langkah 2: Buat Objek Dokumen

```java
Document document = new Document();
```

Baris ini **membuat dokumen OneNote baru** yang nantinya Anda akan **menyimpan file OneNote** dengan konten yang ditambahkan.

### Langkah 3: Buat Objek Halaman

```java
Page page = new Page();
```

Sebuah halaman berfungsi sebagai kanvas untuk gambar dan elemen lain yang mungkin ingin Anda tambahkan.

### Langkah 4: Tambahkan Gambar ke Halaman

```java
Image image = new Image(null, dataDir + "image.jpg");
```

Konstruktor `Image` memuat file gambar dari jalur yang ditentukan. Ini adalah titik di mana Anda akan **menambahkan gambar onenote**.

### Langkah 5: Tetapkan Judul Teks Alternatif (Set Image Alt Text)

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

Di sini kami **menetapkan teks alternatif gambar** yang berfungsi sebagai judul singkat untuk gambar.

### Langkah 6: Tetapkan Deskripsi Teks Alternatif (Set Alt Text Description)

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

Deskripsi memberikan penjelasan yang lebih detail—sempurna untuk pembaca layar.

### Langkah 7: Tambahkan Gambar ke Halaman

```java
page.appendChildLast(image);
```

Sekarang gambar, yang diperkaya dengan teks alternatifnya, **ditambahkan ke halaman OneNote**.

### Langkah 8: Tambahkan Halaman ke Dokumen

```java
document.appendChildLast(page);
```

Lampirkan halaman ke dokumen OneNote yang Anda buat sebelumnya.

### Langkah 9: Simpan Dokumen (Save OneNote File)

```java
document.save(dataDir + "AlternativeText_out.one");
```

Pemanggilan `save` **menulis file OneNote** ke disk, mempertahankan semua metadata teks‑alternatif.

## Masalah Umum dan Solusinya

- **FileNotFoundException:** Pastikan `dataDir` mengarah ke folder yang benar dan `image.jpg` ada.  
- **NullPointerException pada gambar:** Pastikan jalur gambar valid dan file tidak rusak.  
- **Kesalahan lisensi:** Gunakan file lisensi Aspose.Note yang valid atau jalankan dalam mode percobaan untuk evaluasi.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menambahkan teks alternatif ke beberapa gambar dalam satu dokumen?**  
A: Ya, cukup ulangi langkah 4‑6 untuk setiap gambar yang ingin Anda beri anotasi.

**Q: Format gambar apa yang didukung untuk menambahkan teks alternatif?**  
A: Aspose.Note mendukung JPEG, PNG, GIF, BMP, dan beberapa format umum lainnya.

**Q: Apakah memungkinkan untuk memodifikasi atau menghapus teks alternatif setelah ditetapkan?**  
A: Tentu saja. Panggil `setAlternativeTextTitle("")` atau `setAlternativeTextDescription("")` untuk mengosongkan nilai, atau berikan string baru untuk memperbaruinya.

**Q: Apakah Aspose.Note menyediakan API untuk bahasa lain selain Java?**  
A: Ya, perpustakaan ini juga tersedia untuk .NET, C++, dan Python.

**Q: Di mana saya dapat mengunduh versi percobaan Aspose.Note?**  
A: Anda dapat memperoleh percobaan gratis dari [here](https://releases.aspose.com/).

**Q: Bagaimana cara secara programatik **menyimpan file OneNote** setelah menambahkan beberapa halaman?**  
A: Panggil `document.save(<outputPath>)` sekali setelah Anda menambahkan semua halaman dan gambar; API akan menangani pembuatan file lengkap.

**Q: Bisakah saya menggunakan kode yang sama untuk **menambahkan gambar onenote** dalam dokumen yang sudah ada?**  
A: Ya. Muat dokumen yang ada dengan `new Document(<filePath>)`, kemudian ikuti langkah 3‑7 untuk menambahkan gambar baru dan teks alternatif.

## Kesimpulan

Dengan mengikuti panduan ini Anda kini tahu **cara membuat dokumen OneNote**, **menambahkan gambar onenote**, dan **menetapkan teks alternatif gambar** menggunakan Java. Menerapkan langkah‑langkah ini tidak hanya membuat file OneNote Anda lebih dapat diakses tetapi juga meningkatkan kemampuan penemuan dan kualitas keseluruhan. Jangan ragu untuk bereksperimen dengan judul dan deskripsi yang berbeda untuk menyampaikan makna setiap gambar dengan terbaik.

---

**Terakhir Diperbarui:** 2026-03-21  
**Diuji Dengan:** Aspose.Note for Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}