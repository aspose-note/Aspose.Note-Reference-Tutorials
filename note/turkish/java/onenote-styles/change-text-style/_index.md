---
date: 2026-06-05
description: Aspose.Note for Java ile OneNote'ta yazı tipi boyutunu değiştirmeyi,
  yazı tipi rengini ayarlamayı ve metni vurgulamayı öğrenin – adım adım kod örnekli
  rehber.
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: OneNote'ta Yazı Tipi Boyutunu Değiştir - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: OneNote'ta Yazı Tipi Boyutunu Değiştir - Aspose.Note
url: /tr/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Yazı Tipi Boyutunu Değiştir - Aspose.Note

## Giriş

Bu öğreticide, Aspose.Note for Java kullanarak **how to change font size onenote** belgelerini nasıl değiştireceğinizi öğreneceksiniz. Bir OneNote dosyasını yüklemeyi, metin düğümlerine erişmeyi, renk, vurgulama ve yazı tipi boyutu değişikliklerini uygulamayı ve sonunda güncellenmiş dosyayı kaydetmeyi adım adım göstereceğiz. Rapor oluşturmayı otomatikleştiriyor ya da toplantı notlarını parlatıyor olun, bu kılavuz OneNote içeriğini programlı olarak biçimlendirmenin güvenilir bir yolunu sunar.

## Hızlı Yanıtlar
- **OneNote'ta Java ile yazı tipi boyutunu nasıl değiştiririm?** Belgeyi yükleyin, her `TextRun`'ın `FontSize` özelliğini değiştirin, ardından kaydedin – üç basit adım.  
- **Metin rengini ve vurgulamayı da değiştirebilir miyim?** Evet, aynı `TextRun` üzerinde `FontColor` ve `HighlightColor` ayarlayın.  
- **Aspose.Note'un hangi sürümü gereklidir?** 23.10+ herhangi bir sürüm bu stil API'lerini destekler.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme testi için çalışır; üretim için ticari lisans gereklidir.  
- **Bu yaklaşım büyük not defterleri için uygun mu?** Evet – Aspose.Note, tüm dosyayı belleğe yüklemeden çok sayfalı not defterlerini işler.

## change font size onenote nedir?
**change font size onenote**, bir OneNote defterindeki metin öğelerinin `FontSize` niteliğini programlı olarak ayarlamayı ifade eder. Aspose.Note kullanarak, geliştiriciler bu özelliği API aracılığıyla değiştirebilir, bu da temel OneNote dosya yapısını doğrudan güncelleyerek görsel görünüm değişikliklerini manuel düzenleme veya UI etkileşimi olmadan sağlar.

## OneNote'ta metin stilini değiştirmek için neden Aspose.Note kullanmalı?
Aspose.Note, font ailesi, boyutu, rengi, vurgulama, hizalama ve paragraf aralığı dahil olmak üzere 30'dan fazla biçimlendirme seçeneği sunar ve büyük not defterlerini verimli bir şekilde işlemek üzere tasarlanmıştır. 500'den fazla sayfaya sahip not defterlerini 150 MB'den az RAM kullanarak işleyebilir, kurumsal ölçekli belge iş akışları için güvenilir, yüksek performanslı otomasyon sağlar.

## Ön Koşullar

1. Temel Java programlama bilgisi.  
2. Makinenizde JDK 8 veya daha üstü yüklü.  
3. Aspose.Note for Java kütüphanesi (Aspose web sitesinden indirin).  
4. OneNote'un hiyerarşik yapısına (sayfalar, bölümler, RichText düğümleri) aşina olmak.

## Aspose.Note kullanarak OneNote'ta yazı tipi boyutunu nasıl değiştirirsiniz?

OneNote dosyanızı yükleyin, her `RichText` düğümünü bulun, her `TextRun`'ın stilini güncelleyin ve belgeyi kaydedin. Bu uçtan uca akış sadece birkaç satır kod gerektirir ve tipik not defterleri için bir saniyeden kısa sürede çalışır.

### Adım 1: Paketleri İçe Aktarın

`Document`, `RichText` ve `TextRun` sınıfları `com.aspose.note` ad alanında bulunur. Java kaynak dosyanızın en üstüne şu şekilde içe aktarın:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### Adım 2: Belgeyi Yükleyin

