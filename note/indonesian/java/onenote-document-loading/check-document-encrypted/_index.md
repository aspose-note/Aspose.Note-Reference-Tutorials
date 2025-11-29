---
date: 2025-11-29
description: Pelajari cara memeriksa enkripsi OneNote menggunakan Aspose.Note untuk
  Java. Panduan ini menunjukkan cara mendeteksi file OneNote yang terenkripsi sebelum
  diproses.
language: id
linktitle: Check if OneNote Document is Encrypted - Java
second_title: Aspose.Note Java API
title: Periksa Enkripsi OneNote Java – Verifikasi Enkripsi Dokumen OneNote
url: /java/onenote-document-loading/check-document-encrypted/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}  
{{< blocks/products/pf/main-container >}}  
{{< blocks/products/pf/tutorial-page-section >}}  

# Periksa apakah Dokumen OneNote Terenkripsi - Java  

## Pendahuluan  

Saat Anda bekerja dengan file OneNote dalam aplikasi Java, hal pertama yang perlu Anda ketahui adalah **apakah dokumen tersebut terenkripsi**. Mencoba memuat file yang terenkripsi tanpa kata sandi yang tepat akan menyebabkan kesalahan dan mengganggu alur kerja Anda. Dalam tutorial ini kami akan memandu Anda melalui **cara memeriksa enkripsi onenote java** dengan Aspose.Note untuk Java, sehingga Anda dapat dengan aman memutuskan apakah harus meminta kata sandi kepada pengguna atau melanjutkan pemrosesan file.  

## Jawaban Cepat  

- **Metode apa yang menentukan enkripsi?** `Document.isEncrypted`  
- **Apakah saya perlu kata sandi untuk memeriksa?** Tidak, Anda dapat menanyakan status tanpa kata sandi.  
- **Versi API mana yang berfungsi?** Semua rilis terbaru Aspose.Note untuk Java (dicoba dengan 24.11).  
- **Bisakah saya memeriksa aliran dan jalur file?** Ya – API mendukung keduanya.  
- **Apa yang terjadi jika kata sandi salah?** Metode mengembalikan `true`, menandakan file tetap terenkripsi.  

## Apa itu check onenote encryption java?  

`check onenote encryption java` adalah proses memverifikasi secara programatis apakah file OneNote (`.one`) dilindungi dengan kata sandi sebelum mencoba memuat isinya. Mengetahui status enkripsi membantu Anda menghindari pengecualian runtime dan meningkatkan pengalaman pengguna.  

## Mengapa memeriksa enkripsi OneNote sebelum memuat?  

- **Mencegah error runtime** – memuat file terenkripsi tanpa kata sandi akan melempar pengecualian.  
- **Meningkatkan alur UI** – Anda dapat meminta kata sandi kepada pengguna hanya bila diperlukan.  
- **Kepatuhan keamanan** – memastikan Anda menangani konten yang dilindungi sesuai kebijakan.  

## Prasyarat  

