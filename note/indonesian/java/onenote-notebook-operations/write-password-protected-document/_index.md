---
title: Tulis Dokumen yang Dilindungi Kata Sandi di OneNote - Aspose.Note
linktitle: Tulis Dokumen yang Dilindungi Kata Sandi di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Lindungi informasi sensitif OneNote Anda! Pelajari cara menyetel kata sandi untuk dokumen & bagian tertentu - panduan langkah demi langkah & kode disertakan. #OneNote #Java #Aspose
type: docs
weight: 27
url: /id/java/onenote-notebook-operations/write-password-protected-document/
---
## Perkenalan

Dalam tutorial ini, Anda akan mempelajari cara membuat dokumen yang dilindungi kata sandi di OneNote menggunakan Aspose.Note untuk Java. Kemampuan ini menjamin keamanan dan privasi informasi sensitif Anda di dalam buku catatan Anda. Dengan mengikuti petunjuk langkah demi langkah ini, Anda dapat dengan mudah menerapkan perlindungan kata sandi untuk dokumen Anda.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda.
2.  Aspose.Note untuk Perpustakaan Java: Unduh dan instal Aspose.Note untuk perpustakaan Java dari[Di Sini](https://releases.aspose.com/note/java/).
3. Lingkungan Pengembangan Terpadu (IDE): Pilih dan siapkan IDE seperti Eclipse atau IntelliJ IDEA untuk pengembangan Java.

## Paket Impor

Untuk memulai, Anda perlu mengimpor paket yang diperlukan dari perpustakaan Aspose.Note untuk Java ke proyek Anda.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookOneSaveOptions;
import com.aspose.note.OneSaveOptions;
```

## Langkah 1: Muat Dokumen

Pertama, muat dokumen ke Aspose.Note.

```java
String dataDir = "Your Document Directory";

Notebook notebook = new Notebook();
```

## Langkah 2: Simpan Buku Catatan

Simpan buku catatan dengan opsi penyimpanan yang ditangguhkan.

```java
NotebookOneSaveOptions saveOptions = new NotebookOneSaveOptions();
saveOptions.setDeferredSaving(true);
notebook.save(dataDir + "Open Notebook.onetoc2", saveOptions);
```

## Langkah 3: Simpan Dokumen Anak dengan Perlindungan Kata Sandi

Simpan dokumen anak dengan perlindungan kata sandi.

```java
Document childDocument0 = (Document) notebook.get_Item(0);
childDocument0.save(dataDir + "Not Locked.one");

Document childDocument1 = (Document) notebook.get_Item(1);
OneSaveOptions documentSaveOptions1 = new OneSaveOptions();
documentSaveOptions1.setDocumentPassword("pass1");
childDocument1.save(dataDir + "Locked Pass1.one", documentSaveOptions1);

Document childDocument2 = (Document) notebook.get_Item(2);
OneSaveOptions documentSaveOptions2 = new OneSaveOptions();
documentSaveOptions2.setDocumentPassword("pass2");
childDocument2.save(dataDir + "Locked Pass2.one", documentSaveOptions2);
```

## Kesimpulan

Kesimpulannya, Anda telah berhasil mempelajari cara menulis dokumen yang dilindungi kata sandi di OneNote menggunakan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah ini, Anda dapat meningkatkan keamanan dokumen Anda dan memastikan bahwa hanya pengguna yang berwenang yang dapat mengaksesnya.

## FAQ

### Q1: Dapatkah saya mengubah kata sandi untuk dokumen yang dilindungi nanti?

J: Ya, Anda dapat mengubah kata sandi untuk dokumen yang dilindungi kapan saja menggunakan API Aspose.Note.
   
### Q2: Apakah mungkin untuk menghapus proteksi kata sandi dari dokumen?

J: Ya, Anda dapat menghapus proteksi kata sandi dari dokumen secara terprogram menggunakan Aspose.Note.
   
### Q3: Apakah Aspose.Note mendukung algoritma enkripsi selain kata sandi?

J: Ya, Aspose.Note mendukung algoritma enkripsi seperti AES untuk mengamankan dokumen.
   
### Q4: Dapatkah saya menetapkan kata sandi yang berbeda untuk bagian buku catatan yang berbeda?

J: Ya, Anda dapat mengatur kata sandi berbeda untuk bagian berbeda dalam buku catatan menggunakan API Aspose.Note.
   
### Q5: Apakah ada batasan panjang atau kerumitan kata sandi?

J: Aspose.Note tidak menerapkan batasan khusus pada panjang atau kompleksitas kata sandi, sehingga Anda dapat mengatur kata sandi yang kuat dan aman sesuai kebutuhan.