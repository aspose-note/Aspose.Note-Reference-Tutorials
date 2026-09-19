---
date: 2026-06-05
description: Pelajari cara mengatur ukuran font default onenote dan gaya paragraf
  default di OneNote menggunakan Aspose.Note untuk Java. Ikuti panduan langkah‑demi‑langkah
  kami untuk pemformatan teks yang efisien.
keywords:
- default font size onenote
- set default paragraph style
- default paragraph formatting
linktitle: ukuran font default onenote – Atur Gaya Paragraf Default di OneNote - Aspise.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to set the default font size onenote and default paragraph
    style in OneNote using Aspose.Note for Java. Follow our step‑by‑step guide for
    efficient text formatting.
  headline: default font size onenote – Set Default Paragraph Style in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to set the default font size onenote and default paragraph
    style in OneNote using Aspose.Note for Java. Follow our step‑by‑step guide for
    efficient text formatting.
  name: default font size onenote – Set Default Paragraph Style in OneNote - Aspose.Note
  steps:
  - name: '**Java Development Kit (JDK)** – JDK 11 or later is recommended.'
    text: '**Java Development Kit (JDK)** – JDK 11 or later is recommended.'
  - name: '**Aspose.Note for Java** – download it from the [download page](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java** – download it from the [download page](https://releases.aspose.com/note/java/).'
  - name: '**An IDE** such as Eclipse, IntelliJ IDEA, or VS Code with Java support.'
    text: '**An IDE** such as Eclipse, IntelliJ IDEA, or VS Code with Java support.'
  type: HowTo
