---
title: Konversi Buku Catatan menjadi Gambar dengan Opsi di Aspose Note .NET
linktitle: Konversi Buku Catatan menjadi Gambar dengan Opsi di Aspose Note .NET
second_title: Aspose.Catatan .NET API
description: Pelajari cara mengonversi buku catatan menjadi gambar dengan opsi yang dapat disesuaikan menggunakan Aspose.Note untuk .NET.
weight: 13
url: /id/net/notebook-operations/convert-to-image-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi Buku Catatan menjadi Gambar dengan Opsi di Aspose Note .NET

## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara mengonversi buku catatan menjadi gambar dengan berbagai opsi menggunakan pustaka Aspose.Note untuk .NET. Aspose.Note adalah .NET API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram. Dengan mengikuti langkah-langkah yang diuraikan dalam panduan ini, Anda akan mempelajari cara mengonversi buku catatan menjadi gambar dengan mudah sambil menyesuaikan keluarannya sesuai kebutuhan Anda.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Pengetahuan Dasar C#: Keakraban dengan bahasa pemrograman C# sangat penting untuk memahami dan mengimplementasikan cuplikan kode yang disediakan.

2.  Aspose.Note untuk .NET: Unduh dan instal Aspose.Note untuk .NET dari[situs web](https://releases.aspose.com/note/net/). Anda dapat memperoleh uji coba gratis atau membeli lisensi sesuai kebutuhan Anda.

3. Lingkungan Pengembangan: Siapkan lingkungan pengembangan pilihan Anda dengan Visual Studio atau IDE lain yang mendukung pengembangan .NET.

## Impor Namespace

Untuk memulai, mari impor namespace yang diperlukan agar berfungsi dengan Aspose.Note untuk .NET.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Sekarang, mari kita uraikan proses mengubah buku catatan menjadi gambar dengan opsi menjadi beberapa langkah.

## Langkah 1: Muat Notebook

Pertama, muat file buku catatan yang ingin Anda konversi menjadi gambar.

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";

// Memuat Buku Catatan OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Langkah 2: Atur Opsi Penyimpanan Gambar

Tentukan opsi untuk menyimpan buku catatan sebagai gambar. Di sini, kami akan mengatur format gambar ke PNG dan menyesuaikan resolusi.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
```

## Langkah 3: Simpan Buku Catatan sebagai Gambar

Simpan buku catatan sebagai gambar menggunakan opsi yang ditentukan.

```csharp
dataDir = dataDir + "ConvertToImageWithOptions_out.png";

// Simpan Buku Catatan
notebook.Save(dataDir, notebookSaveOptions);
```

## Kesimpulan

Sebagai kesimpulan, kami telah menjelajahi cara mengonversi buku catatan menjadi gambar dengan berbagai opsi menggunakan Aspose.Note untuk .NET. Dengan mengikuti langkah-langkah yang diuraikan dalam tutorial ini, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam aplikasi .NET Anda, sehingga memungkinkan manipulasi file Microsoft OneNote secara efisien.

## FAQ

### Q1: Bisakah saya mengonversi beberapa buku catatan secara bersamaan menggunakan Aspose.Note untuk .NET?

A1: Ya, Anda dapat mengulangi beberapa file buku catatan dan mengonversinya menjadi gambar menggunakan metode serupa yang ditunjukkan dalam tutorial ini.

### Q2: Apakah Aspose.Note untuk .NET kompatibel dengan .NET Core?

A2: Ya, Aspose.Note untuk .NET kompatibel dengan lingkungan .NET Framework dan .NET Core.

### Q3: Apakah ada batasan ukuran buku catatan yang dapat diubah menjadi gambar?

A3: Aspose.Note untuk .NET tidak menerapkan batasan khusus pada ukuran buku catatan yang dapat dikonversi, namun performa dapat bervariasi berdasarkan ukuran dan kompleksitas buku catatan.

### Q4: Dapatkah saya menyesuaikan keluaran gambar lebih jauh dari pengaturan resolusi?

A4: Ya, Aspose.Note untuk .NET menyediakan berbagai opsi untuk menyesuaikan keluaran gambar, seperti menyesuaikan margin, warna, dan tingkat kompresi.

### Q5: Apakah Aspose.Note untuk .NET mendukung format gambar lain selain PNG?

A5: Ya, Aspose.Note untuk .NET mendukung beberapa format gambar, termasuk JPEG, BMP, GIF, dan TIFF.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
