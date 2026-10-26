---
date: 2026-10-26
description: Aspose.Note for Java kullanarak OneNote dosyalarından etiketleri nasıl
  çıkaracağınızı öğrenin. Bu öğreticide OneNote dosyasını nasıl yükleyeceğiniz, OneNote
  etiketlerini alacağınız ve OneNote etiketlerini verimli bir şekilde nasıl değiştireceğiniz
  gösterilmektedir.
keywords:
- how to extract tags
- Aspose.Note Java
- OneNote tag extraction
- Java OneNote API
lastmod: 2026-10-26
linktitle: OneNote'tan Etiketleri Nasıl Çıkarılır - Aspose.Note
og_description: Aspose.Note for Java kullanarak OneNote dosyalarından etiketleri nasıl
  çıkaracağınızı öğrenin. Etiketleri verimli bir şekilde yüklemek, okumak ve değiştirmek
  için adım adım kodu izleyin.
og_image_alt: Screenshot of Java code extracting OneNote tags with Aspose.Note
og_title: Aspose.Note ile OneNote'tan etiketleri çıkarma – Java rehberi
schemas:
- author: Aspose
  dateModified: '2026-10-26'
  description: Learn how to extract tags from OneNote files using Aspose.Note for
    Java. This tutorial shows how to load OneNote file, get OneNote tags, and modify
    OneNote tags efficiently.
  headline: How to extract tags from OneNote with Aspose.Note
  type: TechArticle
- questions:
  - answer: '`Document`'
    question: What is the primary class for opening a OneNote file?
  - answer: '`doc.getChildNodes(RichText.class)`'
    question: Which method returns all RichText nodes?
  - answer: Yes, via `noteTag.getCreationTime()`
    question: Can you read a NoteTag’s creation time?
  - answer: Yes, a valid Aspose.Note license is required
    question: Do I need a license for production use?
  - answer: Absolutely, it supports modern Java versions
    question: Is the API compatible with Java 8 and later?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- OneNote
- Aspose.Note
- Java tag extraction
- document processing
- note tags
title: Aspose.Note ile OneNote'tan etiketleri nasıl çıkarılır
url: /tr/java/onenote-tag-operations/get-node-tags/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'tan Etiketleri Nasıl Çıkarabilirsiniz Aspose.Note ile

## Giriş
Eğer bir OneNote belgesinden **etiketleri nasıl çıkaracağınızı** öğrenmek istiyorsanız, doğru yere geldiniz. Bu rehberde bir OneNote dosyasını yükleme, OneNote etiketlerini alma ve hatta bu etiketleri Aspose.Note for Java kullanarak değiştirme sürecini adım adım göstereceğiz. Öğreticinin sonunda etiket çıkarma işlemini herhangi bir Java uygulamasına güvenle entegre edebileceksiniz.

## Hızlı Yanıtlar
- **OneNote dosyasını açmak için birincil sınıf nedir?** `Document`
- **Tüm RichText düğümlerini döndüren yöntem hangisidir?** `doc.getChildNodes(RichText.class)`
- **Bir NoteTag'in oluşturulma zamanını okuyabilir misiniz?** Evet, `noteTag.getCreationTime()` ile
- **Üretim kullanımında lisansa ihtiyacım var mı?** Evet, geçerli bir Aspose.Note lisansı gereklidir
- **API Java 8 ve üzeri ile uyumlu mu?** Kesinlikle, modern Java sürümlerini destekler

## OneNote'ta “etiketleri nasıl çıkaracağınız” ne demektir?
Etiket çıkarmak, paragraf, onay kutusu veya liste öğeleri gibi OneNote içerik öğelerine eklenmiş `NoteTag` meta verilerini okumak anlamına gelir. Bu etiketler durum, etiket, simge ve zaman damgalarını depolar ve `RichText` düğümleri içinde `NoteTag` nesneleri olarak temsil edilir, böylece programlı olarak inceleyebilir veya değiştirebilirsiniz.

