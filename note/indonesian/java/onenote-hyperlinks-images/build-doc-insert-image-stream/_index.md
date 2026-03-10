---
date: 2025-12-21
description: Pelajari cara membuat dokumen OneNote dengan Java dan dengan mudah menyisipkan
  gambar menggunakan Aspose.Note untuk Java. Panduan langkah demi langkah untuk pengembang
  Java.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Cara membuat dokumen OneNote Java – Membuat Dokumen dan Menyisipkan Gambar
  dengan Stream
url: /id/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara membuat onenote document java – Membuat Dokumen dan Menyisipkan Gambar dengan Stream

## Perkenalan

Selamat datang! Dalam tutorial ini Anda akan **membuat dokumen onenote java** dari awal dan belajar cara menyisipkan gambar menggunakan aliran gambar. Kami akan memandu Anda melalui setiap langkah, menjelaskan mengapa setiap bagian penting, dan memberikan tip praktis agar Anda dapat menerapkan teknik ini dalam proyek nyata. Pada akhir tutorial, Anda akan dapat membuat halaman OneNote secara terprogram dan menyematkan gambar tepat di tempat yang Anda inginkan.

## Jawaban Cepat
- **Perpustakaan apa yang saya perlukan?** Aspose.Note untuk Java
- **Dapatkah saya menyisipkan gambar dari aliran?** Ya – cukup teruskan `InputStream` ke konstruktor `Image`.
- **Format mana yang dapat saya ekspor?** Format apa pun yang didukung oleh Aspose.Note, misalnya PDF, DOCX, HTML.
- **Apakah saya memerlukan lisensi untuk pengembangan?** Lisensi sementara gratis berfungsi untuk evaluasi; lisensi penuh diperlukan untuk produksi.
- **Versi Java apa yang diperlukan?** Java8 atau lebih tinggi.

## Apa itu “buat dokumen onenote java”?

Membuat dokumen OneNote dalam Java berarti menggunakan API Aspose.Note untuk secara terprogram membangun struktur notebook—halaman, outline, dan elemen—tanpa membuka klien desktop OneNote. Pendekatan ini ideal untuk pembuatan laporan otomatis, pembuatan catatan batch, atau mengintegrasikan konten OneNote ke dalam aplikasi Java yang lebih besar.

## Mengapa menggunakan Aspose.Note untuk Java untuk membuat dokumen onenote java?

- **Kontrol penuh** atas tata letak halaman, posisi kerangka, dan gaya elemen. → Kontrol penuh atas tata letak halaman, posisi outline, dan elemen gaya.
- **Tidak ada interop COM** – berfungsi pada OS apa pun yang mendukung Java. → Tanpa interop COM – bekerja pada semua OS yang mendukung Java.
- **Opsi ekspor yang kaya** – mengonversi dokumen yang sama ke PDF, DOCX, HTML, dll., dengan satu panggilan. → Opsi ekspor kaya – mengonversi dokumen yang sama ke PDF, DOCX, HTML, dll., dengan satu panggilan.
- **Ramah streaming** – Anda dapat memuat gambar langsung dari memori, jaringan, atau penyimpanan cloud. → Ramahan stream – Anda dapat memuat gambar langsung dari memori, jaringan, atau penyimpanan cloud.

## Prasyarat

Sebelum kita mulai, pastikan Anda telah menyiapkan hal‑hal berikut:

### Kit Pengembangan Java (JDK)

JDK terbaru (8 atau lebih tinggi) terpasang di mesin Anda.

### Aspose.Note untuk Perpustakaan Java

Unduh perpustakaan dari halaman rilis resmi Aspose: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### Pengaturan IDE

Konfigurasikan IDE favorit Anda (IntelliJ IDEA, Eclipse, VS Code) untuk menyertakan file JAR Aspose.Note pada proyek classpath.

## Impor Paket

Untuk memulai, impor kelas‑kelas Java dan Aspose.Catatan yang diperlukan. Impor ini memberi Anda akses ke pembuatan dokumen, penanganan halaman, garis besar manajemen, dan penyisipan gambar.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Langkah 1: Menyiapkan Direktori Dokumen

Tentukan folder yang berisi gambar sumber Anda dan tempat file output akan disimpan. Ganti placeholder dengan path aktual di mesin Anda.

```java
String dataDir = "Your Document Directory";
```

## Langkah 2: Membuat Objek Dokumen

Instansiasi `Document` baru. Objek ini mewakili notebook OneNote yang sedang Anda bangun.

```java
Document doc = new Document();
```

## Langkah 3: Menginisialisasi Objek Halaman

Buat `Page` yang akan menampung semua outline dan elemen untuk halaman notebook ini.

```java
Page page = new Page();
```

## Langkah 4: Membuat Garis Besar

`Outline` berfungsi sebagai wadah untuk elemen‑elemen yang diposisikan. Di sini kami mengatur offset vertikal dan horizontal untuk menempatkan outline pada halaman.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Langkah 5: Membuat Elemen Garis Besar

`OutlineElement` akan menjadi tempat gambar yang akan kami sisipkan.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Langkah 6: Memuat Aliran Gambar

