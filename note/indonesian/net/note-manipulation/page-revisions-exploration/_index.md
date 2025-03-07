---
title: Jelajahi Revisi Halaman di Dokumen Aspose.Note
linktitle: Jelajahi Revisi Halaman di Dokumen Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menjelajahi revisi halaman di dokumen Aspose.Note menggunakan kerangka .NET dengan panduan langkah demi langkah.
weight: 14
url: /id/net/note-manipulation/page-revisions-exploration/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jelajahi Revisi Halaman di Dokumen Aspose.Note

## Perkenalan

Dalam tutorial ini, kita akan mempelajari revisi halaman di dokumen Aspose.Note menggunakan kerangka .NET. Aspose.Note adalah perpustakaan canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram, menawarkan berbagai fitur untuk memanipulasi dan mengekstrak data dari file ini.

## Prasyarat

Sebelum kita mulai, pastikan Anda telah menyiapkan prasyarat berikut:

### 1. Unduh dan Instal Aspose.Note untuk .NET

 Mengunjungi[Unduh Halaman](https://releases.aspose.com/note/net/) dan unduh perpustakaan Aspose.Note untuk .NET. Ikuti petunjuk instalasi yang disediakan untuk menyiapkan perpustakaan di lingkungan pengembangan Anda.

### 2. Muat Namespace yang Diperlukan

Pastikan untuk mengimpor namespace yang diperlukan dalam proyek .NET Anda untuk mengakses fungsionalitas Aspose.Note dengan lancar.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

Sekarang, mari kita uraikan proses menjelajahi revisi halaman menjadi petunjuk langkah demi langkah:

## Langkah 1: Muat Dokumen

Pertama, kita perlu memuat dokumen Aspose.Note, memastikan untuk mengaktifkan pemuatan riwayat dokumen.

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## Langkah 2: Ambil Revisi Halaman

Setelah dokumen dimuat, kami dapat mengambil revisi untuk halaman tertentu. Dalam contoh ini, kita akan mendapatkan revisi untuk halaman pertama.

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## Langkah 3: Ulangi Melalui Revisi

Dalam loop, ulangi setiap revisi halaman dan akses propertinya seperti waktu modifikasi terakhir, waktu pembuatan, judul, level, dan penulis.

## Kesimpulan

Menjelajahi revisi halaman di dokumen Aspose.Note menggunakan .NET adalah proses yang mudah. Dengan mengikuti langkah-langkah yang diuraikan dalam tutorial ini, Anda dapat secara efektif mengambil dan menganalisis riwayat revisi file OneNote Anda secara terprogram.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.Note untuk .NET untuk membuat dokumen OneNote baru?

A1: Ya, Aspose.Note untuk .NET memungkinkan Anda membuat, mengedit, dan memanipulasi dokumen OneNote secara terprogram.

### Q2: Apakah Aspose.Note mendukung riwayat pemuatan untuk semua jenis file OneNote?

A2: Aspose.Note mendukung riwayat pemuatan untuk format file .one dan .onepkg.

### Q3: Apakah ada uji coba gratis yang tersedia untuk Aspose.Note untuk .NET?

A3: Ya, Anda dapat mengunduh uji coba gratis Aspose.Note untuk .NET dari[Di Sini](https://releases.aspose.com/).

### Q4: Bagaimana cara mendapatkan lisensi sementara Aspose.Note untuk .NET?

 A4: Anda dapat meminta lisensi sementara dari[Link ini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat menemukan dukungan untuk Aspose.Note untuk .NET?

 A5: Anda dapat menemukan dukungan dan sumber daya di[Aspose.Catatan forum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
