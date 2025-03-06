---
title: Terapkan Tema Gelap ke Teks di OneNote - Aspose.Note
linktitle: Terapkan Tema Gelap ke Teks di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Jelajahi langkah mudah untuk menerapkan tema gelap ke teks OneNote Anda menggunakan Aspose.Note untuk Java. Tingkatkan pengalaman dokumentasi digital Anda dengan mudah.
weight: 11
url: /id/java/onenote-text-manipulation/apply-dark-theme/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Terapkan Tema Gelap ke Teks di OneNote - Aspose.Note

## Perkenalan
Dalam lanskap dokumentasi digital yang terus berkembang, estetika catatan Anda dapat berdampak signifikan terhadap keterbacaan dan pengalaman pengguna. Salah satu aspek penting adalah penerapan tema gelap, yang menyediakan lingkungan yang menarik dan nyaman secara visual. Dalam tutorial ini, kami akan memandu Anda melalui proses penerapan tema gelap pada teks di OneNote menggunakan Aspose.Note untuk Java.
## Prasyarat
Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:
-  Aspose.Note untuk Java: Unduh dan instal perpustakaan Aspose.Note untuk Java dari[Di Sini](https://releases.aspose.com/note/java/).
- Java Development Kit (JDK): Pastikan Anda telah menginstal Java di mesin Anda.
- Lingkungan Pengembangan Terintegrasi (IDE): Pilih IDE seperti Eclipse atau IntelliJ untuk pengembangan yang lancar.
## Paket Impor
Untuk memulai, impor paket yang diperlukan ke proyek Java Anda:
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
```
## Langkah 1: Atur Warna Latar Belakang Halaman
```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory";
// Muat dokumen ke Aspose.Note.
Document doc = new Document(Paths.get(dataDir, "Aspose.one").toString());
for (Page page: doc)
{
    page.setBackgroundColor(Color.BLACK);
}
```
## Langkah 2: Sesuaikan Warna Teks
```java
for (RichText node: doc.getChildNodes(RichText.class))
{
    Color c = node.getParagraphStyle().getFontColor();
    if (c.getAlpha() <= 10 || Math.abs(c.getRed() - Color.BLACK.getRed()) + Math.abs(c.getGreen() - Color.BLACK.getGreen()) + Math.abs(c.getBlue() - Color.BLACK.getBlue()) <= 30)
    {
        node.getParagraphStyle().setFontColor(Color.WHITE);
    }
}
```
## Langkah 3: Simpan Dokumen
```java
doc.save(Paths.get(dataDir, "AsposeDarkTheme.pdf").toString());
```
Ulangi langkah-langkah ini untuk setiap dokumen, dan Anda akan berhasil menerapkan tema gelap ke teks OneNote Anda menggunakan Aspose.Note untuk Java.
## Kesimpulan
Kesimpulannya, meningkatkan daya tarik visual catatan digital Anda sangatlah mudah dengan Aspose.Note untuk Java. Dengan mengikuti panduan langkah demi langkah ini, Anda dapat dengan mudah menerapkan tema gelap pada teks di OneNote, sehingga meningkatkan pengalaman dokumentasi Anda.
## FAQ
### Bisakah saya menerapkan tema gelap hanya pada bagian tertentu?
Ya, Anda dapat memodifikasi kode untuk menerapkan tema gelap secara selektif ke bagian tertentu dalam dokumen Anda.
### Apakah ada tema gelap standar yang tersedia di Aspose.Note untuk Java?
Saat ini, Aspose.Note untuk Java memungkinkan Anda menyesuaikan tema, tetapi tidak ada tema gelap yang telah ditentukan sebelumnya.
### Apakah Aspose.Note untuk Java mendukung format dokumen lain?
Ya, Aspose.Note untuk Java mendukung berbagai format dokumen, termasuk PDF, DOCX, dan HTML.
### Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?
 Ya, Anda dapat mengakses versi uji coba gratis[Di Sini](https://releases.aspose.com/).
### Bagaimana saya bisa mendapatkan dukungan untuk Aspose.Note untuk Java?
 Mengunjungi[Aspose.Catatan forum](https://forum.aspose.com/c/note/28) untuk dukungan komunitas atau jelajahi opsi dukungan premium[Di Sini](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
