---
title: Simpan ke Gambar Skala Abu-Abu di OneNote - Aspose.Note
linktitle: Simpan ke Gambar Skala Abu-Abu di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara menyimpan dokumen sebagai gambar skala abu-abu di OneNote menggunakan Aspose.Note untuk Java. Memanipulasi dokumen Microsoft OneNote dengan mudah secara terprogram.
type: docs
weight: 17
url: /id/java/onenote-document-saving/save-to-grayscale-image/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menyimpan dokumen sebagai gambar skala abu-abu di OneNote menggunakan Aspose.Note untuk Java. Gambar skala abu-abu adalah gambar monokromatik yang informasi warnanya hanya diwakili oleh nuansa abu-abu. Aspose.Note adalah Java API kuat yang memungkinkan manipulasi dokumen Microsoft OneNote secara terprogram.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1. Java Development Kit (JDK) diinstal pada sistem Anda.
2.  Aspose.Note untuk perpustakaan Java. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/java/).
3. Pemahaman dasar pemrograman Java.

## Paket Impor

Untuk memulai, impor paket yang diperlukan:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Langkah 1: Muat Dokumen

 Pertama, muat dokumen ke Aspose.Note. Mengganti`"Your Document Directory"` dengan jalur ke direktori dokumen Anda dan`"Aspose.one"` dengan nama dokumen OneNote Anda.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Langkah 2: Tetapkan Jalur dan Opsi Keluaran

Tentukan jalur keluaran untuk gambar skala abu-abu dan tentukan opsi penyimpanan. Kami akan mengatur mode warna ke skala abu-abu.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Langkah 3: Simpan Dokumen

Terakhir, simpan dokumen sebagai gambar skala abu-abu menggunakan opsi yang ditentukan.

```java
oneFile.save(dataDir, options);
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara menyimpan dokumen sebagai gambar skala abu-abu di OneNote menggunakan Aspose.Note untuk Java. Ini bisa sangat berguna untuk berbagai aplikasi yang memerlukan gambar skala abu-abu.

## FAQ

### Q1: Bisakah saya menyimpan gambar skala abu-abu dalam format berbeda?

 A1: Ya, Anda bisa. Cukup ubah`SaveFormat` parameter di`ImageSaveOptions` konstruktor ke format yang Anda inginkan.

### Q2: Apakah Aspose.Note kompatibel dengan semua versi dokumen OneNote?

A2: Aspose.Note mendukung Microsoft OneNote 2010 dan yang lebih baru.

### Q3: Apakah Aspose.Note memerlukan lisensi untuk menggunakannya?

A3: Ya, Anda memerlukan lisensi yang valid untuk menggunakan Aspose.Note di lingkungan produksi. Namun, Anda bisa mendapatkan lisensi sementara untuk tujuan pengujian.

### Q4: Dapatkah saya memanipulasi aspek lain dari dokumen sebelum menyimpannya sebagai gambar?

A4: Tentu saja! Aspose.Note menyediakan berbagai fitur untuk mengedit dokumen OneNote secara terprogram.

### Q5: Di mana saya bisa mendapatkan dukungan jika saya mengalami masalah?

A5: Anda dapat menemukan dukungan di forum Aspose.Note[Di Sini](https://forum.aspose.com/c/note/28).