---
title: Dapatkan Tugas Outlook di OneNote - Aspose.Note
linktitle: Dapatkan Tugas Outlook di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Jelajahi kekuatan Aspose.Note untuk Java dalam mengekstraksi tugas Outlook dari OneNote dengan mudah. Ikuti panduan langkah demi langkah kami dan tingkatkan kemampuan pemrosesan dokumen Anda.
weight: 10
url: /id/java/task-and-outlook-integration/get-outlook-task/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dapatkan Tugas Outlook di OneNote - Aspose.Note

## Perkenalan
Selamat datang di panduan komprehensif kami tentang penggunaan Aspose.Note untuk Java untuk mengambil tugas Outlook di OneNote dengan lancar. Aspose.Note adalah Java API canggih yang memungkinkan pengembang bekerja dengan file Microsoft OneNote dengan mudah. Dalam tutorial ini, kami akan memandu Anda melalui proses mengekstraksi tugas Outlook dari dokumen OneNote langkah demi langkah.
## Prasyarat
Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:
- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.
-  Perpustakaan Aspose.Note: Unduh dan instal perpustakaan Aspose.Note untuk Java. Anda dapat menemukan perpustakaan[Di Sini](https://releases.aspose.com/note/java/).
## Paket Impor
Untuk memulai, impor paket yang diperlukan ke proyek Java Anda. Tambahkan baris berikut ke kode Anda:
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;

```
Sekarang, mari kita bagi prosesnya menjadi langkah-langkah yang dapat dikelola:
## Langkah 1: Siapkan Direktori Dokumen Anda
Tentukan direktori tempat dokumen OneNote Anda berada:
```java
String dataDir = "Your Document Directory";
```
## Langkah 2: Muat Dokumen OneNote
Muat dokumen OneNote menggunakan Aspose.Catatan:
```java
Document doc = new Document(dataDir + "Sample1.one");
```
## Langkah 3: Dapatkan Semua Node RichText
Ambil semua node RichText dari dokumen:
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## Langkah 4: Iterasi Melalui Setiap Node
Ulangi setiap node RichText dan periksa tag NoteTask:
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Ambil properti
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```
## Kesimpulan
Selamat! Anda telah berhasil mempelajari cara menggunakan Aspose.Note untuk Java untuk mengambil tugas Outlook di OneNote. API yang kuat ini menyederhanakan proses, menjadikannya efisien dan ramah pengembang.
## FAQ
### Apakah Aspose.Note kompatibel dengan semua versi OneNote?
Aspose.Note mendukung Microsoft OneNote 2010 dan versi yang lebih baru.
### Bisakah saya menggunakan Aspose.Note untuk proyek pribadi dan komersial?
 Ya, Aspose.Note dapat digunakan untuk proyek pribadi dan komersial. Mengunjungi[Di Sini](https://purchase.aspose.com/buy) untuk mengeksplorasi opsi lisensi.
### Apakah ada uji coba gratis yang tersedia untuk Aspose.Note?
 Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).
### Bagaimana saya bisa mendapatkan dukungan untuk Aspose.Note?
 Mengunjungi[Aspose.Catatan Forum](https://forum.aspose.com/c/note/28) untuk dukungan masyarakat. Untuk bantuan tambahan, pertimbangkan untuk membeli a[izin sementara](https://purchase.aspose.com/temporary-license/).
### Apakah ada contoh dokumen OneNote yang tersedia untuk pengujian?
 Anda dapat menemukan contoh dokumen di dokumentasi Aspose.Note[Di Sini](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
