---
date: 2025-12-17
description: Java'da TIFF JPEG sıkıştırması, PackBits veya CCITT Group 3 Fax kullanarak
  OneNote belgelerini TIFF dosyaları olarak kaydetmeyi öğrenin. Aspose.Note ile görüntü
  kalitesini, dosya boyutunu ve renk modunu kontrol edin.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: OneNote'ta TIFF JPEG Sıkıştırmasıyla TIFF Görüntüsü Kaydet
url: /tr/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta TIFF JPEG Sıkıştırması Kullanarak TIFF Görüntüsü Kaydetme

## Giriş

Bu öğreticide **OneNote belgesini TIFF JPEG sıkıştırmasıyla bir TIFF dosyasına nasıl kaydedeceğinizi** ve iki diğer popüler sıkıştırma yöntemini keşfedeceksiniz. Gerekli ayarları adım adım inceleyecek, gerekli Java paketlerini içe aktaracak ve her sıkıştırma seçeneği için net adım‑adım kod örnekleri sunacağız. Sonunda **TIFF görüntü kalitesini** kontrol edebilecek, dosya boyutunu azaltabilecek ve hatta faks‑stili çıktı için siyah‑beyaz TIFF'ler üretebileceksiniz.

## Hızlı Yanıtlar
- **TIFF JPEG sıkıştırması nedir?** Görsel kaliteyi korurken TIFF dosya boyutunu azaltan kayıplı bir sıkıştırma yöntemidir.  
- **Dönüşümü hangi kütüphane gerçekleştiriyor?** Aspose.Note for Java.  
- **Lisans gerekir mi?** Test için ücretsiz deneme sürümü yeterlidir; üretim için lisans gereklidir.  
- **Görüntü kalitesini değiştirebilir miyim?** Evet, `ImageSaveOptions` üzerindeki `quality` özelliğini ayarlayın.  
- **Toplu dönüşüm mümkün mü?** Kesinlikle – belgeler üzerinden döngü kurup aynı seçenekleri uygulayabilirsiniz.

## TIFF JPEG Sıkıştırması Nedir?
TIFF JPEG sıkıştırması, görüntü verilerini TIFF konteynerinde saklarken dosyayı küçültmek için JPEG’in kayıplı algoritmasını uygular. Web veya arşiv senaryoları gibi **tiff görüntü kalitesi** ile daha küçük dosya boyutu arasında denge gerektiğinde idealdir.

## Farklı TIFF Sıkıştırma Türlerini Neden Kullanmalı?
- **JPEG** – Fotoğraflar için uygundur; ayarlanabilir kalite sunar.  
- **PackBits** – Basit, kayıpsız koşu‑uzunluğu kodlaması; büyük tekdüze alanları olan grafikler için faydalıdır.  
- **CCITT Group 3 Fax** – Yalnızca siyah‑beyaz; taranmış belgeler ve faks iletimi için mükemmeldir.  

Doğru sıkıştırmayı seçmek, uygulamanız için gereken görsel sadakati kaybetmeden depolama kısıtlamalarını karşılamanızı sağlar.

## Ön Koşullar

- Java Development Kit (JDK) yüklü.  
- Projenize Aspose.Note for Java kütüphanesi eklenmiş (Maven/Gradle ya da manuel JAR).  
- Java sözdizimine temel aşinalık.

## Paketleri İçe Aktarma

İlk olarak, gerekli Aspose.Note sınıflarını Java dosyanıza getirin:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Adım 1: TIFF JPEG Sıkıştırması Kullanarak TIFF Kaydetme

Aşağıda, bir OneNote dosyasını yükleyen ve JPEG sıkıştırmasıyla TIFF olarak kaydeden tam yöntem yer alıyor. **tiff görüntü kalitesi**ni kontrol etmek için `quality` değerini (0‑100) ayarlayın.

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Açıklama**

- `ImageSaveOptions`, Aspose.Note’a bir TIFF dosyası üretmesini söyler.  
- `setTiffCompression(TiffCompression.Jpeg)` JPEG sıkıştırmasını seçer.  
- `setQuality(93)` (isteğe bağlı) görüntü kalitesini ince ayarlar; düşük değerler daha küçük dosyalar üretir.

