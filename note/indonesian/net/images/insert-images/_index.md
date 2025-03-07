---
title: Sisipkan Gambar di Dokumen Aspose.Note
linktitle: Sisipkan Gambar di Dokumen Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menyisipkan gambar dengan lancar ke dalam dokumen Aspose.Note menggunakan .NET untuk konten visual yang ditingkatkan. Ikuti panduan langkah demi langkah kami untuk integrasi yang mudah.
weight: 16
url: /id/net/images/insert-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sisipkan Gambar di Dokumen Aspose.Note

## Perkenalan

Menambahkan gambar ke dokumen Aspose.Note Anda dapat meningkatkan daya tarik visual dan kegunaannya secara signifikan. Baik Anda membuat catatan, presentasi, atau dokumen lainnya, mengintegrasikan gambar dapat memberikan konteks dan kejelasan pada konten Anda. Dalam tutorial ini, kami akan memandu Anda melalui proses memasukkan gambar ke dalam dokumen Aspose.Note Anda menggunakan .NET.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1.  Aspose.Note untuk .NET: Unduh dan instal Aspose.Note untuk .NET dari[Di Sini](https://releases.aspose.com/note/net/).
   
2. File Gambar: Siapkan file gambar yang ingin Anda masukkan ke dalam dokumen Aspose.Note Anda.

## Impor Namespace

Pertama, Anda perlu mengimpor namespace yang diperlukan untuk bekerja dengan Aspose.Note di proyek .NET Anda. Inilah cara Anda melakukannya:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Langkah 1: Muat Dokumen dan Dapatkan Halaman

Mulailah dengan memuat dokumen Aspose.Note Anda yang ada dan mengakses halaman yang diinginkan tempat Anda ingin menyisipkan gambar.

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## Langkah 2: Muat Gambar dan Atur Properti

Selanjutnya, muat gambar yang ingin Anda sisipkan dan tentukan propertinya seperti lebar, tinggi, offset, dan perataan sesuai kebutuhan Anda.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Atur lebar gambar
    Height = 100,               // Atur tinggi gambar
    HorizontalOffset = 100,     // Atur offset horizontal
    VerticalOffset = 400,       // Atur offset vertikal
    Alignment = HorizontalAlignment.Right  // Atur perataan gambar
};
```

## Langkah 3: Tambahkan Gambar ke Halaman

Setelah Anda mengonfigurasi properti gambar, tambahkan gambar ke halaman dokumen Aspose.Note yang diinginkan.

```csharp
page.AppendChildLast(image);
```

## Kesimpulan

Selamat! Anda telah berhasil menyisipkan gambar ke dalam dokumen Aspose.Note Anda menggunakan .NET. Gambar dapat meningkatkan representasi visual dokumen Anda secara signifikan, menjadikannya lebih menarik dan informatif.

## FAQ

### Q1: Dapatkah saya menyisipkan gambar dalam format apa pun ke dalam dokumen Aspose.Note?

A1: Ya, Aspose.Note mendukung berbagai format gambar termasuk JPG, PNG, BMP, GIF, dll.

### Q2: Apakah mungkin mengubah ukuran gambar yang disisipkan secara terprogram?

A2: Tentu saja! Anda dapat menyesuaikan lebar dan tinggi gambar sesuai preferensi Anda saat menyisipkan.

### Q3: Apakah Aspose.Note menyediakan opsi untuk mengubah perataan gambar?

A3: Ya, Anda dapat menyelaraskan gambar ke kiri, kanan, atau tengah halaman dokumen Anda.

### Q4: Bisakah saya menyisipkan banyak gambar ke dalam satu halaman dokumen saya?

A4: Tentu saja! Anda dapat menyisipkan gambar sebanyak yang Anda perlukan dalam satu halaman menggunakan Aspose.Note.

### Q5: Apakah ada batasan ukuran file gambar yang dapat disisipkan?

A5: Aspose.Note tidak menerapkan batasan ketat pada ukuran file gambar, namun disarankan untuk mengoptimalkan gambar untuk kinerja yang lebih baik.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
