---
date: 2026-10-26
description: Aspose.Note for Java ile bir meeting notes template oluştururken OneNote'e
  checkboxes eklemeyi öğrenin ve OneNote font style'ını kolayca özelleştirin.
keywords:
- add checkboxes onenote
- generate meeting notes template
- customize font style onenote
- create outline onenote
lastmod: 2026-10-26
linktitle: Aspose.Note for Java ile Meeting Notes Template Oluşturun – OneNote'ta
  Outline Oluşturun
og_description: Aspose.Note for Java ile bir meeting notes template oluştururken OneNote'e
  checkboxes eklemeyi öğrenin ve OneNote font style'ını kolayca özelleştirin.
og_image_alt: 'Developer guide: add checkboxes onenote and generate meeting notes
  template using Aspose.Note for Java'
og_title: Java'da OneNote'e checkboxes ekleyin ve notes template oluşturun
schemas:
- author: Aspose
  dateModified: '2026-10-26'
  description: Learn how to add checkboxes onenote while generating a meeting notes
    template with Aspose.Note for Java, and customize font style onenote easily.
  headline: Add checkboxes onenote and create notes template in Java
  type: TechArticle
- questions:
  - answer: You can create a bulleted list and manually mark items, but using `NoteCheckBox`
      provides interactive checkboxes that sync with OneNote’s UI.
    question: How do I add a checklist to OneNote without using checkboxes?
  - answer: Absolutely. Just change the date formatting or pass a custom title string
      to reuse the same structure for each week.
    question: Can I use this template to create a meeting agenda template for weekly
      repeats?
  - answer: Define `ParagraphStyle` objects with your corporate font name, size, and
      color, then apply them to each `RichText` element as shown in Step 1.
    question: What is the best way to customize font style onenote for branding?
  - answer: Yes. After saving the OneNote file, you can load it with Aspose.Note and
      export to PDF using `Document.save("output.pdf", SaveFormat.Pdf)`.
    question: Does Aspose.Note support exporting the outline to PDF?
  - answer: You can set the checkbox state by adding a `NoteCheckBox` tag with the
      `Checked` property set to `true`.
    question: Is there a way to programmatically mark a checkbox as completed?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote
- Aspose.Note
- Java
- meeting notes template
- checkboxes
title: Java'da OneNote'e checkboxes ekleyin ve notes template oluşturun
url: /tr/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta onay kutuları ekleyin ve Java'da not şablonu oluşturun

## Giriş
Modern işbirliği ortamlarında, **add checkboxes onenote** hızlı bir şekilde ekleyebilir ve manuel biçimlendirme yapmadan şık bir toplantı notları şablonu oluşturabilirsiniz. Aspose.Note for Java, sayfa başlıkları, hiyerarşik ana hatlar, yazı tipi stilleri ve etkileşimli onay kutuları üzerinde tam kontrol sağlar; böylece tekrar kullanılabilir bir gündemi saniyeler içinde üretebilirsiniz. Bu kılavuz, gerekli sınıfların içe aktarımından son OneNote dosyasının kaydedilmesine kadar her adımı size gösterir; böylece sıkıcı UI işine değil, toplantı içeriğine odaklanabilirsiniz.

## Hızlı cevaplar
- **“add checkboxes onenote” ne anlama geliyor?** Bir OneNote ana hattına, UI'nin yaptığı gibi, programatik olarak etkileşimli onay kutuları eklemek anlamına gelir.  
- **Bu konuda hangi kütüphane yardımcı olur?** Aspose.Note for Java tam API'yi sağlar.  
- **Ana hatta onay kutuları ekleyebilir miyim?** Evet – `NoteCheckBox.createBlueCheckBox()` veya diğer renk varyantlarını kullanın.  
- **Lisans gerekir mi?** Geliştirme için ücretsiz deneme çalışır; üretim kullanımı için ticari lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri.

## add checkboxes onenote nedir?
add checkboxes onenote, bir `RichText` öğesine `NoteCheckBox` etiketi ekleyerek, normal bir metin satırını OneNote UI içinde doğrudan işaretlenebilen etkileşimli bir kutuya dönüştürür; bu, cihazlar arasında onay kutusu durumunun korunmasını ve tutarlılığın sağlanmasını sağlar.

## Toplantı notları şablonu oluşturmak için Aspose.Note neden kullanılmalı?
Aspose.Note **50+ giriş ve çıkış formatı** işleyebilir ve **500 satıra kadar** sayfaları belgenin tamamını belleğe yüklemeden işleyebilir; bu sayede büyük gündemlerin hızlı ve bellek‑verimli üretilmesi sağlanır. Ayrıca stil verme için akıcı bir API sunar, Unicode karakterleri destekler ve diğer Aspose kütüphaneleriyle sorunsuz entegrasyon sağlar; bu da kurumsal ölçekli toplantı dokümantasyon iş akışları için idealdir.

