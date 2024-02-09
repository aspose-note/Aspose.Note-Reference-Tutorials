---
title: Buat Dokumen OneNote dan Simpan ke HTML di Aspose.Note
linktitle: Buat Dokumen OneNote dan Simpan ke HTML di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara membuat dan menyimpan dokumen Microsoft OneNote ke format HTML di aplikasi .NET menggunakan Aspose.Note API. Ikuti tutorial komprehensif kami dengan contoh langkah demi langkah.
type: docs
weight: 14
url: /id/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## Perkenalan

Aspose.Note untuk .NET adalah API canggih yang memungkinkan pengembang bekerja dengan dokumen Microsoft OneNote secara terprogram dalam aplikasi .NET mereka. Dengan Aspose.Note, Anda dapat membuat, memanipulasi, dan mengonversi file OneNote dengan mudah. Dalam tutorial ini, kita akan mempelajari cara membuat dokumen OneNote dan menyimpannya ke format HTML menggunakan berbagai opsi yang disediakan oleh Aspose.Note untuk .NET API.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

- Pengetahuan dasar bahasa pemrograman C#.
- Visual Studio diinstal pada sistem Anda.
-  Aspose.Note untuk .NET API diinstal di proyek Anda. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/net/).
- Keakraban dengan struktur dokumen Microsoft OneNote.

## Impor Namespace

Sebelum kita mendalami bagian pengkodean, mari impor namespace yang diperlukan:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Sekarang, mari kita bagi setiap contoh menjadi beberapa langkah dan lihat cara membuat dokumen OneNote dan menyimpannya ke format HTML menggunakan Aspose.Note untuk .NET.

## Langkah 1: Buat Dokumen OneNote dengan Opsi Default

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Inisialisasi dokumen OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Gaya default untuk semua teks dalam dokumen.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Simpan ke dalam format HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

Pada langkah ini, kami menginisialisasi dokumen OneNote baru, menambahkan halaman dengan judul, dan menyimpannya ke format HTML menggunakan opsi default.

## Langkah 2: Buat dan Simpan Rentang Halaman Tertentu ke HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Inisialisasi dokumen OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Gaya default untuk semua teks dalam dokumen.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Simpan ke dalam format HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Di sini, kami mendemonstrasikan cara membuat dokumen dan menyimpan rentang halaman tertentu ke format HTML.

## Langkah 3: Simpan sebagai HTML ke Memory Stream dengan Sumber Daya Tersemat

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Muat dokumen OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Tentukan opsi penyimpanan HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Simpan dokumen ke aliran memori
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Langkah ini mengilustrasikan cara menyimpan dokumen OneNote ke format HTML dengan sumber daya tertanam (CSS, font, dan gambar) ke dalam aliran memori.

## Langkah 4: Simpan sebagai HTML ke File dengan Sumber Daya di File Terpisah

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Muat dokumen OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Tentukan opsi penyimpanan HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //Simpan dokumen ke file HTML dengan sumber daya disimpan dalam file terpisah
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

Pada langkah ini, kami menyimpan dokumen OneNote ke format HTML dengan semua sumber daya (CSS, font, dan gambar) disimpan dalam file terpisah.

## Langkah 5: Simpan sebagai HTML ke Memory Stream dengan Callback untuk Menghemat Sumber Daya

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Tentukan konfigurasi penyimpanan panggilan balik
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Tentukan opsi penyimpanan HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Muat dokumen OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Simpan dokumen ke format HTML dengan sumber daya yang dikelola oleh callback yang ditentukan pengguna
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Tambahkan data secara manual ke aliran CSS
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Di sini, kami mendemonstrasikan cara menyimpan dokumen OneNote ke format HTML dengan sumber daya yang dikelola oleh panggilan balik yang ditentukan pengguna.

## Kesimpulan

Dalam artikel ini, kita telah menjelajahi cara bekerja dengan dokumen OneNote dan menyimpannya ke format HTML menggunakan Aspose.Note untuk .NET. Dengan mengikuti panduan langkah demi langkah, Anda bisa dengan mudah

 mengintegrasikan fungsionalitas ini ke dalam aplikasi .NET Anda, memungkinkan Anda memanipulasi file OneNote secara efisien.

## FAQ

### Q1: Dapatkah saya menyesuaikan tampilan file HTML yang disimpan?

A1: Ya, Anda dapat menyesuaikan tampilan dengan memodifikasi stylesheet CSS yang dihasilkan selama proses konversi.

### Q2: Apakah Aspose.Note mendukung konversi ke format lain selain HTML?

A2: Ya, Aspose.Note mendukung konversi ke berbagai format seperti PDF, gambar, dan dokumen Microsoft Word.

### Q3: Apakah Aspose.Note kompatibel dengan aplikasi .NET Core?

A3: Ya, Aspose.Note kompatibel dengan aplikasi .NET Framework dan .NET Core.

### Q4: Bisakah saya mengekstrak teks dan gambar dari dokumen OneNote menggunakan Aspose.Note?

A4: Ya, Anda dapat mengekstrak teks dan gambar serta melakukan berbagai manipulasi lainnya menggunakan Aspose.Note API.

### Q5: Apakah ada versi uji coba yang tersedia untuk menguji fitur Aspose.Note?

 A5: Ya, Anda dapat mengunduh versi uji coba gratis dari[Di Sini](https://releases.aspose.com/).