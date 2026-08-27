---
date: 2026-01-10
description: Pelajari cara mendapatkan waktu terakhir diubah dan mengambil revisi
  halaman OneNote menggunakan Aspose.Note untuk Java. Integrasikan ini ke dalam aplikasi
  Java Anda untuk manajemen dokumen yang efisien.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Cara Mendapatkan Waktu Modifikasi Terakhir Halaman OneNote – Aspose.Note
url: /id/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mendapatkan Revisi Halaman di OneNote - Aspose.Note

## Pendahuluan

Dalam tutorial ini, Anda akan **mendapatkan waktu terakhir dimodifikasi** untuk halaman di dalam dokumen OneNote dan mengeksplorasi cara mengambil riwayat revisi lengkap menggunakan Aspose.Note untuk Java. Baik Anda sedang membangun sistem manajemen dokumen, melakukan audit perubahan, atau sekadar perlu menampilkan kapan halaman terakhir diedit, panduan ini menunjukkan secara tepat cara mengekstrak informasi tersebut secara programatis.

## Jawaban Cepat
- **Apa yang dikembalikan oleh “get last modified time”?** Stempel waktu dari edit terbaru pada halaman OneNote.  
- **Kelas mana yang menyediakan riwayat revisi?** `PageHistory` melalui `Document.getPageHistory(Page)`.  
- **Apakah saya memerlukan lisensi untuk fitur ini?** Ya, lisensi Aspose.Note yang valid diperlukan untuk penggunaan produksi.  
- **Versi Java apa yang didukung?** Java 8 atau lebih tinggi (JDK 8+).  
- **Bisakah saya memfilter revisi berdasarkan penulis?** Anda dapat membaca properti `Author` dari setiap objek `Page` dan menerapkan filter Anda sendiri.

## Apa itu “get last modified time” di OneNote?

**Waktu terakhir dimodifikasi** adalah bidang metadata yang disimpan bersama setiap halaman yang mencatat kapan halaman terakhir kali diubah. Aspose.Note menampilkan nilai ini melalui metode `Page.getLastModifiedTime()`, memudahkan penampilan atau pencatatan tanggal perubahan.

## Mengapa mengambil revisi halaman?

- **Jejak audit:** Menyimpan catatan siapa yang mengubah apa dan kapan.  
- **Perbandingan versi:** Membuat fitur yang membandingkan dua revisi berdampingan.  
- **Wawasan kolaborasi pengguna:** Memahami pola penyuntingan dalam notebook yang dibagikan.  

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki hal berikut:

### Java Development Kit (JDK) Terpasang
Instal JDK 8 atau yang lebih baru dari situs web Oracle atau manajer paket pilihan Anda.

### Perpustakaan Aspose.Note untuk Java
Unduh perpustakaan dari situs resmi. Anda dapat menemukan tautan unduhan **[here](https://releases.aspose.com/note/java/)**. Ikuti petunjuk instalasi dalam dokumentasi **[here](https://reference.aspose.com/note/java/)**.

## Impor Paket

Untuk memulai, impor paket-paket yang diperlukan ke dalam proyek Java Anda. Paket-paket ini akan memungkinkan Anda memanfaatkan fungsionalitas yang disediakan oleh Aspose.Note untuk Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Sekarang, mari kita uraikan contoh kode yang disediakan menjadi beberapa langkah untuk memahami setiap komponen dan fungsinya.

## Cara Mendapatkan Waktu Terakhir Dimodifikasi dari Halaman OneNote

### Langkah 1: Atur Direktori Dokumen
Tentukan direktori tempat dokumen OneNote Anda berada.

```java
String dataDir = "Your Document Directory";
```

### Langkah 2: Muat Dokumen
Muat dokumen OneNote ke dalam Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Langkah 3: Dapatkan Halaman Pertama
Ambil halaman pertama dari dokumen.

```java
Page firstPage = doc.getFirstChild();
```

### Langkah 4: Dapatkan Revisi Halaman
Dapatkan riwayat revisi halaman.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Langkah 5: Telusuri Revisi Halaman
Iterasi melalui daftar revisi halaman dan ambil informasi relevan, termasuk **waktu terakhir dimodifikasi**.

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

## Masalah Umum dan Solusinya
- **`PageHistory` null:** Pastikan dokumen memang berisi revisi; jika tidak, `getPageHistory` dapat mengembalikan `null`.  
- **Perbedaan zona waktu:** `getLastModifiedTime()` mengembalikan `java.util.Date` dalam zona waktu default sistem. Konversi ke UTC jika diperlukan.  
- **Lisensi tidak dimuat:** Tanpa lisensi yang valid, Aspose.Note dapat beroperasi dalam mode evaluasi, membatasi jumlah halaman yang diproses.

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.Note untuk Java untuk membuat dokumen OneNote baru?
A1: Ya, Aspose.Note untuk Java menyediakan dukungan lengkap untuk membuat, membaca, dan memanipulasi dokumen OneNote secara programatis.

### Q2: Apakah Aspose.Note untuk Java kompatibel dengan berbagai versi file OneNote?
A2: Ya, Aspose.Note untuk Java mendukung berbagai versi file Microsoft OneNote, memastikan kompatibilitas di berbagai lingkungan.

### Q3: Bisakah saya menyesuaikan format output saat mengekspor dokumen OneNote?
A3: Tentu saja, Aspose.Note untuk Java menawarkan fleksibilitas dalam mengekspor dokumen OneNote ke berbagai format seperti PDF, HTML, dan gambar, dengan opsi penyesuaian.

### Q4: Apakah Aspose.Note untuk Java memerlukan lisensi untuk penggunaan komersial?
A4: Ya, lisensi yang valid diperlukan untuk penggunaan komersial Aspose.Note untuk Java. Anda dapat memperoleh lisensi dari situs web Aspose.

### Q5: Di mana saya dapat mencari bantuan jika saya mengalami masalah atau memiliki pertanyaan tentang Aspose.Note untuk Java?
A5: Untuk dukungan dan bantuan, Anda dapat mengunjungi forum Aspose.Note **[here](https://forum.aspose.com/c/note/28)**, di mana Anda dapat mengajukan pertanyaan, berbagi pengalaman, dan berinteraksi dengan pengguna serta ahli lainnya.

---

**Terakhir Diperbarui:** 2026-01-10  
**Diuji Dengan:** Aspose.Note for Java 23.12 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}