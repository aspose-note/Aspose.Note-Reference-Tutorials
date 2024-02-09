---
title: Tambahkan Node Gambar dengan Tag di Aspose.Note
linktitle: Tambahkan Node Gambar dengan Tag di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menyempurnakan dokumen OneNote Anda dengan menambahkan gambar dengan tag kustom menggunakan Aspose.Note untuk .NET.
type: docs
weight: 10
url: /id/net/tag-management/add-image-node-tag/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menambahkan node gambar dengan tag menggunakan Aspose.Note untuk .NET. Fitur ini memungkinkan Anda menyempurnakan dokumen OneNote Anda dengan menambahkan gambar dengan tag khusus.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal berikut:

1. Visual Studio: Instal Visual Studio IDE di sistem Anda.
2.  Aspose.Note untuk .NET: Unduh dan instal perpustakaan Aspose.Note untuk .NET dari[tautan unduhan](https://releases.aspose.com/note/net/).
3. Pengetahuan Dasar: Biasakan diri Anda dengan bahasa pemrograman C# dan kerangka .NET.

## Impor Namespace

Pertama, pastikan untuk menyertakan namespace yang diperlukan dalam kode C# Anda:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Langkah 1: Inisialisasi Objek Dokumen dan Halaman

 Mulailah dengan membuat sebuah instance dari`Document` kelas dan a`Page` obyek:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Langkah 2: Inisialisasi Objek Outline dan OutlineElement

 Selanjutnya, inisialisasi`Outline` Dan`OutlineElement` objek:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## Langkah 3: Muat dan Sisipkan Gambar

Muat gambar yang diinginkan dan masukkan ke dalam simpul dokumen:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## Langkah 4: Tambahkan Tag ke Gambar

Tambahkan tag khusus ke gambar:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## Langkah 5: Tambahkan Elemen Garis Besar dan Node Halaman

Tambahkan elemen kerangka dan simpul kerangka ke halaman:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## Langkah 6: Simpan Dokumen

Simpan dokumen OneNote yang dimodifikasi:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## Kesimpulan

Dengan mengikuti langkah-langkah ini, Anda dapat dengan mudah menambahkan simpul gambar dengan tag kustom menggunakan Aspose.Note untuk .NET, memperkaya dokumen OneNote Anda dengan visual yang dipersonalisasi.

## FAQ

### Q1: Bisakah saya menambahkan banyak gambar dengan tag berbeda dalam satu dokumen menggunakan Aspose.Note?

A1: Ya, Anda dapat menambahkan beberapa gambar dengan tag berbeda dengan mengikuti langkah serupa untuk setiap gambar.

### Q2: Apakah Aspose.Note kompatibel dengan semua versi OneNote?

A2: Aspose.Note mendukung berbagai versi OneNote, memastikan kompatibilitas di berbagai lingkungan.

### Q3: Dapatkah saya menyesuaikan tampilan tag yang ditambahkan ke gambar?

A3: Ya, Aspose.Note memberikan fleksibilitas dalam menyesuaikan tampilan tag agar sesuai dengan preferensi Anda.

### Q4: Apakah Aspose.Note menawarkan dukungan untuk menambahkan gambar dari URL?

A4: Aspose.Note terutama mendukung penambahan gambar dari direktori lokal, tetapi Anda dapat memasukkan gambar eksternal dengan mengunduhnya secara lokal terlebih dahulu.

### Q5: Apakah ada batasan ukuran atau format gambar yang dapat ditambahkan?

A5: Aspose.Note mendukung berbagai format gambar dan tidak menerapkan batasan ketat pada ukuran gambar, memungkinkan Anda menggabungkan beragam visual ke dalam dokumen Anda.