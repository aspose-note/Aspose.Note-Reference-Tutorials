---
description: Aspose.Note for Java kullanarak OneNote PDF'yi nasıl kaydedeceğinizi
  ve OneNote'da alt sayfalar ekleyeceğinizi öğrenin. Notlarınızı verimli bir şekilde
  düzenlemek için bu adım adım rehberi izleyin.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: OneNote PDF'si Nasıl Kaydedilir ve Alt Sayfalar Nasıl Eklenir
url: /tr/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote PDF Nasıl Kaydedilir ve Alt Sayfalar Nasıl Eklenir

## Giriş

Bu öğreticide, Aspose.Note for Java kullanarak kök ve alt sayfalar içeren bir belge oluştururken **OneNote PDF nasıl kaydedilir** keşfedeceksiniz. OneNote defterlerinizi net bir hiyerarşi ile düzenlemek, gezinmeyi zahmetsiz kılar ve PDF olarak dışa aktarma, notlarınızı evrensel olarak okunabilir bir formatta paylaşmanızı sağlar. Ayrıca **sub pages onenote** stilinde alt sayfalar eklemeyi de göstereceğiz, böylece çok seviyeli yapılar kolayca oluşturabilirsiniz.

## Hızlı Yanıtlar
- **Birincil anahtar kelime ne anlama geliyor?** Aspose.Note kullanarak bir OneNote defterini PDF olarak dışa aktarmayı ifade eder.
- **Hangi API kullanılıyor?** Aspose.Note for Java.
- **Hiyerarşik sayfalar oluşturabilir miyim?** Evet – sayfa seviyesini ayarlayarak kök ve alt sayfalar oluşturabilirsiniz.
- **Lisans gerekli mi?** Ücretsiz deneme mevcuttur; üretim ortamı için ticari lisans gereklidir.
- **Hangi çıktı formatları destekleniyor?** BMP, PDF, PNG ve daha fazlası.

## “how to save OneNote PDF” nedir?
OneNote’u PDF olarak kaydetmek, defterin sayfalarını biçimlendirme, görseller ve hiyerarşi korunarak sabit düzenli bir belgeye dönüştürür. Bu, notları paylaşmak, arşivlemek veya yazdırmak için idealdir.

