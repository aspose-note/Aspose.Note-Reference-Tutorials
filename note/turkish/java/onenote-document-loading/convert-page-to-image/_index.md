---
date: 2026-07-05
description: Java kullanarak OneNote sayfalarını görüntülere nasıl dışa aktaracağınızı
  öğrenin ve Aspose.Note ile OneNote sayfa görüntüsünü nasıl dönüştüreceğinizi keşfedin.
  Hızlı entegrasyon için adım adım rehberimizi izleyin.
keywords:
- export onenote page
- convert .one to image
- onenote image conversion
- batch onenote conversion
linktitle: Java Kullanarak OneNote Sayfasını Görüntüye Dışa Aktar
schemas:
- author: Aspose
  dateModified: '2026-07-05'
  description: Learn how to export OneNote pages to images using Java, and discover
    how to convert OneNote page image with Aspose.Note. Follow our step‑by‑step guide
    for quick integration.
  headline: Export OneNote Page to Image Using Java
  type: TechArticle
- questions:
  - answer: Aspose.Note for Java
    question: What library is required?
  - answer: Yes – JPEG, PNG, BMP, GIF, and TIFF via `ImageSaveOptions`
    question: Can I choose the image format?
  - answer: A valid Aspose.Note license is required for commercial deployments.
    question: Do I need a license for production?
  - answer: Any page by setting the zero‑based `PageIndex`.
    question: Which page can I export?
  - answer: Typical pages convert in under a second on a standard JVM.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.Note Java API
title: Java Kullanarak OneNote Sayfasını Görüntüye Dışa Aktar
url: /tr/java/onenote-document-loading/convert-page-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Sayfasını Görüntü Olarak Dışa Aktarma Java Kullanarak

## Giriş

Bu öğreticide **Java ve güçlü Aspose.Note kütüphanesini** kullanarak OneNote sayfalarını görüntü dosyalarına nasıl dışa aktaracağınızı öğreneceksiniz. Bir OneNote sayfasını görüntüye dönüştürmek, not defteri içeriğini raporlara yerleştirmeniz, OneNote olmayan meslektaşlarınızla anlık görüntüler paylaşmanız veya bir belge‑yönetim sistemi için küçük resimler oluşturmanız gerektiğinde faydalıdır. Kodun her satırını adım adım inceleyecek, her ayarın neden önemli olduğunu açıklayacak ve toplu senaryolar için çıktıyı nasıl ayarlayabileceğinizi göstereceğiz.

## Hızlı Yanıtlar
- **Gerekli kütüphane nedir?** Aspose.Note for Java  
- **Görüntü formatını seçebilir miyim?** Evet – JPEG, PNG, BMP, GIF ve TIFF `ImageSaveOptions` aracılığıyla  
- **Üretim için lisansa ihtiyacım var mı?** Ticari dağıtımlar için geçerli bir Aspose.Note lisansı gereklidir.  
- **Hangi sayfayı dışa aktarabilirim?** Sıfır‑tabanlı `PageIndex` ayarlanarak herhangi bir sayfa.  
- **Dönüşüm ne kadar hızlı?** Tipik sayfalar standart bir JVM'de bir saniyeden kısa sürede dönüştürülür.

## OneNote sayfalarını görüntülere dışa aktarmak nedir?
OneNote sayfalarını görüntülere dışa aktarmak, sayfanın zengin içeriğini—metin, kalem, tablolar ve gömülü medya—JPEG gibi statik bir raster resme dönüştürür. Bu, OneNote istemcisi yüklü olmayan cihazlarda bile herhangi bir cihazda görüntülenebilen taşınabilir bir görsel temsil oluşturur.

## OneNote sayfalarını dönüştürmek için Aspose.Note neden kullanılmalı?
Aspose.Note **%100 düzen bütünlüğü** sağlar, yazı tiplerini, kalem darbelerini ve gömülü nesneleri kayıpsız işler. **Microsoft Office'ten bağımsız** çalışır, bu sayede Windows, Linux veya macOS JVM'lerinde çalıştırabilirsiniz. API, görüntü formatı, kalite ve sayfa seçimi üzerinde **ince ayar kontrolü** sunar ve **tek bir toplu işlemde 10.000'den fazla sayfayı** bellek tükenmeden işleyebilir.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulları yerine getirdiğinizden emin olun:

