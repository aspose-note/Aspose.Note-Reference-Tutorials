---
date: 2026-02-18
description: Pelajari cara mengatur gaya paragraf dan menambahkan elemen outline saat
  membuat dokumen OneNote dengan Java menggunakan Aspose.Note. Ekspor OneNote ke PDF,
  simpan OneNote sebagai PDF, dan hasilkan file OneNote dengan mudah.
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: Ekspor OneNote ke PDF – Atur Gaya Paragraf saat Membuat Dokumen OneNote dengan
  Java
url: /id/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Gaya Paragraf saat Membuat Dokumen OneNote dengan Java

## Pendahuluan

Dalam lanskap pengembangan yang bergerak cepat saat ini, kemampuan untuk **mengekspor OneNote ke PDF** secara programatik sangat penting untuk menghasilkan dokumen yang rapi dan siap dibagikan. Tutorial ini akan memandu Anda melalui pembuatan file OneNote, menerapkan gaya paragraf khusus, dan akhirnya **mengekspor OneNote ke PDF** menggunakan Aspose.Note untuk Java. Baik Anda sedang membangun mesin pelaporan, solusi pencatatan otomatis, atau layanan konversi dokumen, teknik yang dibahas di sini akan membantu Anda **menyimpan OneNote sebagai PDF** dengan kontrol format yang tepat.

## Jawaban Cepat
- **Apa arti “set paragraph style”?** Itu menerapkan font, ukuran, warna, dan format lainnya ke sebuah paragraf teks.  
- **Apakah saya dapat mengekspor hasilnya ke PDF?** Ya – tutorial berakhir dengan menyimpan file OneNote sebagai PDF.  
- **Apakah saya memerlukan lisensi untuk Aspose.Note?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi diperlukan untuk produksi.  
- **IDE mana yang didukung?** Semua IDE Java – Eclipse, IntelliJ IDEA, NetBeans, dll.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk dokumen dasar.

## Apa itu “set paragraph style” di Aspose.Note?
Mengatur gaya paragraf mengacu pada konfigurasi objek `ParagraphStyle` (nama font, ukuran, warna, dll.) dan melampirkannya ke node `RichText`. Ini memberi Anda kontrol penuh atas tampilan teks di dalam halaman OneNote.

## Bagaimana Cara Mengatur Gaya Paragraf di OneNote?
Menerapkan gaya semudah membuat instance `ParagraphStyle`, menyesuaikan propertinya, dan menetapkannya ke elemen `RichText`. API menjadikan ini operasi satu baris begitu objek gaya siap.

