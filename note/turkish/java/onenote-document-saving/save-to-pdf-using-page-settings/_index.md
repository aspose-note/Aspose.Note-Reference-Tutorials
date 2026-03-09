---
date: 2025-12-17
description: OneNote'tan PDF kaydetmeyi Aspose.Note for Java ile öğrenin. Bu adım
  adım kılavuz, OneNote'u PDF'ye nasıl dönüştüreceğinizi ve PDF sayfa boyutunu Letter
  ve A4 ayarlarıyla nasıl özelleştireceğinizi gösterir.
linktitle: How to Save PDF Using Page Settings in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'ta Sayfa Ayarlarıyla PDF Nasıl Kaydedilir - Aspose.Note
url: /tr/java/onenote-document-saving/save-to-pdf-using-page-settings/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Sayfa Ayarlarını Kullanarak PDF Kaydetme - Aspose.Note

## Giriiş

OneNote'u PDF'ye dönüştürürken, farklı sayfa boyutu üzerinde tam kontrol sağlamak istiyorsanız doğru yerdesiniz. Bu öğreticide Aspose.Note for Java kullanarak bir OneNote dosyasından **PDF nasıl saklanır** adım adım gösteririz. İki pratik senaryoyu göreceksiniz — klasik Letter veri kaydetme ve ölçeklenebilir olmayan A4 sayfası kaydetme — böylece **PDF sayfa değişimi** raporlama veya baskınıza göre özelleştirebileceksiniz.

## Hızlı Yanıtlar
- **Ana yükü nedir?** Aspose.Note for Java
- **Hangi sayfa boyutları kapsanıyor mu?** Letter ve A4 (yükseklik sınırlaması yok)
- **Test için lisansa ihtiyacınız var mı?** Ücretsiz deneme mevcuttur; üretim için lisans gereklidir
- **Gerekli Java sürümü nedir?** JDK8 veya üzeri
- **Birden fazladan toplu işleyebilir miyim?** Evet, `Belge` sınıfı üzerinden döngü yaparak

## Önkoşullar

Başlamadan önce gelişmelerin olduğundan emin **Java Development Kit (JDK)** yüklü (sürüm8 veya üzeri).
2. **Aspose.Note for Java** kütüphanesini projenizin classpath'ine ekleyin.
3. Java sözlerini ve dosya G/Ç hakkında temel bir anlayış.

## Paketleri İçe Aktar

Öncelikle ihtiyaç duyacağınız ad alanlarını içe aktarın. Bu bloğu tam olarak gösterildiği gibi tutun; kod değişiklik yapılmadan derlenecektir.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Mektup Sayfası Ayarlarını Kullanarak PDF Nasıl Kaydedilir

### Adım 1: OneNote Belgesini Yükleyin

Kaynak `.one` dosyasını yükleyerek başlıyoruz. Yer tutucu yolunu OneNote dosyanızın gerçek konumuyla değiştirin.

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Adım 2: Hedef Yolu Tanımlayın

Oluşturulan PDF'nin nereye yazılacağını seçin. Yine, yolu ortamınıza uygun şekilde güncelleyin.

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### Adım 3: A4 Sayfa Ayarlarıyla Kaydedin

Bir `PdfSaveOptions` örneği oluşturun, **A4** sayfa boyutunu (yaygın bir ABD kağıt formatı) ayarlayın ve `kaydet` komutunu çalıştırın. Bu, Aspose.Note'un yerleşik yardımcılarını kullanarak **PDF sayfa boyutunu özelleştirmeyi** göstermektedir.

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

> **İpucu:** Kenar boşluklarını veya yönlendirmeyi ayarlamanız gerekir, `PageSettings` üzerindeki ek özellikleri inceleyin.

## Yükseklik Sınırı Olmadan A4 Sayfa Ayarlarıyla PDF Nasıl Kaydedilir

### Adım 1: OneNote Belgesini Yükleyin

