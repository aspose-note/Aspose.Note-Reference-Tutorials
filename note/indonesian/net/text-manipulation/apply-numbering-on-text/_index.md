---
title: Terapkan Penomoran pada Teks di Aspose.Note
linktitle: Terapkan Penomoran pada Teks di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menerapkan penomoran teks di Aspose.Note untuk .NET dengan tutorial komprehensif ini. Sempurnakan pemformatan dokumen Anda dengan mudah.
type: docs
weight: 12
url: /id/net/text-manipulation/apply-numbering-on-text/
---
## Perkenalan
Aspose.Note untuk .NET menyediakan alat canggih untuk manipulasi dokumen dalam aplikasi C#. Dalam tutorial ini, kita akan mengeksplorasi proses penerapan penomoran pada teks menggunakan Aspose.Note. Ikuti petunjuk langkah demi langkah berikut untuk menyempurnakan format dokumen Anda dengan mudah.
## Prasyarat
Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:
- Pemahaman dasar bahasa pemrograman C#.
-  Aspose.Note untuk .NET diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/note/net/).
- Lingkungan pengembangan terintegrasi (IDE) seperti Visual Studio.
## Impor Namespace
Untuk memulai, pastikan untuk mengimpor namespace yang diperlukan dalam proyek C# Anda:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Langkah 1: Siapkan Dokumen Anda
Mulailah dengan membuat dokumen baru dan menginisialisasi objek yang diperlukan:
```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
//Buat objek kelas Dokumen
Document doc = new Document();
// Inisialisasi objek kelas Halaman
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Inisialisasi objek kelas Outline
Outline outline = new Outline(doc);
```
## Langkah 2: Tentukan Gaya Default
Siapkan gaya default untuk teks Anda menggunakan kelas ParagraphStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Langkah 3: Terapkan Penomoran
Inisialisasi objek kelas OutlineElement dan terapkan penomoran ke setiap elemen:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Langkah 4: Tambahkan Elemen Garis Besar
Tambahkan elemen kerangka ke kerangka:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Langkah 5: Simpan Dokumen
Simpan dokumen OneNote dengan penomoran yang diterapkan:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Kesimpulan
Selamat! Anda telah berhasil mempelajari cara menerapkan penomoran pada teks di Aspose.Note untuk .NET. Bereksperimenlah dengan berbagai opsi pemformatan untuk membuat dokumen yang menarik secara visual dengan mudah.
## FAQ
### 1. Bisakah saya menyesuaikan format penomoran?
Ya, kelas NumberList memungkinkan Anda untuk menyesuaikan format penomoran sesuai dengan preferensi Anda.
### 2. Apakah ada opsi pemformatan lain yang tersedia?
Aspose.Note menyediakan berbagai pilihan pemformatan, termasuk gaya font, warna, dan banyak lagi.
### 3. Apakah Aspose.Note kompatibel dengan Visual Studio?
Sangat! Aspose.Note terintegrasi secara mulus dengan Visual Studio untuk pengalaman pengembangan yang lancar.
### 4. Bisakah saya mencoba Aspose.Note sebelum membeli?
 Tentu! Anda dapat menjelajahi uji coba gratis[Di Sini](https://releases.aspose.com/).
### 5. Di mana saya bisa mendapatkan dukungan untuk Aspose.Note?
 Untuk bantuan atau pertanyaan apa pun, kunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28).