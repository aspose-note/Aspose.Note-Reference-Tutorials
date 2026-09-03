---
date: 2026-02-07
description: Aspose.Note for Java kullanarak OneNote’u HTML olarak kaydederken yazı
  tiplerini nasıl dışa aktaracağınızı öğrenin. Bu kılavuz, OneNote’u programlı olarak
  nasıl oluşturacağınızı ve yazı tiplerini, CSS’i ve görüntüleri nasıl gömeceğinizi
  gösterir.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: OneNote'i HTML Olarak Kaydederken Yazı Tiplerini Nasıl Dışa Aktarılır – Java
url: /tr/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'i HTML Olarak Kaydederken Yazı Tiplerini Nasıl Dışa Aktarılır – Java

## Giriş

Bu öğreticide **OneNote'i HTML olarak kaydederken** **yazı tiplerini nasıl aktaracağınızı** Aspose.Note for Java kullanarak keşfedeceksiniz. Programlı olarak bir OneNote belgesi oluşturmayı, HTML kayıt kayıt aralıklarını ve gerekli yazı tipi özelliklerini gömerek ortaya çıkan HTML'nin orijinal OneNote sayfalarıyla aynı görünmediğinden emin olun. Bu şekilde, OneNote içeriğinin görsel bütünlüğünü web dostu bir formatta korumanız mümkündür.

## Hızlı Yanıtlar
- **Dışa aktarmayı hangi kütük yönetir?** Aspose.Note for Java
- **Yazı türleri HTML'e gömülebilir mi?** Evet – `ExportFonts` özelliği `ExportEmbedded` olarak set edilir
- **Üretim için lisansa ihtiyacınız var mı?** Ticari kullanım için geçerli bir Aspose.Note lisansı gereklidir
- **Hangi Java sürümü destekleniyor mu?** Java8ve Üzeri
- **Kaynakları ayrı dosyalara kaydetmeniz mümkün mü?** kesinlikle – `ResourceExportType`ı buna göre yapılandırın

## OneNote HTML dönüşümü bağlamında "yazı tipleri nasıl dışa aktarılır" nedir?

OneNote defterini HTML'e dönüştürdüğünüzde görsel görünüm CSS, görüntüler ve özellikle orijinal sayfalarda kullanılan yazı tiplerine bağlıdır. **Yazı tiplerini aktarır**, yazı tipini (ör.TTF) doğrudan HTML paketine gömmek belirtir gelir; bu nedenle tarayıcılar, son kullanıcı bu yazı tiplerini yerel olarak yüklü olmasa bile içeriği OneNote'ta görünmediği gibi render eder.

## OneNote'u neden programlı olarak oluşturup HTML olarak kaydetmelisiniz?

- **Otomasyon:** OneNote'dan raporlar, belgeler veya bilgi‑tabanı makaleleri manuel kopyala‑yapıştırma yapılmadan hazırlanır.
- **Tutarlılık:** Cihazlar arasında düzen, stil ve özel yazı tiplerini kullanın.
- **Taşınabilirlik:** HTML evrensel olarak görüntülenebilir—OneNote'un sergilenmesine gerek yoktur.

## Önkoşullar

