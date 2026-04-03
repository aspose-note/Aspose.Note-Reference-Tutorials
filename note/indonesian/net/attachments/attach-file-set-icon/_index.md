---
date: 2026-04-03
description: Pelajari cara mengatur ikon khusus dan melampirkan file di Aspose.Note
  untuk .NET, termasuk menyimpan file OneNote dan menggunakan gambar sebagai ikon.
keywords:
- set custom icon
- attach multiple files
- use image as icon
- save onenote file
- embed text file
linktitle: Lampirkan File dan Atur Ikon di Aspose.Note
second_title: Aspose.Note .NET API
title: Atur Ikon Kustom dan Lampirkan File di Aspose.Note
url: /id/net/attachments/attach-file-set-icon/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Ikon Kustom dan Lampirkan File di Aspose.Note

## Pendahuluan

Jika Anda perlu **set custom icon** untuk lampiran di halaman OneNote, Aspose.Note untuk .NET mempermudah prosesnya. Dengan melampirkan file dan menetapkan gambar sebagai ikonnya, Anda dapat membuat catatan yang lebih kaya dan informatif yang tampil persis seperti yang Anda inginkan. Dalam tutorial ini kami akan membahas proses lengkap—dimulai dari dokumen baru, menambahkan lampiran, menerapkan ikon JPEG kustom, dan akhirnya menyimpan file OneNote.

## Jawaban Cepat
- **What does “set custom icon” mean?** Ini memungkinkan Anda mengganti thumbnail lampiran default dengan gambar yang Anda sediakan.  
- **Can I attach multiple files?** Ya, ulangi langkah lampiran untuk setiap file.  
- **Which image formats are supported for icons?** Format gambar apa yang didukung untuk ikon? Format apa pun yang kompatibel dengan .NET seperti JPEG, PNG, BMP, atau GIF.  
- **Do I need a license?** Apakah saya memerlukan lisensi? Lisensi Aspose.Note yang valid diperlukan untuk penggunaan produksi; percobaan gratis dapat digunakan untuk evaluasi.  
- **How do I save the OneNote file?** Bagaimana cara menyimpan file OneNote? Gunakan `Document.Save()` dan tentukan jalur file *.one*.

## Apa itu “set custom icon” di Aspose.Note?
Menetapkan ikon kustom berarti memberikan gambar tertentu (mis., JPEG) untuk mewakili file yang dilampirkan dalam halaman OneNote. Hal ini meningkatkan petunjuk visual bagi pengguna dan dapat digunakan untuk menampilkan logo tipe file atau gambar merek.

## Mengapa mengatur ikon kustom untuk lampiran?
- **Better visual context:** Pengguna langsung mengenali tipe atau tujuan file yang dilampirkan.  
- **Brand consistency:** Gunakan logo perusahaan Anda sebagai ikon untuk semua dokumen terkait.  
- **Enhanced UX:** Membuat catatan tampak rapi dan profesional, terutama dalam notebook yang dibagikan.

## Prasyarat

- Pengetahuan dasar pemrograman C#.
- Aspose.Note for .NET library terinstal.
- Visual Studio (atau IDE kompatibel .NET lainnya) siap untuk pengembangan.

## Impor Namespace

