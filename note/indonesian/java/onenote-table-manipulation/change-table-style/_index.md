---
title: Ubah Gaya Tabel di OneNote - Aspose.Note
linktitle: Ubah Gaya Tabel di OneNote - Aspose.Note
second_title: Aspose.Catatan Java API
description: Sempurnakan tabel OneNote Anda dengan mudah dengan Aspose.Note untuk Java. Ikuti panduan langkah demi langkah kami untuk mengubah gaya tabel. Unduh perpustakaannya sekarang!
type: docs
weight: 10
url: /id/java/onenote-table-manipulation/change-table-style/
---
## Perkenalan
Aspose.Note untuk Java adalah perpustakaan canggih yang memungkinkan pengembang memanipulasi file OneNote dengan mudah. Dalam tutorial ini, kita akan fokus mengubah gaya tabel di dokumen OneNote menggunakan Aspose.Note untuk Java. Ikuti panduan langkah demi langkah untuk meningkatkan daya tarik visual tabel Anda.
## Prasyarat
Sebelum memulai, pastikan Anda memiliki hal berikut:
- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.
-  Aspose.Note untuk Perpustakaan Java: Unduh dan instal perpustakaan Aspose.Note untuk Java dari[Unduh Halaman](https://releases.aspose.com/note/java/).
- Direktori Dokumen: Siapkan direktori untuk menyimpan dokumen OneNote Anda.
## Paket Impor
Di proyek Java Anda, impor paket yang diperlukan untuk bekerja dengan Aspose.Catatan:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## Langkah 1: Siapkan Dokumen
Muat dokumen OneNote ke Aspose.Note dan ambil daftar node tabel
```java
// Siapkan dokumen dan dapatkan daftar node tabel
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## Langkah 2: Tetapkan Gaya Baris
Ulangi setiap tabel, atur gaya untuk setiap baris, termasuk menyorot baris pertama setelah header.

```java
// Tetapkan gaya baris untuk setiap tabel dalam dokumen
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Sorot baris pertama setelah kepala.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## Metode setRowStyle
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```
## Langkah 3: Simpan Dokumen
Simpan dokumen yang dimodifikasi dengan gaya tabel baru.
Dengan mengikuti langkah-langkah ini, Anda bisa dengan mudah mengubah gaya tabel di dokumen OneNote menggunakan Aspose.Note untuk Java.

```java
// Simpan dokumen yang diubah
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## Kesimpulan
Aspose.Note untuk Java menyederhanakan proses manipulasi file OneNote. Dengan memanfaatkan kemampuan perpustakaan, Anda dapat meningkatkan presentasi visual tabel Anda dengan mudah.

## FAQ
### Di mana saya dapat menemukan dokumentasi Aspose.Note untuk Java?
 Mengunjungi[dokumentasi](https://reference.aspose.com/note/java/) untuk panduan komprehensif.
### Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Note untuk Java?
 Ikuti ini[tautan](https://purchase.aspose.com/temporary-license/) untuk memperoleh izin sementara.
### Apakah ada uji coba gratis yang tersedia untuk Aspose.Note untuk Java?
 Ya, Anda dapat mengunduh versi uji coba gratis dari[Di Sini](https://releases.aspose.com/).
### Di mana saya bisa mendapatkan dukungan untuk Aspose.Note untuk Java?
 Bergabunglah dengan[Aspose.Catatan forum](https://forum.aspose.com/c/note/28) untuk mencari bantuan dari masyarakat.
### Bagaimana cara membeli Aspose.Note untuk Java?
 Anda dapat membeli perpustakaan[Di Sini](https://purchase.aspose.com/buy).