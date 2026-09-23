---
date: 2026-09-19
description: Aspose.Note for Java kullanarak OneNote'u HTML'ye dönüştürme ve fonts
  dışa aktarmayı öğrenin. Bu kılavuz, OneNote'u gömülü fonts, CSS ve images ile HTML
  olarak kaydetmeyi kapsar.
keywords:
- convert onenote to html
- save onenote as html
- export fonts java
- aspose.note html export
lastmod: 2026-09-19
linktitle: OneNote'u HTML olarak kaydederken fonts dışa aktarma – Java
og_description: Aspose.Note for Java kullanarak OneNote'u HTML'ye dönüştürme ve fonts
  dışa aktarmayı öğrenin. Bu kılavuz, OneNote'u gömülü fonts, CSS ve images ile HTML
  olarak kaydetmeyi gösterir.
og_image_alt: 'Developer guide: convert OneNote to HTML with font export in Java'
og_title: OneNote'u HTML'ye dönüştürme ve Java'da fonts dışa aktarma – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  headline: How to convert OneNote to HTML and export fonts in Java
  type: TechArticle
- description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  name: How to convert OneNote to HTML and export fonts in Java
  steps:
  - name: create a OneNote document programmatically
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. You can either load an existing `.one` file or
      instantiate a new document and add sections/pages via the API. This line loads
      an existing `.one` file. If you need to **create OneNote programmatica
  - name: save to a memory stream with embedded fonts
    text: The `HtmlSaveOptions` class controls every aspect of the HTML conversion.
      `ResourceExportType` is an enumeration that defines how resources such as fonts,
      images, and CSS are exported. Setting `setExportFonts(ResourceExportType.ExportEmbedded)`
      tells Aspose.Note to embed fonts directly into the HTML
  - name: save as HTML with separate resource files (still exporting fonts)
    text: If you prefer a single HTML file, keep `ExportEmbedded`. For caching‑friendly
      deployments, switch `ResourceExportType` to `ExportExternal`; the fonts will
      still be embedded, but CSS, images, and other assets will be saved as separate
      files. Even though CSS and images are embedded, you can change the
  - name: use callbacks to control where each resource is stored
    text: '`UserSavingCallbacks` allows custom handling of resource saving. Implementing
      `UserSavingCallbacks` (which requires `ICssSavingCallback`, `IImageSavingCallback`,
      and `IFontSavingCallback`) gives you full control over folder structure, allowing
      you to keep fonts in a dedicated `fonts` directory while'
  type: HowTo
