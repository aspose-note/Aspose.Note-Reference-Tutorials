---
title: Masukkan Daftar Nomor Cina di Teks Aspose.Note
linktitle: Masukkan Daftar Nomor Cina di Teks Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara memasukkan daftar nomor berbahasa Mandarin di Aspose.Note untuk dokumen .NET dengan mudah. Tingkatkan keterampilan pemformatan dokumen Anda dengan panduan langkah demi langkah ini.
type: docs
weight: 20
url: /id/net/text-manipulation/insert-chinese-number-list/
---
## Perkenalan
Apakah Anda ingin meningkatkan keterampilan Aspose.Note untuk .NET Anda dengan memasukkan daftar nomor berbahasa Mandarin ke dalam dokumen Anda? Jika demikian, Anda berada di tempat yang tepat! Dalam tutorial ini, kami akan memandu Anda melalui proses memasukkan daftar nomor berbahasa Mandarin menggunakan Aspose.Note untuk .NET. Pustaka canggih ini memungkinkan Anda memanipulasi dokumen OneNote dengan lancar.
## Prasyarat
Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:
- Pengetahuan dasar tentang pemrograman C#.
-  Aspose.Note untuk .NET diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/note/net/).
## Impor Namespace
Untuk memulai, impor namespace yang diperlukan ke dalam proyek Anda:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Langkah 1: Inisialisasi Dokumen OneNote
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Langkah 2: Inisialisasi Halaman OneNote
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Langkah 3: Terapkan Pengaturan Gaya Teks
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Langkah 4: Buat Elemen Garis Besar
Sekarang, mari buat tiga elemen kerangka dengan daftar nomor berbahasa Mandarin:
### Langkah 4.1: Elemen Pertama
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Langkah 4.2: Elemen Kedua
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Langkah 4.3: Elemen Ketiga
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Langkah 5: Tambahkan Elemen ke Garis Besar
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Langkah 6: Tambahkan Garis Besar ke Halaman
```csharp
page.AppendChildLast(outline);
```
## Langkah 7: Tambahkan Halaman ke Dokumen
```csharp
doc.AppendChildLast(page);
```
## Langkah 8: Simpan Dokumen OneNote
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Selamat! Anda telah berhasil memasukkan daftar nomor berbahasa Mandarin ke dalam dokumen Aspose.Note Anda menggunakan perpustakaan .NET.
## Kesimpulan
Dalam tutorial ini, kami membahas proses langkah demi langkah dalam memasukkan daftar nomor berbahasa Mandarin ke dalam dokumen Aspose.Note untuk .NET Anda. Tingkatkan keterampilan pemformatan dokumen Anda dan buat konten Anda lebih menarik dengan teknik ini.
## FAQ
### T: Dapatkah saya menyesuaikan format daftar nomor berbahasa Mandarin?
 J: Ya, Anda dapat menyesuaikan format dengan menyesuaikan parameter di`NumberList` konstruktor.
### T: Apakah Aspose.Note kompatibel dengan .NET versi terbaru?
J: Ya, Aspose.Note diperbarui secara berkala untuk mendukung versi terbaru .NET.
### T: Di mana saya dapat menemukan contoh dan dokumentasi tambahan?
 A: Jelajahi secara komprehensif[Dokumentasi Aspose.Note](https://reference.aspose.com/note/net/).
### T: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Note?
 A: Dapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).
### T: Di mana saya dapat mencari bantuan atau mendiskusikan pertanyaan terkait Aspose.Note?
 J: Kunjungi[Forum dukungan Aspose.Note](https://forum.aspose.com/c/note/28) untuk dukungan masyarakat.