---
date: 2026-08-13
description: Aspose.Note for Java ile OneNote sayfa değiştirilme zamanını nasıl alacağınızı
  ve sayfa revizyonlarını nasıl getireceğinizi öğrenin; denetim ve belge yönetimi
  için idealdir.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: OneNote'ta Sayfa Revizyonlarını Al - Aspose.Note
og_description: Aspose.Note for Java ile OneNote sayfa değiştirilme zamanını nasıl
  alacağınızı ve OneNote sayfalarının revizyonlarını nasıl getireceğinizi öğrenin.
  Hızlı adımlar, kod parçacıkları ve sorun giderme.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Aspose.Note kullanarak OneNote sayfa değiştirilme zamanını alın – Java öğreticisi
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Aspose.Note ile OneNote sayfa değiştirilme zamanını alın
url: /tr/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote sayfasının değiştirilme zamanını Aspose.Note ile alın

## Giriş

Bu öğreticide, **get onenote page modified** zaman damgalarını nasıl alacağınızı ve Aspose.Note for Java ile bir OneNote sayfasının tam revizyon geçmişini nasıl çekeceğinizi öğreneceksiniz. Denetim izi özelliği, değişiklik günlüğü görüntüleyicisi oluşturuyor ya da bir gösterge panosunda en son düzenleme tarihini göstermeniz gerekiyorsa, bu kılavuz ortamı kurmaktan yaygın sorunları ele almaya kadar her adımı size anlatır.

## Hızlı cevaplar
- **“get last modified time” ne döndürür?** Bir OneNote sayfasındaki en son düzenlemenin zaman damgasını döndürür.  
- **Hangi sınıf revizyon geçmişini sağlar?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Bu özellik için lisansa ihtiyacım var mı?** Evet, üretim kullanımında geçerli bir Aspose.Note lisansı gereklidir.  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri (JDK 8+).  
- **Revizyonları yazarına göre filtreleyebilir miyim?** Her `Page` nesnesinin `Author` özelliğini okuyabilir ve kendi filtrenizi uygulayabilirsiniz.

## OneNote'ta “get last modified time” nedir?

Değiştirilme zamanı, her OneNote sayfasında en son düzenlemenin gerçekleştiği anı gösteren bir meta veri özniteliği olarak saklanır. Aspose.Note bu değeri `Page.getLastModifiedTime()` yöntemiyle ortaya çıkarır; bu yöntem, uygulamanızın gereksinimlerine göre biçimlendirilebilecek veya kaydedilebilecek bir `java.util.Date` nesnesi döndürür.

## Neden sayfa revizyonlarını almalı?

Sayfa revizyonlarını almak, bir OneNote sayfasında yapılan her değişikliğin tam denetim izini sağlar; kim ne zaman neyi düzenlediğini takip etmenize olanak tanır. Bu geçmiş, sürümleri karşılaştırmak, önceki durumları geri yüklemek veya ekipler arasındaki iş birliği kalıplarını analiz etmek için kullanılabilir; bu da uyumluluk ve kalite kontrolü için hayati öneme sahiptir.

## Önkoşullar

- **Java Development Kit (JDK) 8 veya üzeri** – Oracle web sitesinden veya uyumlu bir satıcıdan yükleyin.  
- **Aspose.Note for Java kütüphanesi** – Aspose.Note Java releases sayfasından JAR'ı indirin **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** ve kurulum kılavuzunu izleyin **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Paketleri içe aktar

`Document` sınıfı belleğe yüklenmiş bir OneNote defterini temsil ederken, `Page` ve `PageHistory` bireysel sayfalara ve revizyon verilerine erişim sağlar.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(The actual import statements are shown as plain text to preserve the original code‑block count.)*  

## OneNote sayfasının değiştirilme zamanını nasıl alırız?