### Java’da JPEG Sıkıştırmasıyla TIFF Nasıl Kaydedilir
1. `dataDir` değişkenini `.one` dosyanızın bulunduğu klasöre yönlendirin.  
2. `SaveToTiffUsingJpegCompression()` metodunu ana metodunuzdan ya da servisinizden çağırın.  
3. Oluşan `.tiff` dosyası aynı dizinde görünecektir.

## Adım 2: PackBits Sıkıştırması Kullanarak TIFF Kaydetme

Kayıpsız bir seçenek gerekiyorsa, PackBits basit bir koşu‑uzunluğu algoritmasıdır ve katı renkli grafiklerde iyi çalışır.

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Açıklama**

- `setTiffCompression(TiffCompression.PackBits)` sıkıştırma yöntemini değiştirir.  
- PackBits kayıpsız olduğundan kalite ayarı gerekmez.

## Adım 3: CCITT Group 3 Fax Sıkıştırması (Siyah‑Beyaz TIFF) Kullanarak TIFF Kaydetme

Faks‑stili belgeler için genellikle **siyah‑beyaz TIFF** istenir. CCITT Group 3, tek renkli görüntüler için yüksek sıkıştırma sağlar.

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Açıklama**

- `setColorMode(ColorMode.BlackAndWhite)` tek renkli çıktıyı zorlar.  
- `setTiffCompression(TiffCompression.Ccitt3)` faks‑odaklı sıkıştırmayı uygular.

## Yaygın Sorunlar ve İpuçları

| Sorun | Çözüm |
|-------|----------|
| **Çıktı dosyası beklenenden büyük** | JPEG `quality` değerini düşürmeyi deneyin veya kayıpsız kabul ediliyorsa PackBits’e geçin. |
| **Renkler soluk görünüyor** | Renkli ihtiyacınız varsa `ColorMode.BlackAndWhite` ayarını yanlışlıkla yapmadığınızdan emin olun. |
| **Desteklenmeyen görüntü formatı hatası** | Aspose.Note’un güncel bir sürümünü kullandığınızdan emin olun; eski sürümler bazı sıkıştırma enum’larını içermeyebilir. |
| **LicenseException çalışma zamanında** | Geçerli bir Aspose.Note lisansı kurun (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Sık Sorulan Sorular

**S: Bu seçeneklerle diğer belge türlerini (ör. PDF, DOCX) TIFF’e dönüştürebilir miyim?**  
C: Evet. Aspose.Note OneNote dosyalarına odaklanır, ancak Aspose’un diğer kütüphaneleri (PDF, Words) kendi formatları için benzer `ImageSaveOptions` sunar.

**S: TIFF JPEG sıkıştırması standart JPEG dosyalarından nasıl farklıdır?**  
C: Görüntü verisi bir TIFF konteyneri içinde saklanır, meta verileri korunur ve birden fazla sayfa desteklenir; sıkıştırma algoritması ise JPEG’dir.

**S: Birden çok `.one` dosyasını toplu işleyebilir miyim?**  
C: Kesinlikle. Bir klasörü döngüyle gezerek her dosya için üç yöntemden birini çağırabilir ve ortaya çıkan TIFF’leri toplayabilirsiniz.

**S: Çıktı TIFF’in DPI/çözünürlüğünü kontrol edebilir miyim?**  
C: Evet. Kaydetmeden önce `options.setResolution(int dpi)` kullanın.

**S: Aspose.Note asenkron işleme destekliyor mu?**  
C: API kendisi senkron çalışır, ancak çağrıları Java’nın `CompletableFuture` veya iş parçacığı havuzlarıyla sarmalayarak paralel yürütme sağlayabilirsiniz.

## Sonuç

Artık **java tiff conversion** araç setinizle OneNote belgelerini JPEG, PackBits veya CCITT Group 3 Fax sıkıştırması kullanarak TIFF dosyalarına kaydedebiliyorsunuz. Kalite, renk modu ve çözünürlüğü ihtiyacınıza göre ayarlayın, toplu iş akışlarına entegre edin ve **tiff görüntü kalitesi** gereksinimlerinizi en verimli şekilde karşılayın.

---

**Son Güncelleme:** 2025-12-17  
**Test Edilen Versiyon:** Aspose.Note for Java 23.12 (yazım anındaki en yeni)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}