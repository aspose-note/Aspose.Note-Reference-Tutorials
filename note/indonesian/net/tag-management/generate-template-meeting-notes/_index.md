---
title: Hasilkan Templat untuk Catatan Rapat dengan Aspose.Note
linktitle: Hasilkan Templat untuk Catatan Rapat dengan Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara membuat catatan rapat terstruktur menggunakan Aspose.Note untuk .NET. Tutorial ini memberikan panduan langkah demi langkah dengan contoh kode.
weight: 13
url: /id/net/tag-management/generate-template-meeting-notes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hasilkan Templat untuk Catatan Rapat dengan Aspose.Note

## Perkenalan

Dalam tutorial ini, kita akan memandu proses pembuatan templat untuk catatan rapat menggunakan Aspose.Note untuk .NET. Pustaka ini menyediakan alat canggih untuk membuat, mengedit, dan memanipulasi dokumen OneNote secara terprogram.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1. Visual Studio: Pastikan Anda telah menginstal Visual Studio di sistem Anda.
2.  Aspose.Note untuk .NET: Unduh dan instal Aspose.Note untuk .NET dari[Link ini](https://releases.aspose.com/note/net/).
3. Pemahaman Dasar C#: Keakraban dengan bahasa pemrograman C# diperlukan untuk mengikuti contoh.

## Impor Namespace

Untuk memulai, Anda perlu mengimpor namespace yang diperlukan ke proyek C# Anda. Namespace ini menyediakan akses ke fungsionalitas yang disediakan oleh Aspose.Note untuk .NET.

```csharp
using System;
using System.IO;
```

Sekarang, mari kita uraikan proses pembuatan templat untuk catatan rapat menjadi beberapa langkah:

## Langkah 1: Buat Gaya Penomoran Daftar Nomor

Pertama, kita mendefinisikan metode untuk membuat gaya penomoran untuk daftar kita. Cara ini akan membuat daftar angka dengan format penomoran desimal.

```csharp
private static NumberList CreateListNumberingStyle(ParagraphStyle bodyStyle, bool restart)
{
    return new NumberList("{0}.", NumberFormat.DecimalNumbers, bodyStyle.FontName, bodyStyle.FontSize.GetValueOrDefault()) { Restart = restart ? 1 : 0 };
}
```

## Langkah 2: Tentukan Struktur Dokumen

Selanjutnya, kita menentukan struktur dokumen catatan rapat kita. Ini termasuk menyiapkan gaya untuk paragraf header dan isi, membuat dokumen baru, dan menambahkan judul untuk rapat mingguan.

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
var headerStyle = new ParagraphStyle() { FontName = "Calibri", FontSize = 16 };
var bodyStyle = new ParagraphStyle() { FontName = "Calibri", FontSize = 12 };

var d = new Document();
var outline = d.AppendChildLast(new Page()
                                    {
                                        Title = new Title() { TitleText = new RichText() { Text = $"Weekly meeting {DateTime.Today:d}", ParagraphStyle = ParagraphStyle.Default } }
                                    })
               .AppendChildLast(new Outline() { VerticalOffset = 30, HorizontalOffset = 30 });
```

## Langkah 3: Tambahkan Bagian Poin Penting

Sekarang, kami menambahkan bagian untuk poin-poin penting yang dibahas selama pertemuan. Kami mengulangi daftar poin penting dan menambahkannya ke dokumen.

```csharp
outline.AppendChildLast(new OutlineElement())
       .AppendChildLast(new RichText() { Text = "Important", ParagraphStyle = headerStyle });

foreach (var e in new[] { "First", "Second", "Third" })
{
    outline.AppendChildLast(new OutlineElement() { NumberList = CreateListNumberingStyle(bodyStyle, restartFlag) })
           .AppendChildLast(new RichText() { Text = e, ParagraphStyle = bodyStyle });
    restartFlag = false;
}
```

## Langkah 4: Tambahkan Bagian TO DO

Terakhir, kami menambahkan bagian untuk tugas yang perlu diselesaikan. Mirip dengan bagian poin penting, kami mengulangi daftar tugas dan menambahkan kotak centang untuk setiap tugas.

```csharp
outline.AppendChildLast(new OutlineElement())
       .AppendChildLast(new RichText() { Text = "TO DO", ParagraphStyle = headerStyle, SpaceBefore = 15 });

restartFlag = true;
foreach (var e in new[] { "First", "Second", "Third" })
{
    outline.AppendChildLast(new OutlineElement() { NumberList = CreateListNumberingStyle(bodyStyle, restartFlag) })
           .AppendChildLast(new RichText() { Text = e, ParagraphStyle = bodyStyle, Tags = { NoteCheckBox.CreateBlueCheckBox() } });
    restartFlag = false;
}
```

## Langkah 5: Simpan Dokumen

Terakhir, kami menyimpan dokumen catatan rapat yang dihasilkan ke direktori tertentu.

```csharp
d.Save(Path.Combine(dataDir, "meetingNotes.one"));
```

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara membuat templat untuk catatan rapat menggunakan Aspose.Note untuk .NET. Dengan mengikuti panduan langkah demi langkah, Anda dapat dengan mudah membuat dokumen catatan rapat yang terstruktur dan terorganisir secara terprogram.

## FAQ

### Q1: Dapatkah saya menyesuaikan gaya paragraf header dan isi?

A1: Ya, Anda dapat menyesuaikan nama font, ukuran font, dan atribut gaya lainnya sesuai kebutuhan Anda.

### Q2: Apakah Aspose.Note untuk .NET kompatibel dengan Visual Studio?

A2: Ya, Aspose.Note untuk .NET terintegrasi secara mulus dengan Visual Studio untuk memudahkan pengembangan.

### Q3: Dapatkah saya menambahkan gambar atau tabel ke dokumen catatan rapat saya?

A3: Ya, Aspose.Note untuk .NET menyediakan API untuk menambahkan gambar, tabel, dan elemen lainnya ke dokumen Anda.

### Q4: Apakah Aspose.Note untuk .NET mendukung format dokumen lain selain OneNote?

A4: Ya, Aspose.Note untuk .NET mendukung berbagai format dokumen, termasuk OneNote (*.one) dan PDF.

### Q5: Apakah ada uji coba gratis yang tersedia untuk Aspose.Note untuk .NET?

 A5: Ya, Anda dapat mengunduh uji coba gratis dari[Link ini](https://releases.aspose.com/).
   
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
