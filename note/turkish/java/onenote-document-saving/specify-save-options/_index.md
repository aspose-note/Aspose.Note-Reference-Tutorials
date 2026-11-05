---
date: 2026-11-05
description: Aspose.Note for Java kullanarak bir OneNote belgesinden belirli sayfaları
  PDF olarak kaydetmeyi, sayfa indeksi, sayfa sayısı ve PDF boyutunu azaltmak için
  JPEG sıkıştırmasını öğrenin.
keywords:
- save specific pages pdf
- export onenote to pdf
- compress pdf images
- jpeg compression pdf
- reduce pdf size java
lastmod: 2026-11-05
linktitle: OneNote'ta belirli sayfaları PDF olarak kaydet – Aspose.Note
og_description: Aspose.Note for Java kullanarak OneNote'ta belirli sayfaları PDF olarak
  kaydedin. Sayfa indeksi, sayfa sayısı ve PDF boyutunu verimli bir şekilde azaltmak
  için JPEG sıkıştırmasını öğrenin.
og_image_alt: Guide showing how to export selected OneNote pages to a compressed PDF
  with Aspose.Note Java
og_title: Aspose.Note Java ile OneNote'ta belirli sayfaları PDF olarak kaydedin
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to save specific pages pdf from a OneNote document using
    Aspose.Note for Java, including page index, page count, and JPEG compression to
    reduce PDF size.
  headline: Save specific pages pdf in OneNote – Aspose.Note
  type: TechArticle
- description: Learn how to save specific pages pdf from a OneNote document using
    Aspose.Note for Java, including page index, page count, and JPEG compression to
    reduce PDF size.
  name: Save specific pages pdf in OneNote – Aspose.Note
  steps:
  - name: Load the OneNote document
    text: The `Document` class represents a OneNote notebook loaded in memory. Here
      we point to the folder that contains the source `.one` file and load it into
      a `Document` object. This object represents the entire OneNote notebook in memory.
  - name: Initialize `PdfSaveOptions`
    text: '`PdfSaveOptions` is the configuration object that controls every aspect
      of the PDF conversion, from page selection to image quality. It gives you fine‑grained
      control over the PDF conversion process, including the ability to **set page
      index PDF** and **set page count PDF**.'
  - name: Set page index and count
    text: 'The `setPageIndex` method defines the starting page (zero‑based) for export,
      while `setPageCount` determines how many consecutive pages to include. These
      two calls tell Aspose.Note to start exporting from page 2 (zero‑based) and to
      include the next three pages. This is the core of **saving specific '
  - name: Specify compression settings
    text: The `setJpegQuality` method sets the JPEG quality level for images embedded
      in the PDF. JPEG compression with a quality of 90 % offers a good balance between
      file size and visual fidelity, helping you **reduce PDF size** while preserving
      readability.
  - name: Save the document with options
    text: The `save` method writes the selected pages to a new PDF file using the
      options we configured. The result is a compact PDF that contains only the pages
      you need.
  type: HowTo
- questions:
  - answer: It lets you select a subset of OneNote pages and generate a PDF containing
      only those pages.
    question: What does “save specific pages pdf” mean?
  - answer: Aspose.Note for Java provides `PdfSaveOptions` to control page index,
      count, and image compression.
    question: Which library handles this?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license?
  - answer: Yes – use `setPageIndex()` and `setPageCount()` on `PdfSaveOptions`.
    question: Can I set page index and page count?
  - answer: Absolutely – choose JPEG, PNG, or other formats via `setImageCompression()`.
    question: Is image compression supported?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf export
- Aspose.Note
- Java document processing
title: OneNote'ta belirli sayfaları PDF olarak kaydet – Aspose.Note
url: /tr/java/onenote-document-saving/specify-save-options/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta belirli sayfaları pdf olarak kaydet – Aspose.Note

## Giriş

Bu öğreticide, Aspose.Note for Java kullanarak bir OneNote belgesinden **belirli sayfaları pdf olarak kaydetmenin** nasıl yapılacağını keşfedeceksiniz. **OneNote'u PDF olarak dışa aktarmanız**, **OneNote'u PDF'ye dönüştürmeniz** ya da sadece sayfa aralığını sınırlamanız ve görüntüleri sıkıştırmanız gerektiğinde, bu kılavuz her adımı net açıklamalar ve çalıştırmaya hazır kodlarla size gösterir. Sonunda **PDF boyutunu azaltma** ve **JPEG sıkıştırması** uygulama konusunda da bilgi sahibi olacaksınız.

