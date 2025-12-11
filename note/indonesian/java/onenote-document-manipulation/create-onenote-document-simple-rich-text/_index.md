---
date: 2025-12-08
description: Pelajari cara mengatur gaya paragraf dan menambahkan elemen outline saat
  membuat dokumen OneNote dalam Java menggunakan Aspose.Note. Ekspor OneNote ke PDF
  dan buat file OneNote dengan mudah.
language: id
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: Atur Gaya Paragraf saat Membuat Dokumen OneNote dalam Java
url: /java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Gaya Paragraf saat Membuat Dokumen OneNote di Java

## Pendahuluan

Dalam lanskap pengembangan yang bergerak cepat saat ini, kemampuan untuk **set paragraph style** secara programatik sangat penting untuk menghasilkan file OneNote yang halus. Tutorial ini menunjukkan kepada Anda, langkah demi langkah, cara menghasilkan dokumen OneNote dengan teks kaya sederhana, menerapkan pemformatan paragraf khusus, dan akhirnya **export OneNote to PDF** menggunakan Aspose.Note for Java. Apakah Anda sedang membangun mesin pelaporan, solusi pencatatan otomatis, atau layanan konversi dokumen, teknik yang dibahas di sini akan membantu Anda **generate OneNote files** yang terlihat persis seperti yang Anda inginkan.

## Jawaban Cepat
- **What does “set paragraph style” mean?** Ini menerapkan font, ukuran, warna, dan pemformatan lainnya ke sebuah paragraf teks.  
- **Can I export the result to PDF?** Ya – tutorial berakhir dengan menyimpan file OneNote sebagai PDF.  
- **Do I need a license for Aspose.Note?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi diperlukan untuk produksi.  
- **Which IDEs are supported?** Setiap IDE Java – Eclipse, IntelliJ IDEA, NetBeans, dll.  
- **How long does the implementation take?** Sekitar 10‑15 menit untuk dokumen dasar.

## Apa itu “set paragraph style” dalam Aspose.Note?

Setting paragraph style mengacu pada mengkonfigurasi objek `ParagraphStyle` (nama font, ukuran, warna, dll.) dan melampirkannya ke node `RichText`. Ini memberi Anda kontrol penuh atas bagaimana teks muncul di dalam halaman OneNote.

## Mengapa mengatur gaya paragraf saat menghasilkan file OneNote?

