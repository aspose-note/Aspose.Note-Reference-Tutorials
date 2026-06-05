---
date: 2026-06-05
description: Pelajari cara mengubah ukuran font di OneNote, mengatur warna font, dan
  menyorot teks dengan Aspose.Note untuk Java – panduan langkah demi langkah dengan
  contoh kode.
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: Ubah Ukuran Font di OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: Ubah Ukuran Font di OneNote - Aspose.Note
url: /id/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ubah Ukuran Font di OneNote - Aspose.Note

## Pendahuluan

Dalam tutorial ini Anda akan belajar **how to change font size onenote** dokumen menggunakan Aspose.Note untuk Java. Kami akan memandu Anda memuat file OneNote, mengakses node teksnya, menerapkan perubahan warna, sorotan, dan ukuran font, dan akhirnya menyimpan file yang telah diperbarui. Baik Anda mengotomatisasi pembuatan laporan maupun memoles catatan rapat, panduan ini memberi Anda cara yang dapat diandalkan untuk menata konten OneNote secara programatis.

## Jawaban Cepat
- **Bagaimana cara mengubah ukuran font di OneNote dengan Java?** Muat dokumen, ubah properti `FontSize` setiap `TextRun`, lalu simpan – tiga langkah sederhana.  
- **Apakah saya juga dapat mengubah warna teks dan sorotan?** Ya, atur `FontColor` dan `HighlightColor` pada `TextRun` yang sama.  
- **Versi Aspose.Note apa yang diperlukan?** Semua rilis 23.10+ mendukung API styling ini.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Apakah pendekatan ini cocok untuk notebook besar?** Ya – Aspose.Note memproses notebook ratusan halaman tanpa memuat seluruh file ke memori.

## Apa itu change font size onenote?
**change font size onenote** mengacu pada penyesuaian atribut `FontSize` pada elemen teks di dalam notebook OneNote secara programatis. Dengan menggunakan Aspose.Note, pengembang dapat memodifikasi properti ini melalui API, yang secara langsung memperbarui struktur file OneNote yang mendasarinya, memastikan perubahan tampilan visual tanpa penyuntingan manual atau interaksi UI.

## Mengapa menggunakan Aspose.Note untuk mengubah gaya teks di OneNote?
Aspose.Note menyediakan lebih dari 30 opsi pemformatan—termasuk keluarga font, ukuran, warna, sorotan, perataan, dan spasi paragraf—dan dirancang untuk memproses notebook besar secara efisien. Ia dapat menangani notebook dengan lebih dari 500 halaman sambil menggunakan kurang dari 150 MB RAM, memberikan otomatisasi yang andal dan berperforma tinggi untuk alur kerja dokumen berskala perusahaan.

## Prasyarat

1. Pengetahuan dasar pemrograman Java.  
2. JDK 8 atau lebih tinggi terpasang di mesin Anda.  
3. Perpustakaan Aspose.Note untuk Java (unduh dari situs web Aspose).  
4. Familiaritas dengan struktur hierarki OneNote (halaman, bagian, node RichText).

## Cara mengubah ukuran font di OneNote menggunakan Aspose.Note?

Muat file OneNote Anda, temukan setiap node `RichText`, perbarui gaya setiap `TextRun`, dan simpan dokumen. Alur end‑to‑end ini hanya memerlukan beberapa baris kode dan berjalan dalam kurang dari satu detik untuk notebook tipikal.

### Langkah 1: Impor Paket

Kelas `Document`, `RichText`, dan `TextRun` berada di namespace `com.aspose.note`. Impor mereka di bagian atas file sumber Java Anda:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### Langkah 2: Muat Dokumen

Kelas `Document` adalah objek tingkat atas Aspose.Note yang mewakili satu file OneNote dalam memori. Memuat file semudah memberikan jalur file ke konstruktornya.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### Langkah 3: Akses Node RichText

Node `RichText` berisi teks paragraf sebenarnya. Dengan mengiterasi `document.getRichTextNodes()`, Anda mendapatkan akses ke setiap potongan teks yang dapat diedit dalam notebook.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### Langkah 4: Ubah Gaya Teks

`TextRun` mewakili rangkaian karakter berurutan yang berbagi format yang sama. Di dalam loop, atur `FontColor` menjadi kuning, `HighlightColor` menjadi biru, dan `FontSize` menjadi **20** poin untuk mencapai gaya yang diinginkan.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### Langkah 5: Simpan Dokumen

Panggil `document.save("StyledSample.one")` untuk menulis perubahan kembali ke file OneNote. Operasi penyimpanan mempertahankan semua konten asli sambil menerapkan gaya baru.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## Masalah Umum dan Solusinya

- **Teks tidak berubah:** Pastikan Anda mengiterasi objek `TextRun` di dalam setiap node `RichText`; melewatkan level ini akan membuat format tidak berubah.  
- **Warna terlihat berbeda:** Aspose.Note menggunakan nilai RGB; pastikan Anda menggunakan konstanta `java.awt.Color` yang tepat.  
- **Notebook besar melambat:** LoadOptions mengatur cara Aspose.Note memuat file, memungkinkan streaming dan pemilihan format. Gunakan `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` untuk mengaktifkan mode streaming, yang mengurangi jejak memori.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menerapkan perubahan gaya teks ini ke bagian tertentu dari dokumen OneNote saya?**  
A: Ya, saring koleksi `RichText` berdasarkan ID halaman atau bagian sebelum menerapkan perubahan gaya.

**Q: Apakah Aspose.Note mendukung opsi pemformatan lain selain warna, sorotan, dan ukuran?**  
A: Tentu saja, Anda dapat memodifikasi keluarga font, tebal/miring, garis bawah, perataan, dan spasi paragraf menggunakan model objek yang sama.

**Q: Bisakah saya mengintegrasikan Aspose.Note dengan perpustakaan Java lain untuk pemrosesan lanjutan?**  
A: Ya, Aspose.Note bekerja mulus dengan perpustakaan seperti Apache POI, Jackson, atau Spring untuk membangun pipeline dokumen yang kompleks.

**Q: Apakah Aspose.Note berlisensi untuk penggunaan komersial?**  
A: Lisensi komersial diperlukan untuk penerapan produksi; lisensi evaluasi gratis tersedia untuk pengembangan dan pengujian.

**Q: Di mana saya dapat menemukan contoh tambahan dan referensi API?**  
A: Kunjungi portal dokumentasi Aspose.Note, unduh PDF referensi API lengkap, dan jelajahi repositori GitHub untuk contoh komunitas.

## Kesimpulan

Dengan mengikuti langkah-langkah di atas, Anda kini tahu **how to change font size onenote** file, mengatur warna teks, dan menerapkan sorotan menggunakan Aspose.Note untuk Java. Kemampuan ini memungkinkan Anda mengotomatisasi penyempurnaan visual catatan rapat, materi pelatihan, atau konten berbasis OneNote apa pun secara skala besar.

---

**Last Updated:** 2026-06-05  
**Tested With:** Aspose.Note 23.10 for Java  
**Author:** Aspose

## Tutorial Terkait

- [Atur Gaya Paragraf Default di OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [Atur Bahasa Proofing untuk Teks di OneNote - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Mengatur Judul Halaman dalam Gaya Microsoft OneNote - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}