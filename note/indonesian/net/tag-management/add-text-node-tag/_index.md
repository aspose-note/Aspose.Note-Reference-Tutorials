---
title: Tambahkan Node Teks dengan Tag di Aspose.Note
linktitle: Tambahkan Node Teks dengan Tag di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menambahkan node teks dengan tag ke dokumen OneNote menggunakan Aspose.Note untuk .NET.
weight: 12
url: /id/net/tag-management/add-text-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tambahkan Node Teks dengan Tag di Aspose.Note

## Perkenalan

Aspose.Note untuk .NET adalah perpustakaan canggih yang memungkinkan pengembang membuat, memanipulasi, dan mengonversi file Microsoft OneNote secara terprogram menggunakan kerangka .NET. Dalam tutorial ini, kita akan mempelajari cara menambahkan simpul teks dengan tag ke dokumen OneNote menggunakan Aspose.Note untuk .NET.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Visual Studio: Pastikan Anda telah menginstal Visual Studio di sistem Anda.
2.  Aspose.Note untuk .NET: Unduh dan instal Aspose.Note untuk .NET dari[situs web](https://releases.aspose.com/note/net/).
3. Pengetahuan Dasar C#: Biasakan diri Anda dengan dasar-dasar bahasa pemrograman C#.

## Impor Namespace

Pertama, Anda perlu mengimpor namespace yang diperlukan untuk mengakses kelas dan metode yang diperlukan untuk bekerja dengan Aspose.Note untuk .NET.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Langkah 1: Buat Objek Dokumen

Inisialisasi objek Dokumen untuk mulai bekerja dengan dokumen OneNote.

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## Langkah 2: Inisialisasi Objek Halaman dan Garis Besar

Buat objek Halaman dan Kerangka untuk menyusun konten dokumen OneNote.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## Langkah 3: Tambahkan Node Teks dengan Tag

Buat objek RichText dengan teks dan gaya yang diinginkan, lalu tambahkan ke OutlineElement.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## Langkah 4: Tambahkan Elemen Garis Besar dan Node Halaman

Tambahkan OutlineElement ke Outline, lalu tambahkan Outline ke Halaman. Terakhir, tambahkan Halaman ke Dokumen.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Langkah 5: Simpan Dokumen

Simpan dokumen OneNote yang dimodifikasi ke lokasi tertentu.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara menambahkan simpul teks dengan tag ke dokumen OneNote menggunakan Aspose.Note untuk .NET. Dengan pengetahuan ini, Anda kini dapat mengkustomisasi dan menyempurnakan file OneNote Anda secara terprogram.

## FAQ

### Q1: Dapatkah saya menambahkan beberapa node teks dengan tag berbeda dalam dokumen yang sama?

A1: Ya, Anda dapat menambahkan beberapa node teks dengan tag berbeda dengan mengikuti proses yang sama untuk setiap node.

### Q2: Apakah Aspose.Note untuk .NET kompatibel dengan semua versi OneNote?

A2: Aspose.Note untuk .NET mendukung berbagai versi OneNote, termasuk 2010, 2013, 2016, dan yang lebih baru.

### Q3: Dapatkah saya menyesuaikan warna dan gaya tag?

A3: Ya, Anda dapat menyesuaikan warna dan gaya tag sesuai dengan kebutuhan Anda.

### Q4: Apakah Aspose.Note untuk .NET mendukung enkripsi dokumen?

A4: Ya, Aspose.Note untuk .NET mendukung enkripsi dokumen untuk memastikan keamanan data.

### Q5: Di mana saya dapat menemukan lebih banyak sumber daya dan dukungan untuk Aspose.Note untuk .NET?

 A5: Anda dapat menjelajahi[Aspose.Note untuk dokumentasi .NET](https://reference.aspose.com/note/net/)dan mencari bantuan dari[Aspose.Catatan forum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
