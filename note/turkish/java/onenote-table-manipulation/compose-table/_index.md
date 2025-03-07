---
title: OneNote'ta Tablo Oluşturma - Aspose.Note
linktitle: OneNote'ta Tablo Oluşturma - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote'ta programlı olarak tablo oluşturmayı öğrenin. Verimli belge oluşturmak için adım adım kılavuz.
weight: 11
url: /tr/java/onenote-table-manipulation/compose-table/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Tablo Oluşturma - Aspose.Note

## giriiş
Günümüzün rekabetçi iş ortamında etkili iletişim ve işbirliği başarıya ulaşmada temel faktörlerdir. Aspose.Note for Java, OneNote belgelerini programlı olarak oluşturmak ve değiştirmek için güçlü bir çözüm sunar. Bu eğitimde Aspose.Note for Java kullanarak OneNote'ta tabloların nasıl oluşturulacağını inceleyeceğiz. Belge oluşturma sürecinizi geliştirmek için aşağıdaki adım adım kılavuzu izleyin.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
- Java programlamanın temel bilgisi.
-  Aspose.Note for Java kütüphanesi kuruldu. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).
- Java geliştirme için kurulmuş bir entegre geliştirme ortamı (IDE).
## Paketleri İçe Aktar
Projenizi başlatmak için gerekli paketleri içe aktardığınızdan emin olun. Aşağıdaki içe aktarma ifadelerini Java sınıfınıza ekleyin:
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```
## 1. Adım: Belge Dizinini Ayarlayın
```java
String dataDir = "Your Document Directory";
```
"Belge Dizininiz"i, OneNote belgenizi kaydetmek istediğiniz asıl yolla değiştirdiğinizden emin olun.
## Adım 2: Başlık Oluşturun
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
Belgeniz için göz alıcı bir başlık oluşturun. Yazı tipi boyutunu, kalınlığını ve hizalamasını gerektiği gibi ayarlayın.
## 3. Adım: Sayfa ve Anahat Oluşturun
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
Yeni bir sayfa ve taslak oluşturun, ardından önceden oluşturulan başlığı taslağa ekleyin.
## 4. Adım: Özet Metni Ekleyin
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
Tabloya bağlam sağlamak için kısa bir özet metni ekleyin.
## Adım 5: Tablo Oluşturun
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// Geriye kalan adımlar tablo yapısının, başlık satırının ve boş satırların eklenmesiyle ilgilidir.
// Ayrıntılı uygulama için sağlanan koda bakın.
```
Tablo yapısını oluşturun ve ilgili bilgilerle doldurun. Sağlanan kod, 'Kişiler' sütunu için sütunların, başlık satırının, boş satırların ve şablon içeriğinin eklenmesini içerir.
## Adım 6: Belgeyi Kaydet
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
Oluşturduğunuz belgeyi belirtilen dosya adı ve dizin yoluyla kaydedin.
## Çözüm
Tebrikler! Aspose.Note for Java'yı kullanarak OneNote'ta başarıyla bir tablo oluşturdunuz. Bu eğitimde, belge oluşturma yeteneklerinizi programlı olarak geliştirmenize olanak tanıyan adım adım süreç gösterildi.
## Sıkça Sorulan Sorular
### S: Aspose.Note for Java belgelerini nerede bulabilirim?
 Belgelere başvurabilirsiniz[Burada](https://reference.aspose.com/note/java/).
### S: Aspose.Note for Java'yı nasıl indirebilirim?
 Şuradan indirebilirsiniz[bu bağlantı](https://releases.aspose.com/note/java/).
### S: Ücretsiz deneme mevcut mu?
 Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).
### S: Aspose.Note for Java desteğini nereden alabilirim?
 Destek forumunu ziyaret edin[Burada](https://forum.aspose.com/c/note/28).
### Soru: Geçici lisans alabilir miyim?
 Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
