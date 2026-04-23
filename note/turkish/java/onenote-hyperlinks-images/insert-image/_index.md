---
date: 2026-03-19
description: Java ve Aspose.Note for Java kullanarak OneNote'a resim eklemeyi, resim
  boyutlarını ayarlamayı ve OneNote'u PDF olarak kaydetmeyi öğrenin.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Java kullanarak OneNote'a resim ekle
url: /tr/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile OneNote Belgesine Görsel Ekleme

## Giriş

Bu öğreticide **OneNote'a görsel ekleme** yöntemini Java ve Aspose.Note for Java kütüphanesini kullanarak programlı bir şekilde öğreneceksiniz. OneNote sayfalarına resim eklemek, toplantı tutanakları, otomatik raporlar veya metinle görsel veriyi birleştiren dokümantasyon oluşturmanız gerektiğinde oldukça kullanışlıdır. Rehberin sonunda mevcut bir OneNote dosyasını yükleyebilecek, bir görsel ekleyebilecek, isteğe bağlı olarak boyut ve konumunu ayarlayabilecek ve hatta **OneNote'u PDF olarak kaydedebileceksiniz** – tüm bunlar OneNote arayüzünü açmadan gerçekleşir.

## Hızlı Yanıtlar
- **Java kullanarak OneNote'a görsel eklemenin en kolay yolu nedir?**  
  Aspose.Note for Java’nın `Image` sınıfını kullanın ve sayfaya ekleyin.
- **Üretim ortamında lisansa ihtiyacım var mı?**  
  Evet, üretim dağıtımları için ticari bir lisans gereklidir.
- **Görsel için özel boyutlar ayarlayabilir miyim?**  
  Kesinlikle – `Image` nesnesi üzerinde `setWidth()` ve `setHeight()` metodlarını çağırın.
- **Görseli ekledikten sonra OneNote dosyasını PDF olarak kaydetmek mümkün mü?**  
  Evet, `save(..., SaveFormat.Pdf)` metodunu çağırarak **OneNote'u PDF olarak kaydedebilirsiniz**.
- **Hangi Java sürümü destekleniyor?**  
  Aspose.Note for Java, JDK 8 ve üzeri sürümlerle çalışır.

## Neden OneNote'a görsel ekleyelim?

Görsel öğeler eklemek notları daha anlaşılır ve ilgi çekici hâle getirir. Görseller, diyagramları, ekran görüntülerini veya veri grafiklerini açıklayan uzun metin açıklamalarının yerine kullanılabilir. Bu adımı otomatikleştirmek, özellikle veri kaynaklarından büyük miktarda not üretirken zaman tasarrufu sağlar.

## Önkoşullar

Başlamadan önce, aşağıdakilerin hazır olduğundan emin olun:

### 1. Java Development Kit (JDK)
JDK 8 veya daha yeni bir sürüm kurun. Oracle web sitesinden indirebilir veya bir OpenJDK dağıtımı kullanabilirsiniz.

