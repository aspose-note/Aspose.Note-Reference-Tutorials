---
description: Pelajari cara menyimpan PDF OneNote dan menambahkan subhalaman di OneNote
  menggunakan Aspose.Note untuk Java. Ikuti panduan langkah demi langkah ini untuk
  mengatur catatan Anda secara efisien.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Cara Menyimpan PDF OneNote dan Menambahkan Subhalaman
url: /id/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menyimpan OneNote PDF dan Menambahkan Sub Halaman

## Pendahuluan

Dalam tutorial ini, Anda akan menemukan **cara menyimpan OneNote PDF** sambil membuat dokumen yang berisi halaman root dan sub halaman menggunakan Aspose.Note for Java. Mengatur notebook OneNote Anda dengan hierarki yang jelas memudahkan navigasi, dan kemampuan mengekspor ke PDF memastikan Anda dapat membagikan catatan dalam format yang dapat dibaca secara universal. Kami juga akan menunjukkan cara **menambahkan sub halaman onenote** gaya, sehingga Anda dapat membangun struktur multi‑level dengan mudah.

## Jawaban Cepat
- **Apa arti kata kunci utama?** Itu merujuk pada mengekspor notebook OneNote ke PDF menggunakan Aspose.Note.  
- **API mana yang digunakan?** Aspose.Note for Java.  
- **Bisakah saya membuat halaman hierarkis?** Ya – atur level halaman untuk membuat halaman root dan sub.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis tersedia; lisensi komersial diperlukan untuk produksi.  
- **Format output apa yang didukung?** BMP, PDF, PNG, dan lainnya.

## Apa itu “cara menyimpan OneNote PDF”?

Menyimpan OneNote sebagai PDF mengonversi halaman notebook menjadi dokumen berlayout tetap yang mempertahankan format, gambar, dan hierarki. Ini ideal untuk berbagi, mengarsipkan, atau mencetak catatan.

## Mengapa menambahkan sub halaman onenote?

Menambahkan sub halaman memungkinkan Anda mengelompokkan konten terkait di bawah halaman induk, meniru struktur seperti folder. Ini meningkatkan organisasi catatan, mempercepat pencarian, dan memperbaiki pengalaman membaca ketika notebook diekspor ke PDF.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda.  
2. Aspose.Note for Java: Unduh dan instal Aspose.Note for Java dari [website](https://purchase.aspose.com/buy).  
3. Integrated Development Environment (IDE): Pilih IDE Java seperti IntelliJ IDEA, Eclipse, atau NetBeans.

## Impor Paket

Mulailah dengan mengimpor paket yang diperlukan dalam proyek Java Anda:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Langkah 1: Siapkan Direktori Dokumen

Tentukan direktori tempat Anda ingin menyimpan dokumen OneNote Anda:

```java
String dataDir = "Your Document Directory";
```

## Langkah 2: Buat Objek Dokumen

Instansiasi objek `Document`:

```java
Document doc = new Document();
```

## Langkah 3: Buat Halaman

Inisialisasi objek halaman dan atur levelnya. Menetapkan level menentukan apakah sebuah halaman merupakan halaman root atau sub halaman:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Langkah 4: Tambahkan Node ke Halaman

### Menambahkan Node ke Halaman Pertama

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Menambahkan Node ke Halaman Kedua

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Menambahkan Node ke Halaman Ketiga

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Langkah 5: Tambahkan Halaman ke Dokumen

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Langkah 6: Simpan Dokumen

Simpan dokumen OneNote sebagai PDF (atau BMP dalam contoh ini). Mengubah `SaveFormat` memungkinkan Anda mengekspor ke PDF, yang memenuhi persyaratan “cara menyimpan OneNote PDF”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Tip Pro:** Untuk mengekspor langsung ke PDF, ganti `SaveFormat.Bmp` dengan `SaveFormat.Pdf`.

Selamat! Anda telah berhasil membuat dokumen OneNote dengan halaman root dan sub serta mempelajari **cara menyimpan OneNote PDF** menggunakan Aspose.Note for Java.

## Mengapa Ini Penting

- **Organisasi hierarkis:** Halaman root dan sub memungkinkan Anda meniru struktur folder di dalam OneNote.  
- **Ekspor PDF tanpa hambatan:** Setelah diatur, mengekspor ke PDF mempertahankan hierarki, membuat dokumen akhir mudah dibaca dan dibagikan.  
- **Otomatisasi:** Kode dapat diintegrasikan ke dalam aplikasi Java yang lebih besar, memungkinkan pembuatan batch notebook terstruktur.

## Kesalahan Umum & Cara Menghindarinya

| Masalah | Penyebab | Solusi |
|-------|-------|----------|
| Halaman muncul pada level yang sama | Nilai `setLevel` tidak tepat | Gunakan `setLevel((byte) 1)` untuk halaman root dan `setLevel((byte) 2)` (atau lebih tinggi) untuk sub halaman. |
| Output PDF terlihat kosong | Tidak ada `SaveFormat.Pdf` atau jalur file salah | Pastikan direktori ada dan gunakan `SaveFormat.Pdf`. |
| Font tidak diterapkan | Nama font salah atau font tidak ada di sistem | Pastikan font (misalnya “David Transparent”) terinstal pada mesin yang menjalankan kode. |

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya membuat beberapa level sub‑halaman menggunakan Aspose.Note for Java?**  
A: Ya, Anda dapat membuat hierarki yang lebih dalam dengan menetapkan nomor level yang lebih tinggi (misalnya, `setLevel((byte) 3)` untuk sub‑halaman tingkat tiga).

**Q: Apakah Aspose.Note for Java kompatibel dengan berbagai IDE Java?**  
A: Tentu saja. Ia bekerja dengan IntelliJ IDEA, Eclipse, NetBeans, dan IDE apa pun yang mendukung pengembangan Java.

**Q: Bisakah saya menyesuaikan format teks dalam dokumen OneNote saya?**  
A: Ya. Gunakan `ParagraphStyle` untuk mengatur nama font, ukuran, warna, dan atribut lainnya untuk setiap elemen `RichText`.

**Q: Apakah Aspose.Note for Java mendukung penyimpanan dokumen dalam format selain BMP?**  
A: Ya. Format yang didukung meliputi PDF, PNG, JPEG, DOCX, dan lainnya. Ubah enum `SaveFormat` sesuai kebutuhan.

**Q: Apakah ada versi percobaan yang tersedia untuk Aspose.Note for Java?**  
A: Ya, Anda dapat mengunduh percobaan gratis dari situs web Aspose.

## Kesimpulan

Mengatur notebook OneNote Anda dengan struktur hierarkis yang jelas dan mengekspornya sebagai PDF membuat catatan lebih mudah diakses dan dibagikan. Dengan mengikuti langkah‑langkah di atas, Anda kini tahu **cara menyimpan OneNote PDF** dan **menambahkan sub halaman onenote** secara programatis dengan Aspose.Note for Java.

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}