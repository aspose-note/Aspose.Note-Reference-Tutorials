---
date: 2026-02-18
description: Pelajari cara membuat dokumen OneNote, memformat teks kaya, dan menyimpan
  sebagai PDF di Java menggunakan Aspose.Note. Panduan langkah demi langkah untuk
  otomatisasi yang mulus.
linktitle: Create OneNote document and save as PDF in Java
second_title: Aspose.Note Java API
title: Buat dokumen OneNote dan simpan sebagai PDF di Java
url: /id/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat dokumen OneNote dan simpan sebagai PDF di Java

## Pendahuluan

Jika Anda perlu **membuat dokumen onenote** dan **menyimpan OneNote sebagai PDF** sambil mempertahankan pemformatan teks kaya, Anda berada di tempat yang tepat. Pada tutorial ini kami akan membahas cara membuat dokumen OneNote, menerapkan gaya khusus, dan mengekspornya langsung ke PDF menggunakan Aspose.Note untuk Java. Pada akhir tutorial Anda akan memiliki potongan kode yang dapat digunakan kembali dan dapat disisipkan ke proyek Java mana pun untuk mengotomatisasi konversi OneNote‑ke‑PDF yang rapi.

## Jawaban Cepat
- **Apa yang diajarkan tutorial ini?** Cara membuat dokumen OneNote dengan teks bergaya dan menyimpannya sebagai PDF.  
- **Perpustakaan apa yang dibutuhkan?** Aspose.Note untuk Java (dapat diunduh dari situs resmi).  
- **Apakah saya memerlukan lisensi?** Lisensi sementara dapat digunakan untuk pengujian; lisensi penuh diperlukan untuk produksi.  
- **IDE apa yang dapat saya gunakan?** Semua IDE Java—IntelliJ IDEA, Eclipse, atau NetBeans.  
- **Bisakah saya mengubah format output?** Ya, Aspose.Note mendukung PDF, HTML, PNG, dan lainnya.

## Apa itu “save onenote pdf”?
Menyimpan OneNote sebagai PDF berarti mengonversi struktur halaman OneNote—termasuk teks, gambar, dan pemformatan—ke dalam file PDF statis yang dapat dilihat di platform apa pun tanpa memerlukan OneNote.

## Mengapa memformat rich text java?
Menerapkan **format rich text** langsung di Java memungkinkan Anda menghasilkan dokumen yang tampak profesional dan sesuai dengan pedoman merek Anda tanpa harus mengedit secara manual.

## Prasyarat

1. **Java Development Kit (JDK)** – versi terbaru (8 atau lebih tinggi).  
2. **Aspose.Note untuk Java JAR** – unduh dari [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau editor apa pun yang Anda sukai.  

## Impor Paket

Sebelum kita mulai, impor kelas yang diperlukan ke dalam file Java Anda:

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

## Cara membuat dokumen OneNote – Panduan langkah demi langkah

### Langkah 1: Siapkan Dokumen dan Halaman

Inisialisasi objek `Document` dan `Page` yang akan menampung semua konten:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Langkah 2: Buat Judul dengan Pemformatan

Tambahkan elemen judul dan terapkan **set paragraph style** untuk mengontrol tampilannya:

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

### Langkah 3: Buat Rich Text dengan Pemformatan

Di sini kami membangun konten rich‑text menggunakan beberapa objek `TextStyle` untuk mendemonstrasikan **rich text formatting**:

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

### Langkah 4: Tambahkan Elemen ke Halaman dan Dokumen

Gabungkan judul dan rich text ke dalam hierarki halaman:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Langkah 5: Simpan Dokumen – ekspor onenote pdf

Akhirnya, ekspor dokumen OneNote sebagai file PDF:

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
J: Ya, Anda dapat menyesuaikan properti tambahan seperti underline, strike‑through, dan perataan teks melalui kelas `TextStyle` dan `ParagraphStyle`.

**T: Apakah Aspose.Note untuk Java kompatibel dengan semua IDE Java?**  
J: Tentu saja. Selama IDE mendukung pengembangan Java standar, Anda dapat menambahkan JAR Aspose.Note ke classpath proyek.

**T: Bisakah saya mengintegrasikan fungsi ini ke dalam aplikasi web?**  
J: Ya, kode yang sama berfungsi dalam aplikasi berbasis servlet atau Spring Boot, memungkinkan generasi OneNote‑to‑PDF dinamis di sisi server.

**T: Apakah ada persyaratan lisensi untuk menggunakan Aspose.Note untuk Java?**  
J: Lisensi komersial diperlukan untuk penggunaan produksi. Lisensi sementara tersedia untuk evaluasi dan pengujian.

**T: Apakah Aspose.Note untuk Java mendukung format dokumen lain selain OneNote?**  
J: Ia mendukung PDF, HTML, PNG, JPEG, dan beberapa format ekspor lainnya, memberi Anda fleksibilitas untuk mengonversi halaman OneNote ke format yang Anda butuhkan.

## Kesimpulan

Dalam panduan ini kami menunjukkan cara **membuat dokumen OneNote**, menerapkan **pemformatan teks kaya**, dan **menyimpan OneNote sebagai PDF** menggunakan Aspose.Note untuk Java. Dengan mengikuti instruksi langkah demi langkah Anda dapat mengotomatisasi pembuatan dokumen OneNote yang rapi dan mengonversinya ke PDF dalam solusi berbasis Java apa pun.

---

**Terakhir Diperbarui:** 2026-02-18  
**Diuji Dengan:** Aspose.Note untuk Java 24.11 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}