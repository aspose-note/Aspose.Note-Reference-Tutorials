---
date: 2025-12-23
description: Java ve Aspose.Note kullanarak OneNote belgelerindeki görsellere alternatif
  metin eklemeyi öğrenin. Bu kılavuz, daha iyi erişilebilirlik için alternatif metin
  eklemenin nasıl yapılacağını gösterir.
linktitle: How to Add Alt Text to Image in OneNote using Java
second_title: Aspose.Note Java API
title: Java Kullanarak OneNote'ta Görsele Alternatif Metin Ekleme
url: /tr/java/onenote-image-alternative-text/add-alternative-text-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Kullanarak OneNote'ta Görsele Alt Metin Ekleme

## Giriiş

Bu öğreticide, Java ve Aspose.Note API'si kullanarak OneNote açıklamalarındaki görsellere **alt metin eklemeyi** keşfedeceksiniz. Alternatif metin (alt metin) seçilebilir, ekran okuyucusu için erişilebilirliği artırılır ve içeriğinizin genel kapsayıcılığı yükseltilir. Bu rehberin sonunda Java'nın görsel alt metnini ayarlayabilecek ve OneNote dosyalarınızı erişilebilir hale getirerek daha uygun hale getirebileceksiniz.

## Hızlı Yanıtlar
- **Hangi kütüphane gereklidir?** Aspose.Note for Java
- **Bu eğitim hangi birincil anahtar kelimeyi hedefliyor?** alt nasıl eklenir
- **Üretim için lisansa ihtiyacım var mı?** Evet, ticari lisans gereklidir (ücretsiz deneme sürümü mevcuttur).
- **Birden fazla görsele alternatif metin ekleyebilir miyim?** Kesinlikle; adımları her görsel için tekrarlamanız yeterli.
- **Hangi Java sürümü destekleniyor?** Java8 veya üzeri.

## OneNote bağlamında "alt nasıl eklenir" nedir?

Alt metni birleştirme, bir görselin yardımcı teknolojiler tarafından okunabilmesi için metinsel bir açıklamanın sağlanması. Bu açıklama, görseli göremeyen kullanıcıların amacını anlamalarına yardımcı olur.

## OneNote'ta görsellere neden alternatif metin eklenmeli?

- **Erişilebilirlik:** WCAG yönergelerine uyar ve görme engelli kullanıcıların deneyimini geliştirir.
- **Aranabilirlik:** Arama motorları açıklamayı indeksleyebilir, dolayısıyla içeriğiniz daha keşfedilebilir olur.
- **Profesyonellik:** Kapsayıcının olan bağlılığınızı gösterir.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. Java Geliştirme Kiti (JDK) – sürüm 8 veya üzeri.
2. Aspose.Note for Java Library – onu [buradan](https://releases.aspose.com/note/java/) adresinden indirin.
3. IntelliJ IDEA veya Eclipse gibi bir IDE.
4. Java programlamaya ilişkin temel bilgiler.

## Paketleri İçe Aktarma

Öncelikle, Aspose.Note işlevlerini kullanmak için gerekli paketleri Java projenize içe aktarın.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

Şimdi, Java ve Aspose.Note kullanarak bir OneNote belgesine **alternatif metinli resim** ekleme sürecini adım adım talimatlara ayıralım.

## Java Kullanarak OneNote'taki Resimlere Alternatif Metin Nasıl Eklenir

### Adım 1: Belge Dizini Kurulumu

```java
String dataDir = "Your Document Directory";
```

"Belge Dizininiz" ifadesini, kaynak görselinizi içeren ve çıktı dosyasının kaydedileceği klasörün yoluyla değiştirin.

### Adım 2: Belge Nesnesi Oluşturma

```java
Document document = new Document();
```

Bu, yeni ve boş bir OneNote belgesi oluşturur.

### Adım 3: Sayfa Nesnesi Oluşturma

```java
Page page = new Page();
```

Ekleyeceğimiz görseli bir sayfaya yerleştireceğiz.

### Adım 4: Sayfaya Görsel Ekleme

```java
Image image = new Image(dataDir + "image.jpg");
```

`Görüntü` yapıcı fonksiyonu, belirtilen yoldan görsel dosyasını yükler.

### Adım 5: Alternatif Metin Başlığı Ayarlama

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

Burada, görsel için kısa bir başlık görevi gören **alternatif metin** ekliyoruz.

### Adım 6: Alternatif Metin Açıklaması Ayarlama

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

Bu açıklama, ekran okuyucular için mükemmel olan daha ayrıntılı bir açıklama sağlar.

### Adım 7: Görseli Sayfaya Ekleme

```java
page.appendChildLast(image);
```

Görüntü (artık alternatif metinle zenginleştirilmiş) sayfaya eklenir.

### Adım 8: Sayfayı Belgeye Ekleyin

```java
document.appendChildLast(page);
```

Sayfayı OneNote belgesine ekleyin.

### Adım 9: Belgeyi Kaydedin

```java
document.save(dataDir + "AlternativeText_out.one");
```

Belge, alternatif metin resmin içine gömülü olarak kaydedilir.

## Sık Karşılaşılan Sorunlar ve Çözümler

- **FileNotFoundException:** `dataDir`'in doğru klasöre işaret ettiğinden ve `image.jpg` dosyasının mevcut olduğundan emin olun.

- **Resimde NullPointerException:** Resim yolunun geçerli olduğundan ve dosyanın bozuk olmadığından emin olun.

- **Lisans hataları:** Geçerli bir Aspose.Note lisans dosyası kullanın veya değerlendirme için deneme modunda çalıştırın.

## Sıkça Sorulan Sorular

**S: Tek bir belge içinde birden fazla resme alternatif metin ekleyebilir miyim?**
C: Evet, açıklama eklemek istediğiniz her resim için 4-6 arasındaki adımları tekrarlayın.

**S: Alternatif metin eklemek için hangi resim formatları destekleniyor?**
C: Aspose.Note, JPEG, PNG, GIF, BMP ve diğer birçok yaygın formatı destekler.

**S: Ayarlandıktan sonra alternatif metni değiştirmek veya kaldırmak mümkün mü?**
C: Kesinlikle. Değerleri temizlemek için `setAlternativeTextTitle("")` veya `setAlternativeTextDescription("")` fonksiyonlarını çağırın veya bunları güncellemek için yeni dizeler sağlayın.

**S: Aspose.Note, Java dışında başka diller için de API sağlıyor mu?**
C: Evet, kütüphane .NET, C++ ve Python için de mevcuttur.

**S: Aspose.Note'un deneme sürümünü nereden indirebilirim?**
C: Ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) edinebilirsiniz.

## Sonuç

Bu adım adım kılavuzu izleyerek, artık Java kullanarak OneNote'ta resimlere alternatif metin **nasıl** ekleyeceğinizi biliyorsunuz. `Alternatif metin resim ekleme` özelliğini uygulamak, belgelerinizi daha erişilebilir hale getirmekle kalmaz, aynı zamanda arama kolaylığını ve genel kalitesini de artırır. Her bir görselin anlamını en iyi şekilde iletmek için farklı başlıklar ve açıklamalarla denemeler yapmaktan çekinmeyin.

---

**Son Güncelleme:** 2025-12-23
**Test Edildiği Sürüm:** Aspose.Note for Java 26.4
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}