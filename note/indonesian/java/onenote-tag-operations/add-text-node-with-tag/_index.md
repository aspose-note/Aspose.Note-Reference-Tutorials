---
date: 2026-09-24
description: Pelajari cara menambahkan tag ke dokumen OneNote dengan Aspose.Note untuk
  Java – buat file OneNote, tambahkan node teks bergaya dengan tag, dan simpan hanya
  dalam beberapa baris kode.
keywords:
- how to add tag
- Aspose.Note Java
- OneNote tag operations
- add text node
lastmod: 2026-09-24
linktitle: Tambahkan Node Teks dengan Tag di OneNote - Aspose.Note
og_description: Pelajari cara menambahkan tag ke dokumen OneNote dengan Aspose.Note
  untuk Java – buat file OneNote, tambahkan node teks bergaya dengan tag, dan simpan
  hanya dalam beberapa baris kode.
og_image_alt: Guide showing how to add a tag to a OneNote document using Aspose.Note
  for Java
og_title: Cara menambahkan tag ke dokumen OneNote dengan Aspose.Note (Java)
schemas:
- author: Aspose
  dateModified: '2026-09-24'
  description: Learn how to add tag to a OneNote document with Aspose.Note for Java
    – create a OneNote file, add a styled text node with a tag, and save it in just
    a few lines of code.
  headline: How to add tag to a OneNote document by adding a text node using Aspose.Note
  type: TechArticle
- questions:
  - answer: It provides a Java API to read, modify, and create OneNote files without
      needing Microsoft Office installed.
    question: What does Aspose.Note do?
  - answer: Roughly 15 lines, including object creation and styling.
    question: How many lines of code to add a tagged text node?
  - answer: A free trial works for development; a license is required for production
      use.
    question: Do I need a license to run the sample?
  - answer: Yes – Aspose.Note offers over 30 built‑in icons such as yellow star, checkmark,
      and heart.
    question: Can I change the tag icon?
  - answer: The library saves the result as a standard *.one* OneNote file.
    question: What format is the output file?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- OneNote
- Aspose.Note
- Java
- tag operations
- document creation
title: Cara menambahkan tag ke dokumen OneNote dengan menambahkan node teks menggunakan
  Aspose.Note
url: /id/java/onenote-tag-operations/add-text-node-with-tag/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menambahkan tag ke dokumen OneNote dengan menambahkan node teks menggunakan Aspose.Note

## Pendahuluan
Dalam tutorial ini Anda akan belajar **cara menambahkan tag** ke dokumen OneNote menggunakan Aspose.Note Java API. Kami akan memandu Anda membuat file OneNote baru, menata paragraf, melampirkan tag bawaan ke teks, dan akhirnya menyimpan notebook dengan satu panggilan `save`. Baik Anda membangun utilitas pencatatan pribadi maupun mengotomatisasi pelaporan perusahaan, langkah-langkah di bawah ini memberi Anda kontrol programatik penuh atas konten OneNote.

## Jawaban Cepat
- **Apa yang dilakukan Aspose.Note?** Ia menyediakan API Java untuk membaca, memodifikasi, dan membuat file OneNote tanpa perlu menginstal Microsoft Office.  
- **Berapa banyak baris kode untuk menambahkan node teks ber-tag?** Sekitar 15 baris, termasuk pembuatan objek dan penataan.  
- **Apakah saya memerlukan lisensi untuk menjalankan contoh?** Versi percobaan gratis cukup untuk pengembangan; lisensi diperlukan untuk penggunaan produksi.  
- **Bisakah saya mengubah ikon tag?** Ya – Aspose.Note menawarkan lebih dari 30 ikon bawaan seperti bintang kuning, centang, dan hati.  
- **Apa format file output?** Perpustakaan menyimpan hasil sebagai file *.one* OneNote standar.

