---
date: 2026-07-29
description: Java ve Aspose.Note kullanarak embed link onenote, OneNote'u PDF olarak
  kaydetmeyi ve hyperlink eklemeyi öğrenin. OneNote'u PDF'ye zahmetsizce dışa aktarın.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: Java ile OneNote'u PDF olarak kaydedin ve OneNote içinde hyperlink ekleyin
og_description: Java ve Aspose.Note kullanarak embed link onenote ve OneNote'u PDF'ye
  dışa aktarın. Adım adım hyperlink eklemeyi ve PDF oluşturmayı öğrenin.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Embed Link onenote – Java ile OneNote'u PDF olarak kaydedin
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: Embed Link onenote – Java ile OneNote'u PDF olarak kaydedin
url: /tr/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u PDF olarak kaydedin ve OneNote içinde Java ile Köprü ekleyin

## Giriş

Bir defteri taşınabilir bir PDF'ye dönüştürürken **embed link onenote** eklemeniz gerekiyorsa, doğru yerdesiniz. Bu öğretici, OneNote'u PDF olarak kaydetmeyi ve Java ile Aspose.Note kütüphanesini kullanarak tıklanabilir köprüler eklemeyi adım adım gösterir. Bu yaklaşımın arşivleme, paylaşma ve belge iş akışlarını otomatikleştirme açısından neden ideal olduğunu göreceksiniz.

## Hızlı Yanıtlar
- **OneNote'u Java ile PDF olarak kaydedebilir miyim?** Evet, Aspose.Note for Java, PDF oluşturmak için tek bir `save` çağrısı sağlar.
- **Bir köprüyü nasıl eklerim?** `RichText` segmentinde `TextStyle.setHyperlinkAddress` kullanın.
- **Önkoşullar nelerdir?** JDK 8+ ve Aspose.Note for Java kütüphanesi.
- **Hangi çıktı formatları destekleniyor?** PDF, DOCX, XPS ve daha fazlası.
- **Üretim için lisans gerekli mi?** Evet, değerlendirme dışı kullanım için ticari bir lisans gereklidir.

## “save onenote as pdf” nedir?

OneNote defterini PDF olarak kaydetmek, herkesin OneNote uygulaması olmadan açabileceği, yalnızca okunabilir, çok platformlu bir sürüm oluşturur. Bu format, arşivleme, yazdırma veya OneNote yüklü olmayan iş ortaklarıyla paylaşma için idealdir ve orijinal düzen, görseller ve gömülü köprüler korunur.

## Neden OneNote'tan Aspose.Note Java ile PDF oluşturmalısınız?

Aspose.Note for Java, **export onenote to pdf** işlemini %100 düzen sadakatiyle yapabilir, belge başına 200 sayfaya kadar bellek içine tüm dosyayı yüklemeden işleyebilir. Kütüphane, görseller, tablolar ve köprü stillerinin %95'i dahil olmak üzere 30'dan fazla içerik türünü işler; böylece orijinal defterin sadık bir kopyasını elde edersiniz. Ayrıca Windows, Linux ve macOS üzerinde çalışır, bulut ya da yerel hizmetlerde toplu dönüşümlere olanak tanır.

## Önkoşullar

Başlamadan önce, sisteminizde aşağıdaki önkoşulların yüklü ve yapılandırılmış olduğundan emin olun:

### Java Geliştirme Kiti (JDK)

