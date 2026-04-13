---
date: 2026-04-13
description: Pelajari cara menambahkan gambar ke dokumen OneNote menggunakan aliran
  gambar di .NET dengan Aspose.Note. Panduan langkah demi langkah ini mencakup memuat
  gambar dari aliran, menambahkannya ke outline, dan menyimpan file.
keywords:
- add image to onenote
- how to insert image
- load image from stream
- append image to outline
- image stream .net
linktitle: Tambahkan Gambar ke OneNote melalui Aliran Gambar menggunakan Aspose.Note
second_title: Aspose.Note .NET API
title: Tambahkan Gambar ke OneNote melalui Aliran Gambar menggunakan Aspose.Note
url: /id/net/images/insert-image-using-image-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menambahkan Gambar ke OneNote melalui Aliran Gambar menggunakan Aspose.Note

## Pendahuluan

Dalam tutorial ini, Anda akan menemukan **cara menambahkan gambar ke OneNote** dokumen dengan memuat gambar dari aliran dan menambahkannya ke outline menggunakan Aspose.Note untuk .NET. Baik Anda sedang membangun alat pelaporan, aplikasi pencatatan, atau mengotomatisasi dokumentasi, menyisipkan gambar secara programatik membuat file OneNote Anda jauh lebih menarik dan berguna.

## Jawaban Cepat
- **Library apa yang saya butuhkan?** Aspose.Note for .NET (trial gratis tersedia).  
- **Versi .NET apa yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Bisakah saya memuat gambar dari aliran?** Ya – gunakan `FileStream` atau implementasi `Stream` apa pun.  
- **Bagaimana cara mengontrol perataan gambar?** Atur properti `Alignment` (misalnya, `HorizontalAlignment.Right`).  
- **Format file apa yang dihasilkan?** File OneNote (`.one`) yang dapat dibuka di Microsoft OneNote.

## Apa itu “menambahkan gambar ke OneNote”?

Menambahkan gambar ke file OneNote berarti menyematkan elemen visual langsung di dalam hierarki konten halaman. Dengan Aspose.Note Anda bekerja dengan objek seperti `Document`, `Page`, `Outline`, dan `OutlineElement`. Dengan menyisipkan objek `Image` ke dalam `OutlineElement`, gambar menjadi bagian dari tata letak halaman OneNote.

## Mengapa menggunakan Aspose.Note untuk penyisipan gambar?

- **Tidak memerlukan instalasi Office** – menghasilkan atau memodifikasi file OneNote di server.  
- **Kontrol penuh atas tata letak** – mengatur perataan, mengubah ukuran, dan menempatkan gambar tepat di tempat yang Anda inginkan.  
- **Ramahan aliran** – bekerja dengan `Stream` apa pun, cocok untuk penyimpanan cloud atau skenario hanya memori.  
- **Lintas platform** – kompatibel dengan runtime .NET Windows, Linux, dan macOS.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki:

1. **Lingkungan Pengembangan** – Visual Studio 2022 atau IDE .NET‑compatible apa pun.  
2. **Pustaka Aspose.Note** – unduh dari situs resmi [here](https://releases.aspose.com/note/net/).  
3. **File Gambar** – setidaknya satu gambar (JPG, PNG, BMP, GIF, atau TIFF) yang ingin Anda sematkan.  
4. **Pengetahuan Dasar C#** – familiaritas dengan penanganan file dan kode berorientasi objek.

## Mengimpor Namespace
Pertama, impor namespace yang memberi kami akses ke kelas Aspose.Note dan utilitas I/O standar .NET.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Sekarang mari kita jalani proses langkah demi langkah.

### Langkah 1: Inisialisasi Objek Document
Kami memulai dengan membuat instance `Document` baru yang akan menampung file OneNote.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

### Langkah 2: Buat Objek Page
File OneNote terdiri dari satu atau lebih halaman. Di sini kami membuat halaman baru untuk menampung konten kami.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Langkah 3: Inisialisasi Objek Outline dan OutlineElement
Outline adalah wadah untuk konten kaya (teks, gambar, tabel). `OutlineElement` adalah anak yang sebenarnya memegang item-item tersebut.

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```

### Langkah 4: Muat Gambar dari Aliran
Dengan menggunakan `FileStream` (atau `Stream` apa pun) kami membaca file gambar dan membuat objek `Image`. Di sinilah kata kunci **load image from stream** bersinar.

```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```

### Langkah 5: Tambahkan Gambar ke OutlineElement
Gambar kini menjadi bagian dari `OutlineElement`. Langkah ini mendemonstrasikan fungsi **append image to outline**.

```csharp
outlineElem1.AppendChildLast(image1);
```

### Langkah 6: Tambahkan OutlineElement ke Outline
Kami kini menempelkan elemen (dengan gambar) ke wadah outline.

```csharp
outline1.AppendChildLast(outlineElem1);
```

### Langkah 7: Tambahkan Outline ke Page
Outline, yang berisi gambar, ditambahkan ke halaman.

```csharp
page.AppendChildLast(outline1);
```

### Langkah 8: Tambahkan Page ke Document
Dengan halaman siap, kami menyisipkannya ke dalam hierarki dokumen.

```csharp
doc.AppendChildLast(page);
```

### Langkah 9: Simpan Document
Akhirnya, kami menyimpan file OneNote ke disk. File yang dihasilkan dapat dibuka di Microsoft OneNote.

```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```

## Masalah Umum dan Solusinya

| Masalah | Mengapa Terjadi | Solusi |
|-------|----------------|-----|
| **Gambar tidak muncul** | Aliran ditutup sebelum gambar ditambahkan. | Pertahankan blok `using` di sekitar pemanggilan `AppendChildLast` (seperti yang ditunjukkan). |
| **Perataan tidak tepat** | Properti `Alignment` tidak diatur atau ditimpa kemudian. | Atur `Alignment` saat membuat `Image` atau ubah `image1.Alignment` sebelum menambahkan. |
| **Format gambar tidak didukung** | Mencoba memuat format yang tidak dikenali oleh Aspose.Note. | Konversi gambar ke JPG, PNG, BMP, GIF, atau TIFF terlebih dahulu. |
| **Kesalahan jalur file** | `dataDir` mengarah ke folder yang tidak ada. | Gunakan `Path.Combine` dan pastikan folder ada sebelum dijalankan. |

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menyisipkan beberapa gambar ke dalam satu dokumen menggunakan metode ini?**  
**A: Ya. Cukup ulangi langkah *Load Image from Stream* dan *Append Image to OutlineElement* untuk setiap gambar.**

**Q: Apakah Aspose.Note mendukung format gambar lain selain JPG?**  
**A: Tentu saja. PNG, BMP, GIF, dan TIFF semuanya didukung.**

**Q: Bisakah saya menyesuaikan perataan dan ukuran gambar yang disisipkan?**  
**A: Ya. Selain `Alignment`, Anda dapat mengatur properti `Width`, `Height`, dan `Scale` pada objek `Image`.**

**Q: Apakah Aspose.Note kompatibel dengan semua versi .NET?**  
**A: Ini bekerja dengan .NET Framework 4.5+, .NET Core 3.1+, .NET 5, dan .NET 6+.**

**Q: Di mana saya dapat menemukan sumber daya tambahan dan dukungan untuk Aspose.Note?**  
**A: Anda dapat menemukan dokumentasi lengkap, forum, dan dukungan di [Aspose Forum](https://forum.aspose.com/c/note/28).**

**Terakhir Diperbarui:** 2026-04-13  
**Diuji Dengan:** Aspose.Note 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}