---
title: OneNote'ta Numaralı Liste Oluşturma - Aspose.Note
linktitle: OneNote'ta Numaralı Liste Oluşturma - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java ile OneNote'ta zahmetsizce numaralandırılmış bir liste oluşturmayı öğrenin. Ücretsiz deneme sürümünü indirin ve Java geliştirme dünyasına dalın!
type: docs
weight: 14
url: /tr/java/onenote-text-manipulation/create-numbered-list/
---
## giriiş
Aspose.Note for Java, Java geliştiricilerinin Microsoft OneNote dosyalarıyla sorunsuz bir şekilde çalışmasını sağlar. Bu eğitimde, güçlü Aspose.Note for Java kütüphanesini kullanarak OneNote'ta numaralandırılmış bir liste oluşturma sürecinde size yol göstereceğiz.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
- Makinenize Java Development Kit'i (JDK) yüklediniz.
-  Aspose.Note for Java kütüphanesi şuradan indirildi:[Burada](https://releases.aspose.com/note/java/).
## Paketleri İçe Aktarma
Öncelikle Aspose.Note işlevselliklerinden en iyi şekilde yararlanmak için Java projenize gerekli paketleri aktaralım. Projenize aşağıdaki kodu ekleyin:
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
## Adım 1: Belgeyi, Sayfayı ve Anahat Nesnelerini Başlatma
```java
// Belge Dizininiz
String dataDir = "Your Document Directory";
// Belge, Sayfa ve Anahat nesneleri oluşturma
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Varsayılan metin stilini ayarla
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Adım 2: Varsayılan Metin Stilini Ayarlama
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Adım 3: Anahat Öğeleri Oluşturma
Şimdi numaralı listeniz için öğeleri oluşturalım.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Diğer öğeler için tekrarlayın (outlineElem2 ve anahatElem3)
```
## Adım 4: Outline'a Anahat Öğeleri Ekleme
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Adım 5: Sayfaya Anahat Ekleme
```java
page.appendChildLast(outline);
```
## Adım 6: Belgeyi Kaydetme
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Bu adımları titizlikle takip ettiğinizde Aspose.Note for Java'yı kullanarak OneNote'ta zahmetsizce numaralandırılmış bir liste oluşturacaksınız.
## Çözüm
Bu eğitimde, Aspose.Note for Java'yı kullanarak OneNote'ta numaralandırılmış bir liste oluşturmanın kusursuz sürecini araştırdık. Kitaplığın güçlü özellikleri, onu Microsoft OneNote dosyalarıyla çalışan Java geliştiricileri için paha biçilmez bir araç haline getiriyor.
## Sıkça Sorulan Sorular
### S: OneNote listemdeki numaralandırma biçimini özelleştirebilir miyim?
C: Kesinlikle! Aspose.Note for Java tarafından sağlanan NumberList sınıfını kullanarak numaralandırma formatını özelleştirebilirsiniz.
### S: Aspose.Note for Java'nın deneme sürümü mevcut mu?
 C: Evet, ücretsiz deneme sürümünü indirebilirsiniz[Burada](https://releases.aspose.com/).
### S: Aspose.Note for Java desteğini nasıl alabilirim?
 C: Ziyaret edin[Java forumu için Aspose.Note](https://forum.aspose.com/c/note/28) topluluk desteği için.
### S: Aspose.Note for Java'nın ayrıntılı belgelerini nerede bulabilirim?
 C: Bkz.[dokümantasyon](https://reference.aspose.com/note/java/) kapsamlı bilgi için.
### S: Aspose.Note for Java lisansını nasıl satın alabilirim?
 C: Lisans satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).