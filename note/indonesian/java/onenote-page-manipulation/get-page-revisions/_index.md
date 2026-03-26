---
date: 2026-01-10
description: Pelajari tutorial revisi halaman Aspose.Note untuk Java – ambil revisi
  halaman OneNote secara programatis menggunakan Aspose.Note. Ikuti panduan langkah
  demi langkah kami.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Tutorial revisi halaman aspose.note – Dapatkan Revisi Halaman di OneNote
url: /id/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dapatkan Revisi Halaman di OneNote - Aspose.Note

OneNote adalah platform pencatatan yang kuat, dan ketika Anda perlu mengaudit perubahan, **aspose.note page revisions tutorial** menunjukkan secara tepat cara mengambil riwayat revisi dengan hanya beberapa baris kode Java. Dalam panduan ini kami akan membahas semua yang Anda perlukan—dari menyiapkan lingkungan hingga mencetak detail setiap revisi—sehingga Anda dapat melacak edit, kontribusi penulis, dan cap waktu dengan mudah.

## Quick Answers
- **What does the tutorial cover?** Mengambil riwayat revisi halaman dari file OneNote menggunakan Aspose.Note untuk Java.  
- **Which library version is required?** Versi terbaru Aspose.Note untuk Java yang mendukung `LoadOptions.setLoadHistory`.  
- **Do I need a license?** Lisensi evaluasi sementara dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Can I modify revisions?** API bersifat read‑only untuk revisi; Anda hanya dapat mengambilnya.  
- **What are the main prerequisites?** Java JDK, Aspose.Note untuk Java, dan dokumen OneNote dengan data revisi.

## What is the “aspose.note page revisions tutorial”?
Tutorial ini menunjukkan cara mengakses secara programatis versi historis dari sebuah halaman OneNote. Setiap revisi berisi metadata seperti penulis, waktu pembuatan, dan waktu modifikasi, memungkinkan Anda membangun jejak audit atau fitur log perubahan di dalam aplikasi Anda.

## Why use Aspose.Note for page revision tracking?
- **No UI dependency** – berfungsi sepenuhnya dalam kode, cocok untuk layanan backend.  
- **Cross‑platform** – Java berjalan di Windows, Linux, dan macOS.  
- **Full control** – mengambil setiap properti revisi tanpa membuka OneNote secara manual.  
- **Performance** – memuat riwayat dioptimalkan, sehingga bahkan notebook besar diproses dengan cepat.

## Prerequisites

### 1. Java Development Kit (JDK)
Pastikan JDK terbaru (8 atau lebih tinggi) terinstal dan `JAVA_HOME` sudah diset.

### 2. Aspose.Note for Java
Unduh pustaka dari [download link](https://releases.aspose.com/note/java/).

### 3. Sample OneNote Document
Buat atau dapatkan file OneNote (misalnya `Sample1.one`) yang berisi halaman dengan riwayat revisi.

## Import Packages
First, import the required Aspose.Note classes.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Step‑by‑Step Implementation

### Step 1: Set Up Document Directory
Define the folder where your OneNote file resides.

```java
String dataDir = "Your Document Directory";
```

### Step 2: Load OneNote Document with History Enabled
Enable the `LoadOptions` flag to pull revision data.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Step 3: Get the First Page
Grab the first page object; this will be the reference point for retrieving its history.

```java
Page firstPage = document.getFirstChild();
```

### Step 4: Iterate Through Page Revisions
Loop through each revision and print useful metadata such as timestamps, title, level, and author.

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

> **Pro tip:** Jika Anda perlu menyaring revisi berdasarkan penulis tertentu atau rentang tanggal, cukup tambahkan pemeriksaan kondisional di dalam loop `for`.

## Common Issues & Solutions
- **No revisions returned:** Verifikasi bahwa `loadOptions.setLoadHistory(true)` dipanggil sebelum memuat dokumen.  
- **Null author or title:** Beberapa versi OneNote yang lebih lama mungkin tidak menyimpan bidang ini; tangani nilai `null` dengan hati-hati.  
- **Performance lag on large notebooks:** Muat hanya bagian yang Anda perlukan atau tingkatkan ukuran heap JVM.

## Frequently Asked Questions

**Q1: Can I use Aspose.Note for Java to modify page revisions?**  
A1: Tidak, API saat ini hanya mendukung akses read‑only ke revisi halaman.

**Q2: Is Aspose.Note for Java compatible with different versions of OneNote documents?**  
A2: Ya, ia bekerja dengan berbagai format file OneNote, memungkinkan pemrosesan mulus di semua versi.

**Q3: Does Aspose.Note for Java require a license to use?**  
A3: Lisensi komersial diperlukan untuk penggunaan produksi, namun lisensi evaluasi sementara tersedia untuk pengujian.

**Q4: Can I seek support if I encounter any issues while using Aspose.Note for Java?**  
A4: Ya, Anda dapat mengajukan pertanyaan di forum Aspose.Note [here](https://forum.aspose.com/c/note/28).

**Q5: Is there a free trial available for Aspose.Note for Java?**  
A5: Ya, Anda dapat mengunduh trial gratis dari [website](https://releases.aspose.com/).

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}