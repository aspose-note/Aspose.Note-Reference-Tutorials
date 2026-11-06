---
date: 2026-11-05
description: Aspose.Note kullanarak Java'da OneNote defterlerini TIFF'e dönüştürürken
  TIFF dosya boyutunu nasıl azaltacağınızı öğrenin. JPEG, PackBits ve siyah-beyaz
  TIFF seçeneklerini içerir.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Java'da OneNote dönüştürürken TIFF dosya boyutunu nasıl azaltılır
og_description: Aspose.Note kullanarak Java'da OneNote defterlerini TIFF'e dönüştürürken
  TIFF dosya boyutunu nasıl azaltacağınızı öğrenin. JPEG, PackBits ve siyah-beyaz
  TIFF seçeneklerini içerir.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Java'da OneNote dönüştürürken TIFF dosya boyutunu nasıl azaltılır
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Java'da OneNote dönüştürürken TIFF dosya boyutunu nasıl azaltılır
url: /tr/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u Java'da TIFF'a dönüştürürken TIFF dosya boyutunu nasıl azaltabilirsiniz

## Giriş

Bu öğreticide, Aspose.Note for Java kullanarak OneNote defterlerini TIFF görüntülerine dönüştürürken **TIFF dosya boyutunu azaltmayı** keşfedeceksiniz. Üç sıkıştırma yöntemi—TIFF JPEG, PackBits ve CCITT Group 3 (siyah‑beyaz TIFF)—üzerinden geçecek, görüntü kalitesini nasıl ayarlayacağınızı, renk modunu kontrol edeceğinizi ve dosya boyutlarını web, arşivleme veya faks‑tipi senaryoları için optimal tutmayı göstereceğiz.

## Hızlı cevaplar
- **TIFF JPEG sıkıştırması nedir?** Görsel kaliteyi korurken TIFF dosya boyutunu azaltan kayıplı bir sıkıştırma yöntemi.  
- **Dönüşümü hangi kütüphane gerçekleştiriyor?** Aspose.Note for Java.  
- **Lisans gerekir mi?** Test için ücretsiz deneme sürümü çalışır; üretim için lisans gereklidir.  
- **Görüntü kalitesini değiştirebilir miyim?** Evet, `ImageSaveOptions` üzerindeki `quality` özelliğini ayarlayın.  
- **Toplu dönüşüm mümkün mü?** Kesinlikle – belgeler üzerinde döngü kurarak aynı seçenekleri uygulayabilirsiniz.

## TIFF JPEG sıkıştırması genel bakışı

TIFF JPEG sıkıştırması, görüntü verilerini bir TIFF konteynerinde saklar ancak dosyayı küçültmek için JPEG’in kayıplı algoritmasını uygular. Web veya arşiv senaryoları için **tiff görüntü kalitesi** ile daha küçük dosya boyutu arasında denge kurmanız gerektiğinde idealdir.

## Farklı TIFF sıkıştırma türlerini neden kullanmalısınız?

İçerik ve depolama ihtiyaçlarına göre sıkıştırma türünü seçersiniz: JPEG fotoğraflar için en iyisidir, PackBits büyük tekdüze alanlara sahip grafikler için kayıpsız sıkıştırma sağlar ve CCITT Group 3 monokrom faks‑stil belgeler için yüksek oranlı sıkıştırma sunar. Doğru yöntemi seçmek, uygulamanızın gerektirdiği görsel sadakati kaybetmeden **TIFF dosya boyutunu azaltmanıza** olanak tanır.

## Doğru sıkıştırmayı seçmek

- **JPEG** – 0‑100 arasında ayarlanabilir kalite, boyut ile detay arasında bir denge kurmanıza izin verir, renk‑zengin sayfalar için mükemmeldir.  
- **PackBits** – Kayıpsız koşu‑uzunluğu kodlaması; her pikseli tam olarak korumanız gerektiğinde idealdir.  
- **CCITT Group 3** – Yalnızca monokrom; taranmış metin veya faks belgeleri için sıkıştırmayı maksimize eder.  

## Aspose.Note kullanarak OneNote'u TIFF'a dönüştürmek

Amacınız **OneNote'u TIFF'a dönüştürmek** ise, aşağıdaki üç yöntem en yaygın senaryoları kapsar. Her yöntem bir `.one` dosyasını yükler, `ImageSaveOptions` yapılandırır ve sonucu bir `.tiff` dosyası olarak kaydeder.

## Önkoşullar

- Java Development Kit (JDK) yüklü.  
- Projenize Aspose.Note for Java kütüphanesi eklenmiş (Maven/Gradle veya manuel JAR).  
- Java sözdizimine temel aşinalık.

## Paketleri içe aktarın

`ImageSaveOptions`, `TiffCompression` ve `ColorMode` sınıfları dönüşüm API'sinin çekirdeğini oluşturur.  

`ImageSaveOptions` görüntüleri kaydetme seçeneklerini, örneğin format ve sıkıştırma, tanımlar.  
`TiffCompression` desteklenen TIFF sıkıştırma algoritmalarını listeler.  
`ColorMode` renk derinliğini belirtir, örneğin renkli veya siyah‑beyaz.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Adım 1: TIFF JPEG sıkıştırmasıyla TIFF kaydetme

### Java'da JPEG sıkıştırmasıyla TIFF kaydetme

OneNote dosyasını yükleyin, `ImageSaveOptions`'ı JPEG sıkıştırmasıyla yapılandırın, isteğe bağlı olarak `quality` değerini ayarlayın ve kaydetme metodunu çağırın. Bu iki‑adımlı desen, çıktı boyutu ve görsel sadakat üzerinde tam kontrol sağlar.

