---
date: 2026-04-06
description: Pelajari cara membuat dokumen OneNote dan menyisipkan gambar secara programatis
  menggunakan Aspose.Note untuk .NET. Ikuti langkah‑langkah mudah untuk menambahkan
  gambar, mengatur perataan, dan lainnya.
keywords:
- create onenote document
- how to insert image
- insert image onenote
- set image alignment
- multiple images onenote
linktitle: Membangun Dokumen dan Menyisipkan Gambar di Aspose.Note
second_title: Aspose.Note .NET API
title: Buat Dokumen OneNote dan Sisipkan Gambar menggunakan Aspose.Note
url: /id/net/images/build-doc-insert-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat Dokumen OneNote dan Sisipkan Gambar menggunakan Aspose.Note

## Pendahuluan

Pada tutorial ini, Anda akan **membuat dokumen OneNote** dan mempelajari **cara menyisipkan gambar** ke dalamnya menggunakan Aspose.Note untuk .NET. Aspose.Note memberi Anda kontrol penuh atas file OneNote, memudahkan penambahan konten kaya seperti gambar, tabel, dan tata letak khusus secara programatis.

## Jawaban Cepat
- **Apa tujuan utama?** Membuat dokumen OneNote dan menyisipkan gambar dengan penjajaran khusus.  
- **Perpustakaan mana yang diperlukan?** Aspose.Note untuk .NET (unduh [di sini](https://releases.aspose.com/note/net/)).  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi berbayar diperlukan untuk produksi.  
- **Bisakah saya menambahkan beberapa gambar?** Ya – ulangi langkah penyisipan untuk setiap gambar (lihat tip “multiple images onenote”).  
- **Apakah konversi ke PDF didukung?** Tentu – Anda dapat kemudian mengonversi dokumen OneNote ke PDF menggunakan metode `Save` Aspose.Note dengan format PDF.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki prasyarat berikut:

1. **Visual Studio** – IDE lengkap untuk pengembangan .NET.  
2. **Aspose.Note untuk .NET** – unduh dan instal perpustakaan dari situs resmi.  
3. **Pemahaman Dasar tentang C#** – familiaritas dengan sintaks C# akan membantu Anda mengikuti contoh kode.

## Impor Namespace

Mari kita mulai dengan mengimpor namespace yang diperlukan ke dalam proyek C# Anda. Namespace ini berisi kelas dan metode yang akan kami gunakan untuk melakukan tugas manipulasi dokumen.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Selanjutnya, mari kita uraikan proses pembuatan dokumen dan penyisipan gambar dalam beberapa langkah:

## Langkah 1: Buat Objek Dokumen

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document();
```

Baris kode ini menginisialisasi instance baru dari kelas `Document`, yang mewakili dokumen OneNote.

## Langkah 2: Inisialisasi Objek Halaman

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

Di sini, kami menginisialisasi instance baru dari kelas `Page`, yang mewakili halaman dalam dokumen OneNote.

## Langkah 3: Inisialisasi Objek Outline

```csharp
Outline outline = new Outline(doc);
```

Kelas `Outline` mewakili node outline dalam hierarki dokumen. Kami membuat objek outline baru untuk menyusun dokumen kami.

## Langkah 4: Inisialisasi Objek OutlineElement

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

`OutlineElement` mewakili elemen dalam sebuah outline. Di sini, kami membuat elemen outline baru untuk menambahkan konten ke dokumen kami.

## Langkah 5: Muat Gambar

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg");
```

Kami memuat file gambar dari jalur yang ditentukan menggunakan konstruktor kelas `Image`.

## Langkah 6: Atur Penjajaran Gambar

```csharp
image.Alignment = HorizontalAlignment.Right;
```

Baris ini mengatur **penjajaran gambar** ke sisi kanan halaman. Anda juga dapat memilih `Left` atau `Center` tergantung pada kebutuhan tata letak Anda.

## Langkah 7: Tambahkan Gambar ke OutlineElement

```csharp
outlineElem.AppendChildLast(image);
```

Di sini, kami menambahkan gambar ke elemen outline, menempatkannya dalam struktur dokumen.

## Langkah 8: Tambahkan OutlineElement ke Outline

```csharp
outline.AppendChildLast(outlineElem);
```

Kami menambahkan elemen outline, bersama dengan gambar yang disisipkan, ke struktur outline dokumen.

## Langkah 9: Tambahkan Outline ke Halaman

```csharp
page.AppendChildLast(outline);
```

Outline yang berisi gambar ditambahkan ke struktur halaman dokumen.

## Langkah 10: Tambahkan Halaman ke Dokumen

```csharp
doc.AppendChildLast(page);
```

Akhirnya, kami menambahkan halaman, lengkap dengan isinya, ke dokumen.

## Langkah 11: Simpan Dokumen

```csharp
dataDir = dataDir + "BuildDocAndInsertImage_out.one";
doc.Save(dataDir);
```

Baris ini menyimpan dokumen OneNote yang telah dimodifikasi ke lokasi yang ditentukan. Anda kemudian dapat **mengonversi OneNote ke PDF** dengan memanggil `doc.Save("output.pdf")`.

## Mengapa Ini Penting

- **Otomatisasi** – Membuat dokumen OneNote secara programatis menghemat waktu dibandingkan dengan penyuntingan manual.  
- **Konsistensi** – Menggunakan kode memastikan setiap dokumen mengikuti tata letak dan aturan gaya yang sama.  
- **Skalabilitas** – Pendekatan yang sama dapat diperluas untuk menyisipkan **multiple images onenote** ke dokumen atau menghasilkan laporan secara massal.

## Kesalahan Umum & Tips

- **Masalah Jalur** – Selalu pastikan bahwa `dataDir` mengarah ke folder yang valid; jika tidak, pemuatan gambar akan gagal.  
- **Ukuran Gambar** – Gambar berukuran besar dapat meningkatkan ukuran file secara signifikan; pertimbangkan untuk mengubah ukuran sebelum penyisipan.  
- **Beberapa Gambar** – Untuk menambahkan lebih dari satu gambar, ulangi Langkah 5‑7 untuk setiap gambar dan tambahkan masing‑masing ke `OutlineElement` yang sama atau berbeda.

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menyisipkan beberapa gambar ke dalam satu dokumen menggunakan Aspose.Note untuk .NET?

A1: Tentu! Anda dapat menyisipkan sebanyak mungkin gambar yang Anda perlukan ke dalam dokumen dengan mengikuti langkah penyisipan yang sama untuk setiap gambar.

### Q2: Apakah Aspose.Note mendukung format file lain selain OneNote?

A2: Ya, Aspose.Note menyediakan dukungan luas untuk berbagai format file, termasuk PDF, DOCX, HTML, dan lainnya.

### Q3: Apakah Aspose.Note cocok untuk solusi manajemen dokumen tingkat perusahaan?

A3: Tentu! Aspose.Note menawarkan fitur yang kuat dan kinerja yang luar biasa, menjadikannya pilihan ideal untuk manajemen dokumen perusahaan.

### Q4: Bisakah saya menyesuaikan tampilan gambar yang disisipkan dalam dokumen?

A4: Ya, Aspose.Note menyediakan opsi lengkap untuk menyesuaikan tampilan gambar, termasuk penjajaran, ukuran, dan rotasi.

### Q5: Di mana saya dapat menemukan sumber daya tambahan dan dukungan untuk Aspose.Note untuk .NET?

A5: Anda dapat menjelajahi dokumentasi Aspose.Note [di sini](https://reference.aspose.com/note/net/) dan mencari bantuan di forum komunitas Aspose [di sini](https://forum.aspose.com/c/note/28/).

---

**Terakhir Diperbarui:** 2026-04-06  
**Diuji Dengan:** Aspose.Note 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}