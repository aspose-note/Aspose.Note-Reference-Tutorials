---
date: 2026-03-21
description: Java ve Aspose.Note kullanarak OneNote belgesi oluşturmayı ve resim alt
  metnini ayarlamayı öğrenin. Bu kılavuz ayrıca OneNote dosyasını nasıl kaydedeceğinizi
  ve erişilebilirliği nasıl artıracağınızı gösterir.
linktitle: Create OneNote Document & Add Alt Text to Images in Java
second_title: Aspose.Note Java API
title: Java'da OneNote Belgesi Oluştur ve Görsellere Alternatif Metin Ekle
url: /tr/java/onenote-image-alternative-text/add-alternative-text-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Belgesi Oluşturma ve Görüntülere Alt Metin Ekleme (Java)

## Giriş

Bu öğreticide, Java ve Aspose.Note API'sını kullanarak programlı bir şekilde **OneNote belgesi oluşturmayı** ve **görüntü alt metni ayarlamayı** öğreneceksiniz. Alternatif metin eklemek, OneNote sayfalarınızı ekran okuyucu kullanıcıları için erişilebilir kılar, aranabilirliği artırır ve **OneNote dosyasını kaydetmenize** daha zengin meta verilerle yardımcı olur. Kılavuzun sonunda, **OneNote sayfalarına görüntü ekleyebilecek**, görüntüye hem bir başlık hem bir açıklama atayabilecek ve dosyayı diske kalıcı olarak kaydedebileceksiniz.

## Hızlı Yanıtlar
- **Gerekli kütüphane nedir?** Aspose.Note for Java  
- **Bu öğreticinin hedeflediği birincil anahtar kelime nedir?** create onenote document  
- **Üretim için lisansa ihtiyacım var mı?** Evet, ticari bir lisans gereklidir (ücretsiz deneme mevcuttur).  
- **Birden fazla görüntüye alt metin ekleyebilir miyim?** Kesinlikle – her görüntü için adımları tekrarlamanız yeterlidir.  
- **Hangi Java sürümü destekleniyor?** Java 8 veya üzeri.

## OneNote bağlamında “create onenote document” ne anlama geliyor?

OneNote belgesi oluşturmak, sayfalar, metin, görüntüler ve diğer zengin içerikleri içerebilen bir `.one` dosyasını programlı olarak oluşturmak anlamına gelir. Aspose.Note ile bu dosyayı sıfırdan oluşturabilir, öğeler ekleyebilir ve ardından **OneNote dosyasını** istediğiniz bir konuma **kaydedebilirsiniz**.

## OneNote'ta görüntülere neden alt metin eklenmeli?

- **Erişilebilirlik:** WCAG yönergelerine uyar ve görme engelli kullanıcıları destekler.  
- **Aranabilirlik:** Arama motorları açıklamayı indeksleyebilir, böylece içeriğiniz daha kolay bulunur.  
- **Profesyonellik:** Kapsayıcı tasarım ve dokümantasyon kalitesine bağlılık gösterir.

## Ön Koşullar

Öğreticiye başlamadan önce aşağıdaki ön koşulları karşıladığınızdan emin olun:

