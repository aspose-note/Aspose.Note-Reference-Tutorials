---
date: 2026-01-28
description: OneNote'ta taslak oluşturmayı, OneNote'a etiket eklemeyi ve Aspose.Note
  for Java kullanarak OneNote'tan PDF oluşturmayı öğrenin.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'ta Anahat Oluştur ve Etiket Ekle – Aspose.Note
url: /tr/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Taslak Oluşturma ve Etiket Ekleme – Aspose.Note

## Giriş
Java kullanarak **OneNote'ta taslak oluşturma** ve etiketlerle iş birliğini artırmak ister misiniz? Aspose.Note for Java, etiket eklemeyi, notlarınızı yapılandırmayı ve hatta **OneNote dosyalarından PDF oluşturmayı** oldukça basit hâle getirir. Bu öğreticide her adımı ayrıntılı olarak inceleyecek, *neden* önemli olduğunu açıklayacak ve sonunda şık bir PDF üretmeyi göstereceğiz.

## Hızlı Yanıtlar
- **“OneNote'ta taslak oluşturma” ne anlama geliyor?** İçeriği başlıklar ve alt‑bölümler gibi hiyerarşik bir yapı (taslaklar) içinde düzenler.  
- **Hangi kütüphane OneNote'a etiket ekler?** Aspose.Note for Java, görsel işaretler için `NoteTag` sınıfını sağlar.  
- **Sonucu PDF olarak dışa aktarabilir miyim?** Evet – `SaveFormat.Pdf` kullanarak **OneNote'tan PDF oluşturabilirsiniz**.  
- **Üretim ortamı için lisansa ihtiyacım var mı?** Test için geçici bir lisans mevcuttur; ticari kullanım için tam lisans gereklidir.  
- **Ana önkoşullar nelerdir?** JDK kurulumu, Aspose.Note for Java kütüphanesi ve temel Java bilgisi.

## “OneNote'ta taslak oluşturma” nedir?
OneNote'ta bir taslak oluşturmak, notlarınız için ağaç‑gibi bir yapı tanımlayan `Outline` ve `OutlineElement` nesnelerini eklemek anlamına gelir. Bu hiyerarşi, bir belge içindeki başlıklar gibi bilgileri daraltıp genişletmenize ve düzenlemenize olanak tanır.

## Neden OneNote'a etiket eklenir?
Yıldızlar, onay işaretleri veya özel simgeler gibi etiketler, okuyuculara görsel ipuçları sunar, aranabilirliği artırır ve ekiplerin öğeleri önceliklendirmesine yardımcı olur. Aspose.Note ile programlı olarak herhangi bir metin parçasına `NoteTag` ekleyebilirsiniz.

## Önkoşullar
Başlamadan önce şunların kurulu olduğundan emin olun:
- Java Development Kit (JDK) yüklü.
- Aspose.Note for Java kütüphanesi indirildi. **[buradan](https://releases.aspose.com/note/java/)** edinebilirsiniz.
- Java programlamaya temel bir hakimiyet.

## Paketleri İçe Aktarma
Projenizi başlatmak için gerekli paketleri içe aktardığınızdan emin olun:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
Yukarıdaki kodu adım‑adım bir rehbere dönüştürelim.

## Adım 1: Belge ve Sayfayı Ayarlama
Yeni bir `Document` nesnesi oluşturup bir `Page` nesnesi başlatın:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```
Burada, belgeler dizinine yolu ayarlıyor, yeni bir `Document` oluşturuyor ve bir `Page` başlatıyoruz.

## Adım 2: Taslak Oluşturma
İçeriğinizi yapılandırmak için bir `Outline` nesnesi oluşturun:
```java
Outline outline = new Outline();
```
Taslaklar, belgenize hiyerarşik bir yapı kazandırır, **OneNote'ta taslak oluşturmayı** kolaylaştırır ve bilgiyi düzenli tutar.

## Adım 3: OutlineElement ve ParagraphStyle Başlatma
Şimdi bir `OutlineElement` başlatın ve metin biçimlendirme için `ParagraphStyle` ayarlayın:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
`OutlineElement`, taslak içindeki bir öğeyi temsil eder; `ParagraphStyle` ise metin biçimlendirme özelliklerini tanımlar.

## Adım 4: RichText ve NoteTag Ekleme
Bir `RichText` nesnesi oluşturun, OneNote metninizi ekleyin ve bir `NoteTag` ekleyin:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
`RichText`, biçimlendirilmiş metin eklemenizi sağlar ve `NoteTag` **OneNote'a etiket ekler** ve görsel bir işaret oluşturur.

## Adım 5: Taslak Yapısını Oluşturma
Metin düğümünü, outline element düğümünü ve outline düğümünü ekleyerek belgenin yapısını inşa edin:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
Bu adım, içeriğinizin belge içinde düzenli olmasını sağlar ve **OneNote'ta taslak oluşturma** sürecini tamamlar.

## Adım 6: Belgeyi Kaydetme
Belgeyi PDF formatında kaydedin; bu işlem **OneNote'tan PDF oluşturur**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
Artık eklenmiş etiketlerle OneNote belgeniz PDF olarak kaydedildi.

Bu adımları izleyerek Aspose.Note for Java ile OneNote belgelerinizi zahmetsizce geliştirebilirsiniz.

## Sonuç
Bu öğreticide **OneNote'ta taslak oluşturma**, OneNote'a etiket ekleme ve ardından Aspose.Note for Java kullanarak **OneNote'tan PDF oluşturma** konularını ele aldık. Java sayesinde not yapısı, görsel etiketleme ve dışa aktarma seçenekleri üzerinde tam kontrol elde eder, notlarınızı daha düzenli ve paylaşılabilir hâle getirirsiniz.

## SSS
### 1. Aspose.Note for Java’yı başka programlama dilleriyle kullanabilir miyim?
Aspose.Note öncelikle Java’yı destekler, ancak .NET için de sürümleri mevcuttur.

### 2. Aspose.Note for Java yeni başlayanlar için uygun mu?
Evet, Aspose.Note for Java kapsamlı dokümantasyon ve destek sunar; hem yeni başlayanlar hem de deneyimli geliştiriciler için erişilebilirdir.

### 3. Aspose.Note for Java için geçici bir lisans nasıl alabilirim?
Geçici lisansı **[buradan](https://purchase.aspose.com/temporary-license/)** edinebilirsiniz.

### 4. Ek destek nereden bulunur?
Herhangi bir sorunuz veya yardıma ihtiyacınız olduğunda **[Aspose.Note forumunu](https://forum.aspose.com/c/note/28)** ziyaret edin.

### 5. Ücretsiz deneme mevcut mu?
Evet, ücretsiz denemeyi **[buradan](https://releases.aspose.com/)** keşfedebilirsiniz.

**Ek Soru‑Cevap**

**S: Etiket simgesini özelleştirebilir miyim?**  
C: Evet – Aspose.Note, `TagIcon` aracılığıyla birçok ön tanımlı simge sunar ve ayrıca özel görselleri de destekler.

**S: PDF çıktı ayarlarını nasıl değiştiririm?**  
C: `PdfSaveOptions` kullanarak görüntü kalitesi, sıkıştırma ve güvenlik gibi ayarları kontrol edip `doc.save` çağrısından önce yapılandırabilirsiniz.

**S: Aynı metne birden fazla etiket eklemek mümkün mü?**  
C: Kesinlikle. Farklı `NoteTag` örnekleriyle `text.getTags().add()` metodunu birden çok kez çağırabilirsiniz.

---

**Son Güncelleme:** 2026-01-28  
**Test Edilen Versiyon:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}