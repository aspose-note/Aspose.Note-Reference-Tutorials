---
title: Konversi Buku Catatan ke PDF dengan Opsi di Aspose Note .NET
linktitle: Konversi Buku Catatan ke PDF dengan Opsi di Aspose Note .NET
second_title: Aspose.Catatan .NET API
description: Pelajari cara mengonversi buku catatan Microsoft OneNote ke format PDF menggunakan perpustakaan Aspose.Note untuk .NET dengan opsi yang dapat disesuaikan.
weight: 16
url: /id/net/notebook-operations/convert-to-pdf-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi Buku Catatan ke PDF dengan Opsi di Aspose Note .NET

## Perkenalan

Dalam tutorial ini, kita akan memandu proses mengonversi buku catatan ke format PDF menggunakan perpustakaan Aspose.Note untuk .NET. Aspose.Note untuk .NET menyediakan serangkaian fitur canggih untuk bekerja dengan file Microsoft OneNote secara terprogram.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

### 1. Aspose.Note untuk Perpustakaan .NET
 Pastikan Anda telah mengunduh dan menginstal perpustakaan Aspose.Note untuk .NET. Anda dapat mengunduhnya dari[situs web](https://releases.aspose.com/note/net/).

### 2. Lingkungan Pembangunan
Anda harus menyiapkan lingkungan pengembangan, seperti Visual Studio, dengan kerangka .NET yang diperlukan terpasang.

## Impor Namespace

Sebelum kita mulai menggunakan Aspose.Note untuk .NET di proyek kita, mari impor namespace yang diperlukan:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Sekarang, mari kita uraikan proses mengonversi buku catatan ke PDF dengan opsi menjadi beberapa langkah:

## Langkah 1: Muat Notebook

Pertama, kita perlu memuat buku catatan OneNote yang ingin kita ubah menjadi file PDF.

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";

// Memuat Buku Catatan OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Langkah 2: Tentukan Opsi Penyimpanan PDF

Selanjutnya, kita akan menentukan opsi untuk menyimpan buku catatan sebagai file PDF. Kami dapat menyesuaikan berbagai pengaturan seperti algoritma pemisahan halaman, margin, dan ukuran halaman.

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## Langkah 3: Simpan Buku Catatan sebagai PDF

Sekarang, kita akan menyimpan buku catatan sebagai file PDF menggunakan opsi yang ditentukan.

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// Simpan Buku Catatan
notebook.Save(dataDir, notebookSaveOptions);
```

## Langkah 4: Verifikasi Konversi

Terakhir, mari verifikasi bahwa konversi berhasil dan cetak lokasi penyimpanan file PDF.

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara mengonversi buku catatan OneNote ke format PDF menggunakan perpustakaan Aspose.Note untuk .NET. Dengan mengikuti langkah-langkah yang diuraikan di atas, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam aplikasi .NET Anda.

## FAQ

### Q1: Apakah Aspose.Note untuk .NET kompatibel dengan semua versi Microsoft OneNote?

A1: Ya, Aspose.Note untuk .NET mendukung berbagai versi Microsoft OneNote, termasuk format .one dan .onetoc2.

### Q2: Dapatkah saya menyesuaikan tampilan keluaran PDF?

A2: Ya, Anda dapat menentukan berbagai opsi seperti ukuran halaman, margin, dan algoritma pemisahan halaman untuk menyesuaikan tampilan keluaran PDF.

### Q3: Apakah Aspose.Note untuk .NET menyediakan dukungan untuk format file lain?

A3: Ya, Aspose.Note untuk .NET mendukung konversi ke berbagai format lain seperti gambar, HTML, dan dokumen Microsoft Word.

### Q4: Apakah ada uji coba gratis yang tersedia untuk Aspose.Note untuk .NET?

A4: Ya, Anda dapat mengunduh uji coba gratis Aspose.Note untuk .NET dari situs web untuk mengevaluasi fitur-fiturnya sebelum melakukan pembelian.

### Q5: Bagaimana saya bisa mendapatkan dukungan teknis untuk Aspose.Note untuk .NET?

 A5: Anda bisa mendapatkan dukungan teknis untuk Aspose.Note untuk .NET dengan mengunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28) atau menghubungi tim dukungan Aspose secara langsung.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
