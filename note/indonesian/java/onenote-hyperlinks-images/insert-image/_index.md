---
date: 2026-03-19
description: Pelajari cara menambahkan gambar ke OneNote menggunakan Java dengan Aspose.Note
  untuk Java, termasuk cara mengatur dimensi gambar di Java dan menyimpan OneNote
  sebagai PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Tambahkan gambar ke OneNote menggunakan Java
url: /id/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menyisipkan Gambar dalam Dokumen OneNote dengan Java

## Pendahuluan

Dalam tutorial ini Anda akan belajar **cara menambahkan gambar ke OneNote** secara programatis menggunakan Java dan pustaka Aspose.Note for Java. Menyisipkan gambar ke halaman OneNote sangat berguna ketika Anda perlu menghasilkan notulen rapat, laporan otomatis, atau dokumentasi yang menggabungkan teks dengan data visual. Pada akhir panduan Anda akan dapat memuat file OneNote yang sudah ada, menyisipkan gambar, secara opsional menyesuaikan ukuran dan posisinya, bahkan **menyimpan OneNote sebagai PDF** – semuanya tanpa membuka UI OneNote.

## Jawaban Cepat
- **Apa cara termudah menambahkan gambar ke OneNote menggunakan Java?**  
  Gunakan kelas `Image` dari Aspose.Note for Java dan tambahkan ke halaman.
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?**  
  Ya, lisensi komersial diperlukan untuk penerapan produksi.
- **Bisakah saya mengatur dimensi khusus untuk gambar?**  
  Tentu – panggil `setWidth()` dan `setHeight()` pada objek `Image`.
- **Apakah memungkinkan menyimpan file OneNote sebagai PDF setelah menambahkan gambar?**  
  Ya, panggil `save(..., SaveFormat.Pdf)` untuk **menyimpan OneNote sebagai PDF**.
- **Versi Java mana yang didukung?**  
  Aspose.Note for Java bekerja dengan JDK 8 dan yang lebih baru.

## Mengapa menambahkan gambar ke OneNote?

Menambahkan elemen visual membuat catatan lebih mudah dipahami dan lebih menarik. Gambar dapat menggambarkan diagram, tangkapan layar, atau grafik data yang sebaliknya memerlukan deskripsi teks yang panjang. Mengotomatiskan langkah ini menghemat waktu, terutama saat menghasilkan banyak catatan dari sumber data.

## Prasyarat

Sebelum memulai, pastikan Anda telah menyiapkan hal‑hal berikut:

### 1. Java Development Kit (JDK)
Instal JDK 8 atau yang lebih baru. Anda dapat mengunduhnya dari situs Oracle atau menggunakan distribusi OpenJDK.

### 2. Pustaka Aspose.Note for Java
Unduh pustaka Aspose.Note for Java terbaru dan tambahkan ke classpath proyek Anda. Instruksi penyiapan detail tersedia di [dokumentasi resmi](https://reference.aspose.com/note/java/).

## Mengimpor Paket

Mulailah dengan mengimpor kelas‑kelas yang diperlukan. Impor ini memberi Anda akses ke fungsionalitas inti Aspose.Note serta utilitas dasar Java.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Panduan Langkah‑per‑Langkah

Berikut adalah walkthrough singkat yang bernomor. Setiap langkah mencakup penjelasan singkat diikuti kode yang harus Anda salin.

### Langkah 1: Memuat dokumen OneNote

Kami membuat instance `LoadOptions` (berguna untuk kustomisasi di masa depan) dan membuka file `.one` yang sudah ada.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### Langkah 2: Mendapatkan halaman target

Untuk kesederhanaan kami bekerja dengan halaman pertama dalam dokumen, tetapi Anda dapat menavigasi ke halaman mana pun yang diperlukan.

```java
Page page = oneFile.getFirstChild();
```

### Langkah 3: Memuat gambar yang ingin disisipkan

Instansiasikan objek `Image` dengan memberikan referensi dokumen dan jalur ke file gambar.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### Langkah 4: Mengatur dimensi gambar Java (opsional)

Jika Anda memerlukan gambar agar sesuai dengan area tertentu, sesuaikan lebar, tinggi, dan offsetnya. Di sinilah kata kunci sekunder **set image dimensions java** berperan.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### Langkah 5: Menambahkan gambar ke halaman

Metode `appendChildLast` menambahkan gambar sebagai elemen terakhir pada halaman yang dipilih.

```java
page.appendChildLast(image);
```

### Langkah 6: Menyimpan dokumen – Anda juga dapat menyimpan OneNote sebagai PDF

Akhirnya, persist perubahan. Contoh ini menunjukkan cara menyimpan file sebagai PDF, memenuhi kata kunci sekunder **save onenote as pdf**.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Masalah Umum dan Solusinya

| Gejala | Penyebab Kemungkinan | Solusi |
|--------|----------------------|--------|
| `FileNotFoundException` saat memuat gambar | Jalur gambar tidak tepat | Verifikasi bahwa `dataDir` dan nama file gambar sudah benar. |
| Gambar tampak terdistorsi | Lebar/tinggi diatur tidak tepat | Gunakan dimensi asli gambar atau hitung rasio aspek yang tepat sebelum memanggil `setWidth`/`setHeight`. |
| Output PDF kosong | Lisensi Aspose.Note belum diterapkan | Terapkan lisensi yang valid sebelum memanggil `save`. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menyisipkan beberapa gambar ke dalam satu dokumen OneNote menggunakan metode ini?

**A:** Ya. Cukup ulangi Langkah 3‑5 untuk setiap gambar yang ingin Anda tambahkan, baik pada halaman yang sama maupun berbeda.

### Q2: Apakah Aspose.Note for Java kompatibel dengan semua versi OneNote?

**A:** Aspose.Note for Java mendukung file OneNote yang dibuat dengan Microsoft OneNote 2010 dan versi yang lebih baru.

### Q3: Bisakah saya menyisipkan gambar dengan format berbeda, seperti PNG atau GIF, ke dalam dokumen OneNote?

**A:** Tentu. Pustaka ini menerima PNG, JPEG, GIF, BMP, dan beberapa format umum lainnya.

### Q4: Apakah ada versi percobaan Aspose.Note for Java yang tersedia untuk tujuan pengujian?

**A:** Ya, Anda dapat mengunduh versi percobaan gratis dari situs Aspose untuk mengevaluasi API sebelum membeli.

### Q5: Bagaimana cara mendapatkan dukungan teknis untuk Aspose.Note for Java?

**A:** Anda dapat memperoleh bantuan dengan mengunjungi [forum](https://forum.aspose.com/c/note/28) yang didedikasikan untuk produk Aspose.Note.

## Kesimpulan

Anda kini memiliki contoh lengkap yang siap produksi yang menunjukkan **cara menambahkan gambar ke OneNote** menggunakan Java, menyesuaikan tampilannya, dan secara opsional **menyimpan OneNote sebagai PDF**. Silakan sesuaikan kode dengan alur kerja Anda—baik Anda membangun mesin pelaporan, sistem dokumentasi otomatis, atau aplikasi pencatatan khusus.

---

**Terakhir Diperbarui:** 2026-03-19  
**Diuji Dengan:** Aspose.Note for Java 24.10  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}