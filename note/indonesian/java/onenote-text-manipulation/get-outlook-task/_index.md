---
title: Dapatkan Tugas Outlook di OneNote - Aspose.Note
linktitle: Dapatkan Tugas Outlook di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Jelajahi potensi Aspose.Note untuk Java dalam mengekstraksi detail Tugas Outlook dari dokumen OneNote dengan mudah. Tingkatkan pengembangan Java Anda dengan perpustakaan tangguh ini.
weight: 10
url: /id/java/onenote-text-manipulation/get-outlook-task/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dapatkan Tugas Outlook di OneNote - Aspose.Note

## Perkenalan
Selamat datang di dunia Aspose.Note untuk Java – alat canggih yang memberdayakan pengembang Java untuk bekerja dengan lancar dengan file Microsoft OneNote. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses mengekstraksi informasi Tugas Outlook dari dokumen OneNote menggunakan Aspose.Note untuk Java.
## Prasyarat
Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:
- Java Development Kit (JDK): Pastikan Anda telah menginstal Java di sistem Anda.
-  Aspose.Note untuk Java: Unduh dan instal perpustakaan Aspose.Note dari[Unduh Halaman](https://releases.aspose.com/note/java/).
## Paket Impor
Mulailah dengan mengimpor paket yang diperlukan ke proyek Java Anda. Tambahkan baris berikut di awal file Java Anda:
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```
## Langkah 1: Siapkan Proyek Anda
Buat proyek Java baru dan sertakan pustaka Aspose.Note dalam dependensi proyek Anda. Pastikan struktur proyek Anda terorganisir, dan Anda memiliki direktori khusus untuk dokumen Anda.
## Langkah 2: Muat Dokumen OneNote
Gunakan kode berikut untuk memuat dokumen OneNote Anda ke Aspose.Catatan:
```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```
Pastikan untuk mengganti "Direktori Dokumen Anda" dengan jalur ke dokumen OneNote Anda.
## Langkah 3: Ambil Node RichText
Ekstrak semua node RichText dari dokumen menggunakan kode berikut:
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## Langkah 4: Iterasi Melalui Setiap Node
Ulangi setiap node RichText dan identifikasi apakah node tersebut berisi tag NoteTask:
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            // Kode Anda untuk menangani NoteTask
        }
    }
}
```
## Langkah 5: Ambil Properti Tugas
Ambil dan cetak berbagai properti NoteTask, seperti Waktu Selesai, Waktu Pembuatan, Tanggal Jatuh Tempo, Status, dan Ikon:
```java
NoteTask noteTask = (NoteTask) tag;
System.out.println("Completed Time: " + noteTask.getCompletedTime());
System.out.println("Create Time: " + noteTask.getCreationTime());
System.out.println("Due Date: " + noteTask.getDueDate());
System.out.println("Status: " + noteTask.getStatus());
System.out.println("Icon: " + noteTask.getIcon());
```
Ulangi proses ini untuk semua node NoteTask di dokumen.
## Kesimpulan
Selamat! Anda telah berhasil mempelajari cara menggunakan Aspose.Note untuk Java untuk mengekstrak informasi Tugas Outlook dari dokumen OneNote. Pustaka yang kuat ini membuka banyak kemungkinan bagi pengembang Java yang bekerja dengan file Microsoft OneNote.
## FAQ
### T: Dapatkah saya menggunakan Aspose.Note untuk Java dengan kerangka kerja Java lainnya?
J: Ya, Aspose.Note for Java kompatibel dengan berbagai framework Java, sehingga memberikan fleksibilitas dalam integrasi.
### T: Apakah tersedia uji coba gratis untuk Aspose.Note untuk Java?
 J: Ya, Anda dapat menjelajahi uji coba gratis Aspose.Note untuk Java[Di Sini](https://releases.aspose.com/).
### T: Bagaimana cara mendapatkan dukungan untuk Aspose.Note untuk Java?
 J: Kunjungi[Aspose.Catatan Forum](https://forum.aspose.com/c/note/28) untuk dukungan komunitas atau jelajahi opsi dukungan premium.
### T: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.Note untuk Java?
 J: Lihat[Aspose.Note untuk dokumentasi Java](https://reference.aspose.com/note/java/) untuk informasi mendalam.
### T: Bagaimana cara mendapatkan lisensi sementara Aspose.Note untuk Java?
 A: Dapatkan lisensi sementara Anda[Di Sini](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
