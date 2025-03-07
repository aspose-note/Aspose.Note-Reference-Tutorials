---
title: OneNote'ta Etiketli Metin Düğümü Ekleme - Aspose.Note
linktitle: OneNote'ta Etiketli Metin Düğümü Ekleme - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote'ta etiketli metin düğümlerinin nasıl ekleneceğini keşfedin. Kolay, verimli ve geliştirici dostu. Kütüphaneyi şimdi indirin!
weight: 13
url: /tr/java/onenote-tag-operations/add-text-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Etiketli Metin Düğümü Ekleme - Aspose.Note

## giriiş
Bu eğitimde, Aspose.Note for Java kullanarak OneNote'ta etiketli bir metin düğümünün nasıl ekleneceğini inceleyeceğiz. Aspose.Note, geliştiricilerin Microsoft OneNote dosyalarıyla programlı olarak çalışmasına olanak tanıyan güçlü bir Java kitaplığıdır. Etiketli metin düğümleri eklemek belge işlemede yaygın bir gerekliliktir ve Aspose.Note bu görevi basitleştirir.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
- Java programlamanın temel bilgisi.
-  Aspose.Note for Java kütüphanesi kuruldu. İndirebilirsin[Burada](https://releases.aspose.com/note/java/).
- Java geliştirme için kurulmuş bir Tümleşik Geliştirme Ortamı (IDE).
## Paketleri İçe Aktar
Java projeniz için gerekli paketleri içe aktararak başlayın. Kodunuza aşağıdaki içe aktarmaları ekleyin:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## Adım 1: Belge Nesnesi Oluşturun
OneNote belgesini temsil edecek bir Document sınıfı nesnesini başlatın:
```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";
//Document sınıfının bir nesnesini oluşturun
Document doc = new Document();
```
## Adım 2: Sayfa Sınıfı Nesnesini Başlatın
Belge içindeki sayfayı temsil edecek bir Page sınıfı nesnesi başlatın:
```java
// Sayfa sınıfı nesnesini başlat
Page page = new Page();
```
## Adım 3: Anahat Sınıfı Nesnesini Başlatın
Sayfa içindeki içeriği yapılandırmak için bir Outline sınıfı nesnesi başlatın:
```java
// Outline sınıfı nesnesini başlat
Outline outline = new Outline();
```
## Adım 4: OutlineElement Sınıfı Nesnesini Başlatın
Anahat içindeki bir öğeyi temsil etmek için bir OutlineElement sınıfı nesnesini başlatın:
```java
// OutlineElement sınıfı nesnesini başlat
OutlineElement outlineElem = new OutlineElement();
```
## Adım 5: Metin Stilini Özelleştirin
Yazı tipi rengi, adı ve boyutu gibi metin düğümü stilini ayarlayın:
```java
// Metin stilini özelleştirin
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## Adım 6: Zengin Metin Nesnesi Oluşturun
Bir RichText nesnesi oluşturun ve istediğiniz metni ona ekleyin:
```java
// RichText nesnesi oluştur
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## Adım 7: Not Etiketi Ekle
Metne sarı yıldız gibi bir not etiketi ekleyin:
```java
// Not etiketi ekle
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## Adım 8: Metin Düğümü Ekle
Metin düğümünü anahat öğesine ekleyin:
```java
// Metin düğümü ekle
outlineElem.appendChildLast(text);
```
## Adım 9: Anahat'a Anahat Öğesi Ekleme
Anahat öğesini ana hatta ekleyin:
```java
// Anahat öğesi düğümü ekle
outline.appendChildLast(outlineElem);
```
## Adım 10: Sayfaya Anahat Ekle
Taslağı sayfaya ekleyin:
```java
// Anahat düğümü ekle
page.appendChildLast(outline);
```
## Adım 11: Belgeye Sayfa Ekle
Sayfayı belgeye ekleyin:
```java
// Sayfa düğümü ekle
doc.appendChildLast(page);
```
## Adım 12: OneNote Belgesini Kaydetme
OneNote belgesini belirtilen dizine kaydedin:
```java
// OneNote belgesini kaydet
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
Tebrikler! Aspose.Note for Java'yı kullanarak OneNote'ta etiketli bir metin düğümünü başarıyla eklediniz.
## Çözüm
Bu eğitimde, Aspose.Note for Java kütüphanesini kullanarak OneNote'ta etiketli bir metin düğümü ekleme işlemini adım adım ele aldık. Bu güçlü kitaplık, belge işleme görevlerini basitleştirerek geliştiricilerin OneNote dosyalarını programlı olarak değiştirmesini kolaylaştırır.
## Sıkça Sorulan Sorular
### S: Aspose.Note for Java'yı diğer Java kütüphaneleriyle birlikte kullanabilir miyim?
C: Evet, Aspose.Note for Java, belge işleme yeteneklerini geliştirmek için diğer Java kitaplıklarıyla sorunsuz bir şekilde entegre edilebilir.
### S: Aspose.Note for Java'nın ücretsiz deneme sürümü mevcut mu?
 C: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).
### S: Aspose.Note for Java desteğini nasıl alabilirim?
C: Aspose.Note topluluğundan destek alabilirsiniz[forum](https://forum.aspose.com/c/note/28).
### S: Aspose.Note for Java için geçici lisanslar mevcut mu?
 C: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).
### S: Aspose.Note for Java belgelerini nerede bulabilirim?
 C: Belgeler mevcut[Burada](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
