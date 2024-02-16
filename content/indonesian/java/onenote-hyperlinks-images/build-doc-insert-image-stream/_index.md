---
title: Buat Dokumen dan Sisipkan Gambar dengan Stream di OneNote - Java
linktitle: Buat Dokumen dan Sisipkan Gambar dengan Stream di OneNote - Java
second_title: Aspose.Catatan Java API
description: Pelajari cara mengintegrasikan gambar dengan mudah ke dalam dokumen OneNote menggunakan Aspose.Note untuk Java. Tutorial langkah demi langkah untuk pengembang Java.
type: docs
weight: 13
url: /id/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---
## Perkenalan

Selamat datang di tutorial komprehensif kami tentang penggunaan Aspose.Note untuk Java untuk membuat dokumen dan menyisipkan gambar menggunakan aliran gambar di OneNote! Dalam tutorial ini, kami akan memandu Anda melalui proses langkah demi langkah, memastikan Anda memiliki pemahaman yang jelas tentang setiap tahap. Pada akhirnya, Anda akan dapat dengan mudah mengintegrasikan gambar ke dalam dokumen OneNote Anda menggunakan Java.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

### Kit Pengembangan Java (JDK)

Pastikan Anda telah menginstal Java Development Kit (JDK) di sistem Anda. Anda dapat mengunduhnya dari situs web Oracle.

### Aspose.Catatan untuk Perpustakaan Java

 Unduh dan instal perpustakaan Aspose.Note untuk Java dari yang disediakan[tautan](https://releases.aspose.com/note/java/).

### Pengaturan IDE

Siapkan Lingkungan Pengembangan Terpadu (IDE) Anda dengan konfigurasi yang diperlukan untuk bekerja dengan proyek Java.

## Paket Impor

Untuk memulai, impor paket yang diperlukan ke proyek Java Anda. Paket-paket ini akan menyediakan fungsionalitas yang diperlukan untuk bekerja dengan dokumen dan gambar OneNote.

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

## Langkah 1: Siapkan Direktori Dokumen

 Tentukan direktori tempat dokumen dan gambar Anda berada. Mengganti`"Your Document Directory"` dengan jalur ke direktori Anda.

```java
String dataDir = "Your Document Directory";
```

## Langkah 2: Buat Objek Dokumen

 Inisialisasi sebuah instance dari`Document` kelas untuk mulai bekerja dengan dokumen OneNote Anda.

```java
Document doc = new Document();
```

## Langkah 3: Inisialisasi Objek Halaman

 Membuat`Page` objek untuk mewakili halaman dalam dokumen.

```java
Page page = new Page();
```

## Langkah 4: Buat Garis Besar

 Inisialisasi sebuah`Outline` objek untuk menyusun konten di dalam halaman.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Langkah 5: Buat Elemen Garis Besar

 Buat sebuah`OutlineElement` untuk menahan gambar dan menentukan posisinya.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Langkah 6: Muat Aliran Gambar

 Muat aliran gambar menggunakan`FileInputStream` untuk gambar yang diinginkan.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Langkah 7: Sisipkan Gambar

 Masukkan gambar ke dalam dokumen dengan membuat`Image` objek dan mengatur perataannya.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Langkah 8: Tambahkan Gambar ke Elemen Garis Besar

Tambahkan gambar ke elemen kerangka.

```java
outlineElem1.appendChildLast(image);
```

## Langkah 9: Tambahkan Elemen Garis Besar ke Garis Besar

Tambahkan elemen kerangka ke kerangka.

```java
outline1.appendChildLast(outlineElem1);
```

## Langkah 10: Tambahkan Garis Besar ke Halaman

Tambahkan kerangka ke halaman.

```java
page.appendChildLast(outline1);
```

## Langkah 11: Tambahkan Halaman ke Dokumen

Terakhir, tambahkan halaman tersebut ke dokumen.

```java
doc.appendChildLast(page);
```

## Langkah 12: Simpan Dokumen

Simpan dokumen yang dimodifikasi, tentukan format yang diinginkan (misalnya PDF).

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Dengan mengikuti langkah-langkah ini, Anda dapat dengan mudah membuat dokumen dan menyisipkan gambar menggunakan aliran gambar di OneNote menggunakan Aspose.Note untuk Java.

## Kesimpulan

Kesimpulannya, menguasai integrasi gambar ke dalam dokumen OneNote Anda menggunakan Java dapat meningkatkan proses pembuatan dokumen Anda secara signifikan. Dengan Aspose.Note untuk Java, Anda memiliki alat canggih yang dapat Anda gunakan untuk menyelesaikan tugas ini dengan lancar.

## FAQ

### Q1: Apakah Aspose.Note untuk Java kompatibel dengan semua versi OneNote?

A1: Aspose.Note untuk Java mendukung berbagai versi OneNote, memastikan kompatibilitas di berbagai lingkungan.

### Q2: Dapatkah saya mengkustomisasi tampilan gambar yang disisipkan dalam dokumen OneNote menggunakan Aspose.Note untuk Java?

A2: Ya, Anda dapat menyesuaikan berbagai aspek gambar yang disisipkan, seperti perataan, ukuran, dan orientasi, agar sesuai dengan kebutuhan spesifik Anda.

### Q3: Apakah Aspose.Note untuk Java menyediakan dukungan untuk format dokumen lain selain PDF?

A3: Ya, Aspose.Note untuk Java mendukung berbagai format dokumen, termasuk DOCX, HTML, dan lainnya, memberi Anda fleksibilitas dalam tugas manajemen dokumen Anda.

### Q4: Di mana saya dapat menemukan sumber daya tambahan dan dukungan untuk Aspose.Note untuk Java?

A4: Anda dapat mengakses dokumentasi, tautan unduhan, forum dukungan, dan lisensi sementara Aspose.Note untuk Java melalui tautan yang disediakan.

### Q5: Apakah ada versi uji coba yang tersedia untuk Aspose.Note untuk Java?

A5: Ya, Anda bisa mendapatkan uji coba gratis Aspose.Note untuk Java guna menjelajahi fitur dan kemampuannya sebelum membuat keputusan pembelian.