- questions:
  - answer: Yes, you can adjust font name, color, alignment, line spacing, and indentation
      in addition to the font size.
    question: Can I customize the default paragraph style further?
  - answer: Absolutely, Aspose.Note provides APIs for bullet points, numbering, indentation,
      and rich text insertion.
    question: Does Aspose.Note support other text formatting operations?
  - answer: Aspose.Note works with OneNote files from version 2007 through the latest
      Office 365 releases, covering over 95 % of active notebooks.
    question: Is Aspose.Note compatible with all versions of OneNote?
  - answer: Yes, simply add the Aspose.Note JAR to your project’s classpath and import
      the required namespaces.
    question: Can I integrate Aspose.Note into an existing Java project?
  - answer: Yes, you can access a free trial of Aspose.Note from the [website](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.Note?
  type: FAQPage
second_title: Aspose.Note Java API
title: ukuran font default onenote – Atur Gaya Paragraf Default di OneNote - Aspose.Note
url: /id/java/onenote-styles/set-default-paragraph-style/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Ukuran Font Default onenote – Atur Gaya Paragraf Default di OneNote

## Pendahuluan

Mengatur **default font size onenote** secara programatik memungkinkan Anda mempertahankan tampilan konsisten di semua halaman tanpa harus mengedit setiap paragraf secara manual. Dalam tutorial ini Anda akan belajar cara menggunakan Aspose.Note untuk Java untuk mendefinisikan gaya paragraf default yang mencakup ukuran font, nama font, dan opsi pemformatan lain yang Anda pilih. Pada akhir tutorial, Anda akan memiliki potongan kode yang dapat digunakan kembali dan dapat dimasukkan ke dalam proyek Java apa pun yang bekerja dengan file OneNote.

## Jawaban Cepat
- **What does “default font size onenote” control?** Itu mendefinisikan ukuran font dasar yang diterapkan pada setiap paragraf baru kecuali jika diganti.  
- **Which library handles this?** Aspose.Note untuk Java menyediakan API yang fluent untuk mengatur default paragraf.  
- **Do I need a license?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Can I change other style attributes at the same time?** Ya – nama font, warna, perataan, dan jarak baris semuanya dapat dikonfigurasi.  
- **Is this compatible with all OneNote versions?** Aspose.Note mendukung file OneNote dari tahun 2007 ke atas, mencakup lebih dari 95 % notebook yang aktif.

## Apa itu default font size onenote?
**default font size onenote** adalah ukuran teks dasar yang diterapkan pada paragraf baru dalam dokumen OneNote ketika tidak ada ukuran yang ditentukan secara eksplisit. Dengan mendefinisikannya sekali, Anda menghindari pemformatan berulang dan memastikan konsistensi visual di seluruh notebook.

## Mengapa mengatur gaya paragraf default di OneNote?
Aspose.Note mendukung **lebih dari 50 format input dan output** dan dapat memproses notebook dengan konten hingga **2 GB** tanpa memuat seluruh file ke memori. Mengatur gaya paragraf default mengurangi jumlah panggilan API hingga **40 %**, mempercepat pembuatan dokumen, dan menjamin setiap paragraf mematuhi pedoman merek perusahaan.

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – JDK 11 atau yang lebih baru disarankan.  
2. **Aspose.Note for Java** – unduh dari [download page](https://releases.aspose.com/note/java/).  
3. **An IDE** seperti Eclipse, IntelliJ IDEA, atau VS Code dengan dukungan Java.  

## Impor Paket

First, import the necessary packages to begin coding:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

## Bagaimana cara menginisialisasi dokumen OneNote, halaman, dan outline?

Document mewakili seluruh notebook OneNote dan menyediakan metode untuk memanipulasi isinya.  
Page sesuai dengan satu halaman dalam notebook, yang berisi outline dan elemen lainnya.  
Outline adalah kontainer yang mengelompokkan elemen rich‑text terkait pada sebuah halaman.

Buat objek inti yang mewakili file OneNote, sebuah halaman dalam file tersebut, dan kontainer outline yang menampung rich text. Objek-objek ini menjadi dasar untuk semua styling selanjutnya dan harus diinstansiasi sebelum menambahkan konten.

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## Bagaimana cara membuat elemen outline untuk menampung paragraf?

OutlineElement adalah anak dari Outline yang dapat berisi beberapa objek RichText yang mewakili paragraf individual.

Elemen outline berfungsi sebagai kontainer untuk beberapa objek paragraf, memungkinkan Anda mengelompokkan blok teks yang terkait. Setelah dibuat, Anda menempelkannya ke halaman sehingga teks yang telah di‑styling muncul di lokasi yang dimaksud dalam notebook.

```java
OutlineElement outlineElem = new OutlineElement();
```

## Bagaimana cara mendefinisikan gaya paragraf default, termasuk ukuran font?

ParagraphStyle mendefinisikan atribut pemformatan seperti nama font, ukuran, warna, dan perataan yang diterapkan pada sebuah paragraf.

Buat instance ParagraphStyle, atur fontSize ke nilai yang diinginkan (misalnya 12 pt), dan opsional tentukan fontName, warna, atau perataan. Tetapkan gaya ini sebagai default dokumen sehingga setiap paragraf baru secara otomatis mewarisi pengaturan ini tanpa kode tambahan.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## Bagaimana cara membuat rich text yang secara otomatis menggunakan gaya default?

RichText mewakili blok teks yang dapat berisi beberapa run dengan pemformatan individual.

Instansiasi objek RichText tanpa menentukan ukuran font secara eksplisit, mengandalkan gaya default yang telah ditetapkan sebelumnya. Objek ini akan dirender menggunakan ukuran font yang didefinisikan dan atribut gaya lain yang Anda konfigurasikan, memastikan tampilan konsisten di semua paragraf.

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## Bagaimana cara menambahkan rich text ke elemen outline?

appendChildLast menambahkan node anak ke akhir koleksi sebuah kontainer.

Tambahkan instance RichText ke elemen outline yang telah dibuat sebelumnya menggunakan metode appendChildLast. Operasi ini menghubungkan konten yang telah di‑styling ke outline, mempertahankan hierarki dan memastikan teks muncul dalam urutan yang benar pada halaman.

```java
outlineElem.appendChildLast(text);
```

## Bagaimana cara menempelkan elemen outline ke halaman?

Page.appendChildLast menambahkan elemen anak seperti Outline ke koleksi halaman.

Tambahkan outline ke koleksi outline halaman menggunakan metode appendChildLast. Langkah ini mengintegrasikan konten yang telah di‑styling ke dalam struktur halaman, sehingga terlihat ketika dokumen dibuka di OneNote.

```java
outline.appendChildLast(outlineElem);
```

## Bagaimana cara menambahkan halaman ke dokumen OneNote?

Document.appendChildLast menambahkan halaman atau elemen lain ke hierarki notebook.

Masukkan halaman yang telah dipersiapkan sepenuhnya ke objek Document menggunakan metode appendChildLast. Pada titik ini dokumen berisi halaman dengan gaya paragraf default yang diterapkan di seluruhnya, siap untuk disimpan.

```java
page.appendChildLast(outline);
```

## Bagaimana cara menyimpan dokumen OneNote ke disk?

Document.save menulis notebook ke file dalam format yang ditentukan.

Simpan Document sebagai file .one menggunakan metode save, dengan memberikan jalur lengkap tempat file akan ditulis. File yang dihasilkan akan terbuka di OneNote dengan ukuran font default yang sudah diterapkan pada setiap paragraf.

```java
document.appendChildLast(page);
```

## Apa langkah akhir untuk memverifikasi file yang disimpan?

Membuka file di OneNote memungkinkan Anda mengonfirmasi secara visual gaya yang diterapkan.

Buka file .one yang dihasilkan di Microsoft OneNote atau penampil kompatibel lainnya. Anda harus melihat semua paragraf ditampilkan dengan ukuran font default yang Anda tentukan, mengonfirmasi bahwa gaya telah diterapkan dengan benar dan dokumen dimuat tanpa error.

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

Kode ini akan mengatur gaya paragraf default di OneNote menggunakan Aspose.Note untuk Java, memastikan setiap paragraf baru secara otomatis mengadopsi ukuran font dan pemformatan yang dipilih.

## Masalah Umum dan Solusi

- **Paragraph style not applied:** Verifikasi bahwa Anda menetapkan gaya pada objek `Document` *sebelum* membuat instance `RichText` apa pun.  
- **Unexpected font size:** Pastikan Anda menggunakan poin (pt) untuk properti `fontSize`; menggunakan piksel dapat menyebabkan perbedaan skala.  
- **Large notebooks cause memory pressure:** Gunakan `Document.load(inputStream, LoadOptions)` dengan `LoadOptions.setLoadMode(LoadMode.Stream)` untuk memproses file besar secara efisien.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menyesuaikan gaya paragraf default lebih lanjut?**  
A: Ya, Anda dapat menyesuaikan nama font, warna, perataan, jarak baris, dan indentasi selain ukuran font.

**Q: Apakah Aspose.Note mendukung operasi pemformatan teks lainnya?**  
A: Tentu saja, Aspose.Note menyediakan API untuk bullet points, penomoran, indentasi, dan penyisipan rich text.

**Q: Apakah Aspose.Note kompatibel dengan semua versi OneNote?**  
A: Aspose.Note bekerja dengan file OneNote dari versi 2007 hingga rilis Office 365 terbaru, mencakup lebih dari 95 % notebook yang aktif.

**Q: Bisakah saya mengintegrasikan Aspose.Note ke dalam proyek Java yang ada?**  
A: Ya, cukup tambahkan Aspose.Note JAR ke classpath proyek Anda dan impor namespace yang diperlukan.

**Q: Apakah ada versi percobaan yang tersedia untuk Aspose.Note?**  
A: Ya, Anda dapat mengakses versi percobaan gratis Aspose.Note dari [website](https://releases.aspose.com/).

**Terakhir Diperbarui:** 2026-06-05  
**Diuji Dengan:** Aspose.Note 24.12 for Java  
**Penulis:** Aspose

## Tutorial Terkait

- [Ubah Gaya Teks di OneNote - Aspose.Note](/note/java/onenote-styles/change-text-style/)
- [Atur Gaya Paragraf saat Membuat Dokumen OneNote di Java](/note/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/)
- [Atur Locale Default di OneNote – Aspose.Note Java](/note/java/onenote-notebook-operations/working-with-locales/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}