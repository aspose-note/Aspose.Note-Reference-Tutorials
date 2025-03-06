---
title: Buat Daftar Bernomor Bahasa Mandarin di OneNote - Aspose.Note
linktitle: Buat Daftar Bernomor Bahasa Mandarin di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Tingkatkan pembuatan dokumen di Java dengan Aspose.Note. Pelajari cara membuat daftar bernomor berbahasa Mandarin di OneNote langkah demi langkah. Jelajahi fitur-fitur canggih Aspose.Note.
weight: 13
url: /id/java/onenote-text-manipulation/create-chinese-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat Daftar Bernomor Bahasa Mandarin di OneNote - Aspose.Note

## Perkenalan
Jika Anda ingin meningkatkan kemampuan pembuatan dokumen di Java, Aspose.Note adalah solusi tepat Anda. Dalam tutorial ini, kami akan memandu Anda melalui proses pembuatan daftar bernomor berbahasa Mandarin di OneNote menggunakan Aspose.Note untuk Java. Pustaka canggih ini memungkinkan Anda memanipulasi dokumen OneNote secara terprogram, memberi Anda kendali penuh atas struktur dan kontennya.
## Prasyarat
Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:
1. Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.
2.  Perpustakaan Aspose.Note: Unduh dan instal perpustakaan Aspose.Note. Anda dapat menemukan tautan unduhan[Di Sini](https://releases.aspose.com/note/java/).
## Paket Impor
Mulailah dengan mengimpor paket yang diperlukan ke proyek Java Anda. Paket-paket ini penting untuk memanfaatkan fitur Aspose.Note untuk Java. Berikut contoh cuplikan kode:
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
Sekarang, mari kita bagi kode menjadi beberapa langkah:
## Langkah 1: Buat Objek Dokumen
```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory";
// membuat objek kelas Dokumen
Document doc = new Document();
```
## Langkah 2: Inisialisasi Objek Halaman
```java
// menginisialisasi objek kelas Halaman
Page page = new Page();
```
## Langkah 3: Inisialisasi Objek Garis Besar
```java
// inisialisasi objek kelas Outline
Outline outline = new Outline();
```
## Langkah 4: Inisialisasi Objek TextStyle
```java
// inisialisasi objek kelas TextStyle dan atur properti pemformatan
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```
## Langkah 5: Inisialisasi Objek OutlineElement dan Terapkan Penomoran
```java
// inisialisasi objek kelas OutlineElement dan terapkan penomoran
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement();
outlineElem2.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text2 = new RichText().append("Second");
text2.setParagraphStyle(defaultStyle);
outlineElem2.appendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement();
outlineElem3.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text3 = new RichText().append("Third");
text3.setParagraphStyle(defaultStyle);
outlineElem3.appendChildLast(text3);
```
## Langkah 6: Tambahkan Elemen Garis Besar
```java
// menambahkan elemen garis besar
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Langkah 7: Tambahkan Node Garis Besar ke Halaman
```java
// tambahkan simpul Garis Besar
page.appendChildLast(outline);
```
## Langkah 8: Tambahkan Node Halaman ke Dokumen
```java
// tambahkan simpul Halaman
doc.appendChildLast(page);
```
## Langkah 9: Simpan Dokumen
```java
// menyimpan dokumen
doc.save(dataDir + "CreateChineseNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateChineseNumberedList_out.pdf");
```
Sekarang Anda telah berhasil membuat daftar bernomor berbahasa Mandarin di OneNote menggunakan Aspose.Note untuk Java!
## Kesimpulan
Dalam tutorial ini, kita telah menjelajahi proses memanfaatkan Aspose.Note untuk Java untuk menghasilkan daftar bernomor berbahasa Mandarin di OneNote. Dengan fitur canggihnya, Aspose.Note memberdayakan pengembang untuk memanipulasi dan menyempurnakan konten dokumen secara terprogram.
## Pertanyaan yang Sering Diajukan
### Apakah Aspose.Note kompatibel dengan IDE Java yang berbeda?
Ya, Aspose.Note kompatibel dengan IDE Java populer seperti Eclipse dan IntelliJ IDEA.
### Bisakah saya menyesuaikan format daftar bernomor?
Sangat. Seperti yang ditunjukkan dalam tutorial, Anda dapat menyesuaikan font, warna, dan ukuran untuk memenuhi kebutuhan spesifik Anda.
### Apakah ada versi uji coba yang tersedia untuk Aspose.Note?
 Ya, Anda dapat menjelajahi versi uji coba[Di Sini](https://releases.aspose.com/).
### Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.Note?
 Lihat dokumentasi[Di Sini](https://reference.aspose.com/note/java/).
### Bagaimana saya bisa mendapatkan dukungan untuk Aspose.Note?
 Kunjungi forum dukungan[Di Sini](https://forum.aspose.com/c/note/28) untuk bantuan atau pertanyaan apa pun.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
