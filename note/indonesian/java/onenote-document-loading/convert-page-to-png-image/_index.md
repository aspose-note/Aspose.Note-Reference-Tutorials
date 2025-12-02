---
date: 2025-11-29
description: Pelajari cara mengekspor halaman OneNote ke PNG menggunakan Aspose.Note
  untuk Java. Ikuti petunjuk langkah demi langkah untuk mengatur indeks halaman, mengonversi
  halaman, dan menyimpan gambar.
language: id
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Ekspor Halaman OneNote ke Gambar PNG dalam Java menggunakan Aspose.Note
url: /java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengekspor Halaman OneNote ke Gambar PNG dalam Java menggunakan Aspose.Note

## Introduction

Dalam tutorial ini Anda akan menemukan **cara mengekspor halaman OneNote** ke gambar PNG menggunakan pustaka Aspose.Note untuk Java. Kami akan membahas semua yang Anda perlukan—dari menyiapkan lingkungan hingga mengatur indeks halaman dan akhirnya menyimpan halaman sebagai file PNG berkualitas tinggi. Pada akhir tutorial, Anda dapat menambahkan kemampuan ini ke aplikasi Java apa pun yang bekerja dengan dokumen OneNote.

## Quick Answers
- **Perpustakaan apa yang dibutuhkan?** Aspose.Note for Java.  
- **Bisakah saya mengekspor satu halaman?** Ya—gunakan `setPageIndex` untuk menargetkan halaman yang tepat.  
- **Format gambar yang didukung?** PNG, JPEG, GIF, BMP, TIFF (PNG ditampilkan di sini).  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis tersedia; lisensi diperlukan untuk produksi.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk konversi dasar.

## What is “export OneNote page”?
Mengekspor halaman OneNote berarti mengonversi halaman tertentu dalam dokumen `.one` menjadi file gambar mandiri (PNG dalam kasus ini). Ini berguna ketika Anda perlu berbagi, menyematkan, atau memproses konten OneNote di luar lingkungan OneNote.

## Why use Aspose.Note for Java to convert OneNote to PNG?
- **Tanpa ketergantungan Microsoft Office** – bekerja di platform apa pun yang menjalankan Java.  
- **Kontrol detail** – Anda dapat memilih halaman mana saja melalui `setPageIndex`.  
- **Output berkualitas tinggi** – PNG mempertahankan grafik vektor dan kejernihan teks.  
- **Siap untuk batch** – mudah melakukan loop melalui halaman untuk konversi massal.

## Prerequisites

Before you start, make sure you have:

1. **Java Development Kit (JDK)** – versi 8 atau lebih tinggi.  
2. **Aspose.Note untuk Java** – unduh JAR terbaru dari [situs Aspose](https://releases.aspose.com/note/java/).  
3. **Dokumen OneNote** (`.one`) yang berisi halaman yang ingin Anda ekspor.

## Import Packages

First, import the necessary Java classes:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

### Step 1: Load the OneNote Document

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

Kami menggunakan kelas `Document` untuk membaca file OneNote dari disk. Objek `LoadOptions` memungkinkan Anda menyesuaikan perilaku pemuatan jika diperlukan.

### Step 2: Initialize ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` memberi tahu Aspose.Note bahwa kami menginginkan output dalam format **PNG**. Anda dapat beralih ke JPEG, BMP, dll., dengan mengubah `SaveFormat`.

### Step 3: Set the Page Index (How to convert OneNote page)

```java
// set page index
opts.setPageIndex(0);
```

Metode `setPageIndex` memilih halaman mana yang akan diekspor. Penomoran halaman dimulai dari **0**, sehingga `0` merujuk ke halaman pertama. Sesuaikan nilai ini untuk mengekspor halaman lain.

### Step 4: Save the Document as PNG (Save OneNote as PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Memanggil `save` menulis halaman yang dipilih ke file PNG di disk. Nama file `ConvertSpecificPageToPngImage_out.png` hanya contoh—Anda dapat menamainya sesuka hati.

## Common Issues & Tips

- **Indeks halaman tidak tepat** – Ingat bahwa indeks dimulai dari 0. Jika Anda mendapatkan gambar kosong, periksa nilai indeksnya.  
- **JAR Aspose.Note tidak ditemukan** – Pastikan JAR berada di classpath Anda; jika tidak, Anda akan melihat `ClassNotFoundException`.  
- **Halaman besar** – Untuk halaman yang sangat besar, pertimbangkan meningkatkan ukuran heap JVM (`-Xmx`) untuk menghindari `OutOfMemoryError`.

## Frequently Asked Questions

### Q1: Can I convert multiple pages to PNG images in one go using Aspose.Note for Java?
A1: Ya, Anda dapat melakukan loop melalui halaman dokumen, memperbarui `opts.setPageIndex(i)`, dan memanggil `save` untuk setiap iterasi.

### Q2: Does Aspose.Note for Java support other image formats besides PNG?
A2: Tentu saja. Anda dapat mengatur `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp`, atau `SaveFormat.Tiff` dalam `ImageSaveOptions`.

### Q3: Is there a free trial available for Aspose.Note for Java?
A3: Ya, Anda dapat mengunduh versi percobaan gratis dari [situs web](https://releases.aspose.com/).

### Q4: Can I get technical assistance if I encounter any issues with Aspose.Note for Java?
A4: Tentu saja, Anda dapat mencari dukungan di forum komunitas Aspose [di sini](https://forum.aspose.com/c/note/28).

### Q5: Where can I purchase a license for Aspose.Note for Java?
A5: Anda dapat membeli lisensi dari [halaman pembelian](https://purchase.aspose.com/buy).

### Q6: How do I export a page that contains embedded images?
A6: Gambar yang disematkan secara otomatis dirender dalam output PNG; tidak diperlukan kode tambahan.

### Q7: Can I set the DPI or image resolution?
A7: Ya, gunakan `opts.setResolution(int dpi)` sebelum memanggil `save` untuk mengontrol kualitas output.

---

**Terakhir Diperbarui:** 2025-11-29  
**Diuji Dengan:** Aspose.Note for Java 24.11 (latest)  
**Penulis:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
