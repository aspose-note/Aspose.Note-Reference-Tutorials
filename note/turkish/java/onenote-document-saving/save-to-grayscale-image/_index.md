---
date: 2026-06-30
description: Aspose.Note for Java kullanarak bir belgeyi gri tonlu PNG görüntüsü olarak
  kaydederek OneNote'u nasıl dışa aktaracağınızı öğrenin. OneNote belgesini yükleme
  ve gri tonlu görüntü oluşturma adımlarını içerir.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: OneNote'u Gri Tonlu Görüntü Olarak Dışa Aktarma – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: OneNote'u Gri Tonlu Görüntü Olarak Dışa Aktarma – Aspose.Note
url: /tr/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'ta Gri Tonlu Görüntü Olarak Kaydet - Aspose.Note

## Giriş

Bu öğreticide, Aspose.Note for Java kullanarak bir OneNote `.one` dosyasını yüksek‑kaliteli gri tonlu PNG görüntüsüne dönüştürerek **how to export onenote**'ı keşfedeceksiniz. Gri tonlu dönüşüm, Java geliştiricileri tarafından genellikle baskı, arşivleme veya **OneNote boyutunu azaltmak** için, temel içeriği kaybetmeden ihtiyaç duyulur. Bir OneNote belgesini yükleme, kaydetme seçeneklerini yapılandırma—**görüntü çözünürlüğünü ayarlama** dahil—ve sonunda belgeyi PNG olarak kaydetme adımlarını göstereceğiz.

## Hızlı Yanıtlar
- **“how to export onenote” ne anlama geliyor?** Kod kullanarak bir OneNote dosyasını başka bir formata, örneğin bir görüntüye, programlı olarak dönüştürmeyi ifade eder.  
- **Gri tonlu çıktı için en iyi format hangisidir?** PNG, kayıpsız kaliteyi koruduğu ve özel bir gri tonlu renk modu desteklediği için iyi çalışır.  
- **Bir lisansa ihtiyacım var mı?** Üretim kullanımı için geçerli bir Aspose.Note lisansı gereklidir; test için geçici bir deneme lisansı mevcuttur.  
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri önerilir.  
- **Görüntü boyutunu değiştirebilir miyim?** Evet, kaydetmeden önce `ImageSaveOptions` özelliklerini `Resolution` veya `PageSize` gibi ayarlayabilirsiniz.  

## “how to export onenote” nedir?

OneNote'u dışa aktarmak, bir OneNote `.one` dosyasını programlı olarak başka bir temsile—örneğin PDF, HTML veya bir görüntü—dönüştürmeyi ifade eder. Bu rehberde **gri tonlu PNG** görüntüleri oluşturmayı odak noktamız olarak ele alıyoruz; bu, dokümantasyon veya baskıya hazır iş akışları için yaygın bir gereksinimdir. Aspose.Note kullanarak dönüşüm tamamen bellek içinde gerçekleşir, bu sayede sunucuda Microsoft OneNote yüklü olmasına hiç ihtiyaç duymazsınız.

## Neden OneNote'u gri tonlu görüntü olarak dışa aktarıyorsunuz?

Gri tonlu PNG'ler genellikle **%30‑40 daha küçüktür** tam renkli karşılıklarından, bu da web teslimatını hızlandırır ve depolama maliyetlerini azaltır. Ayrıca lazer yazıcılarda **daha net kontrast** sağlar, raporların okunmasını kolaylaştırır. PNG evrensel olarak desteklendiği için ortaya çıkan dosyalar tarayıcılarda, mobil cihazlarda ve ek kod çözücülere ihtiyaç duymadan masaüstü editörlerde çalışır.

## Önkoşullar

