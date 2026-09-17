---
date: 2026-03-29
description: Pelajari cara mengatur bahasa untuk teks di OneNote menggunakan Aspose.Note
  untuk Java. Panduan langkah demi langkah ini menunjukkan cara membuat dokumen OneNote,
  mengubah bahasa teks, dan menyimpan file OneNote secara efisien.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Cara Mengatur Bahasa untuk Teks di OneNote – Aspose.Note
url: /id/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengatur Bahasa untuk Teks di OneNote – Aspose.Note

## Pendahuluan
Jika Anda perlu **cara mengatur bahasa** untuk potongan teks tertentu di dalam notebook OneNote, Aspose.Note untuk Java mempermudahnya. Dalam tutorial ini Anda akan belajar cara membuat dokumen OneNote, mengubah bahasa teks untuk kata atau frasa individual, dan akhirnya menyimpan file OneNote dengan bahasa pemeriksaan yang tepat diterapkan. Pada akhir tutorial Anda akan memahami mengapa pengaturan bahasa penting untuk pemeriksaan ejaan dan lokalisasi, serta Anda akan memiliki contoh kode siap‑jalankan.

## Jawaban Cepat
- **Apa yang dipengaruhi oleh “set language”?** Itu memberi tahu OneNote kamus pemeriksaan mana yang digunakan untuk ejaan dan tata bahasa.  
- **Apakah saya dapat mengatur bahasa berbeda dalam catatan yang sama?** Ya, Anda dapat menetapkan bahasa untuk setiap rangkaian teks.  
- **Apakah saya memerlukan lisensi untuk Aspose.Note?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Versi Java mana yang didukung?** Aspose.Note untuk Java mendukung Java 8 dan yang lebih baru.  
- **Apakah outputnya berupa file .one?** Ya, dokumen disimpan sebagai file OneNote *.one*.

## Prasyarat
Sebelum menyelami kode, pastikan Anda memiliki hal‑hal berikut:

1. **Java Development Environment** – JDK 8 atau lebih tinggi terpasang dan dikonfigurasi.  
2. **Aspose.Note for Java Library** – Unduh dan instal pustaka dari [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Buat folder di mesin Anda tempat file OneNote yang dihasilkan akan disimpan.

## Mengapa mengatur bahasa untuk teks di OneNote?
Mengatur bahasa pemeriksaan memastikan bahwa ejaan, saran tata bahasa, dan pengindeksan pencarian bekerja dengan benar untuk konten multibahasa. Ini sangat berguna untuk:

- **Tim global** yang berkolaborasi pada satu notebook.  
- **Dokumentasi terlokalisasi** di mana setiap bagian dapat berada dalam bahasa yang berbeda.  
- **Aplikasi berbasis data** yang menghasilkan catatan secara programatik untuk pengguna di seluruh dunia.

## Impor Paket
Mulailah dengan mengimpor kelas Aspose.Note yang diperlukan serta utilitas Java.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Langkah 1: Siapkan Dokumen dan Halaman
Buat dokumen OneNote baru dan halaman yang akan menampung konten Anda. Langkah ini juga memperlihatkan **membuat dokumen OneNote**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Langkah 2: Buat Outline dan Elemen Outline
Outline adalah wadah untuk konten notebook. Di sini kami membangun struktur yang nantinya akan berisi teks dengan bahasa tertentu.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Langkah 3: Tambahkan Teks Kaya dengan Pengaturan Bahasa
Sekarang kami **mengubah bahasa teks** dengan melampirkan `TextStyle` dengan `Locale` tertentu ke setiap segmen teks. Ini memperlihatkan **mengatur bahasa untuk teks**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Langkah 4: Atur Elemen dan Simpan
Susun hierarki outline, lampirkan ke halaman, dan akhirnya **simpan file OneNote** dengan pengaturan bahasa yang diterapkan.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Kesalahan Umum & Tips
- **Format Locale** – Gunakan tag IETF BCP‑47 (mis., `en-US`, `de-DE`). Tag yang salah akan kembali ke bahasa dokumen.  
- **Path file** – Pastikan `dataDir` mengarah ke folder yang ada; jika tidak, `document.save` akan melempar `IOException`.  
- **Tips pro:** Jika Anda perlu mengatur bahasa untuk seluruh paragraf, terapkan `TextStyle` ke `ParagraphStyle` alih‑alih pada setiap pemanggilan `append`.

## Kesimpulan
Anda baru saja mempelajari **cara mengatur bahasa** untuk fragmen teks individual dalam notebook OneNote menggunakan Aspose.Note untuk Java. Kemampuan ini memungkinkan Anda **membuat dokumen OneNote** secara programatik, **mengubah bahasa teks** secara dinamis, dan **menyimpan file OneNote** dengan metadata pemeriksaan yang akurat.

## Pertanyaan yang Sering Diajukan

**Q: Apakah saya dapat mengatur bahasa pemeriksaan untuk bahasa lain yang tidak disebutkan dalam contoh?**  
A: Tentu saja! Tambahkan pemanggilan `append` tambahan dengan `Locale.forLanguageTag("xx-XX")` yang diinginkan.

**Q: Apakah Aspose.Note untuk Java kompatibel dengan versi Java terbaru?**  
A: Ya, pustaka ini secara rutin diperbarui untuk mendukung rilis Java terbaru.

**Q: Bagaimana saya dapat menangani kesalahan selama proses pengaturan bahasa?**  
A: Bungkus operasi penyimpanan dalam blok `try‑catch` untuk menangkap `IOException` atau `AsposeException`.

**Q: Dapatkah saya mengintegrasikan kode ini ke dalam aplikasi web?**  
A: Tentu. Cukup sertakan JAR Aspose.Note dalam classpath proyek web Anda dan pastikan server memiliki izin menulis ke direktori target.

**Q: Di mana saya dapat menemukan contoh tambahan dan dokumentasi untuk Aspose.Note untuk Java?**  
A: Jelajahi [documentation](https://reference.aspose.com/note/java/) untuk daftar lengkap API dan proyek contoh.

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}