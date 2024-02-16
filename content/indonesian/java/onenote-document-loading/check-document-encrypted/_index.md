---
title: Periksa apakah Dokumen OneNote Dienkripsi - Java
linktitle: Periksa apakah Dokumen OneNote Dienkripsi - Java
second_title: Aspose.Catatan Java API
description: Pelajari cara memeriksa apakah dokumen OneNote dienkripsi di Java menggunakan Aspose.Note. Ikuti panduan langkah demi langkah kami untuk pemrosesan dokumen yang efisien.
type: docs
weight: 10
url: /id/java/onenote-document-loading/check-document-encrypted/
---
## Perkenalan

Saat bekerja dengan dokumen OneNote di Java, penting untuk memastikan bahwa dokumen tersebut tidak dienkripsi sebelum memprosesnya. Mengenkripsi dokumen dapat menambah lapisan keamanan ekstra, namun juga dapat mempersulit langkah pemrosesan jika tidak ditangani dengan benar. Dalam tutorial ini, kami akan memandu Anda melalui proses pemeriksaan apakah dokumen OneNote dienkripsi menggunakan Aspose.Note untuk Java.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki prasyarat berikut:

1.  Java Development Kit (JDK): Pastikan Anda telah menginstal Java di sistem Anda. Anda dapat mengunduhnya dari[Di Sini](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

2.  Aspose.Note untuk Perpustakaan Java: Unduh dan atur perpustakaan Aspose.Note untuk Java. Anda dapat menemukan tautan unduhan[Di Sini](https://releases.aspose.com/note/java/).

## Paket Impor

Untuk memulai, impor paket yang diperlukan dalam proyek Java Anda:

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```

Mari kita bagi prosesnya menjadi beberapa langkah:

## Langkah 1: Periksa apakah Dokumen dari Aliran Dienkripsi

```java
public static void CheckIfDocumentFromStreamIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromStreamIsEncrypted
    String dataDir = "Your Document Directory";

    LoadOptions loadOptions = new LoadOptions();
    loadOptions.setDocumentPassword("password");

    FileInputStream stream = new FileInputStream(Paths.get(dataDir, "Sample1.one").toString());

    try {
        Document ref[] = { null };
        if (!Document.isEncrypted(stream, loadOptions, ref)) {
            System.out.println("The document is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Provide a password.");
        }
    } finally {
        stream.close();
    }
    // ExEnd:CheckIfDocumentFromStreamIsEncrypted
}
```

Penjelasan:

- Metode ini memeriksa apakah dokumen yang dimuat dari aliran dienkripsi.
-  Ini menetapkan kata sandi dokumen menggunakan`setDocumentPassword` metode dari`LoadOptions` kelas.
-  Itu`Document.isEncrypted` metode ini digunakan untuk menentukan apakah dokumen tersebut dienkripsi atau tidak.

## Langkah 2: Periksa apakah Dokumen dari File Dienkripsi

```java
public static void CheckIfDocumentFromFileIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromFileIsEncrypted
    String dataDir = "Your Document Directory";

    Document ref[] = { null };
    if (!Document.isEncrypted(Paths.get(dataDir, "Sample1.one").toString(), "VerySecretPassword", ref)) {
        if (ref[0] != null) {
            System.out.println("The document is decrypted. It is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Invalid password was provided.");
        }
    } else {
        System.out.println("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
    // ExEnd:CheckIfDocumentFromFileIsEncrypted
}
```

Penjelasan:

- Metode ini memeriksa apakah dokumen yang dimuat dari suatu file dienkripsi.
-  Ini menggunakan`Document.isEncrypted` metode yang mirip dengan langkah sebelumnya tetapi dengan parameter jalur file dan kata sandi.

## Kesimpulan

Dalam tutorial ini, kita mempelajari cara memeriksa apakah dokumen OneNote dienkripsi di Java menggunakan Aspose.Note. Dengan mengikuti panduan langkah demi langkah dan memanfaatkan contoh kode yang disediakan, Anda dapat menentukan status enkripsi dokumen Anda secara efisien, memastikan kelancaran pemrosesan di aplikasi Java Anda.

## FAQ

### Q1: Dapatkah saya memeriksa status enkripsi tanpa memberikan kata sandi?

A1: Ya, Anda dapat memeriksa status enkripsi tanpa memberikan kata sandi. Itu`Document.isEncrypted` metode ini memungkinkan Anda melakukannya.

### Q2: Apa yang terjadi jika saya memberikan kata sandi yang salah?

 A2: Jika Anda memberikan kata sandi yang salah saat memeriksa status enkripsi, metode ini akan kembali`true`, menunjukkan bahwa dokumen tersebut dienkripsi, tetapi kata sandi yang diberikan salah.

### Q3: Apakah mungkin untuk mendekripsi dokumen terenkripsi secara terprogram?

A3: Ya, Anda dapat mendekripsi dokumen terenkripsi secara terprogram dengan memberikan kata sandi yang benar saat memuat dokumen.

### Q4: Bisakah saya menggunakan Aspose.Note untuk format dokumen lain selain OneNote?

A4: Tidak, Aspose.Note dirancang khusus untuk bekerja dengan dokumen OneNote saja.

### Q5: Di mana saya dapat menemukan lebih banyak sumber daya dan dukungan untuk Aspose.Note untuk Java?

 A5: Anda dapat mengunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28) untuk dukungan dan dokumentasi komunitas.