---
title: Sisipkan Gambar di Dokumen OneNote dengan Java
linktitle: Sisipkan Gambar di Dokumen OneNote dengan Java
second_title: Aspose.Catatan Java API
description: Pelajari cara menyisipkan gambar ke dalam dokumen OneNote menggunakan Java dengan pustaka Aspose.Note untuk Java. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
weight: 16
url: /id/java/onenote-hyperlinks-images/insert-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sisipkan Gambar di Dokumen OneNote dengan Java

## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menyisipkan gambar ke dalam dokumen OneNote menggunakan Java dengan bantuan Aspose.Note for Java. Aspose.Note untuk Java adalah pustaka canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram, memungkinkan berbagai operasi seperti membuat, membaca, dan memanipulasi dokumen OneNote.

## Prasyarat

Sebelum kita mulai, pastikan Anda telah menyiapkan prasyarat berikut:

### 1. Kit Pengembangan Java (JDK)
Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda. Anda dapat mengunduh dan menginstal JDK dari situs web Oracle.

### 2. Aspose.Note untuk Perpustakaan Java
 Unduh dan atur perpustakaan Aspose.Note untuk Java dengan mengikuti[dokumentasi](https://reference.aspose.com/note/java/).

## Paket Impor

Mulailah dengan mengimpor paket yang diperlukan ke proyek Java Anda. Paket-paket ini mencakup perpustakaan Aspose.Note dan dependensi lain yang diperlukan.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Mari kita uraikan proses memasukkan gambar ke dalam dokumen OneNote menjadi beberapa langkah:

## Langkah 1: Muat Dokumen OneNote

Pertama, muat dokumen OneNote yang ingin Anda sisipkan gambarnya.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Langkah 2: Dapatkan Halamannya

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

Secara opsional, Anda dapat menyesuaikan ukuran, lokasi, dan perataan gambar sesuai kebutuhan Anda.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Langkah 5: Tambahkan Gambar ke Halaman

Tambahkan gambar ke halaman di dokumen OneNote.

```java
page.appendChildLast(image);
```

## Langkah 6: Simpan Dokumen

Simpan dokumen yang dimodifikasi, termasuk gambar yang disisipkan.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara menyisipkan gambar ke dalam dokumen OneNote menggunakan Java dengan bantuan perpustakaan Aspose.Note untuk Java. Dengan mengikuti panduan langkah demi langkah, Anda dapat dengan mudah memasukkan gambar ke dalam dokumen OneNote Anda secara terprogram.

## FAQ

### Q1: Bisakah saya menyisipkan banyak gambar ke dalam satu dokumen OneNote menggunakan metode ini?

A1: Ya, Anda bisa menyisipkan beberapa gambar ke dalam satu dokumen OneNote dengan mengulangi proses yang dijelaskan dalam tutorial ini untuk setiap gambar.

### Q2: Apakah Aspose.Note untuk Java kompatibel dengan semua versi OneNote?

A2: Aspose.Note untuk Java mendukung bekerja dengan file OneNote yang dibuat di Microsoft OneNote 2010 dan versi yang lebih baru.

### Q3: Bisakah saya menyisipkan gambar dengan format berbeda, seperti PNG atau GIF, ke dalam dokumen OneNote?

A3: Ya, Aspose.Note untuk Java mendukung penyisipan gambar dalam berbagai format, termasuk PNG, JPEG, GIF, dan lainnya.

### Q4: Apakah ada versi uji coba Aspose.Note untuk Java yang tersedia untuk tujuan pengujian?

A4: Ya, Anda dapat mengunduh Aspose.Note for Java versi uji coba gratis dari situs web untuk tujuan evaluasi.

### Q5: Bagaimana saya bisa mendapatkan dukungan teknis untuk Aspose.Note untuk Java?

 A5: Anda bisa mendapatkan dukungan teknis untuk Aspose.Note untuk Java dengan mengunjungi[forum](https://forum.aspose.com/c/note/28) didedikasikan untuk produk Aspose.Note.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
