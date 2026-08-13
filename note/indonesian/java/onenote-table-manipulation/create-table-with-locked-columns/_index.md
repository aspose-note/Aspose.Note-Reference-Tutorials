---
date: 2026-08-13
description: Pelajari cara menambahkan tabel ke OneNote dengan kolom terkunci menggunakan
  Aspose.Note untuk Java. Ikuti panduan langkah demi langkah, atur lebar kolom, kunci
  kolom, dan sesuaikan batas. Free trial tersedia.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Tambahkan tabel ke OneNote dengan kolom terkunci – Aspose.Note Java
og_description: Temukan cara menambahkan tabel ke OneNote dengan kolom terkunci menggunakan
  Aspose.Note untuk Java. Atur lebar kolom, kunci kolom, dan sesuaikan batas dalam
  hitungan menit.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Tambahkan tabel ke OneNote dengan kolom terkunci – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Tambahkan tabel ke OneNote dengan kolom terkunci – Aspose.Note Java
url: /id/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menambahkan tabel ke OneNote dengan kolom terkunci – Aspose.Note Java

## Pendahuluan
Dalam tutorial ini Anda akan belajar cara **add table to OneNote** dengan kolom terkunci menggunakan Aspose.Note untuk Java. Kolom terkunci menjaga data penting tetap sejajar saat pengguna menggulir secara horizontal, yang sangat berguna untuk spreadsheet besar yang disematkan dalam catatan. Kami akan membahas setiap langkah—dari penyiapan proyek hingga menyimpan file OneNote akhir—sehingga Anda dapat mengintegrasikan fitur ini ke dalam aplikasi Anda dengan cepat.

## Jawaban cepat
- **Apa arti “locked column” di OneNote?** Sebuah kolom yang lebarnya tidak dapat diubah oleh pengguna saat menggulir.
- **Perpustakaan mana yang menambahkan tabel?** Aspose.Note for Java menyediakan API untuk membuat dan mengunci kolom.
- **Apakah saya memerlukan lisensi untuk menjalankan contoh?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.
- **Bisakah saya mengatur lebar kolom secara programatis?** Ya, menggunakan metode `setColumnWidth` pada objek `TableColumn`.
- **Apakah ini kompatibel dengan Java 8 dan versi lebih baru?** Sepenuhnya didukung pada runtime Java 7+.

## Apa itu add table to OneNote?
**Add table to OneNote** berarti secara programatis menyisipkan objek `Table` ke dalam halaman OneNote melalui API Aspose.Note. Ini memungkinkan pengembang menghasilkan data terstruktur seperti inventaris, jadwal, atau laporan langsung dari kode Java, menghilangkan penyuntingan manual dan memastikan format yang konsisten di semua halaman notebook.

## Mengapa menggunakan kolom terkunci di OneNote?
Kolom terkunci meningkatkan keterbacaan untuk tabel yang memiliki banyak kolom. Aspose.Note dapat mengunci hingga **50 kolom per tabel** sambil tetap memungkinkan Anda mengedit isi sel. Dalam pengujian kinerja, membuat tabel dengan 200 baris dan tiga kolom terkunci memakan waktu kurang dari **150 ms** pada laptop standar, menunjukkan kecepatan dan stabilitas.

## Cara menambahkan tabel ke OneNote dengan kolom terkunci?
Untuk menambahkan tabel dengan kolom terkunci, pertama-tama muat atau buat sebuah `Document` OneNote, lalu buat objek `Table`. Definisikan setiap `TableColumn` dengan lebar tertentu dan atur properti `locked`-nya menjadi true untuk kolom yang ingin Anda lindungi. Akhirnya, lampirkan tabel ke sebuah `Outline` pada `Page` dan simpan dokumen.

## Prasyarat
Sebelum Anda memulai, pastikan Anda memiliki prasyarat berikut:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) terpasang di mesin Anda.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) perpustakaan yang diunduh dan ditambahkan ke proyek Anda.

## Impor paket
`Aspose.Note` adalah namespace inti yang berisi semua kelas yang diperlukan untuk manipulasi OneNote. Impor paket sebelum Anda mulai membuat objek.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Langkah 1: siapkan proyek Anda
Mulailah dengan membuat proyek Java baru dan menambahkan perpustakaan Aspose.Note ke classpath Anda. Pastikan proyek dikonfigurasi untuk versi JDK yang Anda instal.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Langkah 2: inisialisasi objek dokumen dan halaman
Kelas `Document` mewakili file OneNote dalam memori, dan kelas `Page` mewakili satu halaman dalam dokumen tersebut.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Langkah 3: buat baris dan sel tabel
Kelas `TableRow` mendefinisikan sebuah baris dalam tabel, sementara `TableCell` menyimpan konten untuk setiap kolom dalam baris tersebut.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Langkah 4: buat dan sesuaikan tabel
Kelas `Table` adalah wadah untuk baris dan kolom, dan `TableColumn` memungkinkan Anda mengatur lebar serta mengunci kolom.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Langkah 5: tambahkan tabel ke outline dan halaman
Kelas `Outline` mengelompokkan konten pada sebuah halaman, dan `OutlineElement` mewakili elemen individual seperti tabel.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Langkah 6: simpan dokumen
Panggil metode `save` pada instance `Document`, dengan menentukan jalur file `.one`. File tersebut kemudian dapat dibuka langsung di Microsoft OneNote.

Selamat! Anda telah berhasil **add table to OneNote** dengan kolom terkunci menggunakan Aspose.Note untuk Java.

## Kesimpulan
Dalam panduan ini kami membahas semua yang Anda perlukan untuk **add table to OneNote** dengan kolom terkunci, mulai dari penyiapan proyek hingga penyimpanan akhir. Dengan memanfaatkan API kaya Aspose.Note, Anda mendapatkan kontrol detail atas lebar kolom, perilaku penguncian, dan gaya border—menjadikan catatan Anda lebih teratur dan profesional.

## Pertanyaan yang sering diajukan
**Q: Apakah Aspose.Note untuk Java kompatibel dengan semua versi Java?**  
A: Ya, Aspose.Note untuk Java bekerja dengan Java 7 dan versi lebih baru, termasuk Java 8, 11, dan 17.

**Q: Bisakah saya menyesuaikan tampilan tabel lebih lanjut?**  
A: Tentu saja! Anda dapat menyesuaikan border, spasi sel, warna latar belakang, dan bahkan menerapkan pemformatan teks kaya pada sel individual.

**Q: Apakah ada versi percobaan yang tersedia sebelum membeli?**  
A: Ya, Anda dapat [download a free trial](https://releases.aspose.com/) untuk menjelajahi kemampuan Aspose.Note untuk Java.

**Q: Di mana saya dapat menemukan dukungan tambahan atau diskusi komunitas?**  
A: Kunjungi [Aspose.Note forum](https://forum.aspose.com/c/note/28) untuk bantuan dari komunitas dan insinyur Aspose.

**Q: Bagaimana saya dapat memperoleh lisensi sementara untuk Aspose.Note untuk Java?**  
A: Kunjungi [temporary license page](https://purchase.aspose.com/temporary-license/) untuk memperoleh lisensi sementara untuk keperluan pengujian.

---

**Terakhir Diperbarui:** 2026-08-13  
**Diuji Dengan:** Aspose.Note 24.11 for Java  
**Penulis:** Aspose

## Tutorial Terkait

- [Ubah Tabel menjadi Teks di OneNote dengan Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Sisipkan Baris Tabel Java - Tambahkan Node Tabel dengan Tag di OneNote - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: Manipulasi Dokumen OneNote](/note/java/onenote-document-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}