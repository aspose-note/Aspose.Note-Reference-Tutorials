---
date: 2026-01-18
description: Pelajari cara mengatur warna font Java di OneNote menggunakan Aspose.Note,
  menyorot teks, mengubah ukuran font, dan menyimpan OneNote sebagai PDF. Panduan
  langkah demi langkah dengan kode.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Mengatur Warna Font Java di OneNote – Aspose.Note
url: /id/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set Font Color Java di OneNote – Aspose.Note

## Introduction

Dalam tutorial ini Anda akan mempelajari cara **set font color Java** untuk teks di dalam dokumen OneNote menggunakan API Aspose.Note for Java. Kami akan menelusuri proses memuat file `.one`, mengakses node RichText‑nya, menerapkan perubahan warna, sorotan, dan ukuran font, serta akhirnya **menyimpan OneNote sebagai PDF**. Baik Anda perlu **menyorot teks onenote**, **mengubah ukuran font onenote**, atau sekadar mengubah gaya teks secara keseluruhan, langkah‑langkah di bawah ini memberikan solusi lengkap yang siap produksi.

## Quick Answers
- **Apakah saya dapat mengubah warna font pada kata‑kata tertentu?** Ya – iterasi objek `TextRun` dan panggil `setFontColor`.
- **Apakah Aspose.Note memungkinkan saya menyimpan OneNote sebagai PDF?** Tentu; gunakan `document.save("output.pdf")`.
- **Versi Java apa yang dibutuhkan?** Java 8 atau yang lebih baru.
- **Apakah sorotan (highlight) didukung?** Gunakan `setHighlight(Color)` pada `TextStyle`.
- **Bisakah saya mengonversi OneNote ke PDF dalam satu baris?** Tidak secara langsung, tetapi metode `save` menangani konversinya.

## What is “set font color java”?

Frasa ini merujuk pada penetapan warna font baru secara programatik pada elemen teks dalam file OneNote menggunakan kode Java. Dengan Aspose.Note, Anda mendapatkan kontrol penuh atas atribut gaya seperti warna font, sorotan, dan ukuran tanpa harus membuka UI OneNote.

## Why change text style onenote?

- **Meningkatkan keterbacaan** – teks berwarna atau disorot menarik perhatian pada poin‑poin penting.
- **Konsistensi merek** – terapkan warna korporat pada catatan rapat.
- **Kualitas ekspor** – catatan yang bergaya terlihat profesional ketika Anda **mengonversi onenote ke pdf** untuk dibagikan.

## Prerequisites

Sebelum memulai, pastikan Anda memiliki:

1. Pengetahuan dasar pemrograman Java.  
2. JDK 8 atau yang lebih baru terpasang.  
3. Perpustakaan Aspose.Note for Java yang sudah ditambahkan ke proyek Anda (Maven/Gradle atau JAR manual).  
4. File contoh OneNote (`Sample1.one`) untuk percobaan.  

## Import Packages

First, import the classes we’ll need:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## Step‑by‑Step Guide

### Step 1: Load the Document

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

Kami memuat file OneNote (`Sample1.one`) sehingga Aspose.Note dapat bekerja dengan struktur internalnya.

### Step 2: Access RichText Nodes

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

Objek `RichText` berisi paragraf‑paragraf sebenarnya. Dengan mengambil node pertama, kami memperoleh pegangan pada teks yang ingin kami gaya.

### Step 3: Change Text Style (set font color java)

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

Di dalam loop kami **set font color Java** menjadi kuning, menerapkan sorotan biru (menunjukkan **highlight text onenote**), dan memperbesar ukuran menjadi 20 point, yang menggambarkan **modify font size onenote**.

### Step 4: Save the Document (save onenote as pdf)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

Memanggil `save` dengan ekstensi `.pdf` secara otomatis **convert onenote to pdf**, menghasilkan file siap‑bagikan.

## Common Issues & Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| Tidak ada perubahan warna yang terlihat | Dokumen dibuka di OneNote sebelum disimpan | Tutup OneNote atau muat ulang file setelah proses Java selesai |
| Sorotan tidak diterapkan | Menggunakan warna yang sama dengan latar belakang | Pilih `Color` yang kontras (mis., `Color.yellow`) |
| `document.save` melempar `IOException` | Jalur output tidak valid | Pastikan direktori ada dan Anda memiliki izin menulis |

## Frequently Asked Questions

**Q: Bisakah saya menerapkan perubahan gaya ini hanya pada bagian‑bagian tertentu dari file OneNote saya?**  
A: Ya – filter node `RichText` berdasarkan `Section` atau `Page` induknya sebelum mengiterasi `TextRun`.

**Q: Selain warna, sorotan, dan ukuran, format apa lagi yang dapat ditangani Aspose.Note?**  
A: Anda dapat mengubah keluarga font, tebal/miring/garis bawah, perataan, dan bahkan spasi paragraf.

**Q: Apakah memungkinkan memproses banyak file OneNote secara batch?**  
A: Tentu. Bungkus logika pemuatan dan penataan dalam loop yang memproses setiap file `.one` dalam sebuah folder.

**Q: Apakah perpustakaan ini mendukung penyimpanan langsung ke format lain seperti DOCX?**  
A: Ya – Aspose.Note dapat mengekspor ke PDF, DOCX, HTML, dan beberapa format gambar.

**Q: Di mana saya dapat menemukan contoh‑contoh lain dan referensi API?**  
A: Kunjungi situs dokumentasi resmi Aspose.Note, jelajahi referensi API, dan unduh trial gratis untuk percobaan langsung.

## Conclusion

Anda kini memiliki contoh lengkap end‑to‑end tentang cara **set font color Java**, menyorot teks, mengubah ukuran font, dan **menyimpan OneNote sebagai PDF** menggunakan Aspose.Note. Silakan sesuaikan kode untuk menargetkan halaman tertentu, menerapkan gaya bersyarat, atau mengintegrasikannya ke dalam pipeline pemrosesan dokumen yang lebih besar.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-18  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose  

---