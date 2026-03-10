---
date: 2025-12-20
description: OneNote'u PDF olarak kaydetmeyi ve Java ile Aspose.Note kütüphanesini
  kullanarak OneNote'a hiperlink eklemeyi öğrenin. OneNote'tan PDF'yi zahmetsizce
  oluşturun.
linktitle: Save OneNote as PDF and Add Hyperlink in OneNote with Java
second_title: Aspose.Note Java API
title: OneNote'u PDF olarak kaydedin ve Java ile OneNote'a hiperbağlantı ekleyin
url: /tr/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u PDF Olarak Kaydet ve OneNote'a Java ile Köprü Ekle

## Giriiş

OneNote belgelerinizi köprüler halinde değiştirebilir ve aynı zamanda PDF olarak çalıştırabilir, notlarınızın aktarımlarını büyük ölçüde artırabilir ve paylaşımını kolaylaştırabilir. Bu öğreticide **OneNote'u PDF olarak nasıl kaydedeceğinizi** ve Java ile Aspose.Note kütüphanesini kullanarak tıklanabilir bir bağlantı eklemeyi dosyalarını kullanarak. Adımları birlikte inceleyelim!

## Hızlı Yanıtlar
- **Java ile OneNote'u PDF olarak kaydedebilir miyim?** Evet, Aspose.Note for Java, PDF oluşturmak için tek bir `save` birimi sağlar.
- **Bir köprüyü nasıl eklerim?** `RichText` segmentinde `TextStyle.setHyperlinkAddress` kullanın.
- **Gereksinimler nelerdir?** JDK 8+ ve Aspose.Note for Java kütüphanesi.
- **Hangi çıkan formatları destekleniyor mu?** PDF, DOCX, XPS ve daha fazlası.
- **Üretim için lisans gerekli mi?** Evet, değerlendirme dışı kullanım için ticari bir lisans gereklidir.

## "Onenote'u pdf olarak kaydet" nedir?

OneNote defterini PDF olarak kaydeder, notlarınızın OneNote uygulaması olmadan herhangi bir cihazda açılabilir taşınabilir, yalnızca okunabilir bir kaydedilebilir oluşturur. Bu, arşivleme, yazdırma veya OneNote olmayan kullanıcılarla paylaşmak için özellikle faydalıdır.

## Neden Aspose.Note Java ile OneNote'tan PDF oluşturmalısınız?

- **Tam doğruluk:** Biçimlendirme, görseller ve köprüler korunur.
- **Programatik kontrol:** Arka uç hizmetlerinde toplu dönüşümleri otomatikleştirir.
- **Çapraz platformu:** Windows, Linux ve macOS'ta çalışır.
- **Zengin API:** Kaydedilmeden önce içerik kolayca eklenir veya verilir.

## Önkoşullar

Başlamadan önce, aşağıdaki önkoşulların sisteminizde kurulu ve ayarlanmış olduğundan emin olun:

### Java Geliştirme Kiti (JDK)

Sisteminizde Java Development Kit (JDK) yüklü olduğundan emin olun. JDK'yı [Oracle web sitesinde](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilir ve kurabilirsiniz.

### Java Kitaplığı için Aspose.Note

Aspose.Note for Java kütüphanesini indirip kurun. Belgeleri ve indirme dosyalarını [burada](https://reference.aspose.com/note/java/) bulabilirsiniz.

## Paketleri İçe Aktar

Başlamak için, Aspose.Note for Java ile çalışmak için gerekli kapları içe aktarın.

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

Şimdi verilen örneği birden çok adıma ayıralım:

## Adım 1: Belge Yapısını Ayarlayın

İlk olarak, içeriğin içerdiği yeni bir belge ve sayfa birleştirilir.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Adım 2: Varsayılan Metin Stilini Tanımlayın

Çoğu metin öğesine uygulanacak varsayılan paragraf stilini tanımlayın.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Adım 3: Başlık Metnini Ayarlayın

Sayfa için bir başlık oluşturun ve varsayılan stili uygulayın.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Adım 4: Anahat ve Anahat Öğelerini Oluşturun

Outline'lar, paragraflar ve diğer öğeler için kapsayıcılar gibi davranır.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Adım 5: Köprü için Metin Stilini Tanımlayın

Burada, tıklanabilir kısım için kullanılacak kırmızı renkli stili tanımlıyoruz.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Adım 6: Köprü İçeren Metni Ekleyin

Şimdi normal metin ve bir köprü içeren bir `RichText` nesnesi oluşturuyoruz. `setHyperlinkAddress` yöntemi Aspose.Note'a bu segmentin tıklanabilir olması gerektiğini söyler.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Adım 7: Anahatı Sayfaya ve Sayfayı Belgeye Ekleyin

Outline öğesini outline'a, outline'ı sayfaya ve son olarak sayfayı belgeye ekleyin.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Adım 8: Belgeyi PDF Olarak Kaydedin

Son adım, OneNote belgesini PDF dosyası olarak kaydetmektir. Bu, ana anahtar kelime **save onenote as pdf** burada devreye girer.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Çözüm

Tebrikler! Java ve Aspose.Note kütüphanesini kullanarak **OneNote'u PDF olarak kaydettiniz** ve belgeye bir köprü eklediniz. Bu özellik, OneNote içeriğinizden etkileşimli, paylaşılabilir PDF'ler oluşturmanızı sağlar.

## Sıkça Sorulan Sorular

**S: Köprünün görünümünü nasıl değiştirebilirim?**
C: `setHyperlinkAddress` çağrısından önce `setFontColor`, `setUnderline` veya `setFontName` gibi `TextStyle` özelliklerini kullanın.

**S: Belgeyi PDF dışındaki formatlarda kaydedebilir miyim?**
C: Evet, Aspose.Note DOCX, XPS, HTML ve çeşitli diğer kullanılabilir formatlarını kullanılabilir.

**S: Mevcut bir OneNote içeriğine köprü eklemem gerekirse?**
C: `new Document("input.one")` ile mevcut olanı yükleyin, içeriği gösterildiği gibi ve ardından istediğiniz formatta `save` çağırın.

**S: PDF içerdiğinden sonra köprüyü programlı olarak açmanın bir yolu var mı?**
C: PDF görüntüleyici tıklanabilir bağlantılar otomatik olarak işler; ek bir kod gerekmez.

**S: Geliştirme kullanımı için lisans gerekli mi?**
C: Geçici bir değerlendirme lisansı geliştirme ve test için yeterlidir, ancak üretim sunumları için tam lisans gereklidir.

---

**Son Güncelleme:** 2025-12-20
**Şunlarla Test Edildi:** Java 23.12 için Aspose.Note
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}