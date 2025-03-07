---
title: Dorong Versi Halaman Saat Ini di OneNote - Aspose.Note
linktitle: Dorong Versi Halaman Saat Ini di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Jaga agar konten OneNote tetap segar! Pelajari cara memperbarui riwayat halaman & mengelola versi, termasuk panduan langkah demi langkah & kode. #OneNote #Java #Aspose
weight: 18
url: /id/java/onenote-page-manipulation/push-current-page-version/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dorong Versi Halaman Saat Ini di OneNote - Aspose.Note

## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara memanfaatkan Aspose.Note untuk Java untuk mendorong versi halaman saat ini di OneNote. Aspose.Note adalah pustaka Java canggih yang memungkinkan pengembang bekerja dengan dokumen Microsoft OneNote secara terprogram, memungkinkan berbagai operasi seperti membuat, memanipulasi, dan mengonversi file OneNote.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:
1. Pengetahuan dasar bahasa pemrograman Java.
2. Menginstal Java Development Kit (JDK) di sistem Anda.
3.  Aspose.Note untuk perpustakaan Java. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/note/java/).
4. Contoh dokumen OneNote untuk digunakan.

## Paket Impor

Pertama, Anda perlu mengimpor paket yang diperlukan dalam proyek Java Anda untuk menggunakan fungsionalitas Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Langkah 1: Muat Dokumen OneNote

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 Di Sini,`dataDir` harus menunjuk ke direktori tempat dokumen OneNote Anda berada. Mengganti`"Sample1.one"` dengan nama file OneNote Anda.

## Langkah 2: Dapatkan Halaman Saat Ini dan Riwayatnya

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 Kami mengambil halaman pertama dokumen menggunakan`getFirstChild()` dan kemudian dapatkan riwayatnya menggunakan`getPageHistory()`.

## Langkah 3: Dorong Versi Halaman Saat Ini

```java
pageHistory.addItem(page.deepClone());
```

Di sini, kami menambahkan versi halaman saat ini ke riwayatnya dengan mengkloningnya dan menambahkannya sebagai item baru.

## Langkah 4: Simpan Dokumen

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

Terakhir, kami menyimpan dokumen yang dimodifikasi dengan riwayat halaman yang diperbarui.

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara mendorong versi halaman saat ini di OneNote menggunakan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah ini, Anda bisa secara efektif mengelola versi dokumen OneNote Anda secara terprogram.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.Note for Java untuk bekerja dengan file OneNote terenkripsi?

A1: Ya, Aspose.Note untuk Java mendukung bekerja dengan file OneNote terenkripsi dan tidak terenkripsi.

### Q2: Apakah Aspose.Note untuk Java kompatibel dengan OneNote versi terbaru?

A2: Aspose.Note untuk Java berupaya menjaga kompatibilitas dengan versi terbaru dokumen OneNote.

### Q3: Dapatkah saya memanipulasi teks dan gambar dalam dokumen OneNote menggunakan Aspose.Note untuk Java?

A3: Tentu saja, Aspose.Note untuk Java menyediakan fungsionalitas ekstensif untuk memanipulasi teks, gambar, dan elemen lain dalam file OneNote.

### Q4: Apakah Aspose.Note untuk Java mendukung konversi file OneNote ke format lain?

A4: Ya, Aspose.Note untuk Java mendukung konversi file OneNote ke berbagai format seperti PDF, HTML, dan format gambar.

### Q5: Di mana saya bisa mendapatkan dukungan untuk Aspose.Note untuk Java jika saya mengalami masalah?

 A5: Anda dapat mengunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28) untuk mencari bantuan dari komunitas atau menghubungi dukungan Aspose secara langsung.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
