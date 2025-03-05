---
title: Buat Dokumen dengan Judul Halaman di Aspose.Note
linktitle: Buat Dokumen dengan Judul Halaman di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara membuat dokumen dengan halaman berjudul menggunakan Aspose.Note untuk .NET. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
type: docs
weight: 13
url: /id/net/loading-and-saving-operations/create-doc-with-page-title/
---
## Perkenalan

Dalam tutorial ini, kami akan memandu Anda melalui proses pembuatan dokumen dengan halaman berjudul menggunakan Aspose.Note untuk .NET. Aspose.Note adalah API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram.

## Prasyarat

Sebelum kita mulai, pastikan Anda telah menginstal dan menyiapkan prasyarat berikut:

### Instalasi Visual Studio

1. Unduh Visual Studio: Jika Anda belum melakukannya, unduh dan instal Visual Studio dari situs web Microsoft.

2. Instal Beban Kerja Pengembangan .NET: Selama proses instalasi, pastikan untuk memilih beban kerja "pengembangan desktop .NET" untuk memastikan Anda memiliki semua komponen yang diperlukan untuk pengembangan .NET.

3. Buat Proyek Baru: Buka Visual Studio dan buat proyek baru (Aplikasi Konsol atau jenis lain yang Anda inginkan).

### Instalasi Aspose.Note

1.  Dapatkan Aspose.Note: Unduh perpustakaan Aspose.Note untuk .NET dari[situs web](https://releases.aspose.com/note/net/).

2. Instal Aspose.Note melalui NuGet: Alternatifnya, Anda dapat menginstal Aspose.Note untuk .NET melalui NuGet Package Manager di Visual Studio. Cukup cari "Aspose.Note" dan instal versi terbaru.

## Mengimpor Namespace

Pertama, Anda perlu mengimpor namespace yang diperlukan untuk menggunakan Aspose.Note di proyek Anda.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

Sekarang, mari kita uraikan proses pembuatan dokumen dengan judul halaman menjadi beberapa langkah:

## Langkah 1: Buat Objek Dokumen

```csharp
//Buat objek kelas Dokumen
Document doc = new Aspose.Note.Document();
```

## Langkah 2: Inisialisasi Objek Kelas Halaman

```csharp
// Inisialisasi objek kelas Halaman
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Langkah 3: Tetapkan Gaya Default untuk Teks

```csharp
// Gaya default untuk semua teks dalam dokumen.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## Langkah 4: Tetapkan Properti Judul Halaman

```csharp
// Tetapkan properti judul halaman
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Langkah 5: Tambahkan Node Halaman di Dokumen

```csharp
// Tambahkan simpul Halaman dalam dokumen
doc.AppendChildLast(page);
```

## Langkah 6: Simpan Dokumen OneNote

```csharp
// Simpan dokumen OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## Kesimpulan

Selamat! Anda telah berhasil membuat dokumen dengan halaman berjudul menggunakan Aspose.Note untuk .NET. Tutorial ini memberikan panduan langkah demi langkah untuk membantu Anda mengintegrasikan Aspose.Note ke dalam aplikasi .NET Anda untuk mengelola file OneNote secara terprogram.

## FAQ

### Q1: Dapatkah saya menyesuaikan gaya teks judul?

A1: Ya, Anda dapat menyesuaikan warna font, nama font, dan ukuran font teks judul sesuai kebutuhan Anda.

### Q2: Apakah Aspose.Note kompatibel dengan .NET Core?

A2: Ya, Aspose.Note mendukung .NET Core, memungkinkan Anda mengembangkan aplikasi lintas platform.

### Q3: Bisakah saya menambahkan gambar dan lampiran ke dokumen?

A3: Tentu saja! Aspose.Note menyediakan API untuk menambahkan gambar, lampiran, dan elemen lain ke dokumen OneNote Anda dengan lancar.

### Q4: Apakah Aspose.Note mendukung pembacaan file OneNote yang ada?

A4: Ya, Anda bisa menggunakan Aspose.Note untuk membaca, memodifikasi, dan memanipulasi file OneNote yang ada dengan mudah.

### Q5: Di mana saya bisa mendapatkan dukungan jika saya mengalami masalah?

 A5: Anda dapat menemukan dukungan dan bantuan di[Aspose.Catatan forum](https://forum.aspose.com/c/note/28), tempat para pakar dan anggota komunitas dapat membantu menjawab pertanyaan Anda.