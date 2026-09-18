---
date: 2026-01-28
description: Pelajari cara membuat outline di OneNote, menambahkan tag ke OneNote,
  dan menghasilkan PDF dari OneNote menggunakan Aspose.Note untuk Java.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: Buat Outline di OneNote dan Tambahkan Tag – Aspose.Note
url: /id/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat Outline di OneNote dan Tambahkan Tag – Aspose.Note

## Pendahuluan
Apakah Anda ingin **membuat outline di OneNote** dan meningkatkan kolaborasi dengan tag menggunakan Java? Aspose.Note untuk Java memudahkan penambahan tag, penataan catatan Anda, dan bahkan **menghasilkan PDF dari file OneNote**. Dalam tutorial ini kami akan membahas setiap langkah, menjelaskan *mengapa* setiap bagian penting, dan menunjukkan cara menghasilkan PDF yang rapi di akhir.

## Jawaban Cepat
- **Apa arti “create outline in OneNote”?** Itu membangun struktur hierarkis (outline) yang mengatur konten seperti judul dan sub‑bagian.  
- **Library mana yang menambahkan tag ke OneNote?** Aspose.Note untuk Java menyediakan kelas `NoteTag` untuk penanda visual.  
- **Bisakah saya mengekspor hasilnya ke PDF?** Ya – gunakan `SaveFormat.Pdf` untuk **menghasilkan PDF dari OneNote**.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi sementara tersedia untuk pengujian; lisensi penuh diperlukan untuk penggunaan komersial.  
- **Apa prasyarat utama?** JDK terpasang, pustaka Aspose.Note untuk Java, dan pengetahuan dasar Java.

## Apa itu “create outline in OneNote”?
Membuat outline di OneNote berarti menambahkan objek `Outline` dan `OutlineElement` yang mendefinisikan struktur berbentuk pohon untuk catatan Anda. Hierarki ini memungkinkan Anda menyembunyikan, memperluas, dan mengatur informasi seperti judul dalam sebuah dokumen.

## Mengapa menambahkan tag ke OneNote?
Tag seperti bintang, centang, atau ikon khusus memberikan petunjuk visual kepada pembaca, meningkatkan kemampuan pencarian, dan membantu tim memprioritaskan item. Dengan Aspose.Note Anda dapat secara programatik menempelkan `NoteTag` pada teks apa pun.

## Prasyarat
Sebelum memulai, pastikan Anda memiliki:
- Java Development Kit (JDK) terpasang.
- Pustaka Aspose.Note untuk Java telah diunduh. Anda dapat mendapatkannya [di sini](https://releases.aspose.com/note/java/).
- Pemahaman dasar tentang pemrograman Java.

## Impor Paket
Pastikan Anda mengimpor paket yang diperlukan untuk memulai proyek Anda:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```

## Langkah 1: Siapkan Dokumen dan Halaman
Mulailah dengan membuat objek `Document` baru dan menginisialisasi objek `Page`:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Langkah 2: Buat Outline
Selanjutnya, buat objek `Outline` untuk menata konten Anda:
```java
Outline outline = new Outline();
```
Outline menyediakan struktur hierarkis pada dokumen Anda, memudahkan **membuat outline di OneNote** dan menjaga informasi tetap teratur.

## Langkah 3: Inisialisasi OutlineElement dan ParagraphStyle
Sekarang, inisialisasi `OutlineElement` dan atur `ParagraphStyle` untuk pemformatan teks:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```

## Langkah 4: Tambahkan RichText dengan NoteTag
Buat objek `RichText`, tambahkan teks OneNote Anda, dan tambahkan `NoteTag`:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
`RichText` memungkinkan Anda memasukkan teks yang diformat, dan `NoteTag` **menambahkan tag ke OneNote** sebagai petunjuk visual.

## Langkah 5: Bangun Struktur Outline
Tambahkan node teks, node elemen outline, dan node outline untuk membangun struktur dokumen:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
Langkah ini memastikan konten Anda terorganisir dalam dokumen, menyelesaikan proses **membuat outline di OneNote**.

## Langkah 6: Simpan Dokumen
Simpan dokumen dalam format PDF, yang **menghasilkan PDF dari OneNote**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
Sekarang, dokumen OneNote Anda dengan tag yang ditambahkan disimpan sebagai PDF.

Dengan mengikuti langkah-langkah ini, Anda dapat dengan mudah meningkatkan dokumen OneNote Anda menggunakan Aspose.Note untuk Java.

## Kesimpulan
Dalam tutorial ini kami menjelajahi cara **membuat outline di OneNote**, menambahkan tag ke OneNote, dan kemudian **menghasilkan PDF dari OneNote** menggunakan Aspose.Note untuk Java. Memanfaatkan Java memberi Anda kontrol penuh atas struktur catatan, penandaan visual, dan opsi ekspor, menjadikan catatan Anda lebih teratur dan dapat dibagikan.

## FAQ
### 1. Bisakah saya menggunakan Aspose.Note untuk Java dengan bahasa pemrograman lain?
Aspose.Note terutama mendukung Java, namun ada juga versi yang tersedia untuk .NET.

### 2. Apakah Aspose.Note untuk Java cocok untuk pemula?
Ya, Aspose.Note untuk Java menyediakan dokumentasi dan dukungan yang komprehensif, sehingga dapat diakses oleh pemula maupun pengembang berpengalaman.

### 3. Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Note untuk Java?
Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

### 4. Di mana saya dapat menemukan dukungan tambahan?
Untuk pertanyaan atau bantuan, kunjungi [forum Aspose.Note](https://forum.aspose.com/c/note/28).

### 5. Apakah tersedia percobaan gratis?
Ya, Anda dapat mencoba percobaan gratis [di sini](https://releases.aspose.com/).

**Additional Q&A**

**Q: Bisakah saya menyesuaikan ikon tag?**  
A: Ya – Aspose.Note menyediakan banyak ikon bawaan melalui `TagIcon` dan juga memungkinkan gambar khusus.

**Q: Bagaimana cara mengubah pengaturan output PDF?**  
A: Gunakan `PdfSaveOptions` untuk mengontrol kualitas gambar, kompresi, dan keamanan sebelum memanggil `doc.save`.

**Q: Apakah memungkinkan menambahkan beberapa tag pada teks yang sama?**  
A: Tentu saja. Panggil `text.getTags().add()` beberapa kali dengan instance `NoteTag` yang berbeda.

---

**Last Updated:** 2026-01-28  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}