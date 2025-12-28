---
date: 2025-12-28
description: Pelajari cara mengekspor OneNote ke PDF dengan kontrol penuh menggunakan
  Aspose.Note untuk Java. Termasuk opsi mengekspor notebook OneNote ke PDF dan panduan
  mengonversi notebook ke PDF dengan Java.
linktitle: How to Export OneNote to PDF with Options – Convert Notebook to PDF using
  Aspose.Note
second_title: Aspose.Note Java API
title: Cara Mengekspor OneNote ke PDF dengan Opsi – Mengonversi Notebook ke PDF menggunakan
  Aspose.Note
url: /id/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengekspor OneNote ke PDF dengan Opsi – Aspose.Note Java API

## Pendahuluan

Dalam tutorial ini, Anda akan belajar **cara mengekspor OneNote ke PDF** dengan opsi yang dapat disesuaikan menggunakan Aspose.Note untuk Java. Mengonversi notebook OneNote ke PDF adalah kebutuhan yang sering muncul—baik Anda perlu membagikan catatan rapat, mengarsipkan dokumentasi, atau menghasilkan laporan yang dapat dicetak. Dengan Aspose.Note, prosesnya sederhana, sepenuhnya dapat diprogram, dan memberi Anda kontrol yang sangat detail atas PDF yang dihasilkan.

## Jawaban Cepat
- **Apa yang dilakukan API?** API memuat notebook OneNote dan menyimpannya sebagai PDF dengan pengaturan opsional.  
- **Bahasa apa yang digunakan?** Java – sempurna untuk aplikasi sisi‑server atau desktop.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengontrol tata letak halaman?** Ya, Anda dapat mengatur algoritma pemisahan halaman, header, footer, dan lainnya.  
- **Apakah contoh kode dapat dijalankan?** Tentu – cukup ganti jalur placeholder dengan lokasi notebook Anda.

## Apa itu “cara mengekspor onenote ke pdf”?

Mengekspor OneNote ke PDF berarti mengubah notebook OneNote asli (`*.onetoc2` dan file bagian terkait) menjadi dokumen PDF portabel dengan tata letak tetap. Konversi ini mempertahankan pemformatan, gambar, dan objek tertanam sekaligus membuat konten dapat dilihat di perangkat apa pun tanpa memerlukan OneNote.

## Mengapa menggunakan Aspose.Note untuk Java?

- **Tanpa ketergantungan Microsoft Office** – bekerja di platform apa pun yang menjalankan Java.  
- **Opsi PDF kaya** – kontrol pemisahan halaman, header/footer, dan penanganan objek.  
- **Fidelity tinggi** – output PDF sangat mirip dengan tampilan OneNote asli.  
- **Skalabel** – cocok untuk pemrosesan batch ribuan notebook.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – versi 8 atau lebih tinggi.  
2. **Aspose.Note untuk Java** – unduh dari [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau NetBeans (pilihan Anda).  
4. **Notebook OneNote** yang ingin Anda konversi (misalnya `Notizbuch öffnen.onetoc2`).

## Impor Paket

Pertama, impor kelas‑kelas yang menyediakan penanganan notebook dan fungsi penyimpanan PDF.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Langkah 1: Muat Notebook OneNote

Muat file notebook dari disk. Ganti `Your Document Directory` dengan folder sebenarnya yang berisi file `.onetoc2` Anda.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Langkah 2: Tentukan Opsi Penyimpanan PDF

Di sini Anda menentukan bagaimana PDF harus dihasilkan. Contoh ini mengatur algoritma pemisahan halaman yang menjaga objek solid tetap bersama, berguna ketika Anda memiliki diagram atau tabel yang harus tetap pada halaman yang sama.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Langkah 3: Simpan Notebook sebagai PDF

Akhirnya, tulis notebook ke dalam file PDF. Jalur output dapat berupa lokasi mana pun yang Anda inginkan.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Masalah Umum dan Solusinya

| Masalah | Mengapa Terjadi | Solusi |
|-------|----------------|-----|
| **File tidak ditemukan** | Direktori `dataDir` atau nama file salah. | Periksa kembali jalur dan pastikan file notebook ada. |
| **Font hilang** | Rendering PDF membutuhkan font yang sama dengan OneNote. | Instal font yang diperlukan di server atau sematkan melalui opsi Aspose tambahan. |
| **Notebook besar menyebabkan OutOfMemoryError** | Seluruh notebook dimuat ke dalam memori. | Proses setiap bagian secara terpisah atau tingkatkan ukuran heap JVM (`-Xmx`). |

## Kesimpulan

Kami telah membahas **cara mengekspor OneNote ke PDF** menggunakan Aspose.Note untuk Java, mencakup pemuatan notebook, konfigurasi opsi PDF, dan penyimpanan hasil. Dengan mengikuti langkah‑langkah ini, Anda dapat mengintegrasikan konversi notebook‑ke‑PDF ke dalam aplikasi Java apa pun, baik itu alat desktop, layanan web, atau backend pemrosesan batch.

## FAQ

### Q1: Bisakah saya menyesuaikan tampilan output PDF?

A1: Ya, Aspose.Note menyediakan berbagai opsi untuk menyesuaikan output PDF, termasuk pengaturan header/footer, algoritma pemisahan halaman, dan lainnya.

### Q2: Apakah Aspose.Note kompatibel dengan semua versi OneNote?

A2: Aspose.Note mendukung Microsoft OneNote 2010 dan versi selanjutnya.

### Q3: Apakah Aspose.Note menawarkan percobaan gratis?

A3: Ya, Anda dapat mengunduh percobaan gratis Aspose.Note dari [sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dokumentasi untuk Aspose.Note?

A4: Dokumentasi lengkap untuk Aspose.Note dapat ditemukan [di sini](https://reference.aspose.com/note/java/).

### Q5: Bagaimana cara mendapatkan dukungan untuk Aspose.Note?

A5: Untuk bantuan teknis atau pertanyaan, Anda dapat mengunjungi forum dukungan Aspose.Note [di sini](https://forum.aspose.com/c/note/28).

## Pertanyaan Tambahan yang Sering Diajukan

**Q: Bagaimana cara mengekspor notebook onenote ke pdf tanpa kehilangan gambar?**  
A: Pastikan `KeepSolidObjectsAlgorithm` diatur (seperti yang ditunjukkan) dan file gambar notebook sumber dapat diakses di direktori yang sama.

**Q: Bisakah saya mengonversi beberapa notebook secara batch dalam satu kali jalan?**  
A: Ya. Lakukan iterasi pada daftar jalur notebook, buat instance `Notebook` untuk masing‑masing, terapkan `NotebookPdfSaveOptions` yang sama, dan panggil `save()`.

**Q: Apakah ada cara untuk mengatur metadata PDF (penulis, judul) selama konversi?**  
A: Gunakan `PdfSaveOptions.setMetadata()` untuk menentukan penulis, judul, subjek, dan kata kunci sebelum menyimpan.

**Q: Apakah API mendukung PDF yang dilindungi kata sandi?**  
A: Anda dapat menetapkan kata sandi pada `PdfSaveOptions` melalui `setEncryptionPassword()` setelah mengonfigurasi opsi lainnya.

**Q: Versi Aspose.Note apa yang digunakan untuk tutorial ini?**  
A: Kode telah diuji dengan Aspose.Note untuk Java 23.12.

---

**Terakhir Diperbarui:** 2025-12-28  
**Diuji Dengan:** Aspose.Note untuk Java 23.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}