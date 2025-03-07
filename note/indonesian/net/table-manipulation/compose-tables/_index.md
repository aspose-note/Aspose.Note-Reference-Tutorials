---
title: Buat Tabel dengan Aspose.Note
linktitle: Buat Tabel dengan Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara membuat tabel terstruktur dengan konten teks kaya menggunakan Aspose.Note untuk .NET. Tingkatkan pengorganisasian dan keterbacaan dokumen dengan mudah.
weight: 11
url: /id/net/table-manipulation/compose-tables/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat Tabel dengan Aspose.Note

## Perkenalan

Tabel adalah komponen dasar dokumen, yang memungkinkan penyajian informasi terstruktur. Aspose.Note untuk .NET menyediakan alat canggih untuk menyusun tabel dengan mudah. Dalam tutorial ini, kami akan memandu Anda melalui proses pembuatan tabel dengan konten teks kaya menggunakan Aspose.Note.

## Prasyarat

Sebelum mendalami komposisi tabel dengan Aspose.Note untuk .NET, pastikan Anda memiliki prasyarat berikut:

1. Pengaturan Lingkungan: Pastikan Anda memiliki lingkungan pengembangan yang sesuai dengan .NET Framework atau .NET Core.
2.  Instalasi: Unduh dan instal Aspose.Note untuk .NET dari[situs web](https://releases.aspose.com/note/net/).
3. Pengetahuan Dasar: Biasakan diri Anda dengan konsep dasar pemrograman C# dan manipulasi dokumen.

## Impor Namespace

Sebelum Anda mulai membuat tabel, pastikan Anda mengimpor namespace yang diperlukan:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Mari kita bagi contoh yang diberikan menjadi langkah-langkah yang dapat dikelola:

## Langkah 1: Siapkan Direktori Dokumen

Sebelum membuat tabel, tentukan direktori tempat dokumen akan disimpan.

```csharp
string dataDir = "Your Document Directory";
```

## Langkah 2: Buat Teks Header

Tentukan teks header dengan gaya tertentu seperti ukuran font dan ketebalan.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Langkah 3: Buat Halaman dan Garis Besar

Inisialisasi halaman dan kerangka untuk menyusun konten.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Langkah 4: Tambahkan Teks Ringkasan

Sertakan teks ringkasan sebelum tabel.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Langkah 5: Buat Tabel

Inisialisasi tabel untuk mengatur data dalam baris dan kolom.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Langkah 6: Tambahkan Baris Header

Isi tabel dengan baris header yang berisi judul kolom.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Langkah 7: Tambahkan Baris Kosong

Sisipkan baris kosong untuk mempersiapkan penyisipan data.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Langkah 8: Tambahkan Informasi Kontak

Isi kolom 'Kontak' dengan konten templat.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Langkah 9: Simpan Dokumen

Simpan dokumen tabel yang telah dibuat.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Langkah 10: Konfirmasi

Konfirmasikan komposisi dokumen yang berhasil.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi cara membuat tabel dengan konten teks kaya menggunakan Aspose.Note untuk .NET. Dengan mengikuti petunjuk langkah demi langkah ini, Anda dapat membuat tabel terstruktur secara efisien dalam dokumen Anda, sehingga meningkatkan keterbacaan dan pengorganisasian.

## FAQ

### Q1: Dapatkah saya menyesuaikan gaya elemen tabel?
   
A1: Ya, Anda dapat menyesuaikan berbagai aspek seperti ukuran font, warna, dan perataan agar sesuai dengan kebutuhan Anda.

### Q2: Apakah Aspose.Note kompatibel dengan perpustakaan .NET lainnya?
   
A2: Aspose.Note terintegrasi secara mulus dengan perpustakaan .NET lainnya, menawarkan fleksibilitas luas dalam manipulasi dokumen.

### Q3: Apakah Aspose.Note mendukung ekspor tabel ke format berbeda?
   
A3: Tentu saja, Aspose.Note memungkinkan Anda mengekspor tabel ke berbagai format termasuk PDF, DOCX, dan HTML.

### Q4: Bisakah saya mengisi tabel secara dinamis dengan data dari sumber eksternal?
   
A4: Ya, Anda dapat mengisi tabel secara dinamis dengan mengambil data dari database, API, atau input pengguna.

### Q5: Apakah dukungan teknis tersedia untuk pengguna Aspose.Note?
   
A5: Ya, Aspose menyediakan dukungan teknis yang komprehensif melalui forum dan saluran dukungan khusus mereka.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
