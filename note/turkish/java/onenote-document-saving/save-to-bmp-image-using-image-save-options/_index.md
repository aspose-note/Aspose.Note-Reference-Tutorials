---
date: 2025-12-16
description: Aspose.Note for Java'ın görüntü kaydetme seçeneklerini kullanarak OneNote
  belgelerini BMP görüntülerine nasıl kaydedeceğinizi öğrenin. Ayrıca OneNote'u PDF
  veya PNG olarak nasıl kaydedeceğinizi görün.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: 'OneNote''u BMP Görüntüsü Olarak Kaydetme: Görüntü Kaydetme Seçeneklerini Kullanma'
url: /tr/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u BMP Görüntüsü Olarak Kaydetme - Image Save Options Kullanarak

## Giriş

Aspose.Note for Java, Java geliştiricilerinin Microsoft OneNote dosyalarıyla programlı olarak çalışmasını sağlayan güçlü bir kütüphanedir. **Bu öğreticide Aspose.Note for Java'nın Image Save Options özelliğini kullanarak OneNote belgelerini BMP görüntülerine nasıl kaydedeceğinizi öğreneceksiniz**. Her adımı adım adım gösterecek, BMP'yi diğer formatların üzerine neden tercih edebileceğinizi açıklayacak ve bu yeteneği kendi uygulamalarınıza nasıl entegre edeceğinizi göstereceğiz.

## Hızlı Yanıtlar
- **Image Save Options sınıfı ne yapar?** OneNote sayfasını dönüştürürken çıktı görüntü formatını (BMP, PNG, JPEG vb.) belirlemenizi sağlar.  
- **Örneği çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme sürümü yeterlidir, ancak üretim kullanımı için ticari lisans gereklidir.  
- **OneNote sayfasını BMP yerine PDF veya PNG'ye dönüştürebilir miyim?** Evet – sadece `SaveFormat` enum'ını değiştirin (ör. `SaveFormat.Pdf` veya `SaveFormat.Png`).  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri tam olarak desteklenir.  
- **Büyük belgeler için özel bir işlem var mı?** Çıktıyı akış olarak işleyerek yüksek bellek tüketimini önleyebilirsiniz.

## Aspose.Note'ta “Image Save Options” nedir?
`ImageSaveOptions` sınıfı, OneNote sayfalarının raster görüntüler olarak nasıl oluşturulacağını ince ayarlarla kontrol etmenizi sağlar. Görüntü formatını, çözünürlüğü, renk derinliğini ve daha fazlasını ayarlayabilirsiniz. Bu esneklik, eski sistemler için BMP dosyaları ya da web kullanımı için PNG/JPEG dosyaları oluşturmayı kolaylaştırır.

## Ön Koşullar

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

1. Java programlama diline temel bilgi.  
2. Makinenizde JDK (Java Development Kit) yüklü.  
3. Eclipse veya IntelliJ IDEA gibi bir IDE.  
4. Aspose.Note for Java kütüphanesi – indirmek için [buraya](https://releases.aspose.com/note/java/) tıklayın.

## Paketleri İçe Aktarma

İlk olarak, gerekli Aspose.Note sınıflarını ve standart Java I/O yardımcılarını içe aktarın:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Adım 1: OneNote Belgesini Yükleme

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Burada, kaynak OneNote dosyasını (`Aspose.one`) içeren klasöre işaret ediyor ve dosyayı bir `Document` nesnesine yüklüyoruz. Bu nesne, defter içindeki sayfalara, bölümlere ve diğer öğelere tam erişim sağlar.

## Adım 2: Belgeyi BMP Görüntüsü Olarak Kaydetme

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

Çıktı dosya adını birleştiriyoruz, ardından **BMP** (`SaveFormat.Bmp`) için yapılandırılmış bir `ImageSaveOptions` örneğiyle `save` metodunu çağırıyoruz.  
Eğer **OneNote sayfasını** PNG olarak kaydetmek isterseniz, sadece `SaveFormat.Bmp` yerine `SaveFormat.Png` koymanız yeterlidir. Benzer şekilde, `SaveFormat.Pdf` bir **OneNote'tan PDF'ye** dönüşüm yapmanızı sağlar.

## Neden BMP Seçilmeli?
- **Kayıpsız kalite** – BMP, ham piksel verilerini saklar ve orijinal sayfanın tam görünümünü korur.  
- **Uyumluluk** – Eski Windows uygulamaları genellikle BMP dosyalarına ihtiyaç duyar.  
- **Basitlik** – Sıkıştırma artefaktları yoktur, bu da ileri görüntü işleme için idealdir.

## Yaygın Sorunlar ve İpuçları
- **Dosya yolu hataları** – `dataDir` değişkeninin uygun dosya ayırıcıyla (`/` veya `\`) bittiğinden emin olun.  
- **Büyük defterler** – Çok büyük OneNote dosyaları için, bellek kullanımını düşük tutmak amacıyla her sayfayı ayrı ayrı kaydetmeyi düşünün.  
- **Lisans istisnaları** – Geçerli bir lisans olmadan kodu çalıştırmak, oluşturulan görüntüye bir filigran ekleyecektir.

## Sonuç

Bu rehberde, Aspose.Note for Java'nın `ImageSaveOptions` özelliğini kullanarak **OneNote** belgelerini BMP görüntülerine nasıl kaydedeceğinizi gösterdik. `SaveFormat` enum'ını değiştirerek PNG, JPEG, PDF veya diğer desteklenen formatları da üretebilir, OneNote içeriğini herhangi bir sonraki senaryo için esnek bir şekilde dışa aktarabilirsiniz.

## Sıkça Sorulan Sorular

**S1: OneNote belgelerini BMP dışındaki diğer görüntü formatlarına kaydedebilir miyim?**  
C: Evet, `ImageSaveOptions` ile `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` veya `SaveFormat.Tiff` kullanarak bu formatlara dışa aktarabilirsiniz.

**S2: Aspose.Note for Java farklı belge formatları arasında dönüşümü destekliyor mu?**  
C: Kesinlikle. Görüntü formatlarının yanı sıra, uygun `SaveFormat` kullanarak OneNote dosyalarını PDF, DOCX, HTML ve daha fazlasına dönüştürebilirsiniz.

**S3: Aspose.Note for Java en son OneNote sürümleriyle uyumlu mu?**  
C: Evet, kütüphane en yeni OneNote sürümleriyle uyumlu kalacak şekilde düzenli olarak güncellenir.

**S4: OneNote belgelerinin içeriğini programlı olarak manipüle edebilir miyim?**  
C: Evet, API aracılığıyla sayfalar, bölümler ve zengin içerik (metin, resimler, tablolar) ekleyebilir, düzenleyebilir veya silebilirsiniz.

**S5: Aspose.Note for Java teknik destek sağlıyor mu?**  
C: Evet, Aspose teknik destek ve özel bir forum sunar. Yardım için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Son Güncelleme:** 2025-12-16  
**Test Edilen:** Aspose.Note for Java 24.12  
**Yazar:** Aspose