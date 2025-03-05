---
title: Buat Dokumen dan Sisipkan Gambar di OneNote menggunakan Java
linktitle: Buat Dokumen dan Sisipkan Gambar di OneNote menggunakan Java
second_title: Aspose.Catatan Java API
description: Pelajari cara membuat dokumen OneNote dan menyisipkan gambar menggunakan Aspose.Note untuk Java. Tutorial langkah demi langkah untuk integrasi yang lancar.
type: docs
weight: 12
url: /id/java/onenote-hyperlinks-images/build-doc-insert-image/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menggunakan Aspose.Note untuk Java untuk membuat dokumen OneNote dan menyisipkan gambar ke dalamnya. Aspose.Note adalah Java API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram. Kami akan menguraikan setiap langkah secara mendetail untuk memandu Anda melalui prosesnya.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda.
2.  Aspose.Note untuk perpustakaan Java: Unduh dan instal perpustakaan Aspose.Note untuk Java dari[situs web](https://releases.aspose.com/note/java/).
3. IDE (Lingkungan Pengembangan Terpadu): Gunakan IDE apa pun yang didukung Java seperti IntelliJ IDEA atau Eclipse untuk pengkodean.

## Paket Impor

Mulailah dengan mengimpor paket yang diperlukan dalam kode Java Anda:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Langkah 1: Siapkan Dokumen

Pertama, buat dokumen OneNote baru dan inisialisasi objek yang diperlukan:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Langkah 2: Inisialisasi Garis Besar

Siapkan kerangka dokumen dan tentukan properti offset:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## Langkah 3: Tambahkan Gambar

Muat gambar dan tentukan perataannya:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Langkah 4: Tambahkan Gambar ke Elemen Garis Besar

Lampirkan gambar ke elemen kerangka:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## Langkah 5: Tambahkan Garis Besar dan Node Halaman

Tambahkan kerangka dan simpul halaman ke dokumen:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Langkah 6: Simpan Dokumen

Terakhir, simpan dokumen OneNote:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara membuat dokumen OneNote dan menyisipkan gambar ke dalamnya menggunakan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah ini, Anda bisa mengelola dan memanipulasi file OneNote di aplikasi Java Anda secara efisien.

## FAQ

### Q1: Di mana saya dapat menemukan dokumentasi Aspose.Note untuk Java?

 A1: Anda dapat mengakses dokumentasinya[Di Sini](https://reference.aspose.com/note/java/).

### Q2: Bagaimana cara mengunduh Aspose.Note untuk Java?

 A2: Anda dapat mengunduh Aspose.Note untuk Java dari[Unduh Halaman](https://releases.aspose.com/note/java/).

### Q3: Apakah tersedia uji coba gratis untuk Aspose.Note untuk Java?

 A3: Ya, Anda bisa mendapatkan uji coba gratis dari[situs web](https://releases.aspose.com/).

### Q4: Di mana saya bisa mendapatkan dukungan untuk Aspose.Note untuk Java?

 A4: Untuk dukungan, kunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28).

### Q5: Bisakah saya mendapatkan lisensi sementara untuk Aspose.Note untuk Java?

 A5: Ya, Anda dapat meminta izin sementara[Di Sini](https://purchase.aspose.com/temporary-license/).
