---
date: 2025-12-21
description: Pelajari cara membuat dokumen OneNote dengan Java dan dengan mudah menyisipkan
  gambar menggunakan Aspose.Note untuk Java. Panduan langkah demi langkah untuk pengembang
  Java.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Cara membuat dokumen OneNote Java – Membuat Dokumen dan Menyisipkan Gambar
  dengan Stream
url: /id/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara membuat onenote document java – Membuat Dokumen dan Menyisipkan Gambar dengan Stream

## Introduction

Selamat datang! Dalam tutorial ini Anda akan **create onenote document java** dari awal dan belajar cara menyisipkan gambar menggunakan aliran gambar. Kami akan membimbing Anda melalui setiap langkah, menjelaskan mengapa setiap bagian penting, dan memberikan tip praktis agar Anda dapat menerapkan teknik ini dalam proyek nyata. Pada akhir tutorial, Anda akan dapat menghasilkan halaman OneNote secara programatis dan menyematkan gambar tepat di tempat yang Anda inginkan.

## Quick Answers
- **What library do I need?** Aspose.Note for Java  
- **Can I insert images from a stream?** Yes – just pass an `InputStream` to the `Image` constructor.  
- **Which format can I export to?** Any format supported by Aspose.Note, e.g., PDF, DOCX, HTML.  
- **Do I need a license for development?** A free temporary license works for evaluation; a full license is required for production.  
- **What Java version is required?** Java 8 or higher.

## What is “create onenote document java”?

Membuat dokumen OneNote dalam Java berarti menggunakan API Aspose.Note untuk secara programatis membangun struktur notebook—halaman, outline, dan elemen—tanpa membuka klien desktop OneNote. Pendekatan ini ideal untuk pembuatan laporan otomatis, pemrosesan batch catatan, atau mengintegrasikan konten OneNote ke dalam aplikasi Java yang lebih besar.

## Why use Aspose.Note for Java to create onenote document java?

- **Full control** over page layout, outline positioning, and element styling. → Kontrol penuh atas tata letak halaman, posisi outline, dan gaya elemen.  
- **No COM interop** – works on any OS that supports Java. → Tanpa interop COM – bekerja pada semua OS yang mendukung Java.  
- **Rich export options** – convert the same document to PDF, DOCX, HTML, etc., with a single call. → Opsi ekspor kaya – mengonversi dokumen yang sama ke PDF, DOCX, HTML, dll., dengan satu panggilan.  
- **Stream‑friendly** – you can load images directly from memory, network, or cloud storage. → Ramahan stream – Anda dapat memuat gambar langsung dari memori, jaringan, atau penyimpanan cloud.

## Prerequisites

Sebelum kita mulai, pastikan Anda telah menyiapkan hal‑hal berikut:

### Java Development Kit (JDK)

JDK terbaru (8 atau lebih tinggi) terpasang di mesin Anda.

### Aspose.Note for Java Library

Unduh perpustakaan dari halaman rilis resmi Aspose: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### IDE Setup

Konfigurasikan IDE favorit Anda (IntelliJ IDEA, Eclipse, VS Code) untuk menyertakan file JAR Aspose.Note pada classpath proyek.

## Import Packages

Untuk memulai, impor kelas‑kelas Java dan Aspose.Note yang diperlukan. Impor ini memberi Anda akses ke pembuatan dokumen, penanganan halaman, manajemen outline, dan penyisipan gambar.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Step 1: Set Up Document Directory

Tentukan folder yang berisi gambar sumber Anda dan tempat file output akan disimpan. Ganti placeholder dengan path aktual di mesin Anda.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Create Document Object

Instansiasi `Document` baru. Objek ini mewakili notebook OneNote yang sedang Anda bangun.

```java
Document doc = new Document();
```

## Step 3: Initialize Page Object

Buat `Page` yang akan menampung semua outline dan elemen untuk halaman notebook ini.

```java
Page page = new Page();
```

## Step 4: Create Outline

`Outline` berfungsi sebagai wadah untuk elemen‑elemen yang diposisikan. Di sini kami mengatur offset vertikal dan horizontal untuk menempatkan outline pada halaman.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Step 5: Create Outline Element

`OutlineElement` akan menjadi tempat gambar yang akan kami sisipkan.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Step 6: Load Image Stream

