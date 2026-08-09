---
date: 2026-04-01
description: Pelajari cara mengekstrak tugas dari Outlook ke OneNote menggunakan Aspose.Note
  untuk Java. Ikuti panduan langkah demi langkah ini untuk mengambil detail tugas
  dengan cepat.
keywords:
- how to extract tasks
- Aspose.Note Java
- Outlook task extraction
linktitle: Dapatkan Tugas Outlook di OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Cara Mengekstrak Tugas Outlook di OneNote dengan Aspose.Note
url: /id/java/task-and-outlook-integration/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dapatkan Tugas Outlook di OneNote - Aspose.Note

## Pendahuluan
Selamat datang di panduan komprehensif kami tentang **cara mengekstrak tugas** dari Outlook dalam notebook OneNote menggunakan Aspose.Note untuk Java. Baik Anda sedang membangun alat migrasi, menghasilkan laporan, atau sekadar perlu menyinkronkan data tugas, tutorial ini akan memandu Anda melalui setiap langkah—dari memuat file OneNote hingga membaca properti masing‑masing tugas Outlook. Pada akhir tutorial, Anda akan memiliki potongan kode siap pakai yang dapat Anda sesuaikan dengan proyek Anda sendiri.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Mengekstrak detail tugas Outlook dari dokumen OneNote dengan Aspose.Note untuk Java.  
- **API mana yang digunakan?** Perpustakaan Aspose.Note Java.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis cukup untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit setelah lingkungan disiapkan.  
- **Bisakah saya memproses banyak notebook?** Ya—cukup lakukan loop pada file dan gunakan kembali logika yang sama.

## Apa itu ekstraksi tugas?
Ekstraksi tugas mengacu pada pembacaan informasi tugas terstruktur (seperti tanggal jatuh tempo, status, dan ikon) yang disimpan Outlook di dalam halaman OneNote sebagai tag `NoteTask`. Hal ini memungkinkan akses programatik ke metadata tugas tanpa harus menyalin secara manual.

## Mengapa menggunakan Aspose.Note untuk Java?
- **No Microsoft Office required** – works on any platform with a Java runtime.  
- **Full fidelity** – preserves all OneNote elements while giving you direct access to tags.  
- **High performance** – optimized for large notebooks and batch processing.  

## Prasyarat
Sebelum kita mulai, pastikan Anda memiliki hal‑hal berikut siap:

- **Java Development Environment** – JDK 8 atau yang lebih baru terpasang dan terkonfigurasi.  
- **Aspose.Note Library** – Unduh paket Java terbaru dari situs resmi [here](https://releases.aspose.com/note/java/).  
- **A sample OneNote file** – Tutorial ini menggunakan `Sample1.one`; Anda dapat menggantinya dengan notebook apa pun yang berisi tugas Outlook.

## Impor Paket
Tambahkan impor yang diperlukan ke kelas Java Anda. Kelas‑kelas ini memberi Anda akses ke model dokumen dan tag khusus Outlook `NoteTask`.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## Panduan Langkah‑demi‑Langkah

### Langkah 1: Siapkan Direktori Dokumen Anda
Tentukan folder yang menyimpan file OneNote Anda. Menggunakan path absolut atau relatif keduanya dapat, tetapi pertahankan string path tetap rapi untuk kemudahan membaca.

```java
String dataDir = "Your Document Directory";
```

### Langkah 2: Muat Dokumen OneNote
Buat instance `Document` dengan menunjuk ke file `.one`. Aspose.Note mem‑parse file menjadi struktur mirip DOM yang dapat Anda telusuri.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Langkah 3: Dapatkan Semua Node RichText
Tugas Outlook disimpan di dalam elemen `RichText`. Ambil setiap node `RichText` sehingga Anda dapat memeriksa tag‑nya.

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

### Langkah 4: Iterasi Setiap Node
Lakukan loop pada setiap node `RichText`, periksa tag‑nya, dan lakukan aksi ketika menemukan `NoteTask`. Kode di bawah ini mencetak properti paling berguna untuk setiap tugas.

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Retrieve properties
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```

**Tip Pro:** Jika Anda hanya membutuhkan sebagian properti, Anda dapat melewatkan yang lain untuk meningkatkan kinerja saat memproses notebook besar.

### Masalah Umum & Solusi
- **No tasks found:** Pastikan halaman OneNote memang berisi tugas Outlook. Mereka muncul sebagai kotak centang dengan ikon Outlook kecil.  
- **Null values:** Beberapa bidang tugas (mis., `CompletedTime`) mungkin `null` jika tugas belum selesai. Hindari `NullPointerException` dengan memeriksa `null` sebelum mencetak.  
- **File not found:** Verifikasi bahwa `dataDir` diakhiri dengan pemisah path yang tepat (`/` atau `\\`) untuk OS Anda.

## Kesimpulan
Selamat! Anda telah mempelajari **cara mengekstrak tugas** dari Outlook di OneNote menggunakan API Aspose.Note Java. Pendekatan ini memberi Anda kontrol programatik penuh atas data tugas, memungkinkan integrasi dengan alat pelaporan khusus, basis data, atau alur kerja bisnis lainnya.

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.Note kompatibel dengan semua versi OneNote?**  
A: Aspose.Note mendukung Microsoft OneNote 2010 dan versi selanjutnya.

**Q: Bisakah saya menggunakan Aspose.Note untuk proyek pribadi maupun komersial?**  
A: Ya, Aspose.Note dapat digunakan untuk proyek pribadi maupun komersial. Kunjungi [here](https://purchase.aspose.com/buy) untuk menjelajahi opsi lisensi.

**Q: Apakah ada versi percobaan gratis untuk Aspose.Note?**  
A: Ya, Anda dapat mengakses versi percobaan gratis [here](https://releases.aspose.com/).

**Q: Bagaimana cara mendapatkan dukungan untuk Aspose.Note?**  
A: Kunjungi [Aspose.Note Forum](https://forum.aspose.com/c/note/28) untuk dukungan komunitas. Untuk bantuan tambahan, pertimbangkan membeli [temporary license](https://purchase.aspose.com/temporary-license/).

**Q: Apakah ada dokumen OneNote contoh yang tersedia untuk pengujian?**  
A: Anda dapat menemukan dokumen contoh dalam dokumentasi Aspose.Note [here](https://reference.aspose.com/note/java/).

---

**Last Updated:** 2026-04-01  
**Tested With:** Aspose.Note for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}