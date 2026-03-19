---
date: 2026-03-19
description: Pelajari cara membuat dokumen OneNote menggunakan Aspose.Note untuk Java
  dan menyisipkan gambar dari aliran. Panduan langkah demi langkah untuk pengembang
  Java.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Cara membuat dokumen OneNote dengan Java – Membuat Dokumen dan Menyisipkan
  Gambar dengan Stream
url: /id/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara membuat dokumen onenote java – Membuat Dokumen dan Menyisipkan Gambar dengan Stream

## Pendahuluan

Selamat datang! Dalam tutorial ini Anda akan **membuat onenote document java** dari awal dan belajar cara menyisipkan gambar menggunakan aliran gambar. Kami akan membimbing Anda melalui setiap langkah, menjelaskan mengapa setiap bagian penting, dan memberikan tip praktis agar Anda dapat menerapkan teknik ini dalam proyek nyata. Pada akhir tutorial, Anda akan dapat menghasilkan halaman OneNote secara programatis dan menyisipkan gambar tepat di tempat yang Anda inginkan.

## Jawaban Cepat
- **Perpustakaan apa yang saya butuhkan?** Aspose.Note for Java  
- **Bisakah saya menyisipkan gambar dari stream?** Ya – cukup berikan `InputStream` ke konstruktor `Image`.  
- **Format apa yang dapat saya ekspor?** Format apa pun yang didukung oleh Aspose.Note, misalnya PDF, DOCX, HTML.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Lisensi sementara gratis dapat digunakan untuk evaluasi; lisensi penuh diperlukan untuk produksi.  
- **Versi Java apa yang diperlukan?** Java 8 atau lebih tinggi.

## Apa itu “create onenote document java”?

Membuat dokumen OneNote dalam Java berarti menggunakan API Aspose.Note untuk secara programatis membangun struktur notebook—halaman, outline, dan elemen—tanpa membuka klien desktop OneNote. Pendekatan ini ideal untuk pembuatan laporan otomatis, pemrosesan batch catatan, atau mengintegrasikan konten OneNote ke dalam aplikasi Java yang lebih besar.

## Mengapa menggunakan Aspose.Note for Java untuk membuat onenote document java?

- **Kontrol penuh** atas tata letak halaman, posisi outline, dan gaya elemen.  
- **Tanpa interop COM** – berfungsi pada sistem operasi apa pun yang mendukung Java.  
- **Opsi ekspor kaya** – mengonversi dokumen yang sama ke PDF, DOCX, HTML, dll., dengan satu panggilan.  
- **Ramahan stream** – Anda dapat memuat gambar langsung dari memori, jaringan, atau penyimpanan cloud.

## Prasyarat

Sebelum kita mulai, pastikan Anda telah menyiapkan hal berikut:

### Java Development Kit (JDK)

JDK terbaru (8 atau lebih tinggi) yang terpasang di mesin Anda.

### Perpustakaan Aspose.Note untuk Java

Unduh perpustakaan dari halaman rilis resmi Aspose: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### Pengaturan IDE

Konfigurasikan IDE favorit Anda (IntelliJ IDEA, Eclipse, VS Code) untuk menyertakan file JAR Aspose.Note pada classpath proyek.

## Impor Paket

Untuk memulai, impor kelas Java dan Aspose.Note yang diperlukan. Impor ini memberi Anda akses ke pembuatan dokumen, penanganan halaman, manajemen outline, dan penyisipan gambar.

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

## Langkah 1: Siapkan Direktori Dokumen

Tentukan folder yang berisi gambar sumber Anda dan tempat file output akan disimpan. Ganti placeholder dengan path sebenarnya di mesin Anda.

```java
String dataDir = "Your Document Directory";
```

## Langkah 2: Buat Objek Dokumen

Instansiasi `Document` baru. Objek ini mewakili notebook OneNote yang Anda bangun.

```java
Document doc = new Document();
```

## Langkah 3: Inisialisasi Objek Halaman

Buat `Page` yang akan menampung semua outline dan elemen untuk halaman notebook ini.

```java
Page page = new Page();
```

## Langkah 4: Buat Outline

`Outline` berfungsi sebagai wadah untuk elemen yang diposisikan. Di sini kami mengatur offset vertikal dan horizontal untuk menempatkan outline pada halaman.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Langkah 5: Buat Elemen Outline

`OutlineElement` akan menampung gambar yang akan kami sisipkan.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Langkah 6: Muat Stream Gambar

