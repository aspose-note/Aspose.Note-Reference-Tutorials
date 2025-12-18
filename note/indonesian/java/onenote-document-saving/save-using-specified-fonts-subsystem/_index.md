---
date: 2025-12-18
description: Pelajari cara **menyimpan OneNote sebagai PDF** menggunakan subsistem
  font yang ditentukan dalam Java dengan Aspose.Note. Panduan ini juga menunjukkan
  cara mengonversi OneNote ke PDF, memuat file font khusus, dan menentukan font default.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Simpan OneNote sebagai PDF dengan Subsystem Font yang Ditentukan
url: /id/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan OneNote sebagai PDF Menggunakan Subsystem Font yang Ditentukan

## Pendahuluan

Dalam banyak skenario bisnis Anda perlu **menyimpan OneNote sebagai PDF** sambil mempertahankan tampilan persis dari halaman asli. Aspose.Note untuk Java mempermudah hal ini dengan memungkinkan Anda mengontrol subsystem font selama konversi. Pada tutorial ini kami akan membahas tiga cara praktis untuk **mengonversi OneNote ke PDF**, mencakup cara **memuat file font khusus**, **menentukan font default**, dan bahkan **menggunakan aliran font** ketika font tidak tersedia di mesin target.

## Jawaban Cepat
- **Apa arti “simpan OneNote sebagai PDF”?** Itu mengonversi file .one menjadi PDF sambil menjaga tata letak dan gaya tetap utuh.  
- **API mana yang menangani font?** `DocumentFontsSubsystem` memungkinkan Anda menentukan font default atau memuat file/stream font khusus.  
- **Apakah saya memerlukan lisensi untuk produksi?** Ya, lisensi komersial Aspose.Note diperlukan untuk penggunaan non‑trial.  
- **Bisakah saya mengonversi beberapa file sekaligus?** Tentu – cukup lakukan perulangan pada logika pemuatan dan penyimpanan `Document`.  
- **Versi Java apa yang dibutuhkan?** Java 15 atau lebih baru (contoh menggunakan JDK 15).

## Apa itu “simpan OneNote sebagai PDF” dengan subsystem font?

Menyimpan OneNote sebagai PDF dengan subsystem font berarti bahwa selama proses konversi Aspose.Note menggantikan glyph yang hilang dengan font yang Anda sediakan. Ini menjamin PDF terlihat identik di perangkat apa pun, bahkan ketika font asli tidak terpasang.

## Mengapa mengontrol subsystem font saat Anda **mengonversi OneNote ke PDF**?

- **Branding konsisten** – dokumen korporat mempertahankan jenis huruf yang tepat.  
- **Keandalan lintas‑platform** – PDF ditampilkan sama di Windows, macOS, Linux, dan perangkat seluler.  
- **Mengurangi kesalahan** – peringatan font yang hilang menghilang, menghasilkan output yang bersih.

## Prasyarat

### 1. Java Development Kit (JDK)

Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda. Anda dapat mengunduhnya dari [here](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) jika belum.

### 2. Perpustakaan Aspose.Note untuk Java

Unduh dan siapkan perpustakaan Aspose.Note untuk Java. Anda dapat mengunduhnya dari [website](https://releases.aspose.com/note/java/).

## Impor Paket

Pastikan mengimpor paket yang diperlukan dalam proyek Java Anda:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Sekarang mari kita uraikan setiap contoh menjadi beberapa langkah untuk memahami prosesnya dengan lebih baik.

## Cara **menyimpan OneNote sebagai PDF** menggunakan Document Fonts Subsystem dengan font default

### Langkah 1: Simpan Menggunakan Document Fonts Subsystem dengan Nama Font Default

Langkah ini menunjukkan cara **menyimpan OneNote sebagai PDF** secara sederhana dengan menentukan nama font default.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Pada langkah ini:
- Dokumen OneNote dimuat menggunakan Aspose.Note.
- **Font default** ditentukan sebagai **"Times New Roman"**.
- Dokumen disimpan dalam format PDF dengan font yang dipilih.

### Langkah 2: Simpan Menggunakan Document Fonts Subsystem dengan Font Default dari File

Di sini kami **memuat file font khusus** dan menggunakannya sebagai cadangan saat mengonversi ke PDF.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Poin penting- **File font khusus** `geo_1.ttf` **dimuat dari disk**.
- `usingDefaultFontFromFile` **menentukan font default dari file**, memastikan PDF menggunakan font ini ketika yang asli tidak ada.
- PDF yang dihasilkan mempertahankan tampilan yang diinginkan.

### Langkah 3: Simpan Menggunakan Document Fonts Subsystem dengan Font Default dari Stream

Kadang-kadang font disimpan di basis data atau diterima melalui jaringan. Contoh ini menunjukkan cara **menggunakan aliran font**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Apa yang terjadi di sini:
- File font dibuka sebagai **InputStream**, berguna ketika font berada di sumber non‑file.
- `usingDefaultFontFromStream` **menggunakan aliran font** untuk mendefinisikan font cadangan.
- File OneNote disimpan sebagai PDF dengan font berbasis stream.

## Masalah Umum dan Solusinya

| Masalah | Mengapa Terjadi | Cara Memperbaiki |
|-------|----------------|------------|
| **Peringatan font yang hilang** | File .one sumber merujuk pada font yang tidak ada di mesin. | Sediakan font default melalui `usingDefaultFont`, `usingDefaultFontFromFile`, atau `usingDefaultFontFromStream`. |
| **File font khusus tidak ditemukan** | Jalur ke file `.ttf` salah. | Gunakan jalur absolut atau verifikasi jalur relatif dari direktori kerja. |
| **Stream tidak ditutup** | Eksepsi terjadi sebelum `close()` dipanggil. | Gunakan try‑with‑resources (`try (InputStream stream = ...) { ... }`) untuk penutupan otomatis. |

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya menentukan font yang berbeda untuk bagian berbeda dari dokumen?**  
J: Ya, Anda dapat menerapkan pengaturan font khusus pada elemen teks kaya individual menggunakan kelas `Font` di Aspose.Note.

**T: Apakah Aspose.Note kompatibel dengan semua versi OneNote?**  
J: Aspose.Note mendukung file OneNote dari versi desktop dan seluler terbaru, memastikan kompatibilitas yang luas.

**T: Bagaimana cara menangani font yang hilang saat menyimpan dokumen?**  
J: Gunakan metode subsystem font yang ditunjukkan di atas (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) untuk menyediakan cadangan.

**T: Bisakah saya menyesuaikan properti font seperti ukuran dan gaya?**  
J: Tentu – API memungkinkan Anda mengatur ukuran, gaya, warna, dan atribut lain per‑run.

**T: Apakah ada versi percobaan untuk Aspose.Note untuk Java?**  
J: Ya, versi percobaan gratis dapat diunduh dari situs web Aspose.

## Kesimpulan

Pada tutorial ini kami mempelajari cara **menyimpan OneNote sebagai PDF** sambil mengontrol subsystem font di Java dengan Aspose.Note. Dengan mengikuti tiga pendekatan—menentukan nama font default, memuat file font khusus, atau menggunakan aliran font—Anda dapat menjamin representasi font yang konsisten di semua platform saat mengekspor atau menyimpan dokumen OneNote Anda.

---

**Terakhir Diperbarui:** 2025-12-18  
**Diuji Dengan:** Aspose.Note untuk Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}