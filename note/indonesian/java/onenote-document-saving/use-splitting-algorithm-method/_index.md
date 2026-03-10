---
date: 2025-12-18
description: Pelajari cara mengekspor halaman OneNote ke PDF menggunakan Aspose.Note
  untuk Java. Pilih algoritma pemisahan, atur pemisahan halaman, dan hasilkan file
  PDF dengan mudah.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: Ekspor Halaman OneNote dengan Metode Algoritma Pemisahan – Aspose.Note
url: /id/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor Halaman OneNote dengan Metode Algoritma Pemisahan – Aspose.Note

## Pendahuluan

Jika Anda perlu **mengekspor halaman OneNote** ke dokumen PDF secara programatis, Aspose.Note untuk Java mempermudahnya. Dalam tutorial ini kami akan membahas Metode Algoritma Pemisahan, yang memungkinkan Anda mengontrol bagaimana konten dipisahkan antar halaman, memastikan output PDF yang bersih dan mudah dibaca. Anda akan melihat cara mengatur opsi penyimpanan PDF, memilih algoritma pemisahan halaman yang tepat, dan akhirnya menghasilkan file PDF—semua dengan hanya beberapa baris kode Java.

## Jawaban Cepat
- **Apa yang dilakukan Algoritma Pemisahan?** Algoritma menentukan bagaimana objek yang melintasi batas halaman ditangani saat mengekspor halaman OneNote ke PDF.  
- **Perpustakaan apa yang diperlukan?** Aspose.Note untuk Java (unduh dari situs resmi Aspose).  
- **Apakah saya memerlukan lisensi?** Lisensi sementara atau penuh diperlukan untuk penggunaan produksi; percobaan gratis tersedia.  
- **Bisakah saya mengekspor notebook OneNote yang besar?** Ya – perpustakaan ini memproses file besar secara efisien dan memungkinkan Anda mengatur aturan pemisahan halaman.  
- **Format output apa yang didukung?** PDF, JPEG, PNG, XPS, dan lainnya; panduan ini fokus pada ekspor PDF.

## Apa itu **ekspor halaman onenote**?
Mengekspor halaman OneNote berarti mengonversi format file native `.one` ke format yang lebih portabel seperti PDF. Ini berguna untuk berbagi, mengarsipkan, atau mencetak konten tanpa memerlukan aplikasi OneNote.

## Mengapa menggunakan Algoritma Pemisahan untuk **ekspor halaman onenote**?
Algoritma memberikan kontrol yang sangat detail tentang bagaimana objek kompleks (tabel, gambar, gambar tangan) ditangani pada pemisahan halaman. Dengan memilih algoritma yang tepat Anda dapat:

* Mempertahankan tata letak visual setiap halaman.  
* Menghindari konten terpotong yang seharusnya terpotong.  
* Mengurangi jumlah halaman yang dihasilkan ketika objek dapat dipindahkan ke halaman berikutnya dengan bersih.  

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Java Development Kit (JDK): Pastikan Anda memiliki JDK terpasang di sistem Anda. Anda dapat mengunduhnya dari [situs web](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Perpustakaan Aspose.Note untuk Java: Unduh dan instal perpustakaan Aspose.Note untuk Java dari [tautan unduhan](https://releases.aspose.com/note/java/).

## Impor Paket

Dalam proyek Java Anda, impor paket yang diperlukan untuk memanfaatkan fungsionalitas Aspose.Note.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Langkah 1: Tentukan Direktori Dokumen

Siapkan direktori tempat dokumen OneNote Anda berada.

```java
String dataDir = "Your Document Directory";
```

## Langkah 2: Muat Dokumen OneNote

Muat dokumen OneNote menggunakan kelas `Document` dari Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Langkah 3: Atur Opsi Penyimpanan PDF

Buat instance `PdfSaveOptions` untuk menentukan opsi penyimpanan dokumen sebagai PDF. Di sinilah Anda **mengatur pemisahan halaman** dan pengaturan lain yang terkait dengan PDF.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## Langkah 4: Atur Algoritma Pemisahan Halaman

Pilih algoritma pemisahan yang sesuai dengan kebutuhan Anda. Di sini, kami menggunakan `KeepPartAndCloneSolidObjectToNextPageAlgorithm`, yang mempertahankan sebagian objek pada halaman saat ini dan menggandakan sisanya ke halaman berikutnya.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## Langkah 5: Simpan Dokumen

Simpan dokumen dengan opsi penyimpanan PDF yang telah ditentukan. Langkah ini **menghasilkan output PDF onenote** yang dapat Anda buka, bagikan, atau cetak.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **Objek terpotong pada batas halaman** | Coba algoritma lain seperti `AlwaysSplitObjectsAlgorithm` atau tingkatkan nilai ambang pada `KeepPartAndCloneSolidObjectToNextPageAlgorithm`. |
| **PDF output kosong** | Pastikan file `.one` sumber tidak rusak dan jalur `dataDir` sudah benar. |
| **Kinerja lambat pada notebook besar** | Gunakan `pdfSaveOptions.setCompressImages(true)` untuk mengurangi penggunaan memori, dan pertimbangkan memproses notebook dalam bagian yang lebih kecil. |

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya menggunakan Aspose.Note untuk Java dengan bahasa pemrograman lain?**  
J: Ya, Aspose.Note juga tersedia untuk .NET, C++, dan Python.

**T: Apakah Aspose.Note cocok untuk memproses file OneNote yang besar?**  
J: Tentu saja. Perpustakaan ini dioptimalkan untuk menangani notebook besar secara efisien.

**T: Di mana saya dapat menemukan sumber daya tambahan dan dukungan untuk Aspose.Note?**  
J: Anda dapat merujuk ke [dokumentasi](https://reference.aspose.com/note/java/) dan [forum](https://forum.aspose.com/c/note/28) untuk dukungan dan panduan.

**T: Bisakah saya mencoba Aspose.Note sebelum membeli?**  
J: Ya, Anda dapat memanfaatkan [percobaan gratis](https://releases.aspose.com/) untuk menjelajahi fitur sebelum melakukan pembelian.

**T: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Note?**  
J: Anda dapat meminta [lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk mengevaluasi produk selama periode percobaan.

---

**Terakhir Diperbarui:** 2025-12-18  
**Diuji Dengan:** Aspose.Note 24.12 untuk Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}