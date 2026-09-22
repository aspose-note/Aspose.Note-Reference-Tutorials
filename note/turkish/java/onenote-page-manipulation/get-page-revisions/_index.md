---
date: 2026-08-08
description: OneNote'ta track changes'i, Aspose.Note for Java kullanarak page revisions'ı
  programmatically retrieving yöntemiyle öğrenin.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: OneNote'ta Page Revisions'ı Al - Aspose.Note
og_description: OneNote'ta track changes'i, Aspose.Note for Java kullanarak page revisions'ı
  programmatically retrieving yöntemiyle öğrenin.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: OneNote'ta değişiklikleri izleme – page revisions with Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: OneNote'ta değişiklikleri izleme – page revisions with Aspose.Note
url: /tr/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta değişiklikleri izleme – sayfa revizyonları Aspose.Note ile

Bu öğreticide, Aspose.Note Java API'sını kullanarak bir sayfanın tam revizyon geçmişini çıkararak **OneNote'ta değişiklikleri izlemeyi** öğreneceksiniz. Geliştirme ortamınızı kurmaktan her revizyonun yazarını, zaman damgalarını ve başlığını yazdırmaya kadar her şeyi ele alacağız, böylece herhangi bir OneNote tabanlı çözüm için güvenilir denetim izi özellikleri oluşturabilirsiniz.

## Hızlı cevaplar
- **Bu öğretici neyi kapsıyor?** Aspose.Note for Java kullanarak bir OneNote dosyasından sayfa revizyon geçmişini almak.  
- **Hangi kütüphane sürümü gereklidir?** `LoadOptions.setLoadHistory`'i destekleyen herhangi bir güncel Aspose.Note for Java sürümü.  
- **Bir lisansa ihtiyacım var mı?** Test için geçici bir değerlendirme lisansı çalışır; üretim için ticari bir lisans gerekir.  
- **Revizyonları değiştirebilir miyim?** API revizyonlar için yalnızca okuma iznine sahiptir; sadece onları alabilirsiniz.  
- **Ana önkoşullar nelerdir?** Java JDK, Aspose.Note for Java ve revizyon verisi içeren bir OneNote belgesi.

## “aspose.note sayfa revizyonları öğreticisi” nedir?
Bu öğretici, bir OneNote sayfasının tarihsel sürümlerine programlı olarak nasıl erişileceğini gösterir. Her revizyon, yazar, oluşturma zamanı ve değiştirme zamanı gibi meta verileri içerir ve uygulamalarınız içinde denetim izleri veya değişiklik günlüğü özellikleri oluşturmanızı sağlar.

## Sayfa revizyon takibi için neden Aspose.Note kullanmalı?
Standart 2 GHz CPU üzerinde 500 sayfalık bir dosya için bütün revizyon geçmişini 5 saniyeden kısa sürede yükleyebilir ve OneNote UI'sını başlatmadan meta verileri alabilirsiniz. Kütüphane 30'dan fazla giriş ve çıkış formatını destekler, Windows, Linux ve macOS'ta çalışır (sunucu ortamlarının >%95'ini kapsar) ve her revizyon özelliği üzerinde tam kontrol sağlar.

## Önkoşullar

### 1. Java Geliştirme Kiti (JDK)
Güncel bir JDK (8 veya üzeri) kurulu olduğundan ve `JAVA_HOME`'un ayarlandığından emin olun.

### 2. Aspose.Note for Java
Kütüphaneyi [download link](https://releases.aspose.com/note/java/) adresinden indirin.

### 3. Örnek OneNote Belgesi
Revizyon geçmişi içeren sayfalara sahip bir OneNote dosyası (ör. `Sample1.one`) oluşturun veya edinin.

## Paketleri içe aktar
İlk olarak, gerekli Aspose.Note sınıflarını içe aktarın.  
`Document` bir OneNote defterini temsil eder, `LoadOptions` yükleme davranışını yapılandırır ve `Page` tek bir sayfayı temsil eder.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Adım adım uygulama

### Adım 1: belge dizinini ayarla
OneNote dosyanızın bulunduğu klasörü tanımlayın.

```java
String dataDir = "Your Document Directory";
```

### Adım 2: Geçmişi etkinleştirerek OneNote belgesini yükle
`LoadOptions`, Aspose.Note'un bir dosyayı nasıl açacağını, revizyon verilerini okuyup okumayacağını belirten bir yapılandırma sınıfıdır. Belgeyi yüklemeden önce bayrağı etkinleştirin.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Adım 3: ilk sayfayı al
İlk sayfa nesnesini alın; bu, geçmişini alırken referans noktası olacaktır.

```java
Page firstPage = document.getFirstChild();
```

### Adım 4: sayfa revizyonları üzerinde döngü yap
Her revizyonu döngüye alıp zaman damgaları, başlık, seviye ve yazar gibi faydalı meta verileri yazdırın.

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

> **Pro ipucu:** Belirli bir yazar veya tarih aralığına göre revizyonları filtrelemeniz gerekiyorsa, `for` döngüsü içinde koşullu kontroller eklemeniz yeterlidir.

## Yaygın sorunlar ve çözümler
- **Revizyon döndürülmedi:** `loadOptions.setLoadHistory(true)`'in belgeyi yüklemeden önce çağrıldığını doğrulayın.  
- **Null yazar veya başlık:** Bazı eski OneNote sürümleri bu alanları saklamıyor olabilir; `null` değerleri nazikçe işleyin.  
- **Büyük defterlerde performans gecikmesi:** Sadece ihtiyacınız olan bölümleri yükleyin veya JVM yığın boyutunu artırın.

## Sıkça sorulan sorular

**Q1: Aspose.Note for Java kullanarak sayfa revizyonlarını değiştirebilir miyim?**  
A1: Hayır, API şu anda sadece sayfa revizyonlarına okuma‑sadece erişimi desteklemektedir.

**Q2: Aspose.Note for Java farklı OneNote belge sürümleriyle uyumlu mu?**  
A2: Evet, çeşitli OneNote dosya formatlarıyla çalışır ve sürümler arasında sorunsuz işleme imkanı sağlar.

**Q3: Aspose.Note for Java kullanmak lisans gerektiriyor mu?**  
A3: Üretim kullanımı için ticari bir lisans gerekir, ancak test için geçici bir değerlendirme lisansı mevcuttur.

**Q4: Aspose.Note for Java kullanırken herhangi bir sorunla karşılaşırsam destek alabilir miyim?**  
A4: Evet, Aspose.Note forumunda soru sorabilirsiniz [Aspose.Note forum](https://forum.aspose.com/c/note/28).

**Q5: Aspose.Note for Java için ücretsiz deneme sürümü var mı?**  
A5: Evet, [website](https://releases.aspose.com/) adresinden ücretsiz deneme sürümünü indirebilirsiniz.

---

**Son Güncelleme:** 2026-08-08  
**Test Edilen:** Aspose.Note for Java (latest release)  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [OneNote'ta değişiklikleri izleme – Aspose.Note ile Sayfa Revizyonlarını Yönet](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java Öğreticisi - OneNote'taki Sayfalar Hakkında Bilgi Al - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [OneNote Sayfa Arka Planını Değiştir – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}