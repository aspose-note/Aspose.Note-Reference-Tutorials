---
title: OneNote'ta Kilitli Sütunlu Tablo Oluşturma - Aspose.Note
linktitle: OneNote'ta Kilitli Sütunlu Tablo Oluşturma - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java ile OneNote deneyiminizi geliştirin. Adım adım kılavuzu kullanarak kilitli sütunlara sahip tablolar oluşturmayı öğrenin. Şimdi ücretsiz deneme sürümünü indirin!
type: docs
weight: 12
url: /tr/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## giriiş
OneNote, bilgileri düzenlemek için güçlü bir araçtır ve Aspose.Note for Java, kilitli sütunlara sahip tablolar oluşturmanın kusursuz bir yolunu sağlayarak yeteneklerini geliştirir. Bu eğitimde, OneNote'ta kilitli sütunlara sahip bir tablo oluşturmak için Aspose.Note for Java'yı kullanma sürecinde size rehberlik edeceğiz.
## Önkoşullar
Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
- [Java Geliştirme Kiti (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)makinenize kurulu.
- [Java için Aspose.Note](https://downloads.aspose.com/note/java) kütüphane indirildi ve projenize eklendi.
## Paketleri İçe Aktar
Aspose.Note ile çalışmak için gerekli paketleri Java projenize aktarın:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## 1. Adım: Projenizi Kurun
Yeni bir Java projesi oluşturarak ve Aspose.Note kütüphanesini sınıf yolunuza ekleyerek başlayın. Projenizin JDK'yı kullanacak şekilde yapılandırıldığından emin olun.
## Adım 2: Belge ve Sayfa Nesnelerini Başlatın
```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";
//Document sınıfının bir nesnesini oluşturun
Document doc = new Document();
// Sayfa sınıfı nesnesini başlat
Page page = new Page();
```
## Adım 3: Tablo Satırları ve Hücreleri Oluşturun
```java
// TableRow sınıfı nesnesini başlat
TableRow row1 = new TableRow();
// TableCell sınıfı nesnesini başlatın ve metin içeriğini ayarlayın
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// TableRow sınıfı nesnesini başlat
TableRow row2 = new TableRow();
// TableCell sınıfı nesnesini başlatın ve metin içeriğini ayarlayın
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Adım 4: Tabloyu Oluşturun ve Özelleştirin
```java
// Tablo sınıfı nesnesini başlat
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Satır ekle
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Adım 5: Anahat ve Sayfaya Tablo Ekleme
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Tablo düğümü ekle
outlineElem.appendChildLast(table);
// Anahat öğesi düğümü ekle
outline.appendChildLast(outlineElem);
// Anahat düğümü ekle
page.appendChildLast(outline);
// Sayfa düğümü ekle
doc.appendChildLast(page);
```
## Adım 6: Belgeyi Kaydedin
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Tebrikler! Aspose.Note for Java'yı kullanarak OneNote'ta kilitli sütunlara sahip bir tabloyu başarıyla oluşturdunuz.
## Çözüm
Bu eğitimde, kilitli sütunlara sahip tablolar oluşturarak OneNote deneyiminizi geliştirmek için Aspose.Note for Java'yı kullanma sürecini araştırdık. Bu işlevsellik, notlarınıza yeni bir düzenleme ve yapı katmanı ekler.
## SSS
### Aspose.Note for Java tüm Java sürümleriyle uyumlu mu?
Evet, Aspose.Note for Java, Java 6 ve sonraki sürümlerle uyumludur.
### Tablonun görünümünü daha da özelleştirebilir miyim?
Kesinlikle! Aspose.Note for Java, tabloları özelleştirmek için kenarlıkları ayarlama, hücre aralığını ayarlama ve daha fazlası gibi kapsamlı seçenekler sunar.
### Satın almadan önce deneme sürümü mevcut mu?
 Evet yapabilirsin[ücretsiz deneme sürümünü indirin](https://releases.aspose.com/) Aspose.Note for Java'nın yeteneklerini keşfetmek için.
### Ek desteği veya topluluk tartışmalarını nerede bulabilirim?
 Ziyaret edin[Aspose.Note forumu](https://forum.aspose.com/c/note/28) destek ve topluluk tartışmaları için.
### Aspose.Note for Java için nasıl geçici lisans edinebilirim?
 Ziyaret etmek[bu bağlantı](https://purchase.aspose.com/temporary-license/) Test amacıyla geçici bir lisans almak için.