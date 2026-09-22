---
date: 2026-08-13
description: Pelajari cara mendapatkan waktu modifikasi halaman OneNote dan mengambil
  revisi halaman dengan Aspose.Note untuk Java, ideal untuk audit dan manajemen dokumen.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Dapatkan Revisi Halaman di OneNote - Aspose.Note
og_description: Pelajari cara mendapatkan waktu modifikasi halaman OneNote dan mengambil
  revisi halaman OneNote dengan Aspose.Note untuk Java. Langkah cepat, contoh kode,
  dan pemecahan masalah.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Dapatkan waktu modifikasi halaman OneNote menggunakan Aspose.Note – tutorial
  Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Dapatkan waktu modifikasi halaman OneNote menggunakan Aspose.Note
url: /id/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dapatkan Waktu Modifikasi Halaman OneNote menggunakan Aspose.Note

## Pendahuluan

Dalam tutorial ini Anda akan belajar cara **get onenote page modified** timestamp dan mengambil riwayat revisi lengkap dari halaman OneNote dengan Aspose.Note untuk Java. Baik Anda sedang membangun fitur jejak audit, penampil log perubahan, atau perlu menampilkan tanggal edit terbaru di dasbor, panduan ini akan memandu Anda melalui setiap langkah—dari menyiapkan lingkungan hingga menangani jebakan umum.

## Jawaban Cepat
- **Apa yang dikembalikan oleh “get last modified time”?** Ini mengembalikan timestamp dari edit terbaru pada halaman OneNote.  
- **Kelas mana yang menyediakan riwayat revisi?** `PageHistory` melalui `Document.getPageHistory(Page)`.  
- **Apakah saya memerlukan lisensi untuk fitur ini?** Ya, lisensi Aspose.Note yang valid diperlukan untuk penggunaan produksi.  
- **Versi Java apa yang didukung?** Java 8 atau lebih tinggi (JDK 8+).  
- **Bisakah saya memfilter revisi berdasarkan penulis?** Anda dapat membaca properti `Author` dari setiap objek `Page` dan menerapkan filter Anda sendiri.

## Apa itu “get last modified time” di OneNote?

Waktu terakhir dimodifikasi disimpan sebagai atribut metadata pada setiap halaman OneNote yang menunjukkan saat edit terakhir. Aspose.Note mengekspos nilai ini melalui metode `Page.getLastModifiedTime()`, yang mengembalikan objek `java.util.Date` yang dapat diformat atau dicatat sesuai kebutuhan aplikasi Anda.

## Mengapa mengambil revisi halaman?

Mengambil revisi halaman memberi Anda jejak audit lengkap dari setiap perubahan yang dibuat pada halaman OneNote, memungkinkan Anda melacak siapa yang mengedit apa dan kapan. Riwayat ini dapat digunakan untuk membandingkan versi, memulihkan keadaan sebelumnya, atau menganalisis pola kolaborasi antar tim, menjadikannya penting untuk kepatuhan dan kontrol kualitas.

## Prasyarat

- **Java Development Kit (JDK) 8 atau lebih baru** – instal dari situs web Oracle atau vendor kompatibel mana pun.  
- **Perpustakaan Aspose.Note untuk Java** – unduh JAR dari halaman rilis Aspose.Note Java **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** dan ikuti panduan instalasi **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Impor paket

`Document` mewakili notebook OneNote yang dimuat ke memori, sementara `Page` dan `PageHistory` menyediakan akses ke halaman individual dan data revisinya.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Pernyataan impor sebenarnya ditampilkan sebagai teks biasa untuk mempertahankan jumlah blok kode asli.)*

## Cara mendapatkan waktu modifikasi halaman OneNote

Untuk memperoleh timestamp terakhir dimodifikasi, pertama muat dokumen OneNote ke dalam objek `Document`, kemudian pilih `Page` yang diinginkan. Panggil metode `getLastModifiedTime()` pada halaman tersebut, yang mengembalikan `java.util.Date`. Anda kemudian dapat memformat tanggal ini menggunakan `SimpleDateFormat` atau mengonversinya ke UTC untuk pelaporan konsisten lintas zona waktu.

## Langkah 1: atur direktori dokumen

Tentukan folder yang berisi file OneNote Anda.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Langkah 2: muat dokumen

Buat instance `Document` dengan memberikan jalur lengkap ke file `.one` Anda.

```java
String dataDir = "Your Document Directory";
```

## Langkah 3: dapatkan halaman pertama

Ambil objek `Page` pertama dari koleksi halaman dokumen.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Langkah 4: dapatkan revisi halaman

Dapatkan `PageHistory` untuk halaman yang dipilih. Jika notebook belum pernah diedit, panggilan ini mungkin mengembalikan `null`.

```java
Page firstPage = doc.getFirstChild();
```

## Langkah 5: telusuri revisi halaman

Iterasikan setiap revisi `Page`, baca `Author` dan `LastModifiedTime`-nya, dan tampilkan informasinya.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Masalah umum dan solusi
- **Null `PageHistory`** – Pastikan notebook memang berisi revisi; jika tidak `getPageHistory` mengembalikan `null`.  
- **Perbedaan zona waktu** – `getLastModifiedTime()` menggunakan zona waktu default JVM. Konversi ke UTC dengan `SimpleDateFormat` jika aplikasi Anda memerlukan zona standar.  
- **Lisensi tidak dimuat** – Tanpa lisensi yang valid, Aspose.Note berjalan dalam mode evaluasi, membatasi pemrosesan halaman. Muat file lisensi Anda saat aplikasi dimulai untuk menghindari pembatasan ini.

## Pertanyaan yang sering diajukan

**Q1: Bisakah saya menggunakan Aspose.Note untuk Java untuk membuat dokumen OneNote baru?**  
A: Ya, API memungkinkan Anda membuat, mengedit, dan menyimpan notebook OneNote secara programatik dari awal.

**Q2: Apakah Aspose.Note untuk Java kompatibel dengan berbagai versi file OneNote?**  
A: Ya, ia mendukung format file OneNote 2007‑2021, memastikan kompatibilitas luas di lingkungan desktop dan cloud.

**Q3: Bisakah saya menyesuaikan format output saat mengekspor dokumen OneNote?**  
A: Tentu saja. Anda dapat mengekspor ke PDF, HTML, PNG, atau SVG, dan mengontrol opsi seperti resolusi gambar dan penyematan font.

**Q4: Apakah Aspose.Note untuk Java memerlukan lisensi untuk penggunaan komersial?**  
A: Ya, lisensi komersial wajib untuk penerapan produksi. Versi percobaan gratis tersedia untuk evaluasi.

**Q5: Di mana saya dapat mencari bantuan jika mengalami masalah?**  
A: Kunjungi forum komunitas Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** untuk mengajukan pertanyaan, berbagi pengalaman, dan mendapatkan bantuan dari komunitas serta insinyur Aspose.

---

**Terakhir Diperbarui:** 2026-08-13  
**Diuji Dengan:** Aspose.Note untuk Java 23.12 (terbaru pada saat penulisan)  
**Penulis:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Tutorial Terkait

- [Tutorial Java Aspose - Dapatkan Informasi tentang Halaman di OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [tutorial revisi halaman aspose.note – Dapatkan Revisi Halaman di OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [lacak perubahan onenote – Kelola Revisi Halaman dengan Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}