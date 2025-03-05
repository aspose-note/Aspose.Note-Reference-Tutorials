---
title: OneNote'taki Sayfalar Hakkında Bilgi Alın - Aspose.Note
linktitle: OneNote'taki Sayfalar Hakkında Bilgi Alın - Aspose.Note
second_title: Aspose.Note Java API'si
description: OneNote belgelerinizdeki sayfa sırlarını ortaya çıkarın! Aspose.Note ile revizyonları, oluşturma sürelerini ve daha fazlasını çıkarın. Adım adım kılavuz ve kod dahildir! #OneNote #Java #Aspose
type: docs
weight: 12
url: /tr/java/onenote-page-manipulation/get-information-about-pages/
---
## giriiş

Bu eğitimde, Aspose.Note for Java'yı kullanarak OneNote'taki sayfalar hakkında bilgi çıkarma sürecinde size rehberlik edeceğiz. Aspose.Note, Microsoft OneNote belgeleriyle programlı olarak çalışmanıza olanak tanıyan güçlü bir API'dir. Sayfa revizyonlarına, oluşturma zamanlarına, başlıklara veya yazarlara erişmeniz gerekiyorsa Aspose.Note, sezgisel arayüzüyle görevi basitleştirir.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın kurulu olduğundan emin olun.
2.  Aspose.Note for Java: Aspose.Note for Java kütüphanesini indirip yükleyin. Şu adresten alabilirsiniz:[İnternet sitesi](https://purchase.aspose.com/buy).
3. Örnek OneNote Belgesi: Bilgi almak için kullanacağınız örnek bir OneNote belgesi hazırlayın.

## Paketleri İçe Aktar

Öncelikle Java projenizde Aspose.Note ile çalışmak için gerekli paketleri içe aktarmanız gerekiyor.

```java
import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## 1. Adım: OneNote Belgesini Yükleyin

Aspose.Note'u kullanarak OneNote belgesini yükleyerek başlayın.

```java
String dataDir = "Your Document Directory";
// Belgeyi Aspose.Note'a yükleyin
LoadOptions options = new LoadOptions();
Document doc = new Document(dataDir + "Sample1.one", options);
```

 Yer değiştirmek`"Your Document Directory"` OneNote belgenizin yolu ile birlikte.

## Adım 2: Sayfa Bilgilerini Alın

Daha sonra OneNote belgesindeki sayfalarla ilgili bilgileri alın.

```java
// Sayfa revizyonlarını alın
List<Page> pages = doc.getChildNodes(Page.class);

// Sayfaların listesi arasında geçiş yap
for (Page pageRevision : pages) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
}
```

Bu kod parçacığı, belgedeki her sayfa boyunca yinelenir ve her sayfanın son değiştirilme zamanı, oluşturulma zamanı, başlığı, düzeyi ve yazarı gibi bilgileri yazdırır.

## Çözüm

Bu eğitimde Aspose.Note for Java'yı kullanarak OneNote'taki sayfalar hakkındaki bilgileri nasıl alacağınızı öğrendiniz. Yukarıda özetlenen adımları izleyerek Aspose.Note'u Java uygulamalarınıza sorunsuz bir şekilde entegre ederek OneNote belgelerinden değerli veriler elde edebilirsiniz.

## SSS'ler

### S1: OneNote belgelerini düzenlemek için Aspose.Note for Java'yı kullanabilir miyim?

Cevap1: Evet, Aspose.Note, OneNote belgelerini programlı olarak düzenlemek ve değiştirmek için kapsamlı bir dizi özellik sunar.

### S2: Aspose.Note, OneNote'un tüm sürümleriyle uyumlu mudur?

Cevap2: Aspose.Note, OneNote'un çeşitli sürümlerini destekleyerek farklı ortamlar arasında uyumluluk sağlar.

### S3: OneNote belgelerini Aspose.Note'u kullanarak diğer formatlara dönüştürebilir miyim?

Cevap3: Kesinlikle Aspose.Note, OneNote belgelerini PDF, HTML ve görseller gibi formatlara zahmetsizce dönüştürmenize olanak tanır.

### S4: Aspose.Note geliştiricilere teknik destek sunuyor mu?

Cevap4: Evet, Aspose, geliştiricilere Aspose.Note'u kullanırken karşılaştıkları sorunlarda yardımcı olmak için özel teknik destek sağlar.

### S5: Aspose.Note for Java'nın deneme sürümü mevcut mu?

 Cevap5: Evet, Aspose.Note for Java'nın ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Burada](https://releases.aspose.com/).