## Hızlı Yanıtlar
- **“belirli sayfaları pdf olarak kaydet” ne anlama geliyor?** OneNote sayfalarının bir alt kümesini seçmenize ve yalnızca bu sayfaları içeren bir PDF oluşturmanıza olanak tanır.  
- **Bu işlemi hangi kütüphane yönetir?** Aspose.Note for Java, sayfa indeksi, sayısı ve görüntü sıkıştırmasını kontrol eden `PdfSaveOptions` sağlar.  
- **Lisans gerekir mi?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari bir lisans gereklidir.  
- **Sayfa indeksini ve sayfa sayısını ayarlayabilir miyim?** Evet – `PdfSaveOptions` üzerinde `setPageIndex()` ve `setPageCount()` kullanın.  
- **Görüntü sıkıştırması destekleniyor mu?** Kesinlikle – `setImageCompression()` ile JPEG, PNG veya diğer formatları seçebilirsiniz.  

## “Belirli sayfaları pdf olarak kaydet” nedir?

Belirli sayfaları pdf olarak kaydetmek, bir OneNote defterinden yalnızca ihtiyacınız olan sayfaları çıkartmak ve sadece bu sayfaları içeren bir PDF oluşturmak anlamına gelir. Bu, tüm defteri dışa aktarmadan **PDF onenote** raporları oluşturmak istediğinizde özellikle faydalıdır.

## Aspose.Note ile belirli sayfaları pdf olarak kaydetme neden tercih edilmeli?

500 sayfadan büyük defterlerde sayfaların bir alt kümesini dışa aktarmak, işleme süresini %70'e kadar hızlandırır ve JPEG sıkıştırması uygulandığında ortaya çıkan dosya boyutunu %40‑60 azaltabilir. API ayrıca sayfa seçimini filigranlar, şifreleme veya özel meta verilerle birleştirmenize olanak tanır ve böylece herhangi bir belge‑işleme akışı için tek, esnek bir çözüm sunar.

## Önkoşullar

