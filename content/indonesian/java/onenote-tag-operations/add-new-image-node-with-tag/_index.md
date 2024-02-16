---
title: Tambahkan Node Gambar Baru dengan Tag di OneNote - Aspose.Note
linktitle: Tambahkan Node Gambar Baru dengan Tag di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara menambahkan simpul gambar baru dengan tag di OneNote menggunakan Aspose.Note untuk Java. Tingkatkan keterampilan pemrograman Java Anda dengan mudah.
type: docs
weight: 10
url: /id/java/onenote-tag-operations/add-new-image-node-with-tag/
---
## Perkenalan
Di bidang pemrograman Java, Aspose.Note menonjol sebagai alat yang ampuh untuk menangani dokumen OneNote dengan mudah. Jika Anda ingin meningkatkan keterampilan Anda dan mempelajari cara menambahkan simpul gambar baru dengan tag di OneNote menggunakan Aspose.Note, Anda datang ke tempat yang tepat. Panduan langkah demi langkah ini akan memandu Anda melalui prosesnya, memastikan Anda memahami setiap konsep secara menyeluruh.
## Prasyarat
Sebelum kita masuk ke tutorialnya, pastikan Anda memiliki semua yang Anda butuhkan:
1.  Aspose.Note untuk Java: Pastikan Anda telah menginstal perpustakaan Aspose.Note. Jika belum, Anda dapat mendownloadnya[Di Sini](https://releases.aspose.com/note/java/).
2. Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java yang berfungsi di mesin Anda.
Sekarang kita sudah memiliki prasyaratnya, mari kita lanjutkan ke langkah berikutnya.
## Paket Impor
Di proyek Java Anda, mulailah dengan mengimpor paket yang diperlukan:
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
## Langkah 1: Buat Objek Dokumen
```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory";
// membuat objek kelas Dokumen
Document doc = new Document();
```
## Langkah 2: Inisialisasi Objek Kelas Halaman
```java
// menginisialisasi objek kelas Halaman
Page page = new Page();
```
## Langkah 3: Inisialisasi Objek Kelas Garis Besar
```java
// inisialisasi objek kelas Outline
Outline outline = new Outline();
```
## Langkah 4: Inisialisasi Objek Kelas OutlineElement
```java
// inisialisasi objek kelas OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Langkah 5: Muat dan Sisipkan Gambar
```java
// memuat gambar
Image image = new Image(null, dataDir + "Input.jpg");
// masukkan gambar ke dalam node dokumen
outlineElem.appendChildLast(image);
```
## Langkah 6: Tambahkan Tag Catatan ke Gambar
```java
// tambahkan tag catatan bintang kuning ke gambar
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Langkah 7: Tambahkan Node Elemen Garis Besar
```java
// tambahkan simpul elemen garis besar
outline.appendChildLast(outlineElem);
```
## Langkah 8: Tambahkan Node Garis Besar
```java
// tambahkan simpul garis besar
page.appendChildLast(outline);
```
## Langkah 9: Tambahkan Node Halaman
```java
// tambahkan simpul halaman
doc.appendChildLast(page);
```
## Langkah 10: Simpan Dokumen OneNote
```java
// simpan dokumen OneNote sebagai PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Selamat! Anda telah berhasil menambahkan simpul gambar baru dengan tag di OneNote menggunakan Aspose.Note untuk Java.
## Kesimpulan
 Menguasai Aspose.Note untuk Java membuka kemungkinan menarik dalam manipulasi dokumen OneNote. Dengan mengikuti tutorial ini, Anda memperoleh keterampilan praktis yang dapat diterapkan pada berbagai proyek. Terus jelajahi dokumentasi Aspose.Note[Di Sini](https://reference.aspose.com/note/java/)untuk fitur dan kemungkinan lebih lanjut.
## FAQ
### Di mana saya dapat menemukan dokumentasi Aspose.Note?
 Anda dapat menemukan dokumentasinya[Di Sini](https://reference.aspose.com/note/java/).
### Bagaimana cara mengunduh Aspose.Note untuk Java?
 Anda dapat mengunduhnya dari halaman rilis[Di Sini](https://releases.aspose.com/note/java/).
### Apakah ada uji coba gratis yang tersedia?
 Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).
### Di mana saya bisa mendapatkan dukungan untuk Aspose.Note?
 Kunjungi forum komunitas[Di Sini](https://forum.aspose.com/c/note/28) untuk dukungan.
### Apakah saya memerlukan lisensi sementara?
 Jika diperlukan, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).