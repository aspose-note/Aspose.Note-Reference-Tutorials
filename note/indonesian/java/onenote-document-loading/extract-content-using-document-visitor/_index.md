---
date: 2026-02-10
description: Pelajari cara mengonversi OneNote menjadi teks dan mengekstrak gambar
  dengan Aspose.Note untuk Java. Panduan ini menunjukkan cara membaca file .one dengan
  Java dan melakukan ekstraksi teks OneNote.
linktitle: Convert OneNote to Text and Extract Images using Document Visitor - Java
second_title: Aspose.Note Java API
title: Konversi OneNote ke Teks dan Ekstrak Gambar menggunakan Document Visitor -
  Java
url: /id/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi OneNote ke Teks dan Mengekstrak Gambar menggunakan Document Visitor - Java

## Perkenalan

Aspose.Note for Java memudahkan **mengonversi OneNote ke teks** sekaligus **mengekstrak gambar dari OneNote** notebook. Dalam tutorial ini kami akan memandu Anda melalui contoh lengkap, hands‑on yang menunjukkan cara memuat file OneNote, menelusuri strukturnya dengan `DocumentVisitor` khusus, dan mengambil gambar serta teks biasa. Pada akhir Anda juga akan mengetahui cara **membaca file .one java** proyek dan mengapa pendekatan ini ideal untuk migrasi konten otomatis atau pelaporan.

## Jawaban Cepat
- **Perpustakaan apa yang saya butuhkan?** Aspose.Note untuk Java (link download di bawah).
- **Apakah saya dapat mengekstrak gambar saja?** Ya – terapkan metode `VisitImageStart` dalam `DocumentVisitor`.
- **Bagaimana cara membaca file .one di Java?** Gunakan `Dokumen baru(jalur, LoadOptions())` baru.
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan untuk penggunaan non-uji coba.
- **Versi Java apa yang didukung?** JDK8atau lebih tinggi.

## Apa itu mengubah OneNote menjadi teks?

Mengonversi OneNote ke teks berarti mengekstrak konten teks mentah dari notebook `.one` dan menyimpannya sebagai teks Unicode biasa. Ini berguna ketika Anda membutuhkan arsip yang dapat dicari, umpan data ringan, atau ringkasan sederhana tanpa format OneNote asli.

## Mengapa menggunakan Document Visitor Aspose.Note untuk ekstraksi teks OneNote?

- **Kontrol detail:** Pola pengunjung memungkinkan Anda memutuskan node mana (halaman, garis besar, gambar, teks kaya) yang ingin diproses.
- **Kinerja:** Anda menghindari memuat seluruh dokumen ke memori sebagai satu gumpalan; setiap node dikunjungi sesuai permintaan.
- **Fleksibilitas:** Pengunjung yang sama mampu mengekstrak gambar, tabel, atau metadata khusus, menjadikannya solusi satu‑pintu untuk **mengonversi OneNote ke teks** dan **cara mengekstrak gambar**.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

