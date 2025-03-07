---
title: Konversi Dokumen OneNote ke Gambar - Java
linktitle: Konversi Dokumen OneNote ke Gambar - Java
second_title: Aspose.Catatan Java API
description: Pelajari cara mengonversi OneNote menjadi gambar menggunakan Aspose.Note untuk Java. Ikuti langkah mudah, muat dokumen, inisialisasi opsi, dan simpan sebagai PNG.
weight: 14
url: /id/java/onenote-document-loading/convert-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi Dokumen OneNote ke Gambar - Java

## Perkenalan

Dalam tutorial ini, kami akan memandu Anda melalui proses penggunaan Aspose.Note untuk Java untuk mengonversi dokumen OneNote menjadi gambar. Kami akan membagi setiap langkah menjadi petunjuk yang mudah diikuti.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

1. Java Development Kit (JDK) diinstal pada sistem Anda.
2.  Aspose.Note untuk perpustakaan Java. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/java/).

## Paket Impor

Pertama, impor paket yang diperlukan dalam kode Java Anda:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Sekarang mari kita uraikan kode contoh yang diberikan menjadi beberapa langkah:

## Langkah 1: Siapkan Direktori Dokumen

Tentukan direktori tempat dokumen OneNote Anda berada:

```java
String dataDir = "Your Document Directory";
```

 Mengganti`"Your Document Directory"` dengan jalur ke dokumen OneNote Anda.

## Langkah 2: Muat Dokumen

Muat dokumen OneNote ke Aspose.Catatan:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Memastikan`"Sample1.one"` cocok dengan nama file dokumen OneNote Anda.

## Langkah 3: Inisialisasi ImageSaveOptions

 Inisialisasi`ImageSaveOptions` objek untuk menentukan format penyimpanan:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Di sini, kami menyimpan dokumen sebagai gambar PNG. Anda dapat memilih format lain seperti JPEG atau BMP jika diperlukan.

## Langkah 4: Simpan Dokumen sebagai Gambar

Simpan dokumen yang dimuat sebagai gambar:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Baris ini menyimpan dokumen sebagai gambar PNG dengan opsi yang ditentukan.

## Langkah 5: Cetak Konfirmasi

Cetak pesan untuk mengonfirmasi file telah disimpan:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Baris ini memberi tahu Anda tentang konversi yang berhasil dan lokasi file gambar yang disimpan.

## Kesimpulan

Dengan mengikuti langkah-langkah yang diuraikan di atas, Anda dapat dengan mudah mengonversi dokumen OneNote menjadi gambar menggunakan Aspose.Note untuk Java. Ini adalah cara sederhana dan efektif untuk menangani konversi dokumen di aplikasi Java Anda.

## FAQ

### Q1: Bisakah saya mengonversi beberapa dokumen OneNote sekaligus?

A1: Ya, Anda dapat menelusuri daftar dokumen dan melakukan operasi konversi untuk setiap dokumen.

### Q2: Apakah Aspose.Note mendukung format output lain selain gambar?

A2: Ya, Aspose.Note mendukung berbagai format output seperti format PDF, HTML, dan Microsoft Word.

### Q3: Apakah Aspose.Note kompatibel dengan semua versi file OneNote?

A3: Aspose.Note menawarkan kompatibilitas dengan file OneNote yang dibuat di berbagai versi Microsoft OneNote.

### Q4: Dapatkah saya menyesuaikan resolusi gambar keluaran?

A4: Ya, Anda dapat menyesuaikan resolusi dan parameter lainnya menggunakan opsi yang tersedia di Aspose.Note.

### Q5: Apakah Aspose.Note memerlukan konektivitas internet untuk konversi dokumen?

A5: Tidak, Aspose.Note beroperasi secara lokal tanpa memerlukan koneksi internet.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
