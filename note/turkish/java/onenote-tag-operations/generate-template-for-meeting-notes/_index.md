---
date: 2026-03-03
description: OneNote'ta taslak oluşturmayı ve Aspose.Note for Java ile toplantı notları
  şablonu üretmeyi öğrenin. Yazı tipi stilini özelleştirin ve onay kutularını kolayca
  ekleyin.
linktitle: Create Outline in OneNote – Meeting Notes Template
second_title: Aspose.Note Java API
title: OneNote'ta Ana Hat Oluştur – Toplantı Notları Şablonu
url: /tr/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Taslak Oluştur – Toplantı Notları Şablonu

## Giriş
Bugünün hızlı tempolu dünyasında, **OneNote'ta taslak oluşturmak**, net toplantı belgeleri için çok önemlidir. Aspose.Note for Java, **toplantı notları şablonu** oluşturmak için güçlü bir yol sunar; şablonu özelleştirebilir, onay kutuları ekleyebilir ve yazı tiplerini ihtiyacınıza göre biçimlendirebilirsiniz. Bu adım‑adım kılavuzda, yeniden kullanılabilir bir toplantı gündemi şablonu oluşturmayı, **onay kutularını ekleme**, **OneNote'a kontrol listesi ekleme** ve **customize font style onenote** ile şık bir görünüm elde etmeyi anlatacağız.

## Hızlı Yanıtlar
- **“OneNote'ta taslak oluşturmak” ne anlama geliyor?** Bir OneNote dosyası içinde hiyerarşik bir yapı (başlıklar, bölümler, madde işaretleri) programlı olarak oluşturmak demektir.  
- **Hangi kütüphane bunu sağlıyor?** Aspose.Note for Java.  
- **Taslağa onay kutuları ekleyebilir miyim?** Evet – `NoteCheckBox.createBlueCheckBox()` kullanın.  
- **Lisans gerekli mi?** Ücretsiz deneme sürümü mevcuttur; üretim için ticari lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri.

## “OneNote'ta taslak oluşturmak” nedir?
OneNote'ta bir taslak oluşturmak, bir sayfada başlık, birden fazla taslak bölümü ve isteğe bağlı liste numaralandırması ya da onay kutuları tanımlamak anlamına gelir. Bu yapı, OneNote arayüzünde manuel olarak başlıklar ve madde işaretleri yazma şeklinizi taklit eder, ancak kodla otomatik olarak üretilir.

## Toplantı gündemi şablonları için Aspose.Note neden kullanılmalı?
- **Tutarlılık:** Her toplantı aynı temiz düzenle başlar.  
- **Otomasyon:** Manuel yazımı azaltır ve tüm gerekli bölümlerin (gündem, eylem maddeleri, notlar) mevcut olmasını sağlar.  
- **Özelleştirme:** Yazı tiplerini, renkleri değiştirin ve görev takibi için etkileşimli onay kutuları ekleyin.  
- **Entegrasyon:** Herhangi bir Java IDE'siyle çalışır ve PDF, elektronik tablo gibi diğer Aspose kütüphaneleriyle birleştirilebilir.