1. **Java Development Kit (JDK)** – pastikan Java 11 atau yang lebih baru telah terpasang. Unduh dari [here](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.Note for Java** – dapatkan perpustakaan dari halaman unduhan resmi [here](https://releases.aspose.com/note/java/).  

## Impor Paket  

Untuk memulai, tambahkan impor yang diperlukan ke proyek Java Anda:  

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```  

## Cara memeriksa enkripsi onenote java  

Di bawah ini kami membagi solusi menjadi dua skenario praktis: memeriksa dokumen yang dimuat dari **aliran** dan memeriksa dokumen yang dimuat langsung dari **jalur file**.  

### Langkah 1: Periksa apakah dokumen yang dimuat dari aliran terenkripsi  

```java
public static void CheckIfDocumentFromStreamIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromStreamIsEncrypted
    String dataDir = "Your Document Directory";

    LoadOptions loadOptions = new LoadOptions();
    loadOptions.setDocumentPassword("password");

    FileInputStream stream = new FileInputStream(Paths.get(dataDir, "Sample1.one").toString());

    try {
        Document ref[] = { null };
        if (!Document.isEncrypted(stream, loadOptions, ref)) {
            System.out.println("The document is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Provide a password.");
        }
    } finally {
        stream.close();
    }
    // ExEnd:CheckIfDocumentFromStreamIsEncrypted
}
```  

**Penjelasan**  

- `LoadOptions` memungkinkan Anda secara opsional menyediakan kata sandi (`setDocumentPassword`).  
- `Document.isEncrypted(stream, loadOptions, ref)` memeriksa status enkripsi aliran.  
- Array `ref` menerima referensi ke `Document` yang dimuat ketika file **tidak** terenkripsi, memungkinkan Anda melanjutkan pemrosesan tanpa panggilan muat kedua.  

### Langkah 2: Periksa apakah dokumen yang dimuat dari jalur file terenkripsi  

```java
public static void CheckIfDocumentFromFileIsEncrypted() throws IOException {
    // ExStart:CheckIfDocumentFromFileIsEncrypted
    String dataDir = "Your Document Directory";

    Document ref[] = { null };
    if (!Document.isEncrypted(Paths.get(dataDir, "Sample1.one").toString(), "VerySecretPassword", ref)) {
        if (ref[0] != null) {
            System.out.println("The document is decrypted. It is loaded and ready to be processed.");
        } else {
            System.out.println("The document is encrypted. Invalid password was provided.");
        }
    } else {
        System.out.println("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
    // ExEnd:CheckIfDocumentFromFileIsEncrypted
}
```  

**Penjelasan**  

- Overload ini bekerja langsung dengan jalur file dan string kata sandi.  
- Jika file **tidak** terenkripsi, `isEncrypted` mengembalikan `false` dan referensi `ref[0]` berisi dokumen yang dimuat.  
- Jika kata sandi salah, metode tetap mengembalikan `true`, menandakan file tetap terenkripsi.  

## Jebakan Umum & Tips  

- **Jangan pernah menuliskan kata sandi secara hard‑code** dalam kode produksi; ambil secara aman (misalnya, dari vault).  
- Selalu tutup aliran dalam blok `finally` atau gunakan try‑with‑resources untuk menghindari kebocoran sumber daya.  
- Jika Anda menerima `true` dari `isEncrypted` dan `ref[0]` bernilai `null`, file tersebut either terenkripsi **atau** kata sandi yang diberikan tidak tepat. Minta pengguna memasukkan kata sandi yang benar dan coba lagi.  

## Pertanyaan yang Sering Diajukan  

**T: Bisakah saya memeriksa status enkripsi tanpa menyediakan kata sandi?**  
J: Ya. Panggil `Document.isEncrypted` dengan instance `LoadOptions` yang tidak mengatur kata sandi; metode akan melaporkan apakah file terenkripsi atau tidak.  

**T: Apa yang terjadi jika saya memberikan kata sandi yang salah?**  
J: Metode mengembalikan `true`, menandakan dokumen masih terenkripsi, dan `ref[0]` akan bernilai `null`.  

**T: Apakah ada cara untuk mendekripsi dokumen secara programatis?**  
J: Ya. Setelah Anda mengetahui kata sandi yang benar, berikan ke `LoadOptions` (atau overload yang menerima kata sandi) dan muat dokumen; API akan mendekripsinya secara otomatis.  

**T: Apakah Aspose.Note bekerja dengan format Microsoft lainnya?**  
J: Aspose.Note dirancang khusus untuk file OneNote (`.one`) saja. Untuk format Office lainnya, pertimbangkan Aspose.Words, Aspose.Cells, dll.  

**T: Di mana saya dapat menemukan contoh lebih banyak dan dukungan?**  
J: Kunjungi [Aspose.Note forum](https://forum.aspose.com/c/note/28) untuk bantuan komunitas, dan periksa dokumentasi resmi untuk contoh kode tambahan.  

## Kesimpulan  

Dalam panduan ini kami menunjukkan **cara memeriksa enkripsi onenote java** menggunakan Aspose.Note untuk Java, mencakup skenario berbasis aliran dan berbasis file. Dengan mengintegrasikan pemeriksaan ini ke dalam aplikasi Anda, Anda dapat menangani file OneNote yang terenkripsi secara elegan, meningkatkan pengalaman pengguna, dan menjaga pipeline pemrosesan tetap kuat.  

---  

**Terakhir Diperbarui:** 2025-11-29  
**Dicoba Dengan:** Aspose.Note 24.11 untuk Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}  

{{< /blocks/products/pf/main-container >}}  
{{< /blocks/products/pf/main-wrap-class >}}  

{{< blocks/products/products-backtop-button >}}