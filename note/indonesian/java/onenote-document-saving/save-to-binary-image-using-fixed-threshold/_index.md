---
title: Simpan ke Gambar Biner Menggunakan Ambang Batas Tetap di OneNote
linktitle: Simpan ke Gambar Biner Menggunakan Ambang Batas Tetap di OneNote
second_title: Aspose.Catatan Java API
description: Simpan dokumen Microsoft OneNote dengan mudah sebagai gambar biner menggunakan ambang batas tetap dengan Aspose.Note Java. Tingkatkan kemampuan manipulasi file OneNote Anda.
type: docs
weight: 14
url: /id/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---
## Perkenalan

Aspose.Note untuk Java adalah API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram. Dalam tutorial ini, kita akan mempelajari cara menyimpan dokumen sebagai gambar biner menggunakan ambang batas tetap. Ikuti langkah-langkah di bawah ini untuk mencapainya.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal berikut:

1. Java Development Kit (JDK) diinstal pada sistem Anda.
2.  Aspose.Note untuk perpustakaan Java diunduh. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/java/).
3. Pengetahuan dasar tentang pemrograman Java.

## Paket Impor

Pertama, impor paket yang diperlukan ke file Java Anda.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Langkah 1: Muat Dokumen

Muat dokumen OneNote menggunakan Aspose.Note API.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Langkah 2: Tetapkan Opsi Binarisasi

Tentukan opsi binarisasi untuk menyimpan dokumen sebagai gambar biner.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

## Langkah 3: Atur Opsi Penyimpanan Gambar

Atur opsi penyimpanan gambar termasuk mode warna dan opsi binarisasi.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## Langkah 4: Simpan Dokumen

Simpan dokumen sebagai gambar biner dengan opsi yang ditentukan.

```java
oneFile.save(dataDir, options);
```

## Kesimpulan

Dalam tutorial ini, kita mempelajari cara menyimpan dokumen sebagai gambar biner menggunakan ambang batas tetap di Aspose.Note untuk Java. Dengan mengikuti langkah-langkah ini, Anda bisa dengan mudah memanipulasi file OneNote secara terprogram.

## FAQ

### Q1: Dapatkah saya menyesuaikan nilai ambang batas untuk binarisasi?

 A1: Ya, Anda dapat menyesuaikan nilai ambang batas sesuai kebutuhan Anda dengan memodifikasi`setBinarizationThreshold()` parameter metode.

### Q2: Apakah Aspose.Note untuk Java kompatibel dengan semua versi Microsoft OneNote?

A2: Aspose.Note untuk Java mendukung berbagai versi Microsoft OneNote termasuk 2010, 2013, dan 2016.

### Q3: Apakah ada batasan ukuran dokumen yang dapat diproses?

A3: Aspose.Note untuk Java tidak memiliki batasan ukuran dokumen yang dapat diproses, sehingga Anda dapat menangani file besar secara efisien.

### Q4: Dapatkah saya mengonversi beberapa dokumen OneNote secara bersamaan?

A4: Ya, Anda dapat memproses beberapa dokumen OneNote secara batch dengan melakukan iterasi pada setiap file dan menerapkan operasi yang diperlukan.

### Q5: Apakah dukungan teknis tersedia untuk Aspose.Note untuk Java?

 A5: Ya, dukungan teknis tersedia melalui[Aspose.Catatan forum](https://forum.aspose.com/c/note/28), tempat Anda dapat mengajukan pertanyaan dan mencari bantuan dari para ahli.