---
title: OneNote'ta Kök ve Alt Sayfalarla Belge Oluşturma
linktitle: OneNote'ta Kök ve Alt Sayfalarla Belge Oluşturma
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote'ta kök ve alt sayfaları olan bir belge oluşturun. Notlarınızı verimli bir şekilde düzenlemek için adım adım kılavuzu izleyin.
type: docs
weight: 11
url: /tr/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## giriiş

Bu eğitimde, Aspose.Note for Java'yı kullanarak OneNote'ta kök ve alt sayfalardan oluşan bir belge oluşturma sürecinde size rehberlik edeceğiz. Bu adımları izleyerek OneNote belgelerinizi hiyerarşik yapıyla verimli bir şekilde düzenleyebileceksiniz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

1. Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın kurulu olduğundan emin olun.
2. Aspose.Note for Java: Aspose.Note for Java'yı şu adresten indirip yükleyin:[İnternet sitesi](https://purchase.aspose.com/buy).
3. Entegre Geliştirme Ortamı (IDE): IntelliJ IDEA, Eclipse veya NetBeans gibi bir Java IDE seçin.

## Paketleri İçe Aktar

Gerekli paketleri Java projenize aktararak başlayın:

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

## 1. Adım: Belge Dizinini Ayarlayın

OneNote belgenizi kaydetmek istediğiniz dizini tanımlayın:

```java
String dataDir = "Your Document Directory";
```

## Adım 2: Belge Nesnesi Oluşturun

 Bir örnek oluştur`Document` nesne:

```java
Document doc = new Document();
```

## 3. Adım: Sayfalar Oluşturun

Sayfa nesnelerini başlatın ve düzeylerini ayarlayın:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## 4. Adım: Sayfalara Düğümler Ekleyin

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

## Adım 5: Belgeye Sayfa Ekleme

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Adım 6: Belgeyi Kaydedin

OneNote belgesini kaydedin:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // İstisnayı işle
}
```

Tebrikler! Aspose.Note for Java'yı kullanarak OneNote'ta kök ve alt sayfaları içeren bir belgeyi başarıyla oluşturdunuz.

## Çözüm

OneNote belgelerinizi hiyerarşik yapıyla düzenlemek, daha iyi yönetim ve gezinme için çok önemlidir. Aspose.Note for Java ile kök ve alt sayfaları olan belgeleri verimli bir şekilde oluşturabilir, notlarınız için net ve düzenli bir düzen sağlayabilirsiniz.

## SSS'ler

### S1: Aspose.Note for Java'yı kullanarak birden fazla düzeyde alt sayfa oluşturabilir miyim?

Cevap1: Evet, her sayfa için uygun seviyeyi ayarlayarak birden fazla alt sayfa seviyesi oluşturabilirsiniz.

### S2: Aspose.Note for Java farklı Java IDE'leriyle uyumlu mudur?

Cevap2: Evet, Aspose.Note for Java; IntelliJ IDEA, Eclipse ve NetBeans gibi popüler Java IDE'leriyle uyumludur.

### S3: OneNote belgemdeki metnin biçimlendirmesini özelleştirebilir miyim?

Cevap3: Evet, Aspose.Note for Java'nın zengin metin özelliklerini kullanarak yazı tipini, rengini, boyutunu ve diğer formatlama seçeneklerini özelleştirebilirsiniz.

### S4: Aspose.Note for Java, belgelerin farklı formatlarda kaydedilmesini destekliyor mu?

Cevap4: Evet, Aspose.Note for Java, belgelerin BMP, PDF, PNG ve daha fazlası dahil olmak üzere çeşitli formatlarda kaydedilmesini destekler.

### S5: Aspose.Note for Java'nın deneme sürümü mevcut mu?

Cevap5: Evet, Aspose.Note for Java'nın ücretsiz deneme sürümünü web sitesinden indirebilirsiniz.