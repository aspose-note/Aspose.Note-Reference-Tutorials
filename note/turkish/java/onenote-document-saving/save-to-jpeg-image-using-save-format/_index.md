---
date: 2025-12-17
description: OneNote'u resim olarak nasıl kaydedeceğinizi ve Aspose.Note for Java
  kullanarak OneNote'u nasıl dönüştüreceğinizi öğrenin. Bu adım adım kılavuz JPEG
  dönüşümünü gösterir.
linktitle: Save to JPEG Image Using Save Format in OneNote
second_title: Aspose.Note Java API
title: Kaydetme Biçimini Kullanarak OneNote'u Görüntü (JPEG) Olarak Kaydet
url: /tr/java/onenote-document-saving/save-to-jpeg-image-using-save-format/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save Format Kullanarak OneNote'u Görüntü (JPEG) Olarak Kaydet

## Giriş

Bu öğreticide **OneNote'u görüntü olarak kaydetmenin** sadece birkaç satır Java kodu ile nasıl yapılacağını keşfedeceksiniz. Aspose.Note for Java kullanarak bir OneNote defterini yüksek kaliteli bir JPEG dosyasına programlı olarak dönüştürebiliriz; bu, raporlama, küçük resimler veya web sayfalarına gömme için mükemmeldir. Ortamı kurmaktan son görüntüyü üretmeye kadar tüm süreci adım adım inceleyelim.

## Hızlı Yanıtlar
- **“save onenote as image” ne anlama geliyor?** Bir OneNote sayfasını veya defterini JPEG veya PNG gibi bir raster görüntü formatına dönüştürür.  
- **Dönüşümü hangi kütüphane sağlıyor?** Aspose.Note for Java, JPEG dışa aktarma için yerleşik destek sunar.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü yeterlidir; üretim kullanımı için ticari lisans gereklidir.  
- **Önkoşullar nelerdir?** Java JDK yüklü olmalı ve Aspose.Note for Java kütüphanesi indirilmiş olmalıdır.  
- **Görüntü kalitesini değiştirebilir miyim?** Evet, `ImageSaveOptions` sınıfı DPI, sıkıştırma ve diğer ayarları düzenlemenizi sağlar.

## “save onenote as image” nedir?

OneNote'u görüntü olarak kaydetmek, notlarınızın düzenini, yazı tiplerini ve gömülü nesneleri koruyan statik bir görsel temsil oluşturur. Bu, OneNote yüklü olmayan kullanıcılarla notları paylaşmanız gerektiğinde veya içeriği PDF, sunum veya web sayfalarına gömmek istediğinizde özellikle faydalıdır.

## OneNote'u Dönüştürmek İçin Aspose.Note for Java Neden Kullanılmalı?

- **Tam doğruluk:** Tüm sayfa öğeleri (metin, mürekkep, tablolar, görseller) eksiksiz olarak işlenir.  
- **Office kurulumu gerekmez:** Java destekleyen herhangi bir platformda çalışır.  
- **Otomasyon‑hazır:** Toplu işleme, bulut hizmetleri veya CI boru hatları için idealdir.  
- **Genişletilebilir:** Kaydetmeden önce belgeyi daha da işleyebilirsiniz (ör. bölümleri gizleme, filigran ekleme).

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların sağlandığından emin olun:

