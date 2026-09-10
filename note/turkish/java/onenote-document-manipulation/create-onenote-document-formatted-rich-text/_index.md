---
date: 2026-08-18
description: Aspose.Note kullanarak Java'da onenote'yi PDF olarak kaydetmeyi öğrenin,
  OneNote belgeleri oluşturun, zengin metin biçimlendirin ve PDF'ye dışa aktarın.
  Hızlı adım‑adım rehber.
keywords:
- save onenote as pdf
- export onenote to pdf
- format rich text java
lastmod: 2026-08-18
linktitle: Java'da OneNote belgesi oluşturun ve PDF olarak kaydedin
og_description: Aspose.Note ile Java'da onenote'yi PDF olarak kaydetmeyi öğrenin.
  Bu öğreticide OneNote dosyaları oluşturma, zengin metin biçimlendirme ve PDF'ye
  dışa aktarma gösterilmektedir.
og_image_alt: Screenshot of Java code converting OneNote to PDF using Aspose.Note
og_title: Java'da onenote'yi PDF olarak kaydedin – Hızlı Aspose.Note rehberi
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to save onenote as pdf in Java using Aspose.Note, create
    OneNote documents, format rich text, and export to PDF. Quick step‑by‑step guide.
  headline: How to save onenote as pdf in Java with Aspose.Note
  type: TechArticle
- description: Learn how to save onenote as pdf in Java using Aspose.Note, create
    OneNote documents, format rich text, and export to PDF. Quick step‑by‑step guide.
  name: How to save onenote as pdf in Java with Aspose.Note
  steps:
  - name: set up document and page
    text: '`Document` is Aspose.Note''s top‑level object that represents a OneNote
      file in memory. A `Page` object holds the visual elements of a OneNote page,
      such as text, images, and containers.'
  - name: create title with formatting
    text: '`ParagraphStyle` defines alignment, indentation, and spacing for a paragraph.
      `TextStyle` defines font, size, color and other character attributes for rich‑text
      runs.'
  - name: create rich text with formatting
    text: Here we build rich‑text content using several `TextStyle` objects to demonstrate
      **rich text formatting**.
  - name: add elements to page and document
    text: Combine the title and rich text into the page hierarchy so the document
      reflects the desired structure.
  - name: save document – export onenote to pdf
    text: Finally, export the OneNote document as a PDF file in one call, preserving
      all styling and layout.
  type: HowTo
- questions:
  - answer: Yes, you can adjust additional properties such as underline, strike‑through,
      and text alignment via the `TextStyle` and `ParagraphStyle` classes.
    question: Can I customize the font styles further?
  - answer: Absolutely. As long as the IDE supports standard Java development, you
      can add the Aspose.Note JAR to the project’s classpath.
    question: Is Aspose.Note for Java compatible with all Java IDEs?
  - answer: Yes, the same code works in servlet‑based or Spring Boot applications,
      enabling dynamic OneNote‑to‑PDF generation on the server side.
    question: Can I integrate this functionality into web applications?
  - answer: A commercial license is required for production use. A temporary license
      is available for evaluation and testing.
    question: Are there licensing requirements for using Aspose.Note for Java?
  - answer: It supports PDF, HTML, PNG, JPEG, and several other export formats, giving
      you flexibility to convert OneNote pages into the format you need.
    question: Does Aspose.Note for Java support other document formats besides OneNote?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote
- Aspose.Note
- Java document automation
title: Java'da Aspose.Note ile onenote'yi PDF olarak kaydetme
url: /tr/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java ile Aspose.Note kullanarak onenote'yi pdf olarak kaydetme

## Giriş

Her başlığı, paragraf stilini ve gömülü resmi bozulmadan tutarak **save onenote as pdf** yapmanız gerekiyorsa, doğru yerdesiniz. Bu öğreticide bir OneNote belgesi oluşturmayı, özel zengin metin stilleri uygulamayı ve Aspose.Note for Java kullanarak doğrudan PDF olarak dışa aktarmayı adım adım göstereceğiz. Sonunda, herhangi bir Java projesine ekleyebileceğiniz, şık OneNote‑to‑PDF dönüşümlerini otomatikleştiren yeniden kullanılabilir bir kod parçacığına sahip olacaksınız.

## Hızlı cevaplar
- **Bu öğretici ne öğretiyor?** Stil verilen metinle bir OneNote belgesi oluşturmayı ve PDF olarak kaydetmeyi.  
- **Hangi kütüphane gerekiyor?** Aspose.Note for Java (resmi siteden indirilebilir).  
- **Lisans gerekir mi?** Test için geçici bir lisans çalışır; üretim için tam lisans gereklidir.  
- **Hangi IDE'yi kullanabilirim?** Herhangi bir Java IDE—IntelliJ IDEA, Eclipse veya NetBeans.  
- **Çıktı formatını değiştirebilir miyim?** Evet, Aspose.Note PDF, HTML, PNG ve daha fazlasını destekler.

## “save onenote pdf” nedir?
OneNote'u PDF olarak kaydetmek, hiyerarşik OneNote sayfasını—metin, resim, tablo ve biçimlendirme dahil—herhangi bir cihazda OneNote gerektirmeden açılabilen düz bir PDF belgesine dönüştürür. Dönüşüm, düzeni, yazı tiplerini ve gömülü nesneleri korur ve paylaşım, arşivleme veya yazdırma için uygun, taşınabilir, yalnızca okunabilir bir temsil sağlar.

