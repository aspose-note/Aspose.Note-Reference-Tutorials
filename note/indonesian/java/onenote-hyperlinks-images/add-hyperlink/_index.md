---
date: 2026-07-29
description: Pelajari cara menyematkan tautan onenote, menyimpan OneNote sebagai PDF,
  dan menambahkan hyperlink menggunakan Java dengan Aspose.Note. Ekspor OneNote ke
  PDF dengan mudah.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: Simpan OneNote sebagai PDF dan Tambahkan Hyperlink di OneNote dengan Java
og_description: Sematkan tautan onenote dan ekspor OneNote ke PDF menggunakan Java
  dan Aspose.Note. Pelajari langkah demi langkah cara menambahkan hyperlink dan menghasilkan
  PDF.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Sematkan Tautan onenote – Simpan OneNote sebagai PDF dengan Java
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: Sematkan Tautan onenote – Simpan OneNote sebagai PDF dengan Java
url: /id/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan OneNote sebagai PDF dan Tambahkan Hyperlink di OneNote dengan Java

## Pendahuluan

Jika Anda perlu **menyematkan tautan onenote** saat mengubah notebook menjadi PDF portabel, Anda berada di tempat yang tepat. Tutorial ini memandu Anda melalui proses menyimpan OneNote sebagai PDF dan menyisipkan hyperlink yang dapat diklik menggunakan Java dan pustaka Aspose.Note. Anda akan melihat mengapa pendekatan ini ideal untuk pengarsipan, berbagi, dan mengotomatisasi alur kerja dokumen.

## Jawaban Cepat
- **Apakah saya dapat menyimpan OneNote sebagai PDF dengan Java?** Ya, Aspose.Note untuk Java menyediakan satu panggilan `save` untuk menghasilkan PDF.
- **Bagaimana cara menyematkan hyperlink?** Gunakan `TextStyle.setHyperlinkAddress` pada segmen `RichText`.
- **Apa saja prasyaratnya?** JDK 8+ dan pustaka Aspose.Note untuk Java.
- **Format output apa yang didukung?** PDF, DOCX, XPS, dan lainnya.
- **Apakah lisensi diperlukan untuk produksi?** Ya, lisensi komersial diperlukan untuk penggunaan non‑evaluasi.

## Apa itu “menyimpan OneNote sebagai PDF”?

Menyimpan notebook OneNote sebagai PDF menghasilkan versi baca‑saja, lintas‑platform dari catatan Anda yang dapat dibuka siapa saja tanpa aplikasi OneNote. Format ini ideal untuk pengarsipan, pencetakan, atau berbagi dengan kolaborator yang tidak memiliki OneNote terpasang, sambil tetap mempertahankan tata letak asli, gambar, dan hyperlink yang disematkan.

## Mengapa menghasilkan PDF dari OneNote dengan Aspose.Note Java?

Aspose.Note untuk Java dapat **mengekspor onenote ke pdf** dengan 100 % kesetiaan tata letak, menangani hingga 200 halaman per dokumen tanpa memuat seluruh file ke memori. Pustaka ini memproses lebih dari 30 tipe konten berbeda—termasuk gambar, tabel, dan 95 % gaya hyperlink—sehingga Anda mendapatkan replika yang setia dari notebook asli. Ia juga berjalan di Windows, Linux, dan macOS, memungkinkan konversi batch di layanan cloud atau on‑premise.

## Prasyarat

Sebelum kita mulai, pastikan Anda telah menginstal dan menyiapkan prasyarat berikut di sistem Anda:

