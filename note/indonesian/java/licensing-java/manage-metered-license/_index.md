---
title: Kelola Lisensi Terukur untuk OneNote di Java
linktitle: Kelola Lisensi Terukur untuk OneNote di Java
second_title: Aspose.Catatan Java API
description: Pelajari cara mengelola lisensi terukur untuk OneNote di Java menggunakan pustaka Aspose.Note. Kontrol penggunaan, pantau kredit, dan optimalkan biaya secara efisien.
weight: 10
url: /id/java/licensing-java/manage-metered-license/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kelola Lisensi Terukur untuk OneNote di Java

## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara mengelola lisensi terukur untuk OneNote menggunakan Aspose.Note untuk Java. Lisensi terukur memungkinkan Anda memantau dan mengontrol penggunaan berdasarkan kredit, memberikan solusi yang fleksibel dan hemat biaya.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1.  Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda. Anda dapat mengunduhnya dari[Di Sini](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
   
2. Aspose.Note untuk Perpustakaan Java: Anda harus memiliki perpustakaan Aspose.Note untuk Java. Anda dapat mengunduhnya dari[situs web](https://releases.aspose.com/note/java/).

## Paket Impor

Pertama, impor paket yang diperlukan ke proyek Java Anda:

```java
import com.aspose.note.Document;
import com.aspose.note.Metered;



import java.nio.file.Paths;
```

## Langkah 1: Siapkan Lisensi Terukur

```java
Metered metered = new Metered();
metered.setMeteredKey("MyPublicKey", "MyPrivateKey");
```

 Pada langkah ini, kami menginisialisasi`Metered` kelas dan atur kunci terukur dengan kunci publik dan pribadi Anda yang disediakan oleh Aspose.

## Langkah 2: Muat Dokumen dan Lakukan Operasi

```java
String dataDir = "Your Document Directory";
Document doc = new Document(Paths.get(dataDir,"Sample1.one").toString());
doc.save(Paths.get(dataDir,"MeteredLicense.pdf").toString());
```

 Di sini, kami memuat dokumen OneNote dari direktori yang ditentukan dan menyimpannya sebagai file PDF. Pastikan untuk mengganti`"Your Document Directory"` dengan jalur direktori Anda yang sebenarnya.

## Langkah 3: Periksa Konsumsi

```java
System.out.println(String.format("Credit before operation: %.02f", Metered.getConsumptionCredit()));
System.out.println(String.format("Consumption quantity before operation: %.02f", Metered.getConsumptionQuantity()));
```

Langkah ini mengambil dan mencetak jumlah kredit dan konsumsi sebelum dan sesudah operasi.

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara mengelola lisensi terukur untuk OneNote di Java menggunakan pustaka Aspose.Note. Lisensi terukur memberikan fleksibilitas dan kontrol atas penggunaan Anda, memastikan efektivitas biaya dan pengelolaan sumber daya yang efisien.

## FAQ

### Q1: Apa yang dimaksud dengan lisensi terukur?

A1: Lisensi terukur memungkinkan Anda memantau dan mengontrol penggunaan API atau layanan berdasarkan kredit.
   
### Q2: Bagaimana cara mendapatkan kunci terukur untuk produk Aspose?

A2: Anda bisa mendapatkan kunci terukur dengan membeli lisensi dari situs web Aspose atau meminta lisensi sementara untuk tujuan evaluasi.
   
### Q3: Dapatkah saya menggunakan lisensi terukur untuk beberapa aplikasi?

A3: Ya, lisensi terukur dapat digunakan di beberapa aplikasi, namun konsumsinya akan digabungkan.
   
### Q4: Apakah tersedia uji coba gratis untuk Aspose.Note untuk Java?

 A4: Ya, Anda dapat mengunduh uji coba gratis dari[Di Sini](https://releases.aspose.com/).
   
### Q5: Di mana saya bisa mendapatkan dukungan untuk Aspose.Note untuk Java?

 A5: Anda bisa mendapatkan dukungan dari forum komunitas Aspose[Di Sini](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
