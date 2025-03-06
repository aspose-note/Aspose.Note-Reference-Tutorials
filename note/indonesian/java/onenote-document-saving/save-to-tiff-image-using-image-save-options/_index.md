---
title: Simpan ke Gambar TIFF Menggunakan Opsi Penyimpanan Gambar di OneNote
linktitle: Simpan ke Gambar TIFF Menggunakan Opsi Penyimpanan Gambar di OneNote
second_title: Aspose.Catatan Java API
description: Konversikan dokumen OneNote ke TIFF & kendalikan ukuran & kualitas file! Pilih kompresi Jpeg, PackBits, atau Faks di Java. Dapatkan contoh kode & pelajari caranya! #OneNote #Java #Aspose
weight: 21
url: /id/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan ke Gambar TIFF Menggunakan Opsi Penyimpanan Gambar di OneNote

## Perkenalan

Dalam tutorial ini, Anda akan mempelajari cara menyimpan dokumen ke format gambar TIFF menggunakan metode kompresi berbeda di Aspose.Note untuk Java. Kami akan membahas prasyarat, mengimpor paket, dan memberikan panduan langkah demi langkah untuk setiap metode kompresi.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal berikut:

- Java Development Kit (JDK) diinstal pada sistem Anda.
- Aspose.Note untuk perpustakaan Java diunduh dan dikonfigurasi.
- Pemahaman dasar bahasa pemrograman Java.

## Paket Impor

Pertama, Anda perlu mengimpor paket yang diperlukan ke file Java Anda:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Langkah 1: Simpan ke TIFF Menggunakan Kompresi JPEG

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // Jalur ke direktori dokumen.
    String dataDir = "Your Document Directory";

    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  Muat dokumen menggunakan`Document` kelas.
-  Buat sebuah contoh dari`ImageSaveOptions` dan tentukan jenis kompresi TIFF sebagai JPEG.
- Atur kualitas yang diinginkan (opsional).
- Simpan dokumen ke format TIFF menggunakan opsi yang ditentukan.

## Langkah 2: Simpan ke TIFF Menggunakan Kompresi PackBits

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // Jalur ke direktori dokumen.
    String dataDir = "Your Document Directory";

    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  Muat dokumen menggunakan`Document` kelas.
-  Buat sebuah contoh dari`ImageSaveOptions` dan tentukan jenis kompresi TIFF sebagai PackBits.
- Simpan dokumen ke format TIFF menggunakan opsi yang ditentukan.

## Langkah 3: Simpan ke TIFF Menggunakan Kompresi Faks CCITT Group 3

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // Jalur ke direktori dokumen.
    String dataDir = "Your Document Directory";

    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  Muat dokumen menggunakan`Document` kelas.
-  Buat sebuah contoh dari`ImageSaveOptions` dan tentukan jenis kompresi TIFF sebagai CCITT Group 3 Fax.
- Atur mode warna menjadi hitam dan putih.
- Simpan dokumen ke format TIFF menggunakan opsi yang ditentukan.

## Kesimpulan

Dalam tutorial ini, Anda mempelajari cara menyimpan dokumen ke format gambar TIFF menggunakan metode kompresi berbeda di Aspose.Note untuk Java. Dengan mengikuti panduan langkah demi langkah, Anda dapat memanfaatkan kemampuan Aspose.Note secara efisien untuk memenuhi kebutuhan Anda.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.Note untuk Java untuk mengonversi format dokumen lain ke TIFF?

A1: Ya, Aspose.Note untuk Java mendukung konversi dari berbagai format dokumen ke TIFF, termasuk dokumen OneNote.

### Q2: Apa pentingnya menentukan jenis kompresi saat menyimpan ke TIFF?

A2: Menentukan jenis kompresi memungkinkan Anda mengontrol kualitas gambar dan ukuran file. Metode kompresi yang berbeda menawarkan trade-off antara kualitas dan rasio kompresi.

### Q3: Apakah Aspose.Note untuk Java cocok untuk pemrosesan dokumen secara batch?

A3: Ya, Aspose.Note untuk Java menyediakan API untuk pemrosesan batch, memungkinkan Anda mengotomatiskan tugas konversi dokumen secara efisien.

### Q4: Dapatkah saya menyesuaikan pengaturan kompresi lebih lanjut?

A4: Ya, Anda dapat menyesuaikan parameter seperti kualitas, resolusi, dan metode kompresi untuk menyesuaikan keluaran sesuai kebutuhan Anda.

### Q5: Apakah Aspose.Note untuk Java menawarkan dukungan teknis?

A5: Ya, Aspose menyediakan dukungan teknis yang komprehensif melalui forum dan sistem berbasis tiket.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
