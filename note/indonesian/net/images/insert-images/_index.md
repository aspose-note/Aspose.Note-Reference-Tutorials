---
date: 2026-05-05
description: Pelajari cara menyisipkan gambar ke dalam dokumen Aspose.Note menggunakan
  .NET. Panduan langkah demi langkah ini menunjukkan cara menyelaraskan gambar, menambahkan
  gambar ke halaman, dan meningkatkan konten visual.
keywords:
- how to insert image
- how to align image
- append image to page
linktitle: Sisipkan Gambar dalam Dokumen Aspose.Note
second_title: Aspose.Note .NET API
title: Cara Menyisipkan Gambar ke Dokumen Aspose.Note dengan .NET
url: /id/net/images/insert-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menyisipkan Gambar ke Dokumen Aspose.Note dengan .NET

## Pendahuluan

Jika Anda ingin membuat file Aspose.Note Anda lebih menarik, **cara menyisipkan gambar** adalah keterampilan pertama yang harus Anda kuasai. Dalam tutorial ini kami akan memandu langkah‑langkah tepat yang Anda perlukan untuk menambahkan gambar, mengontrol ukuran mereka, menempatkannya dengan presisi, dan bahkan menyelaraskannya sesuai keinginan. Pada akhir tutorial, Anda akan merasa nyaman menyisipkan gambar, menyelaraskannya, dan menambahkan gambar ke halaman—semua dengan kode C# yang bersih dan mudah dibaca.

## Jawaban Cepat
- **Perpustakaan apa yang diperlukan?** Aspose.Note for .NET  
- **Bisakah saya mengatur ukuran gambar secara programatis?** Ya – gunakan properti Width dan Height.  
- **Bagaimana cara memposisikan gambar?** Sesuaikan HorizontalOffset, VerticalOffset atau gunakan opsi penyelarasan.  
- **Apakah ada batasan format gambar?** JPG, PNG, BMP, GIF dan lainnya didukung.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi Aspose.Note yang valid diperlukan untuk penggunaan komersial.

## Apa itu penyisipan gambar di Aspose.Note?

Menyisipkan gambar berarti membuat objek Aspose.Note.Image, mengonfigurasi properti visualnya, dan menempelkannya ke sebuah halaman dalam file .one yang kompatibel dengan OneNote. Ini memungkinkan Anda memperkaya catatan dengan tangkapan layar, diagram, atau bantuan visual apa pun.

## Mengapa menyisipkan gambar dengan Aspose.Note?

- **Komunikasi yang lebih baik:** Visual memperjelas ide kompleks lebih cepat daripada teks saja.  
- **Tata letak konsisten:** Kontrol programatis memastikan setiap dokumen mengikuti standar desain yang sama.  
- **Ramahan otomatisasi:** Ideal untuk menghasilkan laporan, tutorial, atau notebook yang diproses secara batch.

## Prasyarat

