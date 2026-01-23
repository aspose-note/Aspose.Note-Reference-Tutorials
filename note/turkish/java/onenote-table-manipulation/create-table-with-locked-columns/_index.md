---
date: 2026-01-23
description: Aspose.Note for Java kullanarak OneNote’a bir tablo eklerken sütun genişliğini
  nasıl kilitleyeceğinizi öğrenin. Kod, ipuçları ve SSS içeren adım adım rehber.
linktitle: How to Lock Column in OneNote Table – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote Tablosunda Sütunu Kilitleme – Aspose.Note
url: /tr/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Tablosunda Sütunu Kilitleme – Aspose.Note

## Introduction
OneNote, çok yönlü bir not alma platformudur ve Aspose.Note for Java, OneNote'a bir tablo eklerken **sütun kilitleme** genişliğini kolaylaştırır. Bu öğreticide, tablo sütun genişliğini nasıl ayarlayacağınızı, bu genişliği nasıl kilitleyeceğinizi ve OneNote tablo kenarlıklarını nasıl özelleştireceğinizi gösteren eksiksiz, uygulamalı bir örnek göreceksiniz — sadece birkaç satır Java kodu ile.

## Quick Answers
- **“lock column” ne anlama geliyor?** Sütun genişliğini sabitler, böylece kullanıcı OneNote'ta yeniden boyutlandıramaz.  
- **Bu özelliği hangi kütüphane sağlar?** Aspose.Note for Java.  
- **Örneği çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **Sütunu kilitledikten sonra daha fazla satır ekleyebilir miyim?** Evet, satır eklemeye devam edebilirsiniz; kilitli genişlik uygulanmaya devam eder.  
- **Hangi Java sürümü destekleniyor?** Java 6 ve üzeri.

## What is “how to lock column” in a OneNote table?
OneNote tablosunda “sütunu kilitleme” nedir?
Bir sütunu kilitlemek, bir `TableColumn` nesnesine sabit bir genişlik atamak ve `LockedWidth` özelliğini `true` olarak ayarlamak anlamına gelir. Bu, son kullanıcıların yanlışlıkla yeniden boyutlandırmasını önler ve düzeninizin tutarlı kalmasını sağlar.

## Why lock column width in OneNote?
- **Tutarlı düzen** – Notlarınız her cihazda aynı görünür.  
- **Daha iyi okunabilirlik** – Uzun metin, tahmin edilebilir bir sütun boyutunda satır sonuna girer.  
- **Profesyonel görünüm** – Kilitli sütunlar, cilalı ve rapor benzeri bir his verir.

## Prerequisites
Başlamadan önce, aşağıdakilerin hazır olduğundan emin olun:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) makinenize kurulu.  
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) kütüphanesini indirin ve projenizin sınıf yoluna ekleyin.

## Import Packages
Java projenizde, Aspose.Note ile çalışmak için gerekli paketleri içe aktarın:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Step 1: Set Up Your Project
Yeni bir Java projesi oluşturun (veya mevcut bir projeyi kullanın) ve Aspose.Note JAR dosyalarını derleme yoluna ekleyin. Projenin, kurduğunuz JDK ile derlendiğinden emin olun.

## Step 2: Initialize Document and Page Objects
Tablonun yer alacağı yeni bir `Document` ve bir `Page` oluşturarak başlıyoruz.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Step 3: Create Table Rows and Cells
Burada iki satır oluşturuyoruz, her biri örnek metin içeren tek bir hücreye sahip. Bu, kilitli sütunun kısa ve uzun içerikle nasıl davrandığını gösterir.

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Step 4: Create and Customize the Table
Şimdi tabloyu oluşturuyor, **tablo sütun genişliğini ayarlıyor**, **sütunu kilitliyor** ve **OneNote tablo kenarlıklarını özelleştiriyoruz**.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);               // customize onenote table borders
TableColumn col = new TableColumn();
col.setWidth(200);                           // set table column width
col.setLockedWidth(true);                    // onenote table locked width
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Step 5: Add Table to Outline and Page
Şimdi tabloyu bir `OutlineElement`'e ekliyoruz ve sonunda sayfaya ekliyoruz — bu **add outline element java** adımıdır.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Step 6: Save the Document
OneNote dosyasını (`.one`) daha önce belirttiğiniz dizine kaydedin.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

T|------- kenarlıkları olmadan görünüyor | `tableendikten sonra sütun genişliği değişiyor | `col.setLockedWidth(true);` değerinin satırlar eklenmeden **önce** ayarlandığını doğrulayın. |
| Dosya kaydedilmiyor | `dataDir`'in yazılabilir bir klasöre işaret ettiğini ve geçerli bir dosya edin. |

## Frequently Asked Questions

**S: Aspose.Note for Java tüm Java sürümleriyle uyumlu mu?**  
C: Evet, Java 6 ve üzeri, Java 11 ve Java 17 dahil olmak üzere çalışır.

**S: Tablo görünümünü daha da özelleştirebilir miyim?**  
C: Kesinlikle! `Table` ve `TableCell` özellikleri aracılığıyla kenar stili, hücre dolgusu, arka plan renkleri ve daha fazlasını değiştirebilirsiniz.

**S: Satın almadan önce deneme sürümü mevcut mu?**  
C: Evet, Aspose.Note for Java özelliklerini keşfetmek için [ücretsiz bir deneme indirebilir](https://releases.aspose.com/).

**S: Ek destek veya topluluk tartışmalarını nerede bulabilirim?**  
C: Destek ve topluluk tartışmaları için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin.

**S: Aspose.Note for Java için geçici bir lisans nasıl alabilirim?**  
C: Test amaçlı geçici bir lisans edinmek için [bu bağlantıyı](https://purchase.aspose.com/temporary-license/) ziyaret edin.

---

**Son Güncelleme:** 2026-01-23  
**Test Edilen:** Aspose.Note for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}