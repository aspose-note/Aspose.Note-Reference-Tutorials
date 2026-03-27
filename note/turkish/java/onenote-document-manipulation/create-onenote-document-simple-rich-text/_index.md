---
date: 2026-02-18
description: Aspose.Note kullanarak Java’da OneNote belgeleri oluştururken paragraf
  stilini ayarlamayı ve anahat öğesi eklemeyi öğrenin. OneNote’u PDF’ye dışa aktarın,
  OneNote’u PDF olarak kaydedin ve OneNote dosyalarını zahmetsizce oluşturun.
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: OneNote'u PDF'ye Dışa Aktar – Java'da OneNote Belgesi Oluştururken Paragraf
  Stili Ayarla
url: /tr/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da OneNote Belgesi Oluştururken Paragraf Stilini Ayarlama

## Giriş

Bugünün hızlı gelişen yazılım ortamında, **export OneNote to PDF** işlemini programlı olarak yapabilmek, cilalı ve paylaşım‑hazır belgeler üretmek için çok önemlidir. Bu öğretici, bir OneNote dosyası oluşturmayı, özel bir paragraf stili uygulamayı ve son olarak Aspose.Note for Java kullanarak **export OneNote to PDF** işlemini adım adım gösterir. Raporlama motoru, otomatik not‑alma çözümü veya belge‑dönüştürme hizmeti geliştiriyor olun, burada ele alınan teknikler **save OneNote as PDF** işlemini tam biçimlendirme kontrolüyle yapmanıza yardımcı olacaktır.

## Hızlı Yanıtlar
- **set paragraph style** ne anlama geliyor? Bir metin paragrafına yazı tipi, boyut, renk ve diğer biçimlendirmeleri uygular.  
- **Sonucu PDF olarak dışa aktarabilir miyim?** Evet – öğretici, OneNote dosyasını PDF olarak kaydetme ile sona erer.  
- **Aspose.Note için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme sürümü çalışır; üretim için lisans gereklidir.  
- **Hangi IDE'ler destekleniyor?** Herhangi bir Java IDE – Eclipse, IntelliJ IDEA, NetBeans, vb.  
- **Uygulamanın süresi ne kadar?** Temel bir belge için yaklaşık 10‑15 dakika.

## Aspose.Note'ta “set paragraph style” nedir?

Paragraf stilini ayarlamak, bir `ParagraphStyle` nesnesini (yazı tipi adı, boyut, renk vb.) yapılandırıp bir `RichText` düğümüne eklemeyi ifade eder. Bu, OneNote sayfasındaki metnin nasıl görüneceği üzerinde tam kontrol sağlar.

## OneNote'ta Paragraf Stili Nasıl Ayarlanır?

Bir stil uygulamak, bir `ParagraphStyle` örneği oluşturmak, özelliklerini özelleştirmek ve bir `RichText` öğesine atamak kadar basittir. Stil nesnesi hazır olduğunda API, bunu tek satırlık bir işlem haline getirir.

## OneNote PDF Olarak Neden Dışa Aktarılır?

- **Consistent branding:** Dışarıyla not paylaşırken kurumsal yazı tiplerini ve renkleri koruyun.  
- **Readability:** PDF, tam düzeni korur, bu da baskı veya arşivleme için idealdir.  
- **Cross‑platform access:** Alıcılar, OneNote gerekmeksizin PDF'yi herhangi bir cihazda görüntüleyebilir.

## Önkoşullar

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK) 1.8+** – herhangi bir güncel JDK çalışır.  
2. **Aspose.Note for Java** – en son JAR'ı [Aspose.Note download page](https://releases.aspose.com/note/java/) adresinden indirin.  
3. **Bir IDE** (Eclipse, IntelliJ IDEA veya NetBeans), örneği derlemek ve çalıştırmak için.  

> **Pro tip:** Aspose.Note JAR'ı Maven aracılığıyla veya IDE'nizde JAR'ı manuel olarak referans göstererek projenizin classpath'ine ekleyin.

## Paketleri İçe Aktar

İlk olarak, ihtiyacımız olan sınıfları içe aktarın. Bu blok değişmeden kalır.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> `ParagraphStyle` sınıfı, öğreticide daha sonra **set paragraph style** yapmak için anahtardır.

## Adım‑Adım Kılavuz

Aşağıda her işlem için kısa bir yürütme bulunmaktadır. Kod blokları orijinal örnekle aynı; sadece açıklayıcı metin ekliyoruz.

