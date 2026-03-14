---
date: 2026-03-14
description: Java'da TIFF JPEG sıkıştırması, TIFF PackBits sıkıştırması veya CCITT
  Group 3 Fax kullanarak OneNote belgelerini TIFF dosyaları olarak nasıl kaydedeceğinizi
  öğrenin. Aspose.Note ile görüntü kalitesini, dosya boyutunu ve renk modunu kontrol
  edin.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: OneNote'ta TIFF JPEG Sıkıştırması Kullanarak TIFF Görüntüsü Kaydet
url: /tr/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

? Should translate header as well. Let's translate to "Sorun" and "Çözüm". We'll keep markdown table.

Make sure code block placeholders remain as is.

Now produce final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta TIFF JPEG Sıkıştırma Kullanarak TIFF Görüntüsü Kaydetme

## Giriş

Bu öğreticide **OneNote belgesini TIFF JPEG sıkıştırması kullanarak bir TIFF dosyasına nasıl kaydedeceğinizi** ve iki diğer popüler sıkıştırma yöntemini keşfedeceksiniz. Gerekli kurulumu adım adım gösterecek, gerekli Java paketlerini içe aktaracak ve her sıkıştırma seçeneği için net adım‑adım kod sağlayacağız. Sonunda **TIFF görüntü kalitesini** kontrol edebilecek, dosya boyutunu azaltabilecek ve hatta faks‑stili çıktı için siyah‑beyaz TIFF'ler oluşturabileceksiniz.

## Hızlı Yanıtlar
- **TIFF JPEG sıkıştırması nedir?** Görsel kaliteyi korurken TIFF dosya boyutunu azaltan kayıplı bir sıkıştırma yöntemi.  
- **Dönüşümü hangi kütüphane yönetir?** Aspose.Note for Java.  
- **Lisans gerekli mi?** Test için ücretsiz deneme sürümü çalışır; üretim için bir lisans gereklidir.  
- **Görüntü kalitesini değiştirebilir miyim?** Evet, `ImageSaveOptions` üzerindeki `quality` özelliğini ayarlayın.  
- **Toplu dönüşüm mümkün mü?** Kesinlikle – belgeler arasında döngü kurup aynı seçenekleri uygulayın.

## TIFF JPEG Sıkıştırması Nedir?
TIFF JPEG sıkıştırması, görüntü verilerini bir TIFF konteynerinde saklar ancak dosyayı küçültmek için JPEG’in kayıplı algoritmasını uygular. **tiff görüntü kalitesi** ile daha küçük dosya boyutu arasında bir denge gerektiğinde, özellikle web veya arşiv senaryolarında idealdir.

## Farklı TIFF Sıkıştırma Türlerini Neden Kullanmalı?
- **JPEG** – Fotoğraflar için iyidir; ayarlanabilir kalite sunar.  
- **PackBits** – Basit, kayıpsız koşu‑uzunluğu kodlaması; büyük tekdüze alanlara sahip grafikler için faydalıdır.  
- **CCITT Group 3 Fax** – Sadece siyah‑beyaz; taranmış belgeler ve faks iletimi için mükemmeldir.  

Doğru sıkıştırmayı seçmek, uygulamanız için gereken görsel doğruluğu kaybetmeden depolama kısıtlamalarını karşılamanızı sağlar.

## Aspose.Note Kullanarak One'ı TIFF'e Dönüştürme
Eğer amacınız **OneNote'u TIFF'e dönüştürmek** ise, aşağıdaki üç yöntem en yaygın senaryoları kapsar. Her yöntem bir `.one` dosyasını yükler, `ImageSaveOptions` yapılandırır ve sonucu bir `.tiff` dosyası olarak kaydeder.

## Önkoşullar

- Java Development Kit (JDK) yüklü.  
- Aspose.Note for Java kütüphanesi projenize eklenmiş (Maven/Gradle ya da manuel JAR).  
- Java sözdizimi hakkında temel bilgi.

## Paketleri İçe Aktarma

İlk olarak, gerekli Aspose.Note sınıflarını Java dosyanıza ekleyin:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Adım 1: TIFF JPEG Sıkıştırması Kullanarak TIFF'e Kaydetme

Aşağıda, bir OneNote dosyasını yükleyen ve JPEG sıkıştırmasıyla TIFF olarak kaydeden tam yöntem yer almaktadır. **tiff görüntü kalitesi** kontrolü için `quality` değerini (0‑100) ayarlayın.

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

- `ImageSaveOptions`, Aspose.Note'a bir TIFF dosyası çıkışı vermesini söyler.  
- `setTiffCompression(TiffCompression.Jpeg)`, JPEG sıkıştırmasını seçer.  
- `setQuality(93)` (isteğe bağlı) görüntü kalitesini ince ayarlar; daha düşük değerler daha küçük dosyalar üretir.

