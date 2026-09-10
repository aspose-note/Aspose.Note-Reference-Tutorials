---
date: 2026-08-18
description: Pelajari cara mengekspor OneNote ke PDF, mengatur paragraph formatting
  di Java, dan menyimpan OneNote sebagai PDF menggunakan Aspose.Note untuk Java.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: Atur Paragraph Style saat Membuat Dokumen OneNote di Java
og_description: Ekspor OneNote ke PDF dan atur paragraph style di Java menggunakan
  Aspose.Note. Ikuti panduan langkah demi langkah ini untuk menghasilkan PDF yang
  halus dengan mudah.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: Ekspor OneNote ke PDF dengan paragraph style di Java (58 chars)
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  headline: How to export OneNote to PDF with paragraph style in Java
  type: TechArticle
- description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  name: How to export OneNote to PDF with paragraph style in Java
  steps:
  - name: set document directory
    text: Define where the generated files will be saved. Replace `"Your Document
      Directory"` with an absolute or relative path on your machine.
  - name: initialize document object
    text: Create the root `Document` that represents the OneNote file. **Definition
      anchor:** `Document` is Aspose.Note’s top‑level object that holds one or more
      pages in memory.
  - name: initialize page object
    text: A OneNote file consists of one or more pages; we start with a single page.
      **Definition anchor:** `Page` represents a single OneNote page, containing outlines,
      images, and other elements.
  - name: initialize outline object
    text: Outlines act as containers for outline elements (think of them as sections).
      **Definition anchor:** `Outline` groups related `OutlineElement` objects and
      defines their visual hierarchy.
  - name: initialize outline element object
    text: Here we **add outline element** that will hold our rich text. **Definition
      anchor:** `OutlineElement` is a leaf node inside an `Outline` that can contain
      text, images, or other media.
  - name: set text style (set paragraph style)
    text: '`ParagraphStyle` defines the font family, size, color, and other typographic
      attributes for a paragraph. The `ParagraphStyle` instance defines the font,
      size, and color—this is where we **set paragraph style** for the upcoming text
      node.'
  - name: initialize rich text object
    text: '`RichText` is the node that stores styled text within an `OutlineElement`.
      We create a `RichText` node, insert a simple string, and attach the previously
      defined style.'
  - name: add rich text node to outline element
    text: Now the styled text lives inside the outline element.
  - name: add outline element node to outline
    text: The outline now contains the element that holds our paragraph.
  - name: add outline node to page
    text: We place the outline onto the page.
  type: HowTo
