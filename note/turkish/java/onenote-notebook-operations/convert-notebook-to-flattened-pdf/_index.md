---
date: 2025-12-28
description: Aspose.Note for Java kullanarak bir OneNote defterinden PDF düzleştirmeyi
  öğrenin. Bu kılavuz, OneNote'u PDF'ye dönüştürmeyi, dışa aktarma seçeneklerini özelleştirmeyi
  ve Aspose PDF kaydetme seçeneklerini kullanmayı gösterir.
linktitle: Convert Notebook to Flattened PDF in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote Defterinden PDF'yi Düzleştirme – Aspose.Note Öğreticisi
url: /tr/java/onenote-notebook-operations/convert-notebook-to-flattened-pdf/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote Defterinden PDF Düzleştirme – Aspose.Note

## Giriş

OneNote defterlerinden oluşturulan **flatten PDF** dosyalarına ihtiyacınız varsa, bu öğretici Aspose.Note for Java kullanarak tam adımları size gösterecek. OneNote defterini düzleştirilmiş bir PDF’ye dönüştürmek, etkileşimli öğeler olmadan orijinal düzeni koruyan statik, baskıya hazır bir belge istediğinizde yaygın bir gereksinimdir. Ortamı kurmaktan `NotebookPdfSaveOptions` yapılandırmasına kadar her şeyi kapsayacağız, böylece ortaya çıkan PDF tamamen düzleştirilmiş olur.

## Hızlı Yanıtlar
- **“flatten PDF” nedir?** Tüm etkileşimli öğeleri (notlar, katmanlar) tek bir statik sayfada birleştiren bir PDF oluşturur.
- **Dönüştürmeyi hangi kütüphane yönetir?** Aspose.Note for Java, yerleşik PDF kaydetme seçeneklerini kullanır.
- **Lisans gerekli mi?** Değerlendirme için ücretsiz deneme çalışır; üretim için ticari lisans gerekir.
- **Defterleri toplu olarak dönüştürebilir miyim?** Evet – aynı kodla birden fazla `.onetoc2` dosyasını döngüye alabilirsiniz.
- **Çıktı gerçekten düzleştirilmiş mi?** `flatten` değerini `true` olarak ayarlamak, etkileşimsiz bir PDF garantiler.

## Ön Koşullar

Kodun içine girmeden önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – herhangi bir güncel sürüm (8 veya üzeri) kurulu ve yapılandırılmış.
2. **Aspose.Note for Java kütüphanesi** – [buradan](https://releases.aspose.com/note/java/) indirin.
3. **Bir IDE** – IntelliJ IDEA, Eclipse veya tercih ettiğiniz herhangi bir editör.
4. **Bir OneNote defteri** (`.onetoc2` dosyası) – dışa aktarmak istediğiniz dosya.

## Paketleri İçe Aktar

Defter işleme ve PDF dışa aktarma için gerekli sınıfları içe aktarın.

```java
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import java.io.IOException;
```

## Adım 1: OneNote Defterini Yükle

Dönüştürmek istediğiniz defteri yükleyin. Yer tutucu yolu, `.onetoc2` dosyanızın gerçek konumuyla değiştirin.

```java
String dataDir = "Your Document Directory";
Notebook notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Adım 2: Dönüştürme Seçeneklerini Ayarla

PDF kaydetme seçeneklerini yapılandırın. `flatten` değerini `true` olarak ayarlamak, çıktı PDF’nin düzleştirilmesini sağlar. İşte **aspose pdf save options** burada devreye girer.

```java
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
notebookSaveOptions.setFlatten(true);
```

## Adım 3: Defteri Düzleştirilmiş PDF Olarak Kaydet

Çıktı dosya adını tanımlayın ve yapılandırdığımız seçeneklerle `save` metodunu çağırın.

```java
dataDir = dataDir + "ExportNotebookToPDFAsFlattened_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Neden Önemlidir

PDF’yi düzleştirmek, belgeyi orijinal OneNote uygulamasına sahip olmayan kullanıcılarla paylaşmanız gerektiğinde veya baskı, arşivleme ya da yasal uyumluluk için sabit bir düzen gerektiğinde hayati öneme sahiptir. Aspose.Note’un `NotebookPdfSaveOptions` sınıfı, dışa aktarma sürecinde ince ayar yapmanıza olanak tanır ve **OneNote’u PDF’ye dönüştürmeyi** görsel bütünlüğü koruyarak basitleştirir.

## Yaygın Sorunlar ve Sorun Giderme

| Belirti | Muhtemel Neden | Çözüm |
|---------|----------------|------|
| PDF’de boş sayfalar | Defter doğru yüklenmemiş | `.onetoc2` dosyasının yolunu doğrulayın ve dosyanın bozuk olmadığından emin olun. |
| PDF düzleştirilmemiş | `setFlatten(true)` çağrılmamış | `NotebookPdfSaveOptions` örneğinin `save` metoduna geçirildiğini tekrar kontrol edin. |
| Büyük defterlerde bellek hatası | JVM yığını yetersiz | Uygulamayı çalıştırırken yığın boyutunu artırın (`-Xmx2g` veya daha yüksek). |

## Sıkça Sorulan Sorular

**S: Aspose.Note for Java farklı OneNote sürümleriyle uyumlu mu?**  
C: Evet, Aspose.Note for Java çeşitli OneNote sürümlerini destekler, böylece ortamlar arasında sorunsuz dönüşüm sağlar.

**S: PDF çıktısını Aspose.Note for Java ile özelleştirebilir miyim?**  
C: Kesinlikle. `NotebookPdfSaveOptions` aracılığıyla sayfa boyutu, kenar boşlukları, yazı tipleri ve diğer özellikleri ayarlayabilirsiniz.

**S: Aspose.Note for Java defterlerin toplu dönüşümünü destekliyor mu?**  
C: Evet, birden fazla defter dosyasını döngüye alabilir ve aynı kaydetme seçeneklerini her birine uygulayabilirsiniz.

**S: Aspose.Note for Java için deneme sürümü mevcut mu?**  
C: Evet, Aspose.Note for Java’ın ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

**S: Aspose.Note for Java için destek nereden alınır?**  
C: Aspose.Note for Java ile ilgili destek ve yardımı [Aspose.Note forumunda](https://forum.aspose.com/c/note/28) bulabilirsiniz.

---

**Son Güncelleme:** 2025-12-28  
**Test Edilen Versiyon:** Aspose.Note for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}