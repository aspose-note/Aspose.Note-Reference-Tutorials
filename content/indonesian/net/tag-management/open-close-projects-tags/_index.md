---
title: Buka dan Tutup Proyek dengan Tag di Aspose.Note
linktitle: Buka dan Tutup Proyek dengan Tag di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara memanipulasi file Microsoft OneNote secara terprogram menggunakan Aspose.Note untuk .NET. Buka dan tutup proyek dengan tag secara efisien.
type: docs
weight: 15
url: /id/net/tag-management/open-close-projects-tags/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menggunakan Aspose.Note untuk .NET untuk membuka dan menutup proyek dengan tag. Aspose.Note adalah API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram, memungkinkan tugas seperti memanipulasi teks, gambar, dan tag dalam dokumen.

## Prasyarat

Sebelum kita mulai, pastikan Anda telah menyiapkan prasyarat berikut:

## Impor Namespace

```csharp
using System.IO;
using System.Linq;
```

Sekarang mari kita bagi setiap contoh menjadi beberapa langkah:

## Langkah 1: Muat Dokumen

Pertama, kita perlu memuat dokumen ke Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Langkah 2: Tutup Item Proyek C

Sekarang, tutup semua item kotak centang yang terkait dengan 'Proyek C'.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Langkah 3: Simpan Catatan Proyek C yang Tertutup

Simpan dokumen yang dimodifikasi dengan item 'Proyek C' yang tertutup.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Langkah 4: Buka Item Proyek C

Selanjutnya, mari kita buka semua item kotak centang yang terkait dengan 'Proyek C'.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Langkah 5: Simpan Catatan Proyek C yang Terbuka

Simpan dokumen yang dimodifikasi dengan item 'Proyek C' yang terbuka.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Sekarang Anda telah mempelajari cara membuka dan menutup proyek dengan tag di Aspose.Note menggunakan .NET.

## Kesimpulan

Aspose.Note untuk .NET menyediakan cara mudah untuk memanipulasi dokumen OneNote secara terprogram. Dengan mengikuti tutorial ini, Anda dapat mengelola proyek Anda secara efisien dengan membuka dan menutup item menggunakan tag.

## FAQ

### Q1: Apakah Aspose.Note kompatibel dengan semua versi OneNote?

A1: Aspose.Note mendukung Microsoft OneNote 2010 dan versi yang lebih baru.

### Q2: Dapatkah saya menggunakan Aspose.Note untuk proyek komersial?

 A2: Ya, Anda dapat menggunakan Aspose.Note untuk proyek pribadi dan komersial. Mengunjungi[Di Sini](https://purchase.aspose.com/buy) untuk membeli lisensi.

### Q3: Apakah Aspose.Note menawarkan uji coba gratis?

 A3: Ya, Anda bisa mendapatkan uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dokumentasi untuk Aspose.Note?

 A4: Anda dapat menemukan dokumentasinya[Di Sini](https://reference.aspose.com/note/net/).

### Q5: Di mana saya bisa mendapatkan dukungan untuk Aspose.Note?

 A5: Untuk dukungan, Anda dapat mengunjungi Aspose.Note[forum](https://forum.aspose.com/c/note/28).