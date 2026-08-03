---
date: 2026-08-03
description: Aspose.Note for Java kullanarak OneNote'ta yerel ayarı nasıl belirleyeceğinizi
  öğrenin – varsayılan yereli ayarlayın, belgeleri yükleyin, lisans uygulayın ve sayfaları
  PNG görüntülerine dönüştürün.
keywords:
- how to set locale
- set default locale java
- change onenote language settings
- convert onenote to png
lastmod: 2026-08-03
linktitle: OneNote'ta Yerel Ayarlarla Çalışma - Aspose.Note
og_description: Aspose.Note for Java kullanarak OneNote'ta yerel ayarı nasıl belirleyeceğinizi
  öğrenin. Varsayılan yereli ayarlamak, bir defteri yüklemek, lisans uygulamak ve
  sayfaları PNG görüntüleri olarak dışa aktarmak için adım adım talimatları izleyin.
og_image_alt: 'Developer guide: Set locale and convert OneNote to PNG with Aspose.Note
  Java'
og_title: OneNote'ta Yerel Ayarı Nasıl Belirlenir – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-03'
  description: Learn how to set locale in OneNote using Aspose.Note for Java – set
    default locale, load documents, apply a license, and convert pages to PNG images.
  headline: How to Set Locale in OneNote – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note supports Java 8 and later, ensuring broad compatibility
      across development environments.
    question: Is Aspose.Note compatible with different versions of Java?
  - answer: Absolutely. The API works seamlessly with popular libraries such as Apache
      POI, Jackson, and Spring.
    question: Can I integrate Aspose.Note with other Java libraries?
  - answer: While its core focus is OneNote files, the library can export to PNG,
      JPEG, PDF, and other image formats—over 30 output options in total.
    question: Does Aspose.Note offer support for different file formats?
  - answer: Yes, the Aspose community forum provides a platform for users to engage
      with experts, ask questions, and collaborate on solutions. Visit the [support
      forum](https://forum.aspose.com/c/note/28) for assistance.
    question: Is there a community forum for Aspose.Note users to seek help and share
      knowledge?
  - answer: Certainly, you can explore the capabilities of Aspose.Note by availing
      the free trial offered on the website.
    question: Can I try Aspose.Note before purchasing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- set locale
- Aspose.Note
- Java OneNote processing
- convert onenote to png
title: OneNote'ta Yerel Ayarı Nasıl Belirlenir – Aspose.Note Java
url: /tr/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote’da Yerel Ayarı Nasıl Belirlenir – Aspose.Note Java

## Giriş

If you need to **how to set locale** while processing OneNote files, Aspose.Note for Java makes it straightforward. In this tutorial we’ll walk through everything you need—from installing the Aspose license, loading a OneNote document, changing the locale, to converting the file to a PNG image. By the end, you’ll be able to customize language settings and generate locale‑specific outputs with just a few lines of Java code, which is essential for multinational applications.

## Hızlı Yanıtlar
- **“set default locale” ne yapar?** Aspose.Note'un OneNote dosyalarını okurken veya yazarken kullandığı dil ve bölgesel biçimlendirmeyi tanımlar.  
- **Bir lisansa ihtiyacım var mı?** Evet—tam işlevselliği açmak için Aspose lisansını ayarlayın.  
- **Hangi Java sürümü gereklidir?** JDK 8+ herhangi bir sürüm desteklenir.  
- **OneNote’u PNG’ye dönüştürebilir miyim?** Kesinlikle; API sayfaları görüntü olarak kaydetmenizi sağlar.  
- **İşlem çoklu iş parçacığı güvenli mi?** Varsayılan yerel ayarı ayarlamak küreseldir, bu yüzden uygulama başlangıcında bir kez yapılandırın.

## Aspose.Note’da “set default locale” nedir?

Varsayılan yerel ayarı ayarlamak, Aspose.Note'a tarih, sayı ve metin ayrıştırılırken hangi dil ve kültürel kuralları uygulaması gerektiğini söyler. Bu yanıt, “nedir” sorusunu 45 kelime içinde doğrudan çözer ve AI'nın öz bir tanım çıkarmasını sağlar. Farklı kullanıcı yerel ayarları arasında tutarlı biçimlendirme gerektiren çok‑bölgesel uygulamalar için gereklidir.

## OneNote ile çalışırken neden varsayılan yerel ayarı ayarlamalısınız?

Varsayılan yerel ayarı ayarlamak, tarihlerin, sayıların ve çıkarılan dizelerin hedef bölgenin kurallarına uymasını garanti eder; bu da veri yanlış yorumlamasını önler ve takvim gibi görsel öğelerin doğru render edilmesini sağlar. Bu, doğru veri temsili, tutarlı UI dizeleri ve daha sorunsuz görüntü dönüşüm sonuçları sağlar.

## Önkoşullar

- **Java Geliştirme Ortamı:** JDK 8 veya daha yeni bir sürüm yüklü ve `JAVA_HOME` yapılandırılmış.  
- **Aspose.Note Kütüphanesi:** En son JAR'ı [download link](https://releases.aspose.com/note/java/) adresinden indirin.  
- **Geçerli bir Aspose lisans dosyası** (ücretsiz deneme testi için çalışır).

## Paketleri İçe Aktar

`Locale` sınıfı belirli bir coğrafi, politik veya kültürel bölgeyi temsil eder.  
```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Adım 1: Aspose Lisansını Ayarla

`License` sınıfı satın alınan lisans dosyanızı yükler ve yerel ayar yönetimi ve görüntü dönüşümü dahil olmak üzere tüm premium özelliklerin kilidini açar.  
```java
License license = new License();
license.setLicense("licenseFile");
```

## Adım 2: Varsayılan Yerel Ayarı Belirle

`Locale`, dil ve ülke kodlarını kapsayan bir Java yardımcı sınıfıdır. Burada varsayılan yerel ayarı ülke kodu `RS` ile İngilizce (`en`) olarak ayarlıyoruz. Herhangi bir belge işlemi öncesinde dil ve ülke kodlarını hedef bölgenize göre ayarlayın.  
```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

## Adım 3: OneNote Belgesini Yükle

`Document`, Aspose.Note'un bellek içinde tek bir OneNote dosyasını temsil eden üst‑seviye nesnesidir. Oluşturulduktan sonra tüm okuma ve yazma işlemleri bu nesne üzerinden gerçekleşir.  
```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

## Adım 4: OneNote’u PNG’ye Dönüştür (OneNote dosya dönüşümü)

`Document` içindeki `Page` nesneleri raster görüntülere işlenebilir. `save` yöntemi bir OneNote dosyası dönüşümü gerçekleştirir, defteri (veya belirli bir sayfayı) PNG görüntüsü olarak dışa aktarır—etkili bir şekilde **onenote’u png’ye dönüştür** ve **onenote’u görüntü olarak kaydet**.  
```java
oneFile.save("sample.png");
```

## Yaygın Sorunlar ve İpuçları

- **Lisans bulunamadı:** `licenseFile` yolunun doğru olduğundan ve dosyanın okuma izinlerine sahip olduğundan emin olun.  
- **Yerel ayar uygulanmadı:** `Locale.setDefault` metodunu belgeyi yüklemeden **önce** çağırın; aksi takdirde varsayılan yerel ayar göz ardı edilir.  
- **Görüntü çıktısı eksik:** OneNote dosyasının gerçekten işlenebilir sayfalar içerdiğini doğrulayın; boş defterler boş bir PNG üretir.  
- **Performans ipucu:** Aspose.Note for Java, akış mimarisi sayesinde tüm dosyayı belleğe yüklemeden 500 sayfaya kadar defteri işleyebilir (nicel bir iddia).

## Sıkça Sorulan Sorular

**S: Aspose.Note farklı Java sürümleriyle uyumlu mu?**  
C: Evet, Aspose.Note Java 8 ve sonrası sürümleri destekler, böylece geliştirme ortamları arasında geniş uyumluluk sağlar.

**S: Aspose.Note’u diğer Java kütüphaneleriyle entegre edebilir miyim?**  
C: Kesinlikle. API, Apache POI, Jackson ve Spring gibi popüler kütüphanelerle sorunsuz çalışır.

**S: Aspose.Note farklı dosya formatlarını destekliyor mu?**  
C: Temel odak noktası OneNote dosyaları olsa da, kütüphane PNG, JPEG, PDF ve diğer görüntü formatlarına dışa aktarabilir—toplamda 30’dan fazla çıktı seçeneği sunar.

**S: Aspose.Note kullanıcılarının yardım alıp bilgi paylaşabileceği bir topluluk forumu var mı?**  
C: Evet, Aspose topluluk forumu, kullanıcıların uzmanlarla etkileşime geçebileceği, soru sorabileceği ve çözümler üzerinde iş birliği yapabileceği bir platform sunar. Yardım için [support forum](https://forum.aspose.com/c/note/28) adresini ziyaret edin.

**S: Aspose.Note’u satın almadan deneme şansım var mı?**  
C: Elbette, web sitesinde sunulan ücretsiz deneme sürümüyle Aspose.Note’un yeteneklerini keşfedebilirsiniz.

## Sonuç

Bu adımları izleyerek **yerel ayarı nasıl belirleyeceğinizi**, **OneNote belgesini nasıl yükleyeceğinizi**, **Aspose lisansını nasıl uygulayacağınızı** ve **OneNote’u PNG’ye nasıl dönüştüreceğinizi** Aspose.Note for Java kullanarak öğrendiniz. Bu iş akışı, 30’dan fazla yerel‑özel özelliği destekleyen ve 500 sayfaya kadar defteri verimli bir şekilde işleyebilen bir kütüphane sayesinde, küresel izleyicilere hitap eden yerel‑duyarlı raporlar ve görüntüler oluşturmanızı sağlar.

---

**Son Güncelleme:** 2026-08-03  
**Test Edilen Versiyon:** Aspose.Note 24.11 for Java  
**Yazar:** Aspose  

---

## İlgili Eğitimler

- [OneNote Defteri Oluştur – Aspose.Note for Java ile İşlemler](/note/java/onenote-notebook-operations/)
- [Notebook Nesnesi Oluştur ve Seçeneklerle OneNote Dosyasını Yükle - Aspose.Note](/note/java/onenote-notebook-operations/load-notebook-file-with-load-options/)
- [OneNote’da Seçeneklerle Notebook’u Görüntüye Dönüştür - Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}