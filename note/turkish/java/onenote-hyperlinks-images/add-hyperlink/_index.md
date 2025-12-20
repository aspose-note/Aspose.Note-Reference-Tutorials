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

## Introduction

OneNote belgelerinize köprüler eklemek ve aynı zamanda PDF olarak kaydetmek, notlarınızın etkileşimini büyük ölçüde artırabilir ve paylaşımı kolaylaştırabilir. Bu öğreticide **OneNote'u PDF olarak nasıl kaydedeceğinizi** ve Java ile Aspose.Note kütüphanesini kullanarak tıklanabilir bir bağlantı eklemeyi öğreneceksiniz. Adımları birlikte inceleyelim!

## Quick Answers
- **Java ile OneNote'u PDF olarak kaydedebilir miyim?** Evet, Aspose.Note for Java, PDF oluşturmak için tek bir `save` çağrısı sağlar.
- **Bir köprüyü nasıl eklerim?** `RichText` segmentinde `TextStyle.setHyperlinkAddress` kullanın.
- **Gereksinimler nelerdir?** JDK 8+ ve Aspose.Note for Java kütüphanesi.
- **Hangi çıktı formatları destekleniyor?** PDF, DOCX, XPS ve daha fazlası.
- **Üretim için lisans gerekli mi?** Evet, değerlendirme dışı kullanım için ticari bir lisans gereklidir.

## What is “save onenote as pdf”?

OneNote defterini PDF olarak kaydetmek, notlarınızın OneNote uygulaması olmadan herhangi bir cihazda açılabilen taşınabilir, yalnızca okunabilir bir sürümünü oluşturur. Bu, arşivleme, yazdırma veya OneNote olmayan kullanıcılarla paylaşma için özellikle faydalıdır.

## Why generate PDF from OneNote with Aspose.Note Java?

- **Tam doğruluk:** Biçimlendirme, görseller ve köprüler korunur.
- **Programatik kontrol:** Arka uç hizmetlerinde toplu dönüşümleri otomatikleştirin.
- **Çapraz platform:** Windows, Linux ve macOS'ta çalışır.
- **Zengin API:** Kaydetmeden önce içeriği kolayca ekleyin veya değiştirin.

## Prerequisites

Before we begin, ensure you have the following prerequisites installed and set up on your system:

### Java Development Kit (JDK)

Sisteminizde Java Development Kit (JDK) yüklü olduğundan emin olun. JDK'yı [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) indirebilir ve kurabilirsiniz.

### Aspose.Note for Java Library

Aspose.Note for Java kütüphanesini indirin ve kurun. Belgeleri ve indirme bağlantısını [burada](https://reference.aspose.com/note/java/) bulabilirsiniz.

## Import Packages

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

Now, let's break down the provided example into multiple steps:

## Step 1: Set Up Document Structure

İlk olarak, içeriğin yer alacağı yeni bir belge ve sayfa oluşturun.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Step 2: Define Default Text Style

Çoğu metin öğesine uygulanacak varsayılan paragraf stilini tanımlayın.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Step 3: Set Title Text

Sayfa için bir başlık oluşturun ve varsayılan stili uygulayın.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Step 4: Create Outline and Outline Elements

Outline'lar, paragraflar ve diğer öğeler için kapsayıcılar gibi davranır.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Step 5: Define Text Style for Hyperlink

Burada, tıklanabilir kısım için kullanılacak kırmızı renkli stili tanımlıyoruz.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Step 6: Add Text with Hyperlink

Şimdi normal metin ve bir köprü içeren bir `RichText` nesnesi oluşturuyoruz. `setHyperlinkAddress` yöntemi Aspose.Note'a bu segmentin tıklanabilir olması gerektiğini söyler.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Step 7: Add Outline to Page and Page to Document

Outline öğesini outline'a, outline'ı sayfaya ve son olarak sayfayı belgeye ekleyin.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Step 8: Save the Document as PDF

Son adım, OneNote belgesini PDF dosyası olarak kaydetmektir. Bu, ana anahtar kelime **save onenote as pdf** burada devreye girer.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Conclusion

Tebrikler! Java ve Aspose.Note kütüphanesini kullanarak **OneNote'u PDF olarak kaydettiniz** ve belgeye bir köprü eklediniz. Bu özellik, OneNote içeriğinizden doğrudan etkileşimli, paylaşılabilir PDF'ler oluşturmanızı sağlar.

## FAQ's

### Q1: Is Aspose.Note compatible with all versions of Java?

A1: Evet, Aspose.Note for Java, JDK 8 ve üzeri dahil olmak üzere tüm büyük Java sürümlerini destekler.

### Q2: Can I add multiple hyperlinks in a single document using Aspose.Note?

A2: Kesinlikle! Aspose.Note for Java kullanarak OneNote belgenizde ihtiyacınız kadar köprü ekleyebilirsiniz.

### Q3: Does Aspose.Note offer support for other programming languages?

A3: Evet, Aspose.Note .NET, Python ve Android dahil çeşitli programlama dilleri için kütüphaneler sağlar.

### Q4: Is Aspose.Note easy to integrate into existing Java projects?

A4: Evet, Aspose.Note'u Java projelerinize entegre etmek basittir ve iyi belgelenmiştir, bu da başlamayı kolaylaştırır.

### Q5: Where can I find more help and resources for using Aspose.Note?

A5: [Aspose.Note forumunda](https://forum.aspose.com/c/note/28/) kapsamlı belgeler, öğreticiler ve topluluk desteği bulabilirsiniz.

## Frequently Asked Questions

**S: Köprünün görünümünü nasıl özelleştirebilirim?**  
C: `setHyperlinkAddress` çağırmadan önce `setFontColor`, `setUnderline` veya `setFontName` gibi `TextStyle` özelliklerini kullanın.

**S: Belgeyi PDF dışındaki formatlarda kaydedebilir miyim?**  
C: Evet, Aspose.Note DOCX, XPS, HTML ve çeşitli diğer dışa aktarım formatlarını destekler.

**S: Mevcut bir OneNote dosyasına köprü eklemem gerekirse?**  
C: `new Document("input.one")` ile mevcut dosyayı yükleyin, içeriği gösterildiği gibi değiştirin ve ardından istediğiniz formatta `save` çağırın.

**S: PDF oluşturulduktan sonra köprüyü programlı olarak açmanın bir yolu var mı?**  
C: PDF görüntüleyici tıklanabilir bağlantıları otomatik olarak işler; ek bir kod gerekmez.

**S: Geliştirme kullanımı için lisans gerekli mi?**  
C: Geçici bir değerlendirme lisansı geliştirme ve test için yeterlidir, ancak üretim dağıtımları için tam lisans gereklidir.

---

**Last Updated:** 2025-12-20  
**Tested With:** Aspose.Note for Java 23.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}