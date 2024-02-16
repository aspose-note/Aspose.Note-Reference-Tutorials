---
title: Dapatkan Revisi Halaman di OneNote - Aspose.Note
linktitle: Dapatkan Revisi Halaman di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara mengambil revisi halaman di OneNote menggunakan Aspose.Note untuk Java. Ikuti panduan langkah demi langkah kami untuk pelacakan perubahan yang efisien.
type: docs
weight: 14
url: /id/java/onenote-page-manipulation/get-page-revisions/
---
## Perkenalan

OneNote adalah alat canggih untuk mengatur dan mengelola catatan Anda, namun terkadang Anda perlu melacak perubahan dan revisi yang dilakukan pada halaman Anda. Dengan Aspose.Note untuk Java, Anda dapat dengan mudah mengambil revisi halaman secara terprogram. Dalam tutorial ini, kami akan memandu Anda melalui proses mendapatkan revisi halaman di OneNote menggunakan Aspose.Note untuk Java.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

### 1. Kit Pengembangan Java (JDK)

Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda. Anda dapat mengunduh dan menginstal JDK dari situs web Oracle.

### 2. Aspose.Note untuk Java

Unduh dan instal Aspose.Note untuk Java dari[tautan unduhan](https://releases.aspose.com/note/java/).

### 3. Contoh Dokumen OneNote

Siapkan contoh dokumen OneNote (`Sample1.one`) yang berisi halaman yang ingin Anda ambil revisinya.

## Paket Impor

Pertama, Anda perlu mengimpor paket yang diperlukan dari Aspose.Note untuk Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Sekarang, mari kita bagi contoh yang diberikan menjadi beberapa langkah:

## Langkah 1: Siapkan Direktori Dokumen

Tentukan jalur direktori tempat dokumen OneNote Anda berada.

```java
String dataDir = "Your Document Directory";
```

## Langkah 2: Muat Dokumen OneNote

 Muat dokumen OneNote menggunakan`LoadOptions` untuk mengaktifkan riwayat pemuatan.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Langkah 3: Dapatkan Halaman Pertama

Ambil halaman pertama dari dokumen yang dimuat.

```java
Page firstPage = document.getFirstChild();
```

## Langkah 4: Ulangi Revisi Halaman

Ulangi setiap revisi halaman dan ambil informasi yang relevan seperti waktu modifikasi terakhir, waktu pembuatan, judul, level, dan penulis.

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

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara mengambil revisi halaman di OneNote menggunakan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah ini, Anda bisa secara efisien melacak perubahan yang dibuat pada halaman OneNote Anda secara terprogram.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.Note untuk Java untuk mengubah revisi halaman?

A1: Tidak, Aspose.Note untuk Java saat ini mendukung pengambilan revisi halaman tetapi tidak memodifikasinya.

### Q2: Apakah Aspose.Note untuk Java kompatibel dengan versi dokumen OneNote yang berbeda?

A2: Ya, Aspose.Note untuk Java mendukung berbagai versi dokumen OneNote, memungkinkan Anda bekerja dengan format file berbeda secara lancar.

### Q3: Apakah Aspose.Note untuk Java memerlukan lisensi untuk digunakan?

A3: Ya, Anda perlu membeli lisensi untuk menggunakan Aspose.Note untuk Java dalam proyek komersial. Namun, Anda juga bisa mendapatkan lisensi sementara untuk tujuan evaluasi.

### Q4: Dapatkah saya mencari dukungan jika saya mengalami masalah apa pun saat menggunakan Aspose.Note untuk Java?

 A4: Ya, Anda dapat mencari dukungan dari forum Aspose.Note[Di Sini](https://forum.aspose.com/c/note/28).

### Q5: Apakah tersedia uji coba gratis untuk Aspose.Note untuk Java?

 A5: Ya, Anda dapat mengakses uji coba gratis Aspose.Note untuk Java dari[situs web](https://releases.aspose.com/).