---
title: Simpan ke PDF di Aspose.Note
linktitle: Simpan ke PDF di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menyimpan dokumen Microsoft OneNote ke format PDF menggunakan Aspose.Note untuk .NET. Tutorial langkah demi langkah dengan contoh kode untuk tata letak halaman Letter dan A4.
weight: 26
url: /id/net/loading-and-saving-operations/save-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan ke PDF di Aspose.Note

## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menyimpan dokumen ke format PDF menggunakan Aspose.Note untuk .NET. Aspose.Note adalah perpustakaan canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram. Kami akan membahas prasyarat, mengimpor namespace, dan memberikan panduan langkah demi langkah untuk menyimpan dokumen ke PDF dalam berbagai tata letak halaman.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

- Visual Studio diinstal pada sistem Anda.
-  Aspose.Note untuk perpustakaan .NET diunduh dan diinstal. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/net/).
- Pengetahuan dasar bahasa pemrograman C#.

## Impor Namespace

Pertama, mari impor namespace yang diperlukan ke kode C# kita:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Sekarang kita telah memenuhi prasyarat dan namespace telah diimpor, mari lanjutkan dengan menyimpan dokumen ke PDF dalam tata letak halaman yang berbeda.

## Langkah 1: Simpan ke PDF menggunakan Pengaturan Halaman Surat


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Jalur ke direktori dokumen.
    string dataDir = "Your Document Directory";

    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // Simpan dokumennya.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Penjelasan:

- Kami memuat dokumen OneNote ke Aspose.Note.
- Tentukan jalur tujuan untuk file PDF yang disimpan.
-  Simpan dokumen ke PDF menggunakan`PdfSaveOptions` dengan`PageSettings` mulai`Letter`.

## Langkah 2: Simpan ke PDF menggunakan Pengaturan Halaman A4 Tanpa Batas Tinggi

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Jalur ke direktori dokumen.
    string dataDir = "Your Document Directory";

    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // Simpan dokumennya.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Penjelasan:

- Mirip dengan langkah sebelumnya, kita memuat dokumen OneNote ke Aspose.Note.
- Tentukan jalur tujuan untuk file PDF yang disimpan.
-  Simpan dokumen ke PDF menggunakan`PdfSaveOptions` dengan`PageSettings` mulai`A4NoHeightLimit`.

## Kesimpulan

Dalam tutorial ini, kita mempelajari cara menyimpan dokumen ke format PDF menggunakan Aspose.Note untuk .NET. Kami membahas dua tata letak halaman yang berbeda: Letter dan A4 tanpa batas ketinggian. Dengan Aspose.Note, pengembang dapat dengan mudah memanipulasi file OneNote secara terprogram, memberikan fleksibilitas dan efisiensi dalam tugas manajemen dokumen.

## FAQ

### Q1: Bisakah Aspose.Note menangani file OneNote yang kompleks?

A1: Ya, Aspose.Note mendukung berbagai fitur dan fungsi untuk menangani file OneNote yang kompleks secara efektif.

### Q2: Apakah Aspose.Note cocok untuk proyek komersial?

 A2: Tentu saja, Aspose.Note dapat digunakan dalam proyek komersial dengan mudah. Anda dapat membeli lisensi[Di Sini](https://purchase.aspose.com/buy).

### Q3: Apakah Aspose.Note menawarkan uji coba gratis?

 A3: Ya, Anda dapat menjelajahi Aspose.Note dengan uji coba gratis yang tersedia[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dokumentasi untuk Aspose.Note?

 A4: Anda dapat menemukan dokumentasi terperinci[Di Sini](https://reference.aspose.com/note/net/).

### Q5: Butuh bantuan lebih lanjut?

 A5: Jangan ragu untuk mengajukan pertanyaan atau mencari dukungan di forum Aspose.Note[Di Sini](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
