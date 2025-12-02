---
date: 2025-12-02
description: Aspose.Note for Java kullanarak OneNote’u HTML olarak kaydederken yazı
  tiplerini nasıl dışa aktaracağınızı öğrenin. Bu kılavuz, OneNote’u programlı olarak
  nasıl oluşturacağınızı ve yazı tiplerini, CSS’i ve görüntüleri nasıl gömeceğinizi
  gösterir.
language: tr
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: OneNote'i HTML Olarak Kaydederken Yazı Tiplerini Nasıl Dışa Aktarırsınız –
  Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'i HTML Olarak Kaydederken Yazı Tiplerini Dışa Aktarma – Java

## Giriş

Bu öğreticide **yazı tiplerini dışa aktarma** yöntemini, Aspose.Note for Java kullanarak **OneNote'i HTML olarak kaydederken** keşfedeceksiniz. Programatik olarak bir OneNote belgesi oluşturmayı, HTML kaydetme seçeneklerini yapılandırmayı ve gerekli yazı tipi dosyalarını gömerek ortaya çıkan HTML'nin orijinal OneNote sayfalarıyla aynı görünmesini sağlayacağız. Bu yaklaşım, OneNote içeriğinin görsel bütünlüğünü web‑dostu formatta korumanız gerektiğinde mükemmeldir.

## Hızlı Yanıtlar
- **Dışa aktarmayı hangi kütüphane yönetir?** Aspose.Note for Java  
- **Yazı tipleri HTML'e gömülebilir mi?** Evet – `ExportFonts` değerini `ExportEmbedded` olarak ayarlayın  
- **Üretim için lisansa ihtiyacım var mı?** Ticari kullanım için geçerli bir Aspose.Note lisansı gereklidir  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri  
- **Kaynakları ayrı dosyalara kaydetmek mümkün mü?** Kesinlikle – `ResourceExportType` değerini buna göre yapılandırın  

## “Yazı tiplerini dışa aktarma” OneNote HTML dönüşüm bağlamında ne anlama geliyor?

OneNote defterini HTML'e dönüştürdüğünüzde, görsel görünüm CSS, görüntüler ve özellikle orijinal sayfalarda kullanılan yazı tiplerine bağlıdır. **Yazı tiplerini dışa aktarma**, yazı tipi dosyalarını (ör. TTF) doğrudan HTML paketine gömmek anlamına gelir; böylece tarayıcılar, son kullanıcı bu yazı tiplerini yerel olarak yüklü olmasa bile, metni OneNote'da göründüğü gibi render eder.

## Neden OneNote programatik olarak oluşturup HTML olarak kaydetmeliyiz?

- **Otomasyon:** OneNote'tan raporlar, dokümantasyon veya bilgi‑tabanı makaleleri oluşturun, manuel kopyala‑yapıştırmaya gerek kalmasın.  
- **Tutarlılık:** Düzeni, stil ve özel yazı tiplerini cihazlar arasında koruyun.  
- **Taşınabilirlik:** HTML evrensel olarak görüntülenebilir—OneNote istemcisine ihtiyaç yok.  

## Önkoşullar

