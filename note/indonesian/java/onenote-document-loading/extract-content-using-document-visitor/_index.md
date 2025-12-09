---
date: 2025-12-04
description: Pelajari cara mengekstrak gambar dari file OneNote dan mengonversi OneNote
  menjadi teks di Java menggunakan Aspose.Note. Panduan langkah demi langkah dengan
  contoh kode.
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Ekstrak Gambar dari OneNote menggunakan Document Visitor - Java
url: /id/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekstrak Gambar dari OneNote menggunakan Document Visitor - Java

## Introduction

Aspose.Note for Java memudahkan **ekstrak gambar dari OneNote** notebook serta membaca file `.one` yang mendasarinya di Java. Dalam tutorial ini kami akan memandu Anda melalui contoh lengkap, langsung yang menunjukkan cara memuat file OneNote, menelusuri strukturnya dengan `DocumentVisitor` khusus, dan mengambil baik gambar maupun teks biasa. Pada akhir Anda juga akan mengetahui cara **mengonversi OneNote ke teks** jika Anda hanya membutuhkan konten teks.

## Quick Answers
- **Perpustakaan apa yang saya butuhkan?** Aspose.Note for Java (tautan unduhan di bawah).  
- **Bisakah saya hanya mengekstrak gambar?** Ya – implementasikan metode `VisitImageStart` dalam `DocumentVisitor`.  
- **Bagaimana cara membaca file .one di Java?** Gunakan `new Document(path, new LoadOptions())`.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan untuk penggunaan non‑trial.  
- **Versi Java apa yang didukung?** JDK 8 atau lebih tinggi.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

1. Java Development Kit (JDK) 8 atau yang lebih baru terpasang.  
2. Perpustakaan Aspose.Note untuk Java yang sudah diunduh. Anda dapat mengunduhnya **[di sini](https://releases.aspose.com/note/java/)**.  
3. Dokumen OneNote (`.one` file) yang ingin Anda ekstrak gambarnya atau konversi ke teks.

## Import Packages

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

## Langkah 1: Siapkan Document Visitor Kustom

Buat kelas yang memperluas `DocumentVisitor`. Kelas ini akan dipanggil untuk setiap node dalam dokumen OneNote, memungkinkan Anda **mengekstrak gambar dari OneNote** dan secara opsional mengumpulkan teks.

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

## Langkah 2: Implementasikan Metode Visitor

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

### Mengapa mengimplementasikan metode-metode ini?

- **Ekstrak gambar dari OneNote:** `VisitImageStart` memberi Anda akses langsung ke byte gambar mentah.  
- **Konversi OneNote ke teks:** `VisitRichTextStart` mengumpulkan konten teks, memungkinkan operasi **koni OneNote ke teks** yang sederhana.  
- **Baca file .one di Java:** Pola visitor mengabstraksi struktur file `.one` yang mendasari, sehingga Anda tidak perlu mengurai format biner secara manual.

## Langkah 3: Jalankan Visitor dari Metode Main Anda

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

- **Pelaporan otomatis:** Ambil gambar dan teks dari notebook rapat OneNote untuk menghasilkan ringkasan PDF atau HTML.  
- **Migrasi konten:** Konversi arsip OneNote lama ke file teks biasa untuk pengindeksan atau ingest mesin pencari.  
- **Ekstraksi aset digital:** Kumpulkan screenshot, diagram, atau foto yang tertanam untuk digunakan kembali dalam aplikasi lain.

## Pemecahan Masalah & Tips

- **Notebook besar:** Jika Anda mengalami masalah memori, proses halaman secara individual dengan memeriksa `VisitPageStart` dan memuat sumber daya tingkat halaman hanya saat diperlukan.  
- **Format gambar:** Objek `Image` mengembalikan byte mentah; Anda mungkin perlu mendeteksi format (PNG, JPEG) sebelum menyimpan.  
- **Kesalahan lisensi:** Pastikan Anda telah mengatur lisensi Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) sebelum memuat dokumen di produksi.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya mengekstrak tipe konten tertentu dari dokumen OneNote?**  
A: Ya – dengan mengoverride hanya metode visitor yang Anda perlukan (misalnya, `VisitImageStart` untuk gambar, `VisitRichTextStart` untuk teks).

**Q: Apakah Aspose.Note untuk Java kompatibel dengan berbagai versi dokumen OneNote?**  
A: Tentu saja. Perpustakaan ini mendukung semua versi utama file OneNote, sehingga Anda dapat dengan aman **membaca file .one di Java** proyek terlepas dari versi OneNote asalnya.

**Q: Bisakah saya mengintegrasikan proses ekstraksi ini ke dalam aplikasi Java saya?**  
A: Ya. Pola visitor bekerja mulus di dalam basis kode Java apa pun; cukup tambahkan JAR perpustakaan dan panggil contoh yang ditunjukkan di atas.

**Q: Apakah Aspose.Note untuk Java menyediakan dukungan untuk menangani dokumen OneNote yang kompleks?**  
A: Ya. Outline bersarang, media tertanam, dan data khusus semuanya dapat diakses melalui API visitor.

**Q: Apakah ada batasan ukuran dokumen OneNote yang dapat diproses?**  
A: Tidak ada batasan keras, tetapi notebook yang sangat besar mungkin memerlukan lebih banyak memori heap; pertimbangkan memprosesnya halaman per halaman.

**Q: Bagaimana cara mengonversi teks yang diekstrak menjadi file teks biasa?**  
A: Setelah `myConverter.GetText()` mengembalikan `String`, tulis ke file menggunakan I/O Java standar (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}