1. Java Development Kit (JDK) – sürüm 8 veya üzeri.  
2. Aspose.Note for Java Kütüphanesi – [buradan](https://releases.aspose.com/note/java/) indirin.  
3. IntelliJ IDEA veya Eclipse gibi bir IDE.  
4. Java programlama temelleri.

## Paketleri İçe Aktarma

İlk olarak, Aspose.Note işlevlerini kullanabilmek için gerekli paketleri Java projenize içe aktarın.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.Page;
```

Şimdi, **adım adım kılavuzu** izleyerek **OneNote belgesi oluşturmayı**, bir görüntü eklemeyi ve **görüntü alt metnini ayarlamayı** inceleyelim.

## Java'da OneNote Belgesi Oluşturma ve Görüntü Alt Metni Ayarlama

### Adım 1: Belge Dizinini Ayarlama

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini, kaynak görüntünüzün bulunduğu ve çıktı `.one` dosyasının kaydedilmesini istediğiniz mutlak yol ile değiştirin.

### Adım 2: Document Nesnesi Oluşturma

```java
Document document = new Document();
```

Bu satır, daha sonra eklenen içerikle **OneNote dosyasını kaydedeceğiniz** yeni bir **OneNote belgesi** oluşturur.

### Adım 3: Page Nesnesi Oluşturma

```java
Page page = new Page();
```

Bir sayfa, görüntü ve eklemek isteyebileceğiniz diğer öğeler için bir tuval görevi görür.

### Adım 4: Sayfaya Bir Görüntü Ekleme

```java
Image image = new Image(null, dataDir + "image.jpg");
```

`Image` yapıcı metodu, belirtilen yoldan görüntü dosyasını yükler. İşte **OneNote'a görüntü ekleme** (append image onenote) noktasına geldiğiniz yer.

### Adım 5: Alternatif Metin Başlığını Ayarla (Görüntü Alt Metnini Ayarla)

```java
image.setAlternativeTextTitle("ImageAlternativeText Title");
```

Burada, resim için özlü bir başlık görevi gören **görüntü alt metnini** ayarlıyoruz.

### Adım 6: Alternatif Metin Açıklamasını Ayarla (Alt Metin Açıklamasını Ayarla)

```java
image.setAlternativeTextDescription("ImageAlternativeText Description");
```

Açıklama, daha ayrıntılı bir açıklama sağlar—ekran okuyucular için mükemmeldir.

### Adım 7: Görüntüyü Sayfaya Ekleme

```java
page.appendChildLast(image);
```

Şimdi, alt metniyle zenginleştirilmiş görüntü **OneNote sayfasına eklenmiştir**.

### Adım 8: Sayfayı Belgeye Ekleme

```java
document.appendChildLast(page);
```

Sayfayı daha önce oluşturduğunuz OneNote belgesine ekleyin.

### Adım 9: Belgeyi Kaydet (OneNote Dosyasını Kaydet)

```java
document.save(dataDir + "AlternativeText_out.one");
```

`save` çağrısı, tüm alt‑metin meta verilerini koruyarak **OneNote dosyasını** diske **yazar**.

## Yaygın Sorunlar ve Çözümler

- **FileNotFoundException:** `dataDir`'in doğru klasöre işaret ettiğini ve `image.jpg` dosyasının mevcut olduğunu doğrulayın.  
- **NullPointerException** görüntüde: Görüntü yolunun geçerli olduğundan ve dosyanın bozuk olmadığından emin olun.  
- **Lisans hataları:** Geçerli bir Aspose.Note lisans dosyası kullanın veya değerlendirme için deneme modunda çalıştırın.

## Sık Sorulan Sorular

**S: Tek bir belge içinde birden fazla görüntüye alt metin ekleyebilir miyim?**  
C: Evet, eklemek istediğiniz her görüntü için adım 4‑6'yı tekrarlamanız yeterlidir.

**S: Alt metin eklemek için hangi görüntü formatları destekleniyor?**  
C: Aspose.Note JPEG, PNG, GIF, BMP ve birkaç diğer yaygın formatı destekler.

**S: Alt metin ayarlandıktan sonra değiştirmek veya kaldırmak mümkün mü?**  
C: Kesinlikle. Değerleri temizlemek için `setAlternativeTextTitle("")` veya `setAlternativeTextDescription("")` çağırın, ya da yeni metinler sağlayarak güncelleyin.

**S: Aspose.Note Java dışındaki diğer diller için API'ler sunuyor mu?**  
C: Evet, kütüphane .NET, C++ ve Python için de mevcuttur.

**S: Aspose.Note deneme sürümünü nereden indirebilirim?**  
C: Ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) edinebilirsiniz.

**S: Birden fazla sayfa ekledikten sonra programlı olarak **OneNote dosyasını** nasıl kaydederim?**  
C: Tüm sayfa ve görüntüleri ekledikten sonra `document.save(<outputPath>)` metodunu bir kez çağırın; API dosyanın tam oluşturulmasını halleder.

**S: Mevcut bir belgede **OneNote'a görüntü eklemek** (append image onenote) için aynı kodu kullanabilir miyim?**  
C: Evet. Mevcut belgeyi `new Document(<filePath>)` ile yükleyin, ardından yeni görüntüler ve alt metin eklemek için adım 3‑7'yi izleyin.

## Sonuç

Bu kılavuzu izleyerek artık Java kullanarak **OneNote belgesi oluşturmayı**, **OneNote'a görüntü eklemeyi** ve **görüntü alt metnini ayarlamayı** biliyorsunuz. Bu adımları uygulamak, OneNote dosyalarınızı daha erişilebilir kılmakla kalmaz, aynı zamanda bulunabilirliğini ve genel kalitesini artırır. Her görüntünün anlamını en iyi şekilde iletmek için farklı başlık ve açıklamalarla denemeler yapmaktan çekinmeyin.

---

**Son Güncelleme:** 2026-03-21  
**Test Edilen Versiyon:** Aspose.Note for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}