- questions:
  - answer: Yes, the API supports tables, images, hyperlinks, and advanced layout
      features in addition to plain text.
    question: Can Aspose.Note handle complex formatting such as tables or images?
  - answer: Direct conversion isn’t provided, but you can extract PDF content and
      rebuild a OneNote document using the API.
    question: Is it possible to convert a OneNote PDF back to a OneNote file?
  - answer: Absolutely. Aspose.Note for Java is platform‑independent; just ensure
      a compatible JDK is installed.
    question: Does the library work on Linux/macOS environments?
  - answer: Create additional `Page` and `Outline` objects, then append them to the
      `Document` just like the single‑page example.
    question: How do I add multiple pages or outlines?
  - answer: The official Aspose.Note documentation and the [support forum](https://forum.aspose.com/c/note/28)
      contain many code samples and real‑world scenarios.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- export onenote
- aspose.note
- java document processing
title: Cara mengekspor OneNote ke PDF dengan paragraph style di Java
url: /id/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur gaya paragraf saat membuat dokumen OneNote dalam Java

## Pendahuluan

Mengekspor OneNote ke PDF secara programatis adalah kebutuhan umum untuk mesin pelaporan, layanan pencatatan otomatis, dan pipeline konversi dokumen. Dalam tutorial ini Anda akan belajar cara **export OneNote to PDF**, menerapkan pemformatan paragraf khusus, dan menyimpan file OneNote — semuanya menggunakan Aspose.Note untuk Java. Pada akhir tutorial Anda akan memiliki potongan kode Java siap pakai yang menghasilkan PDF yang rapi dengan tampilan persis yang Anda definisikan.

## Jawaban Cepat
- **Apa arti “set paragraph style”?** Itu menerapkan font, ukuran, warna, dan atribut pemformatan lainnya ke sebuah paragraf teks.  
- **Apakah saya dapat mengekspor hasil ke PDF?** Ya – panduan berakhir dengan menyimpan file OneNote sebagai PDF.  
- **Apakah saya memerlukan lisensi untuk Aspose.Note?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi komersial diperlukan untuk penggunaan produksi.  
- **IDE mana yang didukung?** Semua IDE Java – Eclipse, IntelliJ IDEA, NetBeans, dll.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk dokumen dasar.

## Cara mengekspor OneNote ke PDF dalam Java?

`Document` mewakili file OneNote yang berisi halaman, outline, dan elemen lainnya. Muat dokumen OneNote Anda dengan `new Document()` (atau buat yang baru) dan panggil `document.save("output.pdf", SaveFormat.Pdf)`. Aspose.Note menulis PDF dalam satu langkah, mempertahankan gaya, gambar, dan outline tanpa memerlukan Microsoft OneNote terinstal. Pendekatan langsung ini bekerja di Windows, Linux, dan macOS dengan JDK 1.8+ apa pun.

## Apa itu “set paragraph style” di Aspose.Note?

`ParagraphStyle` adalah kelas yang menyimpan nama font, ukuran, warna, perataan, dan pengaturan tipografi lainnya untuk sebuah paragraf. Dengan melampirkan instance `ParagraphStyle` ke node `RichText` Anda mengontrol secara tepat bagaimana paragraf tersebut muncul di halaman OneNote akhir dan PDF yang diekspor.

## Mengapa mengekspor OneNote ke PDF?

Mengekspor OneNote ke PDF memastikan konsistensi merek dengan mempertahankan font dan warna perusahaan, meningkatkan keterbacaan dengan menjaga tata letak tepat untuk pencetakan atau pengarsipan, dan menyediakan akses lintas platform sehingga penerima dapat melihat dokumen di perangkat apa pun tanpa memerlukan OneNote. Ini juga memberikan manfaat kinerja, memungkinkan dokumen besar diproses dengan cepat.

## Prasyarat

1. **Java Development Kit (JDK) 1.8+** – semua JDK terbaru akan berfungsi.  
2. **Aspose.Note for Java** – unduh JAR terbaru dari [Aspose.Note download page](https://releases.aspose.com/note/java/).  
3. **Sebuah IDE** (Eclipse, IntelliJ IDEA, atau NetBeans) untuk mengkompilasi dan menjalankan contoh.  

> **Tip pro:** Tambahkan JAR Aspose.Note ke classpath proyek Anda melalui Maven (`<dependency>`) atau dengan secara manual merujuk JAR di IDE Anda.

## Impor paket

Pertama, impor namespace yang diperlukan. Blok ini tetap tidak berubah.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> Kelas `ParagraphStyle` adalah kunci untuk **set paragraph style** nanti dalam tutorial.

## Panduan langkah‑demi‑langkah

Berikut adalah penjelasan singkat dari setiap operasi. Blok kode persis seperti contoh asli; kami hanya menambahkan teks penjelasan.

### Langkah 1: atur direktori dokumen
Tentukan di mana file yang dihasilkan akan disimpan.

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur absolut atau relatif di mesin Anda.

### Langkah 2: inisialisasi objek dokumen
Buat `Document` root yang mewakili file OneNote.

```java
Document doc = new Document();
```

**Definisi:** `Document` adalah objek tingkat‑atas Aspose.Note yang menyimpan satu atau lebih halaman dalam memori.

### Langkah 3: inisialisasi objek halaman
File OneNote terdiri dari satu atau lebih halaman; kami memulai dengan satu halaman.

```java
Page page = new Page();
```

**Definisi:** `Page` mewakili satu halaman OneNote, berisi outline, gambar, dan elemen lainnya.

### Langkah 4: inisialisasi objek outline
Outline berfungsi sebagai wadah untuk elemen outline (anggap sebagai bagian).

```java
Outline outline = new Outline();
```

**Definisi:** `Outline` mengelompokkan objek `OutlineElement` terkait dan mendefinisikan hierarki visualnya.

### Langkah 5: inisialisasi objek elemen outline
Di sini kami **menambahkan elemen outline** yang akan menampung teks kaya kami.

```java
OutlineElement outlineElem = new OutlineElement();
```

**Definisi:** `OutlineElement` adalah node daun di dalam `Outline` yang dapat berisi teks, gambar, atau media lainnya.

### Langkah 6: atur gaya teks (set paragraph style)
`ParagraphStyle` mendefinisikan keluarga font, ukuran, warna, dan atribut tipografi lainnya untuk sebuah paragraf.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Instance `ParagraphStyle` menentukan font, ukuran, dan warna — di sinilah kami **set paragraph style** untuk node teks yang akan datang.

### Langkah 7: inisialisasi objek teks kaya
`RichText` adalah node yang menyimpan teks bergaya di dalam `OutlineElement`.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Kami membuat node `RichText`, menyisipkan string sederhana, dan melampirkan gaya yang telah didefinisikan sebelumnya.

### Langkah 8: tambahkan node teks kaya ke elemen outline
```java
outlineElem.appendChildLast(text);
```

Sekarang teks bergaya berada di dalam elemen outline.

### Langkah 9: tambahkan node elemen outline ke outline
```java
outline.appendChildLast(outlineElem);
```

Outline kini berisi elemen yang menampung paragraf kami.

### Langkah 10: tambahkan node outline ke halaman
```java
page.appendChildLast(outline);
```

Kami menempatkan outline ke halaman.

### Langkah 11: tambahkan node halaman ke dokumen
```java
doc.appendChildLast(page);
```

Dokumen kini memiliki satu halaman dengan teks bergaya kami.

### Langkah 12: simpan dokumen (export OneNote PDF)
```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Metode `save` menulis file OneNote dan **exports OneNote to PDF** dalam satu langkah. Anda juga dapat menyimpan sebagai `.one` dengan menggunakan `SaveFormat.One` jika memerlukan format asli.

## Masalah umum & solusi

| Masalah | Alasan | Solusi |
|-------|--------|-----|
| **File tidak ditemukan** | `dataDir` mengarah ke folder yang tidak ada. | Pastikan direktori ada atau buat secara programatis (`new File(dataDir).mkdirs();`). |
| **Blank PDF** | Tidak ada konten yang ditambahkan sebelum menyimpan. | Verifikasi bahwa node `RichText` telah ditambahkan dan gaya telah diatur. |
| **Unsupported font** | Nama font tidak terpasang di sistem. | Gunakan font umum seperti `"Arial"` atau sematkan font dalam proyek. |

## Pertanyaan yang sering diajukan

**Q: Apakah Aspose.Note dapat menangani pemformatan kompleks seperti tabel atau gambar?**  
A: Ya, API mendukung tabel, gambar, hyperlink, dan fitur tata letak lanjutan selain teks biasa.

**Q: Apakah memungkinkan mengonversi PDF OneNote kembali ke file OneNote?**  
A: Konversi langsung tidak disediakan, tetapi Anda dapat mengekstrak konten PDF dan membangun kembali dokumen OneNote menggunakan API.

**Q: Apakah perpustakaan ini bekerja di lingkungan Linux/macOS?**  
A: Tentu saja. Aspose.Note untuk Java bersifat lintas platform; pastikan JDK yang kompatibel terinstal.

**Q: Bagaimana cara menambahkan beberapa halaman atau outline?**  
A: Buat objek `Page` dan `Outline` tambahan, lalu tambahkan ke `Document` seperti contoh satu‑halaman.

**Q: Di mana saya dapat menemukan contoh lebih banyak?**  
A: Dokumentasi resmi Aspose.Note dan [forum dukungan](https://forum.aspose.com/c/note/28) berisi banyak contoh kode dan skenario dunia nyata.

## Kesimpulan

Anda kini telah melihat cara **set paragraph style**, **add outline element**, dan **export OneNote to PDF** menggunakan Aspose.Note untuk Java. Menerapkan teks bergaya sejak awal memastikan PDF akhir terlihat profesional, dan operasi `save` satu kali menangani konversi secara efisien. Perluas fondasi ini dengan gambar, tabel, atau metadata khusus untuk memenuhi kebutuhan spesifik aplikasi Anda.

---

**Last Updated:** 2026-08-18  
**Tested With:** Aspose.Note for Java 26.5 (latest release)  
**Author:** Aspose

## Tutorial Terkait

- [Cara Menyimpan OneNote sebagai PDF dengan Aspose.Note untuk Java](/note/java/onenote-document-loading/load-save-format/)
- [Pelajari Cara Mengonversi OneNote ke PDF dengan Aspose.Note menggunakan PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Atur Gaya Paragraf Default di OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}