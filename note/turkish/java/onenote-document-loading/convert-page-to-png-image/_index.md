---
date: 2026-09-04
description: Aspose.Note kullanarak Java'da OneNote sayfasını PNG görüntüsü olarak
  dışa aktarmayı öğrenin. Bu kılavuz .one dosyasını png'ye dönüştürmeyi, sayfa indeksini
  ayarlamayı ve görüntü olarak kaydetmeyi gösterir.
keywords:
- how to export onenote
- convert onenote to png
- save onenote as image
- convert .one to png
lastmod: 2026-09-04
linktitle: Java'da OneNote Sayfasını PNG Görüntüsü Olarak Dışa Aktarma
og_description: Aspose.Note ile Java'da OneNote sayfasını PNG olarak dışa aktarma.
  Bu kılavuz .one dosyasını yüklemeyi, bir sayfa seçmeyi ve yüksek kaliteli bir PNG
  görüntüsü kaydetmeyi adım adım gösterir.
og_image_alt: 'Tutorial: Export OneNote page to PNG image using Aspose.Note for Java'
og_title: Java ile Aspose.Note kullanarak OneNote sayfasını PNG olarak dışa aktarma
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to export OneNote page to PNG image in Java using Aspose.Note.
    This guide shows converting .one to png, setting the page index, and saving as
    an image.
  headline: How to export OneNote page to PNG in Java with Aspose.Note
  type: TechArticle
- description: Learn how to export OneNote page to PNG image in Java using Aspose.Note.
    This guide shows converting .one to png, setting the page index, and saving as
    an image.
  name: How to export OneNote page to PNG in Java with Aspose.Note
  steps:
  - name: Load the OneNote document
    text: The `Document` class represents a OneNote file in memory. Loading the file
      is the foundation for **convert .one to png**.
  - name: Initialise image‑save options
    text: '`ImageSaveOptions` tells Aspose.Note that the output should be **PNG**.
      You can also adjust DPI, color depth, and compression here.'
  - name: Set the page index (how to convert OneNote page)
    text: The `setPageIndex` method selects which page to export. Page numbering starts
      at **0**, so `0` refers to the first page. Adjust this value to export a different
      page or loop through pages for bulk conversion.
  - name: Save the document as PNG (save OneNote as PNG)
    text: Calling `save` writes the selected page to a PNG file on disk. The file
      name `ConvertSpecificPageToPngImage_out.png` is just an example—you can name
      it whatever you like. This final step **exports onenote page image** ready for
      use in reports, web pages, or further processing.
  type: HowTo
- questions:
  - answer: Aspose.Note for Java.
    question: What library is needed?
  - answer: Yes—use `setPageIndex` to target the exact page.
    question: Can I export a single page?
  - answer: PNG, JPEG, GIF, BMP, TIFF (PNG shown here).
    question: Supported image formats?
  - answer: A free trial is available; a license is required for production.
    question: Do I need a license?
  - answer: Typically under 10 minutes for a basic conversion.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote conversion
- Aspose.Note
- java image export
title: Java ile Aspose.Note kullanarak OneNote sayfasını PNG olarak dışa aktarma
url: /tr/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Aspose.Note ile OneNote sayfasını PNG olarak dışa aktarma

Bu öğreticide Aspose.Note for Java kütüphanesini kullanarak **OneNote sayfasını PNG görüntüsü olarak dışa aktarmayı** öğreneceksiniz. OneNote sayfalarını dışa aktarmak, notları OneNote ekosisteminin dışına paylaşmanız, raporlara gömmeniz veya görüntü işleme algoritmaları çalıştırmanız gerektiğinde sıkça ihtiyaç duyulan bir gereksinimdir. Ortam kurulumunu, .one dosyasını yüklemeyi, belirli bir sayfayı seçmeyi, görüntü seçeneklerini yapılandırmayı ve sonunda yüksek çözünürlüklü bir PNG dosyası kaydetmeyi ele alacağız.

## Hızlı yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java.  
- **Tek bir sayfayı dışa aktarabilir miyim?** Evet—tam sayfayı hedeflemek için `setPageIndex` kullanın.  
- **Desteklenen görüntü formatları?** PNG, JPEG, GIF, BMP, TIFF (burada PNG gösterilmiştir).  
- **Bir lisansa ihtiyacım var mı?** Ücretsiz deneme mevcuttur; üretim için bir lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir dönüşüm için genellikle 10 dakikadan az sürer.  
- **.one dosyasını png'ye nasıl dönüştürürüm?** `.one` dosyasını `Document` ile yükleyin, sayfa indeksini ayarlayın ve `ImageSaveOptions` ile kaydedin.  

## “OneNote sayfasını dışa aktarma” nedir?
OneNote sayfasını dışa aktarmak, bir `.one` belgesi içindeki belirli bir sayfayı bağımsız bir görüntü dosyasına (bu durumda PNG) dönüştürmek anlamına gelir. Bu, **onenote sayfa görüntüsünü dışa aktarmak** için paylaşım, gömme veya daha ileri görüntü‑tabanlı analiz gerektiğinde faydalıdır. İşlem, OneNote dosyasını yükerek, istenen sayfayı seçerek ve ardından o sayfayı raster görüntü olarak işleyerek başlar.

## OneNote'u PNG'ye dönüştürmek için neden Aspose.Note for Java kullanmalı?
Aspose.Note **50+ giriş ve çıkış formatını** destekler ve Microsoft Office gerektirmeden çok sayfalı defterleri işleyebilir. Sayfa seçimi, DPI ve renk derinliği üzerinde ayrıntılı kontrol sağlar ve vektör grafikleri ile metin netliğini koruyan PNG dosyaları üretir. Kütüphane, Java 8+ destekleyen herhangi bir platformda çalışır ve sunucu‑tarafı toplu dönüşümler için idealdir.

