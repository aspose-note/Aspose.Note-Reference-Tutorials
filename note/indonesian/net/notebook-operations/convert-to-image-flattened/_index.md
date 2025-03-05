---
title: Konversi Buku Catatan menjadi Gambar (Diratakan) di Aspose Note .NET
linktitle: Konversi Buku Catatan menjadi Gambar (Diratakan) di Aspose Note .NET
second_title: Aspose.Catatan .NET API
description: Pelajari cara mengonversi buku catatan OneNote menjadi gambar rata menggunakan Aspose.Note untuk .NET. Panduan langkah demi langkah untuk integrasi yang lancar.
type: docs
weight: 12
url: /id/net/notebook-operations/convert-to-image-flattened/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menggunakan Aspose.Note untuk .NET untuk mengonversi buku catatan menjadi gambar yang diratakan. Kami akan membagi prosesnya menjadi langkah-langkah sederhana untuk membantu Anda memahami dan menerapkannya secara efektif.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1.  Aspose.Note untuk .NET: Jika Anda belum melakukannya, unduh dan instal Aspose.Note untuk .NET dari[Di Sini](https://releases.aspose.com/note/net/).
2. Lingkungan Pengembangan: Pastikan Anda memiliki lingkungan pengembangan yang sesuai untuk pengembangan .NET.
3. Buku Catatan OneNote: Siapkan buku catatan OneNote yang ingin Anda konversi menjadi gambar.

## Impor Namespace

Sebelum memulai proses konversi, Anda perlu mengimpor namespace yang diperlukan dalam kode Anda:

```csharp
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Sekarang, mari selami panduan langkah demi langkah untuk mengonversi buku catatan menjadi gambar rata menggunakan Aspose.Note untuk .NET.

## Langkah 1: Muat Notebook

Pertama, muat buku catatan OneNote yang ingin Anda konversi menjadi aplikasi Anda.

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";

// Memuat Buku Catatan OneNote
var notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Langkah 2: Tetapkan Opsi Penyimpanan

Tentukan opsi penyimpanan untuk buku catatan, termasuk format dan resolusi gambar.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
notebookSaveOptions.Flatten = true;
```

## Langkah 3: Simpan Buku Catatan sebagai Gambar

Sekarang, simpan buku catatan sebagai gambar yang diratakan menggunakan opsi penyimpanan yang ditentukan.

```csharp
dataDir = dataDir + "ConvertToImageAsFlattenedNotebook_out.png";

// Simpan Buku Catatan
notebook.Save(dataDir, notebookSaveOptions);
```

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara mengonversi buku catatan menjadi gambar rata menggunakan Aspose.Note untuk .NET. Dengan mengikuti panduan langkah demi langkah, Anda dapat mengintegrasikan fungsi ini dengan lancar ke dalam aplikasi .NET Anda.

## FAQ

### Q1: Dapatkah Aspose.Note untuk .NET menangani buku catatan yang rumit?

A1: Ya, Aspose.Note untuk .NET mampu menangani buku catatan kompleks secara efisien.

### Q2: Apakah ada uji coba gratis yang tersedia untuk Aspose.Note untuk .NET?

 A2: Ya, Anda dapat mengunduh uji coba gratis dari[Di Sini](https://releases.aspose.com/).

### Q3: Apakah Aspose memberikan dukungan untuk produknya?

 A3: Ya, Anda bisa mendapatkan dukungan dari komunitas Aspose[Di Sini](https://forum.aspose.com/c/note/28).

### Q4: Bisakah saya membeli lisensi sementara Aspose.Note untuk .NET?

 A4: Ya, Anda dapat membeli lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat menemukan dokumentasi Aspose.Note untuk .NET?

 A5: Anda dapat menemukan dokumentasinya[Di Sini](https://reference.aspose.com/note/net/).