## Apa arti “membuat dokumen OneNote”?
Membuat dokumen OneNote berarti secara programatik menghasilkan file *.one* yang dapat dibuka di Microsoft OneNote. File tersebut berisi halaman, outline, dan elemen rich‑text yang dibangun melalui Aspose.Note API, memungkinkan Anda membuat notebook tanpa aplikasi desktop atau lainnya.

## Mengapa menambahkan node teks dengan tag?
Menambahkan tag ke node teks menyoroti informasi penting dan mengaktifkan navigasi tag bawaan OneNote, yang mempercepat peninjauan dan manajemen tugas. Tag disimpan sebagai metadata, sehingga tetap ada di semua perangkat dan mempertahankan ikon visualnya. Hal ini juga memungkinkan pengguna menyaring atau mencari item ber-tag secara efisien dalam notebook besar.

## Prasyarat
Sebelum memulai tutorial, pastikan Anda memiliki prasyarat berikut:
- Pengetahuan dasar pemrograman Java.  
- Perpustakaan Aspose.Note untuk Java terinstal. Anda dapat mengunduh perpustakaan Aspose.Note untuk Java [download Aspose.Note for Java](https://releases.aspose.com/note/java/).  
- Lingkungan Pengembangan Terintegrasi (IDE) yang disiapkan untuk pengembangan Java.

## Impor paket
Mulailah dengan mengimpor paket yang diperlukan untuk proyek Java Anda. Dalam kode Anda, sertakan impor berikut:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```

## Langkah 1: buat objek dokumen
`Document` adalah kelas tingkat atas yang mewakili file OneNote dalam memori. Setelah diinstansiasi, semua operasi selanjutnya berjalan melalui objek ini.
```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
```

## Langkah 2: inisialisasi objek kelas halaman
`Page` mewakili satu halaman di dalam notebook OneNote. Setiap halaman dapat berisi beberapa outline dan elemen lainnya.
```java
// Initialize Page class object
Page page = new Page();
```

## Langkah 3: inisialisasi objek kelas outline
`Outline` mengelompokkan elemen terkait pada halaman, berfungsi sebagai wadah untuk satu atau lebih objek `OutlineElement`.
```java
// Initialize Outline class object
Outline outline = new Outline();
```

## Langkah 4: inisialisasi objek kelas outlineelement
`OutlineElement` adalah unit visual terkecil yang dapat menampung teks, gambar, atau konten kaya lainnya dalam sebuah outline.
```java
// Initialize OutlineElement class object
OutlineElement outlineElem = new OutlineElement();
```

## Langkah 5: sesuaikan gaya teks
Atur gaya untuk node teks—di sinilah Anda **mengatur gaya paragraf** seperti warna font, nama, dan ukuran. Aspose.Note memungkinkan Anda menentukan warna RGB, keluarga font, dan ukuran poin dalam satu objek `RichTextStyle`.
```java
// Customize text style
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```

## Langkah 6: buat objek richtext
`RichText` adalah kelas yang menyimpan konten string sebenarnya. Setelah membuat objek, Anda menambahkan teks yang diinginkan, yang nantinya akan menerima tag.
```java
// Create RichText object
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```

## Langkah 7: tambahkan tag catatan
`Tag` mewakili penanda visual (misalnya, bintang kuning) yang dapat dilampirkan ke `RichText` mana pun. Aspose.Note menyediakan lebih dari 30 ikon tag bawaan, dan Anda juga dapat mendefinisikan ikon khusus jika diperlukan.
```java
// Add note tag
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```

## Langkah 8: tambahkan node teks
Lampirkan `RichText` (dengan tag-nya) ke `OutlineElement`. Langkah ini mengikat teks yang ditata dan ber-tag ke hierarki outline.
```java
// Add text node
outlineElem.appendChildLast(text);
```

## Langkah 9: tambahkan elemen outline ke outline
Tempatkan `OutlineElement` di dalam wadah `Outline` sehingga menjadi bagian dari struktur visual halaman.
```java
// Add outline element node
outline.appendChildLast(outlineElem);
```

## Langkah 10: tambahkan outline ke halaman
Masukkan `Outline` ke dalam struktur `Page`, menyelesaikan pohon konten halaman.
```java
// Add outline node
page.appendChildLast(outline);
```

## Langkah 11: tambahkan halaman ke dokumen
Tambahkan `Page` yang telah selesai dibangun ke objek `Document`, menyiapkan notebook untuk disimpan.
```java
// Add page node
doc.appendChildLast(page);
```

## Langkah 12: simpan dokumen OneNote
Akhirnya, **simpan file OneNote** ke disk. Ini menyelesaikan alur kerja **membuat dokumen OneNote** dan menghasilkan file *.one* standar yang dapat dibuka di versi Microsoft OneNote terbaru mana pun.
```java
// Save OneNote document
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```

## Mengapa ini penting
Aspose.Note mendukung **lebih dari 50 format input dan output** (termasuk DOCX, PDF, HTML, dan tipe gambar) dan dapat memproses notebook ratusan halaman tanpa memuat seluruh file ke memori, menjadikannya cocok untuk otomasi sisi server dan pembuatan catatan skala besar.

## Masalah umum dan solusi
- **Tag tidak muncul setelah menyimpan** – Pastikan Anda memanggil `richText.getTags().add(tag)` sebelum melampirkan `RichText` ke `OutlineElement`.  
- **Gaya font diabaikan** – Verifikasi bahwa `RichTextStyle` diterapkan pada instance `RichText` sebelum menambahkannya ke outline.  
- **Notebook besar menyebabkan OutOfMemoryError** – Gunakan `Document.setLoadOptions(new LoadOptions(LoadFormat.ONE))` untuk mengaktifkan mode streaming bagi file yang lebih besar dari 500 MB.

## Pertanyaan yang Sering Diajukan
### Q: Bisakah saya menggunakan Aspose.Note untuk Java dengan perpustakaan Java lainnya?
A: Ya, Aspose.Note untuk Java terintegrasi dengan mulus dengan perpustakaan seperti Apache POI, Jackson, atau Spring, memungkinkan Anda menggabungkan pembuatan catatan dengan alur pemrosesan data.

### Q: Apakah tersedia percobaan gratis untuk Aspose.Note untuk Java?
A: Ya, Anda dapat mengakses halaman percobaan gratis Aspose.Note [download Aspose.Note free trial page](https://releases.aspose.com/).

### Q: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.Note untuk Java?
A: Anda dapat mencari dukungan dari komunitas Aspose.Note di forum Aspose.Note [Aspose.Note forum](https://forum.aspose.com/c/note/28).

### Q: Apakah lisensi sementara tersedia untuk Aspose.Note untuk Java?
A: Ya, Anda dapat memperoleh lisensi sementara di halaman pembelian lisensi sementara [temporary license purchase page](https://purchase.aspose.com/temporary-license/).

### Q: Di mana saya dapat menemukan dokumentasi untuk Aspose.Note untuk Java?
A: Dokumentasinya tersedia di dokumentasi Aspose.Note Java API [Aspose.Note Java API documentation](https://reference.aspose.com/note/java/).

**Terakhir Diperbarui:** 2026-09-24  
**Diuji Dengan:** Aspose.Note for Java 24.11  
**Penulis:** Aspose

## Tutorial Terkait

- [Tambahkan Tag ke OneNote – Buat Dokumen OneNote Ber-Tag dengan Aspose.Note](/note/java/onenote-tag-operations/)
- [Hasilkan Template Catatan Rapat dengan Aspose.Note untuk Java – Buat Outline di OneNote](/note/java/onenote-tag-operations/generate-template-for-meeting-notes/)
- [Buat Dokumen OneNote Java – Tutorial Aspose Note Java](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}