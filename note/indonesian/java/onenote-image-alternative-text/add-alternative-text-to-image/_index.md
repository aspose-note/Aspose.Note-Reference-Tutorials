---
date: 2025-12-23
description: Pelajari cara menambahkan teks alt pada gambar dalam dokumen OneNote
  menggunakan Java dengan Aspose.Note. Panduan ini menunjukkan cara menambahkan teks
  alternatif pada gambar untuk aksesibilitas yang lebih baik.
linktitle: How to Add Alt Text to Image in OneNote using Java
second_title: Aspose.Note Java API
title: Cara Menambahkan Teks Alt ke Gambar di OneNote dengan Java
url: /id/java/onenote-image-alternative-text/add-alternative-text-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menambahkan Teks Alt ke Gambar di OneNote menggunakan Java

## Pendahuluan

Dalam tutorial ini, Anda akan menemukan **cara menambahkan alt** teks ke gambar dalam dokumen OneNote menggunakan Java dan Aspose.Note API. Menambahkan teks alternatif (alt text) meningkatkan aksesibilitas bagi pengguna pembaca layar dan meningkatkan inklusivitas keseluruhan konten Anda. Pada akhir panduan ini, Anda akan dapat mengatur teks alt gambar dalam Java, membuat file OneNote Anda lebih sesuai dengan standar aksesibilitas.

## Jawaban Cepat
- **Library apa yang diperlukan?** Aspose.Note for Java  
- **Kata kunci utama apa yang ditargetkan tutorial ini?** how to add alt  
- **Apakah saya memerlukan lisensi untuk produksi?** Ya, lisensi komersial diperlukan (versi percobaan gratis tersedia).  
- **Bisakah saya menambahkan teks alt ke beberapa gambar?** Tentu – cukup ulangi langkah untuk setiap gambar.  
- **Versi Java apa yang didukung?** Java 8 atau lebih tinggi.

## Apa itu “how to add alt” dalam konteks OneNote?

Menambahkan teks alt berarti memberikan deskripsi tekstual untuk sebuah gambar yang dapat dibaca oleh teknologi bantu. Deskripsi ini membantu pengguna yang tidak dapat melihat gambar memahami tujuannya.

## Mengapa menambahkan teks alt ke gambar di OneNote?

- **Aksesibilitas:** Memenuhi pedoman WCAG dan meningkatkan pengalaman bagi pengguna dengan gangguan penglihatan.  
- **Ketercarian:** Mesin pencari dapat mengindeks deskripsi, membuat konten Anda lebih mudah ditemukan.  
- **Profesionalisme:** Menunjukkan komitmen terhadap desain inklusif.

## Prasyarat

Sebelum memulai tutorial, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK) – versi 8 atau lebih baru.  
2. Aspose.Note for Java Library – unduh dari [here](https://releases.aspose.com/note/java/).  
3. IDE seperti IntelliJ IDEA atau Eclipse.  
4. Pengetahuan dasar pemrograman Java.

## Impor Paket

Pertama, impor paket yang diperlukan ke dalam proyek Java Anda untuk memanfaatkan fungsionalitas Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

Sekarang, mari kita uraikan proses menambahkan **gambar teks alternatif** ke dokumen OneNote menggunakan Java dan Aspose.Note menjadi instruksi langkah demi langkah.

## Cara Menambahkan Teks Alt ke Gambar di OneNote menggunakan Java

### Langkah 1: Siapkan Direktori Dokumen

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan path ke folder yang berisi gambar sumber Anda dan tempat file output akan disimpan.

### Langkah 2: Buat Objek Dokumen

```java
Document document = new Document();
```

Ini membuat dokumen OneNote baru yang kosong.

### Langkah 3: Buat Objek Halaman

```java
Page page = new Page();
```

Sebuah halaman akan menampung gambar yang akan kita tambahkan.

### Langkah 4: Tambahkan Gambar ke Halaman

```java
Image image = new Image(null, dataDir + "image.jpg");
```

Konstruktor `Image` memuat file gambar dari path yang ditentukan.

### Langkah 5: Atur Judul Teks Alternatif

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

Di sini kita **menambahkan teks alt** yang berfungsi sebagai judul singkat untuk gambar.

### Langkah 6: Atur Deskripsi Teks Alternatif

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

Deskripsi ini memberikan penjelasan yang lebih detail—sangat cocok untuk pembaca layar.

### Langkah 7: Tambahkan Gambar ke Halaman

```java
page.appendChildLast(image);
```

Gambar (sekarang diperkaya dengan teks alt) ditambahkan ke halaman.

### Langkah 8: Tambahkan Halaman ke Dokumen

```java
document.appendChildLast(page);
```

Lampirkan halaman ke dokumen OneNote.

### Langkah 9: Simpan Dokumen

```java
document.save(dataDir + "AlternativeText_out.one");
```

Dokumen disimpan dengan teks alternatif yang tertanam dalam gambar.

## Masalah Umum dan Solusinya

- **FileNotFoundException:** Pastikan `dataDir` mengarah ke folder yang benar dan `image.jpg` ada.  
- **NullPointerException pada gambar:** Pastikan path gambar valid dan file tidak rusak.  
- **Kesalahan lisensi:** Gunakan file lisensi Aspose.Note yang valid atau jalankan dalam mode percobaan untuk evaluasi.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menambahkan teks alt ke beberapa gambar dalam satu dokumen?**  
A: Ya, cukup ulangi langkah 4‑6 untuk setiap gambar yang ingin Anda beri anotasi.

**Q: Format gambar apa yang didukung untuk menambahkan teks alt?**  
A: Aspose.Note mendukung JPEG, PNG, GIF, BMP, dan beberapa format umum lainnya.

**Q: Apakah memungkinkan untuk memodifikasi atau menghapus teks alt setelah diatur?**  
A: Tentu. Panggil `setAlternativeTextTitle("")` atau `setAlternativeTextDescription("")` untuk mengosongkan nilai, atau berikan string baru untuk memperbaruinya.

**Q: Apakah Aspose.Note menyediakan API untuk bahasa lain selain Java?**  
A: Ya, perpustakaan ini juga tersedia untuk .NET, C++, dan Python.

**Q: Di mana saya dapat mengunduh versi percobaan Aspose.Note?**  
A: Anda dapat memperoleh percobaan gratis dari [here](https://releases.aspose.com/).

## Kesimpulan

Dengan mengikuti panduan langkah demi langkah ini, Anda kini tahu **cara menambahkan alt** teks ke gambar di OneNote menggunakan Java. Menerapkan `add alternative text image` tidak hanya membuat dokumen Anda lebih dapat diakses tetapi juga meningkatkan ketercariannya dan kualitas secara keseluruhan. Jangan ragu untuk bereksperimen dengan judul dan deskripsi yang berbeda untuk menyampaikan makna setiap gambar dengan terbaik.

---

**Terakhir Diperbarui:** 2025-12-23  
**Diuji Dengan:** Aspose.Note for Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}