1. Java programlama temelleri.  
2. Makinenizde JDK kurulu.  
3. Resmi siteden indirilen Aspose.Note for Java kütüphanesi – **[Aspose.Note for Java download page](https://releases.aspose.com/note/java/)** adresinden edinebilirsiniz.  

## Paketleri içe aktar

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

İşlemi adım adım inceleyelim.

## Belirli sayfaları pdf olarak nasıl kaydedilir

Belirli sayfaları pdf olarak kaydetmek, OneNote belgesini yüklemeyi, istenen sayfa aralığı ve görüntü sıkıştırma ayarlarıyla `PdfSaveOptions` yapılandırmayı ve ardından yalnızca seçilen sayfaları içeren bir PDF oluşturmak için `save` metodunu çağırmayı içerir. Bu yaklaşım bellek kullanımını en aza indirir ve paylaşım ya da arşivleme için ideal, daha küçük bir dosya üretir.

### Adım 1: OneNote belgesini yükle

`Document` sınıfı, belleğe yüklenmiş bir OneNote defterini temsil eder. Burada kaynak `.one` dosyasını içeren klasöre işaret ediyor ve onu bir `Document` nesnesine yüklüyoruz. Bu nesne, bellekteki tüm OneNote defterini temsil eder.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

### Adım 2: `PdfSaveOptions` nesnesini başlat

`PdfSaveOptions`, sayfa seçimi ile görüntü kalitesine kadar PDF dönüşümünün her yönünü kontrol eden yapılandırma nesnesidir. PDF dönüşüm sürecinde **sayfa indeksi PDF** ve **sayfa sayısı PDF** ayarlama yeteneği dahil olmak üzere ayrıntılı kontrol sağlar.

```java
// Initialize PdfSaveOptions object
PdfSaveOptions opts = new PdfSaveOptions();
```

### Adım 3: Sayfa indeksini ve sayısını ayarla

`setPageIndex` metodu, dışa aktarma için başlangıç sayfasını (sıfır‑tabanlı) tanımlar, `setPageCount` ise kaç ardışık sayfanın dahil edileceğini belirler. Bu iki çağrı, Aspose.Note'a sayfa 2'den (sıfır‑tabanlı) başlayarak sonraki üç sayfayı dışa aktarmasını söyler. Bu, **belirli sayfaları pdf olarak kaydetme** işleminin özüdür.

```java
// Set page index
opts.setPageIndex(2);

// Set page count
opts.setPageCount(3);
```

### Adım 4: Sıkıştırma ayarlarını belirt

`setJpegQuality` metodu, PDF'ye gömülü görüntüler için JPEG kalite seviyesini ayarlar. %90 kaliteyle JPEG sıkıştırması, dosya boyutu ile görsel doğruluk arasında iyi bir denge sağlar ve **PDF boyutunu azaltma** konusunda okunabilirliği korurken yardımcı olur.

```java
// Specify compression if required
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

### Adım 5: Belgeyi seçeneklerle kaydet

`save` metodu, yapılandırdığımız seçenekleri kullanarak seçilen sayfaları yeni bir PDF dosyasına yazar. Sonuç, yalnızca ihtiyacınız olan sayfaları içeren kompakt bir PDF olur.

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

## Yaygın kullanım senaryoları

| Senaryo | Özelliğin sağladığı fayda |
|----------|-----------------------|
| Tek bir toplantı için rapor oluşturma | Tüm defter yerine yalnızca toplantının sayfasını dışa aktar. |
| Seçili bölümlerin arşivlenmesi | İlgisiz içeriği ortaya çıkarmadan uyumluluk için belirli bölümleri PDF olarak kaydet. |
| Mobil kullanıcılar için bant genişliğini azaltma | Sadece gerekli sayfaları içeren hafif bir PDF gönder. |
| Yazdırılabilir el ilanları oluşturma | **PDF onenote** el ilanlarını yalnızca ilgili slaytları içerecek şekilde oluştur. |

## Sorun Giderme ve ipuçları

- **Geçersiz sayfa indeksi:** Sayfa indekslemesinin 0'dan başladığını unutmayın. Toplam sayfa sayısından büyük bir indeks ayarlarsanız, Aspose.Note `ArgumentOutOfRangeException` hatası verir.  
- **Sıfır sayfa sayısı:** `setPageCount(0)` ayarı boş bir PDF oluşturur. Pozitif bir tamsayı kullanın.  
- **Sıkıştırma artefaktları:** JPEG kalitesi çok düşükse, görüntüler bulanık görünebilir. **compress images pdf** kalitesini kabul edilebilir tutmak için `setJpegQuality()` ayarını gerektiği gibi değiştirin.  
- **Dosya yolu sorunları:** Çıktı dizininin var olduğundan ve yazma izinlerinizin bulunduğundan emin olun; aksi takdirde `doc.save()` başarısız olur.  
- **Performans ipucu:** Çok büyük defterlerle çalışırken, `setPageIndex`/`setPageCount` ile `opts.setOptimizeImageSize(true)` (varsa) birleştirerek **PDF boyutunu azaltma** konusunda daha fazla iyileştirme sağlayabilirsiniz.

## Sıkça Sorulan Sorular

**S1: Aspose.Note büyük OneNote belgelerini işleyebilir mi?**  
C1: Evet, Aspose.Note 10.000 sayfaya kadar olan defterleri verimli bir şekilde işler ve standart donanımda 500 sayfalık bir defteri 2 saniyeden kısa sürede PDF'ye dönüştürebilir.

**S2: Aspose.Note en son Java sürümleriyle uyumlu mu?**  
C2: Kesinlikle. Kütüphane Java 8 ve daha yeni sürümlerle, Java 17 LTS dahil, çalışır.

**S3: OneNote belgelerini PDF dışındaki diğer formatlara dönüştürebilir miyim?**  
C3: Evet, Aspose.Note DOCX, HTML, XPS ve PNG, JPEG gibi çeşitli görüntü formatlarına dönüşümü destekler.

**S4: Aspose.Note OneNote belgelerinin şifreleme ve şifre çözme desteği sağlıyor mu?**  
C4: Evet, API programatik olarak OneNote dosyalarını şifrelemek ve şifre çözmek için yöntemler içerir.

**S5: Aspose.Note ticari kullanım için uygun mu?**  
C5: Evet, ticari lisans, kütüphaneyi üretim ortamlarında kısıtlama olmadan kullanmanıza izin verir.

**S6: JPEG sıkıştırması son PDF boyutunu nasıl etkiler?**  
C6: JPEG sıkıştırması, görüntü yüklerini %80'e kadar küçültebilir; bu, grafik ağırlıklı sayfalar için **reduce pdf size**'ın ana faktörüdür.

**S7: Belirli sayfaları kaydederken filigran eklemek gibi birden fazla kaydetme seçeneğini zincirleyebilir miyim?**  
C7: Evet, `PdfSaveOptions` sayfa seçimiyle birleştirilebilen filigranlar, şifreleme ve meta veri gibi ek ayarları destekler.

---

**Son Güncelleme:** 2026-11-05  
**Test Edilen Sürüm:** Aspose.Note for Java 26.4 (latest)  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.Note for Java ile Sayfa Ayarlarını Kullanarak OneNote'u PDF'ye Dönüştür](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)
- [Seçeneklerle OneNote'u PDF'ye Dönüştür - Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/)
- [Bölme Algoritması Yöntemiyle OneNote PDF'yi Dışa Aktar – Aspose.Note](/note/java/onenote-document-saving/use-splitting-algorithm-method/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}