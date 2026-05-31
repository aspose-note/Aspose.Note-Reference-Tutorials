---
date: 2026-05-31
description: Pelajari cara memodifikasi page history OneNote, mengubah judul halaman
  OneNote, dan menghapus page history OneNote menggunakan Aspose.Note untuk Java.
keywords:
- modify onenote page history
- change onenote page title
- Aspose.Note Java
linktitle: Ubah Page History di OneNote - Aspise.Note
schemas:
- author: Aspose
  dateModified: '2026-05-31'
  description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  headline: How to modify onenote page history with Aspose.Note
  type: TechArticle
- description: Learn how to modify onenote page history, change onenote page title,
    and delete page history onenote using Aspose.Note for Java.
  name: How to modify onenote page history with Aspose.Note
  steps:
  - name: Load the OneNote Document
    text: '`Document` loads a OneNote file into memory and provides access to its
      pages and history.'
  - name: Retrieve the First Page and Its History
    text: '`PageHistory` is the Aspose.Note class that stores a notebook’s revision
      list. It offers methods to query, add, or remove historic pages.'
  - name: Delete a Range of History Items
    text: '`removeRange(int start, int count)` removes a consecutive block of history
      entries starting at the specified index.'
  - name: Replace a History Item
    text: '`set_Item(int index, Page page)` replaces the history entry at the given
      position with a new `Page` object.'
  - name: Change the Title of a History Page
    text: '`setTitle(String title)` updates the title of a historic `Page` instance.'
  - name: Add a New History Entry
    text: '`addItem(Page page)` appends a new page to the end of the history collection.'
  - name: Insert a Page at a Specific Position
    text: '`insertItem(int index, Page page)` inserts a page at the specified index,
      shifting subsequent items forward.'
  - name: Save the Modified Notebook
    text: '`save(String path)` writes the updated notebook to the given file location.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Note for Java integrates seamlessly with Spring, Hibernate,
      Android, and other Java ecosystems.
    question: Can I use Aspose.Note for Java with other Java frameworks?
  - answer: Absolutely—Aspose.Note supports both legacy OneNote 2007 files and the
      modern OneNote 2016/Online formats.
    question: Is Aspose.Note for Java compatible with different versions of OneNote
      files?
  - answer: No, the library is self‑contained; you only need the core JAR and a Java
      runtime.
    question: Does Aspose.Note for Java require any additional dependencies?
  - answer: Yes, you can loop through a directory of `.one` files and apply the same
      history‑editing logic to each notebook.
    question: Can I perform bulk modifications on multiple OneNote files simultaneously?
  - answer: Yes, you can visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28)
      for assistance and to share examples.
    question: Is there a community forum for Aspose.Note for Java where I can ask
      for help?
  type: FAQPage
second_title: Aspose.Note Java API
title: Cara memodifikasi page history OneNote dengan Aspose.Note
url: /id/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara memodifikasi riwayat halaman onenote dengan Aspose.Note

Dalam tutorial ini Anda akan belajar **cara memodifikasi riwayat halaman onenote** langkah‑demi‑langkah menggunakan Aspose.Note untuk Java API. Baik Anda perlu menghapus revisi lama, mengganti nama halaman historis, atau menyisipkan entri baru, panduan ini akan membawa Anda melalui alur kerja siap produksi yang berfungsi dengan notebook OneNote apa pun.

## Jawaban Cepat
- **Apa arti “page history” dalam OneNote?**  
  Ini adalah kumpulan versi halaman sebelumnya yang disimpan di dalam file OneNote.
- **Bisakah saya menghapus entri riwayat tertentu?**  
  Ya, gunakan metode `removeRange` atau `removeItem` pada objek `PageHistory`.
- **Apakah mengubah judul halaman merupakan bagian dari manipulasi riwayat?**  
  Tentu—setiap item riwayat memiliki judulnya sendiri yang dapat Anda ubah.
- **Apakah saya memerlukan lisensi untuk menjalankan kode ini?**  
  Lisensi evaluasi sementara dapat digunakan untuk pengujian; lisensi penuh diperlukan untuk produksi.
- **Versi Java mana yang didukung?**  
  Aspose.Note untuk Java mendukung JDK 8 dan yang lebih baru.

## Apa itu memodifikasi riwayat halaman onenote?
*Memodifikasi riwayat halaman onenote* mengacu pada pengeditan, penambahan, atau penghapusan entri secara programatis dalam daftar revisi internal notebook OneNote. Ini memungkinkan Anda menyimpan hanya versi yang relevan, mengganti nama judul historis, dan mengoptimalkan ukuran notebook sambil mengurangi pembengkakan file secara keseluruhan.

## Mengapa memodifikasi riwayat halaman onenote?
Memodifikasi riwayat halaman dapat secara dramatis meningkatkan keterkelolaan dan kinerja notebook. Dengan memangkas revisi yang tidak terpakai, Anda mengurangi ukuran file, mempercepat pemuatan, dan membuat navigasi lebih konsisten bagi pengguna akhir. Manfaat ini terutama terlihat pada notebook besar dengan ratusan halaman.