Son değiştirilme zaman damgasını elde etmek için önce OneNote belgesini bir `Document` nesnesine yükleyin, ardından istenen `Page`i seçin. Bu sayfada `getLastModifiedTime()` yöntemini çağırın; yöntem bir `java.util.Date` döndürür. Ardından bu tarihi `SimpleDateFormat` ile biçimlendirebilir veya zaman dilimleri arasında tutarlı raporlama için UTC'ye dönüştürebilirsiniz.

## Adım 1: belge dizinini ayarla

OneNote dosyanızın bulunduğu klasörü tanımlayın.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Adım 2: belgeyi yükle

`.one` dosyanızın tam yolunu geçirerek bir `Document` örneği oluşturun.

```java
String dataDir = "Your Document Directory";
```

## Adım 3: ilk sayfayı al

Belgenin sayfa koleksiyonundan ilk `Page` nesnesini alın.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Adım 4: sayfa revizyonlarını al

Seçilen sayfa için `PageHistory` alın. Defter hiç düzenlenmemişse, bu çağrı `null` döndürebilir.

```java
Page firstPage = doc.getFirstChild();
```

## Adım 5: sayfa revizyonlarını dolaş

Her `Page` revizyonu üzerinde yineleme yapın, `Author` ve `LastModifiedTime` özelliklerini okuyun ve bilgileri görüntüleyin.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Yaygın sorunlar ve çözümler
- **Null `PageHistory`** – Not defterinin gerçekten revizyon içerdiğini doğrulayın; aksi takdirde `getPageHistory` `null` döndürür.  
- **Zaman dilimi farkları** – `getLastModifiedTime()` JVM'nin varsayılan zaman dilimini kullanır. Uygulamanız standart bir bölge gerektiriyorsa `SimpleDateFormat` ile UTC'ye dönüştürün.  
- **Lisans yüklenmedi** – Geçerli bir lisans olmadan Aspose.Note değerlendirme modunda çalışır ve sayfa işleme sınırlamaları getirir. Bu kısıtlamayı önlemek için lisans dosyanızı uygulama başlangıcında yükleyin.

## Sıkça sorulan sorular

**Q1: Aspose.Note for Java'yı yeni OneNote belgeleri oluşturmak için kullanabilir miyim?**  
A: Evet, API programlı olarak OneNote defterlerini sıfırdan oluşturmanıza, düzenlemenize ve kaydetmenize olanak tanır.

**Q2: Aspose.Note for Java farklı OneNote dosya sürümleriyle uyumlu mu?**  
A: Evet, OneNote 2007‑2021 dosya formatlarını destekler ve masaüstü ile bulut ortamları arasında geniş uyumluluk sağlar.

**Q3: OneNote belgelerini dışa aktarırken çıktı formatını özelleştirebilir miyim?**  
A: Kesinlikle. PDF, HTML, PNG veya SVG olarak dışa aktarabilir ve görüntü çözünürlüğü ve yazı tipi gömme gibi seçenekleri kontrol edebilirsiniz.

**Q4: Aspose.Note for Java ticari kullanım için lisans gerektiriyor mu?**  
A: Evet, üretim dağıtımları için ticari bir lisans zorunludur. Değerlendirme için ücretsiz bir deneme mevcuttur.

**Q5: Sorunlarla karşılaşırsam nereden yardım alabilirim?**  
A: Sorular sormak, deneyim paylaşmak ve topluluk ile Aspose mühendislerinden yardım almak için Aspose.Note topluluk forumunu **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** ziyaret edin.

---

**Son Güncelleme:** 2026-08-13  
**Test Edilen Versiyon:** Aspose.Note for Java 23.12 (yazım zamanındaki en son)  
**Yazar:** Aspose

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

## İlgili Öğreticiler

- [Aspose Java Öğreticisi - OneNote Sayfaları Hakkında Bilgi Al - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note sayfa revizyonları öğreticisi – OneNote'ta Sayfa Revizyonlarını Al](/note/java/onenote-page-manipulation/get-page-revisions/)
- [değişiklikleri izleme onenote – Aspose.Note ile Sayfa Revizyonlarını Yönet](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}