Pertama, masukkan namespace yang diperlukan ke dalam ruang lingkup sehingga Anda dapat bekerja dengan file, gambar, dan objek OneNote.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing.Imaging;
```

## Panduan Langkah‑per‑Langkah untuk Melampirkan File dan Mengatur Ikonnya

### Langkah 1: Buat Objek Document
Instansi `Document` baru mewakili file OneNote yang akan Anda buat.

```csharp
Document doc = new Document();
```

### Langkah 2: Inisialisasi Objek Page
Setiap file OneNote berisi satu atau lebih halaman. Di sini kami membuat halaman pertama.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Langkah 3: Inisialisasi Objek Outline
Outline berfungsi sebagai wadah untuk blok konten pada sebuah halaman.

```csharp
Outline outline = new Outline(doc);
```

### Langkah 4: Inisialisasi Objek OutlineElement
Elemen ini akan menampung file yang dilampirkan dan ikonnya yang kustom.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

### Langkah 5: Baca Gambar Ikon dan Inisialisasi Objek AttachedFile
Kami membuka aliran gambar (ikon kustom) dan menunjuk ke file yang ingin kami sematkan.

```csharp
string dataDir = "Your Document Directory";
using (var stream = File.OpenRead(dataDir + "icon.jpg"))
{
    AttachedFile attachedFile = new AttachedFile(doc, dataDir + "attachment.txt", stream, ImageFormat.Jpeg);
}
```

> **Pro tip:** Ganti `ImageFormat.Jpeg` dengan `ImageFormat.Png` jika Anda lebih suka ikon PNG.

### Langkah 6: Tambahkan File yang Dilampirkan ke OutlineElement
Sekarang file (dengan ikonnya) menjadi anak dari elemen outline.

```csharp
outlineElem.AppendChildLast(attachedFile);
```

### Langkah 7: Tambahkan OutlineElement ke Outline
Ini menempatkan elemen di dalam wadah outline.

```csharp
outline.AppendChildLast(outlineElem);
```

### Langkah 8: Tambahkan Outline ke Page
Lampirkan seluruh hierarki outline ke halaman.

```csharp
page.AppendChildLast(outline);
```

### Langkah 9: Tambahkan Page ke Document
Tambahkan halaman yang selesai ke struktur dokumen.

```csharp
doc.AppendChildLast(page);
```

### Langkah 10: Simpan Dokumen OneNote
Akhirnya, tulis dokumen ke disk sebagai file *.one*.

```csharp
dataDir = dataDir + "AttachFileAndSetIcon_out.one";
doc.Save(dataDir);
```

## Kasus Penggunaan Umum
- **Embedding contracts:** Lampirkan PDF dan gunakan ikon logo kontrak.  
- **Sharing code snippets:** Lampirkan file `.txt` dengan ikon “code” kustom.  
- **Project documentation:** Lampirkan file desain dan atur thumbnail yang sesuai dengan tipe file.

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **Icon not showing** | Verifikasi format gambar cocok dengan `ImageFormat` yang Anda berikan (mis., JPEG vs PNG). |
| **File path errors** | Gunakan `Path.Combine(dataDir, \"file.ext\")` untuk menghindari masalah slash yang hilang. |
| **Large attachments cause performance lag** | Kompres file terlebih dahulu atau bagi menjadi beberapa lampiran yang lebih kecil. |

## Pertanyaan yang Sering Diajukan

**Q:** Apakah saya dapat melampirkan beberapa file ke satu catatan menggunakan Aspose.Note untuk .NET?  
**A:** Ya. Cukup ulangi blok “Read the Icon Image and Initialize the AttachedFile Object” untuk setiap file dan tambahkan setiap `AttachedFile` ke `OutlineElement` yang sama atau buat elemen terpisah.

**Q:** Apakah memungkinkan untuk mengatur ikon kustom untuk lampiran file?  
**A:** Tentu saja. Konstruktor `AttachedFile` memungkinkan Anda memberikan aliran gambar dan menentukan format gambar, memberi Anda kontrol penuh atas ikon.

**Q:** Apakah Aspose.Note mendukung format gambar lain untuk mengatur ikon?  
**A:** Ya. Selain JPEG, Anda dapat menggunakan PNG, BMP, GIF, atau format apa pun yang didukung oleh `System.Drawing.Imaging.ImageFormat`.

**Q:** Apakah saya dapat melampirkan file dari URL eksternal?  
**A:** Meskipun Aspose.Note bekerja dengan aliran lokal, Anda dapat mengunduh file melalui `HttpClient`, menyimpannya dalam `MemoryStream`, dan kemudian memberikan aliran tersebut ke `AttachedFile`.

**Q:** Apakah ada batas ukuran untuk lampiran file?  
**A:** Aspose.Note sendiri tidak menetapkan batas keras, tetapi file yang sangat besar dapat memengaruhi penggunaan memori dan kinerja. Pertimbangkan untuk mengompres lampiran besar.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.Note 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}