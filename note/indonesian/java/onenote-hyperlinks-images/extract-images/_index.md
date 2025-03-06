---
title: Ekstrak Gambar dari Dokumen OneNote menggunakan Java
linktitle: Ekstrak Gambar dari Dokumen OneNote menggunakan Java
second_title: Aspose.Catatan Java API
description: Pelajari cara mengekstrak gambar dari dokumen OneNote menggunakan Java dengan pustaka Aspose.Note. Ikuti panduan langkah demi langkah kami untuk ekstraksi gambar yang lancar.
weight: 14
url: /id/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekstrak Gambar dari Dokumen OneNote menggunakan Java

## Perkenalan

Dalam tutorial ini, kami akan memandu Anda melalui proses mengekstraksi gambar dari dokumen OneNote menggunakan Java dengan bantuan pustaka Aspose.Note.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal berikut:

1.  Java Development Kit (JDK): Pastikan Anda telah menginstal Java di sistem Anda. Anda dapat mengunduh dan menginstalnya dari[situs web](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Perpustakaan Aspose.Note: Unduh dan sertakan perpustakaan Aspose.Note dalam proyek Java Anda. Anda bisa mendapatkannya dari[tautan unduhan](https://releases.aspose.com/note/java/).

## Paket Impor

Untuk memulai, impor paket yang diperlukan:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Langkah 1: Muat Dokumen

Pertama, muat dokumen OneNote menggunakan Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Langkah 2: Dapatkan Semua Gambar

Selanjutnya, ambil semua gambar dari dokumen:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Langkah 3: Ekstrak Gambar

Ulangi daftar gambar dan simpan setiap gambar ke file:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Kesimpulan

Mengekstrak gambar dari dokumen OneNote menggunakan Java dapat dilakukan secara lancar dengan pustaka Aspose.Note. Dengan mengikuti langkah-langkah yang diuraikan dalam tutorial ini, Anda dapat dengan mudah mengambil gambar dari dokumen Anda untuk diproses atau dianalisis lebih lanjut.

## FAQ

### Q1: Bisakah saya mengekstrak gambar dari dokumen OneNote yang dilindungi kata sandi?

A1: Ya, Aspose.Note juga mendukung ekstraksi gambar dari dokumen yang dilindungi kata sandi.

### Q2: Apakah Aspose.Note kompatibel dengan versi Java yang berbeda?

A2: Aspose.Note kompatibel dengan berbagai versi Java, memastikan fleksibilitas bagi pengembang.

### Q3: Bisakah saya mengekstrak gambar dari beberapa dokumen OneNote dalam satu eksekusi?

A3: Tentu saja, Anda dapat mengulangi beberapa dokumen dan mengekstrak gambar dari masing-masing dokumen menggunakan Aspose.Note.

### Q4: Apakah ada batasan ukuran untuk dokumen OneNote?

A4: Aspose.Note menangani dokumen dengan berbagai ukuran secara efisien, memastikan tidak ada batasan ukuran dokumen untuk ekstraksi gambar.

### Q5: Apakah Aspose.Note mendukung ekstraksi jenis konten lain selain gambar?

A5: Ya, selain gambar, Aspose.Note memungkinkan ekstraksi teks, lampiran, dan tipe konten lainnya dari dokumen OneNote.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
