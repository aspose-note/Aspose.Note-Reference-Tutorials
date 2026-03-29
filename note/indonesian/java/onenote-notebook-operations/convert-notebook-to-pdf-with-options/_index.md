---
date: 2026-03-29
description: Mengonversi notebook OneNote ke PDF dengan opsi, menyimpan notebook sebagai
  PDF, dan menambahkan header serta footer PDF menggunakan Aspose.Note untuk Java.
linktitle: Convert Notebook to PDF with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Konversi OneNote ke PDF dengan opsi - Aspose.Note
url: /id/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi OneNote ke PDF dengan Opsi menggunakan Aspose.Note

## Pendahuluan

Dalam tutorial ini Anda akan belajar cara **convert onenote to pdf** dengan kontrol penuh atas output. Aspose.Note untuk Java memudahkan mengekspor notebook OneNote ke PDF, memungkinkan Anda **save notebook as pdf** sambil menyesuaikan header, footer, dan perilaku pemisahan halaman. Baik Anda perlu membuat laporan, mengarsipkan catatan rapat, atau membagikan konten kepada pengguna yang tidak memiliki OneNote, panduan ini akan memandu Anda melalui setiap langkah.

## Jawaban Cepat
- **Perpustakaan apa yang menangani konversi?** Aspose.Note for Java.
- **Bisakah saya menambahkan header atau footer ke PDF?** Ya – gunakan PDF save options untuk menyisipkan header/footer khusus.
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan untuk penggunaan non‑trial.
- **Versi Java mana yang didukung?** Java 8 dan yang lebih baru.
- **Berapa lama proses konversi?** Biasanya beberapa detik untuk notebook berukuran rata-rata.

## Apa itu “convert onenote to pdf”?

Mengonversi OneNote ke PDF berarti mengambil sebuah notebook OneNote (file *.onetoc2*) dan merender setiap halaman sebagai halaman PDF. PDF yang dihasilkan mempertahankan teks, gambar, dan tata letak, sehingga dapat dilihat di perangkat apa pun tanpa memerlukan OneNote.

## Mengapa menggunakan Aspose.Note untuk mengekspor notebook onenote ke pdf?

- **Tidak memerlukan instalasi Office** – API berfungsi secara mandiri.
- **Kontrol halus** – Anda dapat mengatur algoritma pemisahan halaman, menyematkan font, dan menambahkan header/footer.
- **Fidelity tinggi** – tampilan visual notebook asli tetap dipertahankan.
- **Lintas platform** – berfungsi di Windows, Linux, dan macOS dengan runtime Java apa pun.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK) – JDK 8 atau yang lebih baru terpasang.
2. Aspose.Note untuk Java – unduh dan instal dari [download link](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment) – IntelliJ IDEA, Eclipse, atau NetBeans adalah pilihan populer.

## Impor Paket

Pertama, Anda perlu mengimpor paket yang diperlukan ke dalam proyek Java Anda. Paket-paket ini menyediakan kelas dan metode yang dibutuhkan untuk bekerja dengan dokumen OneNote.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Langkah 1: Muat Notebook OneNote

Untuk **convert onenote to pdf**, Anda perlu memuat notebook OneNote terlebih dahulu. Pastikan jalur ke file notebook sudah ditentukan dengan benar.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Langkah 2: Tentukan Opsi Penyimpanan PDF

Aspose.Note menyediakan berbagai opsi untuk menyesuaikan output PDF. Anda dapat menentukan opsi seperti algoritma pemisahan halaman, pengaturan header/footer, dan lainnya.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Langkah 3: Simpan Notebook sebagai PDF

Setelah Anda memuat notebook dan menentukan opsi penyimpanan, saatnya **save the notebook as pdf**.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|----------|
| PDF tidak menampilkan gambar | Gambar disimpan sebagai objek tersemat tidak dimuat | Pastikan file notebook dan semua sumber daya yang terhubung berada di direktori yang sama sebelum memuat. |
| Header/footer tidak muncul | Opsi header/footer tidak diatur dalam `PdfSaveOptions` | Gunakan `documentSaveOptions.setHeaderFooter()` untuk mendefinisikan konten sebelum menyimpan. |
| Kesalahan memori pada notebook besar | Seluruh notebook dimuat ke memori | Proses notebook per bagian atau tingkatkan ukuran heap JVM (`-Xmx2g`). |

## FAQ

### Q1: Bisakah saya menyesuaikan tampilan output PDF?

A1: Ya, Aspose.Note menyediakan berbagai opsi untuk menyesuaikan output PDF, termasuk pengaturan header/footer, algoritma pemisahan halaman, dan lainnya.

### Q2: Apakah Aspose.Note kompatibel dengan semua versi OneNote?

A2: Aspose.Note mendukung Microsoft OneNote 2010 dan versi yang lebih baru.

### Q3: Apakah Aspose.Note menawarkan percobaan gratis?

A3: Ya, Anda dapat mengunduh percobaan gratis Aspose.Note dari [di sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dokumentasi untuk Aspose.Note?

A4: Anda dapat menemukan dokumentasi lengkap untuk Aspose.Note [di sini](https://reference.aspose.com/note/java/).

### Q5: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.Note?

A5: Untuk bantuan teknis atau pertanyaan apa pun, Anda dapat mengunjungi forum dukungan Aspose.Note [di sini](https://forum.aspose.com/c/note/28).

## Pertanyaan Umum Tambahan

**Q: Bagaimana cara menambahkan header atau footer PDF khusus?**  
A: Buat objek `PdfHeaderFooterOptions`, konfigurasikan teks atau gambar, dan tetapkan ke `documentSaveOptions.setHeaderFooterOptions()` sebelum memanggil `save`.

**Q: Bisakah saya mengekspor hanya bagian tertentu dari notebook?**  
A: Ya – muat notebook, ambil objek `Section` yang diinginkan, dan panggil `section.save()` dengan opsi PDF yang sama.

**Q: Apakah memungkinkan untuk mengenkripsi PDF yang dihasilkan?**  
A: Tentu saja. Gunakan `documentSaveOptions.setEncryptionPassword("yourPassword")` untuk melindungi PDF.

**Q: Pertimbangan kinerja apa yang harus saya perhatikan?**  
A: Untuk notebook yang sangat besar, pertimbangkan untuk men‑stream output ke `FileOutputStream` dan meningkatkan ukuran heap JVM jika Anda mengalami `OutOfMemoryError`.

---

**Terakhir Diperbarui:** 2026-03-29  
**Diuji Dengan:** Aspose.Note for Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}