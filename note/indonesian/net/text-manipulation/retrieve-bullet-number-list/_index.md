---
title: Ambil Daftar Poin atau Nomor di Teks Aspose.Note
linktitle: Ambil Daftar Poin atau Nomor di Teks Aspose.Note
second_title: Aspose.Catatan .NET API
description: Buka potensi Aspose.Note untuk .NET dengan panduan langkah demi langkah kami dalam mengambil daftar poin atau nomor. Tingkatkan keterampilan manipulasi dokumen OneNote Anda!
weight: 23
url: /id/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ambil Daftar Poin atau Nomor di Teks Aspose.Note

## Perkenalan
Selamat datang di dunia Aspose.Note untuk .NET, perpustakaan tangguh dan serbaguna yang memberdayakan pengembang untuk menangani manipulasi dokumen OneNote dengan mudah. Dalam tutorial ini, kita akan mempelajari proses mengambil daftar poin atau nomor menggunakan Aspose.Note untuk .NET. Baik Anda seorang pengembang berpengalaman atau penggemar coding, panduan ini akan membekali Anda dengan pengetahuan untuk menavigasi seluk-beluk bekerja dengan daftar di Aspose.Note.
## Prasyarat
Sebelum kita memulai perjalanan coding ini, pastikan Anda memiliki prasyarat berikut:
-  Aspose.Note untuk .NET: Pastikan Anda telah menginstal perpustakaan Aspose.Note. Jika belum, Anda dapat mendownloadnya dari[Aspose.Note untuk dokumentasi .NET](https://reference.aspose.com/note/net/).
- Lingkungan Pengembangan: Siapkan lingkungan pengembangan yang berfungsi, sebaiknya Microsoft Visual Studio, di mesin Anda.
- Pengetahuan Dasar C#: Biasakan diri Anda dengan C# karena tutorial ini ditulis dalam bahasa ini.
## Impor Namespace
Untuk berinteraksi dengan Aspose.Note untuk .NET, Anda perlu mengimpor namespace yang diperlukan ke dalam proyek Anda. Sertakan namespace berikut di awal kode Anda:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Sekarang, mari kita uraikan proses pengambilan daftar poin atau nomor langkah demi langkah:
## Langkah 1: Atur Direktori Dokumen Anda
```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
```
 Mengganti`"Your Document Directory"` dengan jalur sebenarnya di mana dokumen Aspose.Note Anda berada.
## Langkah 2: Muat Dokumen
```csharp
// Muat dokumen ke Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Pastikan Anda menggantinya`"ApplyNumberingOnText.one"` dengan nama dokumen OneNote spesifik Anda.
## Langkah 3: Ambil Koleksi Node
```csharp
// Ambil kumpulan node dari elemen kerangka.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Langkah ini mengambil kumpulan node kerangka dari dokumen yang dimuat.
## Langkah 4: Iterasi Melalui Setiap Node
```csharp
// Iterasi melalui setiap node.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Lanjutkan ke langkah selanjutnya...
    }
}
```
Perulangan ini memastikan bahwa kita hanya berurusan dengan node yang berisi daftar nomor.
## Langkah 5: Ambil Informasi Font
```csharp
// Ambil nama font
Console.WriteLine("Font Name: " + list.Font);
// Ambil panjang font
Console.WriteLine("Font Length: " + list.Font.Length);
// Ambil ukuran font
Console.WriteLine("Font Size: " + list.FontSize);
// Ambil warna font
Console.WriteLine("Font Color: " + list.FontColor);
// Ambil formatnya
Console.WriteLine("Font format: " + list.Format);
// Centang tebal
Console.WriteLine("Is bold: " + list.IsBold);
// Centang miring
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Baris kode ini mengekstrak berbagai informasi terkait font dari daftar nomor.
## Kesimpulan
 Selamat! Anda telah berhasil mempelajari cara mengambil daftar poin atau nomor menggunakan Aspose.Note untuk .NET. Saat Anda melanjutkan penjelajahan, lihat[dokumentasi](https://reference.aspose.com/note/net/) untuk wawasan dan fungsi yang lebih mendalam.
## FAQ
### Bisakah saya menggunakan Aspose.Note untuk .NET dengan bahasa pemrograman lain?
Aspose.Note terutama mendukung .NET, tetapi ada versi perpustakaan lain yang disesuaikan untuk platform dan bahasa berbeda.
### Apakah Aspose.Note kompatibel dengan format OneNote terbaru?
Ya, Aspose.Note mendukung berbagai format OneNote, memastikan kompatibilitas dengan versi terbaru.
### Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.Note?
 Mengunjungi[Link ini](https://purchase.aspose.com/temporary-license/) untuk mendapatkan izin sementara untuk tujuan evaluasi.
### Opsi dukungan apa yang tersedia untuk pengguna Aspose.Note?
Anda dapat menjelajahi dan mencari bantuan di[Aspose.Catatan forum](https://forum.aspose.com/c/note/28) untuk pertanyaan atau masalah apa pun yang mungkin Anda temui.
### Apakah ada versi uji coba gratis Aspose.Note untuk .NET?
 Ya, Anda dapat mengakses Aspose.Note versi uji coba gratis untuk .NET[Di Sini](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
