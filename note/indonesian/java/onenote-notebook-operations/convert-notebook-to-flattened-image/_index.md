---
title: Konversi Buku Catatan menjadi Gambar Rata di OneNote - Aspose.Note
linktitle: Konversi Buku Catatan menjadi Gambar Rata di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara mengonversi buku catatan menjadi gambar rata di OneNote menggunakan Aspose.Note untuk Java. Pertahankan semua elemen dalam satu file gambar dengan mudah.
type: docs
weight: 13
url: /id/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---
## Perkenalan

Dalam tutorial ini, kami akan memandu Anda melalui proses mengonversi buku catatan menjadi gambar rata di OneNote menggunakan Aspose.Note untuk Java. Hal ini memungkinkan Anda menyimpan buku catatan Anda sebagai file gambar, memastikan bahwa semua elemen disimpan dalam satu format gambar.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1. Java Development Kit (JDK) diinstal pada sistem Anda.
2.  Aspose.Note untuk perpustakaan Java diunduh dan disiapkan di proyek Java Anda. Anda dapat mengunduh perpustakaan dari[Di Sini](https://releases.aspose.com/note/java/).
3. Pengetahuan dasar tentang pemrograman Java.

## Paket Impor

Untuk memulai, Anda perlu mengimpor paket yang diperlukan dari Aspose.Catatan untuk Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Langkah 1: Siapkan Direktori Dokumen

Pertama, tentukan direktori tempat file notebook Anda berada:

```java
String dataDir = "Your Document Directory";
```

 Mengganti`"Your Document Directory"` dengan jalur ke file buku catatan Anda.

## Langkah 2: Muat Buku Catatan

 Selanjutnya, muat file notebook menggunakan`Notebook` kelas:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Pastikan untuk mengganti`"test.onetoc2"` dengan nama file buku catatan Anda.

## Langkah 3: Atur Opsi Penyimpanan Gambar

Sekarang, atur opsi untuk menyimpan buku catatan sebagai gambar. Kami akan menentukan format penyimpanan sebagai PNG dan mengatur resolusi menjadi 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Anda dapat menyesuaikan resolusi sesuai kebutuhan Anda.

## Langkah 4: Ratakan Buku Catatan

Untuk memastikan bahwa semua elemen diratakan menjadi satu gambar, atur`flatten` pilihan untuk`true`:

```java
saveOptions.setFlatten(true);
```

Hal ini memastikan bahwa gambar yang dihasilkan mempertahankan tata letak buku catatan Anda.

## Langkah 5: Simpan Gambar

Terakhir, simpan buku catatan sebagai gambar yang diratakan:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Mengganti`"ExportImageasFlattenedNotebook_out.png"` dengan nama file keluaran yang Anda inginkan.

## Kesimpulan

Kesimpulannya, menggunakan Aspose.Note untuk Java, Anda bisa dengan mudah mengonversi buku catatan Anda menjadi gambar rata di OneNote. Proses ini memastikan bahwa semua elemen disimpan dalam satu format gambar, sehingga memudahkan berbagi dan melihat.

## FAQ

### Q1: Dapatkah saya menyesuaikan resolusi gambar keluaran?

 A1: Ya, Anda dapat menyesuaikan resolusi sesuai kebutuhan Anda dengan memodifikasi`setResolution` parameter metode.

### Q2: Apakah Aspose.Note mendukung format gambar lain untuk diekspor?

A2: Ya, Aspose.Note mendukung berbagai format gambar seperti PNG, JPEG, BMP, dll., untuk mengekspor buku catatan.

### Q3: Dapatkah saya menyesuaikan gambar keluaran lebih lanjut?

A3: Ya, Aspose.Note menyediakan opsi luas untuk menyesuaikan gambar keluaran, termasuk ukuran halaman, orientasi, dan pengaturan kualitas.

### Q4: Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?

 A4: Ya, Anda bisa mendapatkan versi uji coba gratis dari[Di Sini](https://releases.aspose.com/).

### Q5: Di mana saya dapat menemukan dukungan untuk Aspose.Note untuk Java?

 A5: Anda dapat menemukan dukungan dan sumber daya di forum Aspose.Note[Di Sini](https://forum.aspose.com/c/note/28).