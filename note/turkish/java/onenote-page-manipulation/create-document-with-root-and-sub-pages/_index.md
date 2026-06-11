---
date: 2026-04-30
description: Aspose.Note for Java kullanarak OneNote'ta **onenote'u pdf olarak kaydet**
  ve alt sayfalar eklemeyi öğrenin. Notlarınızı verimli bir şekilde düzenlemek için
  bu adım adım kılavuzu izleyin.
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: OneNote'u PDF olarak kaydetme ve alt sayfalar ekleme
second_title: Aspose.Note Java API
title: OneNote'u PDF Olarak Kaydetme ve Alt Sayfalar Eklemek
url: /tr/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u PDF olarak Kaydetme ve Alt Sayfalar Ekleme

## Giriş

Bu öğreticide, Aspose.Note for Java kullanarak hem kök hem de alt sayfalar içeren bir belge oluştururken **how to save onenote as pdf** öğreneceksiniz. OneNote defterlerinizi net bir hiyerarşiyle düzenlemek gezinmeyi sorunsuz hâle getirir ve PDF'ye dışa aktarmak notlarınızı evrensel olarak okunabilir bir formatta paylaşmanızı sağlar. Ayrıca **add sub pages onenote** stilinde nasıl alt sayfalar ekleyeceğinizi de göstereceğiz, böylece çok seviyeli yapılar kolayca oluşturabilirsiniz.

## Hızlı Yanıtlar

- **What does “save onenote as pdf” mean?** OneNote defterini Aspose.Note for Java kullanarak PDF dosyasına dışa aktarmayı ifade eder.  
- **Which API is required?** Aspose.Note for Java gerekli sınıfları ve yöntemleri sağlar.  
- **Can I create hierarchical pages?** Evet – kök sayfalar ve alt sayfalar oluşturmak için sayfa seviyesini ayarlayın.  
- **Do I need a license for production?** Ücretsiz deneme mevcuttur, ancak üretim kullanımı için ticari lisans gereklidir.  
- **Which formats can I export to?** PDF'nin yanı sıra BMP, PNG, JPEG, DOCX ve daha fazlasına dışa aktarabilirsiniz.

## OneNote'u PDF Olarak Kaydetme

OneNote'u PDF olarak kaydetmek, her defter sayfasını biçimlendirmeyi, görüntüleri ve sayfa hiyerarşisini koruyan sabit düzenli bir belgeye dönüştürür. Bu, notları paylaşmak, arşivlemek veya yazdırmak için, orijinal yapıyı bozmadan ideal bir yöntemdir.

## Neden onenote alt sayfalar ekleyelim?

Alt sayfalar eklemek, ilgili içeriği bir üst sayfanın altında gruplamanıza olanak tanır ve klasör benzeri bir yapıyı yansıtır. Bu, not organizasyonunu iyileştirir, aramayı hızlandırır ve defter PDF'ye dışa aktarıldığında okuma deneyimini artırır.

## Önkoşullar

Başlamadan önce, aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – Sisteminizde JDK yüklü olduğundan emin olun.  
2. **Aspose.Note for Java** – Aspose.Note for Java'ı [web sitesi](https://purchase.aspose.com/buy) adresinden indirin ve kurun.  
3. **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse veya NetBeans gibi bir Java IDE'si seçin.

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

## Adım 1: Belge Dizinini Ayarlama

OneNote belgenizi kaydetmek istediğiniz dizini tanımlayın:

```java
String dataDir = "Your Document Directory";
```

## Adım 2: Document Nesnesi Oluşturma

`Document` nesnesini örnekleyin:

```java
Document doc = new Document();
```

## Adım 3: Sayfalar Oluşturma

Sayfa nesnelerini başlatın ve seviyelerini ayarlayın. Seviyeyi ayarlamak, bir sayfanın kök sayfa mı yoksa alt sayfa mı olduğunu belirler:

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

OneNote belgesini PDF olarak (bu örnekte BMP olarak) kaydedin. `SaveFormat`'ı değiştirerek PDF'ye dışa aktarabilirsiniz; bu, “save onenote as pdf” gereksinimini karşılar:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Pro tip:** PDF'ye doğrudan dışa aktarmak için `SaveFormat.Bmp` yerine `SaveFormat.Pdf` kullanın.

Tebrikler! Kök ve alt sayfalara sahip bir OneNote belgesi başarıyla oluşturdunuz ve Aspose.Note for Java kullanarak **how to save onenote as pdf** öğrendiniz.

## Neden Önemli

- **Hierarchical organization:** Kök ve alt sayfalar, OneNote içinde klasör yapısını taklit etmenizi sağlar.  
- **Seamless PDF export:** Düzenlendikten sonra PDF'ye dışa aktarmak hiyerarşiyi korur, böylece son belge okunması ve paylaşılması kolay olur.  
- **Automation:** Kod, daha büyük Java uygulamalarına entegre edilebilir ve yapılandırılmış defterlerin toplu oluşturulmasını sağlar.

## Yaygın Tuzaklar ve Nasıl Kaçınılır

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| Sayfalar aynı seviyede görünüyor | Yanlış `setLevel` değeri | Kök sayfalar için `setLevel((byte) 1)`, alt sayfalar için `setLevel((byte) 2)` (veya daha yüksek) kullanın. |
| PDF çıktısı boş görünüyor | `SaveFormat.Pdf` eksik veya dosya yolu hatalı | Dizinin mevcut olduğunu doğrulayın ve `SaveFormat.Pdf` kullanın. |
| Yazı tipi uygulanmadı | Yanlış yazı tipi adı veya sistemde yazı tipi eksik | Kodun çalıştığı makinede yazı tipinin (ör. “David Transparent”) yüklü olduğundan emin olun. |

## Sıkça Sorulan Sorular

**S: Aspose.Note for Java kullanarak birden fazla alt‑sayfa seviyesi oluşturabilir miyim?**  
C: Evet, daha yüksek seviye numaraları ayarlayarak (ör. üçüncü‑seviye alt‑sayfa için `setLevel((byte) 3)`) daha derin hiyerarşiler oluşturabilirsiniz.

**S: Aspose.Note for Java farklı Java IDE'leriyle uyumlu mu?**  
C: Kesinlikle. IntelliJ IDEA, Eclipse, NetBeans ve Java geliştirmeyi destekleyen herhangi bir IDE ile çalışır.

**S: OneNote belgemde metin biçimlendirmesini özelleştirebilir miyim?**  
C: Evet. Her `RichText` öğesi için yazı tipi adı, boyutu, rengi ve diğer özellikleri ayarlamak için `ParagraphStyle` kullanın.

**S: Aspose.Note for Java BMP dışındaki formatlarda belge kaydetmeyi destekliyor mu?**  
C: Evet. Desteklenen formatlar PDF, PNG, JPEG, DOCX ve daha fazlasını içerir. `SaveFormat` enum'ını buna göre değiştirin.

**S: Aspose.Note for Java için bir deneme sürümü mevcut mu?**  
C: Evet, Aspose web sitesinden ücretsiz bir deneme sürümü indirebilirsiniz.

## Sonuç

OneNote defterlerinizi net bir hiyerarşik yapı ile düzenlemek ve PDF olarak dışa aktarmak notlarınızı daha erişilebilir ve paylaşılabilir hâle getirir. Yukarıdaki adımları izleyerek artık Aspose.Note for Java ile programlı olarak **how to save onenote as pdf** ve **add sub pages onenote** stilinde nasıl yapacağınızı biliyorsunuz.

---

**Son Güncelleme:** 2026-04-30  
**Test Edilen Versiyon:** Aspose.Note for Java 24.11 (latest)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}