## Önkoşullar
- Java programlamaya temel bir anlayış.  
- Aspose.Note for Java kütüphanesi yüklü. İndirilebilir [buradan](https://releases.aspose.com/note/java/).  
- Eclipse veya IntelliJ IDEA gibi bir IDE.

## Paketleri İçe Aktarma
İlk olarak, ihtiyacımız olan sınıfları içe aktaralım. Bu kod parçacığı orijinal öğreticidekiyle tamamen aynı kalır.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## Adım 1: Belge Yapısını Oluşturma
Belgeyi oluşturuyor, bir başlık ayarlıyor ve daha sonra **customize font style onenote** için yardımcı olacak paragraf stillerini hazırlıyoruz.

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
- İki `ParagraphStyle` nesnesi tanımladık (`headerStyle` başlıklar için, `bodyStyle` normal metin için).  
- Bir `Document` oluşturduk ve mevcut tarihi içeren bir `Title` ekleyerek sayfaya net bir başlık verdik.

## Adım 2: Önemli Noktaları Taslak Haline Getirme
Sonra, bir `Outline` nesnesi ekleyerek ve “Important” gibi bölümlerle doldurarak **OneNote'ta taslak oluşturuyoruz**. Bu, gündem maddelerinin bulunduğu yerdir.

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
- `Outline` nesnesi, OneNote'ta gördüğünüz hiyerarşik listeyi temsil eder.  
- `createListNumberingStyle` kullanarak, her yeni bölüm için yeniden başlatılabilen numaralı bir liste oluşturuyoruz.

## Adım 3: Eylem Maddelerini Vurgulama (Onay kutuları nasıl eklenir)
Eylem maddeleri görsel bir işaret gerektirir. Her `RichText` öğesine bir onay kutusu etiketi ekleyerek **onay kutularını ekleme** doğrudan taslak içinde mümkün kılıyor.

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

*İpucu:* Mavi bir onay kutusu için `NoteCheckBox.createBlueCheckBox()` kullanın; farklı bir görsel stil isterseniz diğer renkler de mevcuttur.

## Adım 4: Belgeyi Kaydetme
Son olarak, OneNote dosyasını diske yazıyoruz. Dosya, OneNote masaüstü uygulamasında doğrudan açılabilir.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## Yaygın Sorunlar ve Çözümler
| Sorun | Çözüm |
|-------|----------|
| **Onay kutuları görünmüyor** | `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` çağrısını paragraf stilini ayarladıktan sonra yaptığınızdan emin olun. |
| **Yazı tipleri OneNote'ta farklı görünüyor** | Yazı tipi adının (ör. “Calibri”) OneNote dosyasının açıldığı makinede yüklü olduğundan emin olun. |
| **Taslak girintili değil** | `Outline` nesnesindeki `setVerticalOffset` ve `setHorizontalOffset` değerlerini ayarlayın. |
| **Numaralandırma beklenmedik şekilde yeniden başlıyor** | `restartFlag` özelliğini doğru kullanın; yeni bir bölümdeki ilk liste için sadece `true` olarak ayarlayın. |

## Sık Sorulan Sorular
### Toplantı notlarımda yazı tiplerini özelleştirebilir miyim?
Evet, Aspose.Note başlıklar ve gövde metni için özel yazı tipi stilleri tanımlamanıza izin verir.

### Aspose.Note diğer Java kütüphaneleriyle uyumlu mu?
Aspose.Note, genişletilmiş işlevsellik için diğer Java kütüphaneleriyle sorunsuz bir şekilde bütünleştirilebilir.

### Toplantı notlarıma ek bölümler ekleyebilir miyim?
Evet, öğreticide gösterilen aynı desenle taslak yapısını kolayca genişletebilirsiniz.

### Aspose.Note için lisans konularında nelere dikkat etmeliyim?
Lisans detayları için [Aspose.Note belgelerine](https://reference.aspose.com/note/java/) bakın.

### Aspose.Note için bir deneme sürümü var mı?
Evet, [ücretsiz deneme sürümüne buradan](https://releases.aspose.com/) ulaşabilirsiniz.

## SSS
**S: OneNote'a onay kutusu kullanmadan bir kontrol listesi nasıl eklerim?**  
C: Noktalı bir liste oluşturup öğeleri manuel olarak işaretleyebilirsiniz, ancak `NoteCheckBox` kullanmak, OneNote arayüzüyle senkronize çalışan etkileşimli onay kutuları sağlar.

**S: Bu şablonu haftalık tekrar eden toplantı gündemi şablonu olarak kullanabilir miyim?**  
C: Kesinlikle. Tarih formatını değiştirerek veya özel bir başlık dizesi geçirerek aynı yapıyı her hafta yeniden kullanabilirsiniz.

**S: **customize font style onenote** markalaşma için en iyi yol nedir?**  
C: Kurumsal yazı tipi adınızı, boyutunu ve renginizi içeren `ParagraphStyle` nesneleri tanımlayın ve bunları Step 1'de gösterildiği gibi her `RichText` öğesine uygulayın.

**S: Aspose.Note taslağı PDF'ye dışa aktarmayı destekliyor mu?**  
C: Evet. OneNote dosyasını kaydettikten sonra Aspose.Note ile yükleyebilir ve `Document.save("output.pdf", SaveFormat.Pdf)` kullanarak PDF olarak dışa aktarabilirsiniz.

**S: Programlı olarak bir onay kutusunu tamamlanmış olarak işaretleyebilir miyim?**  
C: `Checked` özelliği `true` olarak ayarlanmış bir `NoteCheckBox` etiketi ekleyerek onay kutusunun durumunu belirleyebilirsiniz.

---

**Son Güncelleme:** 2026-03-03  
**Test Edilen Versiyon:** Aspose.Note for Java 24.11 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}