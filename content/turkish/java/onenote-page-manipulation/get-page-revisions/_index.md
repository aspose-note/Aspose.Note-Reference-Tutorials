---
title: OneNote'ta Sayfa Revizyonlarını Alın - Aspose.Note
linktitle: OneNote'ta Sayfa Revizyonlarını Alın - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote'ta sayfa revizyonlarını nasıl alacağınızı öğrenin. Değişikliklerin verimli takibi için adım adım kılavuzumuzu izleyin.
type: docs
weight: 14
url: /tr/java/onenote-page-manipulation/get-page-revisions/
---
## giriiş

OneNote, notlarınızı düzenlemek ve yönetmek için güçlü bir araçtır ancak bazen sayfalarınızda yapılan değişiklikleri ve düzeltmeleri izlemeniz gerekir. Aspose.Note for Java ile sayfa revizyonlarını programlı olarak kolayca alabilirsiniz. Bu eğitimde, Aspose.Note for Java'yı kullanarak OneNote'ta sayfa revizyonları alma sürecinde size rehberlik edeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

### 1. Java Geliştirme Kiti (JDK)

Sisteminizde Java Development Kit'in (JDK) kurulu olduğundan emin olun. JDK'yı Oracle web sitesinden indirip yükleyebilirsiniz.

### 2. Java için Aspose.Note

Aspose.Note for Java'yı şu adresten indirip yükleyin:[İndirme: {link](https://releases.aspose.com/note/java/).

### 3. Örnek OneNote Belgesi

Örnek bir OneNote belgesi hazırlayın (`Sample1.one`) revizyonları almak istediğiniz sayfaları içeren.

## Paketleri İçe Aktar

Öncelikle gerekli paketleri Aspose.Note for Java'dan içe aktarmanız gerekiyor.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Şimdi verilen örneği birden çok adıma ayıralım:

## 1. Adım: Belge Dizinini Ayarlayın

OneNote belgenizin bulunduğu dizin yolunu tanımlayın.

```java
String dataDir = "Your Document Directory";
```

## 2. Adım: OneNote Belgesini Yükleyin

 OneNote belgesini şunu kullanarak yükleyin:`LoadOptions` yükleme geçmişini etkinleştirmek için.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## 3. Adım: İlk Sayfayı Alın

Yüklenen belgenin ilk sayfasını alın.

```java
Page firstPage = document.getFirstChild();
```

## Adım 4: Sayfa Revizyonlarını Yineleyin

Her sayfa revizyonunu yineleyin ve son değiştirilme zamanı, oluşturulma zamanı, başlık, seviye ve yazar gibi ilgili bilgileri alın.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Çözüm

Bu eğitimde Aspose.Note for Java'yı kullanarak OneNote'ta sayfa revizyonlarının nasıl alınacağını öğrendik. Bu adımları izleyerek OneNote sayfalarınızda yapılan değişiklikleri programlı bir şekilde etkili bir şekilde izleyebilirsiniz.

## SSS'ler

### S1: Sayfa revizyonlarını değiştirmek için Aspose.Note for Java'yı kullanabilir miyim?

Cevap1: Hayır, Aspose.Note for Java şu anda sayfa revizyonlarının alınmasını desteklemektedir ancak bunların değiştirilmesini desteklememektedir.

### S2: Aspose.Note for Java, OneNote belgelerinin farklı sürümleriyle uyumlu mudur?

C2: Evet, Aspose.Note for Java, OneNote belgelerinin çeşitli sürümlerini destekleyerek farklı dosya formatlarıyla sorunsuz bir şekilde çalışmanıza olanak tanır.

### S3: Aspose.Note for Java'yı kullanmak için lisans gerekiyor mu?

Cevap3: Evet, Aspose.Note for Java'yı ticari projelerde kullanmak için lisans satın almanız gerekiyor. Ancak değerlendirme amacıyla geçici bir lisans da alabilirsiniz.

### S4: Aspose.Note for Java'yı kullanırken herhangi bir sorunla karşılaşırsam destek alabilir miyim?

 Cevap4: Evet, Aspose.Note forumundan destek alabilirsiniz[Burada](https://forum.aspose.com/c/note/28).

### S5: Aspose.Note for Java'nın ücretsiz deneme sürümü mevcut mu?

 Cevap5: Evet, Aspose.Note for Java'nın ücretsiz deneme sürümüne şu adresten erişebilirsiniz:[İnternet sitesi](https://releases.aspose.com/).