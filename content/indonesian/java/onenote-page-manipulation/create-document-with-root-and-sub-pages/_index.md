---
title: Buat Dokumen dengan Root dan Sub Halaman di OneNote
linktitle: Buat Dokumen dengan Root dan Sub Halaman di OneNote
second_title: Aspose.Catatan Java API
description: Buat dokumen dengan akar dan sub halaman di OneNote menggunakan Aspose.Note untuk Java. Ikuti panduan langkah demi langkah untuk mengatur catatan Anda secara efisien.
type: docs
weight: 11
url: /id/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## Perkenalan

Dalam tutorial ini, kami akan memandu Anda melalui proses pembuatan dokumen dengan akar dan sub halaman di OneNote menggunakan Aspose.Note untuk Java. Dengan mengikuti langkah-langkah ini, Anda akan dapat mengatur dokumen OneNote Anda secara efisien dengan struktur hierarki.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda.
2. Aspose.Note for Java: Unduh dan instal Aspose.Note for Java dari[situs web](https://purchase.aspose.com/buy).
3. Lingkungan Pengembangan Terintegrasi (IDE): Pilih IDE Java seperti IntelliJ IDEA, Eclipse, atau NetBeans.

## Paket Impor

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

 Buat contoh a`Document` obyek:

```java
Document doc = new Document();
```

## Langkah 3: Buat Halaman

Inisialisasi objek halaman dan atur levelnya:

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

Simpan dokumen OneNote:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Tangani pengecualian
}
```

Selamat! Anda telah berhasil membuat dokumen dengan akar dan sub halaman di OneNote menggunakan Aspose.Note untuk Java.

## Kesimpulan

Mengatur dokumen OneNote Anda dengan struktur hierarki sangat penting untuk manajemen dan navigasi yang lebih baik. Dengan Aspose.Note untuk Java, Anda dapat membuat dokumen dengan akar dan sub halaman secara efisien, memberikan tata letak yang jelas dan terorganisir untuk catatan Anda.

## FAQ

### Q1: Dapatkah saya membuat beberapa tingkat subhalaman menggunakan Aspose.Note untuk Java?

A1: Ya, Anda dapat membuat beberapa tingkat subhalaman dengan mengatur tingkat yang sesuai untuk setiap halaman.

### Q2: Apakah Aspose.Note untuk Java kompatibel dengan IDE Java yang berbeda?

A2: Ya, Aspose.Note untuk Java kompatibel dengan IDE Java populer seperti IntelliJ IDEA, Eclipse, dan NetBeans.

### Q3: Bisakah saya mengkustomisasi pemformatan teks di dokumen OneNote saya?

A3: Ya, Anda dapat menyesuaikan font, warna, ukuran, dan opsi pemformatan lainnya menggunakan Aspose.Note untuk fitur teks kaya Java.

### Q4: Apakah Aspose.Note untuk Java mendukung penyimpanan dokumen dalam format berbeda?

A4: Ya, Aspose.Note untuk Java mendukung penyimpanan dokumen dalam berbagai format termasuk BMP, PDF, PNG, dan lainnya.

### Q5: Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?

A5: Ya, Anda dapat mengunduh Aspose.Note untuk Java versi uji coba gratis dari situs web.