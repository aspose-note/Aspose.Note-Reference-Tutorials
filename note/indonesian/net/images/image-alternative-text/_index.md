---
date: 2026-04-09
description: Pelajari cara menambahkan teks alt ke gambar di Aspose.Note untuk .NET
  dengan mudah. Tingkatkan aksesibilitas dan perbaiki pengalaman pengguna dengan panduan
  langkah demi langkah ini.
keywords:
- how to add alt text
- add alternative text image
- append image to page
linktitle: Tambahkan Teks Alternatif ke Gambar di Aspose.Note
second_title: Aspose.Note .NET API
title: Cara Menambahkan Teks Alt ke Gambar di Aspose.Note
url: /id/net/images/image-alternative-text/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menambahkan Teks Alt ke Gambar di Aspose.Note

## Pendahuluan

Jika Anda perlu **menambahkan teks alt** untuk gambar dalam dokumen bergaya OneNote Anda, Anda berada di tempat yang tepat. Tutorial ini memandu Anda langkah demi langkah untuk menambahkan teks alternatif (baik judul maupun deskripsi) ke sebuah gambar menggunakan Aspose.Note untuk .NET. Menambahkan teks alt tidak hanya meningkatkan aksesibilitas bagi pengguna pembaca layar tetapi juga memperbaiki SEO untuk konten yang dipublikasikan di web yang kemudian menyematkan gambar-gambar ini.

## Jawaban Cepat
- **Apa arti “teks alt”?** Deskripsi tekstual yang mewakili gambar ketika gambar tidak dapat ditampilkan.  
- **Mengapa menggunakan Aspose.Note untuk teks alt?** Menyediakan API sederhana untuk mengatur baik judul maupun deskripsi secara programatis.  
- **Apa prasyaratnya?** Lingkungan pengembangan .NET, Visual Studio, dan Aspose.Note untuk .NET terpasang.  
- **Bisakah saya menambahkan teks alt ke gambar yang sudah ada?** Ya – Anda dapat memuat objek gambar, mengatur propertinya, dan menyimpan dokumen.  
- **Di mana output disimpan?** Pada jalur yang Anda tentukan dengan `document.Save(...)`.

## Apa itu “menambahkan teks alt” di Aspose.Note?

Menambahkan teks alt berarti menetapkan properti `AlternativeTextTitle` dan `AlternativeTextDescription` pada objek `Image`. Properti ini dibaca oleh pembaca layar dan teknologi bantu lainnya untuk menyampaikan makna gambar.

## Mengapa menambahkan teks alternatif pada gambar di dokumen Anda?

- **Kepatuhan aksesibilitas** – memenuhi pedoman WCAG dan Section 508.  
- **SEO yang lebih baik** – mesin pencari mengindeks teks deskriptif.  
- **Pengalaman pengguna yang lebih baik** – pengguna dengan gambar dinonaktifkan tetap memahami konten.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- Pengetahuan dasar tentang C# dan pengembangan .NET.  
- Visual Studio terpasang di mesin Anda.  
- Aspose.Note untuk .NET yang diunduh dan direferensikan dalam proyek Anda – Anda dapat mendapatkannya [di sini](https://releases.aspose.com/note/net/).  
- Sebuah file gambar (misalnya, `image.jpg`) yang ingin Anda sematkan.

## Impor Namespace

Pertama, sertakan namespace yang diperlukan untuk penanganan file dan objek Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Langkah 1: Inisialisasi Dokumen dan Halaman

Buat instance `Document` baru dan tambahkan `Page` tempat gambar akan berada.

```csharp
var document = new Document();
var page = new Page(document);
```

## Langkah 2: Muat Gambar

Tunjuk folder yang berisi gambar Anda dan buat objek `Image`.

```csharp
string dataDir = "Your Document Directory";
var image = new Image(document, dataDir + "image.jpg");
```

## Langkah 3: Atur Teks Alternatif

Di sini kita **menambahkan teks alternatif gambar** dengan mengisi kedua bidang judul dan deskripsi.

```csharp
image.AlternativeTextTitle = "This is an image's title!";
image.AlternativeTextDescription = "And this is an image's description!";
```

## Langkah 4: Tambahkan Gambar ke Halaman

Sekarang kita **menambahkan gambar ke halaman** menggunakan metode `AppendChildLast`.

```csharp
page.AppendChildLast(image);
```

## Langkah 5: Simpan Dokumen

Tentukan nama file output dan persistensikan dokumen OneNote.

```csharp
dataDir = dataDir + "ImageAlternativeText_out.one";
document.Save(dataDir);
```

## Langkah 6: Tampilkan Pesan Sukses

Pesan konsol sederhana mengonfirmasi bahwa operasi berhasil.

```csharp
Console.WriteLine("\nImage alternative text setup successfully.\nFile saved at " + dataDir); 
```

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **Teks alt tidak muncul** | `AlternativeTextTitle` atau `AlternativeTextDescription` kosong | Pastikan kedua properti diatur sebelum menyimpan. |
| **File tidak ditemukan** | Jalur `dataDir` salah | Gunakan jalur absolut atau verifikasi folder relatif ada. |
| **Exception saat Menyimpan** | Hak tulis tidak cukup | Jalankan Visual Studio sebagai administrator atau pilih folder yang dapat ditulis. |

## Pertanyaan yang Sering Diajukan

### Q1: Mengapa teks alternatif penting untuk gambar?

A1: Teks alternatif menyediakan deskripsi tekstual gambar, membuatnya dapat diakses oleh pengguna yang mengandalkan pembaca layar atau yang menonaktifkan gambar.

### Q2: Bisakah saya menambahkan teks alternatif ke gambar yang sudah ada dalam dokumen?

A2: Ya, Anda dapat dengan mudah menambahkan teks alternatif ke gambar yang sudah ada dalam dokumen menggunakan Aspose.Note untuk .NET.

### Q3: Apakah Aspose.Note kompatibel dengan perpustakaan .NET lainnya?

A3: Aspose.Note terintegrasi mulus dengan perpustakaan .NET lainnya, menyediakan fungsionalitas komprehensif untuk manipulasi dokumen.

### Q4: Bagaimana cara mendapatkan dukungan untuk Aspose.Note?

A4: Anda dapat mendapatkan dukungan untuk Aspose.Note dengan mengunjungi [forum Aspose.Note](https://forum.aspose.com/c/note/28), tempat Anda dapat mengajukan pertanyaan dan menemukan solusi.

### Q5: Apakah ada percobaan gratis untuk Aspose.Note?

A5: Ya, Anda dapat mencoba versi percobaan gratis Aspose.Note dengan mengunjungi [di sini](https://releases.aspose.com/).

## Kesimpulan

Menambahkan teks alt ke gambar adalah langkah kecil yang memberikan dampak besar bagi aksesibilitas, SEO, dan pengalaman pengguna secara keseluruhan. Dengan Aspose.Note untuk .NET, prosesnya sederhana—cukup atur properti `AlternativeTextTitle` dan `AlternativeTextDescription`, tambahkan gambar, dan simpan dokumen.

---

**Terakhir Diperbarui:** 2026-04-09  
**Diuji Dengan:** Aspose.Note 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}