1. `dataDir` değişkenini `.one` dosyanızın bulunduğu klasöre yönlendirin.  
2. `SaveToTiffUsingJpegCompression()` metodunu ana metodunuzdan veya servisinizden çağırın.  
3. Oluşan `.tiff` dosyası aynı dizinde görünecektir.

```java
// Placeholder for the JPEG compression method implementation
```

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

- `ImageSaveOptions` Aspose.Note'a bir TIFF dosyası üretmesini söyler.  
- `setTiffCompression(TiffCompression.Jpeg)` JPEG sıkıştırmasını seçer.  
- `setQuality(93)` (isteğe bağlı) görüntü kalitesini ince ayarlar; düşük değerler daha küçük dosyalar üretir.

## TIFF PackBits sıkıştırması genel bakışı

PackBits, büyük tekdüze renk alanlarına sahip görüntülerde en iyi çalışan kayıpsız bir sıkıştırma algoritmasıdır. Belgelerde genellikle **tiff packbits compression** olarak adlandırılır.

## Java'da PackBits sıkıştırmasıyla TIFF kaydetme

Kayıpsız bir seçenek gerekiyorsa, PackBits basit bir koşu‑uzunluğu algoritmasıdır ve katı renkli grafiklerde iyi çalışır. `ImageSaveOptions`'ı `TiffCompression.PackBits` ile yapılandırın ve belgeyi kaydedin.

```java
// Placeholder for the PackBits compression method implementation
```

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
- PackBits kayıpsız olduğu için kalite ayarı gerekmez.

## Java'da CCITT Group 3 sıkıştırmasıyla TIFF kaydetme

Faks‑stil belgeler için genellikle **siyah‑beyaz TIFF** istenir. CCITT Group 3 monokrom görüntüler için yüksek sıkıştırma sağlar. Renk modunu siyah‑beyaz olarak ayarlayın ve CCITT 3 sıkıştırma enum'ını seçin.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

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

- `setColorMode(ColorMode.BlackAndWhite)` monokrom bir çıktı zorlar.  
- `setTiffCompression(TiffCompression.Ccitt3)` faks‑odaklı sıkıştırmayı uygular.

## Yaygın sorunlar & ipuçları

| Sorun | Çözüm |
|-------|----------|
| **Çıktı dosyası beklenenden büyük** | JPEG `quality` değerini düşürmeyi deneyin veya kayıpsız kabul ediliyorsa PackBits'e geçin. |
| **Renkler soluk görünüyor** | Tam renk gerektiğinde `ColorMode.BlackAndWhite`'ı yanlışlıkla ayarlamadığınızdan emin olun. |
| **Desteklenmeyen görüntü formatı hatası** | Aspose.Note'un güncel bir sürümünü kullandığınızı doğrulayın; eski sürümler bazı sıkıştırma enum'larını içermeyebilir. |
| **Runtime'da LicenseException** | Geçerli bir Aspose.Note lisansı kurun (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Sıkça sorulan sorular

**S: Bu seçeneklerle diğer belge türlerini (ör. PDF, DOCX) TIFF'a dönüştürebilir miyim?**  
C: Evet. Aspose.Note OneNote dosyalarına odaklansa da, Aspose.PDF, Aspose.Words ve diğer kütüphaneler kendi formatları için benzer `ImageSaveOptions` sunar.

**S: TIFF JPEG sıkıştırması standart bir JPEG dosyasından nasıl farklıdır?**  
C: JPEG algoritması aynıdır, ancak görüntü verileri bir TIFF konteyneri içinde bulunur; bu konteyner birden çok sayfa ve daha zengin meta veri tutabilir.

**S: Birçok `.one` dosyasını toplu olarak işleyebilir miyim?**  
C: Kesinlikle. Bir dizin üzerinde döngü kurun, her dosya için üç yöntemden birini çağırın ve ortaya çıkan TIFF'ları toplayın.

**S: Çıktı TIFF'ın DPI/çözünürlüğünü kontrol edebilir miyim?**  
C: Evet. Kaydetmeden önce `options.setResolution(int dpi)` kullanın.

**S: Aspose.Note asenkron işleme destekliyor mu?**  
C: API kendisi senkron çalışır, ancak çağrıları Java’nın `CompletableFuture` veya bir iş parçacığı havuzu içinde sararak paralel yürütme sağlayabilirsiniz.

## Sonuç

Artık JPEG, PackBits veya CCITT Group 3 Faks sıkıştırması kullanarak OneNote belgelerini TIFF dosyalarına kaydederken **TIFF dosya boyutunu azaltmanıza** olanak tanıyan eksiksiz bir **Java TIFF dönüşüm** aracına sahipsiniz. Kalite, renk modu ve çözünürlüğü ihtiyaçlarınıza göre ayarlayın, toplu iş akışlarına entegre edin ve üretkenliğinizi en üst düzeye çıkarın.

---

**Son Güncelleme:** 2026-11-05  
**Test Edilen Versiyon:** Aspose.Note for Java 26.4 (yazım zamanı en güncel)  
**Yazar:** Aspose

## İlgili Öğreticiler

- [OneNote Sayfa Görüntüsü (JPEG) Kaydetme ve Save Format Kullanma – Aspose.Note for Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Aspose.Note for Java kullanarak OneNote'u PNG olarak Kaydet – Not Defterini Görüntüye Dönüştür](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [OneNote'u Gri Tonlamalı Görüntü Olarak Dışa Aktarma – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}