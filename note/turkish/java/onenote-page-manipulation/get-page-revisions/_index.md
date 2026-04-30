---
date: 2026-01-10
description: Java için Aspose.Note sayfa revizyonları öğreticisini öğrenin – Aspose.Note
  kullanarak OneNote sayfa revizyonlarını programlı olarak alın. Adım adım rehberimizi
  izleyin.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: aspose.note sayfa revizyonları öğreticisi – OneNote'ta Sayfa Revizyonlarını
  Al
url: /tr/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Sayfa Revizyonlarını Alın - Aspose.Note

OneNote, güçlü bir not alma platformudur ve değişiklikleri denetlemeniz gerektiğinde, **aspose.note page revisions tutorial** size sadece birkaç Java kod satırıyla revizyon geçmişini nasıl alacağınızı tam olarak gösterir. Bu rehberde, ortamı kurmaktan her revizyonun ayrıntılarını yazdırmaya kadar ihtiyacınız olan her şeyi adım adım anlatacağız—böylece düzenlemeleri, yazar katkılarını ve zaman damgalarını zahmetsizce izleyebilirsiniz.

## Hızlı Yanıtlar
- **Bu eğitim neyi kapsıyor?** Aspose.Note for Java kullanarak bir OneNote dosyasından sayfa revizyon geçmişini alma.  
- **Hangi kütüphane sürümü gerekiyor?** `LoadOptions.setLoadHistory` özelliğini destekleyen herhangi bir güncel Aspose.Note for Java sürümü.  
- **Lisans gerekli mi?** Test için geçici bir değerlendirme lisansı yeterlidir; üretim için ticari lisans gerekir.  
- **Revizyonları değiştirebilir miyim?** API revizyonlar için yalnızca okuma izni verir; sadece alabilirsiniz.  
- **Ana önkoşullar nelerdir?** Java JDK, Aspose.Note for Java ve revizyon verisi içeren bir OneNote belgesi.

## “aspose.note page revisions tutorial” nedir?
Bu eğitim, bir OneNote sayfasının tarihsel sürümlerine programlı olarak nasıl erişileceğini gösterir. Her revizyon, yazar, oluşturulma zamanı ve değiştirilme zamanı gibi meta verileri içerir; bu sayede uygulamalarınız içinde denetim izleri veya değişiklik günlükleri oluşturabilirsiniz.

## Sayfa revizyon takibi için neden Aspose.Note kullanmalı?
- **UI bağımlılığı yok** – tamamen kod içinde çalışır, arka uç hizmetleri için mükemmeldir.  
- **Çapraz platform** – Java, Windows, Linux ve macOS üzerinde çalışır.  
- **Tam kontrol** – OneNote’u manuel olarak açmadan her revizyon özelliğini alabilirsiniz.  
- **Performans** – geçmişin yüklenmesi optimize edilmiştir, bu sayede büyük not defterleri bile hızlı işlenir.

## Önkoşullar

### 1. Java Development Kit (JDK)
Güncel bir JDK (8 veya üzeri) kurulu olduğundan ve `JAVA_HOME` değişkeninin ayarlandığından emin olun.

### 2. Aspose.Note for Java
Kütüphaneyi [download link](https://releases.aspose.com/note/java/) adresinden indirin.

### 3. Sample OneNote Document
Revizyon geçmişi içeren sayfalara sahip bir OneNote dosyası (ör. `Sample1.one`) oluşturun veya edinin.

## Paketleri İçe Aktarın
İlk olarak, gerekli Aspose.Note sınıflarını içe aktarın.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Adım Adım Uygulama

### Adım 1: Belge Dizinini Ayarlama
OneNote dosyanızın bulunduğu klasörü tanımlayın.

```java
String dataDir = "Your Document Directory";
```

### Adım 2: Geçmişi Etkinleştirerek OneNote Belgesini Yükleme
`LoadOptions` bayrağını etkinleştirerek revizyon verilerini alın.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Adım 3: İlk Sayfayı Alın
İlk sayfa nesnesini alın; bu, geçmişini alırken referans noktası olacaktır.

```java
Page firstPage = document.getFirstChild();
```

### Adım 4: Sayfa Revizyonları Üzerinde Döngü
Her revizyonu döngüye alarak zaman damgaları, başlık, seviye ve yazar gibi faydalı meta verileri yazdırın.

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

> **Pro tip:** Belirli bir yazar veya tarih aralığına göre revizyonları filtrelemeniz gerekiyorsa, `for` döngüsü içinde koşullu kontroller eklemeniz yeterlidir.

## Yaygın Sorunlar ve Çözümler
- **Revizyon döndürülmedi:** Belgeyi yüklemeden önce `loadOptions.setLoadHistory(true)` çağrısının yapıldığını doğrulayın.  
- **Yazar veya başlık null:** Bazı eski OneNote sürümleri bu alanları saklamayabilir; `null` değerleri nazikçe ele alın.  
- **Büyük not defterlerinde performans gecikmesi:** Sadece ihtiyacınız olan bölümleri yükleyin veya JVM yığın boyutunu artırın.

## Sık Sorulan Sorular

**S1: Aspose.Note for Java kullanarak sayfa revizyonlarını değiştirebilir miyim?**  
C1: Hayır, API şu anda sadece sayfa revizyonlarına yalnızca okuma erişimini desteklemektedir.

**S2: Aspose.Note for Java farklı OneNote belge sürümleriyle uyumlu mu?**  
C2: Evet, çeşitli OneNote dosya formatlarıyla çalışır ve sürümler arasında sorunsuz işleme imkanı sunar.

**S3: Aspose.Note for Java kullanmak için lisans gerekiyor mu?**  
C3: Üretim kullanımı için ticari lisans gerekir, ancak test için geçici bir değerlendirme lisansı mevcuttur.

**S4: Aspose.Note for Java kullanırken bir sorunla karşılaşırsam destek alabilir miyim?**  
C4: Evet, Aspose.Note forumunda sorularınızı [burada](https://forum.aspose.com/c/note/28) sorabilirsiniz.

**S5: Aspose.Note for Java için ücretsiz deneme sürümü var mı?**  
C5: Evet, ücretsiz deneme sürümünü [website](https://releases.aspose.com/) üzerinden indirebilirsiniz.

**Son Güncelleme:** 2026-01-10  
**Test Edilen Versiyon:** Aspose.Note for Java (en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}