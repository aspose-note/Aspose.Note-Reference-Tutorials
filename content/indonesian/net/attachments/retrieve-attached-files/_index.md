---
title: Ambil File Terlampir dengan Aspose.Note
linktitle: Ambil File Terlampir dengan Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara mengambil file lampiran dari dokumen Microsoft OneNote menggunakan Aspose.Note untuk .NET. Ikuti langkah-langkah untuk memuat, mendapatkan node, dan melakukan iterasi melalui lampiran.
type: docs
weight: 12
url: /id/net/attachments/retrieve-attached-files/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara mengambil file lampiran dari dokumen menggunakan Aspose.Note untuk .NET. Aspose.Note adalah API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram. Kami akan membagi prosesnya menjadi beberapa langkah sederhana agar mudah diikuti.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

-  Aspose.Note untuk .NET: Pastikan Anda telah menginstal Aspose.Note untuk .NET. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/net/).

## Impor Namespace

Pertama, mari impor namespace yang diperlukan untuk bekerja dengan Aspose.Catatan:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## Langkah 1: Muat Dokumen

```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";

// Muat dokumen ke Aspose.Note.
Document oneFile = new Document(dataDir + "Sample1.one");
```

## Langkah 2: Dapatkan Node File Terlampir

```csharp
// Dapatkan daftar node file terlampir
IList<AttachedFile> nodes = oneFile.GetChildNodes<AttachedFile>();
```

## Langkah 3: Ulangi Melalui File Terlampir

```csharp
// Iterasi melalui semua node
foreach (AttachedFile file in nodes)
{
    // Muat file terlampir ke objek aliran
    using (Stream outputStream = new MemoryStream(file.Bytes))
    {
        // Buat file lokal
        using (Stream fileStream = System.IO.File.OpenWrite(String.Format(dataDir + file.FileName)))
        {
            // Salin aliran file
            CopyStream(outputStream, fileStream);
        }
    }
}
```

## Kesimpulan

Dalam tutorial ini, kita mempelajari cara mengambil file lampiran dari dokumen menggunakan Aspose.Note untuk .NET. Dengan mengikuti langkah-langkah sederhana ini, Anda dapat mengintegrasikan fungsi ini dengan lancar ke dalam aplikasi .NET Anda.

## FAQ

### Q1: Apakah Aspose.Note kompatibel dengan semua versi file OneNote?

A1: Ya, Aspose.Note mendukung berbagai versi file Microsoft OneNote, memastikan kompatibilitas di berbagai platform.

### Q2: Dapatkah saya mengubah file lampiran yang diambil sebelum menyimpannya secara lokal?

A2: Tentu saja! Anda dapat memanipulasi file lampiran sesuai kebutuhan dalam aplikasi Anda sebelum menyimpannya secara lokal.

### Q3: Apakah Aspose.Note menawarkan dukungan untuk pengembang?

A3: Tentu saja! Aspose menyediakan dokumentasi ekstensif dan forum dukungan khusus untuk membantu pengembang dengan pertanyaan atau masalah apa pun yang mereka temui.

### Q4: Dapatkah saya mencoba Aspose.Note sebelum membelinya?

A4: Ya, Anda dapat memanfaatkan uji coba gratis Aspose.Note untuk menjelajahi fitur dan fungsinya sebelum membuat keputusan pembelian.

### Q5: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Note?

A5: Anda dapat meminta lisensi sementara dari Aspose untuk mengevaluasi kemampuan penuh API di lingkungan pengembangan Anda.