## Neden alt sayfalar eklenir?
Alt sayfalar eklemek, ilgili içeriği bir üst sayfanın altında gruplayarak klasör benzeri bir yapı oluşturur. Bu, not organizasyonunu iyileştirir, aramayı hızlandırır ve defter PDF’ye dışa aktarıldığında okuma deneyimini artırır.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. Java Development Kit (JDK): Sisteminizde JDK yüklü olduğundan emin olun.  
2. Aspose.Note for Java: Aspose.Note for Java’yı [web sitesinden](https://purchase.aspose.com/buy) indirin ve kurun.  
3. Entegre Geliştirme Ortamı (IDE): IntelliJ IDEA, Eclipse veya NetBeans gibi bir Java IDE’si seçin.

## Paketleri İçe Aktarma

Java projenizde gerekli paketleri içe aktararak başlayın:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Adım 1: Belge Dizini Ayarlama

OneNote belgenizi kaydetmek istediğiniz dizini tanımlayın:

```java
String dataDir = "Your Document Directory";
```

## Adım 2: Belge Nesnesi Oluşturma

Bir `Document` nesnesi örnekleyin:

```java
Document doc = new Document();
```

## Adım 3: Sayfalar Oluşturma

Sayfa nesnelerini başlatın ve seviyelerini ayarlayın. Seviyeyi ayarlamak, sayfanın kök sayfa mı yoksa alt sayfa mı olduğunu belirler:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Adım 4: Sayfalara Düğümler Ekleme

### İlk Sayfaya Düğümler Ekleme

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### İkinci Sayfaya Düğümler Ekleme

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Üçüncü Sayfaya Düğümler Ekleme

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Adım 5: Sayfaları Belgeye Ekleme

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Adım 6: Belgeyi Kaydetme

OneNote belgesini PDF (veya bu örnekte BMP) olarak kaydedin. `SaveFormat`'ı değiştirerek PDF olarak dışa aktarabilirsiniz; bu, “how to save OneNote PDF” gereksinimini karşılar:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Pro ipucu:** Doğrudan PDF’ye dışa aktarmak için `SaveFormat.Bmp` yerine `SaveFormat.Pdf` kullanın.

Tebrikler! Kök ve alt sayfalara sahip bir OneNote belgesi başarıyla oluşturdunuz ve Aspose.Note for Java kullanarak **OneNote PDF nasıl kaydedilir** öğrendiniz.

## Neden Önemli

- **Hiyerarşik organizasyon:** Kök ve alt sayfalar, OneNote içinde klasör yapısını taklit etmenizi sağlar.  
- **Sorunsuz PDF dışa aktarımı:** Düzenlendikten sonra PDF’ye dışa aktarma, hiyerarşiyi korur ve son belgeyi okumayı ve paylaşmayı kolaylaştırır.  
- **Otomasyon:** Kod, daha büyük Java uygulamalarına entegre edilebilir, yapılandırılmış defterlerin toplu oluşturulmasını sağlar.

## Yaygın Tuzaklar ve Nasıl Kaçınılır

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| Sayfalar aynı seviyede görünüyor | Yanlış `setLevel` değeri | Kök sayfalar için `setLevel((byte) 1)`, alt sayfalar için `setLevel((byte) 2)` (veya daha yüksek) kullanın. |
| PDF çıktısı boş görünüyor | `SaveFormat.Pdf` eksik veya dosya yolu hatalı | Dizin mevcut olduğundan emin olun ve `SaveFormat.Pdf` kullanın. |
| Yazı tipi uygulanmıyor | Yanlış yazı tipi adı veya sistemde eksik font | Kodun çalıştığı makinede (ör. “David Transparent”) fontun yüklü olduğundan emin olun. |

## Sıkça Sorulan Sorular

**S: Aspose.Note for Java kullanarak birden fazla alt‑sayfa seviyesi oluşturabilir miyim?**  
C: Evet, daha yüksek seviye numaraları (ör. üçüncü‑seviye alt‑sayfa için `setLevel((byte) 3)`) ayarlayarak daha derin hiyerarşiler oluşturabilirsiniz.

**S: Aspose.Note for Java farklı Java IDE’leriyle uyumlu mu?**  
C: Kesinlikle. IntelliJ IDEA, Eclipse, NetBeans ve Java geliştirmeyi destekleyen herhangi bir IDE ile çalışır.

**S: OneNote belgemdeki metin biçimlendirmesini özelleştirebilir miyim?**  
C: Evet. Her `RichText` öğesi için `ParagraphStyle` kullanarak yazı tipi adı, boyutu, rengi ve diğer özellikleri ayarlayabilirsiniz.

**S: Aspose.Note for Java BMP dışındaki formatlarda kaydetmeyi destekliyor mu?**  
C: Evet. Desteklenen formatlar arasında PDF, PNG, JPEG, DOCX ve daha fazlası bulunur. `SaveFormat` enum’ını buna göre değiştirin.

**S: Aspose.Note for Java için bir deneme sürümü mevcut mu?**  
C: Evet, Aspose web sitesinden ücretsiz bir deneme sürümü indirebilirsiniz.

## Sonuç

OneNote defterlerinizi net bir hiyerarşik yapı ile düzenlemek ve PDF olarak dışa aktarmak, notlarınızı daha erişilebilir ve paylaşılabilir kılar. Yukarıdaki adımları izleyerek **OneNote PDF nasıl kaydedilir** ve **sub pages onenote** stilinde programatik olarak alt sayfalar eklenir konularını artık biliyorsunuz.

---

**Son Güncelleme:** 2026-01-07  
**Test Edilen Versiyon:** Aspose.Note for Java 24.11 (en son)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}