Buka file gambar sebagai stream. Menggunakan stream memungkinkan Anda membaca gambar dari sumber apa pun (sistem file, jaringan, basis data) tanpa harus menyimpannya ke disk terlebih dahulu.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Langkah 7: Sisipkan Gambar

Buat objek `Image`. Argumen pertama dapat `null` ketika Anda menyediakan stream nanti, tetapi untuk kesederhanaan kami merujuk ke path file di sini dan mengatur perataan ke sisi kanan halaman.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Langkah 8: Tambahkan Gambar ke Elemen Outline

Tambahkan gambar ke elemen outline sehingga menjadi bagian dari hierarki visual halaman.

```java
outlineElem1.appendChildLast(image);
```

## Langkah 9: Tambahkan Elemen Outline ke Outline

Sekarang lampirkan elemen outline (yang berisi gambar) ke wadah outline.

```java
outline1.appendChildLast(outlineElem1);
```

## Langkah 10: Tambahkan Outline ke Halaman

Letakkan outline pada halaman.

```java
page.appendChildLast(outline1);
```

## Langkah 11: Tambahkan Halaman ke Dokumen

Tambahkan halaman yang telah selesai dibangun ke objek dokumen.

```java
doc.appendChildLast(page);
```

## Langkah 12: Simpan Dokumen

Akhirnya, simpan dokumen OneNote dalam format yang Anda butuhkan. Pada contoh ini kami mengekspor ke PDF, tetapi Anda dapat memilih format apa pun yang didukung oleh Aspose.Note.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Dengan mengikuti langkah-langkah ini Anda telah berhasil **membuat onenote document java** dan menyisipkan gambar menggunakan input stream.

## Kesalahan Umum & Tips

- **Stream tidak ditutup** – Dalam skenario produksi, selalu tutup `InputStream` dalam blok `finally` atau gunakan try‑with‑resources.  
- **Path file tidak benar** – Periksa kembali bahwa `dataDir` diakhiri dengan pemisah yang tepat (`/` atau `\`).  
- **Perataan gambar** – Jika gambar muncul di luar layar, sesuaikan nilai `VerticalOffset`/`HorizontalOffset` pada outline.  
- **Pengecualian lisensi** – Menggunakan versi evaluasi dapat menambahkan watermark pada output; terapkan lisensi yang valid untuk menghilangkannya.

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.Note untuk Java kompatibel dengan semua versi OneNote?

J1: Aspose.Note untuk Java mendukung berbagai format file OneNote, memastikan kompatibilitas di versi desktop, online, dan mobile.

### Q2: Apakah saya dapat menyesuaikan tampilan gambar yang disisipkan dalam dokumen OneNote menggunakan Aspose.Note untuk Java?

J2: Ya, Anda dapat mengubah perataan, ukuran, rotasi, dan bahkan menerapkan pemotongan dengan menggunakan properti yang sesuai pada objek `Image`.

### Q3: Apakah Aspose.Note untuk Java menyediakan dukungan untuk format dokumen lain selain PDF?

J3: Tentu saja. API dapat mengekspor ke DOCX, HTML, XPS, dan beberapa format lainnya, memberi Anda fleksibilitas dalam cara berbagi atau mengarsipkan catatan Anda.

### Q4: Di mana saya dapat menemukan sumber daya tambahan dan dukungan untuk Aspose.Note untuk Java?

J4: Situs resmi Aspose menyediakan dokumentasi lengkap, contoh kode, forum, dan lisensi sementara untuk evaluasi.

### Q5: Apakah ada versi percobaan yang tersedia untuk Aspose.Note untuk Java?

J5: Ya, Anda dapat mengunduh versi percobaan gratis dari halaman rilis Aspose untuk menjelajahi semua fitur sebelum membeli.

## Kesimpulan

Anda kini memiliki contoh lengkap, end‑to‑end tentang cara **membuat onenote document java** dan menyisipkan gambar langsung dari `InputStream`. Jangan ragu untuk bereksperimen dengan elemen tambahan—teks, tabel, atau bentuk—untuk memperkaya catatan Anda. Saat Anda siap, jelajahi banyak opsi ekspor yang disediakan Aspose.Note untuk membagikan konten OneNote Anda sebagai PDF, DOCX, HTML, dan lainnya.

---

**Terakhir Diperbarui:** 2026-03-19  
**Diuji Dengan:** Aspose.Note for Java 24.12 (latest at time of writing)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}