1. Java Development Kit (JDK) 8 veya daha yeni bir sürüm yüklü olmalıdır.  
2. Aspose.Note for Java kütüphanesi – en son sürümü [buradan](https://releases.aspose.com/note/java/) indirin.  
3. Java sözdizimi ve Maven/Gradle proje kurulumu hakkında temel bir anlayış.  

## Paketleri İçe Aktar

`ImageSaveOptions` sınıfı, belgenin bir görüntüye nasıl render edileceğini kontrol eder.  
`ColorMode` ise tam renk ve gri tonlu çıktı arasında geçiş yapmanızı sağlayan bir enumdur.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Adım 1: OneNote Belgesini Yükleyin

`Document` bir OneNote defterini temsil eder ve içeriğini yükleme, düzenleme ve kaydetme yöntemleri sunar. İlk olarak, **OneNote belgesini** Aspose.Note içine yükleyin. `"Your Document Directory"` ifadesini yerel klasörünüzün yolu ile, `"Aspose.one"` ifadesini OneNote dosyanızın adıyla değiştirin.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Adım 2: Çıktı Yolu ve Seçeneklerini Ayarlayın

`ImageSaveOptions` bir OneNote belgesinin bir görüntü dosyasına nasıl render edileceğini yapılandırır. `ColorMode` enumu, gri tonlu veya tam renk gibi renk render modunu seçmenizi sağlar. Gri tonlu görüntünün çıktı yolunu tanımlayın ve kaydetme seçeneklerini belirtin. `ColorMode` değerini `GrayScale` olarak ayarlayacağız ve **belgeyi PNG olarak kaydet** formatını kullanacağız. Ayrıca **görüntü çözünürlüğünü** yüksek kaliteli baskılar için 300 DPI olarak ayarlayabilirsiniz.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Adım 3: Belgeyi Kaydedin

Son olarak, yapılandırılmış seçenekleri kullanarak belgeyi gri tonlu PNG görüntüsü olarak kaydedin. `save` yöntemi, ara geçici dosyalara ihtiyaç duymadan dosyayı diske yazar.

```java
oneFile.save(dataDir, options);
```

## Yaygın Sorunlar ve Çözümler
- **FileNotFoundException** – `dataDir`'in doğru klasöre işaret ettiğini ve `.one` dosyasının mevcut olduğunu doğrulayın.  
- **LicenseException** – `save` metodunu çağırmadan önce geçerli bir Aspose.Note lisansı uyguladığınızdan emin olun.  
- **Low‑resolution output** – DPI'yi artırmak için `options.setResolution(300)` ayarını yapın; daha yüksek DPI daha keskin baskılar sağlar ancak dosya boyutu artar.  

## Sıkça Sorulan Sorular

**Q1: Gri tonlu görüntüyü farklı bir formatta kaydedebilir miyim?**  
A1: Evet, `ImageSaveOptions` yapıcısındaki `SaveFormat` parametresini `Jpeg`, `Bmp` veya desteklenen 20+ görüntü formatından herhangi birine değiştirmeniz yeterlidir.

**Q2: Aspose.Note tüm OneNote belge sürümleriyle uyumlu mu?**  
A2: Aspose.Note, Microsoft OneNote 2010 ve sonrası sürümleri destekler; bu da bugün aktif olarak kullanılan defterlerin %95'inden fazlasını kapsar.

**Q3: Aspose.Note kullanmak için bir lisansa ihtiyaç var mı?**  
A3: Üretim kullanımı için geçerli bir lisans gereklidir, ancak değerlendirme amacıyla ücretsiz bir deneme lisansı alınabilir.

**Q4: Belgeyi görüntü olarak kaydetmeden önce başka yönlerini değiştirebilir miyim?**  
A4: Kesinlikle! Aspose.Note, bölümleri, sayfaları ve metin, tablo, resim gibi bireysel öğeleri dışa aktarmadan önce düzenlemenize olanak tanıyan API'ler sunar.

**Q5: Sorun yaşarsam nereden destek alabilirim?**  
A5: Aspose.Note forumunda [buradan](https://forum.aspose.com/c/note/28) destek bulabilirsiniz.

## Sonuç

Artık **how to export onenote**'ı, bir OneNote dosyasını yükleyerek, **gri tonlu bir görüntü** oluşturmak için kaydetme seçeneklerini yapılandırarak ve **belgeyi PNG olarak kaydederek** öğrendiniz. Bu yaklaşım, OneNote defterlerinden hafif, baskıya hazır görseller üretmek için idealdir. Projenizin gereksinimlerine uygun olarak diğer `ColorMode` ayarlarını, daha yüksek DPI değerlerini veya alternatif görüntü formatlarını denemekten çekinmeyin.

---

**Son Güncelleme:** 2026-06-30  
**Test Edilen:** Aspose.Note 27.0 for Java  
**Yazar:** Aspose  

---

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Java'da Aspose.Note kullanarak OneNote Sayfasını PNG Görüntüsü olarak Dışa Aktarın](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote jpeg çözünürlüğünü ayarla – OneNote'ta Çıktı Görüntü Çözünürlüğünü Ayarla - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Java için Aspose.Note ile OneNote'u PDF olarak Kaydetme](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}