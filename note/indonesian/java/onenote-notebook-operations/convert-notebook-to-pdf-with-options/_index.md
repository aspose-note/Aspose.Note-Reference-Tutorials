---
title: Konversi Buku Catatan ke PDF dengan Opsi di OneNote - Aspose.Note
linktitle: Konversi Buku Catatan ke PDF dengan Opsi di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Sesuaikan & ekspor buku catatan OneNote ke PDF dengan mudah! Aspose.Note untuk Java menangani pekerjaan berat. Panduan langkah demi langkah disertakan! #OneNote #Java #Aspose
weight: 17
url: /id/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi Buku Catatan ke PDF dengan Opsi di OneNote - Aspose.Note

## Perkenalan

Dalam tutorial ini, kita akan mempelajari dunia konversi buku catatan ke PDF dengan opsi yang dapat disesuaikan menggunakan Aspose.Note untuk Java. Aspose.Note adalah Java API canggih yang memungkinkan pengembang memanipulasi dokumen Microsoft OneNote secara terprogram. Mengonversi buku catatan ke format PDF merupakan persyaratan umum di berbagai aplikasi, dan dengan Aspose.Note, tugas ini menjadi efisien dan efisien.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda.
2. Aspose.Note for Java: Unduh dan instal Aspose.Note for Java dari[tautan unduhan](https://releases.aspose.com/note/java/).
3. IDE (Lingkungan Pengembangan Terpadu): Pilih IDE pilihan Anda untuk pengembangan Java. IntelliJ IDEA, Eclipse, atau NetBeans adalah pilihan populer.

## Paket Impor

Pertama, Anda perlu mengimpor paket yang diperlukan ke proyek Java Anda. Paket-paket ini menyediakan kelas dan metode yang diperlukan untuk bekerja dengan dokumen OneNote.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Langkah 1: Muat Buku Catatan OneNote

Untuk mengonversi buku catatan ke PDF, Anda perlu memuat buku catatan OneNote terlebih dahulu. Pastikan jalur ke file buku catatan ditentukan dengan benar.

```java
String dataDir = "Your Document Directory";
// Memuat Buku Catatan OneNote
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Langkah 2: Tentukan Opsi Penyimpanan PDF

Aspose.Note menyediakan berbagai opsi untuk menyesuaikan keluaran PDF. Anda dapat menentukan opsi seperti algoritma pemisahan halaman, pengaturan header/footer, dan banyak lagi.

```java
// Tentukan opsi penyimpanan PDF
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Langkah 3: Simpan Buku Catatan sebagai PDF

Setelah Anda memuat buku catatan dan menentukan opsi penyimpanan, sekarang saatnya menyimpan buku catatan sebagai file PDF.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Simpan Buku Catatan
notebook.save(dataDir, notebookSaveOptions);
```

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi cara mengonversi buku catatan OneNote ke format PDF menggunakan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah sederhana ini, Anda dapat menangani konversi dokumen secara efisien di aplikasi Java Anda.

---

## FAQ

### Q1: Dapatkah saya menyesuaikan tampilan keluaran PDF?

A1: Ya, Aspose.Note menyediakan berbagai opsi untuk menyesuaikan keluaran PDF, termasuk pengaturan header/footer, algoritma pemisahan halaman, dan banyak lagi.

### Q2: Apakah Aspose.Note kompatibel dengan semua versi OneNote?

A2: Aspose.Note mendukung Microsoft OneNote 2010 dan versi yang lebih baru.

### Q3: Apakah Aspose.Note menawarkan uji coba gratis?

 A3: Ya, Anda dapat mengunduh uji coba gratis Aspose.Note dari[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dokumentasi untuk Aspose.Note?

 A4: Anda dapat menemukan dokumentasi komprehensif untuk Aspose.Note[Di Sini](https://reference.aspose.com/note/java/).

### Q5: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.Note?

 A5: Untuk bantuan teknis atau pertanyaan apa pun, Anda dapat mengunjungi forum dukungan Aspose.Note[Di Sini](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
