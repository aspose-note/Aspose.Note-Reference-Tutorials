---
date: 2026-03-19
description: Pelajari cara menambahkan gambar ke OneNote menggunakan Aspose.Note untuk
  Java. Panduan langkah demi langkah ini menunjukkan cara membuat dokumen OneNote,
  menyisipkan gambar ke OneNote, dan menyimpan OneNote sebagai PDF.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Cara menambahkan gambar ke OneNote menggunakan Java – Membuat Dokumen dan Menyisipkan
  Gambar
url: /id/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menambahkan gambar ke OneNote menggunakan Java – Membuat Dokumen dan Menyisipkan Gambar

## Introduction

Pada tutorial ini, Anda akan belajar **cara menambahkan gambar ke OneNote** menggunakan Aspose.Note Java API. Kami akan memandu Anda membuat dokumen OneNote dari awal, menyisipkan gambar, dan menyimpan hasilnya sebagai PDF. Baik Anda sedang membangun alat pelaporan, mengotomatisasi pencatatan, atau hanya perlu menyematkan grafik secara programatis, panduan ini memberikan jalur yang jelas dan praktis.

## Quick Answers
- **Perpustakaan apa yang saya perlukan?** Aspose.Note for Java.  
- **Apakah saya dapat menyisipkan format gambar apa pun?** JPEG, PNG, BMP, GIF and more are supported.  
- **Format output apa yang tersedia?** You can save as OneNote, PDF, XPS, HTML, etc.  
- **Apakah saya memerlukan lisensi untuk produksi?** Yes, a commercial license is required for non‑trial use.  
- **Apakah kode ini lintas‑platform?** Absolutely – Java runs on Windows, Linux, and macOS.

## Cara menambahkan gambar ke OneNote menggunakan Java

Menambahkan gambar ke OneNote berarti secara programatis menyematkan file gambar ke dalam halaman OneNote sehingga muncul bersama teks, outline, atau elemen lainnya. Aspose.Note API mengabstraksi format file OneNote, memungkinkan Anda fokus pada konten daripada struktur XML yang mendasarinya.

### Why embed image in OneNote?

- **Otomatisasi:** Menghasilkan notulen rapat dengan screenshot secara otomatis.  
- **Konsistensi:** Memastikan setiap halaman mengikuti tata letak dan branding yang sama.  
- **Integrasi:** Menggabungkan data dari sistem lain (mis., grafik) langsung ke dalam notebook OneNote.  
- **Lintas‑platform:** Java memungkinkan Anda menjalankan kode yang sama di server atau lingkungan desktop mana pun.

## Prerequisites

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1. **Java Development Kit (JDK)** – versi terbaru apa pun (8 atau lebih tinggi).  
2. **Aspose.Note for Java library** – unduh dari [website](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau editor kompatibel Java lain yang Anda sukai.  

## Import Packages

Mulailah dengan mengimpor kelas yang diperlukan dalam file sumber Java Anda:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

### Langkah 1: Siapkan Dokumen

Buat dokumen OneNote baru dan sebuah kontainer halaman tempat konten akan ditempatkan.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Langkah 2: Inisialisasi Outline

*Outline* berfungsi sebagai kontainer untuk elemen seperti teks dan gambar. Kami mengatur offset-nya ke nol sehingga konten mulai dari pojok kiri‑atas.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Langkah 3: Muat dan Atur Gambar

Muat gambar yang ingin Anda sematkan dan atur ke sisi kanan halaman. Di sinilah kita sebenarnya **menambahkan gambar ke OneNote**. Konstruktor `Image` menunjukkan cara **memuat file gambar java** secara kode.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Langkah 4: Lampirkan Gambar ke Elemen Outline

Bungkus gambar di dalam `OutlineElement`. Langkah ini menghubungkan objek visual ke hierarki outline dokumen dan secara efektif **menyisipkan gambar ke OneNote**.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Langkah 5: Susun Struktur Dokumen

Tambahkan elemen outline ke outline, kemudian lampirkan outline ke halaman, dan akhirnya tambahkan halaman ke dokumen.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Langkah 6: Simpan Dokumen OneNote

Simpan dokumen ke disk. Dalam contoh ini kami mengekspor ke PDF, yang menunjukkan cara **menyimpan OneNote sebagai PDF** atau **mengonversi OneNote ke PDF**. Anda juga dapat menyimpan sebagai file OneNote asli (`.one`) dengan mengubah `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Common Issues and Solutions

| Masalah | Mengapa Terjadi | Solusi |
|-------|----------------|-----|
| **Gambar tidak muncul** | Path file salah atau format tidak didukung. | Pastikan `dataDir` mengarah ke folder yang benar dan gunakan tipe gambar yang didukung (JPEG, PNG, dll.). |
| **Dokumen disimpan sebagai PDF kosong** | Offset outline diatur secara tidak tepat. | Pastikan `setVerticalOffset(0)` dan `setHorizontalOffset(0)` dipanggil, atau sesuaikan offset untuk menempatkan konten dalam batas halaman. |
| **IOException saat menyimpan** | Folder tujuan tidak ada atau tidak memiliki izin menulis. | Buat folder tersebut terlebih dahulu atau jalankan program dengan izin yang sesuai. |

## Frequently Asked Questions

**Q1: Di mana saya dapat menemukan dokumentasi untuk Aspose.Note for Java?**  
A1: Anda dapat mengakses dokumentasi [di sini](https://reference.aspose.com/note/java/).

**Q2: Bagaimana cara mengunduh Aspose.Note for Java?**  
A2: Anda dapat mengunduh Aspose.Note for Java dari [halaman unduhan](https://releases.aspose.com/note/java/).

**Q3: Apakah tersedia trial gratis untuk Aspose.Note for Java?**  
A3: Ya, Anda dapat mendapatkan trial gratis dari [website](https://releases.aspose.com/).

**Q4: Di mana saya dapat mendapatkan dukungan untuk Aspose.Note for Java?**  
A4: Untuk dukungan, kunjungi [forum Aspose.Note](https://forum.aspose.com/c/note/28).

**Q5: Apakah saya dapat memperoleh lisensi sementara untuk Aspose.Note for Java?**  
A5: Ya, Anda dapat meminta lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

**Q6: Apakah saya dapat menggunakan kode ini untuk **menyimpan OneNote sebagai PDF** di server Linux?**  
A6: Tentu saja. Library Aspose.Note bersifat platform‑independen, sehingga kode yang sama bekerja di Windows, Linux, dan macOS.

**Q7: Apakah API mendukung **menyematkan gambar di OneNote** dengan PNG transparan?**  
A7: Ya, file PNG dengan saluran alfa sepenuhnya didukung dan mempertahankan transparansi saat disisipkan.

---

**Terakhir Diperbarui:** 2026-03-19  
**Diuji Dengan:** Aspose.Note for Java 24.12 (latest)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}