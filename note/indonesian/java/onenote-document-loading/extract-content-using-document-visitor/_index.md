---
date: 2025-12-03
description: Pelajari cara mengonversi OneNote menjadi teks menggunakan Aspose.Note
  untuk Java. Panduan langkah demi langkah yang mencakup ekstraksi teks, ekstraksi
  gambar, dan cara membaca file OneNote.
language: id
linktitle: Convert OneNote to Text with Document Visitor – Java
second_title: Aspose.Note Java API
title: Konversi OneNote ke Teks dengan Document Visitor – Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi OneNote ke Teks dengan Document Visitor – Java

## Pendahuluan

Dalam tutorial ini Anda akan belajar **cara mengonversi OneNote ke teks** menggunakan Document Visitor dari Aspose.Note untuk Java. Baik Anda perlu membaca file OneNote secara programatik, mengekstrak konten teks biasa, atau mengambil gambar yang disematkan, Document Visitor memberi Anda kontrol detail atas setiap node dalam dokumen .one.

## Jawaban Cepat
- **Apa arti “convert OneNote to text”?** Itu berarti mengekstrak representasi teks biasa (dan secara opsional gambar) dari file .one.  
- **Perpustakaan mana yang membantu dengan ini?** Aspose.Note untuk Java menyediakan API `DocumentVisitor`.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi berbayar diperlukan untuk produksi.  
- **Bisakah saya juga mengekstrak gambar?** Ya – implementasikan metode `VisitImageStart` untuk mengambil gambar.  
- **Apa prasyaratnya?** Java JDK 8+, JAR Aspose.Note untuk Java, dan file .one untuk diproses.

## Apa itu “convert OneNote to text”?
Mengonversi OneNote ke teks berarti secara programatik membaca file OneNote (.one) dan mengambil konten teksnya, judul, serta elemen lainnya tanpa UI OneNote asli. Hal ini berguna untuk pengindeksan pencarian, pelaporan, atau migrasi konten ke platform lain.

## Mengapa menggunakan Document Visitor untuk **cara membaca file OneNote**?
Document Visitor mengikuti pola desain Visitor, memungkinkan Anda menelusuri setiap elemen (halaman, outline, gambar, run teks kaya, dll.) dalam dokumen OneNote. Dibandingkan dengan memuat seluruh dokumen ke memori dan menguraikannya secara manual, pendekatan visitor adalah:

* **Efisien memori** – memproses node satu per satu.  
* **Dapat diperluas** – Anda dapat menambahkan logika khusus untuk tipe node apa pun (mis., mengekstrak gambar).  
* **Akurat** – mempertahankan hierarki asli, memastikan Anda tidak melewatkan konten tersembunyi.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK) 8 atau lebih baru** terpasang.  
2. **Aspose.Note untuk Java** library diunduh dari situs resmi – [download here](https://releases.aspose.com/note/java/).  
3. Sebuah **dokumen OneNote** (`.one` file) yang ingin Anda konversi ke teks.  

## Langkah 1: Impor Paket

Pertama, impor kelas yang Anda perlukan untuk bekerja dengan Aspose.Note untuk Java.

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

## Langkah 2: Siapkan Kelas Document Visitor

Buat kelas yang memperluas `DocumentVisitor`. Visitor khusus ini akan mengump teks, menghitung node, dan (jika Anda mau) menyimpan gambar.

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

## Langkah 3: Implementasikan Metode Visitor  

Di sini kami mengimplementasikan callback untuk tipe node yang kami pedulikan. Metode-metode tersebut meningkatkan penghitung node dan, untuk `RichText`, menambahkan teks sebenarnya ke `StringBuilder` kami. Anda juga dapat menambahkan logika untuk **mengekstrak gambar dari OneNote** dengan menangani `VisitImageStart`.

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
    // Pro tip: you can save the image stream here if you need to extract images.
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

## Langkah 4: Metode Main – Jalankan Visitor

Metode `main` memuat file OneNote, membuat instance visitor khusus kami, dan memulai penelusuran. Setelah penelusuran, kami mencetak teks yang diekstrak dan total jumlah node.

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
    System.out.println(myConverter.GetText());
    System.out.println(myConverter.NodeCount());
}
```

## Kasus Penggunaan Umum – **mengekstrak gambar dari OneNote**

* **Pengindeksan pencarian** – Mengonversi notebook OneNote menjadi teks biasa untuk mesin pencarian full‑text.  
* **Migrasi konten** – Memindahkan catatan ke CMS atau portal dokumentasi.  
* **Analitik data** – Mengambil teks dan gambar untuk pemrosesan bahasa alami atau analisis gambar.  

## Masalah Umum dan Solusinya

| Issue | Solution |
|-------|----------|
| **NullPointerException saat membaca file .one** | Pastikan jalur file (`dataDir`) diakhiri dengan pemisah jalur (`/` atau `\\`) dan file tersebut ada. |
| **Gambar tidak diekstrak** | Implementasikan logika di dalam `VisitImageStart` untuk menulis `image.getImageData()` ke file atau stream. |
| **Notebook besar menyebabkan penggunaan memori tinggi** | Proses dokumen halaman per halaman atau gunakan API streaming jika tersedia. |

## Pertanyaan yang Sering Diajukan

**Q:** Bisakah saya mengekstrak tipe konten tertentu dari dokumen OneNote?  
**A:** Ya, dengan mengimplementasikan hanya metode visitor yang Anda butuhkan (mis., `VisitRichTextStart` untuk teks, `VisitImageStart` untuk gambar).

**Q:** Apakah Aspose.Note untuk Java kompatibel dengan berbagai versi file OneNote?  
**A:** Tentu saja. Perpustakaan ini mendukung file .one yang dibuat oleh versi terbaru Microsoft OneNote.

**Q:** Bisakah saya mengintegrasikan proses ekstraksi ini ke dalam aplikasi Java saya?  
**A:** Ya. Kode yang ditampilkan adalah contoh mandiri yang dapat Anda sematkan langsung ke proyek Java mana pun.

**Q:** Apakah Aspose.Note untuk Java menangani struktur OneNote yang kompleks?  
**A:** Ya. Pola Visitor memungkinkan Anda menavigasi outline bersarang, grup, dan objek tersemat tanpa kehilangan hierarki.

**Q:** Apakah ada batasan ukuran dokumen OneNote yang dapat diproses?  
**A:** Meskipun tidak ada batasan keras, notebook yang sangat besar mungkin memerlukan lebih banyak memori heap; pertimbangkan memprosesnya secara bertahap.

**Q:** Bagaimana cara mengekstrak gambar dari OneNote?  
**A:** Implementasikan metode `VisitImageStart` untuk mengakses `image.getImageData()` dan menulis byte ke file.

---

**Terakhir Diperbarui:** 2025-12-03  
**Diuji Dengan:** Aspose.Note for Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}