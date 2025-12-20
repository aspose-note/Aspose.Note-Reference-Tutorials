---
date: 2025-12-20
description: Pelajari cara menambahkan gambar ke OneNote menggunakan Aspose.Note untuk
  Java. Panduan langkah demi langkah untuk membuat dokumen OneNote dan menyisipkan
  gambar secara programatis.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Cara menambahkan gambar ke OneNote menggunakan Java – Membuat Dokumen dan Menyisipkan
  Gambar
url: /id/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menambahkan gambar ke OneNote menggunakan Java – Membuat Dokumen dan Menyisipkan Gambar

## Pendahuluan

Dalam tutorial ini, Anda akan belajar **cara menambahkan gambar ke OneNote** menggunakan Aspose.Note Java API. Kami akan memandu Anda membuat dokumen OneNote dari awal, menyisipkan gambar, dan menyimpan hasilnya sebagai PDF. Baik Anda sedang membangun alat pelaporan, mengotomatisasi pencatatan, atau sekadar perlu menyematkan grafik secara programatik, panduan ini memberikan jalur yang jelas dan praktis.

## Jawaban Cepat
- **Perpustakaan apa yang saya perlukan?** Aspose.Note untuk Java.  
- **Apakah saya dapat menyisipkan format gambar apa saja?** JPEG, PNG, BMP, GIF, dan lainnya didukung.  
- **Format output apa yang tersedia?** Anda dapat menyimpan sebagai OneNote, PDF, XPS, HTML, dll.  
- **Apakah saya memerlukan lisensi untuk produksi?** Ya, lisensi komersial diperlukan untuk penggunaan non‑trial.  
- **Apakah kode ini lintas‑platform?** Tentu – Java berjalan di Windows, Linux, dan macOS.

## Apa itu “menambahkan gambar ke OneNote”?
Menambahkan gambar ke OneNote berarti secara programatik menyematkan file gambar ke dalam halaman OneNote sehingga muncul bersama teks, outline, atau elemen lainnya. Aspose.Note API mengabstraksi format file OneNote, memungkinkan Anda fokus pada konten tanpa harus mengelola struktur XML yang mendasarinya.

## Mengapa menambahkan gambar ke OneNote menggunakan Java?
- **Otomatisasi:** Menghasilkan notulen rapat dengan tangkapan layar secara otomatis.  
- **Konsistensi:** Memastikan setiap halaman mengikuti tata letak dan branding yang sama.  
- **Integrasi:** Menggabungkan data dari sistem lain (misalnya, grafik) langsung ke dalam notebook OneNote.  
- **Lintas‑platform:** Java memungkinkan Anda menjalankan kode yang sama di server atau desktop mana pun.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal‑hal berikut:

1. **Java Development Kit (JDK)** – versi terbaru (8 atau lebih tinggi).  
2. **Aspose.Note untuk Java** – unduh dari [situs web](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau editor Java lain yang Anda sukai.  

## Mengimpor Paket

Mulailah dengan mengimpor kelas‑kelas yang diperlukan dalam file sumber Java Anda:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Menyiapkan Dokumen

Buat dokumen OneNote baru dan kontainer halaman tempat konten akan ditempatkan.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Langkah 2: Menginisialisasi Outline

Sebuah *outline* berfungsi sebagai kontainer untuk elemen seperti teks dan gambar. Kami mengatur offset‑nya ke nol sehingga konten mulai dari sudut kiri‑atas.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Langkah 3: Memuat dan Menyelaraskan Gambar

Muat gambar yang ingin Anda sematkan dan sejajarkan ke sisi kanan halaman. Di sinilah kita **menambahkan gambar ke OneNote**.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Langkah 4: Menempelkan Gambar ke Elemen Outline

Bungkus gambar di dalam `OutlineElement`. Langkah ini menghubungkan objek visual ke hierarki outline dokumen.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Langkah 5: Menyusun Struktur Dokumen

Tambahkan elemen outline ke outline, lalu lampirkan outline ke halaman, dan akhirnya tambahkan halaman ke dokumen.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Langkah 6: Menyimpan Dokumen OneNote

Persistensikan dokumen ke disk. Pada contoh ini kami mengekspor ke PDF, tetapi Anda juga dapat menyimpan sebagai file OneNote asli (`.one`) dengan mengubah `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Masalah Umum dan Solusinya

| Masalah | Mengapa Terjadi | Solusi |
|---------|-----------------|--------|
| **Gambar tidak muncul** | Jalur file salah atau format tidak didukung. | Pastikan `dataDir` mengarah ke folder yang benar dan gunakan tipe gambar yang didukung (JPEG, PNG, dll.). |
| **Dokumen disimpan sebagai PDF kosong** | Offset outline diatur tidak tepat. | Pastikan `setVerticalOffset(0)` dan `setHorizontalOffset(0)` dipanggil, atau sesuaikan offset agar konten berada dalam batas halaman. |
| **IOException saat menyimpan** | Folder tujuan tidak ada atau tidak memiliki izin menulis. | Buat folder terlebih dahulu atau jalankan program dengan izin yang sesuai. |

## Pertanyaan yang Sering Diajukan

**T1: Di mana saya dapat menemukan dokumentasi untuk Aspose.Note untuk Java?**  
J: Anda dapat mengakses dokumentasi [di sini](https://reference.aspose.com/note/java/).

**T2: Bagaimana cara mengunduh Aspose.Note untuk Java?**  
J: Anda dapat mengunduh Aspose.Note untuk Java dari [halaman unduhan](https://releases.aspose.com/note/java/).

**T3: Apakah ada versi percobaan gratis untuk Aspose.Note untuk Java?**  
J: Ya, Anda dapat memperoleh percobaan gratis dari [situs web](https://releases.aspose.com/).

**T4: Di mana saya dapat mendapatkan dukungan untuk Aspose.Note untuk Java?**  
J: Untuk dukungan, kunjungi [forum Aspose.Note](https://forum.aspose.com/c/note/28).

**T5: Bisakah saya memperoleh lisensi sementara untuk Aspose.Note untuk Java?**  
J: Ya, Anda dapat meminta lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

---

**Terakhir Diperbarui:** 2025-12-20  
**Diuji Dengan:** Aspose.Note untuk Java 24.12 (terbaru)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}