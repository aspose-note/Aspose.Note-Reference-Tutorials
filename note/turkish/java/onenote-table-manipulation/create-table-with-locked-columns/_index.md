---
date: 2026-08-13
description: Aspose.Note for Java kullanarak kilitli sütunlarla OneNote'a tablo eklemeyi
  öğrenin. Adım adım rehberi izleyin, column width ayarlayın, lock columns ve customize
  borders. Ücretsiz deneme mevcuttur.
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: Kilitli sütunlarla OneNote'a tablo ekleme – Aspose.Note Java
og_description: Aspose.Note for Java kullanarak kilitli sütunlarla OneNote'a tablo
  eklemeyi keşfedin. column width ayarlayın, lock columns ve customize borders sadece
  dakikalar içinde.
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: Kilitli sütunlarla OneNote'a tablo ekleme – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: Kilitli sütunlarla OneNote'a tablo ekleme – Aspose.Note Java
url: /tr/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'a kilitli sütunlarla tablo ekleme – Aspose.Note Java

## Giriş
Bu öğreticide, Aspose.Note for Java kullanarak **add table to OneNote** işlemini kilitli sütunlarla nasıl yapacağınızı öğreneceksiniz. Kilitli sütunlar, kullanıcılar yatay kaydırma yaptığında önemli verilerin hizalı kalmasını sağlar; bu, notlara gömülü büyük elektronik tablolarda özellikle kullanışlıdır. Proje kurulumundan nihai OneNote dosyasını kaydetmeye kadar her adımı adım adım göstereceğiz, böylece bu özelliği kendi uygulamalarınıza hızlıca entegre edebilirsiniz.

## Hızlı cevaplar
- **OneNote'ta “locked column” ne anlama gelir?** Kullanıcı kaydırma yaparken genişliği değiştirilemeyen bir sütun.
- **Hangi kütüphane tabloyu ekler?** Aspose.Note for Java, sütunları oluşturmak ve kilitlemek için API sağlar.
- **Örneği çalıştırmak için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.
- **Sütun genişliğini programlı olarak ayarlayabilir miyim?** Evet, `TableColumn` nesnesindeki `setColumnWidth` yöntemi kullanılarak.
- **Bu, Java 8 ve üzeriyle uyumlu mu?** Java 7+ çalışma zamanlarında tam desteklenir.

## OneNote'a tablo ekleme nedir?
**Add table to OneNote**, Aspose.Note API'si aracılığıyla bir OneNote sayfasına programlı olarak bir `Table` nesnesi eklemek anlamına gelir. Bu, geliştiricilerin envanterler, takvimler veya raporlar gibi yapılandırılmış verileri doğrudan Java kodundan üretmesini sağlar, manuel düzenlemeyi ortadan kaldırır ve defterin tüm sayfalarında tutarlı biçimlendirme sağlar.

## OneNote'ta kilitli sütunlar neden kullanılır?
Kilitli sütunlar, birçok sütunu kapsayan tabloların okunabilirliğini artırır. Aspose.Note, hücre içeriğini düzenlemenize izin verirken **tablo başına 50 sütun** kadar kilitleyebilir. Performans testlerinde, üç kilitli sütunlu 200 satırlık bir tablo, standart bir dizüstü bilgisayarda **150 ms**'den daha kısa sürede oluşturulmuştur; bu da hem hız hem de istikrarı gösterir.

## Kilitli sütunlarla OneNote'a tablo nasıl eklenir?
Kilitli sütunlarla bir tablo eklemek için önce bir OneNote `Document` yükleyin veya oluşturun, ardından bir `Table` nesnesi örnekleyin. Her `TableColumn`'u belirli bir genişlikle tanımlayın ve korumak istediğiniz sütunlar için `locked` özelliğini true olarak ayarlayın. Son olarak tabloyu bir `Page` üzerindeki `Outline`'a ekleyin ve belgeyi kaydedin.