Sisteminize Java Development Kit (JDK)'in yüklü olduğundan emin olun. JDK'yi [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilir ve kurabilirsiniz.

### Aspose.Note for Java Kütüphanesi

Aspose.Note for Java kütüphanesini indirin ve kurun. Dokümantasyonu ve indirme bağlantısını [burada](https://reference.aspose.com/note/java/) bulabilirsiniz.

## Paketleri İçe Aktarma

Başlamak için, Aspose.Note for Java ile çalışmak için gerekli paketleri içe aktarın.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Şimdi, verilen örneği birden fazla adıma ayıralım:

## PDF olarak kaydederken embed link onenote nasıl eklenir?

Yeni bir `Document` örneği yükleyin, sayfa yapısını oluşturun, köprü için kırmızı renkli bir `TextStyle` tanımlayın ve sonunda `document.save("output.pdf", SaveFormat.Pdf)` çağrısını yapın. Bu sıralama, tüm orijinal biçimlendirme ve görselleri koruyan, tam işlevsel bir köprü içeren bir PDF oluşturur.

## Adım 1: Document Yapısını Oluşturma

`Document`, Aspose.Note içinde bir OneNote defterini temsil eder.  
`Page`, taslaklar ve diğer sayfa‑seviyesi öğeler için bir kapsayıcıdır.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Adım 2: Varsayılan Metin Stili Tanımlama

`ParagraphStyle`, hizalama, boşluk ve girinti gibi paragraf varsayılan biçimlendirmesini tanımlar.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Adım 3: Başlık Metnini Ayarlama

`Title`, bir OneNote belgesindeki sayfa başlığı öğesini temsil eder.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Adım 4: Outline ve Outline Elemanlarını Oluşturma

`Outline`, içerik bloklarının hiyerarşisi için bir kapsayıcı görevi görür.  
`OutlineElement`, bir taslak içinde paragraf veya tablo gibi bireysel bir elemandır.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Adım 5: Köprü İçin Metin Stilini Tanımlama

`TextStyle`, yazı tipleri, renk ve alt çizgi ayarları dahil olmak üzere metin akışlarının görsel görünümünü kontrol eder.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Adım 6: Köprü ile Metin Ekleme

`RichText`, bir paragrafta biçimlendirilmiş metin akışını temsil eder. Bir köprü adresi ayarlamak, metnin dışa aktarılan PDF'de tıklanabilir olmasını sağlar.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Adım 7: Outline'ı Sayfaya ve Sayfayı Document'e Ekleme

Bu adım, önceden oluşturulan outline elemanlarını sayfaya ekler ve ardından sayfayı `Document` nesnesine ekler.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Adım 8: Belgeyi PDF Olarak Kaydetme

`SaveFormat.Pdf`, Aspose.Note'a belgeyi PDF formatında dışa aktarmasını söyler.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Sonuç

Tebrikler! Java ve Aspose.Note kütüphanesini kullanarak **OneNote'u PDF olarak kaydettiniz** ve belgeye bir köprü eklediniz. Bu özellik, **embed link onenote** yapmanıza ve OneNote içeriğinizden doğrudan etkileşimli, paylaşılabilir PDF'ler oluşturmanıza olanak tanır.

## Sıkça Sorulan Sorular

**S: Köprünün görünümünü nasıl özelleştirebilirim?**  
C: `setHyperlinkAddress` çağrısından önce `setFontColor`, `setUnderline` veya `setFontName` gibi `TextStyle` özelliklerini kullanın.

**S: Belgeyi PDF dışındaki formatlarda kaydedebilir miyim?**  
C: Evet, Aspose.Note DOCX, XPS, HTML ve birkaç diğer dışa aktarma formatını destekler.

**S: Mevcut bir OneNote dosyasına köprü eklemem gerekirse?**  
C: `new Document("input.one")` ile mevcut dosyayı yükleyin, içeriği gösterildiği gibi değiştirin ve ardından istediğiniz formatta `save` çağrısını yapın.

**S: PDF oluşturulduktan sonra köprüyü programlı olarak açmanın bir yolu var mı?**  
C: PDF görüntüleyici tıklanabilir köprüleri otomatik olarak işler; ek bir kod gerekmez.

**S: Geliştirme kullanımı için lisansa ihtiyacım var mı?**  
C: Geçici bir değerlendirme lisansı geliştirme ve test için yeterlidir, ancak üretim dağıtımları için tam lisans gereklidir.

---

**Last Updated:** 2026-07-29  
**Tested With:** Aspose.Note for Java 26.4  
**Author:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## İlgili Öğreticiler

- [Aspose.Note for Java ile OneNote'u PDF olarak Kaydetme](/note/java/onenote-document-loading/load-save-format/)
- [Aspose.Note ile PdfSaveOptions kullanarak OneNote'u PDF'ye Dönüştürme](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Java ile OneNote'ta Görsele Köprü Ekleme](/note/java/onenote-hyperlinks-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}