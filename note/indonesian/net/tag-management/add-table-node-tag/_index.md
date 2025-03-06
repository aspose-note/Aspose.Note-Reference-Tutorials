---
title: Tambahkan Node Tabel dengan Tag di Aspose.Note
linktitle: Tambahkan Node Tabel dengan Tag di Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menambahkan tabel dengan tag di Aspose.Note untuk .NET. Tingkatkan keterampilan manipulasi dokumen Anda secara terprogram.
weight: 11
url: /id/net/tag-management/add-table-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tambahkan Node Tabel dengan Tag di Aspose.Note

## Perkenalan

Dalam tutorial ini, kami akan memandu Anda melalui proses menambahkan node tabel dengan tag menggunakan Aspose.Note untuk .NET. Ikuti langkah-langkah di bawah ini untuk mencapainya.

## Impor Namespace

Sebelum memulai, pastikan untuk mengimpor namespace yang diperlukan agar berfungsi dengan Aspose.Catatan:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Prasyarat

Pastikan Anda telah menyiapkan prasyarat berikut sebelum melanjutkan:

1.  Instalasi: Unduh dan instal perpustakaan Aspose.Note untuk .NET dari[Di Sini](https://releases.aspose.com/note/net/).
2.  Lisensi: Dapatkan lisensi atau gunakan a[izin sementara](https://purchase.aspose.com/temporary-license/) untuk menggunakan perpustakaan.
3. Lingkungan Pengembangan: Siapkan lingkungan pengembangan yang kompatibel, seperti Visual Studio.

## Langkah 1: Inisialisasi Objek Dokumen dan Halaman

 Mulailah dengan membuat sebuah instance dari`Document` kelas dan inisialisasi a`Page` obyek:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Langkah 2: Buat Objek Tabel, Baris, dan Sel

 Inisialisasi`Table`, `TableRow` , Dan`TableCell` objek:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Langkah 3: Masukkan Konten ke dalam Sel

 Tambahkan konten ke sel dengan menggunakan`AppendChildLast` metode:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Langkah 4: Inisialisasi Node Tabel

 Inisialisasi`Table` objek dengan properti tertentu:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Langkah 5: Tambahkan Baris ke Tabel

Tambahkan simpul baris ke tabel:

```csharp
table.AppendChildLast(row);
```

## Langkah 6: Tambahkan Tag ke Node Tabel

Sertakan tag untuk node tabel:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Langkah 7: Tambahkan Node Tabel ke Elemen Garis Besar

 Buat sebuah`Outline` Dan`OutlineElement` untuk menambahkan simpul tabel:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Langkah 8: Simpan Dokumen

Simpan dokumen OneNote:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Setelah mengikuti langkah-langkah ini, Anda seharusnya berhasil menambahkan simpul tabel dengan tag menggunakan Aspose.Note untuk .NET.

## Kesimpulan

Dalam tutorial ini, kami telah membahas proses menambahkan node tabel dengan tag di Aspose.Note untuk .NET. Dengan mengikuti langkah-langkah ini, Anda dapat memanipulasi dokumen OneNote secara terprogram secara efisien, sehingga meningkatkan kemampuan manajemen dokumen Anda.

## FAQ

### Q1: Apakah Aspose.Note kompatibel dengan semua versi .NET?

A1: Aspose.Note untuk .NET mendukung .NET Framework versi 2.0 dan yang lebih baru, termasuk .NET Core dan .NET Standard.

### Q2: Dapatkah saya mencoba Aspose.Note sebelum membeli lisensi?

 A2: Ya, Anda bisa mendapatkan uji coba gratis Aspose.Note dari[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana cara memperoleh lisensi sementara untuk Aspose.Note?

 A3: Anda bisa mendapatkan lisensi sementara dari[Link ini](https://purchase.aspose.com/temporary-license/), yang berlaku selama 30 hari.

### Q4: Apakah Aspose.Note mendukung enkripsi dokumen?

A4: Ya, Aspose.Note menyediakan dukungan untuk mengenkripsi dokumen OneNote untuk memastikan keamanan data.

### Q5: Apakah dukungan teknis tersedia untuk pengguna Aspose.Note?

 A5: Ya, dukungan teknis diberikan melalui forum Aspose[Di Sini](https://forum.aspose.com/c/note/28), di mana Anda dapat mencari bantuan dari para ahli.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
