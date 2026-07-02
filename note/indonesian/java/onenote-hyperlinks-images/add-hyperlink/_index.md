---
date: 2025-12-20
description: Pelajari cara menyimpan OneNote sebagai PDF dan menambahkan hyperlink
  di OneNote menggunakan Java dengan pustaka Aspose.Note. Hasilkan PDF dari OneNote
  dengan mudah.
linktitle: Save OneNote as PDF and Add Hyperlink in OneNote with Java
second_title: Aspose.Note Java API
title: Simpan OneNote sebagai PDF dan Tambahkan Hyperlink di OneNote dengan Java
url: /id/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan OneNote sebagai PDF dan Tambahkan Hyperlink di OneNote dengan Java

## Introduction

Menambahkan hyperlink ke dokumen OneNote Anda sekaligus menyimpannya sebagai PDF dapat secara dramatis meningkatkan interaktivitas catatan Anda dan mempermudah berbagi. Pada tutorial ini Anda akan belajar **cara menyimpan OneNote sebagai PDF** dan menyisipkan tautan yang dapat diklik menggunakan Java serta pustaka Aspose.Note. Mari ikuti langkah‑langkahnya bersama!

## Quick Answers
- **Apakah saya dapat menyimpan OneNote sebagai PDF dengan Java?** Ya, Aspose.Note untuk Java menyediakan satu panggilan `save` untuk menghasilkan PDF.
- **Bagaimana cara menyisipkan hyperlink?** Gunakan `TextStyle.setHyperlinkAddress` pada segmen `RichText`.
- **Apa saja prasyaratnya?** JDK 8+ dan pustaka Aspose.Note untuk Java.
- **Format output apa yang didukung?** PDF, DOCX, XPS, dan lainnya.
- **Apakah lisensi diperlukan untuk produksi?** Ya, lisensi komersial diperlukan untuk penggunaan non‑evaluasi.

## What is “save onenote as pdf”?

Menyimpan notebook OneNote sebagai PDF menghasilkan versi portabel, hanya‑baca dari catatan Anda yang dapat dibuka di perangkat apa pun tanpa aplikasi OneNote. Ini sangat berguna untuk pengarsipan, pencetakan, atau berbagi dengan pengguna yang tidak memiliki OneNote.

## Why generate PDF from OneNote with Aspose.Note Java?

- **Full fidelity:** Mempertahankan format, gambar, dan hyperlink.
- **Programmatic control:** Mengotomatisasi konversi batch dalam layanan backend.
- **Cross‑platform:** Berfungsi di Windows, Linux, dan macOS.
- **Rich API:** Mudah menambah atau memodifikasi konten sebelum menyimpan.

## Prerequisites

Sebelum memulai, pastikan Anda telah menginstal dan menyiapkan prasyarat berikut pada sistem Anda:

### Java Development Kit (JDK)

Pastikan Java Development Kit (JDK) terpasang di sistem Anda. Anda dapat mengunduh dan menginstal JDK dari [situs Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Aspose.Note for Java Library

Unduh dan instal pustaka Aspose.Note untuk Java. Dokumentasi serta tautan unduhan dapat Anda temukan [di sini](https://reference.aspose.com/note/java/).

## Import Packages

Untuk memulai, impor paket‑paket yang diperlukan untuk bekerja dengan Aspose.Note untuk Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Sekarang, mari uraikan contoh yang diberikan menjadi beberapa langkah:

## Step 1: Set Up Document Structure

Pertama, buat dokumen baru dan halaman tempat konten akan ditempatkan.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Step 2: Define Default Text Style

Tentukan gaya paragraf default yang akan diterapkan pada kebanyakan elemen teks.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Step 3: Set Title Text

Buat judul untuk halaman dan terapkan gaya default.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Step 4: Create Outline and Outline Elements

Outline berfungsi sebagai wadah untuk paragraf dan elemen lainnya.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Step 5: Define Text Style for Hyperlink

Di sini kita mendefinisikan gaya berwarna merah yang akan digunakan untuk bagian yang dapat diklik.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Step 6: Add Text with Hyperlink

Sekarang kita membangun objek `RichText` yang mencampur teks biasa dan hyperlink.  
Metode `setHyperlinkAddress` memberi tahu Aspose.Note bahwa segmen ini harus dapat diklik.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Step 7: Add Outline to Page and Page to Document

Lampirkan elemen outline ke outline, outline ke halaman, dan akhirnya halaman ke dokumen.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Step 8: Save the Document as PDF

Langkah terakhir adalah menyimpan dokumen OneNote sebagai file PDF. Inilah saat kata kunci utama **save onenote as pdf** berperan.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Conclusion

Selamat! Anda telah berhasil **menyimpan OneNote sebagai PDF** dan menambahkan hyperlink ke dokumen menggunakan Java serta pustaka Aspose.Note. Kemampuan ini memungkinkan Anda membuat PDF interaktif dan dapat dibagikan langsung dari konten OneNote Anda.

## Frequently Asked Questions

**Q: Bagaimana cara menyesuaikan tampilan hyperlink?**  
A: Gunakan properti `TextStyle` seperti `setFontColor`, `setUnderline`, atau `setFontName` sebelum memanggil `setHyperlinkAddress`.

**Q: Bisakah saya menyimpan dokumen dalam format selain PDF?**  
A: Ya, Aspose.Note mendukung DOCX, XPS, HTML, dan beberapa format ekspor lainnya.

**Q: Bagaimana jika saya perlu menambahkan hyperlink ke file OneNote yang sudah ada?**  
A: Muat file yang ada dengan `new Document("input.one")`, modifikasi kontennya seperti yang ditunjukkan, lalu panggil `save` dengan format yang diinginkan.

**Q: Apakah ada cara membuka hyperlink secara programatis setelah PDF dihasilkan?**  
A: Penampil PDF akan menangani tautan yang dapat diklik secara otomatis; tidak diperlukan kode tambahan.

**Q: Apakah saya memerlukan lisensi untuk penggunaan pengembangan?**  
A: Lisensi evaluasi sementara cukup untuk pengembangan dan pengujian, tetapi lisensi penuh diperlukan untuk penyebaran produksi.

---

**Last Updated:** 2025-12-20  
**Tested With:** Aspose.Note for Java 26.4  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}