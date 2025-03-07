---
title: OneNote'ta Etiketli Yeni Görüntü Düğümü Ekleme - Aspose.Note
linktitle: OneNote'ta Etiketli Yeni Görüntü Düğümü Ekleme - Aspose.Note
second_title: Aspose.Note Java API'si
description: Aspose.Note for Java'yı kullanarak OneNote'ta etiketli yeni bir görüntü düğümünün nasıl ekleneceğini öğrenin. Java programlama becerilerinizi zahmetsizce geliştirin.
weight: 10
url: /tr/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Etiketli Yeni Görüntü Düğümü Ekleme - Aspose.Note

## giriiş
Java programlama alanında Aspose.Note, OneNote belgelerini kolaylıkla yönetmeye yönelik güçlü bir araç olarak öne çıkıyor. Becerilerinizi geliştirmek ve Aspose.Note'u kullanarak OneNote'ta etiketli yeni bir görüntü düğümünü nasıl ekleyeceğinizi öğrenmek istiyorsanız, doğru yere geldiniz. Bu adım adım kılavuz, süreç boyunca size yol gösterecek ve her konsepti iyice kavramanızı sağlayacaktır.
## Önkoşullar
Eğiticiye dalmadan önce, ihtiyacınız olan her şeye sahip olduğunuzdan emin olalım:
1.  Aspose.Note for Java: Aspose.Note kütüphanesinin kurulu olduğundan emin olun. Değilse indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).
2. Java Geliştirme Ortamı: Makinenizde çalışan bir Java geliştirme ortamının kurulu olduğundan emin olun.
Artık önkoşulları yerine getirdiğimize göre sonraki adımlara geçebiliriz.
## Paketleri İçe Aktar
Java projenizde gerekli paketleri içe aktararak başlayın:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Adım 1: Belge Nesnesi Oluşturun
```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory";
// Document sınıfının bir nesnesini oluşturun
Document doc = new Document();
```
## Adım 2: Sayfa Sınıfı Nesnesini Başlatın
```java
// Sayfa sınıfı nesnesini başlat
Page page = new Page();
```
## Adım 3: Anahat Sınıfı Nesnesini Başlatın
```java
// Outline sınıfı nesnesini başlat
Outline outline = new Outline();
```
## Adım 4: OutlineElement Sınıfı Nesnesini Başlatın
```java
// OutlineElement sınıfı nesnesini başlat
OutlineElement outlineElem = new OutlineElement();
```
## Adım 5: Görüntüyü Yükleyin ve Ekleyin
```java
// bir resim yükle
Image image = new Image(null, dataDir + "Input.jpg");
// belge düğümüne resim ekle
outlineElem.appendChildLast(image);
```
## Adım 6: Resme Not Etiketi Ekleme
```java
// resme sarı yıldız notu etiketi ekleyin
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Adım 7: Anahat Öğesi Düğümünü Ekleyin
```java
// anahat öğesi düğümü ekle
outline.appendChildLast(outlineElem);
```
## Adım 8: Anahat Düğümü Ekle
```java
// anahat düğümü ekle
page.appendChildLast(outline);
```
## Adım 9: Sayfa Düğümü Ekle
```java
// sayfa düğümü ekle
doc.appendChildLast(page);
```
## Adım 10: OneNote Belgesini Kaydetme
```java
// OneNote belgesini PDF olarak kaydetme
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Tebrikler! Aspose.Note for Java'yı kullanarak OneNote'ta etiketli yeni bir görüntü düğümünü başarıyla eklediniz.
## Çözüm
 Aspose.Note for Java'ya hakim olmak, OneNote belge manipülasyonunda heyecan verici olasılıkların kapısını açar. Bu öğreticiyi takip ederek çeşitli projelere uygulanabilecek pratik bir beceri kazandınız. Aspose.Note belgelerini keşfetmeye devam edin[Burada](https://reference.aspose.com/note/java/)daha gelişmiş özellikler ve olanaklar için.
## SSS
### Aspose.Note belgelerini nerede bulabilirim?
 Belgeleri bulabilirsiniz[Burada](https://reference.aspose.com/note/java/).
### Aspose.Note for Java'yı nasıl indirebilirim?
 Sürümler sayfasından indirebilirsiniz[Burada](https://releases.aspose.com/note/java/).
### Ücretsiz deneme mevcut mu?
 Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).
### Aspose.Note için nereden destek alabilirim?
 Topluluk forumunu ziyaret edin[Burada](https://forum.aspose.com/c/note/28) destek için.
### Geçici lisansa ihtiyacım var mı?
 Gerekirse geçici lisans alabilirsiniz.[Burada](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
