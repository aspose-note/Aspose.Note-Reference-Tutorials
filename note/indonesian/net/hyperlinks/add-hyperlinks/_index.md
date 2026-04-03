---
date: 2026-04-03
description: Pelajari cara menambahkan hyperlink dalam dokumen Aspose.Note menggunakan
  Aspose.Note untuk .NET, sesuaikan tampilan hyperlink, dan sisipkan beberapa hyperlink
  untuk file OneNote yang lebih kaya.
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: Cara Menambahkan Hyperlink dalam Dokumen Aspose.Note
second_title: Aspose.Note .NET API
title: Cara Menambahkan Hyperlink di Dokumen Aspose.Note
url: /id/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menambahkan Hyperlink dalam Dokumen Aspose.Note

## Pendahuluan

Dalam tutorial ini Anda akan menemukan **cara menambahkan hyperlink** ke teks di dalam dokumen Aspose.Note dengan API .NET. Menambahkan hyperlink mengubah catatan statis menjadi konten interaktif yang dapat diklik—sempurna untuk menautkan ke sumber web, bagian internal, atau file eksternal. Kami akan membimbing Anda melalui setiap langkah, menunjukkan cara **menyesuaikan tampilan hyperlink**, dan menjelaskan cara **menyisipkan beberapa hyperlink** ketika Anda memerlukan halaman OneNote yang lebih kaya.

## Jawaban Cepat
- **Apa kelas utama untuk membuat file OneNote?** `Document` dari Aspose.Note.
- **Properti mana yang membuat teks berperilaku sebagai hyperlink?** `IsHyperlink = true` pada `TextStyle`.
- **Apakah saya dapat menautkan ke situs web eksternal?** Ya, atur `HyperlinkAddress` ke URL seperti `https://www.google.com`.
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi Aspose.Note yang valid diperlukan untuk build non‑evaluation.
- **Versi .NET apa yang didukung?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.

## Apa itu “cara menambahkan hyperlink” dalam Aspose.Note?
Menambahkan hyperlink berarti melampirkan URL ke sepotong teks sehingga ketika pengguna mengkliknya di dalam OneNote, sumber yang ditautkan terbuka di peramban atau aplikasi lain. Aspose.Note menyediakan flag `TextStyle.IsHyperlink` dan properti `HyperlinkAddress` untuk mewujudkan hal ini secara programatik.

## Mengapa menambahkan hyperlink ke dokumen OneNote?
- **Navigasi yang lebih baik:** Langsung melompat ke halaman web atau bagian terkait.
- **Dokumentasi yang ditingkatkan:** Berikan referensi, tutorial, atau file sumber tanpa meninggalkan catatan.
- **Tampilan profesional:** Warna dan gaya yang dapat disesuaikan memungkinkan hyperlink menyatu dengan desain dokumen Anda.

## Prasyarat

1. Pengetahuan dasar tentang C# dan Visual Studio.  
2. Perpustakaan Aspose.Note untuk .NET terpasang – unduh dari [here](https://releases.aspose.com/note/net/).  
3. Memahami struktur dokumen Aspose.Note (halaman, outline, rich text).

## Impor Namespace

Pertama, impor namespace yang memberi Anda akses ke kelas inti Aspose.Note dan tipe dasar .NET.

```csharp
using System;
using System.Drawing;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Buat Objek Document Baru

Instansiasi sebuah `Document` yang akan menampung semua halaman dan konten Anda.

```csharp
Document doc = new Document();
```

### Langkah 2: Definisikan Gaya Teks (termasuk gaya hyperlink)

Buat dua objek `TextStyle` – satu untuk teks biasa dan satu untuk hyperlink.  
Di sini kami juga **menyesuaikan tampilan hyperlink** dengan mengatur warna font.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **Pro tip:** Untuk menyisipkan **beberapa hyperlink**, definisikan objek `TextStyle` tambahan dengan nilai `HyperlinkAddress` yang berbeda dan gunakan kembali mereka dalam segmen `RichText` berikutnya.

### Langkah 3: Buat Objek RichText

Bangun paragraf yang mencampur teks normal dan hyperlink. Metode `Append` memungkinkan Anda menambahkan fragmen bergaya secara berurutan.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### Langkah 4: Buat Outline dan Elemen Outline

Outline berfungsi sebagai wadah untuk elemen visual pada halaman. Atur ukuran dan posisi sesuai kebutuhan.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### Langkah 5: Tambahkan Elemen ke Halaman

Setiap file OneNote terdiri dari halaman. Kami membuat `Title` dan `Page`, lalu melampirkan outline.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### Langkah 6: Simpan Dokumen

Pilih folder, susun nama file lengkap, dan panggil `Save`. File output akan menjadi file OneNote `.one` yang valid berisi hyperlink Anda.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|---------|--------|
| Hyperlink tidak terbuka | Pastikan `HyperlinkAddress` menyertakan protokol (`http://` atau `https://`). |
| Warna teks tidak diterapkan | Setel `FontColor` pada `TextStyle` yang digunakan untuk hyperlink. |
| Membutuhkan beberapa tautan pada satu halaman | Buat beberapa objek `TextStyle`, masing‑masing dengan `HyperlinkAddress` sendiri, dan tambahkan ke objek `RichText` yang sama atau berbeda. |
| Dokumen gagal dimuat di OneNote | Verifikasi bahwa Anda menggunakan versi OneNote yang didukung (2010+). |

## Pertanyaan yang Sering Diajukan

**Q: Apakah saya dapat menambahkan beberapa hyperlink dalam dokumen yang sama menggunakan Aspose.Note?**  
A: Ya, cukup buat instance `TextStyle` tambahan dengan nilai `HyperlinkAddress` yang berbeda dan tambahkan ke objek `RichText` Anda.

**Q: Bagaimana saya dapat menyesuaikan tampilan hyperlink?**  
A: Gunakan properti seperti `FontColor`, `FontName`, dan `FontSize` pada `TextStyle` yang memiliki `IsHyperlink = true`. Ini memungkinkan Anda menyesuaikan dengan branding dokumen.

**Q: Apakah Aspose.Note mendukung hyperlink ke situs web eksternal?**  
A: Tentu saja. Atur `HyperlinkAddress` ke URL yang valid (termasuk `http://` atau `https://`) untuk menautkan keluar dari file OneNote.

**Q: Apakah memungkinkan menghasilkan satu file OneNote yang berisi banyak hyperlink?**  
A: Ya. Dengan terus-menerus menambahkan segmen `RichText` yang bergaya dengan alamat hyperlink berbeda, Anda dapat **menghasilkan koleksi hyperlink dalam satu file**.

**Q: Apakah Aspose.Note kompatibel dengan versi OneNote terbaru?**  
A: Perpustakaan ini bekerja dengan OneNote 2010 dan yang lebih baru, termasuk versi Windows 10 UWP.

**Terakhir Diperbarui:** 2026-04-03  
**Diuji Dengan:** Aspose.Note for .NET 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}