1. Java Development Kit (JDK) 8 veya daha yeni bir sürüm yüklü olmalı.  
2. Aspose.Note for Java kütüphanesi – [buradan](https://releases.aspose.com/note/java/) indirin.  
3. Yüklemek için bir örnek OneNote dosyası (`.one`) ya da programatik olarak yeni bir dosya oluşturabilirsiniz.  

## Paketleri İçe Aktarma

İlk olarak, Java projenize gerekli sınıfları içe aktarın:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## OneNote'i HTML Olarak Kaydederken Yazı Tiplerini Nasıl Dışa Aktarabilirsiniz?

Aşağıda, **yazı tiplerini dışa aktarma** ve diğer kaynakları gösteren adım‑adım bir rehber bulacaksınız.

### Adım 1: OneNote belgesini programatik olarak oluşturma  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Bu satır mevcut bir `.one` dosyasını yükler. **Programatik olarak OneNote oluşturmanız** gerekiyorsa, yeni bir `Document` nesnesi örnekleyebilir ve API aracılığıyla bölümler/sayfalar ekleyebilirsiniz (burada yazı tiplerini dışa aktarmaya odaklanmak için gösterilmemiştir).

### Adım 2: Gömülü yazı tipleriyle bir bellek akışına kaydetme  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` Aspose.Note'e **yazı tiplerini** doğrudan HTML paketine dışa aktarmasını söyler.  
- `setFontFaceTypes(FontFaceType.Ttf)` TrueType yazı tiplerinin kullanılmasını sağlar; bu tipler geniş tarayıcı desteğine sahiptir.

### Adım 3: Ayrı kaynak dosyalarıyla HTML olarak kaydetme (yazı tipleri hâlâ dışa aktarılıyor)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

CSS ve görüntüler gömülü olsa da, önbellekleme kolaylığı için `ResourceExportType` değerini `ExportExternal` olarak değiştirebilirsiniz. Temel kısım—**yazı tiplerini dışa aktarma**—değişmeden kalır.

### Adım 4: Her kaynağın nereye kaydedileceğini kontrol etmek için geri çağrıları (callbacks) kullanma  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

`UserSavingCallbacks` sınıfı (`ICssSavingCallback`, `IImageSavingCallback` ve `IFontSavingCallback` arayüzlerini uygulamanız gerekir) klasör yapısı üzerinde tam kontrol sağlar; böylece yazı tiplerini ayrı bir `fonts` dizininde tutabilir ve **yazı tiplerini dışa aktarma** işlemini doğru şekilde gerçekleştirebilirsiniz.

## Yaygın Sorunlar ve İpuçları

- **Çıktıda eksik yazı tipleri:** `setExportFonts(ResourceExportType.ExportEmbedded)` ayarının yapıldığını ve kaynak OneNote dosyasının gerçekten gömülü yazı tipleri kullandığını doğrulayın.  
- **Büyük HTML dosyaları:** Yazı tiplerini gömmek dosya boyutunu artırabilir. Bant genişliği bir sorun ise `ExportFonts` değerini `ExportExternal` yapıp yazı tiplerini bir CDN üzerinden sunabilirsiniz.  
- **Geri çağrı (callback) uygulama hataları:** Geri çağrı sınıflarınızın akışı doğru şekilde yazdığından ve kaynakları kapattığından emin olun; aksi takdirde dosya bozulabilir.  

## Sıkça Sorulan Sorular

**S: Birden fazla OneNote belgesini tek seferde HTML'e dönüştürebilir miyim?**  
C: Evet, her `Document` örneği üzerinde döngü kurup aynı `HtmlSaveOptions` ayarlarını uygulayabilirsiniz.  

**S: Aspose.Note for Java HTML dışındaki diğer çıktı formatlarını destekliyor mu?**  
C: Kesinlikle. Uygun kaydetme seçeneklerini kullanarak PDF, DOCX, PNG, JPEG ve daha fazlasına dışa aktarabilirsiniz.  

**S: Aspose.Note for Java için deneme sürümü mevcut mu?**  
C: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.  

**S: Aspose.Note for Java desteğini nereden alabilirim?**  
C: Topluluk ve resmi yardım için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin.  

**S: Aspose.Note for Java lisansını nasıl satın alabilirim?**  
C: Lisanslar [Aspose web sitesinde](https://purchase.aspose.com/buy) mevcuttur.  

## Sonuç

Artık Aspose.Note for Java kullanarak **OneNote'i HTML olarak kaydederken yazı tiplerini dışa aktarma** yöntemini biliyorsunuz. `HtmlSaveOptions` yapılandırması ve isteğe bağlı geri çağrılar sayesinde OneNote sayfalarınızın—özel yazı tipleri dahil—tam görünümünü web ortamına taşıyabilirsiniz. Projenizin performans ve depolama gereksinimlerine uygun olması için farklı `ResourceExportType` ayarlarıyla denemeler yapmaktan çekinmeyin.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2025-12-02  
**Test Edilen Sürüm:** Aspose.Note for Java 24.12  
**Yazar:** Aspose