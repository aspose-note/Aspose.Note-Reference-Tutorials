---
date: 2026-03-29
description: Aspose.Note for Java kullanarak OneNote defterlerini seçeneklerle PDF'ye
  dönüştürün, defteri PDF olarak kaydedin ve PDF'ye başlık ve alt bilgi ekleyin.
linktitle: Convert Notebook to PDF with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'u PDF'ye seçeneklerle dönüştür - Aspose.Note
url: /tr/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note ile Seçenekler Kullanarak OneNote'u PDF'ye Dönüştürme

## Giriş

Bu öğreticide, çıktıyı tam kontrol ederek **convert onenote to pdf** nasıl yapılacağını öğreneceksiniz. Aspose.Note for Java, OneNote defterlerini PDF'ye dışa aktarmayı kolaylaştırır; **save notebook as pdf** yaparken başlıkları, altbilgileri ve sayfa bölme davranışını özelleştirmenizi sağlar. Rapor oluşturmanız, toplantı notlarını arşivlemeniz veya OneNote olmayan kullanıcılarla içerik paylaşmanız gerektiğinde, bu kılavuz size adım adım yol gösterir.

## Hızlı Yanıtlar
- **Dönüşümü hangi kütüphane yönetir?** Aspose.Note for Java.
- **PDF'ye bir başlık veya altbilgi ekleyebilir miyim?** Evet – özel başlık/altbilgi eklemek için PDF kaydetme seçeneklerini kullanın.
- **Üretim için bir lisansa ihtiyacım var mı?** Deneme dışı kullanım için ticari bir lisans gereklidir.
- **Hangi Java sürümleri destekleniyor?** Java 8 ve üzeri.
- **Dönüşüm ne kadar sürer?** Ortalama boyuttaki defterler için genellikle birkaç saniye sürer.

## “convert onenote to pdf” nedir?

OneNote'u PDF'ye dönüştürmek, bir OneNote defterini ( *.onetoc2* dosyası) alıp her sayfayı bir PDF sayfası olarak oluşturmak anlamına gelir. Oluşan PDF, metin, görüntü ve düzeni korur, böylece OneNote gerektirmeden herhangi bir cihazda görüntülenebilir.

## Aspose.Note'ı OneNote defteri PDF'si olarak dışa aktarmak için neden kullanmalısınız?

- **Office kurulumu gerekmez** – API bağımsız çalışır.
- **İnce ayarlı kontrol** – sayfa bölme algoritmalarını ayarlayabilir, yazı tiplerini gömebilir ve başlık/altbilgi ekleyebilirsiniz.
- **Yüksek doğruluk** – orijinal defterin görsel görünümü korunur.
- **Çapraz platform** – Windows, Linux ve macOS'ta herhangi bir Java çalışma zamanı ile çalışır.

## Önkoşullar

Başlamadan önce, aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1. Java Development Kit (JDK) – JDK 8 veya daha yeni bir sürüm yüklü.
2. Aspose.Note for Java – [download link](https://releases.aspose.com/note/java/) adresinden indirin ve kurun.
3. IDE (Integrated Development Environment) – IntelliJ IDEA, Eclipse veya NetBeans popüler seçeneklerdir.

## Paketleri İçe Aktarma

İlk olarak, Java projenize gerekli paketleri içe aktarmanız gerekir. Bu paketler, OneNote belgeleriyle çalışmak için gereken sınıf ve metodları sağlar.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Adım 1: OneNote Defterini Yükleme

**convert onenote to pdf** yapmak için önce OneNote defterini yüklemeniz gerekir. Defter dosyasının yolunun doğru belirtildiğinden emin olun.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Adım 2: PDF Kaydetme Seçeneklerini Belirleme

Aspose.Note, PDF çıktısını özelleştirmek için çeşitli seçenekler sunar. Sayfa bölme algoritmaları, başlık/altbilgi ayarları gibi seçenekleri belirtebilirsiniz.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Adım 3: Defteri PDF Olarak Kaydetme

Defteri yükleyip kaydetme seçeneklerini belirledikten sonra, **save the notebook as pdf** zamanıdır.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| PDF'de eksik görüntüler | Görüntüler gömülü nesneler olarak depolanmış ancak yüklenmemiş | Defter dosyasının ve tüm bağlı kaynakların yüklemeden önce aynı dizinde olduğundan emin olun. |
| Başlık/altbilgi görünmüyor | `PdfSaveOptions` içinde başlık/altbilgi seçenekleri ayarlanmamış | Kaydetmeden önce içeriği tanımlamak için `documentSaveOptions.setHeaderFooter()` kullanın. |
| Büyük defterlerde bellek hatası | Tüm defter belleğe yüklenmiş | Defteri bölümler halinde işleyin veya JVM yığın boyutunu (`-Xmx2g`) artırın. |

## Sık Sorulan Sorular

### Q1: PDF çıktısının görünümünü özelleştirebilir miyim?
A1: Evet, Aspose.Note, başlık/altbilgi ayarları, sayfa bölme algoritmaları ve daha fazlasını içeren PDF çıktısını özelleştirmek için çeşitli seçenekler sunar.

### Q2: Aspose.Note tüm OneNote sürümleriyle uyumlu mu?
A2: Aspose.Note, Microsoft OneNote 2010 ve sonraki sürümlerini destekler.

### Q3: Aspose.Note ücretsiz deneme sunuyor mu?
A3: Evet, Aspose.Note'un ücretsiz denemesini [buradan](https://releases.aspose.com/) indirebilirsiniz.

### Q4: Aspose.Note belgelerini nerede bulabilirim?
A4: Aspose.Note için kapsamlı belgeleri [burada](https://reference.aspose.com/note/java/) bulabilirsiniz.

### Q5: Aspose.Note için destek nasıl alabilirim?
A5: Herhangi bir teknik yardım veya soru için Aspose.Note destek forumunu [buradan](https://forum.aspose.com/c/note/28) ziyaret edebilirsiniz.

## Ek Sık Sorulan Sorular

**Q: Özel bir PDF başlık veya altbilgi nasıl eklenir?**  
A: Bir `PdfHeaderFooterOptions` nesnesi oluşturun, metin veya görüntüleri yapılandırın ve `save` metodunu çağırmadan önce `documentSaveOptions.setHeaderFooterOptions()`'a atayın.

**Q: Bir defterin yalnızca seçili bölümlerini dışa aktarabilir miyim?**  
A: Evet – defteri yükleyin, istediğiniz `Section` nesnelerini alın ve aynı PDF seçenekleriyle `section.save()` metodunu çağırın.

**Q: Oluşturulan PDF şifrelenebilir mi?**  
A: Kesinlikle. PDF'i korumak için `documentSaveOptions.setEncryptionPassword("yourPassword")` kullanın.

**Q: Hangi performans hususlarını göz önünde bulundurmalıyım?**  
A: Çok büyük defterlerde, çıktıyı bir `FileOutputStream`'e akıtmayı ve `OutOfMemoryError` ile karşılaşırsanız JVM yığın boyutunu artırmayı düşünün.

---

**Son Güncelleme:** 2026-03-29  
**Test Edildi:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}