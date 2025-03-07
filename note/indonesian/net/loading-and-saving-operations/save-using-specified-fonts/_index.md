---
title: Simpan Menggunakan Font Tertentu di Aspose.Note
linktitle: Simpan Menggunakan Font Tertentu di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menyimpan dokumen dengan font tertentu di Aspose.Note untuk .NET. Sesuaikan pengaturan font dengan mudah untuk format dokumen yang konsisten.
weight: 28
url: /id/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan Menggunakan Font Tertentu di Aspose.Note

## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menyimpan dokumen menggunakan font tertentu di Aspose.Note untuk .NET. Kami akan mengeksplorasi berbagai metode untuk mencapai hal ini, langkah demi langkah.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1.  Aspose.Note untuk .NET: Pastikan Anda telah menginstal Aspose.Note untuk .NET. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/net/).

2. Lingkungan Pengembangan: Anda memerlukan lingkungan pengembangan yang disiapkan untuk pengembangan .NET.

## Impor Namespace

Pertama, mari impor namespace yang diperlukan:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Langkah 1: Menyimpan dengan Nama Font Default

Pada langkah ini, kita akan menyimpan dokumen menggunakan nama font default yang ditentukan.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Jalur ke direktori dokumen.
    string dataDir = "Your Document Directory";

    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Simpan dokumen sebagai PDF dengan font default yang ditentukan.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Langkah 2: Menyimpan dengan Font Default dari File

Selanjutnya, mari kita simpan dokumen menggunakan font default yang diambil dari file.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Jalur ke direktori dokumen.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Simpan dokumen sebagai PDF dengan font default dimuat dari file.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Langkah 3: Menyimpan dengan Font Default dari Stream

Terakhir, mari simpan dokumen menggunakan font default yang diambil dari aliran.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Jalur ke direktori dokumen.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Simpan dokumen sebagai PDF dengan font default yang dimuat dari aliran.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Kesimpulan

Dalam tutorial ini, kita menjelajahi cara menyimpan dokumen menggunakan font tertentu di Aspose.Note untuk .NET. Dengan mengikuti langkah-langkah ini, Anda dapat menyesuaikan pengaturan font sesuai kebutuhan Anda, memastikan dokumen Anda diformat sesuai keinginan.

## FAQ

### Q1: Dapatkah saya menggunakan font apa pun untuk menyimpan dokumen di Aspose.Note?

A1: Ya, Anda dapat menentukan font apa saja untuk menyimpan dokumen. Pastikan saja file font dapat diakses dan dimuat dengan benar.

### Q2: Apakah Aspose.Note kompatibel dengan format dokumen yang berbeda?

A2: Aspose.Note terutama berfungsi dengan dokumen OneNote tetapi menyediakan opsi untuk menyimpan dalam berbagai format termasuk PDF.

### Q3: Bagaimana cara menangani font yang hilang saat menyimpan dokumen?

A3: Aspose.Note menawarkan opsi untuk menggunakan font default jika font yang ditentukan hilang, memastikan format dokumen konsisten.

### Q4: Apakah Aspose.Note mendukung penyematan font di dokumen keluaran?

A4: Ya, Aspose.Note memungkinkan penyematan font untuk memastikan portabilitas dokumen dan rendering yang konsisten di berbagai platform.

### Q5: Di mana saya bisa mendapatkan bantuan lebih lanjut dengan Aspose.Note?

 A5: Untuk bantuan atau dukungan teknis lebih lanjut, Anda dapat mengunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
