---
title: Konversi Buku Catatan menjadi Gambar dengan Opsi di OneNote - Aspose.Note
linktitle: Konversi Buku Catatan menjadi Gambar dengan Opsi di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara mengonversi Buku Catatan menjadi gambar dengan opsi menggunakan Aspose.Note untuk Java. Ikuti tutorial langkah demi langkah kami untuk integrasi yang lancar ke dalam aplikasi Java Anda.
weight: 14
url: /id/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi Buku Catatan menjadi Gambar dengan Opsi di OneNote - Aspose.Note

## Perkenalan

Dalam tutorial ini, kita akan mempelajari proses mengubah Notebook menjadi gambar dengan berbagai opsi menggunakan Aspose.Note untuk Java. Aspose.Note adalah API Java canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram, sehingga memungkinkan integrasi tanpa hambatan ke dalam aplikasi Java mereka.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda.
2. Aspose.Note untuk file Java JAR: Unduh perpustakaan Aspose.Note untuk Java dari[Di Sini](https://releases.aspose.com/note/java/) dan sertakan dalam classpath proyek Anda.

## Paket Impor

Pertama, mari impor paket yang diperlukan untuk aplikasi Java kita:

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Langkah 1: Muat Notebook

Untuk memulai, kita perlu memuat buku catatan OneNote yang ingin kita ubah menjadi gambar.

```java
String dataDir = "Your Document Directory";
// Memuat Buku Catatan OneNote
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## Langkah 2: Tetapkan Opsi Penyimpanan

Selanjutnya, kita akan menentukan opsi penyimpanan gambar, termasuk format yang diinginkan (PNG, JPEG, dll.) dan resolusi.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

## Langkah 3: Simpan Buku Catatan sebagai Gambar

Sekarang, kita akan menyimpan buku catatan sebagai gambar dengan opsi yang ditentukan.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Simpan Buku Catatan
notebook.save(dataDir, notebookSaveOptions);
```

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara mengonversi Notebook menjadi gambar dengan berbagai opsi menggunakan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah ini, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam aplikasi Java Anda, membuka kemungkinan untuk memanipulasi file OneNote secara terprogram.

## FAQ

### Q1: Bisakah Aspose.Note menangani file OneNote yang kompleks?

A1: Ya, Aspose.Note dapat menangani file OneNote yang kompleks secara efisien, memungkinkan Anda melakukan berbagai operasi pada file tersebut secara terprogram.

### Q2: Apakah Aspose.Note untuk Java mudah diintegrasikan ke dalam proyek yang sudah ada?

A2: Tentu saja! Aspose.Note untuk Java menyediakan API sederhana yang mudah diintegrasikan ke dalam proyek Java Anda, sehingga menghemat waktu dan tenaga Anda.

### Q3: Dapatkah saya menyesuaikan keluaran gambar saat mengonversi Notebook?

A3: Ya, Aspose.Note memungkinkan Anda menyesuaikan keluaran gambar dengan menentukan opsi seperti resolusi, format, dan lainnya.

### Q4: Apakah Aspose.Note menawarkan dukungan untuk pengembang?

A4: Ya, Aspose memberikan dukungan luar biasa bagi pengembang melalui forum dan dokumentasi mereka, memastikan kelancaran integrasi dan pemecahan masalah.

### Q5: Apakah tersedia uji coba gratis untuk Aspose.Note untuk Java?

 A5: Ya, Anda dapat memanfaatkan uji coba gratis Aspose.Note untuk Java dari[Di Sini](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
