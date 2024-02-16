---
title: Simpan Menggunakan Subsistem Font Tertentu di OneNote
linktitle: Simpan Menggunakan Subsistem Font Tertentu di OneNote
second_title: Aspose.Catatan Java API
description: Pelajari cara menyimpan dokumen OneNote menggunakan subsistem font tertentu di Java dengan Aspose.Note. Pastikan representasi font yang konsisten di seluruh platform dengan mudah.
type: docs
weight: 22
url: /id/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---
## Perkenalan

Aspose.Note untuk Java memberikan kemampuan yang kuat untuk bekerja dengan dokumen OneNote. Salah satu persyaratan umum saat bekerja dengan dokumen tersebut adalah memastikan bahwa font dipelihara dengan baik, terutama jika dokumen tersebut akan diekspor atau disimpan dalam format berbeda seperti PDF. Tutorial ini akan memandu Anda melalui proses menyimpan dokumen OneNote sambil menentukan subsistem font, memastikan representasi teks yang konsisten dan akurat di berbagai platform.

## Prasyarat

Sebelum kita masuk ke tutorialnya, pastikan Anda telah menyiapkan prasyarat berikut:

### 1. Kit Pengembangan Java (JDK)

 Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda. Anda dapat mengunduhnya dari[Di Sini](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) jika Anda belum melakukannya.

### 2. Aspose.Note untuk Perpustakaan Java

 Unduh dan atur perpustakaan Aspose.Note untuk Java. Anda dapat mengunduhnya dari[situs web](https://releases.aspose.com/note/java/).

## Paket Impor

Pastikan untuk mengimpor paket yang diperlukan dalam proyek Java Anda:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Sekarang mari kita bagi setiap contoh menjadi beberapa langkah untuk memahami prosesnya dengan lebih baik.

## Langkah 1: Simpan Menggunakan Subsistem Font Dokumen dengan Nama Font Default

Langkah ini menunjukkan cara menyimpan dokumen dalam format PDF menggunakan nama font default yang ditentukan.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Tentukan font default.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Simpan dokumen sebagai PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Pada langkah ini:
- Dokumen OneNote dimuat menggunakan Aspose.Note.
- Font default ditentukan sebagai "Times New Roman".
- Dokumen disimpan dalam format PDF dengan font yang ditentukan.

## Langkah 2: Simpan Menggunakan Subsistem Font Dokumen dengan Font Default dari File

Langkah ini menunjukkan cara menyimpan dokumen dalam format PDF menggunakan font default yang diambil dari file.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Tentukan jalur ke file font.
    String fontFile = "geo_1.ttf";

    // Tentukan font default dari file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Simpan dokumen sebagai PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Pada langkah ini:
- File font "geo_1.ttf" dimuat.
- Font default ditentukan dari file font yang dimuat.
- Dokumen disimpan dalam format PDF dengan font yang ditentukan.

## Langkah 3: Simpan Menggunakan Subsistem Font Dokumen dengan Font Default dari Stream

Langkah ini menunjukkan cara menyimpan dokumen dalam format PDF menggunakan font default yang diambil dari aliran.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Muat dokumen ke Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Tentukan jalur ke file font.
    String fontFile = "geo_1.ttf";

    // Muat file font sebagai aliran.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Tentukan font default dari aliran.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Simpan dokumen sebagai PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Pada langkah ini:
- File font "geo_1.ttf" dimuat sebagai aliran.
- Font default ditentukan dari aliran yang dimuat.
- Dokumen disimpan dalam format PDF dengan font yang ditentukan.

## Kesimpulan

Dalam tutorial ini, kita mempelajari cara menyimpan dokumen OneNote menggunakan subsistem font tertentu di Java menggunakan Aspose.Note. Dengan mengikuti langkah-langkah ini, Anda dapat memastikan representasi font yang konsisten di berbagai platform saat mengekspor atau menyimpan dokumen Anda.

## FAQ

### Q1: Dapatkah saya menentukan font yang berbeda untuk bagian dokumen yang berbeda?

A1: Ya, Anda dapat menentukan font berbeda untuk bagian dokumen berbeda menggunakan Aspose.Note untuk Java.

### Q2: Apakah Aspose.Note kompatibel dengan semua versi OneNote?

A2: Aspose.Note mendukung berbagai versi OneNote, memastikan kompatibilitas di berbagai lingkungan.

### Q3: Bagaimana cara menangani font yang hilang saat menyimpan dokumen?

A3: Aspose.Note menyediakan opsi untuk menentukan font default untuk menangani font yang hilang secara efektif selama penyimpanan dokumen.

### Q4: Dapatkah saya menyesuaikan properti font seperti ukuran dan gaya?

A4: Ya, Anda dapat menyesuaikan properti font seperti ukuran, gaya, dan warna menggunakan Aspose.Note untuk Java.

### Q5: Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?

A5: Ya, Anda bisa mendapatkan uji coba gratis Aspose.Note untuk Java dari situs web.