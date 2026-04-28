---
date: 2025-12-21
description: Pelajari cara mendapatkan dimensi gambar di Java menggunakan Aspose.Note.
  Ekstrak lebar, tinggi, nama file, dan lainnya dari file OneNote hanya dalam beberapa
  langkah.
linktitle: Get Image Dimensions Java from OneNote
second_title: Aspose.Note Java API
title: Dapatkan Dimensi Gambar Java dari OneNote
url: /id/java/onenote-hyperlinks-images/get-image-info/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dapatkan Dimensi Gambar Java dari OneNote

## Perkenalan

Jika Anda perlu **dapatkan dimensi gambar java** dari notebook OneNote, Anda berada di tempat yang tepat. Dalam banyak skenario otomatis—pembuatan laporan, migrasi konten, atau analitik—Anda akan ingin mengetahui lebar, tinggi, ukuran asli, dan nama file setiap gambar tanpa harus membuka notebook secara manual. Tutorial ini memandu Anda mengekstrak informasi tersebut secara terprogram menggunakan Aspose.Note for Java.

## Jawaban Cepat
- **Apa fungsi kodenya?** Mengambil setiap gambar dalam file OneNote dan mencetak dimensinya, ukuran asli, nama file, serta tanggal modifikasi.
- **Perpustakaan mana yang diperlukan?** Aspose.Note untuk Java.
- **Apakah saya memerlukan lisensi?** Lisensi sementara dapat digunakan untuk pengujian; lisensi penuh diperlukan untuk produksi.
- **Berapa baris kode?** Sekitar 30 baris, dibagi menjadi langkah‑langkah yang jelas dan dapat digunakan kembali.
- **Waktu berjalan tipikal?** Milidetik untuk notebook standar dengan beberapa puluh gambar.

## Prasyarat

Sebelum kita masuk ke implementasi, pastikan Anda memiliki prasyarat berikut:

### 1. Kit Pengembangan Java (JDK)

Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda. Anda dapat mengunduh dan menginstal JDK terbaru dari [situs web Oracle](https://www.oracle.com/java/technologies/downloads/).

### 2. Aspose.Note untuk Perpustakaan Java

Unduh dan sertakan pustaka Aspose.Note for Java dalam proyek Anda. Anda dapat memperoleh pustaka tersebut dari [halaman unduh](https://releases.aspose.com/note/java/).

### 3. Dokumen OneNote

Siapkan dokumen OneNote contoh yang berisi gambar. Dokumen ini akan digunakan untuk mengekstrak informasi gambar secara terprogram.

## Impor Paket

Untuk memulai, impor paket yang diperlukan dari Aspose.Note untuk Java:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Mari kita uraikan kode di atas menjadi instruksi langkah‑demi‑langkah:

## Cara mendapatkan dimensi gambar java dari OneNote

### Langkah 1: Tetapkan Direktori Dokumen

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur ke dokumen OneNote Anda.

### Langkah 2: Muat Dokumen

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Muat dokumen OneNote menggunakan pustaka Aspose.Note for Java. Pastikan Anda memberikan jalur yang benar ke dokumen Anda.

### Langkah 3: Dapatkan Semua Gambar

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Ambil semua gambar dari dokumen OneNote yang telah dimuat.

### Langkah 4: Cetak Jumlah Total Gambar

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Cetak total jumlah gambar yang ditemukan dalam dokumen.

### Langkah 5: Telusuri dan Cetak Informasi Gambar

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Iterasi melalui daftar gambar dan cetak detail seperti lebar, tinggi, dimensi asli, nama file, serta waktu terakhir dimodifikasi untuk setiap gambar.

## Mengapa mengekstrak gambar dari OneNote menggunakan Java?

- **Otomasi:** Menghilangkan buku catatan manual inspeksi.
- **Analisis Data:** Menyalurkan metadata gambar ke jalur pelaporan.
- **Migrasi:** Mempertahankan atribut gambar saat memindahkan konten ke platform lain.
- **Kinerja:** Hanya menggunakan metadata yang Anda perlukan, menghindari penguraian file yang berat.

## Kesalahan & Tip Umum

- **Jalur salah:**Periksa kembali bahwa `dataDir` diakhiri dengan batas file yang tepat (`/` atau `\`).
- **Masalah lisensi:** Tanpa lisensi yang valid, Aspose.Note dapat menampilkan peringatan evaluasi.
- **Buku catatan besar:** Untuk buku catatan dengan ribuan gambar, memproses proses dalam batch untuk mengurangi konsumsi memori.

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah Aspose.Note untuk Java menangani format dokumen lain selain OneNote?

A1: Ya, Aspose.Note for Java mendukung berbagai format dokumen, termasuk OneNote, PDF, dan Microsoft Word.

### Q2: Apakah Aspose.Note untuk Java cocok untuk penggunaan pribadi dan komersial?

A2: Ya, Anda dapat menggunakan Aspose.Note for Java untuk keperluan pribadi maupun komersial.

### Q3: Apakah Aspose.Note untuk Java menawarkan dukungan teknis?

A3: Ya, dukungan teknis tersedia melalui forum Aspose di [di sini](https://forum.aspose.com/c/note/28).

### Q4: Dapatkah saya mencoba Aspose.Note untuk Java sebelum melakukan pembelian?

A4: Ya, Anda dapat menjelajahi versi percobaan gratis Aspose.Note for Java dari [Aspose.Note for Java](https://releases.aspose.com/note/java/).

### Q5: Bagaimana cara mendapatkan lisensi sementara Aspose.Note untuk Java?

A5: Anda dapat memperoleh lisensi sementara dari [Lisensi sementara/](https://purchase.aspose.com/temporary-license/).

## Kesimpulan

Dengan mengikuti langkah‑langkah yang dijelaskan dalam tutorial ini, Anda dapat secara efektif **mendapatkan dimensi gambar java** dari dokumen OneNote menggunakan Aspose.Note for Java. Mengintegrasikan fungsionalitas ini ke dalam aplikasi Anda dapat mengotomatisasi tugas terkait pemrosesan dokumen, meningkatkan efisiensi dan produktivitas.

---

**Terakhir Diperbarui:** 21-12-2025
**Diuji Dengan:** Aspose.Note untuk Java 26.4
**Penulis:** Beranggapan 

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
