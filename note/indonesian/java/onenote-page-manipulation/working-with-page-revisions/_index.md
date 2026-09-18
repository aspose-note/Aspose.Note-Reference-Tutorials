---
date: 2026-01-15
description: Pelajari cara melacak perubahan OneNote dan mengelola revisi halaman
  dalam dokumen OneNote menggunakan Aspose.Note untuk Java. Termasuk contoh ringkasan
  revisi dan cara mengubah tanggal revisi.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Lacak Perubahan OneNote – Kelola Revisi Halaman dengan Aspose.Note
url: /id/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bekerja dengan Revisi Halaman di OneNote - Aspose.Note

## Pendahuluan

OneNote adalah alat yang kuat untuk mengatur catatan, dan ketika Anda perlu **track changes onenote**, mengelola revisi halaman menjadi penting untuk kolaborasi yang efektif. Dengan Aspose.Note untuk Java, Anda dapat menangani revisi secara programatis, melihat siapa yang mengedit halaman, dan bahkan menyesuaikan cap waktu. Tutorial ini memandu Anda melalui setiap langkah, mulai dari memuat dokumen hingga memperbarui ringkasan revisi.

## Jawaban Cepat
- **Apa arti “track changes onenote”?** It refers to monitoring who edited a OneNote page and when.
- **Library apa yang diperlukan?** Aspose.Note for Java.
- **Bisakah saya mengubah penulis atau tanggal revisi?** Ya, menggunakan RevisionSummary API (`modify revision date`).
- **Apakah saya memerlukan file OneNote sebelumnya?** Ya, file contoh `.one` diperlukan.
- **Apakah lisensi diperlukan untuk produksi?** Lisensi Aspose.Note yang valid diperlukan untuk penggunaan komersial.

## Apa itu contoh ringkasan revisi?

Sebuah *revision summary* menyediakan metadata tentang perubahan terbaru pada sebuah halaman—nama penulis, waktu terakhir diubah, dan detail lainnya. Dalam panduan ini kami akan mengambil dan menampilkan informasi tersebut, kemudian menunjukkan cara **modify revision date**.

## Mengapa melacak perubahan onenote dengan Aspose.Note?

- **Kolaborasi:** Lihat dengan cepat siapa yang melakukan edit terbaru.
- **Audit:** Simpan riwayat perubahan yang dapat diandalkan untuk kepatuhan.
- **Otomatisasi:** Integrasikan penanganan revisi ke dalam layanan back‑end atau alat migrasi.

## Prasyarat

### Lingkungan Pengembangan Java

Pastikan Anda memiliki Java Development Kit (JDK) terpasang di sistem Anda.

### Perpustakaan Aspose.Note untuk Java

Unduh dan instal perpustakaan Aspose.Note untuk Java dari [di sini](https://releases.aspose.com/note/java/).

### Dokumen OneNote

Siapkan dokumen OneNote contoh untuk keperluan pengujian.

## Impor Paket

Dalam proyek Java Anda, impor paket yang diperlukan untuk bekerja dengan Aspose.Note untuk Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Mari kita uraikan contoh yang diberikan menjadi beberapa langkah untuk pemahaman yang jelas.

## Langkah 1: Muat Dokumen OneNote

Pertama, muat dokumen OneNote dan dapatkan halaman anak pertama.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Langkah 2: Baca Ringkasan Revisi Halaman

Baca ringkasan revisi konten untuk halaman tersebut. Ini adalah **revision summary example** yang menunjukkan siapa yang terakhir mengedit halaman.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Langkah 3: Perbarui Ringkasan Revisi Halaman

Perbarui ringkasan revisi halaman dengan penulis baru dan tanggal modifikasi baru. Ini menunjukkan cara **modify revision date** secara programatis.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Kesimpulan

Mengelola revisi halaman dalam dokumen OneNote secara programatis dapat disederhanakan dengan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah yang dijelaskan dalam tutorial ini, Anda dapat secara efektif **track changes onenote**, melihat detail revisi, dan bahkan **modify revision date** sesuai alur kerja Anda.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.Note untuk Java dengan perpustakaan Java lain?

A: Ya, Aspose.Note untuk Java dapat diintegrasikan dengan perpustakaan Java lain untuk meningkatkan fungsionalitas.

### Q2: Apakah Aspose.Note untuk Java mendukung semua versi dokumen OneNote?

A: Aspose.Note untuk Java mendukung berbagai versi dokumen OneNote, termasuk versi lama.

### Q3: Apakah Aspose.Note untuk Java cocok untuk aplikasi tingkat perusahaan?

A: Tentu saja, Aspose.Note untuk Java dirancang untuk memenuhi kebutuhan aplikasi tingkat perusahaan dengan fitur yang kuat dan skalabilitas.

### Q4: Bisakah saya menyesuaikan revisi halaman dengan Aspose.Note untuk Java?

A: Ya, Anda dapat menyesuaikan revisi halaman sesuai kebutuhan Anda menggunakan Aspose.Note untuk Java.

### Q5: Di mana saya dapat mendapatkan dukungan untuk Aspose.Note untuk Java?

A: Anda dapat mendapatkan dukungan untuk Aspose.Note untuk Java dari [Aspose.Note forum](https://forum.aspose.com/c/note/28).

---

**Terakhir Diperbarui:** 2026-01-15  
**Diuji Dengan:** Aspose.Note for Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}