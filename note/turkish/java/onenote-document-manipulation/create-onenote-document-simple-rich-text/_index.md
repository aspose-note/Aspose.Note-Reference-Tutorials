---
date: 2026-08-18
description: OneNote'u PDF olarak dışa aktarmayı, Java'da paragraf biçimlendirmeyi
  ve Aspose.Note for Java kullanarak OneNote'u PDF olarak kaydetmeyi öğrenin.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: Java'da OneNote Belgesi Oluştururken Paragraf Stili Ayarlama
og_description: Aspose.Note kullanarak OneNote'u PDF olarak dışa aktarın ve Java'da
  paragraf stilini ayarlayın. Pürüzsüz PDF'ler oluşturmak için bu adım adım kılavuzu
  izleyin.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: Java'da paragraf stiliyle OneNote'u PDF olarak dışa aktarma (58 karakter)
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  headline: How to export OneNote to PDF with paragraph style in Java
  type: TechArticle
- description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  name: How to export OneNote to PDF with paragraph style in Java
  steps:
  - name: set document directory
    text: Define where the generated files will be saved. Replace `"Your Document
      Directory"` with an absolute or relative path on your machine.
  - name: initialize document object
    text: Create the root `Document` that represents the OneNote file. **Definition
      anchor:** `Document` is Aspose.Note’s top‑level object that holds one or more
      pages in memory.
  - name: initialize page object
    text: A OneNote file consists of one or more pages; we start with a single page.
      **Definition anchor:** `Page` represents a single OneNote page, containing outlines,
      images, and other elements.
  - name: initialize outline object
    text: Outlines act as containers for outline elements (think of them as sections).
      **Definition anchor:** `Outline` groups related `OutlineElement` objects and
      defines their visual hierarchy.
  - name: initialize outline element object
    text: Here we **add outline element** that will hold our rich text. **Definition
      anchor:** `OutlineElement` is a leaf node inside an `Outline` that can contain
      text, images, or other media.
  - name: set text style (set paragraph style)
    text: '`ParagraphStyle` defines the font family, size, color, and other typographic
      attributes for a paragraph. The `ParagraphStyle` instance defines the font,
      size, and color—this is where we **set paragraph style** for the upcoming text
      node.'
  - name: initialize rich text object
    text: '`RichText` is the node that stores styled text within an `OutlineElement`.
      We create a `RichText` node, insert a simple string, and attach the previously
      defined style.'
  - name: add rich text node to outline element
    text: Now the styled text lives inside the outline element.
  - name: add outline element node to outline
    text: The outline now contains the element that holds our paragraph.
  - name: add outline node to page
    text: We place the outline onto the page.
  type: HowTo
