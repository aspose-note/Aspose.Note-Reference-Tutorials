---
title: OneNote'ta Sayfaların Revizyonlarını Alın - Aspose.Note
linktitle: OneNote'ta Sayfaların Revizyonlarını Alın - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note Java'yı kullanarak OneNote belgeleri içindeki sayfaların revizyonlarını nasıl alacağınızı öğrenin. Verimli belge yönetimi için bunu Java uygulamalarınıza entegre edin.
type: docs
weight: 15
url: /tr/java/onenote-page-manipulation/get-revisions-of-pages/
---
## giriiş

Bu eğitimde, Java uygulamalarınızda Microsoft OneNote dosyalarıyla sorunsuz bir şekilde çalışmanıza olanak tanıyan güçlü bir kütüphane olan Aspose.Note for Java'nın yeteneklerini inceleyeceğiz. Özellikle OneNote belgesindeki sayfaların düzeltmelerinin nasıl alınacağına odaklanacağız. Bu kılavuzun sonunda, son değiştirilme zamanı, oluşturulma zamanı, başlık, seviye ve yazar gibi ayrıntılar da dahil olmak üzere sayfa revizyonlarını verimli bir şekilde çıkarma bilgisine sahip olacaksınız.

## Önkoşullar

Bu eğitime dalmadan önce aşağıdaki önkoşulların ayarlandığından emin olun:

### Java Geliştirme Kiti (JDK) Kurulu

Sisteminizde Java Development Kit'in kurulu olduğundan emin olun. Bunu Oracle web sitesinden indirip yükleyebilir veya Unix tabanlı bir sistem kullanıyorsanız bir paket yöneticisi kullanabilirsiniz.

### Java Kütüphanesi için Aspose.Note

 Aspose.Note for Java kütüphanesini web sitesinden indirip yükleyin. İndirme linkini bulabilirsiniz[Burada](https://releases.aspose.com/note/java/) . Belgelerde sağlanan kurulum talimatlarını izleyin[Burada](https://reference.aspose.com/note/java/).

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Java projenize aktarın. Bu paketler Aspose.Note for Java tarafından sağlanan işlevsellikten yararlanmanıza olanak tanır.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Şimdi, her bir bileşeni ve işlevselliğini anlamak için sağlanan örnek kodu birden fazla adıma ayıralım.

## 1. Adım: Belge Dizinini Ayarlayın

OneNote belgenizin bulunduğu dizini tanımlayın.

```java
String dataDir = "Your Document Directory";
```

## Adım 2: Belgeyi Yükleyin

OneNote belgesini Aspose.Note'a yükleyin.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 3. Adım: İlk Sayfayı Alın

Belgenin ilk sayfasını alın.

```java
Page firstPage = doc.getFirstChild();
```

## 4. Adım: Sayfa Düzeltmelerini Alın

Sayfanın revizyon geçmişini edinin.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Adım 5: Sayfa Düzeltmelerini Geçin

Sayfa revizyonları listesini yineleyin ve ilgili bilgileri alın.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Çözüm

Bu eğitimde, Aspose.Note for Java'yı kullanarak OneNote belgesindeki sayfaların revizyonlarının nasıl alınacağını araştırdık. Adım adım kılavuzu izleyerek ve sağlanan örnek koddan yararlanarak, bu işlevselliği Java uygulamalarınıza kolayca entegre ederek OneNote dosyalarının verimli yönetimini sağlayabilirsiniz.

## SSS'ler

### S1: Aspose.Note for Java'yı yeni OneNote belgeleri oluşturmak için kullanabilir miyim?

C1: Evet, Aspose.Note for Java, OneNote belgelerini programlı olarak oluşturmak, okumak ve değiştirmek için kapsamlı destek sağlar.

### S2: Aspose.Note for Java, OneNote dosyalarının farklı sürümleriyle uyumlu mudur?

C2: Evet, Aspose.Note for Java, Microsoft OneNote dosyalarının çeşitli sürümlerini destekleyerek farklı ortamlar arasında uyumluluk sağlar.

### S3: OneNote belgelerini dışa aktarırken çıktı biçimini özelleştirebilir miyim?

Cevap3: Kesinlikle, Aspose.Note for Java, OneNote belgelerini PDF, HTML ve görseller gibi farklı formatlara ve özelleştirme seçeneklerine dışa aktarma konusunda esneklik sunar.

### S4: Aspose.Note for Java ticari kullanım için lisans gerektiriyor mu?

Cevap4: Evet, Aspose.Note for Java'nın ticari kullanımı için geçerli bir lisans gereklidir. Aspose web sitesinden lisans alabilirsiniz.

### S5: Aspose.Note for Java ile ilgili sorunlarla karşılaşırsam veya sorularım olursa nereden yardım alabilirim?

 Cevap5: Destek ve yardım için Aspose.Note forumunu ziyaret edebilirsiniz.[Burada](https://forum.aspose.com/c/note/28)Soru sorabileceğiniz, deneyimlerinizi paylaşabileceğiniz ve diğer kullanıcılar ve uzmanlarla etkileşimde bulunabileceğiniz yer.