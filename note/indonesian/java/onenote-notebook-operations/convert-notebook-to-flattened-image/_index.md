---
date: 2025-12-25
description: Pelajari cara mengonversi OneNote ke PNG menggunakan Aspose.Note untuk
  Java. Panduan ini menunjukkan cara mengatur resolusi gambar, meratakan notebook,
  dan menyimpan OneNote sebagai gambar secara efisien.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Cara Mengonversi OneNote ke PNG – Mengubah Notebook menjadi Gambar dengan Aspose.Note
url: /id/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi Notebook menjadi Gambar Datar di OneNote - Aspose.Note

## Introduction

Dalam tutorial ini Anda akan menemukan cara **mengonversi OneNote ke PNG** dengan mengubah seluruh notebook menjadi satu gambar datar menggunakan Aspose.Note untuk Java. Pendekatan ini sempurna ketika Anda perlu membagikan notebook sebagai gambar statis, menyematkannya dalam laporan, atau mengarsipkannya tanpa kehilangan detail visual apa pun.

## Quick Answers
- **Apa arti “flatten notebook”?** Ini menggabungkan semua elemen halaman menjadi satu gambar raster.  
- **Format apa yang digunakan?** PNG adalah default, memberikan kualitas loss‑less.  
- **Bisakah saya mengubah DPI?** Ya, gunakan `setResolution` pada `ImageSaveOptions`.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi komersial diperlukan untuk produksi.  
- **Apakah ini didukung di semua OS?** API Java dapat berjalan di mana saja Java berjalan.

## What is converting OneNote to PNG?

Mengonversi OneNote ke PNG membuat representasi bitmap dari setiap halaman dalam notebook, mempertahankan teks, gambar, dan objek tersemat dalam satu file gambar. Ini sangat berguna untuk dokumentasi, presentasi, atau arsip kepatuhan.

## Why convert OneNote to PNG with Aspose.Note?

- **Fidelity penuh** – Semua elemen visual dipertahankan.  
- **Output satu file** – Tidak perlu mengelola banyak file halaman.  
- **Resolusi dapat disesuaikan** – Sesuaikan DPI untuk memenuhi persyaratan kualitas.  
- **Tanpa instalasi Office** – Berfungsi sepenuhnya independen dari Microsoft OneNote.

## Prerequisites

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1. Java Development Kit (JDK) terpasang di sistem Anda.  
2. Perpustakaan Aspose.Note untuk Java sudah diunduh dan disiapkan dalam proyek Java Anda. Anda dapat mengunduh perpustakaan dari [here](https://releases.aspose.com/note/java/).  
3. Pengetahuan dasar tentang pemrograman Java.

## Import Packages

Untuk memulai, Anda perlu mengimpor paket yang diperlukan dari Aspose.Note untuk Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Step 1: Set Up Document Directory

Pertama, tentukan direktori tempat file notebook Anda berada:

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan path ke file notebook Anda.

## Step 2: Load Notebook

Selanjutnya, muat file notebook menggunakan kelas `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Pastikan mengganti `"test.onetoc2"` dengan nama file notebook Anda.

## Step 3: Set Image Save Options

Sekarang, siapkan opsi untuk menyimpan notebook sebagai gambar. Kami akan menentukan format penyimpanan sebagai PNG dan mengatur resolusi menjadi 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Anda dapat menyesuaikan resolusi sesuai kebutuhan. Di sinilah Anda **set image resolution** untuk mengontrol kualitas output.

## Step 4: Flatten Notebook

Agar semua elemen menjadi datar menjadi satu gambar, atur opsi `flatten` ke `true`:

```java
saveOptions.setFlatten(true);
```

Menetapkan `flatten` ke `true` menjamin bahwa PNG yang dihasilkan mempertahankan tata letak notebook Anda secara tepat.

## Step 5: Save Image

Akhirnya, simpan notebook sebagai gambar yang telah diflatkan:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Ganti `"ExportImageasFlattenedNotebook_out.png"` dengan nama file output yang Anda inginkan. Langkah ini **saves OneNote as an image** yang dapat Anda bagikan atau sematkan di mana saja.

## Common Use Cases

- **Documentation:** Sematkan gambar notebook dalam manual teknis atau panduan pengguna.  
- **Presentations:** Gunakan slide PNG resolusi tinggi di PowerPoint tanpa khawatir tentang kompatibilitas font atau objek.  
- **Archiving:** Simpan snapshot read‑only notebook untuk audit kepatuhan.

## Troubleshooting Tips

- **File not found:** Periksa kembali path `dataDir` dan pastikan file `.onetoc2` ada.  
- **Low quality image:** Tingkatkan DPI dengan mengubah `documentSaveOptions.setResolution(600);`.  
- **Missing elements:** Pastikan `saveOptions.setFlatten(true);` diaktifkan; jika tidak, beberapa lapisan mungkin tetap terpisah.

## Frequently Asked Questions

**Q1: Can I adjust the resolution of the output image?**  
A1: Ya, Anda dapat menyesuaikan resolusi sesuai kebutuhan dengan memodifikasi parameter metode `setResolution`.

**Q2: Does Aspose.Note support other image formats for export?**  
A2: Ya, Aspose.Note mendukung berbagai format gambar seperti PNG, JPEG, BMP, dll., untuk mengekspor notebook.

**Q3: Can I customize the output image further?**  
A3: Ya, Aspose.Note menyediakan opsi yang luas untuk menyesuaikan gambar output, termasuk ukuran halaman, orientasi, dan pengaturan kualitas.

**Q4: Is there a trial version available for Aspose.Note for Java?**  
A4: Ya, Anda dapat memperoleh versi percobaan gratis dari [here](https://releases.aspose.com/).

**Q5: Where can I find support for Aspose.Note for Java?**  
A5: Anda dapat menemukan dukungan dan sumber daya di forum Aspose.Note [here](https://forum.aspose.com/c/note/28).

---

**Last Updated:** 2025-12-25  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}