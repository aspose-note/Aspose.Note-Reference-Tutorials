---
date: 2026-01-10
description: Aspose.Note for Java kullanarak OneNote sayfalarının son değiştirilme
  zamanını nasıl alacağınızı ve revizyonlarını nasıl getireceğinizi öğrenin. Bunu
  Java uygulamalarınıza entegre ederek verimli belge yönetimi sağlayın.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote Sayfalarının Son Değiştirilme Zamanını Nasıl Alabilirsiniz – Aspose.Note
url: /tr/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Sayfalarının Revizyonlarını Al - Aspose.Note

## Giriş

Bu öğreticide, bir OneNote belgesi içindeki sayfalar için **son değiştirilme zamanını** alacak ve Aspose.Note for Java kullanarak tam revizyon geçmişini nasıl alacağınızı keşfedeceksiniz. İster bir belge‑yönetim sistemi oluşturuyor olun, değişiklikleri denetliyor olun ya da sadece bir sayfanın en son ne zaman düzenlendiğini göstermeniz gerekiyor olsun, bu kılavuz size bu bilgiyi programlı olarak nasıl çıkaracağınızı tam olarak gösterir.

## Hızlı Yanıtlar
- **“get last modified time” ne döndürür?** OneNote sayfasındaki en son düzenlemenin zaman damgası.  
- **Hangi sınıf revizyon geçmişini sağlar?** `Document.getPageHistory(Page)` aracılığıyla `PageHistory`.  
- **Bu özellik için lisans gerekir mi?** Evet, üretim kullanımında geçerli bir Aspose.Note lisansı gereklidir.  
- **Hangi Java sürümü desteklenir?** Java 8 ve üzeri (JDK 8+).  
- **Revizyonları yazarına göre filtreleyebilir miyim?** Her `Page` nesnesinin `Author` özelliğini okuyabilir ve kendi filtrenizi uygulayabilirsiniz.

## OneNote'ta “get last modified time” nedir?

**Son değiştirilme zamanı**, her sayfada saklanan ve sayfanın en son ne zaman değiştiğini kaydeden bir meta veri alanıdır. Aspose.Note bu değeri `Page.getLastModifiedTime()` yöntemiyle sunar, böylece değişiklik tarihlerini göstermek veya kaydetmek kolaylaşır.

## Sayfa revizyonlarını neden almalı?

- **Denetim izleri:** Kim neyi ve ne zaman değiştirdiğine dair bir kayıt tutun.  
- **Sürüm karşılaştırması:** İki revizyonu yan yana karşılaştıran özellikler oluşturun.  
- **Kullanıcı iş birliği içgörüleri:** Paylaşılan not defterlerindeki düzenleme kalıplarını anlayın.  

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

### Java Development Kit (JDK) Kurulu
Oracle web sitesinden veya tercih ettiğiniz paket yöneticisinden JDK 8 veya daha yeni bir sürümünü kurun.

### Aspose.Note for Java Kütüphanesi
Kütüphaneyi resmi siteden indirin. İndirme bağlantısını **[burada](https://releases.aspose.com/note/java/)** bulabilirsiniz. Belgelerdeki kurulum talimatlarını **[burada](https://reference.aspose.com/note/java/)** izleyin.

## Paketleri İçe Aktarma

Başlamak için, Java projenize gerekli paketleri içe aktarın. Bu paketler, Aspose.Note for Java tarafından sağlanan işlevselliği kullanmanızı sağlar.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Şimdi, verilen örnek kodu birden fazla adıma ayırarak her bileşeni ve işlevini anlamaya çalışalım.

## OneNote Sayfasının Son Değiştirilme Zamanını Nasıl Alırsınız

### Adım 1: Belge Dizini Ayarla
OneNote belgenizin bulunduğu dizini tanımlayın.

```java
String dataDir = "Your Document Directory";
```

### Adım 2: Belgeyi Yükle
OneNote belgesini Aspose.Note içine yükleyin.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Adım 3: İlk Sayfayı Al
Belgeden ilk sayfayı alın.

```java
Page firstPage = doc.getFirstChild();
```

### Adım 4: Sayfa Revizyonlarını Al
Sayfanın revizyon geçmişini elde edin.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Adım 5: Sayfa Revizyonlarını Gezin
Sayfa revizyonları listesini döngüyle geçin ve **son değiştirilme zamanı** dahil ilgili bilgileri alın.

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

## Yaygın Sorunlar ve Çözümler
- **Null `PageHistory`**: Belgenin gerçekten revizyon içerdiğinden emin olun; aksi takdirde `getPageHistory` `null` döndürebilir.  
- **Saat dilimi farkları**: `getLastModifiedTime()` sistemin varsayılan saat diliminde bir `java.util.Date` döndürür. Gerekirse UTC'ye dönüştürün.  
- **Lisans yüklenmedi**: Geçerli bir lisans olmadan Aspose.Note değerlendirme modunda çalışabilir ve işlenen sayfa sayısını sınırlayabilir.

## Sıkça Sorulan Sorular

### S1: Aspose.Note for Java ile yeni OneNote belgeleri oluşturabilir miyim?
C1: Evet, Aspose.Note for Java, OneNote belgelerini programlı olarak oluşturma, okuma ve manipüle etme konusunda kapsamlı destek sağlar.

### S2: Aspose.Note for Java farklı OneNote dosya sürümleriyle uyumlu mu?
C2: Evet, Aspose.Note for Java, Microsoft OneNote dosyalarının çeşitli sürümlerini destekler ve farklı ortamlar arasında uyumluluğu sağlar.

### S3: OneNote belgelerini dışa aktarırken çıktı formatını özelleştirebilir miyim?
C3: Kesinlikle, Aspose.Note for Java, OneNote belgelerini PDF, HTML ve görüntüler gibi farklı formatlara dışa aktarırken özelleştirme seçenekleri sunar.

### S4: Aspose.Note for Java ticari kullanım için lisans gerektiriyor mu?
C4: Evet, Aspose.Note for Java'nun ticari kullanımında geçerli bir lisans gerekir. Lisansı Aspose web sitesinden temin edebilirsiniz.

### S5: Aspose.Note for Java ile ilgili sorun yaşarsam veya sorularım olursa nereden destek alabilirim?
C5: Destek ve yardım için Aspose.Note forumunu **[burada](https://forum.aspose.com/c/note/28)** ziyaret edebilirsiniz; burada sorular sorabilir, deneyimlerinizi paylaşabilir ve diğer kullanıcılar ve uzmanlarla etkileşimde bulunabilirsiniz.

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}