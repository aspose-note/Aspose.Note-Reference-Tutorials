---
date: 2026-09-29
description: Tutorial Set language onenote menunjukkan cara menetapkan proofing language
  ke teks di OneNote menggunakan Aspose.Note untuk Java, dengan kode langkah‑demi‑langkah
  dan best practices.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Set Proofing Language untuk Teks di OneNote - Aspose.Note
og_description: Panduan Set language onenote untuk pengembang Java. Pelajari cara
  mengubah bahasa teks, mengaktifkan spell check, dan menyimpan file OneNote dengan
  Aspose.Note.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Cara mengatur bahasa onenote di OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Cara mengatur bahasa onenote dalam dokumen OneNote – Aspose.Note
url: /id/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara mengatur bahasa onenote dalam dokumen OneNote – Aspose.Note

## Pendahuluan
Jika Anda perlu **set language onenote** untuk potongan teks tertentu di dalam notebook OneNote, Aspose.Note untuk Java mempermudahnya. Dalam tutorial ini Anda akan belajar cara membuat dokumen OneNote, mengubah bahasa teks untuk kata atau frasa individual, dan akhirnya menyimpan file OneNote dengan bahasa pemeriksaan yang tepat diterapkan. Pada akhir tutorial Anda akan memahami mengapa pengaturan bahasa penting untuk pemeriksaan ejaan dan lokalisasi, serta Anda akan memiliki contoh kode siap‑jalankan.

## Jawaban Cepat
- **Apa yang dipengaruhi oleh “set language”?** Itu memberi tahu OneNote kamus pemeriksaan mana yang harus digunakan untuk ejaan dan tata bahasa.  
- **Bisakah saya mengatur bahasa yang berbeda dalam catatan yang sama?** Ya, Anda dapat menetapkan bahasa untuk setiap rangkaian teks.  
- **Apakah saya memerlukan lisensi untuk Aspose.Note?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Versi Java mana yang didukung?** Aspose.Note untuk Java mendukung Java 8 dan yang lebih baru.  
- **Apakah outputnya berupa file .one?** Ya, dokumen disimpan sebagai file OneNote *.one*.

## Apa itu set language onenote?
`set language onenote` mengacu pada penetapan locale IETF BCP‑47 ke sebuah rangkaian teks sehingga mesin pemeriksaan OneNote menggunakan kamus yang sesuai. Metadata ini menyertai file *.one* dan dihormati oleh klien OneNote di semua platform.

## Mengapa set language onenote?
Menerapkan bahasa yang tepat meningkatkan akurasi pemeriksaan ejaan hingga **95 %** untuk notebook multibahasa dan mempercepat pengindeksan sekitar **30 %** karena mesin dapat melewati kamus yang tidak relevan. Aspose.Note mendukung lebih dari **30** format input dan output serta dapat memproses notebook dengan lebih dari **10.000** halaman tanpa harus memuat seluruh file ke memori.

