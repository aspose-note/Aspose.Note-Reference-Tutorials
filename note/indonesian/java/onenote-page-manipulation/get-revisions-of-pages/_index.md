---
title: Dapatkan Revisi Halaman di OneNote - Aspose.Note
linktitle: Dapatkan Revisi Halaman di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara mengambil revisi halaman dalam dokumen OneNote menggunakan Aspose.Note Java. Integrasikan ini ke dalam aplikasi Java Anda untuk manajemen dokumen yang efisien.
weight: 15
url: /id/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dapatkan Revisi Halaman di OneNote - Aspose.Note

## Perkenalan

Dalam tutorial ini, kita akan mempelajari kemampuan Aspose.Note untuk Java, pustaka canggih yang memungkinkan Anda bekerja dengan file Microsoft OneNote secara lancar di aplikasi Java Anda. Secara khusus, kami akan fokus pada cara mengambil revisi halaman dalam dokumen OneNote. Di akhir panduan ini, Anda akan dibekali dengan pengetahuan untuk mengekstrak revisi halaman secara efisien, termasuk detail seperti waktu modifikasi terakhir, waktu pembuatan, judul, level, dan penulis.

## Prasyarat

Sebelum mendalami tutorial ini, pastikan Anda telah menyiapkan prasyarat berikut:

### Kit Pengembangan Java (JDK) Terpasang

Pastikan Anda telah menginstal Java Development Kit di sistem Anda. Anda dapat mengunduh dan menginstalnya dari situs web Oracle atau menggunakan manajer paket jika Anda menggunakan sistem berbasis Unix.

### Aspose.Catatan untuk Perpustakaan Java

 Unduh dan instal Aspose.Note untuk perpustakaan Java dari situs web. Anda dapat menemukan tautan unduhan[Di Sini](https://releases.aspose.com/note/java/) . Ikuti petunjuk instalasi yang disediakan dalam dokumentasi[Di Sini](https://reference.aspose.com/note/java/).

## Paket Impor

Untuk memulai, impor paket yang diperlukan ke proyek Java Anda. Paket-paket ini akan memungkinkan Anda memanfaatkan fungsionalitas yang disediakan oleh Aspose.Note untuk Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Sekarang, mari kita uraikan kode contoh yang diberikan menjadi beberapa langkah untuk memahami setiap komponen dan fungsinya.

## Langkah 1: Atur Direktori Dokumen

Tentukan direktori tempat dokumen OneNote Anda berada.

```java
String dataDir = "Your Document Directory";
```

## Langkah 2: Muat Dokumen

Muat dokumen OneNote ke Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Langkah 3: Dapatkan Halaman Pertama

Ambil halaman pertama dari dokumen.

```java
Page firstPage = doc.getFirstChild();
```

## Langkah 4: Dapatkan Revisi Halaman

Dapatkan riwayat revisi halaman.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Langkah 5: Melintasi Revisi Halaman

Ulangi daftar revisi halaman dan ambil informasi yang relevan.

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

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi cara mengambil revisi halaman dalam dokumen OneNote menggunakan Aspose.Note untuk Java. Dengan mengikuti panduan langkah demi langkah dan memanfaatkan kode contoh yang disediakan, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam aplikasi Java Anda, sehingga memungkinkan pengelolaan file OneNote secara efisien.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.Note untuk Java untuk membuat dokumen OneNote baru?

A1: Ya, Aspose.Note untuk Java menyediakan dukungan komprehensif untuk membuat, membaca, dan memanipulasi dokumen OneNote secara terprogram.

### Q2: Apakah Aspose.Note untuk Java kompatibel dengan versi file OneNote yang berbeda?

A2: Ya, Aspose.Note untuk Java mendukung berbagai versi file Microsoft OneNote, memastikan kompatibilitas di berbagai lingkungan.

### Q3: Bisakah saya mengkustomisasi format output saat mengekspor dokumen OneNote?

A3: Tentu saja, Aspose.Note untuk Java menawarkan fleksibilitas dalam mengekspor dokumen OneNote ke berbagai format seperti PDF, HTML, dan gambar, dengan opsi penyesuaian.

### Q4: Apakah Aspose.Note untuk Java memerlukan lisensi untuk penggunaan komersial?

A4: Ya, diperlukan lisensi yang valid untuk penggunaan komersial Aspose.Note untuk Java. Anda dapat memperoleh lisensi dari situs Aspose.

### Q5: Di mana saya dapat mencari bantuan jika saya mengalami masalah atau memiliki pertanyaan tentang Aspose.Note untuk Java?

 A5: Untuk dukungan dan bantuan, Anda dapat mengunjungi forum Aspose.Note[Di Sini](https://forum.aspose.com/c/note/28)tempat Anda dapat mengajukan pertanyaan, berbagi pengalaman, dan berinteraksi dengan pengguna dan pakar lain.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
