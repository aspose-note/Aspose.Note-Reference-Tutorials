---
date: 2026-03-05
description: Aspose.Note for Java kullanarak numaralı bir liste oluştururken OneNote’u
  PDF olarak kaydetmeyi öğrenin. Varsayılan metin stilini ayarlama ve numaralandırmayı
  özelleştirme adımlarını içerir.
linktitle: Save OneNote as PDF – Create Numbered List with Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'u PDF olarak kaydedin – Aspose.Note ile Numaralı Liste Oluşturun
url: /tr/java/onenote-text-manipulation/create-numbered-list/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u PDF Olarak Kaydet – Aspose.Note ile Numaralı Liste Oluştur

## Introduction
Aspose.Note for Java, Java geliştiricilerine **OneNote'u PDF olarak kaydetme** ve belgeyi numaralı listeler gibi gelişmiş biçimlendirmelerle zenginleştirme imkanı sunar. Bu öğreticide, varsayılan metin stilini ayarlamaktan numaralandırma biçimini özelleştirmeye kadar tüm süreci adım adım göstereceğiz; böylece OneNote sayfalarınızı profesyonel görünümlü PDF'lere dışa aktarabilirsiniz.

## Quick Answers
- **Bu öğreticide ne ele alınıyor?** OneNote'ta numaralı bir liste oluşturma ve Aspose.Note for Java kullanarak dosyayı PDF olarak kaydetme.  
- **Hedeflenen anahtar kelime nedir?** *save onenote as pdf*  
- **Lisans gerekli mi?** Ücretsiz bir deneme sürümü mevcuttur; üretim ortamı için ticari lisans gereklidir.  
- **Hangi Java sürümü gerekiyor?** JDK 8 veya üzeri.  
- **Uygulama ne kadar sürer?** Temel bir liste için yaklaşık 10–15 dakika.

## What is “save OneNote as PDF”?
OneNote'u PDF olarak kaydetmek, zengin metinli OneNote sayfasını, OneNote gerektirmeden farklı platformlarda paylaşılabilen taşınabilir, sabit düzenli bir belgeye dönüştürür. Bu, arşivleme, raporlama veya OneNote yüklü olmayan kullanıcılarla içerik dağıtma gibi durumlarda özellikle faydalıdır.

## Why create a numbered list before exporting?
Numaralı bir liste, yapıyı ve okunabilirliği artırarak dışa aktarılan PDF'nin cilalı bir rapor gibi görünmesini sağlar. Aspose.Note ile **numaralandırma biçimini özelleştirebilir**, yazı tiplerini ayarlayabilir ve boşlukları kontrol edebilir; tüm bunlar orijinal OneNote düzenini korur.

## Prerequisites
Başlamadan önce şunlara sahip olduğunuzdan emin olun:

- Makinenizde Java Development Kit (JDK) kurulu olmalı.  
- Aspose.Note for Java kütüphanesini [buradan](https://releases.aspose.com/note/java/) indirin.  

## Importing Packages
İlk olarak, OneNote nesneleri ve PDF dönüşümüyle çalışabilmek için gerekli sınıfları içe aktarın.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```

## How to save OneNote as PDF with a numbered list?
Aşağıda, **liste öğeleri oluşturma**, **varsayılan metin stilini ayarlama** ve sonunda **OneNote'u PDF olarak dışa aktarma** adımlarını gösteren bir rehber bulacaksınız.

### Step 1: Initialize Document, Page, and Outline Objects
Temel OneNote yapılarını oluşturarak başlıyoruz. Bu aynı zamanda **add outline element java** kullanımını da gösterir.

```java
// Your Document Directory
String dataDir = "Your Document Directory";
// Create Document, Page, and Outline objects
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Set default text style
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```

> **Pro tip:** `dataDir` yolunu mutlak tutun veya yol sorunlarını önlemek için `System.getProperty("user.dir")` kullanın.

### Step 2: Set Default Text Style
Tutarlı bir stil, listenin tüm öğelerde aynı görünmesini sağlar.

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```

### Step 3: Create Outline Elements (Numbered List)
Burada `NumberList` kullanarak **numaralandırma biçimini özelleştiriyoruz**. `"{0})"` deseni “1)”, “2)” gibi değerler üretir.

```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Repeat for other elements (outlineElem2 and outlineElem3)
```

> **Neden Önemlidir:** Her `OutlineElement`e bir `NumberList` ekleyerek numaralandırma stili, yazı tipi ve boyutu üzerinde tam kontrol elde edersiniz.

### Step 4: Add Outline Elements to the Outline
Şimdi bireysel liste öğelerini tek bir outline içinde birleştiriyoruz.

```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

### Step 5: Attach Outline to the Page
Outline, OneNote sayfa hiyerarşisinin bir parçası haline gelir.

```java
page.appendChildLast(outline);
```

### Step 6: Save the Document as PDF
Son olarak **OneNote'u PDF olarak kaydediyoruz**. Çıktı dosyası, tanımlandığı gibi numaralı listeyi içerecektir.

```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```

Yukarıdaki kodu çalıştırdığınızda, belirttiğiniz dizinde `CreateNumberedList_out.pdf` adlı bir PDF oluşturulur ve numaralı liste biçimi korunur.

## Common Issues & Solutions
| Issue | Solution |
|-------|----------|
| **PDF is empty** | `doc.appendChildLast(page);` çağrısının `doc.save()` öncesinde yapıldığından emin olun. |
| **Numbering not displayed** | `NumberList` deseni ve `NumberFormat`'un doğru ayarlandığını kontrol edin. |
| **File not found error** | `dataDir` için mutlak bir yol kullanın veya dizini önceden oluşturun. |
| **Font mismatch** | Kodu çalıştıran makinede (ör. Arial) yazı tipini kurun. |

## Frequently Asked Questions
### Q: OneNote listemde numaralandırma formatını özelleştirebilir miyim?
A: Kesinlikle! Aspose.Note for Java tarafından sağlanan `NumberList` sınıfını kullanarak numaralandırma formatını özelleştirebilirsiniz.

### Q: Aspose.Note for Java için bir deneme sürümü mevcut mu?
A: Evet, ücretsiz bir deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.

### Q: Aspose.Note for Java için nasıl destek alabilirim?
A: Topluluk desteği için [Aspose.Note for Java forumunu](https://forum.aspose.com/c/note/28) ziyaret edin.

### Q: Aspose.Note for Java için ayrıntılı belgeleri nerede bulabilirim?
A: Kapsamlı bilgi için [belgelere](https://reference.aspose.com/note/java/) bakın.

### Q: Aspose.Note for Java için lisans nasıl satın alınır?
A: Lisansı [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

## Conclusion
Bu öğreticide, Aspose.Note for Java kullanarak **OneNote'u PDF olarak kaydetme** ve temiz bir numaralı liste oluşturma sürecini gösterdik. Varsayılan metin stilini ayarlayarak, numaralandırma biçimini özelleştirerek ve adım adım rehberi izleyerek OneNote sayfalarından hızlı ve güvenilir bir şekilde profesyonel PDF'ler üretebilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

---