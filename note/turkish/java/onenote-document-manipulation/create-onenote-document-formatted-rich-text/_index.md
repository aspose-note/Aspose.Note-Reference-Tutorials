---
date: 2025-12-09
description: Aspose.Note for Java kullanarak Java’da biçimlendirilmiş zengin metinle
  OneNote’u PDF olarak kaydetmeyi öğrenin. Sorunsuz belge otomasyonu için adım adım
  rehberimizi izleyin.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: OneNote'u Java'da Biçimlendirilmiş Zengin Metin ile PDF Olarak Kaydet
url: /tr/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u Java'da Biçimlendirilmiş Zengin Metin ile PDF Olarak Kaydet

## Giriş

OneNote'u **PDF olarak kaydetmek** ve zengin metin biçimlendirmesini korumak istiyorsanız doğru yerdesiniz. Bu öğreticide bir OneNote belgesi oluşturmayı, özel stiller uygulamayı ve Aspose.Note for Java kullanarak doğrudan PDF olarak dışa aktarmayı adım adım göstereceğiz. Sonunda, herhangi bir Java projesine ekleyebileceğiniz ve şık OneNote‑to‑PDF dönüşümlerini otomatikleştiren yeniden kullanılabilir bir kod parçacığına sahip olacaksınız.

## Quick Answers
- **Bu öğretici ne öğretir?** Stil verilen metinle bir OneNote belgesi oluşturmayı ve PDF olarak kaydetmeyi.  
- **Hangi kütüphane gereklidir?** Aspose.Note for Java (resmi siteden indirilebilir).  
- **Lisans gerekli mi?** Test için geçici bir lisans yeterli; üretim için tam lisans gerekir.  
- **Hangi IDE'yi kullanabilirim?** Herhangi bir Java IDE—IntelliJ IDEA, Eclipse veya NetBeans.  
- **Çıktı formatını değiştirebilir miyim?** Evet, Aspose.Note PDF, HTML, PNG ve daha fazlasını destekler.

## “save onenote as pdf” nedir?
OneNote'u PDF olarak kaydetmek, OneNote sayfa yapısını—metin, resimler ve biçimlendirme dahil—her platformda OneNote gerektirmeden görüntülenebilen statik bir PDF dosyasına dönüştürmek anlamına gelir.

## Neden Java’da zengin metin biçimlendirmesi?
Java'da doğrudan zengin metin biçimlendirmesi (yazı tipleri, renkler, stiller) uygulamak, belgelerin profesyonel görünmesini ve marka yönergelerinize uymasını manuel düzenleme yapmadan sağlar.

## Gereksinimler

1. **Java Development Kit (JDK)** – herhangi bir yeni sürüm (8 veya üzeri).  
2. **Aspose.Note for Java JAR** – [download link](https://releases.aspose.com/note/java/) adresinden indirin.  
3. **IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.  

## Paketleri İçe Aktarma

İlk olarak, Java projenize gerekli paketleri içe aktarmanız gerekir. Aşağıdaki import ifadelerini Java dosyanızın başına ekleyin:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Adım 1: Belge ve Sayfayı Oluşturma

`Document` ve `Page` nesnelerini başlatarak başlayalım:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Adım 2: Biçimlendirilmiş Başlık Oluşturma

Şimdi, biçimlendirilmiş metinle bir başlık oluşturalım:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## Adım 3: Biçimlendirilmiş Zengin Metin Oluşturma

Sonra, çeşitli biçimlendirme stilleriyle zengin metin oluşturalım:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## Adım 4: Öğfaya ve Belgeye Ekleme

Şimdi, başlığı ve zengin metni sayfaya ve anahat öğelerine ekleyelim:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Adım 5: Belgeyi Kaydetme

Son olarak, oluşturulan OneNote belgesini PDF olarak kaydedin:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Yaygın Sorunlar ve Çözümleri

| Issue | Solution |
|-------|----------|
| **Dosya bulunamadı** | `dataDir`'in mevcut bir klasöre işaret ettiğini ve yazma izinlerinizin olduğunu doğrulayın. |
| **Eksik yazı tipleri** | Referans verdiğiniz yazı tiplerinin (ör. *Calibri*) ana bilgisayarda yüklü olduğundan emin olun. |
| **Lisans uygulanmadı** | `Document` oluşturulmadan önce Aspose lisansınızı yükleyin; böylece değerlendirme filigranlarından kaçınırsınız. |

## Sıkça Sorulan Sorular

**S: Yazı tipi stillerini daha da özelleştirebilir miyim?**  
C: Evet, `TextStyle` ve `ParagraphStyle` sınıfları aracılığıyla alt çizgi, üstü çizili ve metin hizalaması gibi ek özellikleri ayarlayabilirsiniz.

**S: Aspose.Note for Java tüm Java IDE'leriyle uyumlu mu?**  
C: Kesinlikle. IDE standart Java geliştirmeyi desteklediği sürece, Aspose.Note JAR'ını projenin sınıf yoluna ekleyebilirsiniz.

**S: Bu işlevi web uygulamalarına entegre edebilir miyim?**  
C: Evet, aynı kod servlet tabanlı veya Spring Boot uygulamalarında çalışır ve sunucu tarafında dinamik OneNote‑to‑PDF oluşturmayı sağlar.

**S: Aspose.Note for Java kullanımı için lisans gereksinimleri var mı?**  
C: Üretim kullanımı için ticari bir lisans gerekir. Değerlendirme ve test için geçici bir lisans mevcuttur.

**S: Aspose.Note for Java OneNote dışındaki diğer belge formatlarını destekliyor mu?**  
C: PDF, HTML, PNG, JPEG ve çeşitli diğer dışa aktarma formatlarını destekler; böylece OneNote sayfalarını ihtiyacınız olan formata dönüştürme esnekliğine sahipsiniz.

## Sonuç

Bu rehberde, Aspose.Note for Java kullanarak zengin metin biçimlendirmesi uygularken **OneNote'u PDF olarak kaydet** gösterdik. Adım adım talimatları izleyerek şık OneNote belgeleri oluşturmayı ve bunları herhangi bir Java tabanlı çözümde PDF'ye dönüştürmeyi otomatikleştirebilirsiniz.

---

**Son Güncelleme:** 2025-12-09  
**Test Edilen Versiyon:** Aspose.Note for Java 24.11 (yazım zamanındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}