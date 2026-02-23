---
date: 2026-02-23
description: Otsu yöntemi Java'yı kullanarak OneNote'u Aspose.Note for Java ile ikili
  PNG görüntüsü olarak kaydetmeyi öğrenin. Bu kılavuz Otsu ikilileştirmeyi, PNG dışa
  aktarmayı ve OCR için hazır siyah‑beyaz görüntüleri kapsar.
linktitle: How to Save OneNote as Binary Image Using Otsu Method
second_title: Aspose.Note Java API
title: Otsu yöntemi Java ile OneNote'u ikili görüntü olarak kaydetme
url: /tr/java/onenote-document-saving/save-to-binary-image-using-otsu-method/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Otsu Yöntemi Kullanarak İkili Görüntü Kaydetme

## Giriş

Bu öğreticide **Otsu yöntemi Java** kullanarak bir OneNote belgesini hafif bir ikili PNG görüntüsüne nasıl dönüştüreceğinizi öğreneceksiniz. OCR ön işleme hattı oluşturuyor, notları arşivliyor ya da sadece hızlı bir görsel küçük resim ihtiyacınız varsa, Otsu algoritması sadece birkaç satır kodla optimal siyah‑beyaz render sağlar.

## Hızlı Yanıtlar
- **Otsu yöntemi ne yapar?** Gri tonlamalı bir görüntüyü siyah‑beyaz (ikili) bir görüntüye dönüştürmek için optimal eşik değerini otomatik olarak belirler.  
- **Çıktı için hangi format kullanılır?** PNG varsayılan formattır çünkü kayıpsız kaliteyi korur.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü yeterlidir; üretim ortamı için ticari lisans gereklidir.  
- **Çıktıyı başka bir formata değiştirebilir miyim?** Evet – `SaveFormat.Png` ifadesini desteklenen başka bir formatla değiştirmeniz yeterlidir.  
- **Bu OCR için uygun mu?** Kesinlikle – ikili görüntüler gri tonlama gürültüsünü ortadan kaldırarak OCR doğruluğunu artırır.

## Otsu Yöntemi Nedir?
Otsu yöntemi, bir gri tonlamalı görüntünün histogramını analiz eder ve sınıf içi varyansı en aza indirecek eşik değerini seçer; böylece ön plan (siyah) ile arka plan (beyaz) etkili bir şekilde ayrılır. Bu, OneNote sayfalarından **black‑white image Java** çıktıları oluşturmak için idealdir.

## Neden Otsu Method Java’yı İkili Görüntü Dönüştürme İçin Kullanmalısınız?
- **Evrensel uyumluluk:** PNG, tarayıcılar, mobil uygulamalar ve masaüstü araçları arasında sorunsuz çalışır.  
- **Kayıpsız sıkıştırma:** Kalite kaybı olmaz, bu da sonraki işlemler için kritiktir.  
- **OCR‑hazır çıktı:** İkili PNG'ler çoğu OCR motoru için tercih edilen girdi olup tanıma oranlarını artırır.  
- **Minimum kod izi:** Aspose.Note ile Otsu ikileştirmesini sadece birkaç API çağrısıyla uygulayabilirsiniz.

## Ön Koşullar
1. Java programlamaya temel düzeyde hakimiyet.  
2. JDK (Java Development Kit) kurulu.  
3. Projeye eklenmiş Aspose.Note for Java kütüphanesi (Maven/Gradle ya da manuel JAR).  

## Paketleri İçe Aktarma
Başlamak için gerekli Aspose.Note sınıflarını ve Java I/O yardımcılarını içe aktarın.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Adım 1: OneNote Belgesini Yükleyin
Öncelikle `.one` dosyanızın bulunduğu klasöre işaret edin ve belgeyi `Document` nesnesine yükleyin.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Adım 2: Otsu ile İkileştirmeyi Yapılandırın
Bir `ImageBinarizationOptions` örneği oluşturun ve Aspose.Note’a Otsu algoritmasını kullanmasını söyleyin.

```java
dataDir = dataDir + "SaveToBinaryImageUsingOtsuMethod_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.Otsu);
```

