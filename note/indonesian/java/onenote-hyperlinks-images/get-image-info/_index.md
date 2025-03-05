---
title: Dapatkan Info Gambar dari OneNote menggunakan Java
linktitle: Dapatkan Info Gambar dari OneNote menggunakan Java
second_title: Aspose.Catatan Java API
description: Ekstrak info gambar dari dokumen OneNote di Java! Dapatkan dimensi gambar, nama file, & lainnya. Langkah mudah & contoh kode disertakan. #OneNote #Java #Aspose
type: docs
weight: 15
url: /id/java/onenote-hyperlinks-images/get-image-info/
---
## Perkenalan

Dalam bidang pengembangan Java, mengekstraksi informasi dari berbagai format dokumen adalah tugas yang umum. OneNote, platform populer untuk membuat catatan, sering kali berisi gambar di samping teks. Mengambil informasi gambar secara terprogram dari file OneNote menggunakan Java dapat menyederhanakan alur kerja pemrosesan dokumen. Dalam tutorial ini, kita akan mempelajari cara mengekstrak detail gambar dari dokumen OneNote menggunakan Aspose.Note untuk Java.

## Prasyarat

Sebelum kita mendalami penerapannya, pastikan Anda memiliki prasyarat berikut:

### 1. Kit Pengembangan Java (JDK)

Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda. Anda dapat mengunduh dan menginstal JDK terbaru dari[situs web Oracle](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Aspose.Note untuk Perpustakaan Java

 Unduh dan sertakan perpustakaan Aspose.Note untuk Java dalam proyek Anda. Anda dapat memperoleh perpustakaan dari[Unduh Halaman](https://releases.aspose.com/note/java/).

### 3. Dokumen OneNote

Siapkan contoh dokumen OneNote yang berisi gambar. Dokumen ini akan digunakan untuk mengekstrak informasi gambar secara terprogram.

## Paket Impor

Untuk memulai, impor paket yang diperlukan dari Aspose.Note untuk Java:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Mari kita pecahkan kode di atas menjadi petunjuk langkah demi langkah:

## Langkah 1: Atur Direktori Dokumen

```java
String dataDir = "Your Document Directory";
```

 Mengganti`"Your Document Directory"` dengan jalur ke dokumen OneNote Anda.

## Langkah 2: Muat Dokumen

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Muat dokumen OneNote menggunakan pustaka Aspose.Note untuk Java. Pastikan Anda memberikan jalur yang benar ke dokumen Anda.

## Langkah 3: Dapatkan Semua Gambar

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Ambil semua gambar dari dokumen OneNote yang dimuat.

## Langkah 4: Cetak Jumlah Gambar Total

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Cetak jumlah total gambar yang ditemukan dalam dokumen.

## Langkah 5: Melintasi dan Mencetak Informasi Gambar

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Ulangi daftar gambar dan detail cetak seperti lebar, tinggi, dimensi asli, nama file, dan waktu modifikasi terakhir untuk setiap gambar.

## Kesimpulan

Dengan mengikuti langkah-langkah yang diuraikan dalam tutorial ini, Anda dapat secara efektif mengambil informasi gambar dari dokumen OneNote menggunakan Java dengan bantuan perpustakaan Aspose.Note untuk Java. Mengintegrasikan fungsi ini ke dalam aplikasi Anda dapat mengotomatiskan tugas-tugas yang berkaitan dengan pemrosesan dokumen, meningkatkan efisiensi dan produktivitas.

## FAQ

### Q1: Dapatkah Aspose.Note untuk Java menangani format dokumen lain selain OneNote?

A1: Ya, Aspose.Note for Java mendukung berbagai format dokumen, termasuk OneNote, PDF, dan Microsoft Word.

### Q2: Apakah Aspose.Note untuk Java cocok untuk penggunaan pribadi dan komersial?

A2: Ya, Anda dapat menggunakan Aspose.Note untuk Java untuk tujuan pribadi dan komersial.

### Q3: Apakah Aspose.Note untuk Java menawarkan dukungan teknis?

 A3: Ya, dukungan teknis tersedia melalui forum Aspose di[Di Sini](https://forum.aspose.com/c/note/28).

### Q4: Dapatkah saya mencoba Aspose.Note untuk Java sebelum melakukan pembelian?

 A4: Ya, Anda dapat menjelajahi Aspose.Note versi uji coba gratis untuk Java dari[Aspose.Catatan untuk Java](https://releases.aspose.com/note/java/).

### Q5: Bagaimana cara mendapatkan lisensi sementara Aspose.Note untuk Java?
 
 A5: Anda dapat memperoleh lisensi sementara dari[Izin sementara/](https://purchase.aspose.com/temporary-license/).