### Adım 1: Belge Dizinini Ayarla
Define where the generated files will be saved.

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini makinenizdeki mutlak ya da göreli bir yol ile değiştirin.

### Adım 2: Document Nesnesini Başlat
Create the root `Document` that represents the OneNote file.

```java
Document doc = new Document();
```

### Adım 3: Page Nesnesini Başlat
A OneNote file consists of one or more pages; we start with a single page.

```java
Page page = new Page();
```

### Adım 4: Outline Nesnesini Başlat
Outlines act as containers for outline elements (think of them as sections).

```java
Outline outline = new Outline();
```

### Adım 5: OutlineElement Nesnesini Başlat
Here we **add outline element** that will hold our rich text.

```java
OutlineElement outlineElem = new OutlineElement();
```

### Adım 6: Metin Stilini Ayarla (Set Paragraph Style)
```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

The `ParagraphStyle` instance defines the font, size, and color—this is where we **set paragraph style** for the upcoming text node.

### Adım 7: RichText Nesnesini Başlat
```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

We create a `RichText` node, insert a simple string, and attach the previously defined style.

### Adım 8: RichText Düğümünü OutlineElement'e Ekle
```java
outlineElem.appendChildLast(text);
```

Now the styled text lives inside the outline element.

### Adım 9: OutlineElement Düğümünü Outline'a Ekle
```java
outline.appendChildLast(outlineElem);
```

The outline now contains the element that holds our paragraph.

### Adım 10: Outline Düğümünü Page'e Ekle
```java
page.appendChildLast(outline);
```

We place the outline onto the page.

### Adım 11: Page Düğümünü Document'e Ekle
```java
doc.appendChildLast(page);
```

The document now has a single page with our styled text.

### Adım 12: Belgeyi Kaydet (Export OneNote PDF)
```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

The `save` method writes the OneNote file and **exports OneNote PDF** in one step. You can also save as `.one` by using `SaveFormat.One` if you need the native format.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **File not found** | `dataDir`, var olmayan bir klasöre işaret ediyor. | Dizinin var olduğundan emin olun veya programlı olarak oluşturun (`new File(dataDir).mkdirs();`). |
| **Blank PDF** | Kaydetmeden önce içerik eklenmemiş. | `RichText` düğümünün eklendiğini ve stilin ayarlandığını doğrulayın. |
| **Unsupported font** | Yazı tipi adı sistemde yüklü değil. | "Arial" gibi yaygın bir yazı tipi kullanın veya yazı tipini projeye gömün. |

## Sıkça Sorulan Sorular

**Q: Aspose.Note karmaşık biçimlendirmeleri (tablolar veya resimler gibi) işleyebilir mi?**  
A: Evet, API tabloları, resimleri, hiperlinkleri ve daha gelişmiş düzen özelliklerini destekler.

**Q: OneNote PDF'yi bir OneNote dosyasına geri dönüştürmek mümkün mü?**  
A: Doğrudan dönüşüm sağlanmaz, ancak PDF içeriğini çıkarıp API kullanarak bir OneNote belgesi yeniden oluşturabilirsiniz.

**Q: Kütüphane Linux/macOS ortamlarında çalışır mı?**  
A: Kesinlikle. Aspose.Note for Java platform bağımsızdır; sadece JDK'nın kurulu olduğundan emin olun.

**Q: Birden fazla sayfa veya outline nasıl eklenir?**  
A: Ek `Page` ve `Outline` nesneleri oluşturun, ardından tek sayfalı örnek gibi `Document`'e ekleyin.

**Q: Daha fazla örnek nerede bulunur?**  
A: Resmi Aspose.Note belgeleri ve [support forum](https://forum.aspose.com/c/note/28) birçok kod örneği içerir.

## Sonuç

Artık **set paragraph style**, **add outline element** ve Aspose.Note for Java kullanarak **exported to PDF** yapılabilen bir **OneNote dosyası** oluşturmayı gördünüz. Oluşturma sürecinin erken aşamasında stillendirilmiş metin eklemek, son belgenin profesyonel görünmesini ve sonraki **convert OneNote PDF** işleminin biçimlendirmeyi korumasını sağlar. Projenizin ihtiyaçlarını karşılamak için bu temeli resimler, tablolar veya özel meta verilerle genişletmekten çekinmeyin.

---

**Son Güncelleme:** 2026-02-18  
**Test Edilen:** Aspose.Note for Java 24.11 (latest release)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}