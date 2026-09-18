---
date: 2026-04-09
description: Pelajari cara mengekstrak metadata gambar dan mendapatkan dimensi gambar
  dari file OneNote dengan Aspose.Note untuk .NET. Panduan langkah demi langkah untuk
  pengembang C#.
keywords:
- extract image metadata
- how to extract images
- get image dimensions
- load onenote document
- c# get image properties
linktitle: Cara mengekstrak metadata gambar dari OneNote menggunakan Aspose.Note
second_title: Aspose.Note .NET API
title: Cara mengekstrak metadata gambar dari OneNote menggunakan Aspose.Note
url: /id/net/images/get-info-of-images/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekstrak Metadata Gambar dengan Aspose.Note untuk .NET

Dalam tutorial praktis ini Anda akan belajar **cara mengekstrak metadata gambar**—termasuk lebar, tinggi, ukuran asli, nama file, dan waktu modifikasi—dari file Microsoft OneNote menggunakan pustaka Aspose.Note untuk C#. Baik Anda perlu menampilkan thumbnail gambar, memvalidasi ukuran gambar, atau membangun katalog aset tersemat, mengekstrak informasi ini secara programatik menghemat banyak langkah manual.

## Jawaban Cepat
- **Apa arti “extract image metadata”?** Mengambil properti seperti dimensi, nama file, dan cap waktu dari gambar yang disimpan di dalam dokumen OneNote.  
- **Pustaka mana yang menangani ini?** Aspose.Note untuk .NET.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Platform yang didukung?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Waktu eksekusi tipikal?** Kurang dari satu detik untuk file .one standar.

## Apa itu ekstrak metadata gambar?
Mengekstrak metadata gambar berarti secara programatik membaca atribut deskriptif (lebar, tinggi, dimensi asli, nama file, waktu terakhir diubah, dll.) yang menyertai setiap objek gambar di dalam halaman OneNote. Data ini berguna untuk validasi, pelaporan, atau pemrosesan gambar lebih lanjut.

## Mengapa mengekstrak metadata gambar dari OneNote?
- **Otomasi** – Membuat alat yang secara otomatis menghasilkan inventaris gambar.  
- **Validasi** – Memastikan gambar memenuhi persyaratan ukuran sebelum dipublikasikan.  
- **Integrasi** – Menggabungkan konten OneNote dengan sistem lain yang memerlukan detail gambar (CMS, DAM, dll.).  
- **Kinerja** – Menghindari memuat seluruh biner gambar ketika hanya dimensi yang diperlukan.

## Prasyarat
1. **Fundamental C#** – Anda harus nyaman menulis kode C# dasar.  
2. **Aspose.Note untuk .NET** – Unduh dan instal pustaka dari situs resmi [di sini](https://releases.aspose.com/note/net/).  
3. **File OneNote (.one)** – Dokumen OneNote yang ada yang berisi gambar.

## Impor Namespace
Sebelum kita mulai, impor namespace yang diperlukan:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## Langkah 1: Muat dokumen OneNote
Pertama, muat file OneNote target ke dalam objek `Aspose.Note.Document`. Ini adalah langkah **load onenote document** yang menyiapkan API untuk kueri selanjutnya.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Ganti `"Your Document Directory"` dengan folder sebenarnya yang berisi file `.one` Anda.

## Langkah 2: Ambil semua node gambar
Sekarang kita akan **cara mengekstrak gambar** dengan mengambil setiap node `Image` dari dokumen.

```csharp
// Get all Image nodes
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

Metode `GetChildNodes<T>()` memindai seluruh hierarki notebook dan mengembalikan koleksi objek gambar.

## Langkah 3: Iterasi setiap gambar dan **c# get image properties**
Kita akan mengulangi koleksi dan mencetak metadata, termasuk nilai **get image dimensions** dan **extract original image size**.

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

Output menampilkan lebar/tinggi saat ini setiap gambar (seperti yang ditampilkan di halaman), dimensi asli yang disimpan dalam file, nama file, dan cap waktu modifikasi terakhir.

## Masalah Umum dan Solusinya
| Masalah | Alasan | Solusi |
|-------|--------|-----|
| **NullReferenceException** ketika `images` kosong | Dokumen tidak berisi gambar | Pastikan file `.one` sumber memang memiliki gambar tersemat. |
| **Dimensi tidak tepat** | Gambar diubah skala di OneNote | Gunakan `OriginalWidth`/`OriginalHeight` untuk memperoleh ukuran sebenarnya. |
| **FileName kosong** | Gambar ditempelkan dari clipboard | API mungkin tidak memiliki nama file; tangani `null` atau string kosong dalam kode Anda. |

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.Note kompatibel dengan semua versi Microsoft OneNote?**  
A: Aspose.Note mendukung format .one, .onepkg, dan .onetoc2, mencakup sebagian besar versi OneNote sejak 2007.

**Q: Apakah saya dapat memodifikasi properti gambar setelah ekstraksi?**  
A: Ya, Anda dapat mengubah properti seperti `Width`, `Height`, atau `FileName` dan kemudian menyimpan dokumen.

**Q: Apakah Aspose.Note bekerja dengan .NET Core?**  
A: Tentu saja. Pustaka ini sepenuhnya kompatibel dengan .NET Core, .NET 5, dan .NET 6.

**Q: Apakah tersedia versi percobaan gratis?**  
A: Ya, Anda dapat mengunduh versi percobaan dari situs web Aspose untuk menjelajahi semua fitur.

**Q: Di mana saya dapat mendapatkan bantuan tambahan atau dukungan komunitas?**  
A: Kunjungi forum Aspose.Note [di sini](https://forum.aspose.com/c/note/28) untuk tips, contoh kode, dan jawaban dari komunitas.

---

**Terakhir Diperbarui:** 2026-04-09  
**Diuji Dengan:** Aspose.Note 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}