---
title: Tentukan Opsi Simpan di OneNote - Aspose.Note
linktitle: Tentukan Opsi Simpan di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara menentukan opsi penyimpanan di OneNote menggunakan Aspose.Note untuk Java. Sesuaikan pengaturan indeks, jumlah, dan kompresi halaman dengan mudah.
type: docs
weight: 24
url: /id/java/onenote-document-saving/specify-save-options/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menentukan opsi penyimpanan di OneNote menggunakan Aspose.Note untuk Java. Aspose.Note adalah pustaka Java canggih yang memungkinkan pengembang membuat, memanipulasi, dan mengonversi dokumen OneNote secara terprogram. Dengan Aspose.Note, Anda dapat dengan mudah mengontrol berbagai opsi penyimpanan untuk menyesuaikan output sesuai kebutuhan Anda.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki prasyarat berikut:

1. Pengetahuan dasar bahasa pemrograman Java.
2. JDK (Java Development Kit) diinstal pada sistem Anda.
3.  Aspose.Note untuk perpustakaan Java diinstal. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/java/).

## Paket Impor

Untuk memulai, impor paket yang diperlukan dalam kode Java Anda:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Mari kita bagi contoh ini menjadi beberapa langkah:

## Langkah 1: Muat Dokumen OneNote

```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory";

// Muat dokumen ke Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

 Pada langkah ini, kami menentukan jalur ke dokumen OneNote dan memuatnya ke dalam`Document` obyek.

## Langkah 2: Inisialisasi Objek PdfSaveOptions

```java
// Inisialisasi objek PdfSaveOptions
PdfSaveOptions opts = new PdfSaveOptions();
```

 Di sini, kami menginisialisasi a`PdfSaveOptions` objek yang akan digunakan untuk menentukan opsi untuk menyimpan dokumen sebagai PDF.

## Langkah 3: Tetapkan Indeks dan Jumlah Halaman

```java
// Tetapkan indeks halaman
opts.setPageIndex(2);

// Tetapkan jumlah halaman
opts.setPageCount(3);
```

Baris-baris ini mengatur indeks dan jumlah halaman yang akan disimpan. Pada contoh ini, kita menyimpan halaman mulai dari indeks 2 dan total 3 halaman.

## Langkah 4: Tentukan Pengaturan Kompresi

```java
// Tentukan kompresi jika diperlukan
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Di sini, kami menentukan pengaturan kompresi gambar untuk PDF. Kami mengatur kompresi ke format JPEG dan menentukan kualitas JPEG sebagai 90%.

## Langkah 5: Simpan Dokumen dengan Opsi

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Terakhir, kami menyimpan dokumen dengan opsi yang ditentukan. PDF keluaran akan disimpan di lokasi yang ditentukan dengan opsi yang diberikan.

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara menentukan opsi penyimpanan di OneNote menggunakan Aspose.Note untuk Java. Dengan menyesuaikan opsi penyimpanan, Anda dapat mengontrol berbagai aspek dokumen keluaran, seperti indeks halaman, jumlah, dan pengaturan kompresi.

## FAQ

### Q1: Bisakah Aspose.Note menangani dokumen OneNote berukuran besar?

A1: Ya, Aspose.Note dirancang untuk menangani dokumen OneNote berukuran besar secara efisien.

### Q2: Apakah Aspose.Note kompatibel dengan versi Java terbaru?

A2: Ya, Aspose.Note kompatibel dengan versi Java terbaru.

### Q3: Bisakah saya mengonversi dokumen OneNote ke format lain menggunakan Aspose.Note?

A3: Ya, Aspose.Note mendukung konversi dokumen OneNote ke berbagai format seperti PDF, DOCX, dan HTML.

### Q4: Apakah Aspose.Note menyediakan dukungan untuk enkripsi dan dekripsi dokumen OneNote?

A4: Ya, Aspose.Note menyediakan API untuk enkripsi dan dekripsi dokumen OneNote.

### Q5: Apakah Aspose.Note cocok untuk penggunaan komersial?

A5: Ya, Aspose.Note dapat digunakan untuk tujuan komersial dengan membeli lisensi.