1. Java Development Kit (JDK)8atau yang lebih baru terpasang.
2. Aspose.Note untuk perpustakaan Java diunduh. Anda dapat mengunduhnya **[di sini](https://releases.aspose.com/note/java/)**.
3. Dokumen OneNote (`.one` file) yang ingin Anda ekstrak gambar atau konversi ke teks.

## Impor Paket

Pertama, impor kelas yang diperlukan dari API Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Langkah 1: Menyiapkan Pengunjung Dokumen Kustom

Buat kelas yang memperluas `DocumentVisitor`. Kelas ini akan dipanggil untuk setiap node dalam dokumen OneNote, memungkinkan Anda **mengekstrak gambar OneNote** dan secara opsional mengumpulkan teks.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Langkah 2: Menerapkan Metode Pengunjung

Tambahkan override untuk tipe node yang Anda butuhkan. Di bawah ini kami menangani rich‑text, gambar, judul, halaman, outline, dan elemen outline. Metode `VisitImageStart` adalah tempat ekstraksi gambar terjadi.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Mengapa menerapkan metode ini?

- **Mengekstrak gambar dari OneNote:** `VisitImageStart` memberi Anda akses langsung ke byte gambar mentah.
- **Mengonversi OneNote ke teks:** `VisitRichTextStart` mengumpulkan konten teks, memungkinkan operasi **mengonversi OneNote ke teks** sederhana.
- **Membaca file .one Java:** Pola pengunjung mengabstraksi struktur file `.one` yang mendasarinya, sehingga Anda tidak perlu mengurai format biner secara manual.

## Langkah 3: Jalankan Pengunjung dari Metode Utama Anda

Muat file `.one`, buat instance visitor Anda, dan mulai penelusuran.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Kasus Penggunaan Umum

- **Pelaporan otomatis:** Tarik gambar dan teks dari notebook rapat OneNote untuk menghasilkan ringkasan PDF atau HTML.
- **Migrasi konten:** Mengonversi arsip OneNote lama ke file teks biasa untuk pengindeksan atau penyerapan mesin pencari.
- **Ekstraksi aset digital:** Mengumpulkan tangkapan layar, diagram, atau foto yang disematkan untuk digunakan kembali dalam aplikasi lain.

## Pemecahan Masalah & Tip

- **Notebook besar:** Jika Anda mengalami masalah memori, proses halaman secara individual dengan memeriksa `VisitPageStart` dan memuat sumber daya tingkat halaman hanya saat diperlukan.
- **Format gambar:** Objek `Image` mengembalikan byte mentah; Anda mungkin perlu mendeteksi format (PNG, JPEG) sebelum menyimpan.
- **Kesalahan lisensi:** Pastikan Anda telah mengatur lisensi Aspose (`License License = new License(); License.setLicense("Aspose.Note.Java.lic");`) sebelum memuat dokumen di produksi.
- **Cara mengekstrak gambar secara efisien:** Filter node di dalam `VisitImageStart` berdasarkan ukuran atau format jika Anda hanya membutuhkan tipe gambar tertentu.

## Pertanyaan yang Sering Diajukan

**Q: Apakah saya dapat mengekstrak tipe konten tertentu dari dokumen OneNote?**
A: Ya – dengan mengoverride hanya metode pengunjung yang Anda perlukan (misalnya `VisitImageStart` untuk gambar, `VisitRichTextStart` untuk teks).

**Q: Apakah Aspose.Note untuk Java kompatibel dengan berbagai versi dokumen OneNote?**
J: Tentu saja. Perpustakaan ini mendukung semua versi file OneNote utama, sehingga Anda dapat dengan aman **membaca file .one java** proyek terlepas dari versi OneNote asal.

**Q: Apakah saya dapat mengintegrasikan proses ekstraksi ini ke dalam aplikasi Java saya?**
J: Ya. Pola pengunjung bekerja mulus berdasarkan kode Java apa pun; cukup tambahkan perpustakaan JAR dan panggil contoh yang ditampilkan di atas.

**Q: Apakah Aspose.Note untuk Java menyediakan dukungan untuk menangani dokumen OneNote yang kompleks?**
J: Ya. Garis besar penempatan, media yang disematkan, dan data khusus semuanya dapat diakses melalui pengunjung API.

**Q: Apakah ada batasan ukuran dokumen OneNote yang dapat diproses?**
A: Tidak ada batasan keras, tetapi notebook yang sangat besar mungkin memerlukan lebih banyak memori heap; memproses memprosesnya halaman per halaman.

**Q: Bagaimana cara mengubah teks yang diekstrak menjadi file teks biasa?**
A: Setelah `myConverter.GetText()` mengembalikan `String`, tulis ke file menggunakan I/O Java standar (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---
**Terakhir Diperbarui:** 2026-02-10  
**Diuji Dengan:** Aspose.Note for Java 24.10  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}