### Java'da JPEG Sıkıştırmasıyla TIFF Nasıl Kaydedilir
1. `dataDir`'i `.one` dosyanızın bulunduğu klasöre yönlendirin.  
2. `SaveToTiffUsingJpegCompression()` metodunu ana metodunuzdan ya da servisten çağırın.  
3. Oluşan `.tiff` dosyası aynı dizinde görünecektir.

## TIFF PackBits Sıkıştırma Genel Bakışı

PackBits, büyük tek renkli alanlara sahip görüntülerde en iyi çalışan kayıpsız bir sıkıştırma algoritmasıdır. Belgelerde genellikle **tiff packbits compression** olarak adlandırılır.

## Adım 2: PackBits Sıkıştırması Kullanarak TIFF'e Kaydetme

Kayıpsız bir seçenek gerekiyorsa, PackBits, tek renkli grafiklerde iyi çalışan basit bir koşu‑uzunluğu algoritmasıdır.

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

- `setTiffCompression(TiffCompression.PackBits)`, sıkıştırma yöntemini değiştirir.  
- PackBits kayıpsız olduğu için kalite ayarı gerekmez.

## Adım 3: CCITT Group 3 Fax Sıkıştırması (Siyah‑Beyaz TIFF) Kullanarak TIFF'e Kaydetme

Faks‑stili belgeler için genellikle **siyah beyaz TIFF** istersiniz. CCITT Group 3, tek renkli görüntüler için yüksek sıkıştırma sağlar.

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

- `setColorMode(ColorMode.BlackAndWhite)`, tek renkli bir çıktı zorlar.  
- `setTiffCompression(TiffCompression.Ccitt3)`, faks‑odaklı sıkıştırmayı uygular.

## Yaygın Sorunlar ve İpuçları

| Sorun | Çözüm |
|-------|----------|
| **Çıktı dosyası beklenenden büyük** | JPEG `quality` değerini düşürmeyi deneyin veya kayıpsız kabul ediliyorsa PackBits'e geçin. |
| **Renkler soluk görünüyor** | `ColorMode.BlackAndWhite`'ı tam renk gerektiğinde yanlışlıkla ayarlamadığınızdan emin olun. |
| **Desteklenmeyen görüntü formatı hatası** | Aspose.Note'un son sürümünü kullandığınızdan emin olun; eski sürümler belirli sıkıştırma enum'larını içermeyebilir. |
| **Çalışma zamanında LicenseException** | Geçerli bir Aspose.Note lisansı kurun (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Sıkça Sorulan Sorular

**S:** Bu seçeneklerle diğer belge türlerini (ör. PDF, DOCX) TIFF'e dönüştürebilir miyim?  
**C:** Evet. Aspose.Note OneNote dosyalarına odaklansa da, Aspose.PDF, Aspose.Words ve diğer kütüphaneler kendi formatları için benzer `ImageSaveOptions` sunar.

**S:** TIFF JPEG sıkıştırması standart JPEG dosyasından nasıl farklıdır?  
**C:** JPEG algoritması aynı, ancak görüntü verileri bir TIFF konteyneri içinde bulunur; bu konteyner birden fazla sayfa ve daha zengin meta veriler tutabilir.

**S:** Birçok `.one` dosyasını toplu işleyebilir miyim?  
**C:** Kesinlikle. Bir dizini döngüyle gezip, her dosya için üç yöntemden birini çağırın ve ortaya çıkan TIFF'leri toplayın.

**S:** Çıktı TIFF'in DPI/çözünürlüğünü kontrol edebilir miyim?  
**C:** Evet. Kaydetmeden önce `options.setResolution(int dpi)` kullanın.

**S:** Aspose.Note asenkron işleme destek veriyor mu?  
**C:** API kendisi senkroniktir, ancak çağrıları Java’nın `CompletableFuture` veya bir iş parçacığı havuzu ile paralel yürütme için sarmalayabilirsiniz.

## Sonuç

Artık JPEG, PackBits veya CCITT Group 3 Fax sıkıştırması kullanarak OneNote belgelerini TIFF dosyaları olarak kaydetmenizi sağlayan eksiksiz bir **java tiff conversion** araç setine sahipsiniz. Kaliteyi, renk modunu ve çözünürlüğü belirli **tiff görüntü kalitesi** gereksinimlerinize göre ayarlayın ve bu yöntemleri toplu iş akışlarına entegre ederek maksimum verimlilik elde edin.

---

**Last Updated:** 2026-03-14  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}