## Adım 3: Görüntü Kaydetme Seçeneklerini Ayarlayın (PNG, Siyah‑Beyaz)
Görüntünün nasıl kaydedileceğini tanımlayın. Burada PNG seçiyoruz, siyah‑beyaz renk modunu zorunlu kılıyor ve ikileştirme seçeneklerini ekliyoruz.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## Adım 4: Belgeyi İkili Görüntü Olarak Kaydedin
Hazırladığınız seçenekleri kullanarak ikili PNG'yi diske yazın.

```java
// Save the document.
oneFile.save(dataDir, options);
```

## Yaygın Sorunlar ve İpuçları
- **Dosya bulunamadı:** `dataDir` değişkeninin dosya adı eklemeden önce bir yol ayırıcı (`/` veya `\\`) ile bittiğinden emin olun.  
- **Boş çıktı:** Kaynak OneNote sayfasının içerik içerdiğini kontrol edin; boş sayfalar boş bir PNG üretir.  
- **Performans:** Büyük defterlerde belleği düşük tutmak için sayfaları tek tek işleyin.

## Sonuç
Artık **Otsu yöntemi Java** kullanarak OneNote’u ikili PNG olarak kaydettiğinizi biliyorsunuz. Bu yaklaşım, OCR, arşivleme veya bir OneNote sayfasının hafif bir görsel kopyasına ihtiyaç duyulan herhangi bir senaryo için **black‑white image Java** varlıkları oluşturmak için mükemmeldir.

## SSS

### S1: Aspose.Note for Java’yı kullanarak OneNote belgelerinden metin çıkarabilir miyim?
**C1:** Evet, Aspose.Note for Java, OneNote belgelerinden programlı olarak metin içeriği çıkarmak için API'ler sağlar.

### S2: Aspose.Note for Java farklı OneNote dosya sürümleriyle uyumlu mu?
**C2:** Evet, Aspose.Note for Java .one ve .onenote formatları dahil olmak üzere çeşitli OneNote dosya sürümlerini destekler.

### S3: Belgeleri ikili görüntü olarak kaydederken ikileştirme seçeneklerini özelleştirebilir miyim?
**C3:** Kesinlikle, gereksinimlerinize göre ikileştirme yöntemini ve diğer seçenekleri ayarlayabilirsiniz.

### S4: Aspose.Note for Java ikili görüntüleri tekrar OneNote belgelerine dönüştürebilir mi?
**C4:** Aspose.Note esas olarak OneNote belgelerini manipüle eder; ancak görüntüleri OCR (Optik Karakter Tanıma) teknikleriyle OneNote formatına dönüştürebilirsiniz.

### S5: Aspose.Note for Java kullanırken sorun yaşarsam nereden destek alabilirim?
**C5:** Aspose.Note forumunu ziyaret edebilir veya teknik sorunlar ve sorular için destek ekipleriyle iletişime geçebilirsiniz.

## Ek Sık Sorulan Sorular

**S: Çıktı formatını PNG’den JPEG’e nasıl değiştiririm?**  
C: `ImageSaveOptions` yapıcısında `SaveFormat.Png` ifadesini `SaveFormat.Jpeg` ile değiştirin.

**S: Dışa aktarılan görüntü için özel DPI ayarlamak mümkün mü?**  
C: `save` metodunu çağırmadan önce `options.setResolution(double dpi)` kullanın.

**S: Birden fazla OneNote sayfasını döngü içinde işleyebilir miyim?**  
C: Kesinlikle – `Document.getPages()` üzerinden döngü kurup aynı kaydetme mantığını her sayfaya uygulayın.

## Sık Sorulan Sorular

**S: Otsu algoritması tek mevcut ikileştirme yöntemi mi?**  
C: Hayır, Aspose.Note ayrıca FixedThreshold gibi diğer yöntemleri de destekler. `BinarizationMethod.FixedThreshold` ayarlayıp özel bir eşik değeri sağlayarak geçiş yapabilirsiniz.

**S: İkili PNG, OneNote sayfasındaki renkli notları korur mu?**  
C: Hayır. `ColorMode.BlackAndWhite` etkinleştirildiğinde, tüm renkler Otsu eşiğine göre saf siyah veya beyaz olarak dönüştürülür.

**S: Bir OneNote dosyası ne kadar büyük olursa bellek sorunları başlar?**  
C: Bu, JVM heap boyutunuza bağlıdır. 200 MB üzerindeki defterler için sayfaları tek tek işlemek ve her kaydetmeden sonra `System.gc()` çağırmak önerilir.

---

**Last Updated:** 2026-02-23  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}