---
date: 2025-12-14
description: Aspose.Note for Java ile Otsu yöntemi kullanarak OneNote'u ikili PNG
  görüntüsü olarak kaydetmeyi öğrenin. Bu kılavuz, OneNote'un PNG olarak kaydedilmesini
  ve Java'da siyah‑beyaz görüntüler oluşturulmasını kapsar.
linktitle: How to Save OneNote as Binary Image Using Otsu Method
second_title: Aspose.Note Java API
title: OneNote'u Otsu Yöntemiyle İkili Görüntü Olarak Kaydetme
url: /tr/java/onenote-document-saving/save-to-binary-image-using-otsu-method/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Otsu Yöntemiyle İkili Görüntü Olarak Kaydetme

## Giriş

Bu öğreticide **OneNote** belgelerini Aspose.Note for Java ile Otsu yöntemi kullanarak ikili (binary) görüntüler olarak nasıl kaydedeceğinizi keşfedeceksiniz. Bir OneNote dosyasını siyah‑beyaz görüntüye dönüştürmek, görüntü‑işleme boru hatları, OCR ön işleme veya notlarınızın hafif bir görsel temsiline ihtiyaç duyduğunuz durumlar için oldukça kullanışlıdır.

## Hızlı Yanıtlar
- **Otsu yöntemi ne yapar?** Gri tonlamalı bir görüntüyü siyah‑beyaz (ikili) bir görüntüye dönüştürmek için optimal eşik değerini otomatik olarak belirler.  
- **Çıktı hangi formatta olur?** PNG varsayılan formattır çünkü kayıpsız kaliteyi korur.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü yeterlidir; üretim ortamı için ticari lisans gereklidir.  
- **Çıktıyı başka bir formata değiştirebilir miyim?** Evet – `SaveFormat.Png` ifadesini desteklenen başka bir formatla değiştirmeniz yeterlidir.  
- **Bu OCR için uygun mu?** Kesinlikle – ikili görüntüler gri tonlama gürültüsünü ortadan kaldırarak OCR doğruluğunu artırır.

## Otsu Yöntemi Nedir?
Otsu yöntemi, bir gri tonlamalı görüntünün histogramını analiz eder ve sınıf içi varyansı en aza indirecek bir eşik değeri seçer; böylece ön plan (siyah) ile arka plan (beyaz) etkili bir şekilde ayrılır. Bu, **OneNote sayfalarından siyah beyaz görüntü java** çıktıları oluşturmak için idealdir.

## Neden OneNote PNG Olarak Kaydedilir?
- **Evrensel uyumluluk:** PNG tarayıcılar, mobil uygulamalar ve masaüstü araçları arasında sorunsuz çalışır.  
- **Kayıpsız sıkıştırma:** Kalite kaybı olmaz, bu da sonraki işlemler için kritiktir.  
- **OCR'a hazır:** İkili PNG'ler çoğu OCR motoru için tercih edilen girdi formatıdır.

## Önkoşullar
1. Java programlama temellerine hâkim olmak.  
2. JDK (Java Development Kit) yüklü olması.  
3. Projeye eklenmiş Aspose.Note for Java kütüphanesi (Maven/Gradle ya da manuel JAR).

## Paketleri İçe Aktarma
Başlamak için gerekli Aspose.Note sınıflarını ve Java I/O yardımcılarını içe aktarın.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Adım 1: OneNote Belgesini Yükleme
Öncelikle `.one` dosyanızın bulunduğu klasöre işaret edin ve belgeyi `Document` nesnesine yükleyin.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Adım 2: Otsu ile İkilileştirmeyi Yapılandırma
Bir `ImageBinarizationOptions` örneği oluşturun ve Aspose.Note'a Otsu algoritmasını kullanmasını söyleyin.

```java
dataDir = dataDir + "SaveToBinaryImageUsingOtsuMethod_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.Otsu);
```

## Adım 3: Görüntü Kaydetme Seçeneklerini Ayarlama (PNG, Siyah‑Beyaz)
Görüntünün nasıl kaydedileceğini tanımlayın. Burada PNG seçiyoruz, siyah‑beyaz renk modunu zorunlu kılıyor ve ikilileştirme seçeneklerini ekliyoruz.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## Adım 4: Belgeyi İkili Görüntü Olarak Kaydetme
Son olarak, hazırladığınız seçeneklerle ikili PNG'yi diske yazın.

```java
// Save the document.
oneFile.save(dataDir, options);
```

## Yaygın Sorunlar ve İpuçları
- **Dosya bulunamadı:** `dataDir` değişkeninin dosya adı eklemeden önce bir yol ayırıcı (`/` veya `\\`) ile bittiğini kontrol edin.  
- **Boş çıktı:** Kaynak OneNote sayfasının içerik içerdiğinden emin olun; boş sayfalar boş bir PNG üretir.  
- **Performans:** Büyük defterlerde bellek kullanımını düşük tutmak için sayfaları tek tek işleyin.

## Sonuç
Artık **OneNote** belgelerini Java'da Otsu yöntemiyle ikili PNG görüntüsü olarak nasıl kaydedeceğinizi biliyorsunuz. Bu yöntem, **siyah beyaz görüntü java** varlıklarını OCR, arşivleme veya OneNote sayfasının hafif bir görsel kopyasına ihtiyaç duyulan herhangi bir senaryo için oluşturmakta mükemmeldir.

## SSS

### S1: Aspose.Note for Java kullanarak OneNote belgelerinden metin çıkarabilir miyim?

C1: Evet, Aspose.Note for Java, OneNote belgelerinden programlı olarak metin içeriği çıkarmak için API'ler sunar.

### S2: Aspose.Note for Java farklı OneNote dosya sürümleriyle uyumlu mu?

C2: Evet, Aspose.Note for Java .one ve .onenote formatları dahil olmak üzere çeşitli OneNote dosya sürümlerini destekler.

### S3: Belgeleri ikili görüntü olarak kaydederken ikilileştirme seçeneklerini özelleştirebilir miyim?

C3: Kesinlikle, gereksinimlerinize göre ikilileştirme yöntemini ve diğer seçenekleri ayarlayabilirsiniz.

### S4: Aspose.Note for Java ikili görüntüleri OneNote belgelerine geri dönüştürmeyi destekliyor mu?

C4: Aspose.Note esas olarak OneNote belgeleriyle çalışır; ancak görüntüleri OCR (Optik Karakter Tanıma) teknikleriyle OneNote formatına dönüştürebilirsiniz.

### S5: Aspose.Note for Java kullanırken sorun yaşarsam nereden destek alabilirim?

C5: Aspose.Note forumunu ziyaret edebilir veya teknik sorunlar ve sorular için destek ekipleriyle iletişime geçebilirsiniz.

## Ek Sık Sorulan Sorular

**S: Çıktı formatını PNG'den JPEG'e nasıl değiştiririm?**  
C: `ImageSaveOptions` yapıcısında `SaveFormat.Png` ifadesini `SaveFormat.Jpeg` ile değiştirin.

**S: Dışa aktarılan görüntü için özel bir DPI ayarlama imkanı var mı?**  
C: Evet, `save` metodunu çağırmadan önce `options.setResolution(double dpi)` kullanın.

**S: Birden fazla OneNote sayfasını döngü içinde işleyebilir miyim?**  
C: Kesinlikle – `Document.getPages()` üzerinden döngü kurarak aynı kaydetme mantığını her sayfaya uygulayabilirsiniz.

---

**Son Güncelleme:** 2025-12-14  
**Test Edilen Versiyon:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
