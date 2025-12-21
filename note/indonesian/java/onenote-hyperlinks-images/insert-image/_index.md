---
date: 2025-12-21
description: Pelajari cara menambahkan gambar ke dokumen OneNote menggunakan Java
  dengan Aspose.Note for Java. Ikuti panduan langkah demi langkah kami untuk menyisipkan
  gambar dan secara opsional menyimpan OneNote sebagai PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Cara menambahkan gambar ke OneNote menggunakan Java
url: /id/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menyisipkan Gambar dalam Dokumen OneNote dengan Java

## Pendahuluan

Dalam tutorial ini, kami akan menjelajahi cara menyisipkan gambar ke dalam dokumen OneNote menggunakan Java dengan bantuan Aspose.Note untuk Java. Aspose.Note untuk Java adalah pustaka yang kuat yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara programatis, memungkinkan berbagai operasi seperti membuat, membaca, dan memanipulasi dokumen OneNote.

## Jawaban Cepat
- **What is the easiest way to add image to OneNote using Java?**  
  Gunakan kelas `Image` dari Aspose.Note untuk Java dan tambahkan ke halaman.
- **Do I need a license for production use?**  
  Ya, lisensi komersial diperlukan untuk penggunaan produksi.
- **Can I set custom dimensions for the image?**  
  Tentu – panggil `setWidth()` dan `setHeight()` pada objek `Image`.
- **Is it possible to save the OneNote file as PDF after adding the image?**  
  Ya, panggil `save(..., SaveFormat.Pdf)` untuk **save OneNote as PDF**.
- **Which Java version is supported?**  
  Aspose.Note untuk Java bekerja dengan JDK 8 dan versi lebih baru.

## Cara menambahkan gambar ke OneNote menggunakan Java?

Sebelum masuk ke kode, mari kita bahas singkat mengapa Anda mungkin ingin menyisipkan gambar secara programatis ke OneNote. Baik Anda membuat notulen rapat, menghasilkan laporan otomatis, atau membangun alur dokumentasi, menyisipkan gambar memberikan konteks visual pada catatan Anda yang tidak dapat diberikan oleh teks biasa. Dengan Aspose.Note untuk Java Anda dapat melakukan semua ini sepenuhnya melalui kode, tanpa membuka antarmuka OneNote.

## Prasyarat

Sebelum kita mulai, pastikan Anda telah menyiapkan prasyarat berikut:

### 1. Java Development Kit (JDK)
Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda. Anda dapat mengunduh dan menginstal JDK dari situs web Oracle.

### 2. Aspose.Note for Java Library
Unduh dan siapkan pustaka Aspose.Note untuk Java dengan mengikuti [documentation](https://reference.aspose.com/note/java/).

## Impor Paket

Mulailah dengan mengimpor paket yang diperlukan ke dalam proyek Java Anda. Paket-paket ini mencakup pustaka Aspose.Note serta dependensi lain yang diperlukan.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Mari kita uraikan proses menyisipkan gambar ke dalam dokumen OneNote menjadi beberapa langkah:

## Langkah 1: Muat Dokumen OneNote

Pertama, muat dokumen OneNote tempat Anda ingin menyisipkan gambar.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Langkah 2: Dapatkan Halaman

Ambil halaman dalam dokumen tempat Anda ingin menyisipkan gambar.

```java
Page page = oneFile.getFirstChild();
```

## Langkah 3: Muat Gambar

Muat gambar yang ingin Anda sisipkan ke dalam dokumen OneNote.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Langkah 4: Sesuaikan Atribut Gambar (Opsional)

Opsional, Anda dapat menyesuaikan ukuran, lokasi, dan perataan gambar sesuai kebutuhan Anda. Di sinilah Anda **set image dimensions Java** style.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Langkah 5: Tambahkan Gambar ke Halaman

Tambahkan gambar ke halaman dalam dokumen OneNote.

```java
page.appendChildLast(image);
```

## Langkah 6: Simpan Dokumen

Simpan dokumen yang telah dimodifikasi, termasuk gambar yang disisipkan. Anda juga dapat **save OneNote as PDF** pada tahap ini.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Kesimpulan

Dalam tutorial ini, kami telah mempelajari cara menyisipkan gambar ke dalam dokumen OneNote menggunakan Java dengan bantuan pustaka Aspose.Note untuk Java. Dengan mengikuti panduan langkah demi langkah, Anda dapat dengan mudah mengintegrasikan gambar ke dalam dokumen OneNote secara programatis.

## FAQ

### Q1: Bisakah saya menyisipkan beberapa gambar ke dalam satu dokumen OneNote menggunakan metode ini?

A1: Ya, Anda dapat menyisipkan beberapa gambar ke dalam satu dokumen OneNote dengan mengulangi proses yang dijelaskan dalam tutorial ini untuk setiap gambar.

### Q2: Apakah Aspose.Note untuk Java kompatibel dengan semua versi OneNote?

A2: Aspose.Note untuk Java mendukung kerja dengan file OneNote yang dibuat di Microsoft OneNote 2010 dan versi lebih baru.

### Q3: Bisakah saya menyisipkan gambar dengan format berbeda, seperti PNG atau GIF, ke dalam dokumen OneNote?

A3: Ya, Aspose.Note untuk Java mendukung penyisipan gambar dalam berbagai format, termasuk PNG, JPEG, GIF, dan lainnya.

### Q4: Apakah ada versi percobaan Aspose.Note untuk Java yang tersedia untuk tujuan pengujian?

A4: Ya, Anda dapat mengunduh versi percobaan gratis Aspose.Note untuk Java dari situs web untuk keperluan evaluasi.

### Q5: Bagaimana cara mendapatkan dukungan teknis untuk Aspose.Note untuk Java?

A5: Anda dapat mendapatkan dukungan teknis untuk Aspose.Note untuk Java dengan mengunjungi [forum](https://forum.aspose.com/c/note/28) yang didedikasikan untuk produk Aspose.Note.

---

**Terakhir Diperbarui:** 2025-12-21  
**Diuji Dengan:** Aspose.Note for Java 24.10  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}