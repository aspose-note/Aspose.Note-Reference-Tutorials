---
title: Simpan ke Gambar JPEG Menggunakan Format Simpan di OneNote
linktitle: Simpan ke Gambar JPEG Menggunakan Format Simpan di OneNote
second_title: Aspose.Catatan Java API
description: Ubah dokumen OneNote menjadi gambar JPEG dengan mudah! Tutorial Java ini menunjukkan cara menggunakan Aspose.Note. Konversi & otomatisasi dengan contoh kode! #OneNote #Java #Aspose
weight: 18
url: /id/java/onenote-document-saving/save-to-jpeg-image-using-save-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan ke Gambar JPEG Menggunakan Format Simpan di OneNote

## Perkenalan

Dalam tutorial ini, kita akan mempelajari proses menyimpan dokumen ke format gambar JPEG menggunakan Aspose.Note untuk Java. Aspose.Note adalah Java API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote secara terprogram, memungkinkan berbagai operasi seperti konversi, manipulasi, dan ekstraksi konten.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Lingkungan Pengembangan Java: Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda.
2.  Aspose.Note untuk Perpustakaan Java: Unduh dan instal perpustakaan Aspose.Note untuk Java. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/java/).

## Paket Impor

Pertama, mari impor paket yang diperlukan untuk kode Java kita:

```java
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Langkah 1: Muat Dokumen

 Langkah awal adalah memuat dokumen ke Aspose.Note. Hal ini dapat dicapai dengan menggunakan`Document` kelas yang disediakan oleh Aspose.Note.

```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory";

// Muat dokumen ke Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Langkah 2: Simpan sebagai Gambar JPEG

 Selanjutnya, kita akan menentukan jalur file keluaran dan menyimpan dokumen dalam format gambar JPEG menggunakan`save()` metode bersama dengan`SaveFormat.Jpeg` parameter.

```java
// Tentukan jalur file keluaran.
dataDir = dataDir + "SaveToJpegImageUsingSaveFormat_out.jpg";

// Simpan dokumennya.
oneFile.save(dataDir, SaveFormat.Jpeg);
```

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara menyimpan dokumen sebagai gambar JPEG menggunakan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah yang disediakan, Anda dapat dengan lancar mengonversi file OneNote ke format JPEG secara terprogram, memungkinkan berbagai kemungkinan integrasi dan otomatisasi dalam aplikasi Java Anda.

## FAQ

### Q1: Bisakah Aspose.Note menangani file OneNote yang kompleks?

A1: Ya, Aspose.Note dirancang untuk menangani file OneNote yang kompleks secara efisien, memastikan konversi dan manipulasi yang akurat.

### Q2: Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?

 A2: Ya, Anda bisa mendapatkan versi uji coba gratis Aspose.Note untuk Java dari[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.Note untuk Java?

 A3: Anda bisa mendapatkan dukungan untuk Aspose.Note untuk Java dengan mengunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28).

### Q4: Bisakah saya membeli lisensi sementara Aspose.Note untuk Java?

 A4: Ya, Anda dapat membeli lisensi sementara dari[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.Note untuk Java?

A5: Anda dapat menemukan dokumentasi terperinci untuk Aspose.Note untuk Java[Di Sini](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