- **Consistent branding:** Terapkan font dan warna perusahaan secara otomatis.  
- **Readability:** Font yang lebih besar atau warna tertentu meningkatkan aksesibilitas.  
- **Export fidelity:** Teks yang bergaya dipertahankan ketika Anda **convert OneNote PDF** nanti.  

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK) 1.8+** – JDK terbaru apa pun akan berfungsi.  
2. **Aspose.Note for Java** – unduh JAR terbaru dari [Aspose.Note download page](https://releases.aspose.com/note/java/).  
3. **An IDE** (Eclipse, IntelliJ IDEA, atau NetBeans) untuk mengompilasi dan menjalankan contoh.  

> **Pro tip:** Tambahkan JAR Aspose.Note ke classpath proyek Anda melalui Maven atau dengan secara manual merujuk JAR di IDE Anda.

## Impor Paket

Pertama, impor kelas yang akan kita butuhkan. Blok ini tetap tidak berubah.

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

Berikut adalah penjelasan singkat dari setiap operasi. Blok kode persis seperti contoh asli; kami hanya menambahkan teks penjelasan.

### Langkah 1: Atur Direktori Dokumen
Tentukan di mana file yang dihasilkan akan disimpan.

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
File OneNote terdiri dari satu atau lebih halaman; kami mulai dengan satu halaman.

```java
Page page = new Page();
```

### Langkah 4: Inisialisasi Objek Outline
Outline berfungsi sebagai wadah untuk elemen outline (anggap sebagai bagian).

```java
Outline outline = new Outline();
```

### Langkah 5: Inisialisasi Objek OutlineElement
Di sini kami **add outline element** yang akan menampung teks kaya kami.

```java
OutlineElement outlineElem = new OutlineElement();
```

### Langkah 6: Set Text Style (Set Paragraph Style)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Instansi `ParagraphStyle` mendefinisikan font, ukuran, dan warna—di sinilah kami **set paragraph style** untuk node teks yang akan datang.

### Langkah 7: Inisialisasi Objek RichText

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Kami membuat node `RichText`, menyisipkan string sederhana, dan melampirkan gaya yang telah didefinisikan sebelumnya.

### Langkah 8: Add RichText Node to OutlineElement

```java
outlineElem.appendChildLast(text);
```

Sekarang teks yang bergaya berada di dalam elemen outline.

### Langkah 9: Add OutlineElement Node to Outline

```java
outline.appendChildLast(outlineElem);
```

Outline kini berisi elemen yang menampung paragraf kami.

### Langkah 10: Add Outline Node to Page

```java
page.appendChildLast(outline);
```

Kami menempatkan outline ke halaman.

### Langkah 11: Add Page Node to Document

```java
doc.appendChildLast(page);
```

Dokumen kini memiliki satu halaman dengan teks bergaya kami.

### Langkah 12: Save the Document (Export OneNote PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Metode `save` menulis file OneNote dan **exports OneNote PDF** dalam satu langkah. Anda juga dapat menyimpan sebagai `.one` dengan menggunakan `SaveFormat.One` jika memerlukan format asli.

## Masalah Umum & Solusi

| Issue | Reason | Fix |
|-------|--------|-----|
| **File not found** | `dataDir` mengarah ke folder yang tidak ada. | Pastikan direktori ada atau buat secara programatis (`new File(dataDir).mkdirs();`). |
| **Blank PDF** | Tidak ada konten yang ditambahkan sebelum menyimpan. | Verifikasi bahwa node `RichText` telah ditambahkan dan gaya telah diatur. |
| **Unsupported font** | Nama font tidak terpasang di sistem. | Gunakan font umum seperti `"Arial"` atau sematkan font dalam proyek. |

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.Note dapat menangani pemformatan kompleks seperti tabel atau gambar?**  
A: Ya, API mendukung tabel, gambar, hyperlink, dan fitur tata letak yang lebih canggih.

**Q: Apakah memungkinkan untuk **convert OneNote PDF** kembali ke file OneNote?**  
A: Konversi langsung tidak disediakan, tetapi Anda dapat mengekstrak konten PDF dan membangun kembali dokumen OneNote menggunakan API.

**Q: Apakah perpustakaan ini bekerja di lingkungan Linux/macOS?**  
A: Tentu saja. Aspose.Note for Java bersifat platform‑independen; pastikan JDK terpasang.

**Q: Bagaimana cara menambahkan beberapa halaman atau outline?**  
A: Buat objek `Page` dan `Outline` tambahan, lalu tambahkan ke `Document` seperti contoh satu halaman.

**Q: Di mana saya dapat menemukan contoh lainnya?**  
A: Dokumentasi resmi Aspose.Note dan [forum dukungan](https://forum.aspose.com/c/note/28) berisi banyak contoh kode.

## Kesimpulan

Anda sekarang telah melihat cara **set paragraph style**, **add outline element**, dan **generate a OneNote file** yang dapat **exported to PDF** menggunakan Aspose.Note for Java. Menggabungkan teks bergaya sejak awal proses pembuatan memastikan dokumen akhir terlihat profesional dan setiap operasi **convert OneNote PDF** selanjutnya mempertahankan pemformatan. Jangan ragu untuk memperluas fondasi ini dengan gambar, tabel, atau metadata khusus untuk memenuhi kebutuhan proyek Anda.

---

**Terakhir Diperbarui:** 2025-12-08  
**Diuji Dengan:** Aspose.Note for Java 24.11 (latest release)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}