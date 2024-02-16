---
title: Dapatkan Informasi Gambar di Aspose.Note
linktitle: Dapatkan Informasi Gambar di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara mengekstrak informasi gambar dari file Microsoft OneNote menggunakan Aspose.Note untuk .NET. Ikuti panduan langkah demi langkah kami untuk pengembangan yang efisien.
type: docs
weight: 13
url: /id/net/images/get-info-of-images/
---
## Perkenalan

Dalam dunia pengembangan .NET, Aspose.Note menyediakan seperangkat alat canggih untuk bekerja dengan file Microsoft OneNote. Salah satu tugas umum yang sering dihadapi pengembang adalah mengekstraksi informasi dari gambar yang tertanam dalam catatan ini. Baik itu perolehan dimensi, nama file, atau waktu modifikasi, Aspose.Note menyederhanakan proses ini.

## Prasyarat

Sebelum kita mendalami penggalian informasi gambar dengan Aspose.Note, pastikan Anda memiliki hal berikut:

1. Pengetahuan dasar C#: Keakraban dengan bahasa pemrograman C# sangat penting untuk memahami contoh kode.
2.  Aspose.Note untuk .NET diinstal: Pastikan Anda telah menginstal perpustakaan Aspose.Note di lingkungan pengembangan Anda. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/note/net/).

## Impor Namespace

Sebelum kita mulai, mari impor namespace yang diperlukan:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## Langkah 1: Muat Dokumen

Pertama, muat dokumen OneNote target ke Aspose.Catatan:

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";

// Muat dokumen ke Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

 Mengganti`"Your Document Directory"` dengan jalur ke file OneNote Anda.

## Langkah 2: Ambil Informasi Gambar

Selanjutnya, ambil semua node gambar dari dokumen:

```csharp
// Dapatkan semua node Gambar
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

Cuplikan kode ini mengambil semua node gambar dalam dokumen OneNote yang dimuat.

## Langkah 3: Ulangi Melalui Gambar

Sekarang, mari kita ulangi setiap node gambar untuk mengekstrak metadatanya:

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

Loop ini mencetak berbagai atribut setiap gambar, seperti lebar, tinggi, dimensi asli, nama file, dan waktu modifikasi terakhir.

## Kesimpulan

Dengan Aspose.Note untuk .NET, mengekstraksi informasi gambar dari dokumen OneNote menjadi proses yang lancar. Dengan mengikuti langkah-langkah yang diuraikan dalam tutorial ini, pengembang dapat secara efisien mengambil metadata dari gambar yang disematkan, sehingga memberdayakan mereka untuk membangun aplikasi yang tangguh.

## FAQ

### Q1: Apakah Aspose.Note kompatibel dengan semua versi Microsoft OneNote?

A1: Aspose.Note mendukung berbagai format file OneNote, termasuk .one, .onepkg, dan .onetoc2, memastikan kompatibilitas di berbagai versi.

### Q2: Bisakah saya mengubah properti gambar menggunakan Aspose.Note?

A2: Ya, Aspose.Note memungkinkan Anda memanipulasi properti gambar seperti dimensi, nama file, dan waktu modifikasi secara terprogram.

### Q3: Apakah Aspose.Note menawarkan dukungan untuk .NET Core?

A3: Ya, Aspose.Note menyediakan dukungan untuk .NET Core, memungkinkan pengembangan lintas platform untuk aplikasi Anda.

### Q4: Apakah ada uji coba gratis yang tersedia untuk Aspose.Note?

A4: Ya, Anda dapat mengakses uji coba gratis Aspose.Note untuk menjelajahi fitur-fiturnya sebelum melakukan pembelian.

### Q5: Di mana saya dapat menemukan dukungan atau bantuan tambahan dengan Aspose.Note?

A5: Untuk pertanyaan atau bantuan apa pun, Anda dapat mengunjungi forum Aspose.Note[Di Sini](https://forum.aspose.com/c/note/28).