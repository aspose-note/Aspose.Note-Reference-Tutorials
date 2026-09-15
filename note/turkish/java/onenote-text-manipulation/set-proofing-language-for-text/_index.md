---
date: 2026-03-29
description: Aspose.Note for Java kullanarak OneNote'ta metin dili nasıl ayarlanır
  öğrenin. Bu adım adım rehber, OneNote belgesi oluşturmayı, metin dilini değiştirmeyi
  ve OneNote dosyasını verimli bir şekilde kaydetmeyi gösterir.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'ta Metin İçin Dili Nasıl Ayarlarsınız – Aspose.Note
url: /tr/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Metin İçin Dil Nasıl Ayarlanır – Aspose.Note

## Giriş
OneNote defterindeki belirli metin parçaları için **dil ayarlama** ihtiyacınız varsa, Aspose.Note for Java bunu basitleştirir. Bu öğreticide OneNote belgesi oluşturmayı, tek tek kelimeler veya ifadeler için metin dilini değiştirmeyi ve sonunda doğru düzeltme dilinin uygulanmış olduğu OneNote dosyasını kaydetmeyi öğreneceksiniz. Sonunda dil ayarlamanın yazım denetimi ve yerelleştirme için neden önemli olduğunu anlayacak ve çalıştırmaya hazır bir kod örneğine sahip olacaksınız.

## Hızlı Yanıtlar
- **“set language” neyi etkiler?** OneNote'a yazım denetimi ve dilbilgisi için hangi düzeltme sözlüğünün kullanılacağını söyler.  
- **Aynı notta farklı diller ayarlayabilir miyim?** Evet, her metin çalışmasına bir dil atayabilirsiniz.  
- **Aspose.Note için lisansa ihtiyacım var mı?** Test için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **Hangi Java sürümleri destekleniyor?** Aspose.Note for Java, Java 8 ve üzerini destekler.  
- **Çıktı bir .one dosyası mı?** Evet, belge OneNote *.one* dosyası olarak kaydedilir.

## Önkoşullar
Koda dalmadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Geliştirme Ortamı** – Yüklü ve yapılandırılmış JDK 8 veya daha üstü.  
2. **Aspose.Note for Java Kütüphanesi** – Kütüphaneyi [download link](https://releases.aspose.com/note/java/) adresinden indirip kurun.  
3. **Belge Dizini** – Oluşturulan OneNote dosyasının kaydedileceği makinenizde bir klasör oluşturun.

## OneNote'ta Metin İçin Dil Neden Ayarlanmalı?
Düzeltme dilini ayarlamak, çok dilli içerik için yazım denetimi, dilbilgisi önerileri ve arama indekslemesinin doğru çalışmasını sağlar. Bu özellikle şunlar için faydalıdır:

- **Küresel ekipler** tek bir defter üzerinde iş birliği yapar.  
- **Yerelleştirilmiş dokümantasyon** her bölümün farklı bir dilde olabileceği durumlar.  
- **Veri odaklı uygulamalar** dünya çapındaki kullanıcılar için notları programlı olarak üretir.

## Paketleri İçe Aktar
Gerekli Aspose.Note sınıflarını ve Java yardımcılarını içe aktararak başlayın.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Adım 1: Belge ve Sayfayı Ayarla
İçeriğinizi tutacak yeni bir OneNote belgesi ve sayfa oluşturun. Bu adım ayrıca **create OneNote document** ifadesini gösterir.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Adım 2: Anahat ve Anahat Öğesini Oluştur
Anahat, defter içeriği için bir kapsayıcıdır. Burada daha sonra dil‑spesifik metni içerecek yapıyı oluşturuyoruz.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Adım 3: Dil Ayarlarıyla Zengin Metin Ekle
Şimdi her metin segmentine belirli bir `Locale` ile `TextStyle` ekleyerek **change text language** gerçekleştiriyoruz. Bu, **set language for text** ifadesini gösterir.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Adım 4: Öğeleri Düzenle ve Kaydet
Anahat hiyerarşisini birleştirin, sayfaya ekleyin ve sonunda dil ayarları uygulanmış **save OneNote file** işlemini yapın.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Yaygın Tuzaklar ve İpuçları
- **Locale formatı** – IETF BCP‑47 etiketi (ör. `en-US`, `de-DE`) kullanın. Yanlış bir etiket, belgenin diline varsayılan olarak ayarlanır.  
- **Dosya yolu** – `dataDir`'in mevcut bir klasöre işaret ettiğinden emin olun; aksi takdirde `document.save` bir `IOException` fırlatır.  
- **Pro ipucu:** Tüm bir paragraf için dili ayarlamanız gerekiyorsa, her `append` çağrısı yerine `ParagraphStyle`'a `TextStyle` uygulayın.

## Sonuç
Aspose.Note for Java kullanarak OneNote defterindeki bireysel metin parçaları için **how to set language** öğrendiniz. Bu özellik, **create OneNote document** programlı olarak oluşturmanıza, **change text language** anında değiştirmenize ve **save OneNote file** doğru düzeltme meta verileriyle kaydetmenize olanak tanır.

## Sıkça Sorulan Sorular

**S: Örnekte belirtilmeyen diğer diller için düzeltme dili ayarlayabilir miyim?**  
C: Kesinlikle! İstenen `Locale.forLanguageTag("xx-XX")` ile ek `append` çağrıları ekleyin.

**S: Aspose.Note for Java en son Java sürümleriyle uyumlu mu?**  
C: Evet, kütüphane en yeni Java sürümlerini destekleyecek şekilde düzenli olarak güncellenir.

**S: Dil‑ayar sürecinde hataları nasıl yönetebilirim?**  
C: `IOException` veya `AsposeException` yakalamak için kaydetme işlemini bir `try‑catch` bloğuna sarın.

**S: Bu kodu bir web uygulamasına entegre edebilir miyim?**  
C: Elbette. Aspose.Note JAR'ını web projenizin sınıf yoluna ekleyin ve sunucunun hedef dizine yazma izni olduğundan emin olun.

**S: Aspose.Note for Java için ek örnekler ve dokümantasyon nerede bulunabilir?**  
C: API'lerin ve örnek projelerin tam listesi için [documentation](https://reference.aspose.com/note/java/) adresini inceleyin.

---

**Son Güncelleme:** 2026-03-29  
**Test Edilen Versiyon:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}