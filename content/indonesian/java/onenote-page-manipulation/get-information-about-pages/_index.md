---
title: Dapatkan Informasi tentang Halaman di OneNote - Aspose.Note
linktitle: Dapatkan Informasi tentang Halaman di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Temukan rahasia halaman di dokumen OneNote Anda! Ekstrak revisi, waktu pembuatan, & lainnya dengan Aspose.Note. Panduan langkah demi langkah & kode disertakan! #OneNote #Java #Aspose
type: docs
weight: 12
url: /id/java/onenote-page-manipulation/get-information-about-pages/
---
## Perkenalan

Dalam tutorial ini, kami akan memandu Anda melalui proses mengekstraksi informasi tentang halaman di OneNote menggunakan Aspose.Note untuk Java. Aspose.Note adalah API canggih yang memungkinkan Anda bekerja dengan dokumen Microsoft OneNote secara terprogram. Baik Anda perlu mengakses revisi halaman, waktu pembuatan, judul, atau penulis, Aspose.Note menyederhanakan tugas dengan antarmuka intuitifnya.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1. Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda.
2.  Aspose.Note untuk Java: Unduh dan instal perpustakaan Aspose.Note untuk Java. Anda bisa mendapatkannya dari[situs web](https://purchase.aspose.com/buy).
3. Contoh Dokumen OneNote: Siapkan contoh dokumen OneNote yang akan Anda gunakan untuk mengambil informasi.

## Paket Impor

Pertama, Anda perlu mengimpor paket yang diperlukan untuk bekerja dengan Aspose.Note di proyek Java Anda.

```java
import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Langkah 1: Muat Dokumen OneNote

Mulailah dengan memuat dokumen OneNote menggunakan Aspose.Note.

```java
String dataDir = "Your Document Directory";
// Muat dokumen ke Aspose.Note
LoadOptions options = new LoadOptions();
Document doc = new Document(dataDir + "Sample1.one", options);
```

 Mengganti`"Your Document Directory"` dengan jalur ke dokumen OneNote Anda.

## Langkah 2: Ambil Informasi Halaman

Selanjutnya, ambil informasi tentang halaman dalam dokumen OneNote.

```java
// Dapatkan revisi halaman
List<Page> pages = doc.getChildNodes(Page.class);

// Melintasi daftar halaman
for (Page pageRevision : pages) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
}
```

Cuplikan kode ini mengulangi setiap halaman dalam dokumen dan mencetak informasi seperti waktu modifikasi terakhir, waktu pembuatan, judul, level, dan penulis setiap halaman.

## Kesimpulan

Dalam tutorial ini, Anda mempelajari cara mengambil informasi tentang halaman di OneNote menggunakan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah yang diuraikan di atas, Anda dapat mengintegrasikan Aspose.Note dengan lancar ke dalam aplikasi Java Anda untuk mengekstrak data berharga dari dokumen OneNote.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.Note untuk Java untuk mengedit dokumen OneNote?

A1: Ya, Aspose.Note menyediakan serangkaian fitur lengkap untuk mengedit dan memanipulasi dokumen OneNote secara terprogram.

### Q2: Apakah Aspose.Note kompatibel dengan semua versi OneNote?

A2: Aspose.Note mendukung berbagai versi OneNote, memastikan kompatibilitas di berbagai lingkungan.

### Q3: Bisakah saya mengonversi dokumen OneNote ke format lain menggunakan Aspose.Note?

A3: Tentu saja, Aspose.Note memungkinkan Anda mengonversi dokumen OneNote ke format seperti PDF, HTML, dan gambar dengan mudah.

### Q4: Apakah Aspose.Note menawarkan dukungan teknis kepada pengembang?

A4: Ya, Aspose menyediakan dukungan teknis khusus untuk membantu pengembang dengan masalah apa pun yang mereka temui saat menggunakan Aspose.Note.

### Q5: Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?

 A5: Ya, Anda dapat mengunduh Aspose.Note untuk Java versi uji coba gratis dari[Di Sini](https://releases.aspose.com/).