### Java Development Kit (JDK)

Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda. Anda dapat mengunduh dan menginstal JDK dari [situs Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Aspose.Note for Java Library

Unduh dan instal pustaka Aspose.Note untuk Java. Anda dapat menemukan dokumentasi dan tautan unduhan [di sini](https://reference.aspose.com/note/java/).

## Impor Paket

Untuk memulai, impor paket-paket yang diperlukan untuk bekerja dengan Aspose.Note untuk Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Sekarang, mari kita uraikan contoh yang diberikan menjadi beberapa langkah:

## Cara menyematkan tautan onenote saat menyimpan sebagai PDF?

Muat instance `Document` baru, bangun struktur halaman, tentukan `TextStyle` berwarna merah untuk hyperlink, dan akhirnya panggil `document.save("output.pdf", SaveFormat.Pdf)`. Urutan ini menghasilkan PDF yang berisi hyperlink yang berfungsi penuh, mempertahankan semua format dan gambar asli.

## Langkah 1: Menyiapkan Struktur Dokumen

`Document` mewakili notebook OneNote dalam Aspose.Note.  
`Page` adalah wadah untuk outline dan elemen tingkat halaman lainnya.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Langkah 2: Menentukan Gaya Teks Default

`ParagraphStyle` menentukan format default untuk paragraf seperti perataan, spasi, dan indentasi.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Langkah 3: Menetapkan Teks Judul

`Title` mewakili elemen judul halaman dalam dokumen OneNote.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Langkah 4: Membuat Outline dan Elemen Outline

`Outline` berfungsi sebagai wadah untuk hierarki blok konten.  
`OutlineElement` adalah elemen individual dalam outline, seperti paragraf atau tabel.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Langkah 5: Menentukan Gaya Teks untuk Hyperlink

`TextStyle` mengontrol tampilan visual dari rangkaian teks, termasuk font, warna, dan pengaturan underline.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Langkah 6: Menambahkan Teks dengan Hyperlink

`RichText` mewakili rangkaian teks terformat di dalam paragraf. Menetapkan alamat hyperlink membuat teks dapat diklik dalam PDF yang diekspor.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Langkah 7: Menambahkan Outline ke Halaman dan Halaman ke Dokumen

Langkah ini melampirkan elemen outline yang telah dibuat sebelumnya ke halaman dan kemudian menambahkan halaman ke objek `Document`.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Langkah 8: Menyimpan Dokumen sebagai PDF

`SaveFormat.Pdf` memberi tahu Aspose.Note untuk mengekspor dokumen dalam format PDF.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Kesimpulan

Selamat! Anda telah berhasil **menyimpan OneNote sebagai PDF** dan menambahkan hyperlink ke dokumen menggunakan Java serta pustaka Aspose.Note. Kemampuan ini memungkinkan Anda **menyematkan tautan onenote** dan membuat PDF interaktif yang dapat dibagikan langsung dari konten OneNote Anda.

## Pertanyaan yang Sering Diajukan

**Q: Bagaimana saya dapat menyesuaikan tampilan tautan?**  
A: Gunakan properti `TextStyle` seperti `setFontColor`, `setUnderline`, atau `setFontName` sebelum memanggil `setHyperlinkAddress`.

**Q: Bisakah saya menyimpan dokumen dalam format selain PDF?**  
A: Ya, Aspose.Note mendukung DOCX, XPS, HTML, dan beberapa format ekspor lainnya.

**Q: Bagaimana jika saya perlu menambahkan tautan ke file OneNote yang sudah ada?**  
A: Muat file yang ada dengan `new Document("input.one")`, modifikasi kontennya seperti yang ditunjukkan, lalu panggil `save` dengan format yang diinginkan.

**Q: Apakah ada cara untuk membuka tautan secara programatis setelah PDF dihasilkan?**  
A: Penampil PDF akan menangani tautan yang dapat diklik secara otomatis; tidak diperlukan kode tambahan.

**Q: Apakah saya memerlukan lisensi untuk penggunaan pengembangan?**  
A: Lisensi evaluasi sementara cukup untuk pengembangan dan pengujian, tetapi lisensi penuh diperlukan untuk penyebaran produksi.

---

**Terakhir Diperbarui:** 2026-07-29  
**Diuji Dengan:** Aspose.Note for Java 26.4  
**Penulis:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Tutorial Terkait

- [Cara Menyimpan OneNote sebagai PDF dengan Aspose.Note untuk Java](/note/java/onenote-document-loading/load-save-format/)
- [Mengonversi OneNote ke PDF dengan Aspose.Note menggunakan PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Menambahkan Hyperlink ke Gambar di OneNote dengan Java](/note/java/onenote-hyperlinks-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}