- questions:
  - answer: Yes, the API supports tables, images, hyperlinks, and advanced layout
      features in addition to plain text.
    question: Can Aspose.Note handle complex formatting such as tables or images?
  - answer: Direct conversion isn’t provided, but you can extract PDF content and
      rebuild a OneNote document using the API.
    question: Is it possible to convert a OneNote PDF back to a OneNote file?
  - answer: Absolutely. Aspose.Note for Java is platform‑independent; just ensure
      a compatible JDK is installed.
    question: Does the library work on Linux/macOS environments?
  - answer: Create additional `Page` and `Outline` objects, then append them to the
      `Document` just like the single‑page example.
    question: How do I add multiple pages or outlines?
  - answer: The official Aspose.Note documentation and the [support forum](https://forum.aspose.com/c/note/28)
      contain many code samples and real‑world scenarios.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- export onenote
- aspose.note
- java document processing
title: Java'da paragraf stiliyle OneNote'u PDF olarak dışa aktarma
url: /tr/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da OneNote belgesi oluştururken paragraf stilini ayarlama

## Giriş

OneNote'u programlı olarak PDF'ye dışa aktarmak, raporlama motorları, otomatik not alma hizmetleri ve belge dönüşüm hatları için yaygın bir gereksinimdir. Bu öğreticide **OneNote'u PDF'ye dışa aktarmayı**, özel paragraf biçimlendirmeyi uygulamayı ve OneNote dosyasını kaydetmeyi—tümü Aspose.Note for Java kullanarak—öğreneceksiniz. Sonunda, tanımladığınız görünümle profesyonel bir PDF üreten, kullanıma hazır bir Java kod parçacığına sahip olacaksınız.

## Hızlı cevaplar
- **“set paragraph style” ne anlama geliyor?** Bir metin paragrafına yazı tipi, boyut, renk ve diğer biçimlendirme özelliklerini uygular.  
- **Sonucu PDF'ye dışa aktarabilir miyim?** Evet – kılavuz, OneNote dosyasını PDF olarak kaydetme ile sona erer.  
- **Aspose.Note için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim kullanımı için ticari lisans gereklidir.  
- **Hangi IDE'ler destekleniyor?** Herhangi bir Java IDE – Eclipse, IntelliJ IDEA, NetBeans vb.  
- **Uygulama ne kadar sürer?** Temel bir belge için yaklaşık 10‑15 dakika.

## Java'da OneNote'u PDF'ye nasıl dışa aktarılır?

`Document`, sayfalar, taslaklar ve diğer öğeler içeren bir OneNote dosyasını temsil eder. OneNote belgenizi `new Document()` ile yükleyin (veya yeni bir tane oluşturun) ve `document.save("output.pdf", SaveFormat.Pdf)` metodunu çağırın. Aspose.Note, PDF'yi tek bir geçişte yazar, stilleri, görüntüleri ve taslakları Microsoft OneNote yüklü olmasa da korur. Bu doğrudan yaklaşım, Windows, Linux ve macOS'ta herhangi bir JDK 1.8+ ile çalışır.

## Aspose.Note'ta “set paragraph style” nedir?

`ParagraphStyle`, bir paragraf için yazı tipi adı, boyut, renk, hizalama ve diğer tipografik ayarları depolayan sınıftır. Bir `ParagraphStyle` örneğini bir `RichText` düğümüne ekleyerek, o paragrafın son OneNote sayfasında ve dışa aktarılan PDF'de nasıl görüneceğini tam olarak kontrol edersiniz.

## OneNote'u PDF'ye neden dışa aktarılır?

OneNote'u PDF'ye dışa aktarmak, kurumsal yazı tipleri ve renkleri koruyarak tutarlı bir marka kimliği sağlar, baskı veya arşivleme için tam düzeni koruyarak okunabilirliği artırır ve alıcıların OneNote'a ihtiyaç duymadan herhangi bir cihazda belgeyi görüntülemesini sağlayarak çapraz platform erişimi sunar. Ayrıca, büyük belgelerin hızlı bir şekilde işlenmesini sağlayarak performans avantajları da getirir.

## Önkoşullar

1. **Java Development Kit (JDK) 1.8+** – herhangi bir yeni JDK çalışır.  
2. **Aspose.Note for Java** – en son JAR'ı [Aspose.Note indirme sayfasından](https://releases.aspose.com/note/java/) indirin.  
3. **Bir IDE** (Eclipse, IntelliJ IDEA veya NetBeans) örneği derlemek ve çalıştırmak için.  

> **Pro ipucu:** Aspose.Note JAR'ını Maven (`<dependency>`) aracılığıyla projenizin sınıf yoluna ekleyin veya IDE'nizde JAR'ı manuel olarak referans gösterin.

## Paketleri içe aktar

İlk olarak, gerekli ad alanlarını içe aktarın. Bu blok değişmeden kalır.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> `ParagraphStyle` sınıfı, öğreticide daha sonra **paragraf stilini ayarlamak** için anahtardır.

## Adım adım kılavuz

Aşağıda her işlem için öz bir yürütme bulunmaktadır. Kod blokları orijinal örnekle aynı şekilde; sadece açıklayıcı metin ekliyoruz.

### Adım 1: belge dizinini ayarla
Oluşturulan dosyaların nereye kaydedileceğini tanımlayın.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini makinenizdeki mutlak ya da göreli bir yol ile değiştirin.

### Adım 2: belge nesnesini başlat
OneNote dosyasını temsil eden kök `Document` nesnesini oluşturun.

```java
Document doc = new Document();
```

**Tanım bağlantısı:** `Document`, bellekte bir veya daha fazla sayfa tutan Aspose.Note'un üst‑seviye nesnesidir.

### Adım 3: sayfa nesnesini başlat
Bir OneNote dosyası bir veya daha fazla sayfadan oluşur; tek bir sayfa ile başlıyoruz.

```java
Page page = new Page();
```

**Tanım bağlantısı:** `Page`, taslaklar, görüntüler ve diğer öğeler içeren tek bir OneNote sayfasını temsil eder.

### Adım 4: taslak nesnesini başlat
Taslaklar, taslak öğeleri için konteyner görevi görür (bölümler gibi düşünün).

```java
Outline outline = new Outline();
```

**Tanım bağlantısı:** `Outline`, ilgili `OutlineElement` nesnelerini gruplar ve görsel hiyerarşilerini tanımlar.

### Adım 5: taslak öğesi nesnesini başlat
Burada, zengin metnimizi tutacak **taslak öğesini ekliyoruz**.

```java
OutlineElement outlineElem = new OutlineElement();
```

**Tanım bağlantısı:** `OutlineElement`, bir `Outline` içinde metin, görüntü veya diğer medyaları içerebilen yaprak düğümdür.

### Adım 6: metin stilini ayarla (paragraf stilini ayarla)
`ParagraphStyle`, bir paragraf için yazı tipi ailesi, boyut, renk ve diğer tipografik özellikleri tanımlar.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

`ParagraphStyle` örneği yazı tipini, boyutu ve rengi tanımlar—bu, sonraki metin düğümü için **paragraf stilini ayarladığımız** yerdir.

### Adım 7: zengin metin nesnesini başlat
`RichText`, bir `OutlineElement` içinde biçimlendirilmiş metni depolayan düğümdür.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Bir `RichText` düğümü oluşturur, basit bir dize ekler ve önceden tanımlanan stili ekleriz.

### Adım 8: zengin metin düğümünü taslak öğesine ekle
```java
outlineElem.appendChildLast(text);
```

Artık biçimlendirilmiş metin taslak öğesi içinde yer alıyor.

### Adım 9: taslak öğesi düğümünü taslağa ekle
```java
outline.appendChildLast(outlineElem);
```

Taslak artık paragrafımızı tutan öğeyi içeriyor.

### Adım 10: taslak düğümünü sayfaya ekle
```java
page.appendChildLast(outline);
```

Taslağı sayfaya yerleştiriyoruz.

### Adım 11: sayfa düğümünü belgeye ekle
```java
doc.appendChildLast(page);
```

Belge artık biçimlendirilmiş metnimizle tek bir sayfaya sahip.

### Adım 12: belgeyi kaydet (OneNote PDF'yi dışa aktar)
```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

`save` yöntemi OneNote dosyasını yazar ve **OneNote'u PDF'ye dışa aktarır** tek bir adımda. Yerel format gerekiyorsa `SaveFormat.One` kullanarak `.one` olarak da kaydedebilirsiniz.

## Yaygın sorunlar ve çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **Dosya bulunamadı** | `dataDir`, var olmayan bir klasöre işaret ediyor. | Dizinin var olduğundan emin olun veya programlı olarak oluşturun (`new File(dataDir).mkdirs();`). |
| **Boş PDF** | Kaydetmeden önce içerik eklenmemiş. | `RichText` düğümünün eklendiğini ve stilin ayarlandığını doğrulayın. |
| **Desteklenmeyen yazı tipi** | Yazı tipi adı sistemde yüklü değil. | `"Arial"` gibi yaygın bir yazı tipi kullanın veya yazı tipini projeye gömün. |

## Sıkça sorulan sorular

**S: Aspose.Note, tablolar veya görüntüler gibi karmaşık biçimlendirmeleri işleyebilir mi?**  
C: Evet, API düz metnin yanı sıra tabloları, görüntüleri, hiperlinkleri ve gelişmiş düzen özelliklerini destekler.

**S: OneNote PDF'sini tekrar OneNote dosyasına dönüştürmek mümkün mü?**  
C: Doğrudan dönüşüm sağlanmaz, ancak PDF içeriğini çıkarıp API kullanarak bir OneNote belgesi yeniden oluşturabilirsiniz.

**S: Kütüphane Linux/macOS ortamlarında çalışıyor mu?**  
C: Kesinlikle. Aspose.Note for Java platform bağımsızdır; sadece uyumlu bir JDK kurulu olduğundan emin olun.

**S: Birden fazla sayfa veya taslak nasıl eklenir?**  
C: Ek `Page` ve `Outline` nesneleri oluşturup, tek sayfalı örnek gibi `Document`'e ekleyin.

**S: Daha fazla örnek nerede bulunabilir?**  
C: Resmi Aspose.Note dokümantasyonu ve [destek forumu](https://forum.aspose.com/c/note/28) birçok kod örneği ve gerçek dünya senaryosu içerir.

## Sonuç

Artık Aspose.Note for Java kullanarak **paragraf stilini ayarlamayı**, **taslak öğesi eklemeyi** ve **OneNote'u PDF'ye dışa aktarmayı** gördünüz. Stilize metni erken uygulamak, son PDF'nin profesyonel görünmesini sağlar ve tek çağrı `save` işlemi dönüşümü verimli bir şekilde gerçekleştirir. Bu temeli görüntüler, tablolar veya özel meta verilerle genişleterek uygulamanızın özel ihtiyaçlarını karşılayabilirsiniz.

---

**Son Güncelleme:** 2026-08-18  
**Test Edilen Versiyon:** Aspose.Note for Java 26.5 (latest release)  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.Note for Java ile OneNote'u PDF olarak kaydetme](/note/java/onenote-document-loading/load-save-format/)
- [Aspose.Note kullanarak PdfSaveOptions ile OneNote'u PDF'ye dönüştürmeyi öğrenin](/note/java/onenote-document-loading/load-pdf-save-options/)
- [OneNote'ta Varsayılan Paragraf Stilini Ayarlama - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}