## Mengapa Mengekspor OneNote ke PDF?
- **Branding konsisten:** Mempertahankan font dan warna perusahaan saat membagikan catatan ke luar.  
- **Keterbacaan:** PDF menjaga tata letak persis, menjadikannya ideal untuk pencetakan atau pengarsipan.  
- **Akses lintas‑platform:** Penerima dapat melihat PDF di perangkat apa pun tanpa memerlukan OneNote.  

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK) 1.8+** – JDK terbaru mana pun akan berfungsi.  
2. **Aspose.Note untuk Java** – unduh JAR terbaru dari [halaman unduhan Aspose.Note](https://releases.aspose.com/note/java/).  
3. **IDE** (Eclipse, IntelliJ IDEA, atau NetBeans) untuk mengkompilasi dan menjalankan contoh.  

> **Tips pro:** Tambahkan JAR Aspose.Note ke classpath proyek Anda melalui Maven atau dengan mereferensikan JAR secara manual di IDE.

## Mengimpor Paket

Pertama, impor kelas‑kelas yang diperlukan. Blok ini tetap tidak berubah.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> Kelas `ParagraphStyle` adalah kunci untuk **set paragraph style** nanti dalam tutorial.

## Panduan Langkah‑per‑Langkah

Berikut adalah penjelasan singkat setiap operasi. Blok kode persis seperti contoh asli; kami hanya menambahkan teks penjelasan.

### Langkah 1: Atur Direktori Dokumen
Tentukan tempat file yang dihasilkan akan disimpan.

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur absolut atau relatif di mesin Anda.

### Langkah 2: Inisialisasi Objek Document
Buat `Document` root yang mewakili file OneNote.

```java
Document doc = new Document();
```

### Langkah 3: Inisialisasi Objek Page
File OneNote terdiri dari satu atau lebih halaman; kita mulai dengan satu halaman.

```java
Page page = new Page();
```

### Langkah 4: Inisialisasi Objek Outline
Outline berfungsi sebagai kontainer untuk elemen outline (anggap sebagai bagian).

```java
Outline outline = new Outline();
```

### Langkah 5: Inisialisasi Objek OutlineElement
Di sini kita **menambahkan outline element** yang akan menampung teks kaya kami.

```java
OutlineElement outlineElem = new OutlineElement();
```

### Langkah 6: Atur Gaya Teks (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Instansi `ParagraphStyle` mendefinisikan font, ukuran, dan warna—ini tempat kami **set paragraph style** untuk node teks yang akan datang.

### Langkah 7: Inisialisasi Objek RichText

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Kami membuat node `RichText`, menyisipkan string sederhana, dan melampirkan gaya yang telah didefinisikan sebelumnya.

### Langkah 8: Tambahkan Node RichText ke OutlineElement

```java
outlineElem.appendChildLast(text);
```

Sekarang teks yang telah bergaya berada di dalam outline element.

### Langkah 9: Tambahkan Node OutlineElement ke Outline

```java
outline.appendChildLast(outlineElem);
```

Outline kini berisi elemen yang memegang paragraf kami.

### Langkah 10: Tambahkan Node Outline ke Page

```java
page.appendChildLast(outline);
```

Kami menempatkan outline pada halaman.

### Langkah 11: Tambahkan Node Page ke Document

```java
doc.appendChildLast(page);
```

Dokumen kini memiliki satu halaman dengan teks bergaya kami.

### Langkah 12: Simpan Dokumen (Ekspor OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Metode `save` menulis file OneNote dan **mengekspor OneNote PDF** dalam satu langkah. Anda juga dapat menyimpan sebagai `.one` dengan menggunakan `SaveFormat.One` jika memerlukan format asli.

## Masalah Umum & Solusi

| Masalah | Penyebab | Solusi |
|-------|--------|-----|
| **File tidak ditemukan** | `dataDir` mengarah ke folder yang tidak ada. | Pastikan direktori ada atau buat secara programatis (`new File(dataDir).mkdirs();`). |
| **PDF kosong** | Tidak ada konten yang ditambahkan sebelum menyimpan. | Verifikasi bahwa node `RichText` telah ditambahkan dan gaya telah diatur. |
| **Font tidak didukung** | Nama font tidak terpasang di sistem. | Gunakan font umum seperti `"Arial"` atau sematkan font dalam proyek. |

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.Note dapat menangani format kompleks seperti tabel atau gambar?**  
J: Ya, API mendukung tabel, gambar, hyperlink, dan fitur tata letak lanjutan lainnya.

**T: Apakah memungkinkan untuk **convert OneNote PDF** kembali ke file OneNote?**  
J: Konversi langsung tidak disediakan, tetapi Anda dapat mengekstrak konten PDF dan membangun kembali dokumen OneNote menggunakan API.

**T: Apakah perpustakaan ini bekerja di lingkungan Linux/macOS?**  
J: Tentu. Aspose.Note untuk Java bersifat platform‑independen; cukup pastikan JDK terinstal.

**T: Bagaimana cara menambahkan beberapa halaman atau outline?**  
J: Buat objek `Page` dan `Outline` tambahan, lalu tambahkan ke `Document` seperti contoh satu halaman.

**T: Di mana saya dapat menemukan contoh lebih lanjut?**  
J: Dokumentasi resmi Aspose.Note dan [forum dukungan](https://forum.aspose.com/c/note/28) berisi banyak contoh kode.

## Kesimpulan

Anda kini telah melihat cara **set paragraph style**, **menambahkan outline element**, dan **menghasilkan file OneNote** yang dapat **diekspor ke PDF** menggunakan Aspose.Note untuk Java. Menyertakan teks bergaya sejak awal proses pembuatan memastikan dokumen akhir terlihat profesional dan setiap operasi **convert OneNote PDF** berikutnya mempertahankan formatnya. Jangan ragu untuk memperluas fondasi ini dengan gambar, tabel, atau metadata khusus sesuai kebutuhan proyek Anda.

---

**Terakhir Diperbarui:** 2026-02-18  
**Diuji Dengan:** Aspose.Note untuk Java 24.11 (rilis terbaru)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}