## Önkoşullar
- Java programlamaya temel bir anlayış.  
- Aspose.Note for Java kütüphanesi yüklü. Resmi Aspose.Note for Java sürüm sayfasından **Aspose.Note for Java'yi indirebilirsiniz**: [Aspose.Note for Java sürüm sayfası](https://releases.aspose.com/note/java/).  
- Eclipse veya IntelliJ IDEA gibi bir IDE.  

## Paketleri içe aktar
`Document`, `Outline`, `ParagraphStyle`, `RichText` ve `NoteCheckBox` sınıfları temel yapı taşlarıdır.  

`Document`, bellekte tüm OneNote dosyasını temsil eder; sayfalar ve içerik eklenip değiştirilebilir.  
`Outline`, OneNote'ta görülen hiyerarşik liste yapısını modeller; iç içe madde işaretleri ve numaralandırma sağlar.  
`ParagraphStyle`, birden fazla `RichText` öğesine uygulanabilen yeniden kullanılabilir yazı tipi ve paragraf özelliklerini tanımlar.  
`RichText`, bir paragrafın gerçek metin içeriğini tutar ve `NoteCheckBox` gibi etiketler içerebilir.  
`NoteCheckBox`, bir `RichText` paragrafına eklenebilen etkileşimli onay kutusu etiketini oluşturur.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Adım 1: belge yapısını oluşturun
İlk olarak bir `Document` örneği oluşturun, sayfa başlığı ayarlayın ve iki yeniden kullanılabilir `ParagraphStyle` nesnesi tanımlayın—biri başlıklar için, diğeri gövde metni için.  

`ParagraphStyle` nesneleri, aynı yazı tipi ailesi, boyutu ve rengini birden fazla paragraf için kod tekrarı yapmadan uygulamanızı sağlar.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*Yaptıklarımız:*  
- Başlıklar için `headerStyle` ve normal metin için `bodyStyle` tanımlandı.  
- Bir `Document` oluşturuldu ve bugünün tarihini içeren bir `Title` eklendi; bu sayfaya net bir başlık verir.

## Adım 2: önemli noktaları ana hatlarıyla belirtin
Sonra sayfaya bir `Outline` nesnesi ekleyin ve “Agenda”, “Discussion Items” ve “Action Items” gibi bölümlerle doldurun.  

`Outline` nesnesi OneNote'ta gördüğünüz hiyerarşik listeyi temsil eder. `createListNumberingStyle` kullanarak her yeni bölüm için yeniden başlatılabilen numaralı bir liste oluştururuz.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*Neden önemli:*  
- Ana hat hiyerarşisi, OneNote'ta manuel olarak yazacağınız yapıyı yansıtarak tüm oluşturulan sayfalarda tutarlılık sağlar.  
- Numara stilleri, her gündem bölümünü düzenli ve takip etmesi kolay tutar.

## Adım 3: eylem öğelerini vurgulayın (onay kutuları nasıl eklenir)
Eylem öğeleri görsel bir işaret gerektirir. Her `RichText` öğesine bir `NoteCheckBox` etiketi ekleyerek **add checkboxes onenote** işlevini doğrudan ana hat içinde etkinleştirirsiniz.  

`NoteCheckBox.createBlueCheckBox()` mavi bir işaretli kutu oluşturur; marka renkleri için diğer renkler de mevcuttur.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*Pro tip:* `NoteCheckBox.createBlueCheckBox()` mavi bir işaret kutusu oluşturur; farklı bir görsel stil isterseniz diğer renkleri de kullanabilirsiniz.

## Adım 4: OneNote'ta yazı tipi stilini özelleştirin
Toplantı notlarınızın marka uyumlu kalması için, önceden tanımlı `ParagraphStyle` nesnelerini her `RichText` öğesine uygulayın.  

`FontName`, `FontSize` ve `FontColor` özelliklerini ayarlamak, oluşturulan sayfanın kurumsal stil rehberinizle eşleşmesini sağlar.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Adım 5: belgeyi kaydedin
Son olarak OneNote dosyasını diske yazın. Dosya doğrudan OneNote masaüstü uygulamasında açılabilir ve gerektiğinde PDF'ye dönüştürülebilir.

*Doğrudan yanıt:* `document.save("MeetingTemplate.one")` çağrısını yapın—API, OneNote istemcisinde anında açılan tam uyumlu bir OneNote dosyası yazar.

