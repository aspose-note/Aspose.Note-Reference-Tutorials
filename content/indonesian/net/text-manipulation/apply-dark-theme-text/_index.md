---
title: Transformasi Tema Gelap dengan Aspose.Note untuk .NET
linktitle: Terapkan Tema Gelap ke Teks di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Ubah dokumen OneNote Anda dengan Aspose.Note untuk .NET! Terapkan tema gelap yang ramping dengan mudah. Unduh sekarang dan tingkatkan pengalaman mencatat Anda.
type: docs
weight: 11
url: /id/net/text-manipulation/apply-dark-theme-text/
---
## Perkenalan
Selamat datang di panduan langkah demi langkah kami dalam menerapkan tema gelap pada teks di Aspose.Note untuk .NET. Aspose.Note adalah .NET API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram. Dalam tutorial ini, kita akan mengeksplorasi cara memberikan tampilan ramping dan modern pada dokumen OneNote Anda dengan menerapkan tema gelap pada teks.
## Prasyarat
Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:
-  Aspose.Note untuk .NET: Pastikan Anda telah menginstal Aspose.Note untuk .NET. Jika belum, Anda dapat mendownloadnya dari[Dokumentasi Aspose.Note](https://reference.aspose.com/note/net/).
- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET pilihan Anda, seperti Visual Studio.
- Direktori Dokumen: Siapkan direktori tempat dokumen OneNote Anda berada.
## Impor Namespace
Di proyek .NET Anda, impor namespace yang diperlukan untuk bekerja dengan Aspose.Catatan:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## Langkah 1: Muat Dokumen OneNote
Muat dokumen OneNote Anda ke Aspose.Note menggunakan kode berikut:
```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
// Muat dokumen ke Aspose.Note.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## Langkah 2: Atur Warna Latar Belakang
Atur warna latar belakang setiap halaman menjadi hitam:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## Langkah 3: Sesuaikan Warna Teks
Sesuaikan warna font teks menjadi putih untuk visibilitas yang lebih baik:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## Langkah 4: Simpan Dokumen
Simpan dokumen OneNote yang dimodifikasi sebagai PDF:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## Kesimpulan
Selamat! Anda telah berhasil menerapkan tema gelap pada teks di dokumen Aspose.Note Anda. Peningkatan sederhana namun efektif ini dapat memberikan tampilan lebih canggih pada file OneNote Anda.
## Pertanyaan yang Sering Diajukan
### Bisakah saya menerapkan tema gelap ke bagian tertentu di dokumen OneNote saya?
Ya, Anda dapat menyesuaikan kode untuk menargetkan halaman atau bagian tertentu dalam dokumen Anda.
### Apakah Aspose.Note mendukung format ekspor lain selain PDF?
Sangat! Aspose.Note mendukung berbagai format ekspor, termasuk gambar dan Microsoft Word.
### Apakah ada batasan ukuran dokumen yang dapat ditangani Aspose.Note?
Aspose.Note dapat menangani dokumen dengan berbagai ukuran, dan kinerjanya dioptimalkan untuk efisiensi.
### Bisakah saya kembali ke tema asli setelah menerapkan tema gelap?
Ya, Anda dapat mengubah kode untuk beralih antar tema berdasarkan preferensi Anda.
### Di mana saya bisa mendapatkan dukungan untuk pertanyaan terkait Aspose.Note?
 Untuk bantuan apa pun, kunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28) atau jelajahi[dokumentasi](https://reference.aspose.com/note/net/).