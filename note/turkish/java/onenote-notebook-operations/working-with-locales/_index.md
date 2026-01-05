---
date: 2026-01-05
description: Varsayılan yerel ayarı nasıl ayarlayacağınızı, OneNote belgesini nasıl
  yükleyeceğinizi, Aspose lisansını nasıl ayarlayacağınızı, OneNote'u PNG'ye nasıl
  dönüştüreceğinizi ve Aspose.Note for Java kullanarak OneNote'u resim olarak nasıl
  kaydedeceğinizi öğrenin.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'ta Varsayılan Yerel Ayarı Ayarla – Aspose.Note Java
url: /tr/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote’da Varsayılan Yerel Ayarı Belirleme – Aspose.Note Java

## Giriş

OneNote dosyalarını işlerken **varsayılan yerel ayarı** ayarlamanız gerekiyorsa, Aspose.Note for Java bu işi çok kolaylaştırır. Bu öğreticide, ürünü lisanslamaktan OneNote belgesini yüklemeye, yerel ayarı değiştirmeye ve nihayet dosyayı PNG görüntüsüne dönüştürmeye kadar ihtiyacınız olan her şeyi adım adım göstereceğiz. Sonunda, sadece birkaç satır kodla dil ayarlarını özelleştirebilecek ve yerel‑özel çıktılar üretebileceksiniz.

## Hızlı Yanıtlar
- **“Varsayılan yerel ayarı belirleme” ne işe yarar?** Aspose.Note’un OneNote dosyalarını okurken veya yazarken kullandığı dil ve bölgesel biçimlendirmeyi tanımlar.  
- **Lisans gerekir mi?** Evet—tam işlevselliği açmak için Aspose lisansını ayarlamalısınız.  
- **Hangi Java sürümü gerekli?** JDK 8 ve üzeri tüm sürümler desteklenir.  
- **OneNote’u PNG’ye dönüştürebilir miyim?** Kesinlikle; API sayfaları görüntü olarak kaydetmenize olanak tanır.  
- **İşlem çoklu iş parçacığı (thread‑safe) mi?** Varsayılan yerel ayarı küreseldir, bu yüzden uygulama başlangıcında bir kez yapılandırmanız yeterlidir.

## Aspose.Note’da “varsayılan yerel ayarı belirleme” nedir?
Varsayılan yerel ayarı ayarlamak, Aspose.Note’un tarih, sayı ve metin ayrıştırırken hangi dil ve kültürel kuralları uygulayacağını belirler. Bu, farklı kullanıcı yerelleri arasında tutarlı biçimlendirme gerektiren çok‑bölgesel uygulamalar için hayati öneme sahiptir.

## OneNote ile çalışırken varsayılan yerel ayarı neden ayarlamalıyız?
- **Doğru veri temsili:** Tarihler ve sayılar hedef kitle için doğru biçimde gösterilir.  
- **Tutarlı UI metinleri:** OneNote’tan çıkarılan metin dil ayarlarına saygı gösterir.  
- **Basitleştirilmiş dönüşüm:** OneNote dosyasını daha sonra PNG veya diğer formatlara dönüştürdüğünüzde görsel düzen beklenen yerel ayara uygun olur.

## Önkoşullar

- **Java Geliştirme Ortamı:** JDK yüklü ve `JAVA_HOME` yapılandırılmış olmalı.  
- **Aspose.Note Kütüphanesi:** En son JAR dosyasını [download link](https://releases.aspose.com/note/java/) adresinden indirin.  
- **Geçerli bir Aspose lisans dosyası** (test için ücretsiz deneme sürümü de kullanılabilir).

## Paketleri İçe Aktarma

Kod yazmaya başlamadan önce gerekli işlevselliği sağlayan sınıfları içe aktarın.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## Adım 1: Aspose Lisansını Ayarlama

```java
License license = new License();
license.setLicense("licenseFile");
```

Aspose lisansını ayarlamak, yerel ayar yönetimi ve görüntü dönüşümü dahil tüm özelliklerin kilidini açar.

## Adım 2: Varsayılan Yerel Ayarı Belirleme

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

Burada **varsayılan yerel ayarı** İngilizce (`en`) ve ülke kodu `rs` olarak ayarlıyoruz. Hedef bölgenize uygun dil ve ülke kodlarını değiştirin.

## Adım 3: OneNote Belgesini Yükleme

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

Bu adım **OneNote belgesini** `Document` nesnesine **yükler**, böylece içeriğiyle çalışabilirsiniz.

## Adım 4: OneNote’u PNG’ye Dönüştürme (OneNote dosya dönüşümü)

```java
oneFile.save("sample.png");
```

`save` metodu bir **onenote dosya dönüşümü** gerçekleştirir; defteri (veya belirli bir sayfayı) PNG görüntüsü olarak dışa aktarır—dolayısıyla **convert onenote to png** ve **save onenote as image** işlemlerini yapar.

## Yaygın Sorunlar ve İpuçları

- **Lisans bulunamadı:** `licenseFile` yolunun doğru olduğundan ve dosyanın okuma izinlerine sahip olduğundan emin olun.  
- **Yerel ayar uygulanmadı:** Belgeyi yüklemeden **önce** `Locale.setDefault` çağrısını yapın.  
- **Görüntü çıktısı eksik:** OneNote dosyasının gerçekten renderlanabilir sayfalar içerdiğini kontrol edin; boş defterler boş bir PNG üretir.

## Sık Sorulan Sorular

**S: Aspose.Note farklı Java sürümleriyle uyumlu mu?**  
C: Evet, Aspose.Note Java 8 ve üzeri sürümleri destekler, böylece geniş bir geliştirme ortamı uyumluluğu sağlar.

**S: Aspose.Note’u diğer Java kütüphaneleriyle entegre edebilir miyim?**  
C: Kesinlikle. API, Apache POI, Jackson ve Spring gibi popüler kütüphanelerle sorunsuz çalışır.

**S: Aspose.Note farklı dosya formatlarını destekliyor mu?**  
C: Temel odak noktası OneNote dosyaları olsa da, kütüphane PNG, JPEG, PDF ve diğer görüntü formatlarına dışa aktarım yapabilir.

**S: Aspose.Note kullanıcıları için bir topluluk forumu var mı?**  
C: Evet, Aspose topluluk forumu, kullanıcıların uzmanlarla etkileşime geçebildiği, soru sorabildiği ve çözümler paylaşabildiği bir platform sunar. Yardım için [support forum](https://forum.aspose.com/c/note/28) adresini ziyaret edin.

**S: Aspose.Note’u satın almadan deneyebilir miyim?**  
C: Elbette, web sitesinde sunulan ücretsiz deneme sürümüyle Aspose.Note’un yeteneklerini keşfedebilirsiniz.

## Sonuç

Bu adımları izleyerek **varsayılan yerel ayarı** nasıl **belirleyeceğinizi**, **OneNote belgesini nasıl yükleyeceğinizi**, **Aspose lisansını nasıl ayarlayacağınızı** ve **OneNote’u PNG’ye nasıl dönüştüreceğinizi** Aspose.Note for Java kullanarak öğrendiniz. Bu iş akışı, küresel izleyicilere hitap eden yerel‑duyarlı raporlar ve görüntüler üretmenizi sağlar.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-01-05  
**Test Edilen Versiyon:** Aspose.Note 24.11 for Java  
**Yazar:** Aspose  

---