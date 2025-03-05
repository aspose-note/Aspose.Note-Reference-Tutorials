---
title: Atur Resolusi Gambar Output di OneNote - Aspose.Note
linktitle: Atur Resolusi Gambar Output di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara menyesuaikan resolusi gambar di dokumen OneNote menggunakan Aspose.Note untuk Java. Ikuti panduan langkah demi langkah kami untuk kemudahan penerapan
type: docs
weight: 23
url: /id/java/onenote-document-saving/set-output-image-resolution/
---
## Perkenalan

Apakah Anda ingin memanipulasi resolusi gambar dalam dokumen OneNote Anda menggunakan Java? Aspose.Note untuk Java menawarkan solusi tangguh untuk tugas-tugas tersebut. Dalam tutorial ini, kita akan memandu langkah-langkah untuk mengatur resolusi gambar keluaran menggunakan Aspose.Note.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK): Instal JDK di sistem Anda.
2. Aspose.Note for Java: Unduh dan instal Aspose.Note for Java dari[situs web](https://releases.aspose.com/note/java/).
3. Lingkungan Pengembangan Terpadu (IDE): Pilih IDE pilihan Anda seperti Eclipse atau IntelliJ IDEA.

## Paket Impor

Di proyek Java Anda, impor paket Aspose.Note yang diperlukan:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Langkah 1: Muat Dokumen OneNote

Mulailah dengan memuat dokumen OneNote ke dalam aplikasi Java Anda:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 Mengganti`"Your Document Directory"` dengan direktori sebenarnya tempat dokumen OneNote Anda berada.

## Langkah 2: Atur Opsi Penyimpanan Gambar

Tentukan opsi penyimpanan gambar dan tentukan resolusi yang diinginkan:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 Di sini, kami menetapkan resolusinya`120 dpi`. Anda dapat menyesuaikan nilai ini sesuai dengan kebutuhan Anda.

## Langkah 3: Simpan Dokumen dengan Resolusi yang Dimodifikasi

Simpan dokumen dengan resolusi gambar yang diperbarui:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

Ini akan menyimpan dokumen yang dimodifikasi dengan resolusi yang ditentukan.

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi cara mengatur resolusi gambar keluaran di dokumen OneNote menggunakan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah sederhana ini, Anda dapat memanipulasi resolusi gambar secara efisien untuk memenuhi kebutuhan aplikasi Anda.


## FAQ

### Q1: Dapatkah saya menyesuaikan resolusi gambar ke nilai yang lebih tinggi dari 120 dpi?

A1: Ya, Anda dapat mengatur resolusi ke nilai apa pun yang diinginkan sesuai kebutuhan Anda.

### Q2: Apakah Aspose.Note mendukung format gambar lain selain JPEG?

A2: Ya, Aspose.Note mendukung berbagai format gambar seperti PNG, BMP, GIF, dll.

### Q3: Apakah Aspose.Note kompatibel dengan semua versi Java?

A3: Aspose.Note kompatibel dengan Java 1.6 atau versi yang lebih baru.

### Q4: Dapatkah saya memanipulasi aspek gambar lainnya dalam dokumen OneNote menggunakan Aspose.Note?

A4: Ya, Aspose.Note menyediakan fitur lengkap untuk manipulasi gambar, termasuk mengubah ukuran, memotong, dan memutar.

### Q5: Di mana saya bisa mendapatkan dukungan untuk pertanyaan terkait Aspose.Note?

 A5: Anda dapat mencari bantuan dari forum komunitas Aspose.Note[Di Sini](https://forum.aspose.com/c/note/28).