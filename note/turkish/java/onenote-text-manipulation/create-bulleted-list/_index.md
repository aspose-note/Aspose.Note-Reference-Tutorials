---
title: OneNote'ta Madde İşaretli Liste Oluşturma - Aspose.Note
linktitle: OneNote'ta Madde İşaretli Liste Oluşturma - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote'ta madde işaretli listeler oluşturmaya ilişkin adım adım kılavuzu keşfedin. Belge oluşturma sürecinizi kolaylıkla geliştirin.
weight: 12
url: /tr/java/onenote-text-manipulation/create-bulleted-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Madde İşaretli Liste Oluşturma - Aspose.Note

## giriiş
Java geliştirmenin dinamik ortamında ilgi çekici ve düzenli belgeler oluşturmak çok önemlidir. Aspose.Note for Java, belge oluşturma sürecinizi geliştirmek için güçlü bir araç seti sağlar. Bu eğitim, Aspose.Note for Java'yı kullanarak OneNote'ta madde işaretli listeler oluşturma sürecinde size rehberlik edecektir. Ayrıntılara dalalım.
## Önkoşullar
Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
- Java programlamanın temel bilgisi.
-  Aspose.Note for Java kütüphanesi kuruldu. adresinden indirebilirsiniz.[Java Belgelendirmesi için Aspose.Note](https://reference.aspose.com/note/java/).
- Makinenizde kurulu bir Java Tümleşik Geliştirme Ortamı (IDE).
## Paketleri İçe Aktar
Gerekli paketleri Java projenize aktararak başlayın. Bu, Aspose.Note for Java işlevlerine erişiminizi sağlar.
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
// Aspose.Note for Java paketlerini içe aktarın
```
## 1. Adım: Belgeyi ve Sayfayı Başlatın
Document sınıfının bir nesnesini oluşturun ve bir Page sınıfı nesnesini başlatın.
```java
String dataDir = "Your Document Directory";
// Document sınıfının bir nesnesini oluşturun
Document doc = new Document();
// Sayfa sınıfı nesnesini başlat
Page page = new Page();
```
## 2. Adım: Outline'ı ve TextStyle'ı başlatın
Şimdi, biçimlendirme özellikleriyle bir Outline sınıfı nesnesini ve bir TextStyle sınıfı nesnesini başlatın.
```java
// Outline sınıfı nesnesini başlat
Outline outline = new Outline();
// TextStyle sınıfı nesnesini başlatın ve biçimlendirme özelliklerini ayarlayın
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```
## Adım 3: Madde İşaretli Liste Öğeleri Oluşturun
OutlineElement sınıfı nesneleri oluşturun ve madde işaretli bir liste oluşturmak için madde işaretleri uygulayın.
```java
// OutlineElement sınıfı nesnelerini başlatın ve madde işaretleri uygulayın
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// RichText sınıfı nesnesini başlatın ve metin stilini uygulayın
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```
Madde işaretli listenizdeki her öğe için yukarıdaki adımları tekrarlayın.
## 4. Adım: Anahat'a Anahat Öğeleri Ekleme
Oluşturulan OutlineElement nesnelerini Outline'a ekleyin.
```java
// anahat öğeleri ekle
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## 5. Adım: Sayfaya Anahat Ekleyin ve Kaydedin
Anahat düğümünü Sayfaya ekleyin ve ardından Sayfa düğümünü Belgeye ekleyin. Son olarak belgeyi kaydedin.
```java
// Anahat düğümü ekle
page.appendChildLast(outline);
// Sayfa düğümü ekle
doc.appendChildLast(page);
// belgeyi kaydet
doc.save(dataDir + "CreateBulletedList_out.pdf");
```
Tebrikler! Aspose.Note for Java'yı kullanarak OneNote'ta başarıyla madde işaretli bir liste oluşturdunuz.
## Çözüm
Aspose.Note for Java, iyi biçimlendirilmiş belgeler oluşturma sürecini basitleştirir. Bu eğitim, OneNote'ta madde işaretli liste oluşturma adımlarında size yol gösterdi. Belge oluşturma deneyiminizi geliştirmek için Aspose.Note ile daha fazla olasılığı keşfedin.
## SSS
### Aspose.Note for Java tüm Java IDE'leriyle uyumlu mu?
Evet, Aspose.Note for Java, Eclipse ve IntelliJ IDEA gibi popüler Java Entegre Geliştirme Ortamlarıyla uyumludur.
### Madde işaretli listenin formatını özelleştirebilir miyim?
Kesinlikle! Madde işaretli liste öğelerinin yazı tipini, rengini ve boyutunu tercihlerinize göre değiştirebilirsiniz.
### Aspose.Note for Java için ek desteği nerede bulabilirim?
 Ziyaret edin[Aspose.Note for Java destek forumu](https://forum.aspose.com/c/note/28) topluluktan yardım almak için.
### Aspose.Note for Java'nın ücretsiz deneme sürümü mevcut mu?
 Evet, ücretsiz deneme sürümünü keşfedebilirsiniz[Burada](https://releases.aspose.com/).
### Aspose.Note for Java için nasıl geçici lisans edinebilirim?
 Geçici lisans alın[Burada](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