1. **Java Geliştirme Ortamı:** Sisteminizde Java Development Kit (JDK) kurulu olmalı.  
2. **Aspose.Note for Java Kütüphanesi:** Aspose.Note for Java kütüphanesini indirin ve kurun. İndirme bağlantısı: [burada](https://releases.aspose.com/note/java/).

## Paketleri İçe Aktarma

İlk olarak Java kodumuz için gerekli paketleri içe aktaralım:

```java
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Adım 1: Belgeyi Yükleme

İlk adım, OneNote dosyasını Aspose.Note içine yüklemektir. Bu, `Document` sınıfı kullanılarak yapılır.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Adım 2: JPEG Görüntüsü Olarak Kaydet

Şimdi çıktı dosya yolunu belirleyip `save()` metodunu `SaveFormat.Jpeg` enum değeriyle birlikte kullanarak belgeyi JPEG formatında kaydediyoruz.

```java
// Specify the output file path.
dataDir = dataDir + "SaveToJpegImageUsingSaveFormat_out.jpg";

// Save the document.
oneFile.save(dataDir, SaveFormat.Jpeg);
```

> **Pro ipucu:** Görüntü kalitesini kontrol etmeniz gerekiyorsa, `save` çağrısını bir `ImageSaveOptions` örneğiyle değiştirin ve `setResolution` veya `setCompressionLevel` gibi özellikleri ayarlayın.

## Yaygın Sorunlar ve Sorun Giderme

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| **Dosya bulunamadı** | Yanlış `dataDir` yolu | Mutlak yolu doğrulayın veya yolu güvenli bir şekilde oluşturmak için `Paths.get(...)` kullanın. |
| **Boş görüntü çıktısı** | Belge yalnızca varsayılan olarak desteklenmeyen mürekkep nesneleri içeriyor | `ImageSaveOptions` kullanın ve `setRenderInk(true)` özelliğini etkinleştirin. |
| **Büyük defterlerde OutOfMemoryError** | Çok büyük bir sayfayı tek seferde render etmeye çalışmak | Sayfaları tek tek işleyin veya JVM yığın boyutunu artırın (`-Xmx2g`). |

## Sık Sorulan Sorular (Orijinal)

### S1: Aspose.Note karmaşık OneNote dosyalarını işleyebilir mi?

C1: Evet, Aspose.Note karmaşık OneNote dosyalarını verimli bir şekilde işlemek üzere tasarlanmıştır; doğru dönüşüm ve manipülasyon sağlar.

### S2: Aspose.Note for Java için bir deneme sürümü mevcut mu?

C2: Evet, Aspose.Note for Java ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) edinebilirsiniz.

### S3: Aspose.Note for Java için destek nasıl alınır?

C3: Aspose.Note for Java desteğini [Aspose.Note forumu](https://forum.aspose.com/c/note/28) üzerinden alabilirsiniz.

### S4: Aspose.Note for Java için geçici bir lisans satın alabilir miyim?

C4: Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) satın alabilirsiniz.

### S5: Aspose.Note for Java için ayrıntılı belgeleri nerede bulabilirim?

C5: Aspose.Note for Java için ayrıntılı belgeleri [burada](https://reference.aspose.com/note/java/) bulabilirsiniz.

## Ek SSS – OneNote Nasıl Dönüştürülür

**S: OneNote'u diğer görüntü formatlarına (PNG, BMP) nasıl dönüştürürüm?**  
C: `save` çağrısındaki `SaveFormat` enum değerini `SaveFormat.Png` veya `SaveFormat.Bmp` olarak değiştirin.

**S: Birden fazla OneNote dosyasını toplu olarak dönüştürebilir miyim?**  
C: Evet, bir klasördeki `.one` dosyalarını döngüyle okuyup her birini `new Document(...)` ile yükleyebilir ve benzersiz bir çıktı adıyla `save` metodunu çağırabilirsiniz.

**S: Tüm defter yerine belirli bir sayfayı dönüştürmek mümkün mü?**  
C: `Document` içinden istenen `Page` nesnesini alın ve `page.save(outputPath, SaveFormat.Jpeg)` metodunu kullanın.

## Sonuç

Aspose.Note for Java kullanarak **OneNote'u görüntü olarak kaydetme** sürecinin tüm adımlarını—ortam kurulumundan JPEG dosyası üretimine ve yaygın hataların çözümüne kadar—ele aldık. Bu bilgiyle OneNote dönüşümlerini otomatikleştirebilir, daha büyük iş akışlarına entegre edebilir veya kullanıcılarınıza notlarının taşınabilir görüntü anlık görüntülerini sunabilirsiniz.

---

**Son Güncelleme:** 2025-12-17  
**Test Edilen Sürüm:** Aspose.Note for Java 23.12 (yazım anındaki en yeni sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}