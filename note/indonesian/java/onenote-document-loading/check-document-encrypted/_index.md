---
date: 2026-07-05
description: Pelajari cara memeriksa enkripsi OneNote menggunakan Aspose.Note untuk
  Java. Deteksi file OneNote yang terenkripsi sebelum dimuat untuk menghindari kesalahan
  dan meningkatkan pengalaman pengguna.
keywords:
- check onenote encryption
- Aspose.Note encryption detection
- Java OneNote password check
linktitle: Periksa apakah Dokumen OneNote terenkripsi - Java
second_title: Aspose.Note Java API
title: periksa enkripsi OneNote – Verifikasi Enkripsi Dokumen OneNote dengan Java
url: /id/java/onenote-document-loading/check-document-encrypted/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}  
{{< blocks/products/pf/main-container >}}  
{{< blocks/products/pf/tutorial-page-section >}}  

# Periksa apakah Dokumen OneNote Terenkripsi – Java  

## Pendahuluan  

Ketika Anda bekerja dengan file OneNote dalam aplikasi Java, hal pertama yang perlu Anda ketahui adalah **apakah dokumen tersebut terenkripsi**. Mencoba memuat file yang terenkripsi tanpa kata sandi yang tepat akan menyebabkan pengecualian dan mengganggu alur kerja Anda. Dalam tutorial ini kami akan memandu Anda melalui **cara memeriksa enkripsi onenote** dengan Aspose.Note untuk Java, sehingga Anda dapat dengan aman memutuskan apakah akan meminta kata sandi kepada pengguna atau melanjutkan pemrosesan file.  

## Jawaban Cepat  

- **Metode apa yang menentukan enkripsi?** `Document.isEncrypted`  
- **Apakah saya memerlukan kata sandi untuk memeriksa?** Tidak, Anda dapat menanyakan status tanpa kata sandi.  
- **Versi API mana yang berfungsi?** Rilis terbaru Aspose.Note untuk Java (diuji dengan 26.4).  
- **Bisakah saya memeriksa baik aliran (stream) maupun jalur file?** Ya – API mendukung keduanya.  
- **Apa yang terjadi jika kata sandi salah?** Metode mengembalikan `true`, menunjukkan file tetap terenkripsi.  

## Apa itu pemeriksaan enkripsi onenote?  

Memeriksa enkripsi onenote berarti secara programatik menentukan apakah file OneNote (`.one`) dilindungi dengan kata sandi sebelum ada upaya membaca isinya. Pemeriksaan status cepat ini mencegah pengecualian runtime, memungkinkan Anda meminta kata sandi kepada pengguna hanya bila diperlukan, dan membantu Anda tetap mematuhi kebijakan keamanan.  

## Mengapa memeriksa enkripsi OneNote sebelum memuat?  

Memuat file OneNote yang terenkripsi tanpa menyediakan kata sandi yang benar memicu pengecualian yang dapat menghentikan layanan Anda atau menampilkan kesalahan yang membingungkan bagi pengguna. Dengan memeriksa flag enkripsi terlebih dahulu, Anda dapat menampilkan prompt kata sandi hanya bila diperlukan, mengurangi I/O yang tidak perlu, dan memastikan konten yang dilindungi ditangani sesuai aturan tata kelola perusahaan.  

## Prasyarat  

