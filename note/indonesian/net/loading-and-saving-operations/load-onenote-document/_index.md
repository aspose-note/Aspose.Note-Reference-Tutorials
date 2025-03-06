---
title: Muat Dokumen OneNote di Aspose.Note
linktitle: Muat Dokumen OneNote di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara memuat, mengenkripsi, dan mendekripsi dokumen OneNote secara terprogram di .NET menggunakan Aspose.Note.
weight: 16
url: /id/net/loading-and-saving-operations/load-onenote-document/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Muat Dokumen OneNote di Aspose.Note

## Perkenalan

Aspose.Note untuk .NET adalah API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram dalam aplikasi .NET mereka. Baik Anda perlu memuat, memanipulasi, atau mengonversi dokumen OneNote, Aspose.Note untuk .NET menyediakan fungsionalitas komprehensif untuk menyederhanakan alur kerja Anda.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

1. Visual Studio: Instal Visual Studio, lingkungan pengembangan terintegrasi (IDE) yang komprehensif untuk pengembangan .NET.
2.  Aspose.Note untuk .NET: Unduh dan instal Aspose.Note untuk .NET dari[Unduh Halaman](https://releases.aspose.com/note/net/).
3. Pengetahuan Dasar C#: Keakraban dengan dasar-dasar bahasa pemrograman C# diperlukan untuk memahami dan menerapkan contoh yang diberikan dalam tutorial ini.

## Impor Namespace

Sebelum Anda mulai bekerja dengan Aspose.Note untuk .NET, pastikan untuk mengimpor namespace yang diperlukan ke proyek C# Anda:

```csharp
using System;
using System.IO;
```

Mari kita bagi setiap contoh menjadi beberapa langkah:

## Muat Dokumen OneNote di Aspose.Note

### Langkah 1: Muat Notebook Sederhana:
   -  Mulailah dengan membuat instance baru dari`Notebook` kelas, meneruskan jalur ke dokumen OneNote.
   - Iterasi melalui node anak buku catatan menggunakan loop foreach.
   - Menampilkan nama tampilan setiap node anak.
   - Lakukan tindakan spesifik berdasarkan apakah simpul anak adalah dokumen atau buku catatan lain.

```csharp
public static void SimpleLoadNotebook()
{
    // Jalur ke direktori dokumen.
    string dataDir = "Your Document Directory";
    string fileName = "Open Notebook.onetoc2";
    try
    {
        var notebook = new Notebook(Path.Combine(dataDir, fileName));
        foreach (var notebookChildNode in notebook)
        {
            Console.WriteLine(notebookChildNode.DisplayName);
            if (notebookChildNode is Document)
            {
                // Lakukan sesuatu dengan dokumen anak
            }
            else if (notebookChildNode is Notebook)
            {
                // Lakukan sesuatu dengan buku catatan anak
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}
```

### Langkah 2: Periksa Apakah Dokumen Dienkripsi dan Muat:
   -  Periksa apakah dokumen OneNote dienkripsi dengan memanggil`Document.IsEncrypted` metode, meneruskan nama file.
   - Jika tidak dienkripsi, lanjutkan dengan pemrosesan dokumen.
   - Jika dienkripsi, minta pengguna memberikan kata sandi untuk dekripsi.

```csharp
public static void Document_CheckIfEncryptedAndLoad()
{
    // Jalur ke direktori dokumen.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (!Document.IsEncrypted(fileName, out document))
    {
        Console.WriteLine("The document is loaded and ready to be processed.");
    }
    else
    {
        Console.WriteLine("The document is encrypted. Provide a password.");
    }
}
```

### Langkah 3: Periksa Apakah Dokumen Dienkripsi dengan Kata Sandi dan Muat:
   - Mirip dengan langkah sebelumnya, periksa apakah dokumen dienkripsi dengan kata sandi tertentu.
   - Jika dienkripsi dan kata sandi yang benar diberikan, lanjutkan dengan pemrosesan dokumen.
   - Jika dienkripsi tetapi kata sandi yang diberikan salah, beri tahu pengguna tentang kata sandi yang tidak valid.

```csharp
public static void Document_CheckIfEncryptedByPasswordAndLoad()
{
    // Jalur ke direktori dokumen.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (Document.IsEncrypted(fileName, "VerySecretPassword", out document))
    {
        if (document != null)
        {
            Console.WriteLine("The document is decrypted. It is loaded and ready to be processed.");
        }
        else
        {
            Console.WriteLine("The document is encrypted. Invalid password was provided.");
        }
    }
    else
    {
        Console.WriteLine("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
}
```

### Langkah 4: Tangani Format OneNote 2007 yang Tidak Didukung:
   - Mencoba memuat dokumen OneNote dalam format 2007.
   -  Jika formatnya tidak didukung, tangkap`UnsupportedFileFormatException`dan menanganinya dengan tepat, memberi tahu pengguna tentang format yang tidak didukung.

```csharp
public static void Document_OneNote2007_Is_NotSupported()
{
    // Jalur ke direktori dokumen.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "OneNote2007.one");

    try
    {
        new Document(fileName);
    }
    catch (UnsupportedFileFormatException e)
    {
        if (e.FileFormat == FileFormat.OneNote2007)
        {
            Console.WriteLine("It looks like the provided file is in OneNote 2007 format that is not supported.");
        }
        else
            throw;
    }
}
```

## Kesimpulan

Dalam tutorial ini, kita menjelajahi cara memuat dokumen OneNote di Aspose.Note untuk .NET menggunakan berbagai metode. Dengan mengikuti petunjuk langkah demi langkah ini, Anda bisa dengan lancar mengintegrasikan kemampuan pemrosesan dokumen OneNote ke dalam aplikasi .NET Anda.

## FAQ

### Q1: Apakah Aspose.Note untuk .NET kompatibel dengan semua versi Microsoft OneNote?

A1: Aspose.Note untuk .NET mendukung berbagai versi OneNote. Namun, mungkin ada batasan pada format lama seperti OneNote 2007.

### Q2: Bisakah saya mengenkripsi dan mendekripsi dokumen OneNote secara terprogram dengan Aspose.Note untuk .NET?

A2: Ya, Anda dapat memeriksa apakah suatu dokumen dienkripsi dan mendekripsinya menggunakan Aspose.Note untuk .NET.

### Q3: Di mana saya dapat menemukan lebih banyak sumber daya dan dukungan untuk Aspose.Note untuk .NET?

 A3: Anda dapat mengunjungi[Aspose.Note untuk dokumentasi .NET](https://reference.aspose.com/note/net/) untuk panduan dan contoh yang komprehensif. Selain itu, Anda dapat meminta bantuan dari[Aspose.Catatan untuk forum .NET](https://forum.aspose.com/c/note/28).

### Q4: Apakah ada uji coba gratis yang tersedia untuk Aspose.Note untuk .NET?

 A4: Ya, Anda dapat mengunduh uji coba gratis dari[Asumsikan situs web](https://releases.aspose.com/).

### Q5: Bagaimana cara mendapatkan lisensi sementara Aspose.Note untuk .NET?

 A5: Anda dapat meminta lisensi sementara dari[Asumsikan halaman pembelian](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