Buka file gambar sebagai stream. Menggunakan stream memungkinkan Anda membaca gambar dari sumber apa pun (sistem file, jaringan, basis data) tanpa harus menyimpannya terlebih dahulu ke disk.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Step 7: Insert Image

Buat objek `Image`. Argumen pertama dapat `null` ketika Anda menyediakan stream nanti, tetapi untuk kesederhanaan kami merujuk ke path file di sini dan mengatur perataan ke sisi kanan halaman.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Step 8: Append Image to Outline Element

Tambahkan gambar ke elemen outline sehingga menjadi bagian dari hierarki visual halaman.

```java
outlineElem1.appendChildLast(image);
```

## Step 9: Append Outline Element to Outline

Sekarang lampirkan elemen outline (yang berisi gambar) ke wadah outline.

```java
outline1.appendChildLast(outlineElem1);
```

## Step 10: Append Outline to Page

Letakkan outline pada halaman.

```java
page.appendChildLast(outline1);
```

## Step 11: Append Page to Document

Tambahkan halaman yang telah selesai dibangun ke objek dokumen.

```java
doc.appendChildLast(page);
```

## Step 12: Save Document

Akhirnya, simpan dokumen OneNote dalam format yang Anda butuhkan. Pada contoh ini kami mengekspor ke PDF, tetapi Anda dapat memilih format apa pun yang didukung oleh Aspose.Note.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Dengan mengikuti langkah‑langkah ini Anda telah berhasil **create onenote document java** dan menyematkan gambar menggunakan input stream.

## Common Pitfalls & Tips

- **Stream not closed** – In a production scenario, always close the `InputStream` in a `finally` block or use try‑with‑resources. → Stream tidak ditutup – Dalam skenario produksi, selalu tutup `InputStream` di blok `finally` atau gunakan try‑with‑resources.  
- **Incorrect file path** – Double‑check that `dataDir` ends with the appropriate separator (`/` or `\`). → Path file tidak benar – Periksa kembali bahwa `dataDir` diakhiri dengan pemisah yang tepat (`/` atau `\`).  
- **Image alignment** – If the image appears off‑screen, adjust the outline’s `VerticalOffset`/`HorizontalOffset` values. → Penjajaran gambar – Jika gambar muncul di luar layar, sesuaikan nilai `VerticalOffset`/`HorizontalOffset` pada outline.  
- **License exceptions** – Using the evaluation version may add a watermark to the output; apply a valid license to remove it. → Pengecualian lisensi – Menggunakan versi evaluasi dapat menambahkan watermark pada output; terapkan lisensi yang valid untuk menghilangkannya.

## Frequently Asked Questions

### Q1: Is Aspose.Note for Java compatible with all versions of OneNote?

A1: Aspose.Note for Java supports various OneNote file formats, ensuring compatibility across desktop, online, and mobile versions. → Aspose.Note for Java mendukung berbagai format file OneNote, memastikan kompatibilitas di versi desktop, online, dan seluler.

### Q2: Can I customize the appearance of inserted images in OneNote documents using Aspose.Note for Java?

A2: Yes, you can modify alignment, size, rotation, and even apply cropping by using the corresponding properties on the `Image` object. → Ya, Anda dapat mengubah perataan, ukuran, rotasi, bahkan menerapkan pemotongan dengan menggunakan properti yang sesuai pada objek `Image`.

### Q3: Does Aspose.Note for Java provide support for other document formats besides PDF?

A3: Absolutely. The API can export to DOCX, HTML, XPS, and several other formats, giving you flexibility in how you share or archive your notes. → Tentu saja. API dapat mengekspor ke DOCX, HTML, XPS, dan beberapa format lainnya, memberi Anda fleksibilitas dalam cara berbagi atau mengarsipkan catatan.

### Q4: Where can I find additional resources and support for Aspose.Note for Java?

A4: The official Aspose website offers extensive documentation, code examples, forums, and temporary licenses for evaluation. → Situs resmi Aspose menyediakan dokumentasi lengkap, contoh kode, forum, dan lisensi sementara untuk evaluasi.

### Q5: Is there a trial version available for Aspose.Note for Java?

A5: Yes, you can download a free trial from the Aspose release page to explore all features before purchasing. → Ya, Anda dapat mengunduh versi percobaan gratis dari halaman rilis Aspose untuk menjelajahi semua fitur sebelum membeli.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}