### 2. Aspose.Note for Java Library
En son Aspose.Note for Java kütüphanesini indirin ve projenizin sınıf yoluna ekleyin. Ayrıntılı kurulum talimatları resmi [documentation](https://reference.aspose.com/note/java/) sayfasında mevcuttur.

## Paketleri İçe Aktarma

Gerekli sınıfları içe aktararak başlayın. Bu importlar, temel Aspose.Note işlevselliğine ve temel Java yardımcı araçlarına erişmenizi sağlar.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Adım‑Adım Kılavuz

Aşağıda kısa ve numaralı bir yürütme adımı bulacaksınız. Her adım, kısa bir açıklama ve kopyalamanız gereken tam kodu içerir.

### Adım 1: OneNote belgesini yükleyin

`LoadOptions` örneği oluştururuz (gelecekteki özelleştirmeler için faydalıdır) ve mevcut `.one` dosyasını açarız.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### Adım 2: Hedef sayfayı alın

Basitlik açısından belgedeki ilk sayfa ile çalışıyoruz, ancak ihtiyacınız olan herhangi bir sayfaya gidebilirsiniz.

```java
Page page = oneFile.getFirstChild();
```

### Adım 3: Gömmek istediğiniz görseli yükleyin

Belge referansını ve resim dosyasının yolunu geçirerek bir `Image` nesnesi örnekleyin.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### Adım 4: Görsel boyutlarını ayarlayın Java (isteğe bağlı)

Resmin belirli bir alana sığmasını istiyorsanız, genişliğini, yüksekliğini ve ofsetlerini ayarlayın. İşte **set image dimensions java** anahtar kelimesinin devreye girdiği nokta.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### Adım 5: Görseli sayfaya ekleyin

`appendChildLast` yöntemi, görseli seçilen sayfanın son öğesi olarak ekler.

```java
page.appendChildLast(image);
```

### Adım 6: Belgeyi kaydedin – ayrıca OneNote'u PDF olarak da kaydedebilirsiniz

Son olarak değişiklikleri kalıcı hâle getirin. Örnek, dosyayı PDF olarak kaydetmeyi gösterir ve **save onenote as pdf** ikincil anahtar kelimesini karşılar.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Yaygın Sorunlar ve Çözümler

| Semptom | Muhtemel Neden | Çözüm |
|---------|----------------|-------|
| `FileNotFoundException` görüntü yüklenirken | Yanlış görüntü yolu | `dataDir` ve görüntü dosya adının doğru olduğunu doğrulayın. |
| Görsel bozulmuş görünüyor | Genişlik/yükseklik hatalı ayarlanmış | `setWidth`/`setHeight` metodlarını çağırmadan önce orijinal görüntü boyutlarını kullanın veya uygun en‑boy oranını hesaplayın. |
| PDF çıktısı boş | Aspose.Note için lisans eksik | `save` metodunu çağırmadan önce geçerli bir lisans uygulayın. |

## Sıkça Sorulan Sorular

### S1: Bu yöntemle tek bir OneNote belgesine birden fazla görsel ekleyebilir miyim?
**A:** Evet. Eklemek istediğiniz her görsel için Adım 3‑5’i tekrarlayın, aynı ya da farklı sayfalara hedefleyebilirsiniz.

### S2: Aspose.Note for Java, tüm OneNote sürümleriyle uyumlu mu?
**A:** Aspose.Note for Java, Microsoft OneNote 2010 ve sonraki sürümlerle oluşturulmuş OneNote dosyalarını destekler.

### S3: Farklı formatlarda (PNG veya GIF gibi) görselleri OneNote belgesine ekleyebilir miyim?
**A:** Kesinlikle. Kütüphane PNG, JPEG, GIF, BMP ve birkaç yaygın formatı kabul eder.

### S4: Test amaçlı bir Aspose.Note for Java deneme sürümü mevcut mu?
**A:** Evet, satın almadan API’yı değerlendirmek için Aspose web sitesinden ücretsiz bir deneme sürümü indirebilirsiniz.

### S5: Aspose.Note for Java için teknik destek nasıl alınır?
**A:** Aspose.Note ürünlerine özel [forum](https://forum.aspose.com/c/note/28) üzerinden yardım alabilirsiniz.

## Sonuç

Artık **OneNote'a görsel ekleme** yöntemini Java ile gösteren, görünümünü özelleştiren ve isteğe bağlı olarak **OneNote'u PDF olarak kaydedebilen** eksiksiz, üretim‑hazır bir örneğe sahipsiniz. Kodu kendi iş akışlarınıza uyarlamaktan çekinmeyin—raporlama motoru, otomatik dokümantasyon sistemi veya özel bir not‑alma uygulaması geliştiriyor olun.

---

**Son Güncelleme:** 2026-03-19  
**Test Edilen Sürüm:** Aspose.Note for Java 24.10  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}