---
title: Buat Tabel dengan Kolom Terkunci di OneNote - Aspose.Note
linktitle: Buat Tabel dengan Kolom Terkunci di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Tingkatkan pengalaman OneNote Anda dengan Aspose.Note untuk Java. Pelajari cara membuat tabel dengan kolom terkunci menggunakan panduan langkah demi langkah. Unduh uji coba gratis Anda sekarang!
weight: 12
url: /id/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat Tabel dengan Kolom Terkunci di OneNote - Aspose.Note

## Perkenalan
OneNote adalah alat canggih untuk mengatur informasi, dan Aspose.Note untuk Java meningkatkan kemampuannya dengan menyediakan cara yang lancar untuk membuat tabel dengan kolom terkunci. Dalam tutorial ini, kami akan memandu Anda melalui proses penggunaan Aspose.Note untuk Java untuk membuat tabel dengan kolom terkunci di OneNote.
## Prasyarat
Sebelum memulai, pastikan Anda memiliki prasyarat berikut:
- [Kit Pengembangan Java (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)diinstal pada mesin Anda.
- [Aspose.Catatan untuk Java](https://downloads.aspose.com/note/java) perpustakaan diunduh dan ditambahkan ke proyek Anda.
## Paket Impor
Di proyek Java Anda, impor paket yang diperlukan untuk bekerja dengan Aspose.Catatan:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Langkah 1: Siapkan Proyek Anda
Mulailah dengan membuat proyek Java baru dan menambahkan perpustakaan Aspose.Note ke classpath Anda. Pastikan proyek Anda dikonfigurasi untuk menggunakan JDK.
## Langkah 2: Inisialisasi Objek Dokumen dan Halaman
```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory";
//Buat objek kelas Dokumen
Document doc = new Document();
// Inisialisasi objek kelas Halaman
Page page = new Page();
```
## Langkah 3: Buat Baris dan Sel Tabel
```java
// Inisialisasi objek kelas TableRow
TableRow row1 = new TableRow();
// Inisialisasi objek kelas TableCell dan atur konten teks
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Inisialisasi objek kelas TableRow
TableRow row2 = new TableRow();
// Inisialisasi objek kelas TableCell dan atur konten teks
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Langkah 4: Buat dan Sesuaikan Tabel
```java
// Inisialisasi objek kelas Tabel
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Tambahkan baris
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Langkah 5: Tambahkan Tabel ke Garis Besar dan Halaman
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Tambahkan simpul tabel
outlineElem.appendChildLast(table);
// Tambahkan simpul elemen garis besar
outline.appendChildLast(outlineElem);
// Tambahkan simpul garis besar
page.appendChildLast(outline);
// Tambahkan simpul halaman
doc.appendChildLast(page);
```
## Langkah 6: Simpan Dokumen
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Selamat! Anda telah berhasil membuat tabel dengan kolom terkunci di OneNote menggunakan Aspose.Note untuk Java.
## Kesimpulan
Dalam tutorial ini, kami menjelajahi proses penggunaan Aspose.Note untuk Java untuk meningkatkan pengalaman OneNote Anda dengan membuat tabel dengan kolom terkunci. Fungsionalitas ini menambahkan lapisan organisasi dan struktur baru pada catatan Anda.
## FAQ
### Apakah Aspose.Note untuk Java kompatibel dengan semua versi Java?
Ya, Aspose.Note untuk Java kompatibel dengan Java 6 dan versi yang lebih baru.
### Bisakah saya menyesuaikan tampilan tabel lebih lanjut?
Sangat! Aspose.Note untuk Java menyediakan opsi ekstensif untuk menyesuaikan tabel, seperti menyesuaikan batas, spasi sel, dan banyak lagi.
### Apakah ada versi uji coba yang tersedia sebelum membeli?
 Ya kamu bisa[unduh uji coba gratis](https://releases.aspose.com/) untuk mengeksplorasi kemampuan Aspose.Note untuk Java.
### Di mana saya dapat menemukan dukungan tambahan atau diskusi komunitas?
 Mengunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28) untuk dukungan dan diskusi komunitas.
### Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Note untuk Java?
 Mengunjungi[Link ini](https://purchase.aspose.com/temporary-license/) untuk mendapatkan izin sementara untuk tujuan pengujian.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
