---
date: 2026-09-24
description: Aspose.Note for Java ile OneNote belgesine tag eklemeyi öğrenin – bir
  OneNote dosyası oluşturun, bir styled text node ve tag ekleyin ve sadece birkaç
  satır kodla kaydedin.
keywords:
- how to add tag
- Aspose.Note Java
- OneNote tag operations
- add text node
lastmod: 2026-09-24
linktitle: OneNote'da Tag ile Text Node Ekle - Aspose.Note
og_description: Aspose.Note for Java ile OneNote belgesine tag eklemeyi öğrenin –
  bir OneNote dosyası oluşturun, bir styled text node ve tag ekleyin ve sadece birkaç
  satır kodla kaydedin.
og_image_alt: Guide showing how to add a tag to a OneNote document using Aspose.Note
  for Java
og_title: Aspose.Note (Java) ile OneNote belgesine tag ekleme
schemas:
- author: Aspose
  dateModified: '2026-09-24'
  description: Learn how to add tag to a OneNote document with Aspose.Note for Java
    – create a OneNote file, add a styled text node with a tag, and save it in just
    a few lines of code.
  headline: How to add tag to a OneNote document by adding a text node using Aspose.Note
  type: TechArticle
- questions:
  - answer: It provides a Java API to read, modify, and create OneNote files without
      needing Microsoft Office installed.
    question: What does Aspose.Note do?
  - answer: Roughly 15 lines, including object creation and styling.
    question: How many lines of code to add a tagged text node?
  - answer: A free trial works for development; a license is required for production
      use.
    question: Do I need a license to run the sample?
  - answer: Yes – Aspose.Note offers over 30 built‑in icons such as yellow star, checkmark,
      and heart.
    question: Can I change the tag icon?
  - answer: The library saves the result as a standard *.one* OneNote file.
    question: What format is the output file?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- OneNote
- Aspose.Note
- Java
- tag operations
- document creation
title: Aspose.Note kullanarak bir text node ekleyerek OneNote belgesine tag ekleme
url: /tr/java/onenote-tag-operations/add-text-node-with-tag/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note kullanarak bir metin düğümü ekleyerek OneNote belgesine etiket ekleme

## Giriş
Bu öğreticide, Aspose.Note Java API'sını kullanarak bir OneNote belgesine **etiket ekleme** yöntemini öğreneceksiniz. Yeni bir OneNote dosyası oluşturma, bir paragrafı biçimlendirme, metne yerleşik bir etiket ekleme ve son olarak tek bir `save` çağrısıyla defteri kalıcı hâle getirme adımlarını göstereceğiz. Kişisel not alma aracını mı geliştiriyorsunuz yoksa kurumsal raporlamayı mı otomatikleştiriyorsunuz, aşağıdaki adımlar OneNote içeriği üzerinde tam programatik kontrol sağlar.

## Hızlı cevaplar
- **Aspose.Note ne yapar?** Microsoft Office yüklü olmadan OneNote dosyalarını okuma, değiştirme ve oluşturma için bir Java API'si sağlar.  
- **Etiketli bir metin düğümü eklemek için kaç satır kod gerekir?** Nesne oluşturma ve stil eklemeyi içeren yaklaşık 15 satır.  
- **Örneği çalıştırmak için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme yeterlidir; üretim kullanımı için lisans gereklidir.  
- **Etiket simgesini değiştirebilir miyim?** Evet – Aspose.Note, sarı yıldız, onay işareti ve kalp gibi 30'dan fazla yerleşik simge sunar.  
- **Çıktı dosyasının formatı nedir?** Kütüphane sonucu standart bir *.one* OneNote dosyası olarak kaydeder.

## “OneNote belgesi oluşturma” ne anlama geliyor?
OneNote belgesi oluşturmak, Microsoft OneNote'ta açılabilen bir *.one* dosyasını programlı olarak üretmek anlamına gelir. Dosya, Aspose.Note API'si aracılığıyla oluşturulan sayfalar, outline'lar ve zengin‑metin öğeleri içerir; böylece masaüstü uygulamasına ihtiyaç duymadan defterler inşa edebilirsiniz.

## Neden bir metin düğümüne etiket ekleyelim?
Bir metin düğümüne etiket eklemek, önemli bilgileri vurgular ve OneNote'un yerleşik etiket gezinmesini etkinleştirir; bu da inceleme ve görev yönetimini hızlandırır. Etiketler meta veri olarak saklanır, cihazlar arasında kalıcıdır ve görsel simgelerini korur. Bu sayede kullanıcılar büyük defterlerde etiketli öğeleri etkili bir şekilde filtreleyebilir veya arayabilir.

