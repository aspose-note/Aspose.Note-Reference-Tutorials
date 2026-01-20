---
date: 2026-01-20
description: Pelajari cara mengatur gaya paragraf default di OneNote menggunakan Aspise.Note
  untuk Java, dan tambahkan font default OneNote dengan font paragraf yang disesuaikan.
linktitle: Set Default Paragraph Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Atur Gaya Paragraf Default di OneNote - Aspose.Note
url: /id/java/onenote-styles/set-default-paragraph-style/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Gaya Paragraf Default di OneNote - Aspose.Note

## Pendahuluan

Dalam tutorial ini Anda akan belajar **cara mengatur gaya paragraf default** di OneNote secara programatis dengan Aspose.Note untuk Java. Menerapkan gaya default memungkinkan Anda menambahkan font default pada halaman OneNote dan menyesuaikan font paragraf di seluruh dokumen, menghemat Anda dari mengulang kode pemformatan untuk setiap paragraf.

## Jawaban Cepat
- **Apa yang dilakukan “set default paragraph style”?** Itu mendefinisikan templat pemformatan tingkat paragraf yang diwarisi oleh setiap paragraf baru kecuali Anda menimpanya.  
- **Perpustakaan apa yang diperlukan?** Aspose.Note untuk Java.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi komersial diperlukan untuk produksi.  
- **Apa langkah utama?** Inisialisasi dokumen, definisikan `ParagraphStyle`, terapkan pada `RichText`, dan simpan file OneNote.  
- **Bisakah saya mengubah font nanti?** Ya – Anda dapat memodifikasi gaya atau menerapkan `TextStyle` yang berbeda pada tiap run.

## Apa itu “set default paragraph style”?
Mengatur gaya paragraf default berarti membuat objek `ParagraphStyle` (nama font, ukuran, warna, dll.) dan menugaskannya ke elemen `RichText`. Setelah terpasang, setiap baris di dalam `RichText` tersebut secara otomatis menggunakan pemformatan yang telah didefinisikan kecuali `TextStyle` tertentu menimpanya.

## Mengapa menyesuaikan font paragraf di OneNote?
- **Konsistensi:** Menjamin tampilan seragam di semua bagian buku catatan.  
- **Produktivitas:** Menghilangkan kebutuhan untuk memformat setiap paragraf secara manual.  
- **Branding:** Memudahkan penerapan pedoman gaya perusahaan.  

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal berikut:

1. Java Development Kit (JDK) terpasang di sistem Anda.  
2. Aspose.Note untuk Java Library – unduh dari [halaman unduhan](https://releases.aspose.com/note/java/).  
3. IDE seperti Eclipse atau IntelliJ IDEA untuk menulis dan menjalankan kode Java.

## Impor Paket

Pertama, impor paket yang diperlukan untuk memulai penulisan kode:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

Sekarang, mari kita uraikan contoh kode menjadi beberapa langkah:

## Langkah 1: Inisialisasi Dokumen, Halaman, dan Outline

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## Langkah 2: Buat Elemen Outline

```java
OutlineElement outlineElem = new OutlineElement();
```

## Langkah 3: Definisikan Gaya Paragraf Default

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## Langkah 4: Buat Rich Text dengan Gaya Default

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## Langkah 5: Tambahkan Rich Text ke Elemen Outline

```java
outlineElem.appendChildLast(text);
```

## Langkah 6: Tambahkan Elemen Outline ke Outline

```java
outline.appendChildLast(outlineElem);
```

## Langkah 7: Tambahkan Outline ke Halaman

```java
page.appendChildLast(outline);
```

## Langkah 8: Tambahkan Halaman ke Dokumen

```java
document.appendChildLast(page);
```

## Langkah 9: Simpan Dokumen

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

Kode ini akan mengatur gaya paragraf default di OneNote menggunakan Aspose.Note untuk Java.

## Masalah Umum dan Solusinya
- **Font tidak ada di mesin target:** Font harus terpasang di sistem tempat file OneNote dibuka; jika tidak, OneNote akan kembali ke font default.  
- **Kesalahan jalur:** Pastikan `dataDir` mengarah ke folder yang ada dan dapat ditulisi; jika tidak, `document.save` akan melempar `IOException`.  
- **Lisensi tidak diatur:** Jika Anda menjalankan ini tanpa lisensi yang valid, file yang dihasilkan akan berisi watermark.

## Kesimpulan

Mengatur gaya paragraf default di OneNote secara programatis dapat dicapai secara efisien dengan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah yang dijelaskan dalam tutorial ini, Anda dapat mengintegrasikan fungsi ini ke dalam aplikasi Java Anda secara mulus, menambahkan font default pada halaman OneNote, dan menyesuaikan font paragraf agar sesuai dengan merek atau standar dokumentasi Anda.

## Pertanyaan yang Sering Diajukan

**Q1: Bisakah saya menyesuaikan gaya paragraf default lebih lanjut?**  
A1: Ya, Anda dapat menyesuaikan parameter seperti nama font, ukuran, warna, perataan, dan jarak baris sesuai kebutuhan Anda.

**Q2: Apakah Aspose.Note mendukung operasi pemformatan teks lainnya?**  
A2: Tentu saja. Aspose.Note menyediakan dukungan luas untuk memanipulasi pemformatan teks, termasuk gaya font, poin bullet, indentasi, dan lainnya.

**Q3: Apakah Aspose.Note kompatibel dengan semua versi OneNote?**  
A3: Aspose.Note dirancang untuk bekerja dengan file Microsoft OneNote di berbagai versi, memastikan kompatibilitas yang luas.

**Q4: Bisakah saya mengintegrasikan Aspose.Note ke dalam proyek Java saya yang sudah ada?**  
A4: Ya, Anda dapat dengan mudah menambahkan Aspose.Note ke proyek Anda dengan menyertakan file JAR atau dependensi Maven/Gradle dan mengimpor paket yang diperlukan.

**Q5: Apakah ada versi percobaan untuk Aspose.Note?**  
A5: Ya, Anda dapat mengakses percobaan gratis Aspose.Note dari [situs web](https://releases.aspose.com/).

**Q6: Bagaimana cara mengubah gaya default setelah dokumen dibuat?**  
A6: Dapatkan `ParagraphStyle` dari objek `RichText` yang ada, ubah propertinya, dan tetapkan kembali, atau buat gaya baru dan terapkan pada paragraf tambahan.

**Q7: Apakah gaya default akan memengaruhi paragraf yang sudah ada dalam dokumen yang dimuat?**  
A7: Tidak. Gaya default hanya berlaku untuk paragraf baru yang Anda tambahkan setelah mengaturnya. Paragraf yang sudah ada mempertahankan pemformatan aslinya kecuali Anda secara eksplisit memodifikasinya.

---

**Terakhir Diperbarui:** 2026-01-20  
**Diuji Dengan:** Aspose.Note 24.11 for Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}