Aspose.Note mendukung **lebih dari 50 format input dan output** dan dapat memproses notebook yang berisi **hingga 10.000 halaman** tanpa memuat seluruh file ke memori, memastikan operasi berperforma tinggi.

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – JDK 8 atau yang lebih baru terpasang di mesin Anda.  
2. **Aspose.Note for Java library** – unduh dari [halaman unduhan](https://releases.aspose.com/note/java/).  
3. **Sebuah dokumen OneNote contoh** – misalnya `Sample1.one` yang dapat Anda modifikasi dengan aman.

## Impor Paket

Kelas-kelas berikut diperlukan: `Document` mewakili seluruh notebook, `Page` mewakili satu halaman individual, dan `PageHistory` mengelola kumpulan halaman historis.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Cara memodifikasi riwayat halaman onenote?

Muat notebook, ambil koleksi `PageHistory`‑nya, lalu gunakan metode yang disediakan untuk menghapus, mengganti, atau menyisipkan entri. Semua operasi dilakukan di memori, dan Anda hanya perlu memanggil `save` sekali di akhir untuk menyimpan perubahan.

### Langkah 1: Muat Dokumen OneNote

`Document` memuat file OneNote ke memori dan menyediakan akses ke halaman serta riwayatnya.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### Langkah 2: Ambil Halaman Pertama dan Riwayatnya

`PageHistory` adalah kelas Aspose.Note yang menyimpan daftar revisi notebook. Kelas ini menawarkan metode untuk menanyakan, menambah, atau menghapus halaman historis.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### Langkah 3: Hapus Rentang Item Riwayat

`removeRange(int start, int count)` menghapus blok berurutan entri riwayat yang dimulai pada indeks yang ditentukan.

```java
pageHistory.removeRange(0, 1);
```

### Langkah 4: Ganti Item Riwayat

`set_Item(int index, Page page)` menggantikan entri riwayat pada posisi tertentu dengan objek `Page` baru.

```java
pageHistory.set_Item(0, new Page());
```

### Langkah 5: Ubah Judul Halaman Riwayat

`setTitle(String title)` memperbarui judul dari instance `Page` historis.

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### Langkah 6: Tambahkan Entri Riwayat Baru

`addItem(Page page)` menambahkan halaman baru ke akhir koleksi riwayat.

```java
pageHistory.addItem(new Page());
```

### Langkah 7: Sisipkan Halaman pada Posisi Tertentu

`insertItem(int index, Page page)` menyisipkan halaman pada indeks yang ditentukan, menggeser item berikutnya ke depan.

```java
pageHistory.insertItem(1, new Page());
```

### Langkah 8: Simpan Notebook yang Dimodifikasi

`save(String path)` menulis notebook yang diperbarui ke lokasi file yang diberikan.

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## Kesalahan Umum & Tips
- **Indeks di luar batas:** Selalu verifikasi ukuran koleksi sebelum memanggil `removeRange` atau `insertItem`.  
- **Judul null:** Beberapa halaman historis mungkin tidak memiliki judul; lindungi terhadap `null` saat memanggil `getTitle()`.  
- **Lokasi penyimpanan:** Pastikan jalur output (`ModifyPageHistory_out.one`) dapat ditulisi; jika tidak, akan terjadi `IOException`.  
- **Tips kinerja:** Saat bekerja dengan notebook yang sangat besar, panggil `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` untuk mengaktifkan pemuatan malas dan menjaga penggunaan memori tetap rendah.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan Aspose.Note untuk Java dengan kerangka kerja Java lainnya?**  
A: Ya, Aspose.Note untuk Java terintegrasi dengan mulus dengan Spring, Hibernate, Android, dan ekosistem Java lainnya.

**Q: Apakah Aspose.Note untuk Java kompatibel dengan berbagai versi file OneNote?**  
A: Tentu—Aspose.Note mendukung baik file OneNote 2007 lama maupun format modern OneNote 2016/Online.

**Q: Apakah Aspose.Note untuk Java memerlukan dependensi tambahan?**  
A: Tidak, perpustakaan ini berdiri sendiri; Anda hanya memerlukan JAR inti dan runtime Java.

**Q: Bisakah saya melakukan modifikasi massal pada beberapa file OneNote secara bersamaan?**  
A: Ya, Anda dapat melakukan loop melalui direktori berisi file `.one` dan menerapkan logika pengeditan riwayat yang sama ke setiap notebook.

**Q: Apakah ada forum komunitas untuk Aspose.Note untuk Java tempat saya dapat meminta bantuan?**  
A: Ya, Anda dapat mengunjungi [forum Aspose.Note](https://forum.aspose.com/c/note/28) untuk bantuan dan berbagi contoh.

---

**Terakhir Diperbarui:** 2026-05-31  
**Diuji Dengan:** Aspose.Note for Java 24.11 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [tutorial revisi halaman aspose.note – Dapatkan Revisi Halaman di OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Cara Menyimpan Versi Halaman OneNote – Dorong Versi Halaman Saat Ini di OneNote - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [lacak perubahan onenote – Kelola Revisi Halaman dengan Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}