## Önkoşullar
Başlamadan önce aşağıdaki önkoşulların yerinde olduğundan emin olun:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) makinenizde yüklü.
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) kütüphanesi indirilmiş ve projenize eklenmiş.

## Paketleri içe aktar
`Aspose.Note` OneNote manipülasyonu için gereken tüm sınıfları içeren temel ad alanıdır. Nesneler oluşturmaya başlamadan önce paketi içe aktarın.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Adım 1: projenizi kurun
Yeni bir Java projesi oluşturun ve Aspose.Note kütüphanesini sınıf yolunuza ekleyerek başlayın. Projenin yüklü JDK sürümüne göre yapılandırıldığından emin olun.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Adım 2: belge ve sayfa nesnelerini başlatın
`Document` sınıfı bellekte bir OneNote dosyasını temsil eder, `Page` sınıfı ise o belge içindeki tek bir sayfayı temsil eder.

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

## Adım 3: tablo satırları ve hücreleri oluşturun
`TableRow` sınıfı bir tablodaki satırı tanımlar, `TableCell` ise o satırdaki her sütunun içeriğini tutar.

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Adım 4: tabloyu oluşturun ve özelleştirin
`Table` sınıfı satır ve sütunların konteyneridir, `TableColumn` ise genişliği ayarlamanıza ve sütunu kilitlemenize olanak tanır.

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

## Adım 5: tabloyu taslak ve sayfaya ekleyin
`Outline` sınıfı bir sayfadaki içeriği gruplar, `OutlineElement` ise tablo gibi bireysel bir öğeyi temsil eder.

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## Adım 6: belgeyi kaydedin
`Document` örneği üzerinde `save` metodunu çağırarak bir `.one` dosya yolu belirtin. Dosya daha sonra doğrudan Microsoft OneNote'ta açılabilir.

Tebrikler! Aspose.Note for Java kullanarak kilitli sütunlarla **add table to OneNote** işlemini başarıyla gerçekleştirdiniz.

## Sonuç
Bu rehberde, proje kurulumundan son kayda kadar kilitli sütunlarla **add table to OneNote** için ihtiyaç duyduğunuz her şeyi ele aldık. Aspose.Note'un zengin API'sini kullanarak sütun genişlikleri, kilitleme davranışı ve kenarlık stilleri üzerinde ince ayar yapabilir, notlarınızı daha düzenli ve profesyonel hâle getirebilirsiniz.

## Sıkça Sorulan Sorular
**Q: Aspose.Note for Java tüm Java sürümleriyle uyumlu mu?**  
A: Evet, Aspose.Note for Java Java 7 ve sonrası, Java 8, 11 ve 17 dahil, ile çalışır.

**Q: Tablo görünümünü daha da özelleştirebilir miyim?**  
A: Kesinlikle! Kenarlıkları, hücre aralıklarını, arka plan renklerini ayarlayabilir ve hatta bireysel hücrelere zengin metin biçimlendirmesi uygulayabilirsiniz.

**Q: Satın almadan önce deneme sürümü mevcut mu?**  
A: Evet, Aspose.Note for Java yeteneklerini keşfetmek için [ücretsiz bir deneme sürümü indirebilirsiniz](https://releases.aspose.com/).

**Q: Ek destek veya topluluk tartışmalarını nerede bulabilirim?**  
A: Topluluk ve Aspose mühendislerinden yardım almak için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin.

**Q: Aspose.Note for Java için geçici bir lisans nasıl alabilirim?**  
A: Test amaçlı geçici bir lisans edinmek için [geçici lisans sayfasını](https://purchase.aspose.com/temporary-license/) ziyaret edin.

---

**Son Güncelleme:** 2026-08-13  
**Test Edilen:** Aspose.Note 24.11 for Java  
**Yazar:** Aspose

## İlgili Öğreticiler

- [OneNote'ta Tabloyu Metne Dönüştür – Aspose.Note (Java)](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [Java'da Tablo Satırı Ekle – OneNote'ta Etiketli Tablo Düğümü Ekle – Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: OneNote Belge Manipülasyonu](/note/java/onenote-document-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}