---
date: 2025-12-09
description: Pelajari cara menyimpan OneNote sebagai PDF dengan teks kaya berformat
  di Java menggunakan Aspose.Note untuk Java. Ikuti panduan langkah demi langkah kami
  untuk otomatisasi dokumen yang mulus.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Simpan OneNote sebagai PDF dengan Teks Kaya yang Diformat di Java
url: /id/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan OneNote sebagai PDF dengan Teks Kaya yang Diformat di Java

## Pendahuluan

Jika Anda perlu **menyimpan OneNote sebagai PDF** sambil mempertahankan pemformatan teks‑kaya, Anda berada di tempat yang tepat. Pada tutorial ini kamiandu Anda membuat dokumen OneNote, menerapkan gaya khusus, dan mengekspornya langsung ke PDF menggunakan Aspose.Note untuk Java. Pada akhir tutorial Anda akan memiliki potongan kode yang dapat digunakan kembali dan dapat dimasukkan ke proyek Java apa pun untuk mengotomatiskan konversi OneNoteke‑PDF yang tampak profesional.

## Jawaban Cepat
- **Apa yang diajarkan tutorial ini?** Cara membuat dokumen OneNote dengan teks yang diformat dan menyimpannya sebagai PDF.  
- **Perpustakaan apa yang diperlukan?** Aspose.Note untuk Java (unduh dari situs resmi).  
- **Apakah saya memerlukan lisensi?** Lisensi sementara cukup untuk pengujian; lisensi penuh diperlukan untuk produksi.  
- **IDE apa yang dapat saya gunakan?** IDE Java apa saja—IntelliJ IDEA, Eclipse, atau NetBeans.  
- **Bisakah saya mengubah format output?** Ya, Aspose.Note mendukung PDF, HTML, PNG, dan lainnya.

## Apa itu “save onenote as pdf”?
Menyimpan OneNote sebagai PDF berarti mengonversi struktur halaman OneNote—termasuk teks, gambar, dan pemformatan—ke dalam file PDF statis yang dapat dilihat di platform mana pun tanpa memerlukan OneNote.

## Mengapa memformat teks kaya di Java?
Menerapkan pemformatan teks kaya (font, warna, gaya) langsung di Java memungkinkan Anda menghasilkan dokumen yang tampak profesional dan sesuai dengan pedoman merek Anda tanpa harus melakukan penyuntingan manual.

## Prasyarat

1. **Java Development Kit (JDK)** – versi terbaru (8 atau lebih tinggi).  
2. **Aspose.Note untuk Java JAR** – unduh dari [tautan unduhan](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau editor lain yang Anda sukai.  

## Impor Paket

Pertama, Anda perlu mengimpor paket yang diperlukan ke proyek Java Anda. Tambahkan pernyataan impor berikut di bagian awal file Java Anda:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Langkah 1: Siapkan Dokumen dan Halaman

Mari kita mulai dengan menginisialisasi objek `Document` dan `Page`:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Langkah 2: Buat Judul dengan Pemformatan

Sekarang, mari buat judul dengan teks yang diformat:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## Langkah 3: Buat Teks Kaya dengan Pemformatan

Selanjutnya, mari buat teks kaya dengan berbagai gaya pemformatan:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## Langkah 4: Tambahkan Elemen ke Halaman dan Dokumen

Sekarang, mari tambahkan judul dan teks kaya ke halaman serta elemen outline:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Langkah 5: Simpan Dokumen

Akhirnya, simpan dokumen OneNote yang telah dibuat sebagai PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **File tidak ditemukan** | Pastikan `dataDir` mengarah ke folder yang ada dan Anda memiliki izin menulis. |
| **Font tidak ditemukan** | Pastikan font yang Anda referensikan (misalnya *Calibri*) terpasang di mesin host. |
| **Lisensi tidak diterapkan** | Muat lisensi Aspose Anda sebelum membuat `Document` untuk menghindari watermark evaluasi. |

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya menyesuaikan gaya font lebih lanjut?**  
J: Ya, Anda dapat mengatur properti tambahan seperti underline, strike‑through, dan perataan teks melalui kelas `TextStyle` dan `ParagraphStyle`.

**T: Apakah Aspose.Note untuk Java kompatibel dengan semua IDE Java?**  
J: Tentu saja. Selama IDE mendukung pengembangan Java standar, Anda dapat menambahkan JAR Aspose.Note ke classpath proyek.

**T: Bisakah saya mengintegrasikan fungsionalitas ini ke aplikasi web?**  
J: Ya, kode yang sama berfungsi pada aplikasi berbasis servlet atau Spring Boot, memungkinkan pembuatan OneNote‑ke‑PDF secara dinamis di sisi server.

**T: Apakah ada persyaratanensi untuk menggunakan Aspose.Note untuk Java?**  
J: Lisensi komersial diperlukan untuk penggunaan produksi. Lisensi sementara tersedia untuk evaluasi dan pengujian.

**T: Apakah Aspose.Note untuk Java mendukung format dokumen lain selain OneNote?**  
J: Ia mendukung PDF, HTML, PNG, JPEG, dan beberapa format ekspor lainnya, memberi Anda fleksibilitas mengonversi halaman OneNote ke format yang Anda butuhkan.

## Kesimpulan

Dalam panduan ini kami menunjukkan cara **menyimpan OneNote sebagai PDF** sambil menerapkan pemformatan teks kaya menggunakan Aspose.Note untuk Java. Dengan mengikuti instruksi langkah‑demi‑langkah, Anda dapat mengotomatiskan pembuatan dokumen OneNote yang rapi dan mengonversinya ke PDF dalam solusi berbasis Java apa pun.

---

**Last Updated:** 2025-12-09  
**Tested With:** Aspose.Note untuk Java 24.11 (terbaru pada saat penulisan)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}