1. Java Development Kit (JDK)8veya daha yeni bir sürüm kurulu.
2. Aspose.Note for Java kütüphanesi – [buradan](https://releases.aspose.com/note/java/) indirilir.
3. Yüklemek için bir örnek OneNote dosyasını (`.one`) ya da programlı olarak yeni bir dosya oluşturabilirsiniz.

## Paketleri İçe Aktar

Öncelikle gerekli sınıfları Java projenize aktarın:

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

## OneNote'u HTML Olarak Kaydederken Yazı Tiplerini Nasıl Dışa Aktarabilirim?

Aşağıda, yazı tiplerini ve diğer kaynakları nasıl dışa aktaracağınızı gösteren adım adım bir kılavuz bulunmaktadır.

### Adım 1: Programatik Olarak Bir OneNote Belgesi Oluşturma

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Bu satır, mevcut bir `.one` dosyasını yükler. **OneNote'u programatik olarak oluşturmanız** gerekiyorsa, yeni bir `Document` nesnesi oluşturabilir ve API aracılığıyla bölümler/sayfalar ekleyebilirsiniz (yazı tiplerini dışa aktarmaya odaklanmak için burada gösterilmemiştir).

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

- `setExportFonts(ResourceExportType.ExportEmbedded)` Aspose.Note'a yazı tiplerini doğrudan HTML paketine **dışa aktarmasını** söyler.

- `setFontFaceTypes(FontFaceType.Ttf)` geniş tarayıcı desteğine sahip TrueType yazı tiplerinin kullanılmasını sağlar.

### Adım 3: Ayrı kaynak dosyalarıyla HTML olarak kaydedin (yazı tiplerini dışa aktarmaya devam edin)

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

CSS ve resimler gömülü olsa bile, daha kolay önbelleğe alma için ayrı dosyaları tercih ederseniz `ResourceExportType`'ı `ExportExternal` olarak değiştirebilirsiniz. Önemli kısım—**yazı tiplerini dışa aktarma**—değişmez.

### Adım 4: Her kaynağın nerede saklanacağını kontrol etmek için geri çağırma işlevlerini kullanın 

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

`UserSavingCallbacks` sınıfı (`ICssSavingCallback`, `IImageSavingCallback` ve `IFontSavingCallback` arayüzlerini uygulamanız gerekecek), klasör yapısı üzerinde tam kontrol sağlar ve yazı tiplerini ayrı bir `fonts` dizininde tutarken **yazı tiplerini doğru şekilde dışa aktarmanıza** olanak tanır.

## OneNote'u HTML'ye dönüştürürken özel yazı tiplerini nasıl gömersiniz?

Özel yazı tiplerini gömmek, bu yazı tiplerinin yüklü olmadığı cihazlarda bile HTML oluşturma işleminin orijinal OneNote düzeniyle eşleşmesini garanti eder. `ExportEmbedded`'ı `FontFaceType.Ttf` ile birlikte kullanarak, TrueType dosyaları base-64 kodlanır ve doğrudan oluşturulan CSS'ye eklenir, böylece harici yazı tipi barındırma ihtiyacı ortadan kalkar.

## Kaynak Dışa Aktarımını Kontrol Etmek İçin ResourceExportType Kullanımı

`ResourceExportType`, CSS, resimler ve yazı tiplerinin HTML dosyasının **içine** mi (`ExportEmbedded`) yoksa **harici** dosyalar olarak mı (`ExportExternal`) kaydedileceğine karar vermenizi sağlar. Tek dosya çözümü için `ExportEmbedded`'ı, büyük varlıklar için tarayıcı önbelleklemesini kullanmak istediğinizde ise `ExportExternal`'ı seçin.

## HTML Dışa Aktarımı İçin OneNote'u Programatik Olarak Oluşturma

Sıfırdan başlarsanız, OneNote belgesini tamamen kodla oluşturabilir, bölümler, sayfalar ve zengin metin ekleyebilir ve ardından yukarıda gösterilen aynı `HtmlSaveOptions`'ı uygulayabilirsiniz. Bu size uçtan uca otomasyon sağlar: veri üretiminden, özel yazı tipleri gömülü, tamamen stilize edilmiş bir HTML çıktısına kadar.

## Yaygın Sorunlar ve İpuçları

- **Çıktıda eksik yazı türleri:** `setExportFonts(ResourceExportType.ExportEmbedded)` ayarlandı ve kaynak OneNote yazıcılarının gerçekten yerleşik yazı türlerini doğrulayın.
- **Büyük HTML dosyaları:** Yazı tiplerini saklamak dosya olasılığını artırabilir. Bant genişliği bir sorun ise `ExportFonts`'u `ExportExternal` olarak etkinleştirildi ve yazı tiplerini bir CDN'de barındırın.
- **Geri çağırma (geri çağırma) uygulama hataları:** Geri çağırma sınıflarınızın verilerinden doğru yazdıklarından ve kaynakların kapatılmasından emin olun, aksi takdirde dosya bozulabilir.

## Sıkça Sorulan Sorular

**S: Birden fazla OneNote belgesini tek seferde HTML'e dönüştürebilir miyim?**
C: Evet, her `Document` örneği üzerinden döngü süresi boyunca aynı `HtmlSaveOptions`ı uygulayabilirsiniz.

**S: Aspose.Note for Java, HTML dışındaki diğer çıktı formatlarını kullanabilir mi?**
C: elbette. Uygun kayıt ayarlarını kullanarak PDF, DOCX, PNG, JPEG ve daha fazlasından daha fazlasına aktarabilirsiniz.

**S: Aspose.Note for Java için deneme sürümü mevcut mu?**
A: Evet, ücretsiz deneme yazılımı [buradan](https://releases.aspose.com/) indirebilirsiniz.

**S: Aspose.Note for Java için destek nereden alındı?**
A: Topluluk ve resmi yardım için [Aspose.Note forumunu](https://forum.aspose.com/c/note/28) ziyaret edin.

**S: Aspose.Note for Java lisansı nasıl satın alınır?**
A: Lisanslar, [Aspose web sitesinde](https://purchase.aspose.com/buy) mevcuttur.

## Çözüm

Aspose.Note for Java'yı kullanarak **OneNote'u HTML olarak kaydederken** artık **fontları nasıl dışa aktaracağınızı** biliyorsunuz. `HtmlSaveOptions` ayarını yapılandırarak ve isteğe bağlı olarak geri çağırma işlevlerini kullanarak, OneNote sayfalarınızın görünümünü (özel yazı tipleri de dahil olmak üzere) web'de sunarken aynen koruyabilirsiniz. Projenizin performans ve depolama gereksinimlerine uygun farklı `ResourceExportType` ayarlarıyla denemeler yapmaktan çekinmeyin.

---
**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}