## Etiket çıkarma için neden Aspose.Note kullanmalısınız?
OneNote masaüstü uygulamasını kurmadan OneNote dosyalarını işleyebilirsiniz, dağıtım boyutunu 150 MB'a kadar azaltır. Kütüphane Windows, macOS ve Linux'ta çalışır, Java 8'den Java 17 LTS'ye kadar destek sağlar ve gerçek çapraz platform yeteneği sunar. Ayrıca 50'den fazla etiketle ilgili özelliğe tam okuma/yazma erişimi sağlar, toplu analiz veya taşıma senaryolarını mümkün kılar.

## Önkoşullar
- Java geliştirme ortamı (JDK 8+).
- Aspose.Note kütüphanesi, [Aspose.Note for Java download page](https://releases.aspose.com/note/java/) adresinden indirilmiş.
- Bilinen bir dizine yerleştirilmiş örnek bir OneNote belgesi (ör. `Sample1.one`).

## Paketleri İçe Aktarma
İhtiyacınız olan sınıfları içe aktararak başlayın. Bu içe aktarmalar, belge işleme, etiket arayüzleri ve zengin metin düğümlerine erişim sağlar.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTag;
import com.aspose.note.RichText;
```

## OneNote dosyasını nasıl yüklersiniz
`.one` dosyasını, dosya yolu ile yeni bir `Document` örneği oluşturarak yükleyin, örneğin `Document doc = new Document(dataDir + "Sample1.one");`. Bu, not defterini belleğe okur ve etiket işlemleri için hazırlar.

`Document` sınıfı, bir OneNote dosyasını bellek içinde temsil eder ve içeriğini okuma ve manipüle etme yöntemleri sunar.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
```

> **Pro tip:** `dataDir` yolunu mutlak tutun veya yol hatalarını önlemek için `Paths.get(...)` kullanın.

## OneNote etiketlerini nasıl alırsınız
`doc.getChildNodes(RichText.class)` kullanarak tüm `RichText` düğümlerini alın; bu, bir veya daha fazla `NoteTag` nesnesi içerebilen bir koleksiyon döndürür. Ardından bu koleksiyonu döngüyle gezerek her düğümün etiketlerini inceleyebilirsiniz.

Bir `RichText` düğümü, OneNote'ta bir paragraf veya metin bloğuna karşılık gelir ve birden fazla etiket tutabilir.

```java
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
```

## Her düğüm üzerinden yineleme
`RichText` koleksiyonunu bir for‑each döngüsüyle dolaşın, her düğümün etiket koleksiyonunu kontrol ederek ekli `NoteTag` nesnelerini işleyin. Döngü içinde durum veya oluşturulma zamanı gibi özellikleri okuyabilir veya gerektiğinde değiştirmeye karar verebilirsiniz.

```java
// Iterate through each node
for (RichText richText : nodes) {
    // Process each node here
}
```

## Not etiketlerini al (OneNote etiketlerini nasıl değiştirirsiniz)
Düğüm döngüsü içinde, etiket listesini elde etmek için `richText.getTags()` kullanın, `NoteTag` örneklerini filtreleyin ve ardından belgeyi kaydetmeden önce `setStatus` veya `setLabel` gibi özellikleri okuyun veya ayarlayın.

`NoteTag` sınıfı bir OneNote etiketini kapsüller ve durum, etiket, simge, oluşturulma zamanı ve yazar gibi özellikleri ortaya çıkarır.

```java
for (ITag tag : richText.getTags()) {
    if (tag.getClass() == NoteTag.class) {
        NoteTag noteTag = (NoteTag) tag;
        // Retrieve properties
        System.out.println("Completed Time: " + noteTag.getCompletedTime());
        System.out.println("Create Time: " + noteTag.getCreationTime());
        System.out.println("Font Color: " + noteTag.getFontColor());
        System.out.println("Status: " + noteTag.getStatus());
        System.out.println("Label: " + noteTag.getLabel());
        System.out.println("Icon: " + noteTag.getIcon());
        System.out.println("High Light: " + noteTag.getHighlight());
        // Example of modifying a property
        // noteTag.setLabel("Updated Label");
    }
}
```

> **Uyarı:** Bir etiketi değiştirmek temel belgeyi değiştirir. Değişiklik yaptıktan sonra belgeyi kaydetmeyi unutmayın.

## Sonuç
Artık **etiketleri nasıl çıkaracağınızı**, **OneNote dosyasını nasıl yükleyeceğinizi**, **OneNote etiketlerini nasıl alacağınızı** ve hatta Aspose.Note for Java kullanarak **OneNote etiketlerini nasıl değiştireceğinizi** biliyorsunuz. Bu kod parçacıklarını kendi projelerinize entegre ederek not analizi, raporlama veya taşıma görevlerini otomatikleştirebilirsiniz.

## SSS
### Aspose.Note tüm OneNote sürümleriyle uyumlu mu?
Aspose.Note, çeşitli OneNote dosya formatlarını destekler ve farklı sürümler arasında uyumluluğu garanti eder.

### Alınan NoteTag özelliklerini değiştirebilir miyim?
Evet, Aspose.Note, NoteTag özelliklerini programlı olarak değiştirmenize ve güncellemenize olanak tanır.

### Aspose.Note için bir deneme sürümü mevcut mu?
Kesinlikle! Ücretsiz deneme sürümüne [Aspose free trial download page](https://releases.aspose.com/) adresinden erişebilirsiniz.

### Aspose.Note for Java için kapsamlı belgeleri nerede bulabilirim?
Ayrıntılı belgeleri [Aspose.Note Java API documentation](https://reference.aspose.com/note/java/) adresinde inceleyebilirsiniz.

### Herhangi bir sorun veya soru için nasıl destek alabilirim?
Aspose topluluğundan yardım almak için destek forumu [Aspose.Note support forum](https://forum.aspose.com/c/note/28) adresine gidin.

## Sıkça Sorulan Sorular
**Q:** *Şifre korumalı OneNote dosyalarından etiketleri çıkarabilir miyim?*  
**A:** Evet, `Document` nesnesini oluştururken şifreyi sağlayın.

**Q:** *Etiketleri değiştirdikten sonra bir kaydetme metodunu çağırmam gerekiyor mu?*  
**A:** Kesinlikle. Değişiklikleri kalıcı hale getirmek için `doc.save("UpdatedSample.one");` kullanın.

**Q:** *Etiketleri durumuna göre filtrelemek mümkün mü?*  
**A:** Döngü içinde `noteTag.getStatus()` kontrol ederek yalnızca istenen durumları işleyebilirsiniz.

**Q:** *Bir RichText düğümünün etiketi yoksa ne olur?*  
**A:** `richText.getTags()` boş bir koleksiyon döndürür; döngü sadece onu atlar.

**Q:** *Birden fazla OneNote dosyasını toplu olarak işleyebilir miyim?*  
**A:** Yukarıdaki mantığı bir dosya yineleme rutinine sarın ve her belgeyi sırasıyla işleyin.

**Last Updated:** 2026-10-26  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose

## İlgili Eğitimler

- [Java Notebook Nesnesi Oluştur – Seçeneklerle OneNote Dosyasını Yükle - Aspose.Note](/note/java/onenote-notebook-operations/load-notebook-file-with-load-options/)
- [OneNote'u Düz Metne Dönüştür – Tüm Metni Aspose.Note for Java ile Çıkar](/note/java/onenote-text-manipulation/extract-all-text/)
- [Aspose.Note for Java kullanarak OneNote eklerini al](/note/java/onenote-java-integration/retrieve-attachment/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}