## Önkoşullar

Başlamadan önce şunların olduğundan emin olun:

1. **Java Development Kit (JDK)** – sürüm 8 veya üzeri.  
2. **Aspose.Note for Java** – en son JAR'ı [Aspose web sitesinden](https://releases.aspose.com/note/java/) indirin.  
3. **Bir OneNote belgesi** (`.one`) içinde dışa aktarmak istediğiniz sayfa bulunmalıdır.

## Paketleri içe aktar

İlk olarak gerekli Java sınıflarını içe aktarın:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

Bu içe aktarmalar, belge yükleme ve görüntü‑kaydet seçeneklerini yapılandırma dahil, Aspose.Note API'sinin çekirdek işlevlerine erişmenizi sağlar.

## Adım‑adım kılavuz

### Adım 1: OneNote belgesini yükleyin

`Document` sınıfı, bellekte bir OneNote dosyasını temsil eder. Dosyayı yüklemek, **.one dosyasını png'ye dönüştürmek** için temeldir.

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

### Adım 2: Görüntü‑kaydet seçeneklerini başlat

`ImageSaveOptions`, çıktının **PNG** olması gerektiğini Aspose.Note'a bildirir. Burada DPI, renk derinliği ve sıkıştırmayı da ayarlayabilirsiniz.

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

### Adım 3: Sayfa indeksini ayarla (OneNote sayfasını nasıl dönüştürürsünüz)

`setPageIndex` yöntemi, dışa aktarılacak sayfayı seçer. Sayfa numaralandırması **0**'dan başlar, bu yüzden `0` ilk sayfayı ifade eder. Farklı bir sayfayı dışa aktarmak veya toplu dönüşüm için sayfalar arasında döngü yapmak için bu değeri ayarlayın.

```java
// set page index
opts.setPageIndex(0);
```

### Adım 4: Belgeyi PNG olarak kaydedin (OneNote'u PNG olarak kaydet)

`save` çağrısı, seçilen sayfayı diskte bir PNG dosyasına yazar. `ConvertSpecificPageToPngImage_out.png` dosya adı sadece bir örnektir—istediğiniz gibi adlandırabilirsiniz. Bu son adım, **onenote sayfa görüntüsünü dışa aktarır** ve raporlarda, web sayfalarında veya daha ileri işleme için hazır hale getirir.

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

## Yaygın sorunlar ve ipuçları

- **Yanlış sayfa indeksi** – İndekslemenin 0'dan başladığını unutmayın. Boş bir görüntü alırsanız, indeks değerini kontrol edin.  
- **Eksik Aspose.Note JAR** – JAR'ın sınıf yolunuzda (classpath) olduğundan emin olun; aksi takdirde `ClassNotFoundException` alırsınız.  
- **Büyük sayfalar** – Çok büyük sayfalar için, `OutOfMemoryError` hatasından kaçınmak amacıyla JVM yığın boyutunu (`-Xmx`) artırmayı düşünün.  
- **Çözünürlük kontrolü** – Görüntü netliğini artırmak için `save` çağırmadan önce `opts.setResolution(300)` (veya ihtiyacınız olan herhangi bir DPI) kullanın.  

## Sıkça sorulan sorular

**Q1: Aspose.Note for Java kullanarak birden fazla sayfayı tek seferde PNG görüntülerine dönüştürebilir miyim?**  
A1: Evet, belge sayfaları üzerinde yineleme yapabilir, `opts.setPageIndex(i)` güncelleyebilir ve her yineleme için `save` çağırabilirsiniz.

**Q2: Aspose.Note for Java PNG dışındaki diğer görüntü formatlarını destekliyor mu?**  
A2: Kesinlikle. `ImageSaveOptions` içinde `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` veya `SaveFormat.Tiff` ayarlayarak bu formatları oluşturabilirsiniz.

**Q3: Aspose.Note for Java için ücretsiz bir deneme mevcut mu?**  
A3: Evet, ücretsiz denemeyi [Aspose Note indirme sayfasından](https://releases.aspose.com/) indirebilirsiniz.

**Q4: Sorunlarla karşılaştığımda teknik destek nereden alabilirim?**  
A5: Aspose topluluk forumundan destek alabilirsiniz [Aspose community forum](https://forum.aspose.com/c/note/28).

**Q5: Aspose.Note for Java için lisans nasıl satın alınır?**  
A5: Lisansı [satın alma sayfasından](https://purchase.aspose.com/buy) satın alabilirsiniz.

**Q6: Gömülü görüntüler dışa aktarım sırasında nasıl işlenir?**  
A6: Gömülü görüntüler PNG çıktısına otomatik olarak işlenir; ek bir kod gerektirmez.

**Q7: DPI veya görüntü çözünürlüğü ayarlayabilir miyim?**  
A7: Evet, çıktı kalitesini kontrol etmek için `save` çağırmadan önce `opts.setResolution(int dpi)` kullanabilirsiniz.

---

**Son Güncelleme:** 2026-09-04  
**Test Edilen Versiyon:** Aspose.Note for Java 24.11 (latest)  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.Note for Java Görüntü Kaydet Seçenekleri ile OneNote'u BMP Görüntüsü Olarak Dışa Aktarma](/note/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/)
- [OneNote Sayfalarını Dışa Aktar – Belirli Sayfa Aralığını Java ile PDF'ye Dönüştür](/note/java/onenote-document-loading/convert-page-range-to-pdf/)
- [JPEG DPI'yi artırmayı öğrenin – OneNote'ta Aspose.Note ile Çıktı Görüntü Çözünürlüğünü Ayarlama](/note/java/onenote-document-saving/set-output-image-resolution/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}