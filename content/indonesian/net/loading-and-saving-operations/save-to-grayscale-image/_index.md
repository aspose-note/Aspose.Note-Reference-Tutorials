---
title: Simpan ke Gambar Grayscale di Aspose.Note
linktitle: Simpan ke Gambar Grayscale di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menyimpan dokumen OneNote sebagai gambar skala abu-abu menggunakan Aspose.Note untuk .NET. Ikuti tutorial komprehensif ini untuk pemrosesan dokumen yang efisien.
type: docs
weight: 24
url: /id/net/loading-and-saving-operations/save-to-grayscale-image/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara memanfaatkan Aspose.Note untuk .NET untuk menyimpan dokumen sebagai gambar skala abu-abu. Aspose.Note adalah perpustakaan canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram, menyediakan berbagai fungsi.

## Prasyarat

Sebelum melanjutkan, pastikan Anda memiliki prasyarat berikut:

- Pemahaman dasar bahasa pemrograman C#.
- Visual Studio diinstal pada sistem Anda.
-  Aspose.Note untuk perpustakaan .NET diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/note/net/).
- Keakraban dalam mengakses dan memanipulasi file menggunakan .NET.

## Impor Namespace

Mari kita mulai dengan mengimpor namespace yang diperlukan:

```csharp
using System;

using Aspose.Note.Saving;

```

## Langkah 1: Muat Dokumen

Pertama, muat dokumen ke Aspose.Note. 

```csharp
string dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Langkah 2: Simpan sebagai Gambar Skala Abu-Abu

Selanjutnya, tentukan jalur untuk menyimpan gambar skala abu-abu dan simpan dokumen sesuai dengan itu.

```csharp
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
oneFile.Save(dataDir, new ImageSaveOptions(SaveFormat.Png)
					  {
						  ColorMode = ColorMode.GrayScale
					  });
```

## Langkah 3: Verifikasi dan Tampilkan Hasil

Terakhir, verifikasi dan tampilkan pesan konversi yang berhasil beserta jalur file.

```csharp
Console.WriteLine("\nOneNote document converted successfully to grayscale image.\nFile saved at " + dataDir);
```

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara menggunakan Aspose.Note untuk .NET untuk mengonversi dokumen menjadi gambar skala abu-abu. Dengan mengikuti langkah-langkah sederhana ini, pengembang dapat secara efisien menggabungkan fungsi ini ke dalam aplikasi mereka, sehingga meningkatkan kemampuan pemrosesan dokumen mereka.

## FAQ

### Q1: Bisakah Aspose.Note menangani file OneNote yang kompleks?

A1: Ya, Aspose.Note dapat secara efisien menangani file OneNote yang kompleks, menyediakan fungsionalitas yang kuat untuk manipulasi dokumen.

### Q2: Apakah Aspose.Note kompatibel dengan format file yang berbeda?

A2: Tentu saja, Aspose.Note mendukung berbagai format file, memastikan fleksibilitas dalam pemrosesan dokumen.

### Q3: Apakah Aspose.Note menawarkan dukungan untuk pengembang?

A3: Ya, pengembang dapat mengakses dukungan komprehensif melalui forum dan dokumentasi Aspose.

### Q4: Dapatkah saya mencoba Aspose.Note sebelum membeli?

A4: Ya, Anda dapat menjelajahi Aspose.Note melalui uji coba gratis yang tersedia di situs web mereka.

### Q5: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Note?

A5: Anda bisa mendapatkan lisensi sementara untuk Aspose.Note dengan mengunjungi tautan yang disediakan dan mengikuti instruksinya.