## Java’da zengin metin biçimlendirme neden?
Java’da zengin metni biçimlendirmek, başlıkları, paragrafları ve kalın ya da renkli metin gibi satır içi öğeleri programlı olarak stil vermenizi sağlar; böylece oluşturulan OneNote sayfaları, manuel düzenleme yapmadan marka veya raporlama standartlarınıza uyar. Kodu içinde stiller uygulayarak tutarlılığı sağlarsınız, hataları azaltırsınız ve veriye ya da kullanıcı girdisine dayalı olarak dinamik belge oluşturabilirsiniz.

## Önkoşullar

1. **Java Development Kit (JDK)** – herhangi bir yeni sürüm (8 veya üzeri).  
2. **Aspose.Note for Java JAR** – [download link](https://releases.aspose.com/note/java/) adresinden indirin.  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  

## Paketleri içe aktar

Başlamadan önce, gerekli sınıfları Java dosyanıza içe aktarın:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Java’da onenote'yi pdf olarak kaydetme – adım adım kılavuz

OneNote belgenizi yükleyin, stil verilen içeriği ekleyin ve PDF dışa aktarma metodunu çağırın – bu, üç kısa adımda tam iş akışıdır.

### Adım 1: belge ve sayfayı ayarla

`Document` Aspose.Note'un bellek içinde bir OneNote dosyasını temsil eden üst‑seviye nesnesidir.  
`Page` nesnesi bir OneNote sayfasının metin, resim ve kapsayıcılar gibi görsel öğelerini tutar.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Adım 2: biçimlendirme ile başlık oluştur

`ParagraphStyle` bir paragrafın hizalamasını, girintisini ve boşluklarını tanımlar.  
`TextStyle` zengin metin akışları için yazı tipi, boyut, renk ve diğer karakter özelliklerini tanımlar.

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

### Adım 3: biçimlendirme ile zengin metin oluştur

Burada, **rich text formatting** göstermek için birkaç `TextStyle` nesnesi kullanarak zengin metin içeriği oluşturuyoruz.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

### Adım 4: öğeleri sayfaya ve belgeye ekle

Başlığı ve zengin metni sayfa hiyerarşisine birleştirerek belgenin istenen yapıyı yansıtmasını sağlayın.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Adım 5: belgeyi kaydet – onenote'u pdf olarak dışa aktar

Son olarak, tüm stil ve düzeni koruyarak OneNote belgesini tek bir çağrıyla PDF dosyası olarak dışa aktarın.

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Yaygın sorunlar ve çözümler

| Sorun | Çözüm |
|-------|----------|
| **Dosya bulunamadı** | `dataDir`'in mevcut bir klasöre işaret ettiğini ve yazma izniniz olduğunu doğrulayın. |
| **Eksik yazı tipleri** | Başvurduğunuz yazı tiplerinin (ör. *Calibri*) ana makinede yüklü olduğundan emin olun. |
| **Lisans uygulanmadı** | `Document` oluşturulmadan önce Aspose lisansınızı yükleyin, böylece değerlendirme filigranlarından kaçınırsınız. |

## Sıkça sorulan sorular

**Q: Yazı tipi stillerini daha da özelleştirebilir miyim?**  
A: Evet, `TextStyle` ve `ParagraphStyle` sınıfları aracılığıyla alt çizgi, üstü çizili ve metin hizalaması gibi ek özellikleri ayarlayabilirsiniz.

**Q: Aspose.Note for Java tüm Java IDE'leriyle uyumlu mu?**  
A: Kesinlikle. IDE standart Java geliştirmeyi desteklediği sürece, Aspose.Note JAR'ını projenin sınıf yoluna ekleyebilirsiniz.

**Q: Bu işlevi web uygulamalarına entegre edebilir miyim?**  
A: Evet, aynı kod servlet tabanlı veya Spring Boot uygulamalarında çalışır ve sunucu tarafında dinamik OneNote‑to‑PDF oluşturmayı sağlar.

**Q: Aspose.Note for Java kullanımı için lisans gereksinimleri var mı?**  
A: Üretim kullanımı için ticari bir lisans gereklidir. Değerlendirme ve test için geçici bir lisans mevcuttur.

**Q: Aspose.Note for Java OneNote dışındaki diğer belge formatlarını destekliyor mu?**  
A: PDF, HTML, PNG, JPEG ve birkaç diğer dışa aktarma formatını destekler, bu da OneNote sayfalarını ihtiyacınız olan formata dönüştürme esnekliği sağlar.

## Sonuç

Bu rehberde **OneNote belgesi oluşturmayı**, **zengin metin biçimlendirmeyi** ve Aspose.Note for Java kullanarak **onenote'yi pdf olarak kaydetmeyi** gösterdik. Adım adım talimatları izleyerek şık OneNote belgeleri oluşturmayı otomatikleştirebilir ve herhangi bir Java tabanlı çözümde PDF'ye dönüştürebilirsiniz.

---

**Son Güncelleme:** 2026-08-18  
**Test Edilen:** Aspose.Note for Java 26.5 (yazım zamanındaki en son sürüm)  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.Note kullanarak PdfSaveOptions ile OneNote'u PDF'ye Dönüştürmeyi Öğrenin](/note/java/onenote-document-loading/load-pdf-save-options/)
- [OneNote PDF'yi Akışa Kaydet - Aspose.Note](/note/java/onenote-document-saving/save-onenote-document-to-stream/)
- [OneNote'ta Belirli Sayfaları PDF Olarak Kaydet - Aspose.Note](/note/java/onenote-document-saving/specify-save-options/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}