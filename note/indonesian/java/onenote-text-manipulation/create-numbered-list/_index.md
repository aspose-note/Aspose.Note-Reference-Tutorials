---
title: Buat Daftar Bernomor di OneNote - Aspose.Note
linktitle: Buat Daftar Bernomor di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara membuat daftar bernomor dengan mudah di OneNote dengan Aspose.Note untuk Java. Unduh uji coba gratis dan selami dunia pengembangan Java!
type: docs
weight: 14
url: /id/java/onenote-text-manipulation/create-numbered-list/
---
## Perkenalan
Aspose.Note untuk Java memberdayakan pengembang Java untuk bekerja dengan lancar dengan file Microsoft OneNote. Dalam tutorial ini, kami akan memandu Anda melalui proses membuat daftar bernomor di OneNote dengan pustaka Aspose.Note untuk Java yang canggih.
## Prasyarat
Sebelum masuk ke tutorial, pastikan prasyarat berikut sudah ada:
- Menginstal Java Development Kit (JDK) di mesin Anda.
-  Aspose.Note untuk perpustakaan Java diunduh dari[Di Sini](https://releases.aspose.com/note/java/).
## Mengimpor Paket
Pertama, mari impor paket yang diperlukan dalam proyek Java Anda untuk memanfaatkan fungsi Aspose.Note secara maksimal. Sertakan kode berikut dalam proyek Anda:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## Langkah 1: Inisialisasi Objek Dokumen, Halaman, dan Garis Besar
```java
// Direktori Dokumen Anda
String dataDir = "Your Document Directory";
// Buat objek Dokumen, Halaman, dan Garis Besar
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Tetapkan gaya teks default
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Langkah 2: Mengatur Gaya Teks Default
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Langkah 3: Membuat Elemen Garis Besar
Sekarang, mari buat elemen untuk daftar bernomor Anda.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Ulangi untuk elemen lainnya (outlineElem2 dan outlineElem3)
```
## Langkah 4: Menambahkan Elemen Garis Besar ke Garis Besar
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Langkah 5: Menambahkan Garis Besar ke Halaman
```java
page.appendChildLast(outline);
```
## Langkah 6: Menyimpan Dokumen
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Ikuti langkah-langkah ini dengan cermat, dan Anda akan dengan mudah membuat daftar bernomor di OneNote menggunakan Aspose.Note untuk Java.
## Kesimpulan
Dalam tutorial ini, kita menjelajahi proses mulus dalam membuat daftar bernomor di OneNote menggunakan Aspose.Note untuk Java. Fitur perpustakaan yang kuat menjadikannya alat yang sangat berharga bagi pengembang Java yang bekerja dengan file Microsoft OneNote.
## Pertanyaan yang Sering Diajukan
### T: Bisakah saya mengkustomisasi format penomoran di daftar OneNote saya?
J: Tentu saja! Anda dapat menyesuaikan format penomoran menggunakan kelas NumberList yang disediakan oleh Aspose.Note untuk Java.
### T: Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?
 A: Ya, Anda dapat mengunduh uji coba gratis[Di Sini](https://releases.aspose.com/).
### T: Bagaimana cara mendapatkan dukungan untuk Aspose.Note untuk Java?
 J: Kunjungi[Aspose.Catatan untuk forum Java](https://forum.aspose.com/c/note/28) untuk dukungan masyarakat.
### T: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.Note untuk Java?
 J: Lihat[dokumentasi](https://reference.aspose.com/note/java/) untuk informasi yang komprehensif.
### T: Bagaimana cara membeli lisensi Aspose.Note untuk Java?
 A: Anda dapat membeli lisensi[Di Sini](https://purchase.aspose.com/buy).