1. **Java Development Kit (JDK)** – JDK 11 veya daha yenisini kurun. Henüz yapmadıysanız [Oracle'ın resmi sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilirsiniz.  
2. **Aspose.Note for Java** – En son kütüphaneyi [Aspose.Note indirme sayfasından](https://releases.aspose.com/note/java/) edinin. JAR dosyasını projenizin sınıf yoluna ekleyin.

## Paketleri İçe Aktarma

`Document`, `ImageSaveOptions` ve ilgili sınıflar Aspose.Note API'sinin bir parçasıdır; OneNote dosyalarını yükleme, manipülasyon ve kaydetme işlevselliği sağlar.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Adım 1: OneNote Belgesini Yükleme

`Document` sınıfı bellekte tek bir OneNote defterini temsil eder. `.one` dosyasını yüklemek, sayfalara, bölümlere ve kaynaklara erişim sağlar.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Pro tip:** Dosyanız bir JAR içinde bulunuyorsa mutlak bir yol veya kaynak akışı kullanın; bu, çalışma zamanında `FileNotFoundException` oluşmasını önler.

## Adım 2: Görüntü Kaydetme Seçeneklerini Başlatma

`ImageSaveOptions`, sayfanın bir görüntüye nasıl render edileceğini tanımlar. `SaveFormat`'ı `Jpeg` olarak ayarlamak yaygın desteklenen bir dosya üretirken, `Png` şeffaflığı korur.

```java
// Initialize ImageSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
```

## Adım 3: Sayfa Dizini Belirleme

Sayfalar sıfır‑tabanlıdır, bu yüzden `1` **ikinci** sayfayı seçer. İhtiyacınız olan herhangi bir sayfayı dışa aktarmak için bu değeri ayarlayın veya toplu dönüşüm için tüm sayfalarda döngü yapın.

```java
// Specify second page for conversion
options.setPageIndex(1);
```

## Adım 4: Belgeyi Görüntü Olarak Kaydetme

`Document` nesnesi üzerinde `save` metodunu çağırmak, yapılandırdığınız seçenekleri kullanarak render edilen sayfayı dosya sistemine yazar.

```java
// Save the document
oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);
```

## Adım 5: Onayı Yazdırma

Basit bir konsol mesajı, görüntünün başarıyla oluşturulduğunu onaylar; bu, otomatikleştirilmiş boru hatlarında günlük tutmak için kullanışlıdır.

```java
// Print confirmation message
System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
```

## Yaygın Kullanım Senaryoları

- **Rapor Oluşturma:** OneNote ekran görüntülerini doğrudan PDF veya HTML raporlarına manuel ekran görüntüsü almadan gömün.  
- **Küçük Resim Oluşturma:** Büyük bir OneNote sayfa koleksiyonu için düşük çözünürlüklü ön izlemeler oluşturun, hızlı görsel aramayı mümkün kılar.  
- **Çapraz Platform Paylaşımı:** OneNote istemcisi olmayan macOS, Linux veya mobil cihaz kullanıcılarıyla bir OneNote sayfasının JPEG'ini paylaşın.

## OneNote sayfalarını görüntülere dönüştürme (alternatif senaryolar)

Birden fazla OneNote sayfasını toplu olarak **dönüştürmeniz** gerekiyorsa, yukarıdaki kodu `document.getPages()` üzerinde dönen bir döngüye yerleştirin. Her yineleme için `options.setPageIndex(i)` güncelleyin ve isteğe bağlı olarak JPEG sıkıştırmasını kontrol etmek için `options.setQuality(90)` ayarlayın. Bu yaklaşım, tek bir metod çağrısıyla tüm defterleri işleyebilmenizi sağlar.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **Görüntü boş** | Sayfa indeksi aralık dışında veya belge doğru yüklenmemiş. | `options.setPageIndex` değerinin `0 .. document.getPages().size() - 1` içinde olduğundan emin olun. |
| **Desteklenmeyen format** | Belirli formatları içermeyen eski bir Aspose.Note sürümü kullanılıyor. | En son Aspose.Note for Java sürümüne güncelleyin. |
| **OutOfMemoryError** | Düşük bellekli bir JVM'de çok büyük sayfalar dönüştürülüyor. | Yığın boyutunu artırın (`-Xmx2g`) veya sayfaları tek tek işleyin. |

## Sıkça Sorulan Sorular

**S1: Bu yöntemle birden fazla sayfayı görüntülere dönüştürebilir miyim?**  
C: Evet. Kaydetme mantığını bir döngüye sarın ve dışa aktarmak istediğiniz her sayfa için `options.setPageIndex(i)` değiştirin.

**S2: Aspose.Note farklı OneNote dosya sürümleriyle uyumlu mu?**  
C: Kesinlikle. Aspose.Note, OneNote 2007, 2010, 2013, 2016 ve sonraki sürümlerin `.one` dosyalarını destekler.

**S3: Dönüşüm sırasında görüntü formatını ve kalitesini özelleştirebilir miyim?**  
C: Evet. `SaveFormat.Png`, `SaveFormat.Bmp` veya `SaveFormat.Tiff` seçin ve JPEG sıkıştırması için `options.setQuality(int)` (0‑100) ayarlayın.

**S4: Aspose.Note diğer programlama dilleri için destek sunuyor mu?**  
C: Evet. .NET, Python, C++ ve daha fazlası için kütüphaneler mevcuttur; hepsi benzer işlevsellik sağlar.

**S5: Ek destek veya yardım nereden bulunabilir?**  
C: [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin veya resmi dokümantasyona [buradan](https://reference.aspose.com/note/java/) bakın.

**Last Updated:** 2026-07-05  
**Tested With:** Aspose.Note for Java 26.4  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Eğitimler

- [OneNote Sayfalarını Dışa Aktarma – Belirli Sayfa Aralığını Java ile PDF'e Dönüştürme](/note/java/onenote-document-loading/convert-page-range-to-pdf/)
- [OneNote'ta Defteri Görüntüye Dönüştürme - Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-image/)
- [Aspose Java Eğitimi - OneNote Sayfaları Hakkında Bilgi Almak - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}