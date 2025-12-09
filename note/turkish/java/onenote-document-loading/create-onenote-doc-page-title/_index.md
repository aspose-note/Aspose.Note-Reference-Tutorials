---
date: 2025-12-02
description: Java'da Aspose.Note for Java kullanarak başlıklı bir OneNote sayfası
  oluşturmayı öğrenin. Bu kılavuz, OneNote sayfa başlığını nasıl ayarlayacağınızı
  ve başlık yazı tipini nasıl özelleştireceğinizi gösterir.
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: Başlıklı OneNote Sayfası Nasıl Oluşturulur - Java
url: /tr/java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Sayfası Başlığı Nasıl Oluşturulur - Java

## Giriş

Programlı olarak **OneNote sayfası oluşturma** ihtiyacınız varsa, Aspose.Note for Java bunu çok basit hâle getirir. Bu öğreticide bir OneNote dosyası oluşturmayı, sayfa başlığını ayarlamayı ve hatta başlığın yazı tipini özelleştirmeyi Java kodu üzerinden öğreneceksiniz. Sonunda, herhangi bir Java uygulamasına entegre edebileceğiniz kullanıma hazır bir OneNote belgeniz olacak.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java.
- **Başlık için özel bir yazı tipi ayarlayabilir miyim?** Evet – `ParagraphStyle` kullanarak yazı tipi adı, boyutu ve rengini tanımlayabilirsiniz.
- **Hangi Java sürümü destekleniyor?** JDK 8+ (API geriye dönük uyumludur).
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü yeterlidir; üretim için lisans gereklidir.
- **Çıktı nerede kaydedilir?** `dataDir` değişkeninde belirttiğiniz yolda.

## OneNote Sayfa Başlığı Nedir?
OneNote sayfa başlığı, her sayfanın üst kısmında görüntülenen başlıktır. Genellikle sayfa adı, oluşturulma tarihi ve zamanı içerir. Bu başlığı programlı olarak ayarlamak, tutarlı ve iyi yapılandırılmış defterler oluşturmanıza yardımcı olur.

## OneNote Sayfa Başlığı Programlı Olarak Neden Ayarlanmalı?
- **Otomasyon:** Raporları veya toplantı notlarını manuel düzenleme yapmadan oluşturun.  
- **Tutarlılık:** Tüm sayfalarda aynı adlandırma kurallarını uygulayın.  
- **Entegrasyon:** OneNote’u diğer sistemlerle (ör. CRM, proje yönetim araçları) birleştirin.  

## Önkoşullar

- **Java Development Kit (JDK)** – sürüm 8 veya üzeri.  
- **Aspose.Note for Java** – resmi siteden **[buradan](https://releases.aspose.com/note/java/)** indirin.  
- **IDE** – IntelliJ IDEA, Eclipse veya NetBeans (seçiminize göre).

## Paketleri İçe Aktar

İlk olarak, Aspose.Note kütüphanesinden ihtiyacımız olan sınıfları içe aktaralım.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### Adım 1: Belge Dizinini Ayarla  
Oluşturulacak OneNote dosyasının kaydedileceği yeri tanımlayın.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### Adım 2: Belge Nesnesi Oluştur  
Yeni bir `Document` örneği oluşturun – bu, oluşturacağınız OneNote dosyasını temsil eder.

```java
// Create an object of the Document class
Document doc = new Document();
```

### Adım 3: Sayfa Nesnesini Başlat  
Başlığı ve diğer içeriği tutacak bir `Page` nesnesi oluşturun.

```java
// Initialize Page class object
Page page = new Page();
```

### Adım 4: Varsayılan Metin Stili Ayarla  
Başlık metnine uygulanacak varsayılan bir `ParagraphStyle` tanımlayın. Burada **OneNote başlık yazı tipini özelleştiriyoruz**.

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### Adım 5: Sayfa Başlığı Özelliklerini Ayarla  
Burada **OneNote sayfa başlığını** detaylarıyla (başlık metni, tarih ve saat) ayarlıyoruz. Kullanım senaryonuza göre dizeleri değiştirebilirsiniz.

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### Adım 6: Başlığı Sayfaya Ata  
Şimdi `Title` nesnesini `Page` ile ilişkilendirerek **başlığı OneNote’a ekliyoruz**.

```java
page.setTitle(title);
```

### Adım 7: Sayfayı Belgeye Ekle  
Yapılandırılmış sayfayı belge yapısına ekleyin.

```java
doc.appendChildLast(page);
```

### Adım 8: OneNote Belgesini Kaydet  
Çıktı dosya adını belirleyin ve defteri kaydedin. Bu, **java create onenote file** sürecini tamamlar.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## Yaygın Sorunlar ve İpuçları

| Sorun | Çözüm |
|-------|----------|
| **Geçersiz dosya yolu** | `dataDir` değişkeninin uygun bir ayırıcı (`/` veya `\\`) ile bittiğinden ve klasörün var olduğundan emin olun. |
| **Başlık görünmüyor** | `ParagraphStyle`’ın her `RichText` öğesine uygulandığını kontrol edin. |
| **Lisans istisnası** | Test için deneme lisansı kullanın; dağıtıma geçmeden önce tam lisansı uygulayın. |
| **Tarih yanlış ay gösteriyor** | Java ayları sıfır‑tabanlıdır; `cal.set(2018, 04, 03)` aslında Mayıs ayını ayarlar. Buna göre düzeltin. |

## Sık Sorulan Sorular

**S: Aspose.Note for Java farklı Java sürümleriyle uyumlu mu?**  
C: Evet, kütüphane Java 8 ve üzeri sürümlerle çalışır, böylece ortamlar arasında esneklik sağlar.

**S: Sayfa başlığının yazı tipi stilini ve boyutunu özelleştirebilir miyim?**  
C: Kesinlikle! Adım 4’te gösterildiği gibi `ParagraphStyle` kullanarak istediğiniz yazı tipi adı, boyutu ve rengini ayarlayabilirsiniz.

**S: Sayfaya daha fazla içerik (ör. paragraflar, resimler) eklemek istiyorum, nasıl?**  
C: Ek `RichText` veya `Image` nesneleri oluşturun, stillerini ayarlayın ve `page.appendChildLast(yourObject)` ile sayfaya ekleyin.

**S: Aspose.Note for Java için deneme sürümü mevcut mu?**  
C: Evet, tüm özellikleri değerlendirebilmeniz için Aspose web sitesinden ücretsiz bir deneme sürümü indirebilirsiniz.

**S: Sorun yaşarsam nereden destek alabilirim?**  
C: Topluluk yardımı için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin veya Aspose’tan bir destek bileti açın.

---

**Son Güncelleme:** 2025-12-02  
**Test Edilen Versiyon:** Aspose.Note for Java 24.12 (yazım anındaki en yeni sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}