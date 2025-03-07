---
title: Callback Penghematan Pengguna di Aspose.Note
linktitle: Callback Penghematan Pengguna di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menerapkan callback penyimpanan pengguna di Aspose.Note untuk .NET guna menyesuaikan penyimpanan font, CSS, dan gambar.
weight: 31
url: /id/net/loading-and-saving-operations/user-saving-callbacks/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Callback Penghematan Pengguna di Aspose.Note

## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara mengimplementasikan callback yang menyimpan pengguna di Aspose.Note untuk .NET. Callback ini memungkinkan Anda menyesuaikan proses penyimpanan dengan menyediakan kait untuk melakukan intervensi di berbagai tahapan, seperti menyimpan font, lembar gaya CSS, dan gambar. Dengan memanfaatkan callback ini, Anda dapat menyesuaikan perilaku penyimpanan agar sesuai dengan kebutuhan spesifik Anda, sehingga meningkatkan fleksibilitas dan kontrol atas output.

## Prasyarat

Sebelum mendalami penerapan callback hemat pengguna di Aspose.Note, pastikan Anda memiliki prasyarat berikut:

1.  Aspose.Note untuk .NET SDK: Unduh dan instal Aspose.Note untuk .NET SDK dari[Unduh Halaman](https://releases.aspose.com/note/net/).
   
2. Lingkungan Pengembangan: Siapkan lingkungan pengembangan yang sesuai, seperti Visual Studio atau lingkungan pengembangan .NET lainnya.

## Impor Namespace

Untuk memulai, pastikan untuk mengimpor namespace yang diperlukan ke proyek Anda untuk mengakses kelas dan metode yang diperlukan dari perpustakaan Aspose.Note:

```csharp
using Aspose.Note.Saving.Html;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Sekarang, mari kita uraikan implementasi callback yang menyimpan pengguna menjadi beberapa langkah:

## Langkah 1: Tentukan Properti Panggilan Balik

```csharp
public string RootFolder { get; set; }
public bool KeepCssStreamOpened { get; set; }
public string CssFolder { get; set; }
public Stream CssStream { get; private set; }
public string FontsFolder { get; set; }
public string ImagesFolder { get; set; }
```

Di sini, kami mendefinisikan berbagai properti untuk menentukan folder root, folder CSS, folder font, folder gambar, dan pengaturan relevan lainnya.

## Langkah 2: Terapkan Panggilan Balik Penyimpanan Font

```csharp
public void FontSaving(FontSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.FontsFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = Path.Combine("..", uri).Replace("\\", "\\\\");
}
```

 Pada langkah ini, kami menerapkan`FontSaving` metode panggilan balik untuk menangani penyimpanan font. Ini membuat sumber daya di folder font yang ditentukan dan menetapkan aliran dan URI yang sesuai.

## Langkah 3: Terapkan Panggilan Balik Penghematan CSS

```csharp
public void CssSaving(CssSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.CssFolder, args.FileName, out uri, out stream);
    args.Stream = this.CssStream = stream;
    args.KeepStreamOpen = this.KeepCssStreamOpened;
    args.Uri = uri;
}
```

 Di sini, kami mendefinisikan`CssSaving` metode panggilan balik untuk mengelola penyimpanan stylesheet CSS. Ini membuat sumber daya di folder CSS yang ditentukan dan mengatur aliran, URI, dan properti lainnya sesuai dengan itu.

## Langkah 4: Terapkan Panggilan Balik Penghematan Gambar

```csharp
public void ImageSaving(ImageSavingArgs args)
{
    string uri;
    Stream stream;
    this.CreateResourceInFolder(this.ImagesFolder, args.FileName, out uri, out stream);
    args.Stream = stream;
    args.Uri = uri;
}
```

 Terakhir, kami menerapkan`ImageSaving` metode panggilan balik untuk menangani penyimpanan gambar. Mirip dengan langkah sebelumnya, ini membuat sumber daya di folder gambar yang ditentukan dan menetapkan aliran dan URI.

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara mengimplementasikan callback yang menyimpan pengguna di Aspose.Note untuk .NET. Dengan mengikuti langkah-langkah yang disediakan, Anda dapat menyesuaikan proses penyimpanan font, lembar gaya CSS, dan gambar, sehingga memungkinkan fleksibilitas dan kontrol yang lebih besar terhadap keluaran.

## FAQ

### Q1: Bisakah saya menggunakan callback ini untuk menyesuaikan aspek lain dari proses penyimpanan?

A1: Ya, Anda dapat memperluas callback ini atau menerapkan callback tambahan untuk menyesuaikan berbagai aspek proses penyimpanan sesuai kebutuhan Anda.

### Q2: Apakah Aspose.Note untuk .NET kompatibel dengan kerangka .NET lainnya?

A2: Ya, Aspose.Note untuk .NET kompatibel dengan berbagai kerangka .NET, termasuk .NET Core dan .NET Standard.

### Q3: Bagaimana cara menangani kesalahan atau pengecualian selama proses penyimpanan?

A3: Anda dapat menggabungkan mekanisme penanganan kesalahan dalam setiap metode panggilan balik untuk menangani kesalahan atau pengecualian apa pun yang mungkin terjadi dengan baik.

### Q4: Apakah ada pertimbangan performa saat menggunakan callback ini?

A4: Meskipun callback ini menawarkan fleksibilitas, pastikan callback ini diterapkan secara efisien untuk menghindari overhead kinerja, terutama ketika menangani dokumen atau sumber daya berukuran besar.

### Q5: Bisakah saya mengubah perilaku penyimpanan secara dinamis berdasarkan masukan pengguna atau kondisi lainnya?

A5: Ya, Anda dapat memasukkan logika kondisional dalam metode panggilan balik untuk menyesuaikan perilaku penyimpanan secara dinamis berdasarkan berbagai faktor.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
