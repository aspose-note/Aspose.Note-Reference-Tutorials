---
title: Tambahkan Node Teks dengan Tag di OneNote - Aspose.Note
linktitle: Tambahkan Node Teks dengan Tag di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Jelajahi cara menambahkan node teks dengan tag di OneNote menggunakan Aspose.Note untuk Java. Mudah, efisien, dan ramah pengembang. Unduh perpustakaannya sekarang!
weight: 13
url: /id/java/onenote-tag-operations/add-text-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tambahkan Node Teks dengan Tag di OneNote - Aspose.Note

## Perkenalan
Dalam tutorial ini, kita akan mempelajari cara menambahkan simpul teks dengan tag di OneNote menggunakan Aspose.Note untuk Java. Aspose.Note adalah pustaka Java canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram. Menambahkan node teks dengan tag merupakan persyaratan umum dalam pemrosesan dokumen, dan Aspose.Note menyederhanakan tugas ini.
## Prasyarat
Sebelum kita masuk ke tutorialnya, pastikan Anda memiliki prasyarat berikut:
- Pengetahuan dasar tentang pemrograman Java.
-  Aspose.Note untuk perpustakaan Java diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/note/java/).
- Lingkungan Pengembangan Terpadu (IDE) yang disiapkan untuk pengembangan Java.
## Paket Impor
Mulailah dengan mengimpor paket yang diperlukan untuk proyek Java Anda. Dalam kode Anda, sertakan impor berikut:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## Langkah 1: Buat Objek Dokumen
Inisialisasi objek kelas Dokumen untuk mewakili dokumen OneNote:
```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory";
//Buat objek kelas Dokumen
Document doc = new Document();
```
## Langkah 2: Inisialisasi Objek Kelas Halaman
Inisialisasi objek kelas Halaman untuk mewakili halaman dalam dokumen:
```java
// Inisialisasi objek kelas Halaman
Page page = new Page();
```
## Langkah 3: Inisialisasi Objek Kelas Garis Besar
Inisialisasi objek kelas Outline untuk menyusun konten dalam halaman:
```java
// Inisialisasi objek kelas Outline
Outline outline = new Outline();
```
## Langkah 4: Inisialisasi Objek Kelas OutlineElement
Inisialisasi objek kelas OutlineElement untuk mewakili elemen dalam kerangka:
```java
// Inisialisasi objek kelas OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Langkah 5: Sesuaikan Gaya Teks
Siapkan gaya untuk node teks, seperti warna font, nama, dan ukuran:
```java
// Sesuaikan gaya teks
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## Langkah 6: Buat Objek RichText
Buat objek RichText dan tambahkan teks yang diinginkan ke dalamnya:
```java
// Buat objek RichText
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## Langkah 7: Tambahkan Tag Catatan
Tambahkan tag catatan, seperti bintang kuning, ke teks:
```java
// Tambahkan tag catatan
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## Langkah 8: Tambahkan Node Teks
Tambahkan simpul teks ke elemen kerangka:
```java
// Tambahkan simpul teks
outlineElem.appendChildLast(text);
```
## Langkah 9: Tambahkan Elemen Garis Besar ke Garis Besar
Tambahkan elemen kerangka ke kerangka:
```java
// Tambahkan simpul elemen garis besar
outline.appendChildLast(outlineElem);
```
## Langkah 10: Tambahkan Garis Besar ke Halaman
Tambahkan kerangka ke halaman:
```java
// Tambahkan simpul garis besar
page.appendChildLast(outline);
```
## Langkah 11: Tambahkan Halaman ke Dokumen
Tambahkan halaman ke dokumen:
```java
// Tambahkan simpul halaman
doc.appendChildLast(page);
```
## Langkah 12: Simpan Dokumen OneNote
Simpan dokumen OneNote ke direktori yang ditentukan:
```java
// Simpan dokumen OneNote
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
Selamat! Anda telah berhasil menambahkan simpul teks dengan tag di OneNote menggunakan Aspose.Note untuk Java.
## Kesimpulan
Dalam tutorial ini, kita membahas proses langkah demi langkah menambahkan simpul teks dengan tag di OneNote menggunakan pustaka Aspose.Note untuk Java. Pustaka canggih ini menyederhanakan tugas pemrosesan dokumen, sehingga memudahkan pengembang untuk memanipulasi file OneNote secara terprogram.
## Pertanyaan yang Sering Diajukan
### T: Dapatkah saya menggunakan Aspose.Note untuk Java dengan pustaka Java lainnya?
J: Ya, Aspose.Note untuk Java dapat diintegrasikan secara lancar dengan pustaka Java lainnya untuk meningkatkan kemampuan pemrosesan dokumen.
### T: Apakah tersedia uji coba gratis untuk Aspose.Note untuk Java?
 A: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).
### T: Bagaimana cara mendapatkan dukungan untuk Aspose.Note untuk Java?
J: Anda dapat mencari dukungan dari komunitas Aspose.Note[forum](https://forum.aspose.com/c/note/28).
### T: Apakah lisensi sementara tersedia untuk Aspose.Note untuk Java?
 A: Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).
### T: Di mana saya dapat menemukan dokumentasi Aspose.Note untuk Java?
 J: Dokumentasinya tersedia[Di Sini](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
