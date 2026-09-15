---
date: 2026-03-05
description: Pelajari cara menyimpan OneNote sebagai PDF sambil membuat daftar bernomor
  menggunakan Aspose.Note untuk Java. Termasuk langkah-langkah untuk mengatur gaya
  teks default dan menyesuaikan penomoran.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: Simpan OneNote sebagai PDF – Buat Daftar Bernomor dengan Aspose.Note
url: /id/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan OneNote sebagai PDF – Buat Daftar Bernomor dengan Aspose.Note

## Pendahuluan
Aspose.Note for Java memungkinkan pengembang Java untuk **menyimpan OneNote sebagai PDF** dan memperkaya dokumen dengan pemformatan lanjutan, seperti daftar bernomor. Dalam tutorial ini, kami akan memandu Anda melalui proses lengkap—dari mengatur gaya teks default hingga menyesuaikan format penomoran—sehingga Anda dapat mengekspor OneNote ke PDF dengan tampilan profesional.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Membuat daftar bernomor di OneNote dan menyimpan file sebagai PDF menggunakan Aspose.Note for Java.  
- **Kata kunci utama apa yang ditargetkan?** *save onenote as pdf*  
- **Apakah saya memerlukan lisensi?** Tersedia versi percobaan gratis; lisensi komersial diperlukan untuk produksi.  
- **Versi Java apa yang diperlukan?** JDK 8 atau lebih baru.  
- **Berapa lama implementasinya?** Sekitar 10–15 menit untuk daftar dasar.

## Apa itu “save OneNote as PDF”?
Menyimpan OneNote sebagai PDF mengonversi halaman OneNote berformat rich‑text menjadi dokumen portabel dengan tata letak tetap yang dapat dibagikan lintas platform tanpa memerlukan OneNote. Ini sangat berguna untuk pengarsipan, pelaporan, atau mendistribusikan konten kepada pengguna yang tidak memiliki OneNote terpasang.

## Mengapa membuat daftar bernomor sebelum mengekspor?
Daftar bernomor menambah struktur dan keterbacaan, membuat PDF yang diekspor terlihat seperti laporan yang rapi. Dengan Aspose.Note Anda dapat **menyesuaikan format penomoran**, mengatur font, dan mengontrol spasi—semua sambil mempertahankan tata letak OneNote asli.

## Prasyarat
Sebelum memulai, pastikan Anda memiliki:

- Java Development Kit (JDK) terpasang di mesin Anda.  
- Perpustakaan Aspose.Note for Java diunduh dari [di sini](https://releases.aspose.com/note/java/).  

## Mengimpor Paket
Pertama, impor kelas yang diperlukan sehingga Anda dapat bekerja dengan objek OneNote dan konversi PDF.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## Cara menyimpan OneNote sebagai PDF dengan daftar bernomor?
Berikut adalah panduan langkah demi langkah yang menunjukkan **cara membuat elemen daftar**, **mengatur gaya teks default**, dan akhirnya **mengekspor OneNote ke PDF**.

### Langkah 1: Inisialisasi Objek Document, Page, dan Outline
Kami memulai dengan membuat struktur inti OneNote. Ini juga memperlihatkan penggunaan **add outline element java**.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Tip pro:** Jaga agar path `dataDir` bersifat absolut atau gunakan `System.getProperty("user.dir")` untuk menghindari masalah path.

### Langkah 2: Atur Gaya Teks Default
Gaya yang konsisten memastikan daftar terlihat seragam di semua item.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Langkah 3: Buat Elemen Outline (Daftar Bernomor)
Di sini kami **menyesuaikan format penomoran** menggunakan `NumberList`. Pola `"{0})"` menghasilkan “1)”, “2)”, dll.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Mengapa ini penting:** Dengan melampirkan `NumberList` ke setiap `OutlineElement`, Anda mendapatkan kontrol penuh atas gaya penomoran, font, dan ukuran.

### Langkah 4: Tambahkan Elemen Outline ke Outline
Sekarang kami menggabungkan item daftar individual menjadi satu outline.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Langkah 5: Lampirkan Outline ke Halaman
Outline menjadi bagian dari hierarki halaman OneNote.

```java
page.appendChildLast(outline);
```

### Langkah 6: Simpan Dokumen sebagai PDF
Akhirnya, kami **menyimpan OneNote sebagai PDF**. File output akan berisi daftar bernomor persis seperti yang didefinisikan.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

Menjalankan kode di atas menghasilkan PDF bernama `CreateNumberedList_out.pdf` di direktori yang Anda tentukan, mempertahankan format daftar bernomor.

## Masalah Umum & Solusi
| Masalah | Solusi |
|-------|----------|
| **PDF kosong** | Pastikan `doc.appendChildLast(page);` dipanggil sebelum `doc.save()`. |
| **Penomoran tidak tampil** | Verifikasi pola `NumberList` dan `NumberFormat` telah diatur dengan benar. |
| **Error file tidak ditemukan** | Gunakan path absolut untuk `dataDir` atau buat direktori terlebih dahulu. |
| **Font tidak cocok** | Instal font (misalnya Arial) pada mesin yang menjalankan kode. |

## Pertanyaan yang Sering Diajukan
### Q: Bisakah saya menyesuaikan format penomoran dalam daftar OneNote saya?
A: Tentu saja! Anda dapat menyesuaikan format penomoran menggunakan kelas `NumberList` yang disediakan oleh Aspose.Note for Java.

### Q: Apakah ada versi percobaan tersedia untuk Aspose.Note for Java?
A: Ya, Anda dapat mengunduh versi percobaan gratis [di sini](https://releases.aspose.com/).

### Q: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.Note for Java?
A: Kunjungi [forum Aspose.Note for Java](https://forum.aspose.com/c/note/28) untuk dukungan komunitas.

### Q: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.Note for Java?
A: Lihat [dokumentasi](https://reference.aspose.com/note/java/) untuk informasi lengkap.

### Q: Bagaimana cara membeli lisensi untuk Aspose.Note for Java?
A: Anda dapat membeli lisensi [di sini](https://purchase.aspose.com/buy).

## Kesimpulan
Dalam tutorial ini kami menunjukkan cara **menyimpan OneNote sebagai PDF** sambil membuat daftar bernomor yang bersih menggunakan Aspose.Note for Java. Dengan mengatur gaya teks default, menyesuaikan format penomoran, dan mengikuti panduan langkah demi langkah, Anda dapat menghasilkan PDF profesional dari halaman OneNote dengan cepat dan andal.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose