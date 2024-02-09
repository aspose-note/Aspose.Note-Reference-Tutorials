---
title: Sisipkan Gambar menggunakan Image Stream di Aspose.Note
linktitle: Sisipkan Gambar menggunakan Image Stream di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menyisipkan gambar dengan lancar ke dalam dokumen Aspose.Note menggunakan aliran gambar di .NET. Sempurnakan file Note Anda dengan visual dengan mudah.
type: docs
weight: 11
url: /id/net/images/insert-image-using-image-stream/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menyisipkan gambar ke dalam dokumen Aspose.Note menggunakan aliran gambar di .NET. Aspose.Note adalah API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram. Dengan mengikuti langkah-langkah yang diuraikan dalam panduan ini, Anda akan mempelajari cara mengintegrasikan gambar ke dalam dokumen Note Anda dengan lancar, sehingga meningkatkan daya tarik visual dan fungsionalitasnya secara keseluruhan.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:
1. Lingkungan Pengembangan: Siapkan lingkungan pengembangan dengan kemampuan .NET.
2.  Perpustakaan Aspose.Note: Unduh dan instal perpustakaan Aspose.Note untuk .NET. Anda dapat menemukan tautan unduhan[Di Sini](https://releases.aspose.com/note/net/).
3. File Gambar: Siapkan file gambar yang ingin Anda masukkan ke dalam dokumen Note Anda.
4. Pemahaman Dasar: Biasakan diri Anda dengan konsep dasar bahasa pemrograman C# dan penanganan file.

## Impor Namespace
Pertama, mari impor namespace yang diperlukan ke proyek kita. Namespace ini akan memberikan akses ke kelas dan metode yang diperlukan untuk bekerja dengan Aspose.Note dan menangani penyisipan gambar.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Sekarang, mari kita uraikan proses memasukkan gambar menggunakan aliran gambar menjadi beberapa langkah.

## Langkah 1: Inisialisasi Objek Dokumen
```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
Document doc = new Document();
```
Kami menginisialisasi instance baru dari kelas Dokumen, yang mewakili dokumen OneNote.

## Langkah 2: Buat Objek Halaman
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```
Kami membuat objek Halaman baru untuk menambahkan konten ke dalamnya.

## Langkah 3: Inisialisasi Objek Outline dan OutlineElement
```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```
Kami membuat instance kelas Outline dan OutlineElement untuk menyusun konten kami di dalam halaman.

## Langkah 4: Muat Gambar dari Stream
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
Kami membuka file gambar menggunakan FileStream dan memuatnya ke dalam objek Gambar. Kita dapat menentukan properti seperti perataan gambar.

## Langkah 5: Tambahkan Gambar ke OutlineElement
```csharp
outlineElem1.AppendChildLast(image1);
```
Kami menambahkan gambar ke OutlineElement, secara efektif menambahkannya ke struktur dokumen.

## Langkah 6: Tambahkan OutlineElement ke Outline
```csharp
outline1.AppendChildLast(outlineElem1);
```
Kami menambahkan OutlineElement yang berisi gambar ke Outline.

## Langkah 7: Tambahkan Garis Besar ke Halaman
```csharp
page.AppendChildLast(outline1);
```
Kami menambahkan Garis Besar ke Halaman, menyelesaikan struktur konten.

## Langkah 8: Tambahkan Halaman ke Dokumen
```csharp
doc.AppendChildLast(page);
```
Kami menambahkan Halaman ke Dokumen, menyelesaikan perakitan dokumen.

## Langkah 9: Simpan Dokumen
```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```
Terakhir, kami menyimpan dokumen rakitan dengan gambar yang disisipkan.

## Kesimpulan
Dengan mengikuti tutorial ini, Anda telah mempelajari cara menyisipkan gambar ke dalam dokumen Aspose.Note menggunakan aliran gambar di .NET. Memanfaatkan kemampuan Aspose.Note, kini Anda dapat dengan mulus mengintegrasikan visual ke dalam file Note Anda, meningkatkan utilitas dan daya tarik visualnya.

## FAQ

### Q1: Bisakah saya menyisipkan banyak gambar ke dalam satu dokumen menggunakan metode ini?

A1: Ya, Anda dapat menyisipkan banyak gambar ke dalam satu dokumen dengan mengulangi langkah-langkah penyisipan gambar untuk setiap gambar.

### Q2: Apakah Aspose.Note mendukung format gambar lain selain JPG?

A2: Ya, Aspose.Note mendukung berbagai format gambar, termasuk PNG, BMP, GIF, dan TIFF.

### Q3: Dapatkah saya menyesuaikan perataan dan ukuran gambar yang disisipkan?

A3: Tentu saja, Aspose.Note menyediakan opsi luas untuk menyesuaikan perataan, ukuran, dan properti lain dari gambar yang disisipkan.

### Q4: Apakah Aspose.Note kompatibel dengan semua versi .NET?

A4: Aspose.Note untuk .NET kompatibel dengan beberapa versi kerangka .NET, memastikan kompatibilitas luas di berbagai lingkungan pengembangan.

### Q5: Di mana saya dapat menemukan sumber daya tambahan dan dukungan untuk Aspose.Note?

 A5: Anda dapat menemukan dokumentasi komprehensif, forum, dan dukungan untuk Aspose.Note di[Asumsikan Forum](https://forum.aspose.com/c/note/28).