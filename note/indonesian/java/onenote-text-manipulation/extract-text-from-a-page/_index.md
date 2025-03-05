---
title: Ekstrak Teks dari Halaman di OneNote - Aspose.Note
linktitle: Ekstrak Teks dari Halaman di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Temukan cara mengekstrak teks dari halaman OneNote dengan mudah menggunakan Aspose.Note untuk Java. Sederhanakan proses Anda dengan panduan langkah demi langkah yang komprehensif ini.
type: docs
weight: 16
url: /id/java/onenote-text-manipulation/extract-text-from-a-page/
---
## Perkenalan
Jika Anda ingin membuka potensi mengekstraksi teks dari halaman OneNote secara efisien menggunakan Java, Anda berada di tempat yang tepat. Panduan langkah demi langkah ini akan memandu Anda melalui proses menggunakan Aspose.Note untuk Java. Aspose.Note adalah API canggih yang menyederhanakan pekerjaan dengan dokumen OneNote, memungkinkan Anda mengekstrak teks dari halaman dengan mudah dengan mudah.
## Prasyarat
Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:
- Pemahaman dasar tentang pemrograman Java.
-  Aspose.Note untuk Java diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/note/java/).
## Paket Impor
Mulailah dengan mengimpor paket yang diperlukan dalam proyek Java Anda untuk memanfaatkan fungsionalitas Aspose.Note:
```java
import com.aspose.note.Document;
import com.aspose.note.Node;
import com.aspose.note.NodeType;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import java.util.List;
import java.util.stream.Collectors;
```
Sekarang, mari kita uraikan setiap langkah secara mendetail.
## Langkah 1: Atur Direktori Dokumen
 Pastikan Anda memiliki direktori dokumen khusus tempat file OneNote Anda disimpan. Mengganti`"Your Document Directory"` dengan jalur sebenarnya.
```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory";
```
## Langkah 2: Muat Dokumen OneNote
 Menggunakan`Document` kelas dari Aspose.Note untuk memuat dokumen OneNote Anda:
```java
Document oneFile = new Document(dataDir + "Sample1.one");
```
 Mengganti`"Sample1.one"` dengan nama file OneNote Anda.
## Langkah 3: Ambil Node Halaman
Dapatkan daftar node halaman dari dokumen yang dimuat:
```java
List<Node> nodes = oneFile.getChildNodes(Node.class);
```
Ini memastikan Anda memiliki akses ke halaman dalam dokumen OneNote.
## Langkah 4: Periksa dan Ekstrak Teks
Periksa apakah dokumen memiliki halaman, dan jika demikian, ambil teksnya:
```java
if (nodes.size() > 0 && nodes.get(0).getNodeType() == NodeType.Page)
{
    Page page = (Page)nodes.get(0);
    // Ambil teks
    List<RichText> textNodes = (List<RichText>) page.getChildNodes(RichText.class);
    StringBuilder text = new StringBuilder();
    for (RichText richText : textNodes) {
        text = text.append(richText.getText().toString());
    }
    
    // Cetak teks pada layar keluaran
    System.out.println(text);
}
```
Cuplikan ini memeriksa apakah node pertama adalah halaman, lalu mengekstrak dan mencetak teksnya.
Lanjutkan langkah-langkah ini untuk meningkatkan kemampuan aplikasi Java Anda dalam mengekstraksi teks dari halaman OneNote menggunakan Aspose.Note untuk Java.
## Kesimpulan
Selamat! Anda telah berhasil mempelajari cara mengekstrak teks dari halaman OneNote menggunakan Aspose.Note untuk Java. Gabungkan pengetahuan ini ke dalam proyek Anda dan sederhanakan proses ekstraksi teks Anda dengan mudah.
## Pertanyaan yang Sering Diajukan
### Bisakah saya menggunakan Aspose.Note untuk Java dengan bahasa pemrograman lain?
Aspose.Note terutama mendukung Java tetapi memiliki versi untuk bahasa lain seperti .NET. Periksa dokumentasi untuk kompatibilitas bahasa.
### Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?
 Ya, Anda dapat menjelajahi versi uji coba gratis[Di Sini](https://releases.aspose.com/).
### Di mana saya dapat menemukan dukungan untuk Aspose.Note untuk Java?
 Kunjungi Aspose.Note[forum](https://forum.aspose.com/c/note/28) untuk dukungan dan diskusi komunitas.
### Bagaimana saya bisa membeli Aspose.Note untuk Java?
 Anda dapat membeli produknya[Di Sini](https://purchase.aspose.com/buy).
### Apakah saya memerlukan lisensi sementara untuk Aspose.Note untuk Java?
 Jika Anda memerlukan lisensi sementara, Anda bisa mendapatkannya[Di Sini](https://purchase.aspose.com/temporary-license/).