Yükleme adımı A4 senaryosu için aynıdır.

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### Adım 2: Hedef Yolu Tanımlayın

Önceki PDF'nin üzerine yazılmasını önlemek için farklı bir dosya adı sağlayın.

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### Adım 3: A4 Sayfa Ayarlarıyla Kaydet (Yükseklik Sınırı Yok)

Burada, uzun notlar veya kaydırılabilir içerik için mükemmel olan, dikey olarak otomatik olarak genişleyen bir PDF oluşturmak için `PageSettings.getA4NoHeightLimit()` kullanıyoruz.

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

> **Neden önemli:** **A4 boyutunda sınırlanmayan** seçeneği içeriğinin kesilmesini önler, OneNote'un uzunluğunun uzunluğunun tümünün PDF'de görünmesini sağlar.

## Yaygın Sorunlar ve Çözümler

| Sorun | Nedenleri | Çözüm |
|----------|-----|-----|
| **Boş PDF çıktısı** | Kaynak dosya yolu hatalı veya dosyaya erişilemiyor. | Yolu doğrulayın ve dosyanın mevcut olduğundan emin olun. |
| **Sayfa boyutu uygulanmadı** | `PdfSaveOptions` `save` şasisine bağlanmamış. | `seçenekler` nesnesini `oneFile.save()``e devam edebileceğinizden emin olun. |
| **Büyük notlar için süre sınırı** | Çok büyük `.one` eklenti yığınını (yığın) kapatabilir. | JVM veri değişimini (`-Xmx`) artırın veya dosyaları daha küçük partilerde işleyin. |

## Sıkça Sorulan Sorular

**S: Sayfanın düzeni, örnek kenarları veya yönlendirme gibi, daha da özelleştirilebilir mi?**
C: Evet, `PageSettings`in kenarları, yönlendirme ve DPI için özellikler sunar. Özel bir `PageSettings` nesnesi oluşturup `PdfSaveOptions`a atayabilirsiniz.

**S: **OneNote'u PDF'ye dönüştürmeyi** toplu bir işlemde nasıl birleştirilsin?**
C: Dosya yolu koleksiyonunda döngü oluşturma, biri için bir `Document` örneği oluşturma ve istediğiniz `PdfSaveOptions` ile `save` yöntemini çağırma. Bu, yukarıda belirtilen kodu desenini tekrar kullanır.

**S: Aspose.Note PDF dışarıdaki diğer taşınabilir formatlarını mı taşıyor?**
C: elbette. İlgili `SaveOptions` sınıflarını kullanarak HTML, XPS veya PNG ve JPEG gibi çeşitli görüntü formatlarına aktarabilirsiniz.

**S: **OneNote belgesi PDF**'yi gömülü yazı tipleriyle birlikte dağıtmanın bir yolu var mı?**
C: Kaydetmeden önce `PdfSaveOptions` örneğinde `options.setEmbedStandardFonts(true)` ayarlayın.

**S: Üretim kullanımında lisanslama hususları var mı?**
C: Değerlendirme için ücretsiz bir deneme mevcuttur, ancak üretim ortamlarında mevcut olması için ticari lisans gereklidir.

## Çözüm

Artık Aspose.Note for Java kullanarak OneNote dosyalarından **PDF nasıl kaydedilir** konusunda tam sayfa boyutu kontrolüne sahipsiniz — standart Letter düzeni ya da içeriğinizle birlikte büyüyen A4 sayfası ihtiyacınız olsun. Bu kod parçacıklarını mevcut Java uygulamalarınıza entegre ederek belge dönüşümünü otomatikleştirebilir, yazdırılabilir raporlar oluşturabilir veya OneNote defterlerini PDF olarak arşivleyebilirsiniz.

---

**Son Güncelleme:** 2025-12-17  
**Test Edilen Sürüm:** Aspose.Note for Java 23.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}