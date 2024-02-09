---
title: Konversi Buku Catatan ke PDF (Diratakan) di Aspose Note .NET
linktitle: Konversi Buku Catatan ke PDF (Diratakan) di Aspose Note .NET
second_title: Aspose.Catatan .NET API
description: Pelajari cara mengonversi buku catatan OneNote menjadi PDF yang diratakan dengan mudah menggunakan Aspose.Note untuk .NET. Pertahankan konten Anda dengan lancar.
type: docs
weight: 15
url: /id/net/notebook-operations/convert-to-pdf-flattened/
---
## Perkenalan

Apakah Anda ingin mengonversi buku catatan OneNote Anda menjadi PDF rata menggunakan Aspose Note .NET? Anda berada di tempat yang tepat! Dalam tutorial ini, kita akan menjalani prosesnya langkah demi langkah.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1.  Aspose.Note untuk .NET: Pastikan Anda telah mengunduh dan menginstal Aspose.Note untuk .NET. Jika tidak, Anda bisa mendapatkannya dari[Di Sini](https://releases.aspose.com/note/net/).
2. Visual Studio: Anda perlu menginstal Visual Studio di sistem Anda untuk pengkodean dan kompilasi.
3. Buku Catatan OneNote: Siapkan Buku Catatan OneNote yang ingin Anda konversi ke PDF.

## Impor Namespace

Mari kita mulai dengan mengimpor namespace yang diperlukan dalam kode C# Anda:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## Langkah 1: Muat Buku Catatan OneNote

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";

// Memuat Buku Catatan OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 Pada langkah ini, kita memuat Buku Catatan OneNote menggunakan`Notebook` kelas yang disediakan oleh Aspose.Note.

## Langkah 2: Konversi ke PDF dengan Perataan

```csharp
// Simpan Notebook sebagai PDF dengan perataan
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 Di sini, kami menyimpan buku catatan yang dimuat sebagai PDF dengan`Flatten` properti disetel ke`true`. Properti ini meratakan semua konten, termasuk anotasi dan gambar, ke dalam PDF.

## Langkah 3: Cetak Pesan Sukses

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

Terakhir, kami mencetak pesan sukses beserta jalur penyimpanan PDF.

## Kesimpulan

Selamat! Anda telah berhasil mengonversi Buku Catatan OneNote Anda ke PDF yang diratakan menggunakan Aspose.Note untuk .NET. Proses ini memastikan bahwa semua konten Anda disimpan secara akurat dalam format PDF, sehingga lebih mudah untuk dibagikan dan didistribusikan.

## FAQ

### Q1: Dapatkah saya mempertahankan elemen interaktif dalam PDF?

A1: Aspose.Note meratakan konten, termasuk elemen interaktif seperti kotak centang atau bidang formulir, ke dalam PDF, menjadikannya statis.

### Q2: Apakah Aspose.Note mendukung konversi buku catatan ke format lain?

A2: Ya, Aspose.Note mendukung konversi buku catatan ke berbagai format seperti PDF, HTML, Gambar, dan lainnya.

### Q3: Dapatkah saya menyesuaikan opsi konversi?

A3: Tentu saja! Aspose.Note memberikan opsi penyesuaian yang luas selama proses konversi, memungkinkan Anda menyesuaikan keluaran sesuai dengan kebutuhan Anda.

### Q4: Apakah ada versi uji coba yang tersedia?

 A4: Ya, Anda bisa mendapatkan uji coba gratis Aspose.Note dari[Di Sini](https://releases.aspose.com/).

### Q5: Di mana saya bisa mendapatkan dukungan jika saya mengalami masalah?

 A5: Anda dapat mencari dukungan dari komunitas Aspose di[Forum Aspose.Note](https://forum.aspose.com/c/note/28).