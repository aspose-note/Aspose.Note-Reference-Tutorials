---
date: 2026-08-13
description: Pelajari cara memasukkan gambar ke OneNote, menambahkan tag pada gambar,
  dan menyimpan OneNote sebagai PDF menggunakan Aspose.Note untuk Java.
keywords:
- insert image into onenote
- save onenote as pdf
- java add tag to image
lastmod: 2026-08-13
linktitle: Tambahkan Tag pada Gambar di OneNote – Aspose.Note
og_description: Masukkan gambar ke OneNote, tambahkan tag bintang kuning pada gambar,
  dan ekspor notebook sebagai PDF menggunakan Aspose.Note untuk Java. Ikuti panduan
  langkah demi langkah untuk implementasi cepat.
og_image_alt: Guide showing how to insert an image and tag it in OneNote using Aspose.Note
  for Java
og_title: Masukkan gambar ke OneNote dan tambahkan tag – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to insert image into OneNote, add a tag to the image, and
    save OneNote as PDF using Aspose.Note for Java.
  headline: Insert image into OneNote and add tag with Aspose.Note – Java
  type: TechArticle
- description: Learn how to insert image into OneNote, add a tag to the image, and
    save OneNote as PDF using Aspose.Note for Java.
  name: Insert image into OneNote and add tag with Aspose.Note – Java
  steps:
  - name: create document object
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      OneNote notebook in memory. After instantiation, all subsequent operations flow
      through this object.
  - name: initialize page class object
    text: The `Page` class defines a single page inside the notebook. You can set
      page properties such as title and size before adding content.
  - name: initialize outline class object
    text: The `Outline` class groups related content blocks on a page. Outlines are
      containers for `OutlineElement` objects.
  - name: initialize outline element class object
    text: The `OutlineElement` class represents an individual block inside an outline,
      such as a paragraph, image, or table.
  - name: load and insert image
    text: '*(This step demonstrates **insert image into OneNote**)* The `Image` class
      encapsulates image data to be placed on a OneNote page.'
  - name: add note tag to image
    text: '*(Here we answer **how to add image tag**)* The `NoteTag` class defines
      a visual tag that can be attached to page elements.'
  - name: add outline element node
    text: Attach the image (now tagged) to the outline element so it appears in the
      correct order on the page.
  - name: add outline node
    text: Insert the outline into the page’s collection of outlines.
  - name: add page node
    text: Add the fully built page to the document’s page collection.
  type: HowTo
