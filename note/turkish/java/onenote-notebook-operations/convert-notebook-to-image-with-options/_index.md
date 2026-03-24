---
date: 2026-03-24
description: Aspose.Note for Java kullanarak OneNote'u PNG olarak seçeneklerle kaydetmeyi
  öğrenin. Bu kılavuz, OneNote'u görüntü olarak dışa aktarmayı, Java'da görüntü çözünürlüğünü
  ayarlamayı ve OneNote'u programlı olarak görüntüye dönüştürmeyi gösterir.
linktitle: Convert Notebook to Image with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote'u PNG Olarak Seçeneklerle Kaydet – Aspose.Note Kullanarak Defteri Görsele
  Dönüştür
url: /tr/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote’u PNG Olarak Kaydetme ve Seçenekler – Not Defterini Görsele Dönüştürme

## Giriş

Bu öğreticide **OneNote’u PNG olarak kaydetme** işlemini, Aspose.Note for Java kullanarak görüntü ayarları üzerinde tam kontrol sağlayarak öğreneceksiniz. Raporlama, küçük resim oluşturma veya arşivleme amacıyla OneNote’u görsele aktarmanız gerektiğinde, aşağıdaki adımlar **görüntü çözünürlüğünü Java‑stilinde ayarlayarak** net sonuçlar elde etmenizi sağlayacak.

## Hızlı Yanıtlar
- **Görüntü formatını seçebilir miyim?** Evet – `SaveFormat`ı değiştirerek PNG, JPEG, BMP vb. formatlarda dışa aktarabilirsiniz.
- **Görüntü kalitesini nasıl kontrol ederim?** DPI değerini (ör. 400 dpi) tanımlamak için `ImageSaveOptions.setResolution()` metodunu kullanın.
- **Üretim ortamında lisansa ihtiyacım var mı?** Deneme dışı kullanım için ticari bir lisans gereklidir.
- **API Java 8+ ile uyumlu mu?** Kesinlikle, Aspose.Note Java 8 ve üzeri sürümleri destekler.
- **Birden fazla not defterini toplu işleyebilir miyim?** Evet – not defterleri üzerinde döngü kurarak aynı kaydetme seçeneklerini uygulayabilirsiniz.

## “save onenote as png” nedir?
OneNote’u PNG olarak kaydetmek, tüm not defterini (veya belirli bölümleri) raster görüntülere dönüştürmek anlamına gelir. PNG kayıpsızdır, bu da notların, çizimlerin ve gömülü medyanın görsel bütünlüğünü korumak için idealdir.

## Neden seçeneklerle OneNote’u görsele dışa aktaralım?
OneNote’u görsele dışa aktarmak, OneNote yüklü olmayan kullanıcılarla içeriği paylaşmanızı, notları web sayfalarına gömmenizi veya yüksek çözünürlüklü PDF’ler oluşturmanızı sağlar. Aspose.Note ile **OneNote’u görsele dönüştürürken** çözünürlük, renk derinliği ve çıktı formatını Java kodundan özelleştirebilirsiniz.

## Önkoşullar

1. Makinenizde Java Development Kit (JDK) yüklü olmalı.  
2. Aspose.Note for Java JAR dosyaları. Kütüphaneyi [buradan](https://releases.aspose.com/note/java/) indirin ve projenizin classpath’ine ekleyin.

## Paketleri İçe Aktarma

İhtiyacımız olan sınıfları içe aktaralım:

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Adım‑Adım Kılavuz

### Adım 1: Not Defterini Yükleyin
Dönüştürmek istediğiniz OneNote not defterini yükleyin.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

### Adım 2: Kaydetme Seçeneklerini Ayarlayın
`NotebookImageSaveOptions` örneği oluşturun, format olarak PNG seçin ve **görüntü çözünürlüğünü Java‑stilinde ayarlayın**.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

### Adım 3: Not Defterini Görsel Olarak Kaydedin
Çıktı yolunu belirleyin ve `save` metodunu çağırın. Bu işlem **OneNote’u PNG olarak kaydeder** ve belirttiğiniz çözünürlüğü uygular.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Yaygın Sorunlar ve İpuçları

- **Çözünürlük uygulanmadı:** Çözünürlüğü ayarlamadan önce `getDocumentSaveOptions()` metodunu çağırdığınızdan emin olun; aksi takdirde varsayılan DPI kullanılır.  
- **Dosya bulunamadı:** `dataDir` değişkeninin doğru klasöre işaret ettiğini ve `test.onetoc2` dosyasının mevcut olduğunu kontrol edin.  
- **Büyük not defterleri:** Çok büyük not defterleri için JVM heap boyutunu (`-Xmx`) artırarak `OutOfMemoryError` hatasından kaçının.

## Sonuç

Artık **OneNote’u PNG olarak kaydetme** ve özel seçeneklerle **OneNote’u görsele dışa aktarma** konularını biliyorsunuz. Bu kod parçacıklarını Java uygulamalarınıza entegre ederek not defteri işleme otomasyonu, küçük resim üretimi veya mükemmel görsel kaliteye sahip arşiv kopyaları oluşturabilirsiniz.

## SSS

### S1: Aspose.Note karmaşık OneNote dosyalarını işleyebilir mi?
C1: Evet, Aspose.Note karmaşık OneNote dosyalarını verimli bir şekilde işleyebilir ve programatik olarak çeşitli işlemler yapmanıza olanak tanır.

### S2: Aspose.Note for Java mevcut projelere kolayca entegre edilebilir mi?
C2: Kesinlikle! Aspose.Note for Java, Java projelerinize sorunsuz bir şekilde entegre edilebilen basit bir API sunar, zaman ve çaba tasarrufu sağlar.

### S3: Not Defteri dönüştürürken görüntü çıktısını özelleştirebilir miyim?
C3: Evet, Aspose.Note çözünürlük, format ve diğer ayarları belirterek görüntü çıktısını özelleştirmenize izin verir.

### S4: Aspose.Note geliştiricilere destek sağlıyor mu?
C4: Evet, Aspose geliştiricilere forumları ve kapsamlı dokümantasyonu aracılığıyla mükemmel destek sunar, entegrasyon ve sorun giderme süreçlerini kolaylaştırır.

### S5: Aspose.Note for Java için ücretsiz deneme mevcut mu?
C5: Evet, [buradan](https://releases.aspose.com/) Aspose.Note for Java ücretsiz deneme sürümüne ulaşabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-03-24  
**Test Edilen Versiyon:** Aspose.Note for Java (en son)  
**Yazar:** Aspose  

---