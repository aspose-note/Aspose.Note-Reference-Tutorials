---
date: 2025-11-29
description: Java kullanarak OneNote sayfalarını görüntülere nasıl dışa aktaracağınızı
  öğrenin ve Aspose.Note ile OneNote sayfa görüntüsünü nasıl dönüştüreceğinizi keşfedin.
  Hızlı entegrasyon için adım adım rehberimizi izleyin.
linktitle: How to Export OneNote Page to Image Using Java
second_title: Aspose.Note Java API
title: Java Kullanarak OneNote Sayfasını Görüntü Olarak Dışa Aktarma
url: /tr/java/onenote-document-loading/convert-page-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Kullanarak OneNote Sayfasını Görüntü Olarak Dışa Aktarma

## Giriş

Bu öğreticide, **OneNote** sayfalarını Java ve Aspose.Note kullanarak görüntü dosyalarına nasıl dışa aktaracağınızı öğreneceksiniz. Bir OneNote sayfasını görüntüye dönüştürmek, not defteri içeriğini raporlara eklemeniz, OneNote kullanmayan kişilerle anlık görüntüler paylaşmanız veya belge yönetim sistemleri için küçük resimler (thumbnail) oluşturmanız gerektiğinde oldukça kullanışlıdır. Her adımı adım adım inceleyecek, her satırın neden önemli olduğunu açıklayacak ve çıktıyı nasıl özelleştirebileceğinizi göstereceğiz.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekli?** Aspose.Note for Java  
- **Görüntü formatını seçebilir miyim?** Evet – `ImageSaveOptions` aracılığıyla JPEG, PNG, BMP vb.  
- **Üretim ortamında lisansa ihtiyacım var mı?** Ticari kullanım için geçerli bir Aspose.Note lisansı gereklidir.  
- **Hangi sayfayı dışa aktarabilirim?** `PageIndex` (sıfır‑tabanlı) ayarlanarak herhangi bir sayfa.  
- **Dönüşüm ne kadar sürer?** Standart bir sayfa için genellikle bir saniyenin altında.

## OneNote sayfalarını görüntülere dışa aktarmak nedir?
OneNote sayfalarını dışa aktarmak, sayfanın zengin içeriğini—metin, çizimler, tablolar—statik bir görüntü dosyasına (ör. JPEG) dönüştürmek anlamına gelir. Bu işlem, OneNote istemcisinin yüklü olmadığı ortamlarda bile görüntülenebilen taşınabilir bir görsel temsil oluşturur.

## OneNote sayfalarını dönüştürmek için Aspose.Note neden kullanılmalı?
- **Tam doğruluk** – düzeni, yazı tiplerini ve kalem darbelerini korur.  
- **Microsoft Office bağımlılığı yok** – Java’yı destekleyen herhangi bir platformda çalışır.  
- **İnce ayar kontrolü** – görüntü formatı, kalite ve belirli sayfa indeksi seçilebilir.  
- **Ölçeklenebilir** – çok sayıda sayfanın toplu işlenmesi için uygundur.

## Ön Koşullar

Başlamadan önce aşağıdaki ön koşulların sağlandığından emin olun:

1. **Java Development Kit (JDK)** – JDK 11 veya daha yeni bir sürüm kurun. Henüz kurmadıysanız [Oracle'ın resmi sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilirsiniz.  
2. **Aspose.Note for Java** – En yeni kütüphaneyi [Aspose.Note indirme sayfasından](https://releases.aspose.com/note/java/) edinin. JAR dosyasını projenizin sınıf yoluna ekleyin.

## Paketleri İçe Aktarma

İlk olarak, belge işleme ve görüntü kaydetme seçeneklerine erişmemizi sağlayacak gerekli paketleri içe aktaralım.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Adım 1: OneNote Belgesini Yükleme

`.one` dosyasını bir `Aspose.Note` `Document` nesnesine yükleyerek işe başlıyoruz.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **İpucu:** Dosyanız bir JAR içinde bulunuyorsa mutlak yol ya da kaynak akışı (resource stream) kullanın.

## Adım 2: Görüntü Kaydetme Seçeneklerini Başlatma

Çıktı formatını (bu örnekte JPEG) tanımlamak için bir `ImageSaveOptions` örneği oluşturun. `SaveFormat` değerini değiştirerek PNG, BMP veya GIF gibi formatlara geçiş yapabilirsiniz.

```java
// Initialize ImageSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
```

## Adım 3: Sayfa İndeksini Belirleme

Sayfalar sıfır‑tabanlıdır, bu yüzden `1` **ikinci** sayfayı seçer. İhtiyacınız olan herhangi bir sayfayı dışa aktarmak için bu değeri ayarlayın.

```java
// Specify second page for conversion
options.setPageIndex(1);
```

## Adım 4: Belgeyi Görüntü Olarak Kaydetme

Şimdi `Document` nesnesi üzerinde `save` metodunu çağırarak hedef dosya adını ve yapılandırdığınız seçenekleri geçiyoruz.

```java
// Save the document
oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);
```

## Adım 5: Onay Mesajı Yazdırma

Basit bir konsol mesajı, görüntünün başarıyla oluşturulduğunu onaylar.

```java
// Print confirmation message
System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
```

## OneNote sayfalarını görüntülere dönüştürme (alternatif senaryolar)

OneNote sayfa görüntülerini toplu olarak **dönüştürmeniz** gerekiyorsa, yukarıdaki kodu `Document.getPages()` üzerinden dönen bir döngüye yerleştirin. Her yineleme için `options.setPageIndex(i)` çağrısını değiştirin ve isteğe bağlı olarak JPEG sıkıştırmasını kontrol etmek için `options.setQuality(90)` ayarlayın.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **Görüntü boş** | Sayfa indeksi aralık dışında veya belge doğru yüklenmemiş. | `options.setPageIndex` değerinin `0 .. document.getPages().size() - 1` arasında olduğundan emin olun. |
| **Desteklenmeyen format** | Belirli formatları içermeyen eski bir Aspose.Note sürümü. | En son Aspose.Note for Java sürümüne güncelleyin. |
| **OutOfMemoryError** | Çok büyük sayfalar düşük bellekli JVM’de işleniyor. | Heap boyutunu artırın (`-Xmx2g`) veya sayfaları tek tek işleyin. |

## Sık Sorulan Sorular

**S1: Bu yöntemle birden fazla sayfayı görüntüye dönüştürebilir miyim?**  
C: Evet. Kaydetme mantığını bir döngüye sarın ve dışa aktarmak istediğiniz her sayfa için `options.setPageIndex(i)` değerini değiştirin.

**S2: Aspose.Note farklı OneNote dosya sürümleriyle uyumlu mu?**  
C: Kesinlikle. Aspose.Note, OneNote 2007, 2010, 2013 ve sonraki sürümlerin `.one` dosyalarını destekler.

**S3: Dönüşüm sırasında görüntü formatını ve kalitesini özelleştirebilir miyim?**  
C: Evet. `SaveFormat.Png`, `SaveFormat.Bmp` vb. seçebilir ve JPEG kalitesi için `options.setQuality(int)` (0‑100) ayarlayabilirsiniz.

**S4: Aspose.Note başka programlama dilleri için de destek sağlıyor mu?**  
C: Evet. .NET, Python, C++ ve daha fazlası için kütüphaneler mevcuttur.

**S5: Ek destek veya yardım nereden alınabilir?**  
C: [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin veya resmi belgeleri [buradan](https://reference.aspose.com/note/java/) inceleyin.

---

**Son Güncelleme:** 2025-11-29  
**Test Edilen Sürüm:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}