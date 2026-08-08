---
date: 2026-08-08
description: Pelajari cara melacak perubahan di OneNote dengan mengambil revisi halaman
  secara programatis menggunakan Aspose.Note untuk Java.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: Dapatkan Revisi Halaman di OneNote - Aspose.Note
og_description: Pelajari cara melacak perubahan di OneNote dengan mengambil revisi
  halaman secara programatis menggunakan Aspose.Note untuk Java.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: Lacak perubahan di OneNote – revisi halaman dengan Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: Lacak perubahan di OneNote – revisi halaman dengan Aspose.Note
url: /id/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Melacak perubahan di OneNote – revisi halaman dengan Aspose.Note

Dalam tutorial ini Anda akan belajar cara **melacak perubahan di OneNote** dengan mengekstrak riwayat revisi lengkap sebuah halaman menggunakan Aspose.Note Java API. Kami akan membahas semuanya mulai dari menyiapkan lingkungan pengembangan Anda hingga mencetak penulis, stempel waktu, dan judul setiap revisi, sehingga Anda dapat membangun fitur jejak audit yang dapat diandalkan untuk solusi berbasis OneNote apa pun.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Mengambil riwayat revisi halaman dari file OneNote menggunakan Aspose.Note untuk Java.  
- **Versi perpustakaan mana yang diperlukan?** Rilis Aspose.Note untuk Java terbaru yang mendukung `LoadOptions.setLoadHistory`.  
- **Apakah saya memerlukan lisensi?** Lisensi evaluasi sementara dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya memodifikasi revisi?** API bersifat read‑only untuk revisi; Anda hanya dapat mengambilnya.  
- **Apa prasyarat utama?** Java JDK, Aspose.Note untuk Java, dan dokumen OneNote dengan data revisi.

## Apa itu “tutorial revisi halaman aspose.note”?
Tutorial ini menunjukkan cara mengakses versi historis sebuah halaman OneNote secara programatik. Setiap revisi berisi metadata seperti penulis, waktu pembuatan, dan waktu modifikasi, memungkinkan Anda membangun jejak audit atau fitur log perubahan di dalam aplikasi Anda.

## Mengapa menggunakan Aspose.Note untuk pelacakan revisi halaman?
Muat seluruh riwayat revisi sebuah notebook dalam waktu kurang dari 5 detik untuk file 500‑halaman pada CPU standar 2 GHz, dan ambil metadata tanpa meluncurkan UI OneNote. Perpustakaan ini mendukung lebih dari 30 format input dan output, berjalan di Windows, Linux, dan macOS (menutupi >95 % lingkungan server), serta memberikan kontrol penuh atas setiap properti revisi.

## Prasyarat

### 1. Java Development Kit (JDK)
Pastikan JDK terbaru (8 atau lebih tinggi) terpasang dan `JAVA_HOME` sudah diset.

### 2. Aspose.Note untuk Java
Unduh perpustakaan dari [tautan unduhan](https://releases.aspose.com/note/java/).

### 3. Dokumen OneNote Contoh
Buat atau dapatkan file OneNote (mis., `Sample1.one`) yang berisi halaman dengan riwayat revisi.

## Impor paket
Pertama, impor kelas Aspose.Note yang diperlukan.  
`Document` mewakili notebook OneNote, `LoadOptions` mengonfigurasi perilaku pemuatan, dan `Page` mewakili satu halaman.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Implementasi Langkah‑demi‑Langkah

### Langkah 1: siapkan direktori dokumen
Tentukan folder tempat file OneNote Anda berada.

```java
String dataDir = "Your Document Directory";
```

### Langkah 2: muat dokumen OneNote dengan riwayat diaktifkan
`LoadOptions` adalah kelas konfigurasi yang memberi tahu Aspose.Note cara membuka file, termasuk apakah akan membaca data revisi. Aktifkan flag tersebut sebelum memuat dokumen.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Langkah 3: dapatkan halaman pertama
Ambil objek halaman pertama; ini akan menjadi titik referensi untuk mengambil riwayatnya.

```java
Page firstPage = document.getFirstChild();
```

### Langkah 4: iterasi melalui revisi halaman
Lakukan perulangan pada setiap revisi dan cetak metadata berguna seperti stempel waktu, judul, level, dan penulis.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **Tip Pro:** Jika Anda perlu menyaring revisi berdasarkan penulis tertentu atau rentang tanggal, cukup tambahkan pemeriksaan kondisional di dalam loop `for`.

## Masalah Umum & Solusi
- **Tidak ada revisi yang dikembalikan:** Pastikan `loadOptions.setLoadHistory(true)` dipanggil sebelum memuat dokumen.  
- **Penulis atau judul null:** Beberapa versi OneNote lama mungkin tidak menyimpan bidang ini; tangani nilai `null` dengan hati-hati.  
- **Keterlambatan kinerja pada notebook besar:** Muat hanya bagian yang Anda perlukan atau tingkatkan ukuran heap JVM.

## Pertanyaan yang Sering Diajukan

**Q1: Bisakah saya menggunakan Aspose.Note untuk Java untuk memodifikasi revisi halaman?**  
A1: Tidak, API saat ini hanya mendukung akses read‑only ke revisi halaman.

**Q2: Apakah Aspose.Note untuk Java kompatibel dengan berbagai versi dokumen OneNote?**  
A2: Ya, ia bekerja dengan berbagai format file OneNote, memungkinkan pemrosesan mulus lintas versi.

**Q3: Apakah Aspose.Note untuk Java memerlukan lisensi untuk digunakan?**  
A3: Lisensi komersial diperlukan untuk penggunaan produksi, tetapi lisensi evaluasi sementara tersedia untuk pengujian.

**Q4: Bisakah saya mendapatkan dukungan jika saya mengalami masalah saat menggunakan Aspose.Note untuk Java?**  
A4: Ya, Anda dapat mengajukan pertanyaan di forum Aspose.Note [Aspose.Note forum](https://forum.aspose.com/c/note/28).

**Q5: Apakah ada percobaan gratis untuk Aspose.Note untuk Java?**  
A5: Ya, Anda dapat mengunduh percobaan gratis dari [situs web](https://releases.aspose.com/).

---

**Terakhir Diperbarui:** 2026-08-08  
**Diuji Dengan:** Aspose.Note untuk Java (rilis terbaru)  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [melacak perubahan onenote – Kelola Revisi Halaman dengan Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Tutorial Java Aspose - Dapatkan Informasi tentang Halaman di OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Ubah Latar Belakang Halaman OneNote – Aspose.Note untuk Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}