1. Aspose.Note untuk .NET: Unduh dan instal Aspose.Note untuk .NET dari [di sini](https://releases.aspose.com/note/net/).  
2. File Gambar: Siapkan file gambar (JPG, PNG, dll.) yang akan Anda sematkan **di disk**.

## Impor Namespace

Kami memulai dengan mengimpor namespace yang memberi kami akses ke I/O file dan API Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Langkah 1: Muat Dokumen dan Dapatkan Halaman

Pertama, buka dokumen .one yang ada dan ambil halaman tempat gambar akan ditempatkan.

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## Cara Menyelaraskan Gambar

Sebelum menambahkan gambar, tentukan bagaimana gambar tersebut harus sejajar dengan konten lainnya. Aspose.Note menyediakan opsi penyelarasan horizontal (Kiri, Tengah, Kanan). Anda juga dapat menyempurnakan penempatan dengan nilai offset.

## Langkah 2: Muat Gambar dan Atur Properti

Buat objek Image, arahkan ke file Anda, dan tentukan dimensinya, offset, serta penyelarasan.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Set image width
    Height = 100,               // Set image height
    HorizontalOffset = 100,     // Set horizontal offset
    VerticalOffset = 400,       // Set vertical offset
    Alignment = HorizontalAlignment.Right  // Set image alignment
};
```

## Tambahkan Gambar ke Halaman

Setelah gambar sepenuhnya dikonfigurasi, lampirkan ke pohon elemen halaman.

```csharp
page.AppendChildLast(image);
```

## Jebakan Umum & Tips

- **Offset yang tidak tepat:** Ingat bahwa offset diukur dari sudut kiri‑atas halaman. Offset vertikal yang besar dapat memindahkan gambar keluar layar.  
- **Format tidak didukung:** Jika Anda mencoba format yang tidak dikenali, Aspose.Note akan melemparkan pengecualian—konversi file ke JPG atau PNG terlebih dahulu.  
- **Peringatan lisensi:** Menjalankan tanpa lisensi menambahkan watermark pada dokumen yang dihasilkan; selalu terapkan lisensi Anda di produksi.

## Kesimpulan

Anda kini telah mempelajari **cara menyisipkan gambar** ke dalam dokumen Aspose.Note, **cara menyelaraskan gambar**, dan **menambahkan gambar ke halaman** menggunakan beberapa baris C# yang sederhana. Teknik ini memungkinkan Anda membangun notebook yang lebih kaya dan profesional secara otomatis.

## FAQ

### Q1: Bisakah saya menyisipkan gambar dalam format apa pun ke dokumen Aspose.Note?
**A:** Ya, Aspose.Note mendukung berbagai format gambar termasuk JPG, PNG, BMP, GIF, dll.

### Q2: Apakah memungkinkan untuk mengubah ukuran gambar yang disisipkan secara programatis?
**A:** Tentu saja! Anda dapat menyesuaikan lebar dan tinggi gambar sesuai keinginan Anda saat penyisipan.

### Q3: Apakah Aspose.Note menyediakan opsi untuk mengubah penyelarasan gambar?
**A:** Ya, Anda dapat menyelaraskan gambar ke kiri, kanan, atau tengah dalam halaman dokumen Anda.

### Q4: Bisakah saya menyisipkan beberapa gambar ke satu halaman dokumen saya?
**A:** Tentu! Anda dapat menyisipkan sebanyak mungkin gambar yang Anda perlukan pada satu halaman menggunakan Aspose.Note.

### Q5: Apakah ada batas ukuran file gambar yang dapat disisipkan?
**A:** Aspose.Note tidak memberlakukan batasan ketat pada ukuran file gambar, tetapi disarankan untuk mengoptimalkan gambar demi kinerja yang lebih baik.

## Pertanyaan yang Sering Diajukan

**Q: Bagaimana cara memuat gambar dari stream alih-alih jalur file?**  
A: Gunakan konstruktor Image(Stream, Document) dan berikan MemoryStream yang berisi byte gambar.

**Q: Bisakah saya mengubah gambar setelah ditambahkan ke halaman?**  
A: Ya, Anda dapat memodifikasi properti Width, Height, HorizontalOffset, VerticalOffset, dan Alignment dari objek Image yang ada, lalu panggil page.Update().

**Q: Apakah memungkinkan menambahkan keterangan di bawah gambar?**  
A: Sisipkan elemen RichText setelah gambar dan atur teksnya sebagai keterangan.

**Q: Apakah Aspose.Note mendukung GIF animasi?**  
A: GIF animasi diperlakukan sebagai gambar statis; hanya frame pertama yang ditampilkan.

**Q: Apa yang harus saya lakukan jika gambar terlihat buram?**  
A: Pastikan gambar sumber memiliki resolusi yang cukup dan hindari memperbesarnya melebihi ukuran aslinya.

---

**Terakhir Diperbarui:** 2026-05-05  
**Diuji Dengan:** Aspose.Note 23.12 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}