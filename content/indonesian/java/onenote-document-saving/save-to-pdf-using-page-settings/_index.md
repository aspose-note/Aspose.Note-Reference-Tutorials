---
title: Simpan ke PDF Menggunakan Pengaturan Halaman di OneNote - Aspose.Note
linktitle: Simpan ke PDF Menggunakan Pengaturan Halaman di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara menyimpan dokumen OneNote ke PDF di Java menggunakan perpustakaan Aspose.Note. Panduan langkah demi langkah dengan contoh kode untuk berbagai pengaturan halaman.
type: docs
weight: 19
url: /id/java/onenote-document-saving/save-to-pdf-using-page-settings/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menyimpan dokumen OneNote ke format PDF menggunakan pengaturan halaman berbeda dengan Aspose.Note untuk Java. Kami akan membahas dua metode: menyimpan dengan pengaturan halaman Letter dan menyimpan dengan pengaturan halaman A4 tanpa batas ketinggian.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK) diinstal pada sistem Anda.
2. Aspose.Note untuk perpustakaan Java diunduh dan disertakan dalam proyek Java Anda.
3. Pemahaman dasar bahasa pemrograman Java.

## Paket Impor

Pastikan Anda telah mengimpor paket yang diperlukan untuk menggunakan Aspose.Note untuk Java di proyek Anda. Berikut pernyataan impornya:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Simpan ke PDF Menggunakan Pengaturan Halaman Surat

### Langkah 1: Muat Dokumen

Pertama, muat dokumen OneNote ke Aspose.Catatan:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Langkah 2: Tentukan Jalur Tujuan

Tentukan jalur tujuan untuk file PDF:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Langkah 3: Simpan Dokumen

Simpan dokumen dengan pengaturan halaman Surat:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Simpan ke PDF Menggunakan Pengaturan Halaman A4 Tanpa Batas Tinggi

### Langkah 1: Muat Dokumen

Demikian pula, muat dokumen OneNote ke Aspose.Catatan:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Langkah 2: Tentukan Jalur Tujuan

Tentukan jalur tujuan untuk file PDF:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Langkah 3: Simpan Dokumen

Simpan dokumen dengan pengaturan halaman A4 tanpa batas ketinggian:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Setelah mengikuti langkah-langkah ini, Anda berhasil menyimpan dokumen OneNote ke PDF menggunakan pengaturan halaman berbeda.

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi cara menyimpan dokumen OneNote ke format PDF menggunakan perpustakaan Aspose.Note untuk Java. Dengan mengikuti panduan langkah demi langkah, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam aplikasi Java Anda.

## FAQ

### Q1: Dapatkah saya menyesuaikan pengaturan halaman lebih lanjut?

A1: Ya, Anda dapat menyesuaikan pengaturan halaman sesuai kebutuhan Anda menggunakan Aspose.Note untuk Java.

### Q2: Apakah Aspose.Note mendukung format keluaran lain selain PDF?

A2: Ya, Aspose.Note mendukung berbagai format output termasuk gambar dan HTML.

### Q3: Apakah Aspose.Note kompatibel dengan versi file OneNote yang berbeda?

A3: Ya, Aspose.Note mendukung file OneNote dari versi berbeda termasuk .one dan .onetoc2.

### Q4: Bisakah saya mengonversi beberapa file OneNote ke PDF sekaligus?

A4: Ya, Anda dapat memproses beberapa file OneNote secara batch menggunakan Aspose.Note untuk Java.

### Q5: Apakah ada versi uji coba yang tersedia untuk tujuan pengujian?

A5: Ya, Anda bisa mendapatkan uji coba gratis Aspose.Note untuk Java dari situs web.