1. **Java Development Kit (JDK)** – Java 11 atau lebih baru diperlukan. Unduh dari [di sini](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.Note for Java** – dapatkan perpustakaan dari halaman unduhan resmi [di sini](https://releases.aspose.com/note/java/).  

## Impor Paket  

Kelas `Document` mewakili file OneNote dan menyediakan metode untuk memuat serta memeriksa isinya.  

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```  

```java
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
```  

## Bagaimana cara memeriksa status enkripsi untuk dokumen yang dimuat dari aliran (stream)?  

`Document.isEncrypted` adalah metode statis yang mengembalikan nilai boolean yang menunjukkan apakah file OneNote terenkripsi. Muat aliran OneNote gaya PDF Anda dan panggil metode statis `Document.isEncrypted`. Metode ini mengembalikan nilai boolean yang menandakan enkripsi dan, ketika file tidak terenkripsi, mengisi array referensi dengan instance `Document` yang dimuat sehingga Anda tidak memerlukan panggilan muat kedua.  

**Jawaban langsung (40‑70 kata):**  
Panggil `Document.isEncrypted(inputStream, loadOptions, ref)` – metode ini langsung memberi tahu Anda apakah aliran dilindungi kata sandi. Jika hasilnya `false`, `ref[0]` berisi objek `Document` yang siap pakai, memungkinkan Anda melanjutkan pemrosesan tanpa I/O tambahan. Jika hasilnya `true`, aliran tersebut terenkripsi dan Anda harus meminta kata sandi sebelum melanjutkan.  

**Penjelasan**  

- `LoadOptions` memungkinkan Anda secara opsional menyediakan kata sandi (`setDocumentPassword`).  
- `Document.isEncrypted(stream, loadOptions, ref)` memeriksa status enkripsi aliran.  
- Array `ref` menerima referensi ke `Document` yang dimuat ketika file **tidak** terenkripsi, memungkinkan Anda melanjutkan pemrosesan tanpa panggilan muat kedua.  

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

## Bagaimana cara memeriksa status enkripsi untuk dokumen yang dimuat dari jalur file?  

`Document.isEncrypted` juga menyediakan overload yang bekerja langsung dengan jalur file dan string kata sandi. Overload ini mengikuti pola pengembalian boolean yang sama, mengisi array referensi hanya ketika file tidak terenkripsi.  

**Jawaban langsung (40‑70 kata):**  
Panggil `Document.isEncrypted(filePath, password, ref)` – pemanggilan ini mengembalikan `true` jika file terenkripsi (atau kata sandi salah) dan `false` sebaliknya. Ketika `false`, `ref[0]` berisi `Document` yang sepenuhnya dimuat dan siap untuk dimanipulasi. Pendekatan ini menghindari langkah muat terpisah dan membuat kode Anda ringkas.  

**Penjelasan**  

- Overload ini bekerja langsung dengan jalur file dan string kata sandi.  
- Jika file **tidak** terenkripsi, `isEncrypted` mengembalikan `false` dan referensi `ref[0]` berisi dokumen yang dimuat.  
- Jika kata sandi salah, metode tetap mengembalikan `true`, menunjukkan file tetap terenkripsi.  

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

## Kesalahan Umum & Tips  

- **Jangan pernah menuliskan kata sandi secara hard‑code** dalam kode produksi; ambil secara aman (mis., dari vault).  
- Selalu tutup aliran dalam blok `finally` atau gunakan try‑with‑resources untuk menghindari kebocoran sumber daya.  
- Jika Anda menerima `true` dari `isEncrypted` dan `ref[0]` bernilai `null`, file tersebut enten terenkripsi **atau** kata sandi yang diberikan tidak benar. Minta pengguna memasukkan kata sandi yang benar dan coba lagi.  

## Pertanyaan yang Sering Diajukan  

**Q: Bisakah saya memeriksa status enkripsi tanpa menyediakan kata sandi?**  
A: Ya. Panggil `Document.isEncrypted` dengan instance `LoadOptions` yang tidak menetapkan kata sandi; metode tersebut akan melaporkan apakah file terenkripsi.  

**Q: Apa yang terjadi jika saya memberikan kata sandi yang salah?**  
A: Metode mengembalikan `true`, menunjukkan dokumen masih terenkripsi, dan `ref[0]` akan menjadi `null`.  

**Q: Apakah ada cara untuk mendekripsi dokumen secara programatik?**  
A: Ya. Setelah Anda mengetahui kata sandi yang benar, berikan ke `LoadOptions` (atau overload yang menerima kata sandi) dan muat dokumen; API akan mendekripsinya secara otomatis.  

**Q: Apakah Aspose.Note bekerja dengan format Microsoft lainnya?**  
A: Aspose.Note dibuat khusus untuk file OneNote (`.one`) saja. Untuk Word, Excel, PowerPoint, dll., pertimbangkan Aspose.Words, Aspose.Cells, Aspose.Slides masing‑masing.  

**Q: Di mana saya dapat menemukan contoh dan dukungan lebih lanjut?**  
A: Kunjungi [forum Aspose.Note](https://forum.aspose.com/c/note/28) untuk bantuan komunitas, dan periksa dokumentasi resmi untuk contoh kode tambahan.  

## Kesimpulan  

Dalam panduan ini kami menunjukkan **cara memeriksa enkripsi onenote** menggunakan Aspose.Note untuk Java, mencakup skenario berbasis aliran maupun berbasis file. Dengan mengintegrasikan pemeriksaan ini ke dalam aplikasi Anda, Anda dapat menangani file OneNote yang terenkripsi secara elegan, meningkatkan pengalaman pengguna, dan menjaga pipeline pemrosesan Anda tetap kuat.  

---  

**Terakhir Diperbarui:** 2026-07-05  
**Diuji Dengan:** Aspose.Note 26.4 for Java  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Buat Dokumen OneNote – Muat Notebook dengan Aspose.Note](/note/java/onenote-notebook-operations/loading-notebook/)
- [Lindungi onenote dengan kata sandi menggunakan Aspose.Note untuk Java](/note/java/onenote-notebook-operations/write-password-protected-document/)
- [Dapatkan Info Format File Aspose Note dari OneNote menggunakan Java](/note/java/onenote-document-loading/get-file-format-info/)


{{< /blocks/products/pf/tutorial-page-section >}}  
{{< /blocks/products/pf/main-container >}}  
{{< /blocks/products/pf/main-wrap-class >}}