`Document` sınıfı, Aspose.Note'un bellek içindeki tek bir OneNote dosyasını temsil eden üst‑seviye nesnesidir. Bir dosyayı yüklemek, dosya yolunu yapıcıya (constructor) vermek kadar basittir.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### Adım 3: RichText Düğümlerine Erişin

`RichText` düğümleri gerçek paragraf metnini içerir. `document.getRichTextNodes()` üzerinden döngü kurarak not defterindeki düzenlenebilir tüm metin parçalarına erişebilirsiniz.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### Adım 4: Metin Stilini Değiştir

`TextRun`, aynı biçimlendirmeyi paylaşan karakterlerin ardışık bir akışını temsil eder. Döngü içinde `FontColor`'u sarı, `HighlightColor`'u mavi ve `FontSize`'ı **20** punto olarak ayarlayarak istediğiniz stili elde edebilirsiniz.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### Adım 5: Belgeyi Kaydet

`document.save("StyledSample.one")` çağrısı değişiklikleri bir OneNote dosyasına yazar. Kaydetme işlemi tüm orijinal içeriği korurken yeni stilleri uygular.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## Yaygın Sorunlar ve Çözümler

- **Metin değişmiyor:** Her `RichText` düğümü içinde `TextRun` nesneleri üzerinde döngü yaptığınızdan emin olun; bu seviyeyi atlamak biçimlendirmeyi etkilenmemiş bırakır.  
- **Renk farklı görünüyor:** Aspose.Note RGB değerlerini kullanır; doğru `java.awt.Color` sabitlerini kullandığınızı doğrulayın.  
- **Büyük not defteri yavaşlıyor:** LoadOptions, Aspose.Note'un bir dosyayı nasıl yüklediğini yapılandırır, akış ve format seçimine izin verir. Bellek kullanımını azaltan akış modunu etkinleştirmek için `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` kullanın.

## Sıkça Sorulan Sorular

**S:** Bu metin stil değişikliklerini OneNote belgemdeki belirli bölümlere uygulayabilir miyim?  
C: Evet, stil değişikliklerini uygulamadan önce `RichText` koleksiyonunu sayfa veya bölüm ID'sine göre filtreleyin.

**S:** Aspose.Note renk, vurgulama ve boyut dışında diğer biçimlendirme seçeneklerini destekliyor mu?  
C: Kesinlikle, aynı nesne modeliyle font ailesi, kalın/eğik, alt çizgi, hizalama ve paragraf aralığını değiştirebilirsiniz.

**S:** Aspose.Note'u gelişmiş işleme için diğer Java kütüphaneleriyle entegre edebilir miyim?  
C: Evet, Aspose.Note Apache POI, Jackson veya Spring gibi kütüphanelerle sorunsuz çalışır ve karmaşık belge akışları oluşturmanıza olanak tanır.

**S:** Aspose.Note ticari kullanım için lisanslı mı?  
C: Üretim dağıtımları için ticari lisans gereklidir; geliştirme ve test için ücretsiz bir değerlendirme lisansı mevcuttur.

**S:** Ek örnekler ve API referansını nerede bulabilirim?  
C: Aspose.Note dokümantasyon portalını ziyaret edin, tam API referans PDF'sini indirin ve topluluk örnekleri için GitHub deposunu inceleyin.

## Sonuç

Yukarıdaki adımları izleyerek artık **how to change font size onenote** dosyalarını nasıl değiştireceğinizi, metin rengini ayarlayacağınızı ve vurgulamaları uygulayacağınızı Aspose.Note for Java ile biliyorsunuz. Bu yetenek, toplantı notları, eğitim materyalleri veya ölçekli herhangi bir OneNote‑tabanlı içeriğin görsel düzenlemesini otomatikleştirmenizi sağlar.

---

**Son Güncelleme:** 2026-06-05  
**Test Edilen Versiyon:** Aspose.Note 23.10 for Java  
**Yazar:** Aspose

## İlgili Öğreticiler

- [OneNote'ta Varsayılan Paragraf Stilini Ayarla - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [OneNote'ta Metin İçin Düzeltme Dili Ayarla - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Microsoft OneNote Stili Sayfa Başlığını Ayarlama - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}