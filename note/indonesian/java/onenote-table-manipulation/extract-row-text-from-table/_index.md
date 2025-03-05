---
title: Ekstrak Teks Baris dari Tabel di Dokumen OneNote - Aspose.Note
linktitle: Ekstrak Teks Baris dari Tabel di Dokumen OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Pelajari cara mengekstrak teks baris dari tabel OneNote dengan mudah menggunakan Aspose.Note untuk Java. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
type: docs
weight: 13
url: /id/java/onenote-table-manipulation/extract-row-text-from-table/
---
## Perkenalan
Selamat datang di tutorial komprehensif tentang mengekstrak teks baris dari tabel di dokumen OneNote menggunakan Aspose.Note untuk Java. Aspose.Note adalah pustaka Java canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote dengan lancar. Dalam tutorial ini, kami akan memandu Anda melalui proses langkah demi langkah, menunjukkan cara mengekstrak teks baris dari tabel di dokumen OneNote Anda secara efisien.
## Prasyarat
Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:
-  Aspose.Note untuk Perpustakaan Java: Pastikan Anda telah menginstal perpustakaan Aspose.Note untuk Java. Anda dapat mengunduhnya dari[tautan unduhan](https://releases.aspose.com/note/java/).
- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.
- Dokumen OneNote: Siapkan contoh dokumen OneNote (misalnya, "Sample1.one") yang berisi tabel tempat Anda ingin mengekstrak teks barisnya.
## Paket Impor
Di proyek Java Anda, impor paket Aspose.Note yang diperlukan. Hal ini memastikan bahwa Anda memiliki akses ke kelas dan metode yang diperlukan untuk bekerja dengan dokumen OneNote.
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableRow;
```
## Langkah 1: Atur Direktori Dokumen
```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory";
```
## Langkah 2: Muat Dokumen OneNote
```java
// Muat dokumen ke Aspose.Note.
Document document = new Document(dataDir + "Sample1.one", new LoadOptions());
```
## Langkah 3: Dapatkan Node Tabel
```java
// Dapatkan daftar node tabel
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```
## Langkah 4: Iterasi Melalui Tabel dan Baris
```java
// Tetapkan jumlah baris
int rowCount = 0;
for (Table table : nodes) {
    // Iterasi melalui baris tabel
    for (TableRow row : table) {
        rowCount++;
        // Ambil teks
        List<RichText> textNodes = (List<RichText>) row.getChildNodes(RichText.class);
        StringBuilder text = new StringBuilder();
        for (RichText richText : textNodes) {
            text = text.append(richText.getText().toString());
        }
        // Cetak teks pada layar keluaran
        System.out.println(text);
    }
}
```
Ulangi langkah-langkah ini untuk setiap tabel di dokumen OneNote Anda, dan Anda akan berhasil mengekstrak teks baris.
## Kesimpulan
Selamat! Anda telah mempelajari cara mengekstrak teks baris dari tabel di dokumen OneNote menggunakan Aspose.Note untuk Java. Tutorial ini memberikan landasan untuk memanfaatkan kemampuan Aspose.Note yang kuat dalam aplikasi Java Anda.
## Pertanyaan yang Sering Diajukan
### Apakah Aspose.Note kompatibel dengan versi terbaru Microsoft OneNote?
 Aspose.Note mendukung berbagai versi OneNote, termasuk yang terbaru. Mengacu kepada[dokumentasi](https://reference.aspose.com/note/java/) untuk detail kompatibilitas.
### Bisakah saya mencoba Aspose.Note untuk Java sebelum membeli?
Ya, Anda dapat menjelajahi uji coba gratis Aspose.Note di[Link ini](https://releases.aspose.com/).
### Di mana saya dapat memperoleh dukungan dan bantuan tambahan?
 Mengunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28) untuk dukungan dan diskusi komunitas.
### Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Note?
 Dapatkan lisensi sementara dari[Link ini](https://purchase.aspose.com/temporary-license/).
### Apakah ada persyaratan sistem khusus untuk menggunakan Aspose.Note untuk Java?
Lihat dokumentasi untuk persyaratan sistem terperinci.