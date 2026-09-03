---
date: 2026-01-25
description: Pelajari cara menambahkan tag ke gambar, menyisipkan gambar ke OneNote,
  dan menyimpan OneNote sebagai PDF menggunakan Aspose.Note untuk Java.
linktitle: Add Tag to Image in OneNote – Aspose.Note
second_title: Aspose.Note Java API
title: Tambahkan Tag ke Gambar di OneNote dengan Aspose.Note – Java
url: /id/java/onenote-tag-operations/add-new-image-node-with-tag/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menambahkan Tag ke Gambar di OneNote dengan Aspose.Note – Java

## Pendahuluan
Jika Anda perlu **menambahkan tag ke gambar** di dalam notebook OneNote saat bekerja dengan Java, Aspose.Note membuat seluruh proses menjadi sederhana. Dalam tutorial ini kami akan menunjukkan cara menyisipkan gambar ke OneNote, menerapkan tag bintang kuning pada gambar tersebut, dan akhirnya **menyimpan OneNote sebagai PDF**. Pada akhir tutorial Anda akan melihat dengan tepat cara menambahkan tag ke gambar, menyisipkan gambar ke OneNote, dan mengonversi OneNote ke PDF—semua dengan hanya beberapa baris kode.

## Jawaban Cepat
- **Apa arti “menambahkan tag ke gambar”?** Itu menempelkan tag catatan visual (misalnya, bintang kuning) ke node gambar dalam halaman OneNote.  
- **Perpustakaan mana yang menangani ini?** Aspose.Note untuk Java.  
- **Apakah saya memerlukan lisensi untuk pengujian?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengekspor hasilnya sebagai PDF?** Ya – gunakan `doc.save(..., SaveFormat.Pdf)` untuk **menyimpan OneNote sebagai PDF**.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk skenario dasar.

## Apa itu “menambahkan tag ke gambar” di OneNote?
Menambahkan tag ke gambar berarti menempelkan elemen metadata (seperti bintang, bendera, atau ikon khusus) ke node gambar. Tag ini ditampilkan di UI OneNote dan dapat digunakan untuk pencarian cepat, pengkategorian, atau petunjuk visual.

## Mengapa menambahkan tag ke gambar di OneNote?
Menandai gambar membantu Anda:
- Mengatur konten visual tanpa mengubah gambar itu sendiri.  
- Dengan cepat menemukan grafik penting menggunakan pencarian tag OneNote.  
- Menyediakan konteks (misalnya, “tinjau nanti”, “referensi penting”) langsung pada halaman.  

## Prasyarat
Sebelum kita mulai, pastikan Anda memiliki hal‑hal berikut:

1. Aspose.Note untuk Java: Pastikan Anda telah menginstal pustaka Aspose.Note. Jika belum, Anda dapat mengunduhnya [di sini](https://releases.aspose.com/note/java/).  
2. Lingkungan Pengembangan Java: Pastikan Anda memiliki lingkungan pengembangan Java yang berfungsi di mesin Anda.  

Setelah prasyarat tersedia, mari lanjut ke langkah‑langkah berikutnya.

## Mengimpor Paket
Di proyek Java Anda, mulailah dengan mengimpor paket‑paket yang diperlukan:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Membuat Objek Dokumen
```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
```

### Langkah 2: Menginisialisasi Objek Kelas Page
```java
// initialize Page class object
Page page = new Page();
```

### Langkah 3: Menginisialisasi Objek Kelas Outline
```java
// initialize Outline class object
Outline outline = new Outline();
```

### Langkah 4: Menginisialisasi Objek Kelas OutlineElement
```java
// initialize OutlineElement class object
OutlineElement outlineElem = new OutlineElement();
```

### Langkah 5: Memuat dan Menyisipkan Gambar  
*(Langkah ini menunjukkan **menyisipkan gambar ke OneNote**)*  
```java
// load an image
Image image = new Image(null, dataDir + "Input.jpg");
// insert image in the document node
outlineElem.appendChildLast(image);
```

### Langkah 6: Menambahkan Tag Catatan ke Gambar  
*(Di sini kami menjawab **cara menambahkan tag gambar**)*  
```java
// add a yellow star note tag to the image
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```

### Langkah 7: Menambahkan Node Outline Element
```java
// add outline element node
outline.appendChildLast(outlineElem);
```

### Langkah 8: Menambahkan Node Outline
```java
// add outline node
page.appendChildLast(outline);
```

### Langkah 9: Menambahkan Node Page
```java
// add page node
doc.appendChildLast(page);
```

### Langkah 10: Menyimpan Dokumen OneNote  
*(Sekarang kami **menyimpan OneNote sebagai PDF** dan secara efektif **mengonversi OneNote ke PDF**)*  
```java
// save OneNote document as a PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```

Selamat! Anda telah berhasil **menambahkan tag ke gambar**, menyisipkan gambar ke OneNote, dan mengekspor notebook ke PDF menggunakan Aspose.Note untuk Java.

## Masalah Umum dan Solusinya
| Masalah | Solusi |
|---------|--------|
| **Gambar tidak ditampilkan** | Verifikasi bahwa jalur pada `dataDir + "Input.jpg"` sudah benar dan file dapat diakses. |
| **Tag tidak terlihat** | Pastikan Anda menggunakan versi OneNote yang mendukung tag catatan (sebagian besar versi terbaru melakukannya). |
| **Output PDF kosong** | Periksa bahwa dokumen berisi setidaknya satu halaman/outline sebelum memanggil `save`. |

## Pertanyaan yang Sering Diajukan

**T: Di mana saya dapat menemukan dokumentasi Aspose.Note?**  
J: Dokumentasi dapat Anda temukan [di sini](https://reference.aspose.com/note/java/).

**T: Bagaimana cara mengunduh Aspose.Note untuk Java?**  
J: Anda dapat mengunduhnya dari halaman rilis [di sini](https://releases.aspose.com/note/java/).

**T: Apakah tersedia versi percobaan gratis?**  
J: Ya, Anda dapat mengakses versi percobaan gratis [di sini](https://releases.aspose.com/).

**T: Di mana saya dapat mendapatkan dukungan untuk Aspose.Note?**  
J: Kunjungi forum komunitas [di sini](https://forum.aspose.com/c/note/28) untuk dukungan.

**T: Apakah saya memerlukan lisensi sementara?**  
J: Jika diperlukan, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

## Kesimpulan
Menguasai Aspose.Note untuk Java membuka peluang menarik dalam manipulasi dokumen OneNote. Dengan mengikuti tutorial ini, Anda telah mempelajari **cara menambahkan tag ke gambar**, **menyisipkan gambar ke OneNote**, dan **menyimpan OneNote sebagai PDF**—kemampuan yang dapat Anda terapkan pada berbagai proyek otomasi. Terus jelajahi dokumentasi Aspose.Note [di sini](https://reference.aspose.com/note/java/) untuk fitur dan kemungkinan yang lebih lanjutan.

---

**Terakhir Diperbarui:** 2026-01-25  
**Diuji Dengan:** Aspose.Note 24.11 untuk Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}