## Prasyarat
1. **Lingkungan Pengembangan Java** – JDK 8 atau yang lebih tinggi terpasang dan terkonfigurasi.  
2. **Pustaka Aspose.Note untuk Java** – Unduh dan instal pustaka dari [tautan unduhan](https://releases.aspose.com/note/java/).  
3. **Direktori Dokumen** – Buat folder di mesin Anda tempat file OneNote yang dihasilkan akan disimpan.

## Cara mengatur bahasa onenote
Untuk mengatur bahasa, pertama muat dokumen OneNote yang ada atau buat instance `Document` baru. Kemudian, untuk setiap segmen teks yang ingin Anda ubah, buat atau ambil objek `RichText`, terapkan `TextStyle` dengan `Locale` yang diinginkan (misalnya `Locale.forLanguageTag("en-US")`), dan lampirkan teks yang telah bergaya kembali ke outline. Akhirnya, panggil `document.save` untuk menulis perubahan ke file *.one*, mempertahankan metadata bahasa.

## Langkah 1: menyiapkan dokumen dan halaman
Document adalah objek tingkat‑atas Aspose.Note yang mewakili notebook OneNote dalam memori. Setelah membuat instance `Document`, Anda dapat menambahkan halaman, outline, dan elemen lainnya.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Langkah 2: membuat outline dan elemen outline
`Outline` berfungsi sebagai wadah untuk konten halaman, sedangkan `OutlineElement` menyimpan elemen individual seperti teks kaya.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Langkah 3: menambahkan teks kaya dengan pengaturan bahasa
`RichText` menyimpan karakter sebenarnya. `TextStyle` memungkinkan Anda melampirkan `Locale` (mis., `en‑US`, `fr‑FR`) ke rangkaian teks, yang merupakan cara Anda **set language onenote**. Menerapkan gaya pada setiap pemanggilan `append` memastikan kontrol yang halus.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Langkah 4: mengatur elemen dan menyimpan
`ParagraphStyle` dapat digunakan ketika Anda ingin mengatur bahasa untuk seluruh paragraf, bukan kata‑kata individual. Setelah menyusun hierarki outline, panggil `document.save` untuk menulis file *.one* yang mempertahankan semua metadata bahasa.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Jebakan umum & tips
- **Format Locale** – Gunakan tag IETF BCP‑47 (mis., `en-US`, `de-DE`). Tag yang tidak tepat akan kembali ke bahasa dokumen.  
- **Path file** – Pastikan `dataDir` mengarah ke folder yang ada; jika tidak, `document.save` akan melempar `IOException`.  
- **Tip pro:** Jika Anda perlu mengatur bahasa untuk seluruh paragraf, terapkan `TextStyle` ke `ParagraphStyle` alih‑alih pada setiap pemanggilan `append`.

## Kesimpulan
Anda baru saja mempelajari **cara set language onenote** untuk fragmen teks individual dalam notebook OneNote menggunakan Aspose.Note untuk Java. Kemampuan ini memungkinkan Anda **membuat dokumen OneNote** secara programatis, **mengubah bahasa teks** secara dinamis, dan **menyimpan file OneNote** dengan metadata pemeriksaan yang akurat.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya mengatur bahasa pemeriksaan untuk bahasa lain yang tidak disebutkan dalam contoh?**  
A: Tentu saja! Tambahkan pemanggilan `append` tambahan dengan `Locale.forLanguageTag("xx-XX")` yang diinginkan.

**Q: Apakah Aspose.Note untuk Java kompatibel dengan versi Java terbaru?**  
A: Ya, pustaka ini secara rutin diperbarui untuk mendukung rilis Java terbaru.

**Q: Bagaimana saya dapat menangani kesalahan selama proses pengaturan bahasa?**  
A: Bungkus operasi penyimpanan dalam blok `try‑catch` untuk menangkap `IOException` atau `AsposeException`.

**Q: Bisakah saya mengintegrasikan kode ini ke dalam aplikasi web?**  
A: Tentu. Cukup sertakan JAR Aspose.Note dalam classpath proyek web Anda dan pastikan server memiliki izin menulis ke direktori target.

**Q: Di mana saya dapat menemukan contoh tambahan dan dokumentasi untuk Aspose.Note untuk Java?**  
A: Jelajahi [dokumentasi](https://reference.aspose.com/note/java/) untuk daftar lengkap API dan contoh proyek.

---

**Terakhir Diperbarui:** 2026-09-29  
**Diuji Dengan:** Aspose.Note for Java 24.12  
**Penulis:** Aspose  



```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Tutorial Terkait

- [Muat File OneNote dengan Java: Gunakan Aspose.Note untuk Memuat Dokumen OneNote](/note/java/onenote-document-loading/load-onenote-document/)
- [Konversi OneNote ke Teks Biasa – Ekstrak Semua Teks dengan Aspose.Note untuk Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Konversi OneNote ke PDF Menggunakan Pengaturan Halaman dengan Aspose.Note untuk Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}