## Önkoşullar
- Java programlama temelleri.  
- Aspose.Note for Java kütüphanesi yüklü. Aspose.Note for Java kütüphanesini [download Aspose.Note for Java](https://releases.aspose.com/note/java/) adresinden indirebilirsiniz.  
- Java geliştirme için bir Entegre Geliştirme Ortamı (IDE) kurulu.

## Paketleri içe aktar
Java projeniz için gerekli paketleri içe aktararak başlayın. Kodunuzda aşağıdaki importları ekleyin:
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

## Adım 1: belge nesnesi oluştur
`Document` bellek içinde bir OneNote dosyasını temsil eden üst‑seviye sınıftır. Oluşturulduktan sonra tüm sonraki işlemler bu nesne üzerinden yürütülür.
```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
```

## Adım 2: sayfa sınıfı nesnesini başlat
`Page`, OneNote defterindeki tek bir sayfayı temsil eder. Her sayfa birden fazla outline ve diğer öğeleri içerebilir.
```java
// Initialize Page class object
Page page = new Page();
```

## Adım 3: outline sınıfı nesnesini başlat
`Outline`, sayfadaki ilgili öğeleri gruplar ve bir veya daha fazla `OutlineElement` nesnesi için kapsayıcı görevi görür.
```java
// Initialize Outline class object
Outline outline = new Outline();
```

## Adım 4: outlineelement sınıfı nesnesini başlat
`OutlineElement`, bir outline içinde metin, resim veya diğer zengin içerikleri tutabilen en küçük görsel birimdir.
```java
// Initialize OutlineElement class object
OutlineElement outlineElem = new OutlineElement();
```

## Adım 5: metin stilini özelleştir
Metin düğümü için stil ayarlayın—bu adımda **paragraf stilini** font rengi, adı ve boyutu gibi özelliklerle belirleyebilirsiniz. Aspose.Note, tek bir `RichTextStyle` nesnesinde RGB renkleri, font aileleri ve punto boyutlarını belirtmenize olanak tanır.
```java
// Customize text style
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```

## Adım 6: richtext nesnesi oluştur
`RichText`, gerçek dize içeriğini tutan sınıftır. Nesneyi oluşturduktan sonra, daha sonra etikete sahip olacak istenen metni ekleyebilirsiniz.
```java
// Create RichText object
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```

## Adım 7: not etiketi ekle
`Tag`, herhangi bir `RichText`'e eklenebilen görsel bir işaretçidir (ör. sarı yıldız). Aspose.Note, 30'dan fazla yerleşik etiket simgesi sunar; ayrıca ihtiyaç duyulursa özel simgeler de tanımlanabilir.
```java
// Add note tag
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```

## Adım 8: metin düğümü ekle
`RichText`'i (etiketiyle birlikte) `OutlineElement`'e ekleyin. Bu adım, biçimlendirilmiş ve etiketli metni outline hiyerarşisine bağlar.
```java
// Add text node
outlineElem.appendChildLast(text);
```

## Adım 9: outline elementini outline'a ekle
`OutlineElement`'i `Outline` kapsayıcısının içine yerleştirerek sayfanın görsel yapısının bir parçası hâline getirin.
```java
// Add outline element node
outline.appendChildLast(outlineElem);
```

## Adım 10: outline'ı sayfaya ekle
`Outline`'ı `Page` yapısına ekleyerek sayfanın içerik ağacını tamamlayın.
```java
// Add outline node
page.appendChildLast(outline);
```

## Adım 11: sayfayı belgeye ekle
Tamamen oluşturulmuş `Page`'i `Document` nesnesine ekleyerek defteri kalıcı hâle getirmeye hazırlayın.
```java
// Add page node
doc.appendChildLast(page);
```

## Adım 12: OneNote belgesini kaydet
Son olarak **OneNote dosyasını** diske kaydedin. Bu, **OneNote belgesi oluşturma** iş akışını tamamlar ve herhangi bir yeni Microsoft OneNote sürümünde açılabilen standart bir *.one* dosyası üretir.
```java
// Save OneNote document
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```

## Bunun önemi
Aspose.Note **50+ giriş ve çıkış formatını** (DOCX, PDF, HTML ve görüntü türleri dahil) destekler ve tüm dosyayı belleğe yüklemeden çok sayfalı defterleri işleyebilir; bu da sunucu‑tarafı otomasyon ve büyük ölçekli not üretimi için uygundur.

## Yaygın sorunlar ve çözümler
- **Etiket kaydedildikten sonra görünmüyor** – `RichText`'i `OutlineElement`'e eklemeden önce `richText.getTags().add(tag)` çağrısını yaptığınızdan emin olun.  
- **Font stili göz ardı ediliyor** – `RichText` örneğine `RichTextStyle`'ı outline'a eklemeden önce uyguladığınızı doğrulayın.  
- **Büyük defterler OutOfMemoryError veriyor** – 500 MB'den büyük dosyalar için akış modunu etkinleştirmek üzere `Document.setLoadOptions(new LoadOptions(LoadFormat.ONE))` kullanın.

## Sıkça sorulan sorular
### Q: Aspose.Note for Java'yı diğer Java kütüphaneleriyle kullanabilir miyim?
A: Evet, Aspose.Note for Java Apache POI, Jackson veya Spring gibi kütüphanelerle sorunsuz bir şekilde entegre olur; böylece not oluşturmayı veri işleme hatlarıyla birleştirebilirsiniz.

### Q: Aspose.Note for Java için ücretsiz bir deneme mevcut mu?
A: Evet, ücretsiz deneme sayfasına şu adresten ulaşabilirsiniz: [download Aspose.Note free trial page](https://releases.aspose.com/).

### Q: Aspose.Note for Java için destek nasıl alınır?
A: Aspose.Note topluluğu forumundan destek alabilirsiniz: [Aspose.Note forum](https://forum.aspose.com/c/note/28).

### Q: Aspose.Note for Java için geçici lisanslar mevcut mu?
A: Evet, geçici lisansları şu sayfadan satın alabilirsiniz: [temporary license purchase page](https://purchase.aspose.com/temporary-license/).

### Q: Aspose.Note for Java dokümantasyonunu nerede bulabilirim?
A: Dokümantasyon şu adreste mevcuttur: [Aspose.Note Java API documentation](https://reference.aspose.com/note/java/).

---

**Son Güncelleme:** 2026-09-24  
**Test Edilen Versiyon:** Aspose.Note for Java 24.11  
**Yazar:** Aspose

## İlgili Eğitimler

- [Add Tags to OneNote – Create Tagged OneNote Document with Aspose.Note](/note/java/onenote-tag-operations/)
- [Generate Meeting Notes Template with Aspose.Note for Java – Create Outline in OneNote](/note/java/onenote-tag-operations/generate-template-for-meeting-notes/)
- [Create OneNote Document Java – Aspose Note Java Tutorial](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}