---
date: 2025-12-21
description: Pelajari cara mendapatkan dimensi gambar di Java menggunakan Aspose.Note.
  Ekstrak lebar, tinggi, nama file, dan lainnya dari file OneNote hanya dalam beberapa
  langkah.
linktitle: Get Image Dimensions Java from OneNote
second_title: Aspose.Note Java API
title: Dapatkan Dimensi Gambar Java dari OneNote
url: /id/java/onenote-hyperlinks-images/get-image-info/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dapatkan Dimensi Gambar Java dari OneNote

## Introduction

Jika Anda perlu **get image dimensions java** dari notebook OneNote, Anda berada di tempat yang tepat. Dalam banyak skenario otomatisasi—pembuatan laporan, migrasi konten, atau analitik—Anda akan ingin mengetahui lebar, tinggi, ukuran asli, dan nama file setiap gambar tanpa harus membuka notebook secara manual. Tutorial ini memandu Anda mengekstrak informasi tersebut secara programatis menggunakan Aspose.Note for Java.

## Quick Answers
- **What does the code do?** Mengambil setiap gambar dalam file OneNote dan mencetak dimensinya, ukuran asli, nama file, serta tanggal modifikasi.  
- **Which library is required?** Aspose.Note for Java.  
- **Do I need a license?** Lisensi sementara dapat digunakan untuk pengujian; lisensi penuh diperlukan untuk produksi.  
- **How many lines of code?** Sekitar 30 baris, dibagi menjadi langkah‑langkah yang jelas dan dapat digunakan kembali.  
- **Typical run time?** Milidetik untuk notebook standar dengan beberapa puluh gambar.

## Prerequisites

Sebelum kita masuk ke implementasi, pastikan Anda memiliki prasyarat berikut:

### 1. Java Development Kit (JDK)

Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda. Anda dapat mengunduh dan menginstal JDK terbaru dari [Oracle website](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Aspose.Note for Java Library

Unduh dan sertakan pustaka Aspose.Note for Java dalam proyek Anda. Anda dapat memperoleh pustaka tersebut dari [download page](https://releases.aspose.com/note/java/).

### 3. OneNote Document

Siapkan dokumen OneNote contoh yang berisi gambar. Dokumen ini akan digunakan untuk mengekstrak informasi gambar secara programatis.

## Import Packages

Untuk memulai, impor paket yang diperlukan dari Aspose.Note for Java:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Mari kita uraikan kode di atas menjadi instruksi langkah‑demi‑langkah:

## How to get image dimensions java from OneNote

### Step 1: Set Document Directory

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur ke dokumen OneNote Anda.

### Step 2: Load the Document

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Muat dokumen OneNote menggunakan pustaka Aspose.Note for Java. Pastikan Anda memberikan jalur yang benar ke dokumen Anda.

### Step 3: Get All Images

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Ambil semua gambar dari dokumen OneNote yang telah dimuat.

### Step 4: Print Total Images Count

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Cetak total jumlah gambar yang ditemukan dalam dokumen.

### Step 5: Traverse and Print Image Information

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Iterasi melalui daftar gambar dan cetak detail seperti lebar, tinggi, dimensi asli, nama file, serta waktu terakhir dimodifikasi untuk setiap gambar.

## Why extract images from OneNote using Java?

- **Automation:** Menghilangkan inspeksi manual notebook.  
- **Data Analytics:** Menyalurkan metadata gambar ke pipeline pelaporan.  
- **Migration:** Mempertahankan atribut gambar saat memindahkan konten ke platform lain.  
- **Performance:** Mengambil hanya metadata yang Anda butuhkan, menghindari parsing file yang berat.

## Common Pitfalls & Tips

- **Incorrect path:** Periksa kembali bahwa `dataDir` diakhiri dengan pemisah file yang tepat (`/` atau `\`).  
- **License issues:** Tanpa lisensi yang valid, Aspose.Note dapat menampilkan peringatan evaluasi.  
- **Large notebooks:** Untuk notebook dengan ribuan gambar, pertimbangkan memproses dalam batch untuk mengurangi konsumsi memori.

## Frequently Asked Questions

### Q1: Can Aspose.Note for Java handle other document formats apart from OneNote?

A1: Ya, Aspose.Note for Java mendukung berbagai format dokumen, termasuk OneNote, PDF, dan Microsoft Word.

### Q2: Is Aspose.Note for Java suitable for both personal and commercial use?

A2: Ya, Anda dapat menggunakan Aspose.Note for Java untuk keperluan pribadi maupun komersial.

### Q3: Does Aspose.Note for Java offer technical support?

A3: Ya, dukungan teknis tersedia melalui forum Aspose di [here](https://forum.aspose.com/c/note/28).

### Q4: Can I try Aspose.Note for Java before making a purchase?

A4: Ya, Anda dapat menjelajahi versi percobaan gratis Aspose.Note for Java dari [Aspose.Note for Java](https://releases.aspose.com/note/java/).

### Q5: How can I obtain a temporary license for Aspose.Note for Java?

A5: Anda dapat memperoleh lisensi sementara dari [Temporary license/](https://purchase.aspose.com/temporary-license/).

## Conclusion

Dengan mengikuti langkah‑langkah yang dijelaskan dalam tutorial ini, Anda dapat secara efektif **get image dimensions java** dari dokumen OneNote menggunakan Aspose.Note for Java. Mengintegrasikan fungsionalitas ini ke dalam aplikasi Anda dapat mengotomatisasi tugas terkait pemrosesan dokumen, meningkatkan efisiensi dan produktivitas.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 23.12  
**Author:** Aspose  

---