---
date: 2026-03-05
description: Aspose.Note for Java'nın Görüntü Kaydetme Seçeneklerini kullanarak OneNote
  belgelerini BMP görüntülerine nasıl dışa aktaracağınızı öğrenin. Ayrıca OneNote'u
  PDF'ye nasıl dönüştüreceğinizi veya OneNote'u PNG olarak nasıl kaydedeceğinizi görün.
linktitle: how to export onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: OneNote'u Görüntü Kaydetme Seçenekleriyle BMP Görüntüsü Olarak Dışa Aktarma
url: /tr/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ı BMP Görüntüsü Olarak Dışa Aktarma – Image Save Options Kullanarak

## OneNote'ı BMP Görüntüsü Olarak Dışa Aktarma

Aspose.Note for Java, Java geliştiricilerinin Microsoft OneNote dosyalarıyla programatik olarak çalışmasını sağlayan güçlü bir kütüphanedir. **Bu öğreticide Image Save Options özelliğini kullanarak OneNote belgelerini BMP görüntülerine nasıl dışa aktaracağınızı** öğreneceksiniz. Her adımı ayrıntılı olarak inceleyecek, BMP'yi diğer formatlara göre neden tercih edebileceğinizi açıklayacak ve bu yeteneği kendi uygulamalarınıza nasıl entegre edeceğinizi göstereceğiz.

## Hızlı Yanıtlar
- **Image Save Options sınıfı ne işe yarar?** OneNote sayfasını dönüştürürken çıktı görüntü formatını (BMP, PNG, JPEG vb.) belirlemenizi sağlar.  
- **Örneği çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme sürümü çalışır, ancak üretim kullanımı için ticari lisans gereklidir.  
- **OneNote sayfasını BMP yerine PDF veya PNG'ye dönüştürebilir miyim?** Evet – sadece `SaveFormat` enum'ını değiştirin (ör. `SaveFormat.Pdf` veya `SaveFormat.Png`).  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri tam olarak desteklenir.  
- **Büyük belgeler için özel bir işlem var mı?** Bellek tüketimini azaltmak için çıktıyı akış olarak yazdırabilirsiniz.

## Aspose.Note'ta “Image Save Options” nedir?
`ImageSaveOptions` sınıfı, OneNote sayfalarının raster görüntüler olarak nasıl oluşturulacağını ince ayarlarla kontrol etmenizi sağlar. Görüntü formatını, çözünürlüğü, renk derinliğini ve daha fazlasını ayarlayabilirsiniz. Bu esneklik, eski sistemler (BMP) veya modern web senaryoları (PNG/JPEG) için **OneNote sayfa görüntüsünü dışa aktarmayı** kolaylaştırır.  

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

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

Burada, kaynak OneNote dosyasını (`Aspose.one`) içeren klasöre işaret ediyor ve bunu bir `Document` nesnesine yüklüyoruz. Bu nesne, defter içindeki sayfalara, bölümlere ve diğer öğelere tam erişim sağlar.

## Adım 2: Belgeyi BMP Görüntüsü Olarak Kaydetme

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

Çıktı dosya adını birleştiriyoruz, ardından **BMP** (`SaveFormat.Bmp`) için yapılandırılmış bir `ImageSaveOptions` örneğiyle `save` metodunu çağırıyoruz.  
PNG olarak **OneNote sayfasını kaydetmek** isterseniz, sadece `SaveFormat.Bmp` yerine `SaveFormat.Png` koymanız yeterlidir. Benzer şekilde, `SaveFormat.Pdf` size **OneNote'tan PDF'ye** dönüşüm yapma imkanı verir.

## Neden BMP Seçilmeli?
- **Kayıpsız kalite** – BMP, ham piksel verilerini saklar ve orijinal sayfanın tam görünümünü korur.  
- **Uyumluluk** – Eski Windows uygulamaları genellikle BMP dosyalarına ihtiyaç duyar.  
- **Basitlik** – Sıkıştırma artefaktları yoktur, bu da sonraki görüntü işleme işlemleri için idealdir.

## Yaygın Sorunlar ve İpuçları

- **Dosya yolu hataları** – `dataDir`'in uygun dosya ayırıcıyla (`/` veya `\`) bittiğinden emin olun.  
- **Büyük defterler** – Çok büyük OneNote dosyaları için, bellek kullanımını düşük tutmak amacıyla her sayfayı ayrı ayrı kaydetmeyi düşünün.  
- **Lisans istisnaları** – Geçerli bir lisans olmadan kodu çalıştırmak, oluşturulan görüntüye bir filigran ekleyecektir.

## Sonuç

Bu rehberde, Aspose.Note for Java’nın `ImageSaveOptions` özelliğini kullanarak **OneNote belgelerini BMP görüntülerine dışa aktarmayı** gösterdik. `SaveFormat` enum'ını değiştirerek PNG, JPEG, PDF veya diğer desteklenen formatları da üretebilir, böylece OneNote içeriğini herhangi bir sonraki senaryo için esnek bir şekilde dışa aktarabilirsiniz.

## Sıkça Sorulan Sorular

**S1: OneNote belgelerini BMP dışındaki diğer görüntü formatlarında kaydedebilir miyim?**  
C: Evet, `ImageSaveOptions` ile `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif` veya `SaveFormat.Tiff` kullanarak bu formatlara dışa aktarabilirsiniz.

**S2: Aspose.Note for Java farklı belge formatları arasında dönüşümü destekliyor mu?**  
C: Kesinlikle. Görüntü formatlarının yanı sıra, uygun `SaveFormat` kullanarak OneNote dosyalarını PDF, DOCX, HTML ve daha fazlasına dönüştürebilirsiniz.

**S3: Aspose.Note for Java en son OneNote sürümleriyle uyumlu mu?**  
C: Evet, kütüphane en yeni OneNote sürümleriyle uyumlu kalacak şekilde düzenli olarak güncellenir.

**S4: OneNote belgelerinin içeriğini programlı olarak manipüle edebilir miyim?**  
C: Evet, API aracılığıyla sayfalar, bölümler ve zengin içerik (metin, resimler, tablolar) ekleyebilir, düzenleyebilir veya silebilirsiniz.

**S5: Aspose.Note for Java teknik destek sağlıyor mu?**  
C: Evet, Aspose teknik destek ve özel bir forum sunar. Yardım için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin.

---

**Son Güncelleme:** 2026-03-05  
**Test Edilen:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}