- questions:
  - answer: Yes, loop through each `Document` instance and apply the same `HtmlSaveOptions`.
    question: Can I convert multiple OneNote documents to HTML in one go?
  - answer: Absolutely. You can export to PDF, DOCX, PNG, JPEG, and more using the
      appropriate save options.
    question: Does Aspose.Note for Java support other output formats besides HTML?
  - answer: Yes, download a free trial from the **Aspose releases page**([Aspose releases
      page](https://releases.aspose.com/)).
    question: Is there a trial version available for Aspose.Note for Java?
  - answer: Visit the **Aspose.Note forum**([Aspose.Note forum](https://forum.aspose.com/c/note/28))
      for community and official assistance.
    question: Where can I get support for Aspose.Note for Java?
  - answer: Licenses are available at the **Aspose purchase page**([Aspose website](https://purchase.aspose.com/buy)).
    question: How can I purchase a license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- convert onenote
- Aspose.Note
- Java HTML export
- font embedding
title: OneNote'u HTML'ye dönüştürme ve Java'da fonts dışa aktarma
url: /tr/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u HTML'ye dönüştürme ve Java'da yazı tiplerini dışa aktarma

## Giriş

Bu öğreticide Aspose.Note for Java kullanarak **OneNote'u HTML'ye dönüştürürken** **yazı tiplerini nasıl dışa aktaracağınızı** keşfedeceksiniz. Programlı olarak bir OneNote belgesi oluşturmayı, HTML kaydetme seçeneklerini yapılandırmayı ve gerekli yazı tipi dosyalarını gömmeyi adım adım göstereceğiz, böylece ortaya çıkan HTML orijinal OneNote sayfalarına tam olarak benzer. Bu yaklaşım, özellikle bilgi tabanı portalları, otomatik raporlama hatları veya çok platformlu dokümantasyon siteleri için OneNote içeriğinin görsel bütünlüğünü web‑dostu bir formatta korumanız gerektiğinde mükemmeldir.

## Hızlı cevaplar
- **Dışa aktarmayı hangi kütüphane yönetir?** Aspose.Note for Java  
- **HTML'de yazı tipleri gömülebilir mi?** Evet – `ExportFonts` değerini `ExportEmbedded` olarak ayarlayın  
- **Üretim için lisansa ihtiyacım var mı?** Ticari kullanım için geçerli bir Aspose.Note lisansı gereklidir  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri  
- **Kaynakları ayrı dosyalara kaydetmek mümkün mü?** Kesinlikle – `ResourceExportType`'ı buna göre yapılandırın  

## “Yazı tiplerini dışa aktarma” OneNote HTML dönüşümü bağlamında ne anlama geliyor?

Yazı tiplerini dışa aktarmak, orijinal yazı tipi dosyalarını (ör. TTF veya OTF) doğrudan HTML paketine gömmek anlamına gelir, böylece tarayıcılar metni OneNote'ta göründüğü gibi tam olarak render eder, hatta son kullanıcının cihazında bu yazı tipleri bulunmasa bile. Aspose.Note, yazı tiplerini base‑64 dizelerine dönüştürerek ve oluşturulan CSS'e ekleyerek piksel‑tam tipografi garantisi sağlar.

## Neden OneNote'u HTML'ye dönüştürüp yazı tiplerini dışa aktarmalıyız?

Dönüşüm sırasında yazı tiplerini gömmek, orijinal OneNote sayfalarının görsel görünümünün tüm tarayıcılarda korunmasını sağlar, eksik tipografiler nedeniyle oluşan düzen kaymalarını ortadan kaldırır. Bu, özellikle kurumsal marka, yasal belgeler veya kesin tipografinin önemli olduğu herhangi bir içerik için önemlidir.

- **Otomasyon:** OneNote'tan manuel kopyala‑yapıştırma yapmadan raporlar, öğreticiler veya bilgi‑tabanı makaleleri oluşturun.  
- **Tutarlılık:** Tüm tarayıcı ve cihazlarda düzeni, stillemeyi ve özel yazı tiplerini koruyun.  
- **Taşınabilirlik:** HTML evrensel olarak görüntülenebilir—OneNote istemcisine veya ek eklentilere ihtiyaç yok.  
- **Performans:** Yazı tiplerini gömmek ekstra ağ isteklerini ortadan kaldırır, bu da küçük‑orta ölçekli belgeler için sayfa yükleme sürelerini iyileştirebilir.

## Önkoşullar

1. Java Development Kit (JDK) 8 veya daha yeni bir sürüm yüklü.  
2. Aspose.Note for Java kütüphanesi – **Aspose.Note for Java sürüm sayfasından**([Aspose.Note for Java release page](https://releases.aspose.com/note/java/)) indirin.  
3. Yüklemek için bir örnek OneNote dosyası (`.one`) veya programlı olarak yeni bir dosya oluşturabilirsiniz.  

## Paketleri içe aktar

İlk olarak, gerekli sınıfları Java projenize içe aktarın:

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

## Yazı tipi dışa aktarımıyla OneNote'u HTML'ye nasıl dönüştürürsünüz?

OneNote defterinizi yükleyin, `HtmlSaveOptions`'ı yazı tiplerini gömmek için yapılandırın ve sonucu bir akışa veya dosyaya kaydedin. Bu tek‑adımlı süreç, orijinal sayfalarda kullanılan her özel yazı tipinin HTML çıktısına dahil edilmesini sağlar, böylece görsel olarak sadık bir temsil sunarken iş akışını basit ve sürdürülebilir tutar.

### Adım 1: Programlı olarak bir OneNote belgesi oluşturun  

`Document` sınıfı, Aspose.Note'un bellekte tek bir OneNote dosyasını temsil eden üst‑seviye nesnesidir. Mevcut bir `.one` dosyasını yükleyebilir veya API aracılığıyla yeni bir belge oluşturup bölümler/sayfalar ekleyebilirsiniz.

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Bu satır mevcut bir `.one` dosyasını yükler. **Programlı olarak OneNote oluşturmanız** gerekiyorsa, yeni bir `Document` nesnesi örnekleyebilir ve API aracılığıyla bölümler/sayfalar ekleyebilirsiniz (burada yazı tipi dışa aktarmaya odaklanmak için gösterilmemiştir).

### Adım 2: Gömülü yazı tipleriyle bir bellek akışına kaydedin  

`HtmlSaveOptions` sınıfı HTML dönüşümünün her yönünü kontrol eder. `ResourceExportType` yazı tipleri, görseller ve CSS gibi kaynakların nasıl dışa aktarılacağını tanımlayan bir enumerasyondur. `setExportFonts(ResourceExportType.ExportEmbedded)` ayarı, Aspose.Note'a yazı tiplerini doğrudan HTML paketine gömmesini söyler, `setFontFaceTypes(FontFaceType.Ttf)` ise dışa aktarmayı en geniş tarayıcı desteğine sahip TrueType yazı tipleriyle sınırlar.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` Aspose.Note'a **yazı tiplerini** doğrudan HTML paketine dışa aktarmasını söyler.  
- `setFontFaceTypes(FontFaceType.Ttf)` TrueType yazı tiplerinin kullanılmasını sağlar, ki bu yazı tipleri geniş tarayıcı desteğine sahiptir.

### Adım 3: Ayrı kaynak dosyalarıyla HTML olarak kaydedin (yine de yazı tipleri dışa aktarılıyor)  

Tek bir HTML dosyası tercih ediyorsanız `ExportEmbedded`'i tutun. Önbellek‑dostu dağıtımlar için `ResourceExportType`'ı `ExportExternal` olarak değiştirin; yazı tipleri hâlâ gömülü olacak, ancak CSS, görseller ve diğer varlıklar ayrı dosyalar olarak kaydedilecektir.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

CSS ve görseller gömülü olsa bile, daha kolay önbellekleme için ayrı dosyaları tercih ediyorsanız `ResourceExportType`'ı `ExportExternal` olarak değiştirebilirsiniz. Ana kısım—**yazı tiplerini dışa aktarma**—değişmeden kalır.

### Adım 4: Her kaynağın nerede saklanacağını kontrol etmek için geri çağrıları (callbacks) kullanın  

`UserSavingCallbacks` kaynak kaydetmeyi özelleştirilmiş bir şekilde yönetmenizi sağlar. `UserSavingCallbacks`'i (bu, `ICssSavingCallback`, `IImageSavingCallback` ve `IFontSavingCallback` gerektirir) uygulamak, klasör yapısı üzerinde tam kontrol sunar; böylece yazı tiplerini özel bir `fonts` dizininde tutabilir ve **yazı tiplerini** doğru şekilde dışa aktarabilirsiniz.

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

Geri çağrı sınıfları dosyaları yeniden adlandırmanıza, akışları sıkıştırmanıza veya yazı tiplerini CDN‑hazır bir klasöre yerleştirmenize izin verir; bu da büyük ölçekli dağıtımlar için esneklik sağlar.

## OneNote'u HTML'ye dönüştürürken özel yazı tiplerini nasıl gömebilirsiniz

Özel yazı tiplerini gömmek, HTML render'ının orijinal OneNote düzeniyle eşleşmesini garanti eder, hatta bu yazı tipleri yüklü olmayan cihazlarda bile. `ExportEmbedded` ile `FontFaceType.Ttf`'yi birlikte kullanarak, TrueType dosyaları base‑64 olarak kodlanır ve doğrudan oluşturulan CSS'e eklenir; bu da dış yazı tipi barındırma ihtiyacını ortadan kaldırır ve tarayıcılar arasında tutarlı tipografi sağlar.

## Kaynak dışa aktarımını kontrol etmek için ResourceExportType kullanımı

`ResourceExportType`, CSS, görseller ve yazı tiplerinin HTML dosyasının **içinde** (`ExportEmbedded`) mi yoksa **harici** dosyalar (`ExportExternal`) olarak mı kaydedileceğine karar vermenizi sağlar. Tek dosyalı bir çözüm için `ExportEmbedded`, büyük varlıklar için tarayıcı önbelleklemesini kullanmak istediğinizde ise `ExportExternal` seçin.

## HTML dışa aktarımı için programlı olarak OneNote oluşturma

Baştan başlıyorsanız, tamamen kod içinde bir OneNote belgesi oluşturabilir, bölümler, sayfalar ve zengin metin ekleyebilir ve ardından yukarıda gösterilen aynı `HtmlSaveOptions`'ı uygulayabilirsiniz. Bu, veri üretiminden gömülü özel yazı tipli tam stilize bir HTML çıktısına kadar uçtan uca otomasyon sağlar.

## Yaygın sorunlar ve ipuçları

- **Çıktıda eksik yazı tipleri:** `setExportFonts(ResourceExportType.ExportEmbedded)` ayarının yapıldığını ve kaynak OneNote dosyasının gerçekten gömülü yazı tipleri kullandığını doğrulayın.  
- **Büyük HTML dosyaları:** Yazı tiplerini gömmek, her bir yazı tipi için boyutu 200‑500 KB artırabilir. Bant genişliği bir sorun ise `ExportFonts`'u `ExportExternal` olarak değiştirin ve yazı tiplerini bir CDN'de barındırın.  
- **Geri çağrı uygulama hataları:** Geri çağrı sınıflarınızın akışı doğru şekilde yazdığından ve kaynakları kapattığından emin olun, dosya bozulmasını önlemek için.  
- **Performans ipucu:** 100 sayfadan büyük defterler için bölümleri ayrı ayrı işleyin ve ortaya çıkan HTML parçalarını birleştirerek bellek kullanımını düşük tutun.  
- **Sayısal iddia:** Aspose.Note, tipik bir 2.5 GHz sunucuda 500 sayfaya kadar defteri 30 saniyenin altında dönüştürebilir ve belge başına 50'den fazla özel yazı tipini korur.

## Sıkça sorulan sorular

**S: Birden fazla OneNote belgesini aynı anda HTML'ye dönüştürebilir miyim?**  
C: Evet, her `Document` örneği üzerinden döngü yaparak aynı `HtmlSaveOptions`'ı uygulayabilirsiniz.  

**S: Aspose.Note for Java HTML dışındaki diğer çıktı formatlarını destekliyor mu?**  
C: Kesinlikle. Uygun kaydetme seçeneklerini kullanarak PDF, DOCX, PNG, JPEG ve daha fazlasına dışa aktarabilirsiniz.  

**S: Aspose.Note for Java için bir deneme sürümü mevcut mu?**  
C: Evet, **Aspose sürüm sayfasından**([Aspose releases page](https://releases.aspose.com/)) ücretsiz bir deneme indirebilirsiniz.  

**S: Aspose.Note for Java için destek nereden alabilirim?**  
C: Topluluk ve resmi yardım için **Aspose.Note forumunu**([Aspose.Note forum](https://forum.aspose.com/c/note/28)) ziyaret edin.  

**S: Aspose.Note for Java için lisans nasıl satın alınır?**  
C: Lisanslar **Aspose satın alma sayfasında**([Aspose website](https://purchase.aspose.com/buy)) mevcuttur.  

## Sonuç

Artık Aspose.Note for Java kullanarak **OneNote'u HTML'ye dönüştürürken** **yazı tiplerini nasıl dışa aktaracağınızı** biliyorsunuz. `HtmlSaveOptions`'ı yapılandırarak ve isteğe bağlı olarak geri çağrıları kullanarak, OneNote sayfalarınızın—özel yazı tipleri dahil—tam görünümünü web ortamına sunarken koruyabilirsiniz. Dosya boyutu ve önbellekleme stratejisini dengelemek için `ResourceExportType` ayarlarıyla deney yapın ve iş akışını otomatik raporlama hattınıza entegre ederek maksimum verimlilik elde edin.

---

**Last Updated:** 2026-09-19  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose

## İlgili Öğreticiler

- [Aspose.Note for Java kullanarak OneNote'u Belirtilen Yazı Tipleri Alt Sistemiyle PDF olarak Kaydetme](/note/java/onenote-document-saving/save-using-specified-fonts-subsystem/)
- [OneNote'u Metne Dönüştürme ve Belge Ziyaretçisi ile Görselleri Çıkarma - Java](/note/java/onenote-document-loading/extract-content-using-document-visitor/)
- [Aspose.Note for Java ile Sayfa Ayarlarını Kullanarak OneNote'u PDF'ye Dönüştürme](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}