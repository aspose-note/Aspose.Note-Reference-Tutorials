---
date: 2026-03-16
description: Pelajari cara mengekspor PDF OneNote menggunakan Aspose.Note untuk Java
  dengan Metode Algoritma Pemisahan, mengontrol pemisahan halaman, dan mengompresi
  gambar PDF secara efisien.
linktitle: Export OneNote PDF with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Ekspor PDF OneNote dengan Metode Algoritma Pemisahan – Aspose.Note
url: /id/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor OneNote PDF dengan Metode Algoritma Pemisahan – Aspose.Note

## Introduction

Jika Anda perlu **mengekspor OneNote PDF** secara programatis, Aspose.Note untuk Java membuatnya menjadi mudah. Pada tutorial ini kami akan membahas Metode Algoritma Pemisahan, yang memungkinkan Anda mengontrol bagaimana konten dipisahkan antar halaman, sehingga menghasilkan PDF yang bersih dan mudah dibaca. Anda akan melihat cara mengatur opsi penyimpanan PDF, memilih algoritma pemisahan halaman yang tepat, dan akhirnya menghasilkan file PDF—semua hanya dengan beberapa baris kode Java.

## Quick Answers
- **Apa yang dilakukan Algoritma Pemisahan?** Algoritma ini menentukan bagaimana objek yang melintasi batas halaman ditangani saat mengekspor halaman OneNote ke PDF.  
- **Perpustakaan apa yang diperlukan?** Aspose.Note untuk Java (unduh dari situs resmi Aspose).  
- **Apakah saya memerlukan lisensi?** Lisensi sementara atau penuh diperlukan untuk penggunaan produksi; tersedia versi percobaan gratis.  
- **Bisakah saya mengekspor notebook OneNote yang besar?** Ya – perpustakaan ini memproses file besar secara efisien dan memungkinkan Anda mengatur aturan pemisahan halaman.  
- **Format output apa yang didukung?** PDF, JPEG, PNG, XPS, dan lainnya; panduan ini fokus pada ekspor PDF.  
- **Bagaimana cara mengompres gambar PDF?** Gunakan `pdfSaveOptions.setCompressImages(true)` untuk mengurangi ukuran gambar dalam PDF yang dihasilkan.  

## How to export OneNote PDF with Splitting Algorithm
Bagian ini memandu Anda melalui langkah‑langkah tepat untuk **mengonversi halaman OneNote** menjadi PDF sambil menangani pemisahan halaman secara cerdas.

## What is export onenote pdf?
Mengekspor OneNote PDF berarti mengonversi format file native `.one` menjadi dokumen PDF yang dapat dibawa ke mana saja. Ini berguna untuk berbagi, mengarsipkan, atau mencetak konten tanpa memerlukan aplikasi OneNote.

## Why use the Splitting Algorithm for export onenote pdf?
Algoritma ini memberi Anda kontrol detail tentang bagaimana objek kompleks (tabel, gambar, gambar tangan) ditangani pada pemisahan halaman. Dengan memilih algoritma yang tepat, Anda dapat:

* Mempertahankan tata letak visual setiap halaman.  
* Menghindari konten terpotong yang sebaliknya akan terpotong.  
* Mengurangi jumlah halaman yang dihasilkan ketika objek dapat dipindahkan ke halaman berikutnya secara bersih.  

## Prerequisites

Sebelum memulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK): Pastikan JDK terinstal di sistem Anda. Anda dapat mengunduhnya dari [website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.Note for Java Library: Unduh dan instal perpustakaan Aspose.Note untuk Java dari [download link](https://releases.aspose.com/note/java/).

## Import Packages

Di proyek Java Anda, impor paket yang diperlukan untuk memanfaatkan fungsionalitas Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Step 1: Define Document Directory

Siapkan direktori tempat dokumen OneNote Anda berada.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the OneNote Document

Muat dokumen OneNote menggunakan kelas `Document` milik Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Step 3: Set PDF Save Options

Buat instance `PdfSaveOptions` untuk menentukan opsi penyimpanan dokumen sebagai PDF. Di sinilah Anda **mengatur perilaku pemisahan halaman** dan pengaturan terkait PDF lainnya.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Step 4: Set Page Splitting Algorithm

Pilih algoritma pemisahan yang sesuai dengan kebutuhan Anda. Di sini, kami menggunakan `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, yang mempertahankan sebagian objek pada halaman saat ini dan menggandakan sisanya ke halaman berikutnya.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Step 5: Save the Document

Simpan dokumen dengan opsi penyimpanan PDF yang telah ditentukan. Langkah ini **menghasilkan output PDF OneNote** yang dapat Anda buka, bagikan, atau cetak.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Common Issues and Solutions

| Masalah | Solusi |
|-------|----------|
| **Objek terpotong pada batas halaman** | Coba algoritma lain seperti `AlwaysSplitObjectsAlgorithm` atau tingkatkan nilai ambang pada `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **PDF output kosong** | Pastikan file `.one` sumber tidak rusak dan jalur `dataDir` sudah benar. |
| **Kinerja lambat pada notebook besar** | Gunakan `pdfSaveOptions.setCompressImages(true)` untuk mengurangi penggunaan memori, dan pertimbangkan memproses notebook dalam bagian yang lebih kecil. |

## Frequently Asked Questions

**Q: Bisakah saya menggunakan Aspose.Note untuk Java dengan bahasa pemrograman lain?**  
A: Ya, Aspose.Note juga tersedia untuk .NET, C++, dan Python.

**Q: Apakah Aspose.Note cocok untuk memproses file OneNote yang besar?**  
A: Tentu saja. Perpustakaan ini dioptimalkan untuk menangani notebook besar secara efisien.

**Q: Di mana saya dapat menemukan sumber daya tambahan dan dukungan untuk Aspose.Note?**  
A: Anda dapat merujuk ke [documentation](https://reference.aspose.com/note/java/) dan [forum](https://forum.aspose.com/c/note/28) untuk dukungan dan panduan.

**Q: Bisakah saya mencoba Aspose.Note sebelum membeli?**  
A: Ya, Anda dapat memanfaatkan [free trial](https://releases.aspose.com/) untuk menjelajahi fitur sebelum melakukan pembelian.

**Q: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Note?**  
A: Anda dapat meminta [temporary license](https://purchase.aspose.com/temporary-license/) untuk mengevaluasi produk dalam periode percobaan.

---

**Last Updated:** 2026-03-16  
**Tested With:** Aspose.Note 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}