Buka file gambar sebagai stream. Menggunakan stream memungkinkan Anda membaca gambar dari sumber apa pun (sistem file, jaringan, basis data) tanpa harus menyimpannya terlebih dahulu ke disk.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Langkah 7: Menyisipkan Gambar

Buat objek `Image`. Argumen pertama dapat `null` ketika Anda menyediakan stream nanti, tetapi untuk kesederhanaan kami merujuk ke path file di sini dan mengatur perataan ke sisi kanan halaman.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Langkah 8: Menambahkan Gambar ke Elemen Garis Besar

Tambahkan gambar ke elemen outline sehingga menjadi bagian dari hierarki visual halaman.

```java
outlineElem1.appendChildLast(image);
```

## Langkah 9: Menambahkan Elemen Garis Besar ke Garis Besar

Sekarang lampirkan elemen outline (yang berisi gambar) ke wadah outline.

```java
outline1.appendChildLast(outlineElem1);
```

## Langkah 10: Menambahkan Garis Besar ke Halaman

Letakkan outline pada halaman.

```java
page.appendChildLast(outline1);
```

## Langkah 11: Menambahkan Halaman ke Dokumen

Tambahkan halaman yang telah selesai dibangun ke objek dokumen.

```java
doc.appendChildLast(page);
```

## Langkah 12: Menyimpan Dokumen

Akhirnya, simpan dokumen OneNote dalam format yang Anda butuhkan. Pada contoh ini kami mengekspor ke PDF, tetapi Anda dapat memilih format apa pun yang didukung oleh Aspose.Note.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Dengan mengikuti langkah‑langkah ini Anda telah berhasil **create onenote document java** dan menyematkan gambar menggunakan input stream.

## Kesalahan & Tip Umum

- **Stream tidak ditutup** – Dalam skenario produksi, selalu tutup `InputStream` di blok `finally` atau gunakan sumber daya coba-dengan-sumber daya. → Stream tidak ditutup – Dalam skenario produksi, selalu tutup `InputStream` di blok `finally` atau gunakan try‑with‑resources.
- **Jalur file salah** – Periksa kembali apakah `dataDir` diakhiri dengan pemisah yang sesuai (`/` atau `\`). → Path file tidak benar – Periksa kembali bahwa `dataDir` diakhiri dengan batas yang tepat (`/` atau `\`).
- **Penjajaran gambar** – Jika gambar muncul di luar layar, sesuaikan nilai `VerticalOffset`/`HorizontalOffset` garis luarnya. → Penjajaran gambar – Jika gambar muncul di luar layar, sesuaikan nilai `VerticalOffset`/`HorizontalOffset` pada outline.
- **Pengecualian lisensi** – Menggunakan versi evaluasi dapat menambahkan tanda air pada keluaran; terapkan lisensi yang valid untuk menghapusnya. → Pengecualian lisensi – Menggunakan versi evaluasi dapat menambahkan watermark pada output; menerapkan lisensi yang valid untuk menghilangkannya.

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.Note untuk Java kompatibel dengan semua versi OneNote?

A1: Aspose.Note untuk Java mendukung berbagai format file OneNote, memastikan kompatibilitas di seluruh versi desktop, online, dan seluler. → Aspose.Note for Java mendukung berbagai format file OneNote, memastikan kompatibilitas di versi desktop, online, dan seluler.

### Q2: Dapatkah saya mengkustomisasi tampilan gambar yang disisipkan dalam dokumen OneNote menggunakan Aspose.Note untuk Java?

A2: Ya, Anda dapat mengubah perataan, ukuran, rotasi, dan bahkan menerapkan pemotongan dengan menggunakan properti yang sesuai pada objek `Gambar`. → Ya, Anda dapat mengubah perataan, ukuran, rotasi, bahkan menerapkan pemotongan dengan menggunakan properti yang sesuai pada objek `Image`.

### Q3: Apakah Aspose.Note untuk Java menyediakan dukungan untuk format dokumen lain selain PDF?

A3: Tentu saja. API dapat mengekspor ke DOCX, HTML, XPS, dan beberapa format lainnya, memberi Anda fleksibilitas dalam cara berbagi atau mengarsipkan catatan Anda. → Tentu saja. API dapat mengekspor ke DOCX, HTML, XPS, dan beberapa format lainnya, memberi Anda kenangan dalam cara berbagi atau mengarsipkan catatan.

### Q4: Di mana saya dapat menemukan sumber daya tambahan dan dukungan untuk Aspose.Note untuk Java?

A4: Situs web resmi Aspose menawarkan dokumentasi ekstensif, contoh kode, forum, dan lisensi sementara untuk evaluasi. → Situs resmi Aspose menyediakan dokumentasi lengkap, contoh kode, forum, dan lisensi sementara untuk evaluasi.

### Q5: Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?

A5: Ya, Anda dapat mengunduh uji coba gratis dari halaman rilis Aspose untuk menjelajahi semua fitur sebelum membeli. → Ya, Anda dapat mengunduh versi percobaan gratis dari halaman rilis Aspose untuk menjelajahi semua fitur sebelum membeli.

---

**Terakhir Diperbarui:** 21-12-2025
**Diuji Dengan:** Aspose.Note untuk Java 24.12 (terbaru pada saat penulisan)
**Penulis:** Beranggapan  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}