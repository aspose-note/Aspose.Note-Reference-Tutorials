---
date: 2026-03-03
description: Java için Aspose.Note kullanarak OneNote'ta madde işaretli liste oluşturmayı
  ve OneNote belgesini PDF olarak kaydetmeyi öğrenin. Java madde işaretleriyle adım
  adım rehber.
linktitle: Create Bulleted List OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'ta Madde İşaretli Liste Oluştur - Aspose.Note
url: /tr/java/onenote-text-manipulation/create-bulleted-list/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'da Madde İşaretli Liste Oluşturma - Aspose.Note

## Introduction
Eğer programlı olarak **OneNote'da madde işaretli liste oluşturmak** istiyorsanız, Aspose.Note for Java size OneNote iç işleyişini sizin yerinize yöneten temiz, akıcı bir API sunar. Bu öğreticide, Java'da madde işaretlerini ayarlama, bunları bir taslağa ekleme ve sonunda **OneNote belgesini PDF olarak kaydetme** adımlarını adım adım göstereceğiz. Sonunda, herhangi bir Java projesine ekleyebileceğiniz hazır bir kod parçacığına sahip olacaksınız.

## Quick Answers
- **Aspose.Note ne yapar?** OneNote dosyalarını OneNote kurmadan oluşturmanıza, düzenlemenize ve dönüştürmenize olanak tanır.  
- **Java ile madde işaretleri ayarlayabilir miyim?** Evet – madde işareti stilini tanımlamak için `NumberList` kullanın.  
- **PDF olarak nasıl dışa aktarırım?** Sayfayı oluşturduktan sonra `doc.save(...".pdf")` çağırın.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü çalışır; üretim için lisans gereklidir.  
- **Hangi IDE'ler destekleniyor?** Eclipse, IntelliJ IDEA veya VS Code gibi herhangi bir Java IDE'si.

## What is “create bulleted list OneNote”?
OneNote'da madde işaretli bir liste oluşturmak, her öğesi bir madde işareti karakteri (ör. “*”) ile başlayan bir dizi taslak öğesi eklemek anlamına gelir. Bu yapı okunabilirliği artırır ve kullanıcıların OneNote arayüzünde manuel olarak liste ekleme şeklini taklit eder.

## Why use Aspose.Note for Java to set bullet points?
- **OneNote kurulumu gerekmez** – sunucularda ve CI pipeline'larında çalışır.  
- **Stil üzerinde tam kontrol** – yazı tipi, boyut, renk ve madde işareti karakteri tamamen yapılandırılabilir.  
- **Doğrudan PDF dışa aktarımı** – tek satırda PDF oluşturur, raporlama veya arşivleme için mükemmeldir.  

## Prerequisites
Başlamadan önce şunlara sahip olduğunuzdan emin olun:

- Temel Java programlama bilgisi.  
- Aspose.Note for Java kütüphanesi yüklü – [Aspose.Note for Java Documentation](https://reference.aspose.com/note/java/) adresinden indirin.  
- Makinenizde kurulu bir Java IDE'si (Eclipse, IntelliJ IDEA vb.).

## Import Packages
Gerekli paketleri Java projenize içe aktararak başlayın. Bu, kullanacağımız tüm Aspose.Note sınıflarına erişmenizi sağlar.

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
// Import Aspose.Note for Java packages
```

## Step 1: Initialize Document and Page
`Outline`'ın bulunacağı bir `Document` örneği ve bir `Page` oluşturun.

```java
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
// initialize Page class object
Page page = new Page();
```

## Step 2: Initialize Outline and TextStyle (set bullet points java)
Bir `Outline` konteyneri kuracağız ve varsayılan bir `ParagraphStyle` tanımlayacağız. İşte **Java madde işareti ayarlama** stil formatlamasını yaptığımız yer.

```java
// initialize Outline class object
Outline outline = new Outline();
// initialize TextStyle class object and set formatting properties
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

## Step 3: Create Bulleted List Elements
Bireysel `OutlineElement` nesneleri oluşturun, madde işareti karakterini tanımlayan bir `NumberList` ekleyin ve metni ekleyin.

```java
// initialize OutlineElement class objects and apply bullets
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// initialize RichText class object and apply text style
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```

*İhtiyacınız olan her ek madde için yukarıdaki bloğu tekrarlayın (ör. `outlineElem2`, `outlineElem3`).*

## Step 4: Add Outline Elements to Outline
Tüm madde işareti öğelerini ana `Outline` içine toplayın.

```java
// add outline elements
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

## Step 5: Add Outline to Page and Save (save OneNote document as PDF)
`Outline`'ı `Page`'e ekleyin, sayfayı `Document`'e ekleyin ve sonunda **OneNote belgesini PDF olarak kaydedin**.

```java
// add Outline node
page.appendChildLast(outline);
// add Page node
doc.appendChildLast(page);
// save the document
doc.save(dataDir + "CreateBulletedList_out.pdf");
```

Tebrikler! Artık programlı olarak **OneNote'da madde işaretli liste oluşturmuş** ve Aspose.Note for Java kullanarak PDF olarak dışa aktarmış durumdasınız.

## Common Issues and Solutions
| Sorun | Çözüm |
|-------|----------|
| `outlineElem2` veya `outlineElem3` tanımlı değil | Step 3'ten kod bloğunu her ek madde için çoğaltıp değişkenleri uygun şekilde yeniden adlandırdığınızdan emin olun. |
| PDF dosyası oluşturulmadı | `dataDir`'in yazılabilir bir klasöre işaret ettiğini ve yazma izinlerinizin olduğunu doğrulayın. |
| Madde işareti stili farklı görünüyor | İstediğiniz görünüme uyması için `NumberList` yapıcı parametrelerini (yazı tipi, boyut veya karakter) ayarlayın. |

## Frequently Asked Questions

**S: Aspose.Note for Java tüm Java IDE'leriyle uyumlu mu?**  
C: Evet, Eclipse, IntelliJ IDEA, NetBeans ve standart Java projelerini destekleyen herhangi bir IDE ile çalışır.

**S: Madde işaretli listenin biçimlendirmesini özelleştirebilir miyim?**  
C: Kesinlikle! `NumberList` parametrelerini değiştirerek yazı tipini, rengi, boyutu ve hatta özel Unicode sembollerini kullanabilirsiniz.

**S: Aspose.Note for Java için ek destek nereden bulunabilir?**  
C: Topluluk yardımı ve resmi destek için [Aspose.Note for Java support forum](https://forum.aspose.com/c/note/28) adresini ziyaret edin.

**S: Aspose.Note for Java için ücretsiz deneme sürümü var mı?**  
C: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) inceleyebilirsiniz.

**S: Aspose.Note for Java için geçici lisans nasıl alınır?**  
C: Geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

## Conclusion
Aspose.Note for Java, birkaç kısa adımda **OneNote'da madde işaretli liste oluşturmayı**, her maddeyi biçimlendirmeyi ve **OneNote belgesini PDF olarak kaydetmeyi** kolaylaştırır. Uygulamanızın tasarım diline uyması için farklı madde işareti karakterleri, yazı tipleri ve renklerle denemeler yapmaktan çekinmeyin. Tablolar, görseller ve hiperlinkler gibi diğer Aspose.Note özelliklerini keşfederek daha zengin OneNote içeriği oluşturun.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-03-03  
**Test Edilen Sürüm:** Aspose.Note for Java 24.11  
**Yazar:** Aspose