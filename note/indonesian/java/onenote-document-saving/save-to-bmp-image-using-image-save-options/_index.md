---
title: Simpan ke Gambar BMP Menggunakan Opsi Penyimpanan Gambar di OneNote
linktitle: Simpan ke Gambar BMP Menggunakan Opsi Penyimpanan Gambar di OneNote
second_title: Aspose.Catatan Java API
description: Pelajari cara menyimpan dokumen OneNote ke gambar BMP secara terprogram menggunakan Aspose.Note untuk Java. Panduan langkah demi langkah dengan contoh kode.
type: docs
weight: 16
url: /id/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
---
## Perkenalan

Aspose.Note untuk Java adalah perpustakaan canggih yang memungkinkan pengembang Java bekerja dengan file Microsoft OneNote secara terprogram. Dengan Aspose.Note untuk Java, Anda dapat membuat, memanipulasi, dan mengonversi dokumen OneNote dengan lancar. Dalam tutorial ini, kita akan mempelajari cara menyimpan dokumen OneNote ke gambar BMP menggunakan Opsi Penyimpanan Gambar yang disediakan oleh Aspose.Note untuk Java.

## Prasyarat

Sebelum melanjutkan tutorial ini, pastikan Anda memiliki hal berikut:

1. Pengetahuan dasar bahasa pemrograman Java.
2. Menginstal JDK (Java Development Kit) di sistem Anda.
3. Lingkungan Pengembangan Terintegrasi (IDE) seperti Eclipse atau IntelliJ IDEA.
4.  Aspose.Note untuk perpustakaan Java. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/java/).

## Paket Impor

Pertama, Anda perlu mengimpor paket yang diperlukan dari Aspose.Note untuk Java agar dapat memanfaatkan fungsinya. Tambahkan pernyataan import berikut ke file Java Anda:

```java
import com.aspose.note.*;
import java.io.IOException;
```

Sekarang, mari kita bagi contoh yang diberikan menjadi beberapa langkah:

## Langkah 1: Muat Dokumen

```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory";

// Muat dokumen ke Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Pada langkah ini, kami menentukan jalur ke direktori tempat dokumen OneNote kami berada. Kemudian, kami memuat dokumen menggunakan`Document` kelas yang disediakan oleh Aspose.Note untuk Java.

## Langkah 2: Simpan ke Gambar BMP

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Simpan dokumennya.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

 Pada langkah ini, kami menentukan jalur keluaran untuk gambar BMP yang akan dihasilkan dari dokumen OneNote. Kami menggunakan`save` metode`Document` kelas untuk menyimpan dokumen sebagai gambar BMP, menyediakan jalur keluaran dan instance`ImageSaveOptions` dengan yang diinginkan`SaveFormat` (pada kasus ini,`SaveFormat.Bmp`).

## Kesimpulan

Dalam tutorial ini, kita mempelajari cara menyimpan dokumen OneNote ke gambar BMP menggunakan Aspose.Note untuk Java. Dengan mengikuti panduan langkah demi langkah, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam aplikasi Java Anda, memungkinkan Anda memanipulasi dokumen OneNote dengan mudah.

## FAQ

### Q1: Bisakah saya menyimpan dokumen OneNote ke format gambar lain selain BMP?

A1: Ya, Anda dapat menyimpan dokumen OneNote ke berbagai format gambar seperti JPEG, PNG, GIF, dan TIFF menggunakan Aspose.Note untuk Java.

### Q2: Apakah Aspose.Note untuk Java mendukung konversi antara format dokumen yang berbeda?

A2: Ya, Aspose.Note untuk Java mendukung konversi antara dokumen OneNote dan format lain seperti PDF, DOCX, HTML, dan lainnya.

### Q3: Apakah Aspose.Note untuk Java kompatibel dengan OneNote versi terbaru?

A3: Ya, Aspose.Note untuk Java diperbarui secara berkala untuk memastikan kompatibilitas dengan versi terbaru OneNote.

### Q4: Dapatkah saya memanipulasi konten dokumen OneNote secara terprogram menggunakan Aspose.Note untuk Java?

A4: Ya, Anda bisa memanipulasi konten, struktur, dan pemformatan dokumen OneNote secara terprogram menggunakan Aspose.Note untuk Java.

### Q5: Apakah Aspose.Note untuk Java menyediakan dukungan teknis?

 A5: Ya, Aspose menyediakan dukungan teknis untuk produknya. Anda dapat mengunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28) untuk bantuan.