- questions:
  - answer: You can find the documentation at the **[Aspose.Note Java API reference](https://reference.aspose.com/note/java/)**.
    question: Where can I find Aspose.Note documentation?
  - answer: You can download it from the releases page **[Aspose.Note Java release
      page](https://releases.aspose.com/note/java/)**.
    question: How do I download Aspose.Note for Java?
  - answer: Yes, you can access the free trial at the **[Aspose free trial page](https://releases.aspose.com/)**.
    question: Is there a free trial available?
  - answer: Visit the community forum **[Aspose.Note community forum](https://forum.aspose.com/c/note/28)**
      for support.
    question: Where can I get support for Aspose.Note?
  - answer: If required, you can obtain a temporary license from the **[temporary
      license request page](https://purchase.aspose.com/temporary-license/)**.
    question: Do I need a temporary license?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote automation
- aspose.note java
- insert image into onenote
- add tag to image
- export onenote pdf
title: Masukkan gambar ke OneNote dan tambahkan tag dengan Aspose.Note – Java
url: /id/java/onenote-tag-operations/add-new-image-node-with-tag/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sisipkan gambar ke OneNote dan tambahkan tag dengan Aspose.Note – Java

## Pendahuluan
Jika Anda perlu **menyisipkan gambar ke OneNote** saat bekerja dengan Java, Aspose.Note membuat seluruh proses menjadi sederhana. Dalam tutorial ini kami akan memandu Anda menyisipkan gambar ke halaman OneNote, menerapkan tag bintang kuning pada gambar tersebut, dan akhirnya **menyimpan OneNote sebagai PDF**. Pada akhir tutorial Anda akan melihat secara tepat cara menambahkan tag ke gambar, menyisipkan gambar ke OneNote, dan mengonversi OneNote ke PDF—semua dengan hanya beberapa baris kode.

## Jawaban Cepat
- **Apa arti “menambahkan tag ke gambar”?** Itu menempelkan tag catatan visual (mis., bintang kuning) ke node gambar dalam halaman OneNote.  
- **Perpustakaan mana yang menangani ini?** Aspose.Note untuk Java.  
- **Apakah saya memerlukan lisensi untuk pengujian?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengekspor hasil sebagai PDF?** Ya – gunakan `doc.save(..., SaveFormat.Pdf)` untuk **menyimpan OneNote sebagai PDF**.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk skenario dasar.

## Apa itu “menambahkan tag ke gambar” di OneNote?
Elemen `NoteTag` adalah objek metadata yang secara visual menandai sebuah gambar dengan ikon seperti bintang atau bendera. Elemen ini muncul di UI OneNote dan dapat dicari atau difilter, memungkinkan pengguna dengan cepat menemukan visual yang ditandai dalam notebook besar.

## Mengapa menambahkan tag ke gambar di OneNote?
Menandai gambar memberikan cara ringan untuk menambahkan konteks tanpa mengubah gambar itu sendiri. Tag disimpan sebagai bagian dari struktur halaman, memungkinkan pencarian cepat, petunjuk visual, dan pengkategorian, yang sangat berguna dalam penelitian, pelacakan proyek, atau notebook pendidikan.

- Mengatur konten visual tanpa mengubah gambar itu sendiri.  
- Dengan cepat menemukan grafik penting menggunakan pencarian tag OneNote.  
- Menyediakan konteks (mis., “tinjau nanti”, “referensi penting”) langsung pada halaman.  

## Prasyarat
Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1. Aspose.Note untuk Java: Pastikan Anda telah menginstal pustaka Aspose.Note. Jika belum, Anda dapat mengunduhnya dari **[halaman unduhan Aspose.Note untuk Java](https://releases.aspose.com/note/java/)**.  
2. Lingkungan pengembangan Java: JDK yang berfungsi (versi 8 atau lebih baru) serta IDE atau alat build pilihan Anda.  

Sekarang setelah prasyarat tersedia, mari lanjut ke langkah berikutnya.

## Impor paket
Dalam proyek Java Anda, mulailah dengan mengimpor paket yang diperlukan:

Kelas `Document` mewakili notebook OneNote dalam memori.  
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```

## Bagaimana cara menyisipkan gambar ke OneNote?

Muat file gambar target, buat node `Image`, dan tambahkan ke outline halaman. Penyisipan hanya memerlukan tiga panggilan API dan mempertahankan resolusi gambar asli. Pendekatan ini bekerja untuk format PNG, JPEG, BMP, dan GIF tanpa konversi tambahan.

### Langkah 1: buat objek dokumen
Kelas `Document` adalah objek tingkat atas Aspose.Note yang mewakili notebook OneNote dalam memori. Setelah dibuat, semua operasi selanjutnya berjalan melalui objek ini.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```

### Langkah 2: inisialisasi objek kelas halaman
Kelas `Page` mendefinisikan satu halaman di dalam notebook. Anda dapat mengatur properti halaman seperti judul dan ukuran sebelum menambahkan konten.

```java
// initialize Page class object
Page page = new Page();
```

### Langkah 3: inisialisasi objek kelas outline
Kelas `Outline` mengelompokkan blok konten terkait pada sebuah halaman. Outline adalah wadah untuk objek `OutlineElement`.

```java
// initialize Outline class object
Outline outline = new Outline();
```

### Langkah 4: inisialisasi objek kelas elemen outline
Kelas `OutlineElement` mewakili blok individual di dalam outline, seperti paragraf, gambar, atau tabel.

```java
// initialize OutlineElement class object
OutlineElement outlineElem = new OutlineElement();
```

## Bagaimana cara menambahkan tag ke gambar di OneNote?

Buat objek `NoteTag`, konfigurasikan tipenya (mis., bintang kuning), dan lampirkan ke node `Image` yang telah dibuat sebelumnya. Tag menjadi bagian dari metadata gambar dan ditampilkan secara otomatis oleh OneNote.

Untuk melampirkan tag, buat instance objek `NoteTag`, set `TagIcon`-nya ke simbol yang diinginkan (misalnya, `TagIcon.YellowStar`), dan hubungkan dengan node `Image` menggunakan metode `addTag`. Tag menjadi bagian dari metadata gambar dan ditampilkan secara otomatis oleh OneNote.

### Langkah 5: muat dan sisipkan gambar  
*(Langkah ini menunjukkan **menyisipkan gambar ke OneNote**)  
Kelas `Image` mengenkapsulasi data gambar yang akan ditempatkan pada halaman OneNote.  
```java
// load an image
Image image = new Image(dataDir + "Input.jpg");
// insert image in the document node
outlineElem.appendChildLast(image);
```

### Langkah 6: tambahkan note tag ke gambar  
*(Di sini kami menjawab **cara menambahkan tag gambar**)  
Kelas `NoteTag` mendefinisikan tag visual yang dapat dilampirkan ke elemen halaman.  
```java
// add a yellow star note tag to the image
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```

### Langkah 7: tambahkan node elemen outline
Lampirkan gambar (yang kini ditandai) ke elemen outline sehingga muncul dalam urutan yang tepat pada halaman.

```java
// add outline element node
outline.appendChildLast(outlineElem);
```

### Langkah 8: tambahkan node outline
Sisipkan outline ke dalam koleksi outline halaman.

```java
// add outline node
page.appendChildLast(outline);
```

### Langkah 9: tambahkan node halaman
Tambahkan halaman yang telah selesai dibangun ke koleksi halaman dokumen.

```java
// add page node
doc.appendChildLast(page);
```

## Bagaimana cara menyimpan OneNote sebagai PDF?

Panggil metode `save` pada instance `Document`, dengan menentukan `SaveFormat.Pdf`. Aspose.Note mengonversi semua elemen halaman—termasuk gambar, tag, dan outline—menjadi representasi PDF yang akurat tanpa memerlukan Microsoft OneNote terinstal.

Enum `SaveFormat` menentukan format output untuk menyimpan dokumen.  
```java
// save OneNote document as a PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```

Selamat! Anda telah berhasil **menambahkan tag ke gambar**, menyisipkan gambar ke OneNote, dan mengekspor notebook ke PDF menggunakan Aspose.Note untuk Java.

## Masalah umum dan solusi
| Masalah | Solusi |
|-------|----------|
| **Gambar tidak ditampilkan** | Verifikasi bahwa path di `dataDir + "Input.jpg"` sudah benar dan file dapat diakses. |
| **Tag tidak terlihat** | Pastikan Anda menggunakan versi OneNote yang mendukung note tag (sebagian besar versi terbaru melakukannya). |
| **Output PDF kosong** | Periksa bahwa dokumen berisi setidaknya satu halaman/outline sebelum memanggil `save`. |

## Pertanyaan yang Sering Diajukan

**Q: Di mana saya dapat menemukan dokumentasi Aspose.Note?**  
A: Anda dapat menemukan dokumentasi di **[referensi API Aspose.Note Java](https://reference.aspose.com/note/java/)**.

**Q: Bagaimana cara mengunduh Aspose.Note untuk Java?**  
A: Anda dapat mengunduhnya dari halaman rilis **[halaman rilis Aspose.Note Java](https://releases.aspose.com/note/java/)**.

**Q: Apakah tersedia versi percobaan gratis?**  
A: Ya, Anda dapat mengakses percobaan gratis di **[halaman percobaan gratis Aspose](https://releases.aspose.com/)**.

**Q: Di mana saya dapat mendapatkan dukungan untuk Aspose.Note?**  
A: Kunjungi forum komunitas **[forum komunitas Aspose.Note](https://forum.aspose.com/c/note/28)** untuk dukungan.

**Q: Apakah saya memerlukan lisensi sementara?**  
A: Jika diperlukan, Anda dapat memperoleh lisensi sementara dari **[halaman permintaan lisensi sementara](https://purchase.aspose.com/temporary-license/)**.

## Kesimpulan
Menguasai Aspose.Note untuk Java membuka peluang menarik dalam manipulasi dokumen OneNote. Dengan mengikuti tutorial ini, Anda telah belajar **cara menambahkan tag ke gambar**, **menyisipkan gambar ke OneNote**, dan **menyimpan OneNote sebagai PDF**—keterampilan yang dapat Anda terapkan pada berbagai proyek otomasi. Terus jelajahi dokumentasi Aspose.Note di **[dokumentasi Aspose.Note Java](https://reference.aspose.com/note/java/)** untuk fitur dan kemungkinan yang lebih maju.

---

**Last Updated:** 2026-08-13  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose

## Tutorial Terkait

- [Cara menambahkan gambar ke OneNote menggunakan Java – Membuat Dokumen dan Menyisipkan Gambar](/note/java/onenote-hyperlinks-images/build-doc-insert-image/)
- [Cara Menyimpan OneNote sebagai PDF dengan Aspose.Note untuk Java](/note/java/onenote-document-loading/load-save-format/)
- [Sisipkan Baris Tabel Java - Tambahkan Node Tabel dengan Tag di OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}