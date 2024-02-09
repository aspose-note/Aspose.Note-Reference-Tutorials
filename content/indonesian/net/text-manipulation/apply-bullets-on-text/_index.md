---
title: Terapkan Poin pada Teks di Aspose.Note
linktitle: Terapkan Poin pada Teks di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menerapkan poin pada teks di Aspose.Note untuk .NET untuk menyempurnakan dokumen OneNote Anda. Ikuti panduan langkah demi langkah ini untuk pemformatan yang efektif.
type: docs
weight: 10
url: /id/net/text-manipulation/apply-bullets-on-text/
---
## Perkenalan
Selamat datang di panduan langkah demi langkah dalam menerapkan poin ke teks menggunakan Aspose.Note untuk .NET. Aspose.Note adalah perpustakaan canggih yang memungkinkan pengembang bekerja secara lancar dengan file Microsoft OneNote di aplikasi .NET mereka. Dalam tutorial ini, kami akan memandu Anda melalui proses penerapan poin pada teks, meningkatkan daya tarik visual dokumen OneNote Anda.
## Prasyarat
Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:
- Pengetahuan dasar tentang pemrograman C# dan .NET.
-  Aspose.Note untuk perpustakaan .NET diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/note/net/).
## Impor Namespace
Dalam kode C# Anda, pastikan untuk menyertakan namespace yang diperlukan:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Langkah 1: Siapkan Dokumen Anda
```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
// Buat objek kelas Dokumen
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Langkah 2: Inisialisasi Halaman dan Garis Besar
```csharp
// Inisialisasi objek kelas Halaman
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inisialisasi objek kelas Outline
Outline outline = new Outline(doc);
```
## Langkah 3: Tetapkan Gaya Teks Default
```csharp
// Inisialisasi objek kelas TextStyle dan atur properti pemformatan
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Langkah 4: Buat Elemen Garis Besar dengan Poin
```csharp
// Inisialisasi objek kelas OutlineElement dan terapkan poin
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Ulangi untuk elemen kerangka lainnya
```
## Langkah 5: Tambahkan Elemen Garis Besar ke Garis Besar
```csharp
// Tambahkan elemen kerangka
outline.AppendChildLast(outlineElem1);
// Ulangi untuk elemen kerangka lainnya
```
## Langkah 6: Tambahkan Garis Besar ke Halaman
```csharp
// Tambahkan simpul Garis Besar
page.AppendChildLast(outline);
```
## Langkah 7: Tambahkan Halaman ke Dokumen
```csharp
// Tambahkan simpul Halaman
doc.AppendChildLast(page);
```
## Langkah 8: Simpan Dokumen OneNote
```csharp
// Simpan dokumen OneNote
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Kesimpulan
Selamat! Anda telah berhasil mempelajari cara menerapkan poin ke teks menggunakan Aspose.Note untuk .NET. Fitur ini dapat menyempurnakan pemformatan dokumen OneNote Anda secara signifikan, menjadikannya lebih menarik secara visual.
## FAQ
### Bisakah saya menerapkan gaya poin yang berbeda pada setiap item dalam daftar?
 Ya, Anda dapat menyesuaikan gaya poin dengan memodifikasi`NumberList` properti untuk masing-masing`OutlineElement`.
### Apakah Aspose.Note kompatibel dengan versi terbaru Microsoft OneNote?
Aspose.Note mendukung berbagai versi Microsoft OneNote, memastikan kompatibilitas dengan versi lama dan baru.
### Bisakah saya menggunakan Aspose.Note untuk tujuan komersial?
 Ya, Anda dapat menggunakan Aspose.Note untuk .NET dalam proyek komersial. Untuk mendapatkan lisensi, kunjungi[Di Sini](https://purchase.aspose.com/buy).
### Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk .NET?
 Ya, Anda dapat mengunduh uji coba gratis[Di Sini](https://releases.aspose.com/).
### Di mana saya dapat menemukan dukungan dan sumber daya tambahan?
 Anda dapat mengunjungi forum komunitas Aspose.Note[Di Sini](https://forum.aspose.com/c/note/28) untuk dukungan dan diskusi.