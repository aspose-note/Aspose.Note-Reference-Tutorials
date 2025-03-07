---
title: Buat Dokumen dengan Root dan Sub-Halaman menggunakan Aspose.Note
linktitle: Buat Dokumen dengan Root dan Sub-Halaman menggunakan Aspose.Note
second_title: Aspose.Catatan .NET API
description: Pelajari cara menggunakan Aspose.Note untuk .NET untuk membuat dokumen OneNote dinamis dengan struktur hierarki.
weight: 11
url: /id/net/note-manipulation/create-documents-root-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat Dokumen dengan Root dan Sub-Halaman menggunakan Aspose.Note

## Perkenalan

Selamat datang di tutorial kami tentang membuat dokumen dengan root dan subhalaman menggunakan Aspose.Note untuk .NET! Aspose.Note adalah perpustakaan canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram, memungkinkan pembuatan, manipulasi, dan konversi dokumen OneNote.

Dalam tutorial ini, kami akan memandu Anda melalui proses pembuatan dokumen OneNote dengan akar dan subhalaman langkah demi langkah. Kami akan memberikan penjelasan mendetail dan cuplikan kode menggunakan Aspose.Note untuk .NET, sehingga memudahkan Anda untuk mengikuti dan menerapkannya dalam proyek Anda sendiri.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Visual Studio: Anda perlu menginstal Visual Studio di sistem Anda untuk menulis dan mengkompilasi kode .NET.
2.  Aspose.Note untuk .NET: Unduh dan instal Aspose.Note untuk .NET dari[Unduh Halaman](https://releases.aspose.com/note/net/).
3. Pengetahuan Dasar C#: Keakraban dengan bahasa pemrograman C# diperlukan untuk memahami dan mengimplementasikan contoh kode.

Sekarang setelah semuanya siap, mari selami tutorialnya!

## Impor Namespace

Pertama, mari impor namespace yang diperlukan ke dalam proyek kita:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## Langkah 1: Inisialisasi Objek Dokumen

```csharp
//Buat objek kelas Dokumen
Document doc = new Document();
```

## Langkah 2: Buat Halaman Root dan Sub-Halaman

```csharp
// Inisialisasi objek kelas Halaman dan atur levelnya
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### Untuk Halaman 1:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### Untuk Halaman 2:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### Untuk Halaman 3:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## Langkah 4: Tambahkan Halaman ke Dokumen

```csharp
// Tambahkan halaman ke Dokumen OneNote
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## Langkah 5: Simpan Dokumen

```csharp
// Simpan dokumen OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara membuat dokumen dengan root dan subhalaman menggunakan Aspose.Note untuk .NET. Sekarang Anda dapat memanfaatkan pengetahuan ini untuk secara dinamis menghasilkan dokumen OneNote yang kompleks di aplikasi Anda.

## FAQ

### Q1: Bisakah Aspose.Note menangani dokumen OneNote berukuran besar?

A1: Ya, Aspose.Note dirancang untuk menangani dokumen OneNote berukuran besar secara efisien tanpa mengurangi performa.

### Q2: Apakah Aspose.Note kompatibel dengan .NET Core?

A2: Ya, Aspose.Note mendukung .NET Core bersama dengan .NET Framework tradisional.

### Q3: Bisakah saya mengonversi dokumen OneNote ke format lain menggunakan Aspose.Note?

A3: Tentu saja, Aspose.Note menyediakan kemampuan konversi ke berbagai format termasuk PDF, DOCX, HTML, dan lainnya.

### Q4: Apakah Aspose.Note menawarkan integrasi cloud?

A4: Aspose.Note terutama berfokus pada pengembangan lokal, namun Anda dapat menggunakannya dalam lingkungan cloud dengan pengaturan yang tepat.

### Q5: Apakah dukungan teknis tersedia untuk Aspose.Note?

A5: Ya, Aspose menyediakan dukungan teknis khusus melalui forum mereka di mana Anda dapat mengajukan pertanyaan dan mendapatkan bantuan.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