## Yaygın sorunlar ve çözümler
| Sorun | Çözüm |
|-------|----------|
| **Checkboxes not appearing** | Paragraf stilini ayarladıktan sonra `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` çağrısını yaptığınızdan emin olun. |
| **Fonts look different in OneNote** | Yazı tipi adının (ör. “Calibri”) OneNote dosyasını açan makinede yüklü olduğunu doğrulayın. |
| **Outline not indented** | `Outline` nesnesinde `setVerticalOffset` ve `setHorizontalOffset` değerlerini ayarlayın. |
| **Numbering restarts unexpectedly** | `restartFlag` özelliğini doğru kullanın; yeni bir bölümdeki ilk liste için yalnızca `true` olarak ayarlayın. |

## Sıkça Sorulan Sorular
### OneNote'ta nasıl onay kutuları eklenir?
Bir `RichText` öğesi yükleyin, ardından `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` çağrısını yapın. Etiket, satırı OneNote içinde kullanıcıların işaretleyebileceği etkileşimli bir onay kutusuna dönüştürür.

### Toplantı notlarımda yazı tipi stillerini özelleştirebilir miyim?
Evet. İstediğiniz `FontName`, `FontSize` ve `FontColor` değerleriyle `ParagraphStyle` nesneleri oluşturun ve bunları her `RichText` öğesine Step 1'de gösterildiği gibi atayın.

### Aspose.Note diğer Java kütüphaneleriyle uyumlu mu?
Aspose.Note, diğer Aspose ürünleri (PDF, Cells, Slides) ve standart Java kütüphaneleriyle sorunsuz çalışır; böylece oluşturulan OneNote dosyasını PDF'ye dönüştürmek gibi zincirleme işlemler yapabilirsiniz.

### Toplantı notlarıma ek bölümler nasıl eklenir?
Aynı deseni tekrar edin: yeni bir `Outline` düğümü oluşturun, bir `ParagraphStyle` uygulayın ve isteğe bağlı olarak onay kutuları ekleyin. API, istenilen sayıda bölüm için tamamen tekrarlanabilir.

### Aspose.Note için lisanslama hususları var mı?
Tam lisans detayları için [Aspose.Note dokümantasyonuna](https://reference.aspose.com/note/java/) bakın. Geliştirme için ücretsiz deneme yeterlidir; üretim dağıtımları için ticari lisans gereklidir.

### Aspose.Note için deneme sürümü mevcut mu?
Evet, **ücretsiz Aspose.Note deneme indirme sayfasına** erişebilirsiniz: [Aspose.Note deneme indirme sayfası](https://releases.aspose.com/).

## SSS
**S: OneNote'a onay kutuları kullanmadan nasıl bir kontrol listesi ekleyebilirim?**  
C: Madde işaretli bir liste oluşturup öğeleri manuel olarak işaretleyebilirsiniz, ancak `NoteCheckBox` kullanmak, OneNote UI ile senkronize çalışan etkileşimli onay kutuları sağlar.

**S: Bu şablonu haftalık tekrarlar için bir toplantı gündemi şablonu olarak kullanabilir miyim?**  
C: Kesinlikle. Tarih formatını değiştirerek veya özel bir başlık dizesi geçirerek aynı yapıyı her hafta yeniden kullanabilirsiniz.

**S: Marka uyumu için OneNote'ta yazı tipi stilini nasıl özelleştiririm?**  
C: Kurumsal yazı tipi adınızı, boyutunuzu ve renginizi içeren `ParagraphStyle` nesneleri tanımlayın, ardından bunları Step 1'de gösterildiği gibi her `RichText` öğesine uygulayın.

**S: Aspose.Note ana hatları PDF'ye dışa aktarabilir mi?**  
C: Evet. OneNote dosyasını kaydettikten sonra Aspose.Note ile yükleyip `Document.save("output.pdf", SaveFormat.Pdf)` kullanarak PDF'ye dönüştürebilirsiniz.

**S: Programatik olarak bir onay kutusunu tamamlanmış olarak işaretleyebilir miyim?**  
C: `NoteCheckBox` etiketine `Checked` özelliğini `true` olarak ayarlayarak kutunun işaretli olmasını sağlayabilirsiniz.

**Son Güncelleme:** 2026-10-26  
**Test Edilen Versiyon:** Aspose.Note for Java 24.11 (yazım zamanındaki en son sürüm)  
**Yazar:** Aspose

## İlgili Eğitimler

- [OneNote'a Etiket Ekle – Aspose.Note ile Etiketli OneNote Belgesi Oluştur](/note/java/onenote-tag-operations/)
- [Aspose.Note for Java ile OneNote Stillerini Özelleştirme](/note/java/onenote-styles/)
- [Java ile OneNote Belgesi Oluştur – Aspose Note Java Eğitimi](/note/java/onenote-document-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}