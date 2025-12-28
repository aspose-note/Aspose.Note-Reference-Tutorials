---
date: 2025-12-28
description: Aspose.Note kullanarak Java'da **OneNote'u görüntüye dönüştürmeyi** ve
  görüntü çözünürlüğünü ayarlamayı öğrenin. Bu adım adım kılavuz, OneNote PNG dosyalarını
  dışa aktarmayı da gösterir.
linktitle: Convert OneNote to Image with Options - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'u Görsele Dönüştürme Seçenekleri - Aspose.Note
url: /tr/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote'u Görüntüye Dönüştürme ve Seçenekler - Aspose.Note

## Giriş

Bu öğreticide, Aspose.Note for Java kullanarak **OneNote'u görüntüye dönüştürmeyi** çeşitli seçeneklerle nasıl yapacağınızı öğreneceksiniz. Raporlama için yüksek çözünürlüklü bir PNG ya da hızlı bir JPEG küçük resmi ihtiyacınız olsun, aşağıdaki adımlar tam olarak nasıl yapılacağını ve bu sürecin Java uygulamalarınıza nasıl entegre edileceğini gösterir.

## Hızlı Yanıtlar
- **“OneNote'u görüntüye dönüştürmek” ne anlama geliyor?** Bir OneNote defterinin tamamını raster görüntü dosyalarına (PNG, JPEG vb.) dönüştürür.
- **Kayıpsız kalite için hangi format önerilir?** PNG, çünkü sıkıştırma artefaktları olmadan tüm detayları korur.
- **Java’da görüntü çözünürlüğünü nasıl ayarlarım?** `NotebookImageSaveOptions` üzerinden `ImageSaveOptions.setResolution(int dpi)` kullanın.
- **OneNote defterini tek adımda PNG olarak dışa aktarabilir miyim?** Evet, Aspose.Note uygun seçeneklerle tek bir `save` çağrısı sağlar.
- **Üretim kullanımında lisansa ihtiyacım var mı?** Üretim için ticari bir lisans gereklidir; değerlendirme için ücretsiz bir deneme sürümü mevcuttur.

## “OneNote'u görüntüye dönüştürmek” ne demektir?
Bir OneNote defterini görüntüye dönüştürmek, defterdeki her sayfayı bitmap dosyası olarak render etmek anlamına gelir. Bu, statik ön izlemeler oluşturmak, içeriği arşivlemek veya orijinal OneNote formatının desteklenmediği raporlara defter sayfalarını gömmek için faydalıdır.

## Neden Aspose.Note for Java?
- **Çıktı formatı, çözünürlük ve renk derinliği üzerinde tam kontrol** sağlar.  
- **Microsoft Office bağımlılığı yok** – herhangi bir sunucu‑tarafı Java ortamında çalışır.  
- **Gömülü dosyalar, kalem ve zengin metin içeren karmaşık defterleri** destekler.

## Önkoşullar

1. **Java Development Kit (JDK)** – sürüm 8 veya üzeri.  
2. **Aspose.Note for Java JAR dosyaları** – en yeni kütüphaneyi [buradan](https://releases.aspose.com/note/java/) indirip projenizin sınıf yoluna ekleyin.  

## Paketleri İçe Aktarma

İlk olarak, defteri yüklemek ve görüntü çıktısını yapılandırmak için ihtiyacımız olan sınıfları içe aktaralım.

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Adım 1: Defteri Yükleme

Dönüştürmek istediğiniz OneNote defterini yükleyin. `.onetoc2` dosyanızın konumunu yolu ile değiştirin.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## Adım 2: Kaydetme Seçeneklerini Ayarlama (**set image resolution java**)

Bir `NotebookImageSaveOptions` örneği oluşturun, çıktı formatını seçin ve istediğiniz çözünürlüğü belirtin. Bu örnekte PNG ve 400 dpi kullanıyoruz.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

> **Pro ipucu:** Büyük defterlerde daha hızlı işleme için çözünürlüğü düşürün (ör. 150 dpi). Baskı‑hazır grafikler için çözünürlüğü artırın.

## Adım 3: Defteri Görüntü Olarak Kaydetme (**export OneNote PNG**)

Çıktı dosya adını tanımlayın ve `save` metodunu çağırın. Aynı seçenekler defterdeki her sayfaya uygulanır.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

Yukarıdaki kod, belirttiğiniz çözünürlükte bir PNG dosyası (veya sayfa başına bir PNG dosyası serisi) oluşturur.

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **OutOfMemoryError** büyük defterlerde | JVM yığın boyutunu artırın (`-Xmx2g`) veya çözünürlüğü azaltın. |
| **Çıktıda boş sayfalar** | Defterin şifre korumalı olmadığından emin olun; gerekirse `Notebook.load(path, password)` kullanın. |
| **Desteklenmeyen görüntü formatı** | Sadece `SaveFormat.Png`, `SaveFormat.Jpeg` veya `SaveFormat.Bmp` kullanın – diğer formatlar defter dışa aktarımı için desteklenmez. |

## Sık Sorulan Sorular

**S: Aspose.Note karmaşık OneNote dosyalarını işleyebilir mi?**  
C: Evet, gömülü dosyalar, kalem açıklamaları ve zengin biçimlendirme içeren defterleri verimli bir şekilde işler.

**S: Aspose.Note for Java mevcut projelere kolayca entegre edilebilir mi?**  
C: Kesinlikle. API basittir ve sadece JAR dosyasını sınıf yolunuza eklemeniz yeterlidir.

**S: Bir Defteri dönüştürürken görüntü çıktısını özelleştirebilir miyim?**  
C: Evet. `ImageSaveOptions` aracılığıyla çözünürlük, format ve hatta renk derinliğini ayarlayabilirsiniz.

**S: Aspose.Note geliştiricilere destek sağlıyor mu?**  
C: Evet. Aspose kapsamlı dokümantasyon, forumlar ve hızlı yanıt veren destek kanalları sunar.

**S: Aspose.Note for Java için ücretsiz bir deneme sürümü var mı?**  
C: Evet, deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.

---

**Son Güncelleme:** 2025-12-28  
**Test Edilen Sürüm:** Aspose.Note 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}